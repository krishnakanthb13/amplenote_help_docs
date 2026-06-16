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
- Included in OpenID Connect `id_token` JWT payload
- Server-signed and publicly verifiable

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

## Appendix: End-to-End Encryption

Standard Notes are not end-to-end encrypted by default, enabling features like sharing and password reset. All notes encrypt before leaving devices and remain encrypted at rest.

## Appendix: Attachments

Attachments are unencrypted, stored at locations identifiable by a random 122-bit number and note identifier, creating 5.3 septillion possible addresses.

## Glossary Terms Defined

Initialization Vector, Note Key, Standard Key, Vault Key, Vault Password, Vault Key Challenge, Vault Key Response, Vault Key Salt, Vault Key Verifier, Standard Note Key, Vault Note Key, and Vault Notes.
