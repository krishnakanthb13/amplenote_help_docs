# Setting up an account dashboard

> [← Help Index](../00-index.md) · Category: [Make it Sparkle](./index.md) · [Source ↗](https://www.amplenote.com/help/set_up_personalized_account_dashboard)

Amplenote enables users to customize a dashboard that tracks activity across your account. The dashboard operates through plugins capable of rendering embeds, such as the Overview Dashboard plugin.

## Enabling an Amplenote Dashboard

To activate your dashboard:
1. Install a plugin that supports dashboards
2. Click the "Notes" pane
3. Click "Customize" in your dashboard area

This displays a list of installed plugins capable of rendering a dashboard. The Overview Dashboard plugin, developed by Amplenote, is expected to reach full v1 by late March 2026. The plugin was created using Cursor and Claude Code, allowing further enhancement through AI tools.

## Dashboard Components

**🌎 Task Domain Selection**
Most dashboard widgets filter notes and tasks based on your selected Task Domain from the top bar. If you haven't configured a Task Domain, instructions and video guides are available.

**📜 Quarterly/Monthly/Weekly Planning**
The Planning widget displays your quarterly plan by default, inspired by Deep Work methodology. Your plan informs DreamTask suggestions and future Task Trash functionality. Setting the Planning widget to two cells tall displays your weekly plan below your monthly plan.

**🏆 Victory Value vs Contentment**
This component tracks completed task value alongside optional mood ratings (-2 to +2). Cal Newport advocates rating each day in real time to identify patterns across your optimal circumstances over time.

**🔮 DreamTask**
Combining your Task Domain with quarterly goals and current day context, DreamTask suggests tasks you could complete today. Larger widget sizes generate more suggestions, and past suggestions are tracked to avoid repetition within a week.

**🗒️ Day Sketcher**
This drag-and-drop scheduler auto-populates with scheduled tasks and events, allowing you to sketch your day outline. Your sketch is saved to a note for persistence and historical reference.

**🕰️ Revisit Candidates**
This widget identifies notes with languishing tasks, offering opportunities to resume past projects within your Task Domain.

**🎭 Satisfaction/Contentment Meter**
This component helps balance productivity with enjoyment, allowing you to record daily mood ratings via emoji selection and toggle between visualization types.

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

The "Sizing" tab within Layout controls widget dimensions. The "Components" tab allows moving widgets to a "Hidden" section if they lack sufficient value.

## Mobile Dashboard

Currently in progress as of March 2026. Access via Quick Open by selecting "Overview Dashboard (full)" to view the dashboard in your left pop-out menu. By late April 2026, mobile access will be available directly above "Notes."
