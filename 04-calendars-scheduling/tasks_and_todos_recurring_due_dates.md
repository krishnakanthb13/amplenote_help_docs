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

## Weekday and Weekend Limiting

Use slash commands `/weekday` or `/weekend` within recurring tasks to restrict occurrence:

- **Weekdays**: Monday through Friday
- **Weekends**: Saturday and Sunday

Flexible tasks automatically adjust: weekend tasks shift to Saturday if completion falls on a weekday, and weekday tasks shift to Monday if completion falls on a weekend.

## Limiting Recurrence Instances

Control how many times tasks repeat using the "Start At" field:

- `every day until [date]` — repeats until specified date
- `every day for [number] times` — repeats exact number of times

The `until` keyword requires a date; the `for` keyword requires a number representing total repetitions.
