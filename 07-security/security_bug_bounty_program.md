# Amplenote Security Bug Bounty Program

> [← Help Index](../00-index.md) · Category: [Security](./index.md) · [Source ↗](https://www.amplenote.com/help/security_bug_bounty_program)

Amplenote invites reports of genuine security vulnerabilities affecting Amplenote or its users, with bounties available for verified issues. Submissions should be sent to `support@amplenote.com`.

## What Qualifies for a Bounty

Reports must meet all of these criteria:

- Describe an actual security vulnerability
- Include sufficient detail for testing
- Be reproducible
- Affect Amplenote production systems or user data
- Be submitted in good faith through responsible disclosure

The company reviews each case individually; submission does not guarantee payment.

## What Does Not Qualify

The program excludes reports that cannot be reproduced.

## Reward Decisions

Bounty amounts depend on severity, impact, exploitation difficulty, user/data risk, and whether the report accurately described the issue. All payments are discretionary.

## Resolved Reports

All reports are published on this page after they are resolved. Resolved reports are listed with a date, a link to the disclosure, and an outcome marker (✅ fixed, ☑️ partially addressed, ❌ not a vulnerability). The log currently includes entries through October 2026, such as:

- ❌ 10/19/2026 — Missing X-Permitted-Cross-Domain-Policies HTTP Response Header
- ❌ 09/17/2026 — CSRF Allows an Attacker to Force an Authenticated User's Subscription to the Personal Plan
- ❌ 09/15/2026 — Account Takeover via Malicious PDF
- ❌ 09/14/2026 — High severity stored XSS in Amplenote affecting all users
- ❌ 08/05/2026 — Pre-Account Takeover Allows Attacker-Controlled 2FA Setup and Account Lockout
- ✅ 08/13/2026 — Missing rate limit for old password field

See the [live page](https://www.amplenote.com/help/security_bug_bounty_program) for the complete, linked list.

## Responsible Disclosure Rules

Researchers must:

- Limit data access to what proves the issue
- Avoid service disruption
- Withhold public disclosure until fixes are deployed
- Allow reasonable investigation time

Violations may eliminate payment and future eligibility.

## Legal Boundaries

This program does not give permission to break the law, violate terms of service, or test systems outside scope. All testing requires legal and ethical compliance.
