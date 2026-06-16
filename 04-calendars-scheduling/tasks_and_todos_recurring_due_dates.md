# Recurring events and tasks: fixed and flexible options

> [← Help Index](../00-index.md) · Category: [Calendars & Scheduling](./index.md) · [Source ↗](https://www.amplenote.com/help/tasks_and_todos_recurring_due_dates)

## Overview

Amplenote supports two recurrence types: **fixed** and **flexible**. Fixed recurrence suits predictable events like meetings, while flexible recurrence (also called "relative recurrence") bases the next due date on task completion, making it ideal for activities like exercise or chores.

## Fixed Recurrence

Select from menu options or create custom schedules using natural language like "every" combined with numbers, days, or time intervals.

The interface displays:

- **Blue fields**: Define the recurrence rules
- **Non-blue fields**: Show when the next instance occurs

You can modify specific instances without changing the underlying rule.

![Fixed recurrence menu — blue fields define the rules, non-blue fields show the next instance](https://images.amplenote.com/cce04e4c-fad0-11ea-95c1-f200a12bf340/b027c773-947c-4b22-bcdf-37afe0a7c269.png)

### Advanced Weekly Recurrence

Tasks can repeat weekly on specific days. Examples include:

- Every weekday (Monday–Friday)
- Custom day patterns combining multiple weekdays

## Flexible ("Relative") Recurrence

Set up flexible recurrence by:

1. Opening Task Details
2. Choosing "When the task is complete" as the "Repeat" value
3. Entering a recurrence rule in the "Start at" menu
4. (Optional) Selecting a "Hide until" option to delay the task's reappearance

This approach allows tasks to reschedule based on actual completion rather than fixed intervals.

![Configuring flexible recurrence with the 'When the task is complete' repeat option in Task Details](https://images.amplenote.com/cce04e4c-fad0-11ea-95c1-f200a12bf340/8421fae5-ae29-4fbb-b64a-13cc0f2cb37e.gif)

## Weekday and Weekend Limiting

Use slash commands `/weekday` or `/weekend` within recurring tasks to restrict occurrence:

- **Weekdays**: Monday through Friday
- **Weekends**: Saturday and Sunday

Flexible tasks automatically adjust: weekend tasks shift to Saturday if completion falls on a weekday, and weekday tasks shift to Monday if completion falls on a weekend.

![Using the /weekday or /weekend slash commands to limit recurrence](https://images.amplenote.com/a33e980c-b5f0-11ef-9d1d-d7fedc24f425/42cd8eea-6e93-4b84-bccb-626614c127d8.png)

![Task Details configuration for weekday- or weekend-limited recurrence](https://images.amplenote.com/a33e980c-b5f0-11ef-9d1d-d7fedc24f425/9af384f7-a852-4d7a-a21f-4b7bbdd51f9f.png)

## Limiting Recurrence Instances

Control how many times tasks repeat using the "Start At" field:

- `every day until [date]` — repeats until specified date
- `every day for [number] times` — repeats exact number of times

The `until` keyword requires a date; the `for` keyword requires a number representing total repetitions.
