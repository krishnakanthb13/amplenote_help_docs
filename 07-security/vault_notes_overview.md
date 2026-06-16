# What are Vault Notes and how do I create them?

> [← Help Index](../00-index.md) · Category: [Security](./index.md) · [Source ↗](https://www.amplenote.com/help/vault_notes_overview)

## Introduction

Vault Notes are end-to-end encrypted, with their encryption password never sent to Amplenote's servers. This design ensures that even with database access, decryption would be impossible within a human lifetime using advanced computing resources.

## Accessing Vault Notes

Vault Notes are exclusive to the Amplenote Unlimited Subscription tier.

## What is a Vault Note?

A Vault Note uses a Vault Encryption Key never available to Amplenote's database server. The technical implementation includes:

- A random 256-bit Vault Key Salt generated and stored encrypted with AES-256-GCM
- PBKDF2-HMAC-SHA256 key derivation using 100,000 rounds
- A Vault Key Verifier stored on servers for zero-knowledge password verification

## How Vault Notes Look/Act

**Visual designation:** Vault Notes display with a blue icon when pending decryption upon session start.

**Functional limitations:**

- Cannot be shared or made public
- Preview content never displays
- Content won't match in searches (titles do match)
- Not included in notebook exports
- Best navigated via tags and hierarchy

## Creating a Vault Note

1. Click the note settings icon in the note header.
2. Select "Apply Vault encryption."
3. Enter your vault password.
4. Check the acknowledgment box confirming password loss means permanent data loss.
5. Click "Secure note."

**Critical warning:** "The content of this note cannot be recovered if you forget your secure password." Password storage in a password manager (1Password, Bitwarden) is strongly recommended.

## Offline Availability

Vault Notes work offline after initial content download, provided the vault password is supplied when prompted.

## Removing Vault Encryption

Click "Remove Vault encryption" and enter your vault password to convert a Vault Note back to a standard note.
