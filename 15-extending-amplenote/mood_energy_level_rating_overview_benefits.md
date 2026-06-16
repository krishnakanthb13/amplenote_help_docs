# Mood Rating Overview

> [← Help Index](../00-index.md) · Category: [Extending Amplenote](./index.md) · [Source ↗](https://www.amplenote.com/help/mood_energy_level_rating_overview_benefits)

## Overview

Amplenote offers all users the ability to track daily mood and energy levels. The feature targets logic-driven business users by framing mood tracking as data collection for productivity optimization. As the article notes, "what gets measured gets improved" motivates users to establish an "energy compass" for decision-making.

!["Completed Task Stats" utilize ratings (orange line) to contextualize experience](https://images.amplenote.com/3fbec732-e760-11f0-9cf5-33c83009c142/5a9060b6-fb48-40f2-8d9f-f8cf46734b85.png)

## What Gets Measured?

The popup captures either mood or energy level—whichever users find easier to estimate. The two concepts correlate heavily, so the distinction remains flexible based on individual preference.

![Capturing energy level/mood is never far in desktop or mobile](https://images.amplenote.com/3fbec732-e760-11f0-9cf5-33c83009c142/ca90746f-c4de-40b1-99cb-003496702e72.gif)

## Benefits

Regular tracking (morning and/or evening) can reveal patterns about high-performing days. The article references [Jim Collins on Tim Ferriss](https://active-recall.com/podcast-notes-jim-collins-on-rating-your-days-tim-ferriss-show/) and the [Cal Newport podcast](https://www.amplenote.com/help/victory_value_guide_intuition_toward_elevated_mood) as sources documenting these benefits.

Real-world data may show counterintuitive patterns—for example, highest productivity sometimes inversely correlates with mood. Users can export mood data to examine trends or feed information to LLMs for pattern recognition.

![Highest Victory Value (productivity)? Purely opposite to high mood](https://images.amplenote.com/3fbec732-e760-11f0-9cf5-33c83009c142/0e0df018-4f3a-4824-a7a5-92bc5749c1db.png)

## Data Security & Export

Mood ratings receive identical encryption treatment as note content: encrypted client-side, in transit, and at rest. Full details appear in [Amplenote's security documentation](https://www.amplenote.com/help/amplenote_security_design).

Exported data includes a `data/mood-ratings.json` file containing note references, numeric ratings, timestamps, and UUIDs.
