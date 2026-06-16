# Victory Value & the "Good Life Algorithm"

> [← Help Index](../00-index.md) · Category: [Concepts & Terminology](./index.md) · [Source ↗](https://www.amplenote.com/help/victory_value_guide_intuition_toward_elevated_mood)

## Overview

Victory Value quantifies progress toward an ideal life by measuring not just task completion, but overall well-being improvement. The system combines completed tasks with mood tracking to help users identify which activities correlate with happiness and life satisfaction.

## Core Concept

The "Good Life Algorithm," coined by Cal Newport, draws inspiration from author Jim Collins's daily tracking method. Collins uses a -2 to +2 rating system to evaluate each day, then analyzes patterns: "what's going on in all of the +2 days?" versus "-2 days?" This iterative approach, comparable to the Simplex Method in operations research, enables progression toward optimal living without knowing the destination beforehand.

## Victory Value Components

**1. Base Completion**
Every finished task earns one Victory Value point.

**2. Marked Important**
Tasks flagged as important contribute 7 additional points, reflecting alignment with long-term goals.

**3. Longer Duration**
Time investment is calculated using the formula `Math.max(0, ln(minutes)-1)`:

- 1-2 minute tasks: 0 extra value
- 30-minute task: 2.4 points
- 60-minute task: 3.1 points
- 24-hour task: 6.2 points

**4. Enjoyable/Satisfying**
Mood ratings submitted near task completion boost Victory Value:

- Within 0-30 minutes: mood rating multiplied by 2
- Within 30-90 minutes: mood rating added directly
- Daily average mood applied to all that day's tasks

**5. High Leverage**
"Lead domino" tasks that preclude other tasks receive bonus points proportional to obsoleted work.

**6. Tag Multiplier**
Users can assign Victory Value multipliers to priority tags (Unlimited subscribers only). The highest multiplier applies when multiple tags exist.

**7. Unblocked Value**
Completing tasks that unblock others adds 1 point per unblocked task.

## Dismissed Tasks

Dismissed tasks calculate Victory Value but divide it by half, philosophically supporting the ability to "let go" of initially promising but ultimately unnecessary work.

## Manual Adjustment

Users can manually override calculated Victory Value for completed tasks based on retrospective judgment of actual value.

## Mood Tracking Integration

Amplenote emphasizes pairing productivity metrics with emotional satisfaction. The platform provides first-class mood tracking across desktop and mobile apps, making the connection between task completion and well-being immediately visible in completed task statistics.

## Sources of Inspiration

The concept draws from:

- Jim Collins (author, *Good to Great*) – original daily tracking methodology
- Tim Ferriss podcast interview with Collins (Episode 361)
- Cal Newport's "Good Life Algorithm" discussion (Deep Life podcast, Episode 342)

Collins describes ideal days as containing focused creative work interspersed with meaningful relationships and self-care—emphasizing that "the very best days don't have much in them at all."
