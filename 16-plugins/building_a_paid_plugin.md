# Building a paid Amplenote plugin

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/building_a_paid_plugin)

## Overview

Amplenote has built infrastructure that allows a plugin to charge a monthly fee for use, like Agent Pro (the AI plugin) does. This article describes how a developer can build a plugin to be monetized through [Amplenote's plugin directory](https://amplenote.com/plugins).

## Code requirements for paid plugins

In order to preserve Amplenote's core values of transparency and security, any potential plugin must be audited on the following prior to being released as a paid plugin.

### 1. Code visible

Read access to the source Github repos must be granted to the `amplenote-team` user on Github.

### 2. AI audited

Copy the code from the provided **Copy/pasteable review prompt**, and run it from the root of the plugin's source repository using a code-capable AI agent that can inspect every file. The exact executable artifact submitted to Amplenote must also be present in the repository or identified to the agent.

Commit both generated files without deleting findings or changing their conclusions:

- `AMPLENOTE_PLUGIN_SECURITY_REVIEW_[month]_[year].md`
- `amplenote-plugin-data-practices-[month]-[year].json`

You may add developer responses beneath findings, but you may not remove the original finding. Resolve all Blocker findings before submission. The review must be regenerated for every month that a new published plugin version is released.

Amplenote may independently regenerate the review, compare it with your submitted review, and reject a plugin whose source, built artifact, disclosures, or review do not agree.

### 3. Elective work

The more ideas you have to help users believe that their data is going to be private, the higher your conversion rate is going to be among users. You are encouraged to think about other safeguards you can show to prove to customers that they can trust you with their data.

## Other requirements for paid plugins

### 4. Refund rate below 5%

Amplenote does not have a streamlined process to handle refunds for paid plugins, so they need to work with plugins that can clearly set expectations for their users, such that they are not inclined to contact support to request a refund.

### 5. Offer an evaluation version

During this beta phase of development, it is not possible to offer a single plugin that works initially before allowing the user to consummate a purchase. Thus, authors are requested to release a free version of their plugin that customers can use to evaluate the functionality and substantiate that they will be satisfied with their purchase.

## Revenue share

Amplenote offers 70% of the revenue Amplenote collects for a plugin back to the developer. It will be paid net 60 days, after handling any refunds or chargebacks that may originate from the payment processing.

Developers are encouraged to propose the price for their plugin at hello@amplenote.com, where they will collaborate to choose a final price that can maximize user purchases.

## Related

- [Published Plugins Directory](./published_plugins_directory.md) — the community plugin directory
- [Guide to Building Plugins](../15-extending-amplenote/guide_to_developing_amplenote_plugins.md) — creating plugins from beginner to advanced
