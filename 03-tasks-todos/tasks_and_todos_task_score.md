# How does Task Score work?

> [← Help Index](../00-index.md) · Category: [Tasks & Todo Lists](./index.md) · [Source ↗](https://www.amplenote.com/help/tasks_and_todos_task_score)

> "Lindy cannot be fooled... The only effective judge of things is time."
> — Nicholas Taleb, An Expert Called Lindy

Task Score is Amplenote's proprietary algorithm designed to automatically sort your todo list by combining project context with multiple factors to help you determine what to schedule or dismiss next.

### Key Benefits

The system helps identify which tasks deserve your attention from potentially hundreds or thousands created over time, considering factors like whether a task could be completed in 15 minutes.

### On YouTube

Two video resources are available explaining Task Score functionality and how to visualize task importance and urgency.

### Core Concept

Task Score optimizes your decision-making about focus priorities by leveraging your past actions to produce a sorted task list relative to your current note or project context, supplemented by note tagging practices.

## Task Score Factors

Task Score derives from these elements:

1. **Note Opening Frequency** — Tasks accumulate score based on how many days their containing note has been opened.
2. **Urgent Status** — Marked urgent tasks increment aggressively daily, indicating harm prevention if not completed within days.
3. **Important Status** — Marked important tasks accumulate roughly 3x faster than unmarked tasks, reflecting alignment with short or long-term goals.
4. **Due Today** — Tasks due today receive 10 bonus points for higher list positioning.
5. **Duration Set** — Tasks with specified durations gain priority, especially those marked completable quickly.
6. **Blocking Other Tasks** — Tasks blocking others accumulate score from those dependencies.
7. **Deadline** — Tasks with deadlines earn 10 bonus points on and after the deadline date.

## Color Coding System

Task Score thresholds use color-coding:

- **Red** — 10+ Task Score
- **Gold** — 5+ Task Score
- **Blue** — 2+ Task Score
- **Gray** — 1+ Task Score

## How Task Score Changes Over Time

Task Score increases at different velocities depending on task attributes set during creation. The system's "magic" involves proportional increases aligned with project consideration frequency.

### Example Application

A note tagged `todo/amplenote` might contain low-priority plugin ideas unlikely to be worked on for months. Because Task Score accumulates only when notes open, tasks remain uncluttered in the Work Task Domain until the note receives regular attention, at which point associated tasks rapidly ascend priority.

## Editing Task Score

**Individual Tasks** — Click the Task Score number to enter a new value.

**Bulk Editing** — Use the per-note Task Score Adjustment option to modify all tasks within a note simultaneously, adjusting scores either as relative percentages or absolute value numbers.

## Productivity Estimation

Amplenote displays graphs showing completed tasks and Task Points by day and over longer periods, helping answer questions about:

- Most productive days of the week
- Long-term productivity growth trends
- Habits correlating to high-impact days

Details available on the Completed Tasks help page.
