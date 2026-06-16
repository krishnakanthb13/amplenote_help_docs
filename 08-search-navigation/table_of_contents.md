# Inserting a Table of Contents

> [← Help Index](../00-index.md) · Category: [Search, Lookup & Navigation](./index.md) · [Source ↗](https://www.amplenote.com/help/table_of_contents)

## Calculation & Evaluation Operator: Dates, Time, Math, and Table of Contents via {}

Amplenote enables calculation of relative dates and mathematical formulas by enclosing expressions in curly braces. For example, entering `{1+1}` produces a calculated result stored in a Rich Footnote.

## Date & Time Calculations

Date calculation pairs well with double-bracket syntax to link to notes named for future days, visible in Jots mode when that day arrives.

**Important:** Type the closing `}` bracket manually to trigger expression evaluation.

### Date Calculation

Useful for:

- Setting start dates via the `Start at` option in Task Details
- Creating daily jots (past or future)
- Creating time stamps within notes

**Relative dates:**

- `{Today}`
- `{Tomorrow}`
- `{Yesterday}`

**Absolute dates:**

- `{Monday}`
- `{The weekend}`
- `{September}`
- `{October 31st}`
- `{Oct 31}`
- `{End of March}`
- `{Beginning of April}`
- `{First monday of September}`
- `{Last friday of December}`

**Past and future dates:**

- `{Next monday}`
- `{Last week}`
- `{Next year}`
- `{In 14 days}`
- `{A month ago}`
- `{End of next month}`

### Time Calculation

- `{Now}`
- `{10 minutes ago}`
- `{In three hours}`
- `{9 pm}`
- `{21:30}`

**Date and time combined:**

- `{Today at 8pm}`
- `{Tomorrow at 10:45}`
- `{Tuesday 22:00}`
- `{Mar 12 8am}`

### Date Calculation: Defining Recurring Rules

These expressions work in the `Start at` field for task recurrence, not within curly brackets:

- Every 2 days
- Every 3 weeks
- Every 3 weeks on Friday
- Every week on Monday and Thursday
- Every weekday
- Every 2 months
- Every 3 months on the 21st
- Every month on the 20th and 25th
- Every month on the last Friday
- Every month on the last day
- Every 2 months on the first Monday
- Every 2 years

## Math Calculations

Examples: `{1+1}`, `{pi*10**2}`, `{(1+1)*(12/36)}`

## Table of Contents

Paying subscribers can insert a table of contents using `{toc}`, which generates a hierarchical list of all sections within a note.

**Note:** Changing note headings requires manual regeneration of the table of contents. Automatic updating is planned for future versions.
