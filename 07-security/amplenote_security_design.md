# How are my Amplenote notes secured?

> [← Help Index](../00-index.md) · Category: [Security](./index.md) · [Source ↗](https://www.amplenote.com/help/amplenote_security_design)

## Amplenote Security Design

This document describes the technical security systems protecting the Amplenote API, covering client-server interactions but not client-application-specific protections.

## Account Access

Users must authenticate, authorize client access, and receive encryption keys to decrypt note data.

### Authentication

- Login occurs at https://login.amplenote.com
- Passwords use BCrypt using a cost parameter of 10
- Cookies are Secure, HttpOnly, and domain-restricted
- Security headers implemented (CSP, HSTS, X-Frame-Options)

### Authorization

- OAuth2 authorization code flow with access tokens
- Tokens expire after 2 hours with refresh token support
- Supports OpenID Connect `nonce` parameter and PKCE

### Encryption Key Delivery

- Standard Key delivered upon authorization completion
- The Standard Key and Vault Key Salt are included in the OpenID Connect `id_token` JWT payload
- `id_token` is a JWT signed with the server's private key, and publicly verifiable with the corresponding public key
- The encrypted Note Key is delivered to the client in the `Encryption-Key` response header for any request that responds with encrypted note data. Since the header value is the encrypted Note Key, clients may cache the response in less secure storage.

## Note Encryption

Notes use AES-256-CBC with a Note Key, encrypted with either Standard or Vault Keys. Standard Keys are encrypted at rest with AES-256-GCM using database-inaccessible keys. Vault Keys never reach Amplenote servers.

### Encryption Key Storage

- Unique Initialization Vector per user-note combination
- Database storage encrypted with block-level AES-256
- Standard Key stored encrypted with an inaccessible encryption key
- Vault Key Salt: 256-bit random value using PBKDF2-HMAC-SHA256 with 100,000 rounds

### Sharing

The source user's Standard Key decrypts the Note Key, then the target user's Standard Key re-encrypts it with a new Initialization Vector.

### Public Notes

The Note Key is encrypted with a server-inaccessible key; the server decrypts and delivers decrypted content to viewers.

### Vault Notes

Disables sharing and public links; uses zero-knowledge verification to ensure consistent Vault Password usage.

### Changing a Standard Note to a Vault Note

When a Standard Note is converted to a Vault Note:

1. The client requests the Vault Note Key setup parameters. The server returns the *Vault Key Challenge* plus two random *Initialization Vector*s.
2. The client encrypts the challenge with AES-256-CBC using the *Vault Key*, producing the *Vault Key Response*. On repeat conversions, the previously used challenge IV is returned (only the first conversion generates it).
3. The server BCrypt-hashes the *Vault Key Response* and concatenates the IV to produce the *Vault Key Verifier*, stored AES-256-GCM-encrypted.
4. The server then replaces the stored *Standard Note Key* with the *Vault Note Key*.

## Appendix: End-to-End Encryption

Standard Notes are not end-to-end encrypted by default, enabling features like sharing and password reset. All notes encrypt before leaving devices and remain encrypted at rest.

## Appendix: Attachments

Attachments are unencrypted, stored at locations identifiable by a random 122-bit number and note identifier, creating 5,316,911,983,139,663,491,615,228,241,121,378,304 possible addresses. This remains true even in *Vault Notes*. A more likely risk than address guessing is accidental disclosure of the attachment address; encrypted attachments are on the roadmap for *Vault Notes*, with feasibility for *Standard Notes* to be evaluated at that point.

## Glossary Terms Defined

- *Initialization Vector*: Initialization Vectors used for AES-256-CBC encryption are 128-bit (16 bytes), while those used for AES-256-GCM are 96-bit (12 bytes).
- *Note Key*: 256-bit key used to encrypt a note.
- *Standard Key*: 256-bit key used to encrypt Note Keys for Standard Notes; delivered in the `id_token`.
- *Vault Key*: Derived from the Vault Password; never reaches Amplenote servers.
- *Vault Password*: User-chosen password protecting Vault Notes.
- *Vault Key Challenge*: Randomly generated 128-bit value used to verify Vault Key consistency.
- *Vault Key Response*: The challenge encrypted with the Vault Key.
- *Vault Key Salt*: 256-bit random value used with PBKDF2-HMAC-SHA256 and 100,000 rounds.
- *Vault Key Verifier*: BCrypt hash of the Vault Key Response concatenated with the challenge IV, stored AES-256-GCM-encrypted.
- *Standard Note Key*: The per-note key encrypted with the Standard Key, using a randomly generated 128-bit Initialization Vector.
- *Vault Note Key*: The per-note key encrypted with the Vault Key.
- *Vault Notes*: End-to-end encrypted notes whose keys never reach Amplenote servers.
