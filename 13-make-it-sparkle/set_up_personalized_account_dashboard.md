# Setting up an account dashboard (Mission Control Dashboard)

> [← Help Index](../00-index.md) · Category: [Make it Sparkle](./index.md) · [Source ↗](https://www.amplenote.com/help/set_up_personalized_account_dashboard)

Amplenote enables users to customize a dashboard that tracks activity across your account. The dashboard operates through plugins capable of rendering embeds, such as the Overview Dashboard plugin.

## Enabling an Amplenote Dashboard

New Amplenote accounts have the Dashboard enabled by default. If you registered your account before 2026, activate it by:
1. Installing a plugin that supports dashboards
2. Clicking the "Notes" pane
3. Clicking "Customize" in your dashboard area

This displays a list of installed plugins capable of rendering a dashboard. The Overview Dashboard plugin, developed by Amplenote, is expected to reach full v1 by late March 2026. The plugin was created using Cursor and Claude Code, allowing further enhancement through AI tools.

## Dashboard Components

**🌎 Task Domain Selection**
Most dashboard widgets filter notes and tasks based on your selected Task Domain from the top bar. If you haven't configured a Task Domain, instructions and video guides are available. By default, the "Work" task domain includes any note that has a `todo` tag applied. Tag hierarchies such as `todo/project-a` and `todo/project-b/writing` are recommended for separating projects.

**📜 Quarterly/Monthly/Weekly Planning**
The Planning widget displays your quarterly plan by default, inspired by Deep Work methodology. Your plan informs DreamTask suggestions and Task Trash functionality. When the Task Trash widget is enabled (coming March 2026), your quarterly plan is used to pick out which tasks you might be able to retire. Setting the Planning widget to two cells tall displays your weekly plan below your monthly plan.

**🧙 Proposed Agenda**
Considers all tasks in your Task Domain and proposes which fit today. You can choose a different priority or change the AI provider for a different opinion.

**🏆 Victory Value vs Energy Level**
This component tracks completed task value alongside optional mood ratings (-2 to +2). Cal Newport advocates rating each day in real time to identify patterns across your optimal circumstances over time. The mood overlay can optionally be disabled, and ratings also appear in Victory Value.

**🔮 Goal Coach**
Combining your Task Domain with quarterly goals and current day context, Goal Coach suggests tasks you could complete today (the suggestions it generates are called DreamTask). If you've added an LLM key to the Dashboard Settings and some details to your Quarterly Plan, DreamTask has suggestions. Larger widget sizes generate more suggestions, and past suggestions are tracked to avoid repetition within a week. Click a task to navigate to it, or create it within the note that has the most tasks.

**🏃 Habits by Energy Impact**
Uses flexible recurring tasks/habits to compute how each habit affects your daily energy ("Energy Delta per Habit"), including how many times each habit was completed in the past year.

**👬 Shared Notes**
Shows recently updated shared notes, lets you pin a note to follow up later, and filter by collaborator. Any collaborator with a note updated in the past year is shown in the filter.

**🗒️ Day Sketcher**
This drag-and-drop scheduler auto-populates with scheduled tasks and events from Amplenote or third-party connected calendars, allowing you to sketch your day outline. Use tab and shift-tab to navigate between hours of the day. Your sketch is saved to a note for persistence and historical reference. External events are coming soon.

**🕰️ Revisit Candidates**
This widget identifies notes with languishing tasks, offering opportunities to resume past projects within your Task Domain. By early Q2 2026, it will keep a history of past suggestions to ensure maximum variety from day to day.

**🎭 Satisfaction/Contentment Meter**
This component helps balance productivity with enjoyment, allowing you to record daily mood ratings (-2 to +2) via emoji selection. Use the "Configure" link at the bottom of the component to toggle between visualizations; changing the calendar date refreshes the ratings.

**⏰ Peak Hours**
Visualizes when completed tasks were created or finished within a given month, showing which hours yielded maximum creative energy.

**📆 Calendar**
Acts as the control center for other widgets. Selecting different weeks or months displays historic data from completed tasks. Past days are colored by completion volume; future days by scheduled volume.

**📋 Task Agenda**
Displays scheduled tasks for your selected date. By early Q2 2026, this will also show external calendar events.

**💡 Inspiration Quotes**
Provides 100 quotes and ideas to encourage forward progress.

**🏃 Quick Actions**
Enables visiting random notes, jumping to your daily journal, and other shortcuts.

## Dashboard Settings

**⚙️ Settings**
Control your dashboard background and select your preferred LLM provider for generating task suggestions from your Quarterly Plan.

## Reordering & Resizing Components

**⤴️ Layout Options**
Two methods exist for reordering widgets:
- Click "Layout" in the upper right and drag components
- Click a widget header for two seconds until it shakes, then drag to reposition

The "Sizing" tab within Layout controls widget dimensions. The "Components" tab allows moving widgets to a "Hidden" section if they lack sufficient value. When developers add new components, they often begin life in the "Hidden" section, so check Layout periodically for new widgets.

## Mobile Dashboard

Currently in progress as of March 2026. Access via Quick Open by selecting "Overview Dashboard (full)" to view the dashboard in your left pop-out menu. By late April 2026, mobile access will be available directly above "Notes."
