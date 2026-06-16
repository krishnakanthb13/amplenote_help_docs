# Batch updating Task Score based on goals or custom criteria

> [← Help Index](../00-index.md) · Category: [Make it Sparkle](./index.md) · [Source ↗](https://www.amplenote.com/help/agent_pro_task_scoring)

## Remind me why we are assigning scores to tasks again?

Amplenote's Task Score algorithm "automatically calculates a number" to suggest which tasks merit your attention. Since tasks from all notes appear together, prioritization becomes overwhelming. Task Score reduces this by assigning calculated numbers to each task.

The limitation: no universal formula exists for determining importance. The solution leverages LLMs—provide direction, and relevant tasks surface. "Rescore tasks every month, week, or even day" to keep your calendar focused on what matters now.

## Open Task Rescorer

Access Task Rescorer from a note via **Plugins menu** (after clicking the Note Options triple dot), or from the global "Open" dialog by typing "rescore" (requires Ample Agent Pro).

## Which tasks to score?

When invoked outside a note, you'll select your task source:

- **Everything**: All tasks
- **Task Domain**: Score valuable tasks from a chosen Task Domain
- **Tag**: Score tasks in notes containing the selected tag or child tags
- **Note**: Score tasks within a specific note

Up to 100 tasks per invocation are processed.

## Scoring tasks by enjoyability and more

Specify scoring criteria from these options:

- Your quarterly plan (Mission Control Dashboard)
- Most enjoyable tasks
- Fastest tasks
- Newest tasks
- Instructions from a note
- Ad hoc custom instructions

The LLM evaluates tasks in roughly 10 seconds.

## Finalizing new scores

Review recommended scores and click any value to adjust it. A score of 0 dismisses the task.
