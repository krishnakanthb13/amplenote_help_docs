# Linking tasks: Block, Mirror, Implement Goal, and basic connections

> [← Help Index](../00-index.md) · Category: [Tasks & Todo Lists](./index.md) · [Source ↗](https://www.amplenote.com/help/task_dependencies_block_task_implement_goal_task_mirror_or_connect_task)

## Task Dependencies: Linking Tasks with "Block," "Mirror," "Implement Goal" connected tasks for CEO-level powers

## Overview

Task Linking is available to Pro-level subscribers and above. As of December 2024, Amplenote enables users to connect tasks together to execute complex strategies for scheduling and arranging todo lists.

## Four Types of Task Links

### 1. "Implement Goal" Task Link 🏆
Connects tasks where the value assigned to big-time goal tasks supplies "energy" to channel attention to bite-sized implementation tasks that carry out the ultimate goal.

### 2. "Block" Task Link 🛑
Stops guessing about task duration hiding. Link tasks when one blocks another. The blocked task automatically stops cluttering your todo list until its prerequisite is complete. Multiple blockers will hide a task until all are done.

### 3. "Mirror" (Follow-on) Task Link 👯‍♂️
A versatile link that triggers action when the link-holding task finishes. Allows constructing "super tasks" that automatically resolve a cascade of other tasks upon completion.

### 4. "Connect" Basic Task Link 🖇️
A basic task connection facilitating jumping between related tasks or visualizing them in graph view.

## Creating a Task Link

Task links are created similarly to note links using double brackets (`[[`) or `@`. To switch from note lookup to task lookup, add a `-` after the opening characters (`[[-` or `@-`). This prompts you for the type of task link to create.

**Searching Options:**

- Using `@-` immediately after the opening character searches tasks across all existing notes
- Indicating a note name before pressing `-` narrows the search to that specific note

![Calling up the Task Link menu by entering `@-` while in a task](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/20c9387d-083a-465a-b669-69b64d6eed58.png)

![Looking up a task from any note by creating Task Link with `@-`](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/a3fccb08-e1bf-48e2-ab0f-33c1f5f0ed3c.png)

![Creating a new Task Link to a task within the note that begins with 'quarter'](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/6953963a-e204-4f32-8422-9d6278a5cb8e.gif)

## "Implement Goal Task" Link Details

This link type steers long-term achievers toward tasks implementing their current goals. It works with planning strategies like maintaining "Monthly Plan" or "Quarterly Plan" notes.

![Initiating creation of an Implement Goal Task link](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/f86bcf54-df1d-4a41-bf93-79b9a1c5e417.png)

![Choose the Goal Task being implemented by this Implementation Task](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/1883c393-7ea8-418c-b6a8-c9dd9f049063.png)

![Viewing the created 'Implement Goal' link](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/3ada0ecc-2070-49b4-8f25-dbbbd22f5ee0.png)

**How It Works:**
Every day you open a note containing an Implementation Task, Amplenote evaluates the Task Score that would be assigned to the Goal Task based on its attributes (Important, Urgent, etc.). This score is split evenly among all Implementation Tasks linking to it.

**Example:**
Create a "Q1 Goals" note with task "Finish building the ark." Apply Important, Urgent, and "90+ minutes" attributes. Implementation Tasks receive their normal Task Score plus extra points inherited from the Goal Task each day the note opens.

**Advanced Example:**
If a single Implementation Task advances multiple monthly goals, create links to all Goal Tasks. The Implementation Task receives boosted Task Score daily, ensuring top-of-mind visibility in Tasks or Calendar Pane.

**Reset Option:**
Use `!reset` Task Command to zero-out Task Score without hiding the task. It takes 2-3 days to re-accumulate enough score to top the recommended task list.

## "Block Task" Link Details

Automatically removes tasks from your todo list until prerequisites are complete. In long-term lists, approximately 25% of tasks sit idle waiting for other tasks to finish.

![Creating a new Block Task link to hide a task until its prerequisite task is complete](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/ce65b009-5c2e-4425-a588-82b8d6d3965f.gif)

**How It Works:**
Creating a "Block Task" link maintains a connection from the Blocking Task to the Blocked Task. When the Blocking Task is completed, dismissed, or deleted—or when the link is deleted—the Blocked Task unhides from the note's "Hidden Tasks" tab, unless other tasks block it.

**Multiple Prerequisites:**
A task can have multiple blocking tasks. It unhides only when all Blocking Tasks are completed, deleted, or dismissed.

**Creating from Blocked Task:**
Type `!blocked` while in a Blocked Task to trigger a Task Action letting you pick which task blocks it. A "Block Task" link is added from the blocking task back to your current task, which then moves to the "Hidden" tab.

## "Mirror Task" Link Details

Places a copy of the original task into a selected note. Mirror Task links enable evolved task sharing from multiple contexts.

![Creating a Mirror Task link to a new note](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/11dc9a48-f06f-4e18-bd69-954d83a1111d.gif)

**Key Concepts:**

- **Mirrored Task:** A task linked to by a Mirror Task link
- **Mirror Trigger Task:** A task containing a Mirror Task link

**Cascading Effect:**
If Task A creates a Mirror Task link to Task B, then Task A is a Mirror Trigger Task that marks Task B complete upon completion. If Task B links to Task C, Task C also marks complete. This creates powerful cascading possibilities.

### Use Case 1: "Lead Domino" Tasks
Also called "super tasks," these complete multiple related tasks automatically. Example: "Fix the kitchen sink" as a Mirror Trigger Task linked to "Contact Pete about plumbing" and "Contact Jim about plumbing." Completing the super task removes the mirrored tasks automatically.

### Use Case 2: Sharing Task Responsibility
Multiple people might complete a task. Each mirrored instance can be modified independently without disturbing other versions, allowing different team members to adjust task text or add subtasks.

### Use Case 3: Daily Planning Mix-and-Match
Create Mirror Task links in your daily/weekly plan note to ensure original tasks mark complete only when finished in the plan note. Visit important todo lists in the morning and mirror original tasks into your daily plan.

### Re-syncing Mirrored Tasks
Mirrored tasks stay in sync for completion or dismissal actions, but can contain different content. Use `/overwrite` command to refresh all task copies to match current content.

![Re-syncing mirrored tasks with the /overwrite command](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/58e051c9-fadc-42e6-ae2d-6bc16e3ce49d.png)

## "Connect Task" Link Details

Creates vanilla connections between tasks without side effects, useful for remembering related tasks or navigating webs of related tasks. Enables visualization in Graph View (planned for later). Plugins could use this functionality in interesting ways.

![Creating a basic Connect Task link](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/862aa84a-a580-4a4b-add6-763d285cdd11.gif)

![When Task B met Task A](https://images.amplenote.com/4f020c68-b41c-11ef-b4ea-e972ef1cda6a/2a5da9fe-c25d-4735-a1fc-0804763cf8e6.png)

## Task Links with Recurring Tasks

Each recurring task instance has a unique identifier, so linking to a recurring task only links to the current version. If you link from a recurring task, the link removes itself if it would cause a loop. Connect links should function fine. Report undesirable behavior to customer support or product roadmap boards.

## Comparison with Other Apps

For CEO-level todo makers, these advanced features significantly influence which "daily driver" app to trust for task management. A blog post compares advanced todo features available on Amplenote, Todoist, and TickTick platforms.
