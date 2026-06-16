# Mood Rating Overview

> [← Help Index](../00-index.md) · Category: [Extending Amplenote](./index.md) · [Source ↗](https://www.amplenote.com/help/mood_energy_level_rating_overview_benefits)

## Overview

Amplenote offers all users the ability to track daily mood and energy levels. The feature targets logic-driven business users by framing mood tracking as data collection for productivity optimization. As the article notes, "what gets measured gets improved" motivates users to establish an "energy compass" for decision-making.

## What Gets Measured?

The popup captures either mood or energy level—whichever users find easier to estimate. The two concepts correlate heavily, so the distinction remains flexible based on individual preference.

## Benefits

Regular tracking (morning and/or evening) can reveal patterns about high-performing days. The article references [Jim Collins on Tim Ferriss](https://active-recall.com/podcast-notes-jim-collins-on-rating-your-days-tim-ferriss-show/) and the [Cal Newport podcast](https://www.amplenote.com/help/victory_value_guide_intuition_toward_elevated_mood) as sources documenting these benefits.

Real-world data may show counterintuitive patterns—for example, highest productivity sometimes inversely correlates with mood. Users can export mood data to examine trends or feed information to LLMs for pattern recognition.

## Data Security & Export

Mood ratings receive identical encryption treatment as note content: encrypted client-side, in transit, and at rest. Full details appear in [Amplenote's security documentation](https://www.amplenote.com/help/amplenote_security_design).

Exported data includes a `data/mood-ratings.json` file containing note references, numeric ratings, timestamps, and UUIDs.
