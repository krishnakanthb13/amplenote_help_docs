# Tables

> [← Help Index](../00-index.md) · Category: [Notes & Writing](./index.md) · [Source ↗](https://www.amplenote.com/help/tables)

## How do I create a table in Amplenote?

To insert a table, use the formatting toolbar button available on both web and mobile platforms.

Within the web app, the fastest method involves pressing the `Tab` key.

Upon creation, tables contain a single cell. To expand, position your cursor inside and use the formatting bar to add additional columns or rows.

**Insertion behavior:**

- New columns append to the left of the current cell.
- New rows insert above the current cell.

## Table manipulation using the keyboard

| Action | Windows | macOS | Conditions |
|--------|---------|-------|-----------|
| Delete a row | `Enter` | `Enter` | While on the last row, if empty |
| Delete a row/column | `Backspace` | `Backspace` | While on a full-row/full-column selection, if selection is empty and has no formatting |
| Delete cell contents | `Backspace` | `Backspace` | While on a cell selection |
| Delete/clear cell formatting | `Backspace` | `Backspace` | While on a cell selection, if selection is empty |
| Insert a row above | `Enter` | `Enter` | While in front of the first word, first column |
| Insert column to the right | `Tab` | `Tab` | While on the first row, last column |
| Insert row below | `Tab` | `Tab` | While on the last row, last column, when last row is not empty |
| Insert row below | `Enter` | `Enter` | While on the last row, if it's not empty |
| Move cursor a cell down | `Enter` | `Enter` | — |
| Move cursor a cell to the left | `Shift-Tab` | `Shift-Tab` | — |
| Move cursor a cell to the left | `Backspace` | `Backspace` | While in an empty cell |
| Move cursor a cell to the right | `Tab` | `Tab` | — |
| Move cursor to the first cell | `Ctrl-Left` | `Cmd-Left` | While at the edge of the cell |
| Move cursor to the last cell | `Ctrl-Right` | `Cmd-Right` | While at the edge of the cell |
| Rearrange column left | `Ctrl-Alt-Shift-Left` | `Cmd-Ctrl-Shift-Left` | — |
| Rearrange column right | `Ctrl-Alt-Shift-Right` | `Cmd-Ctrl-Shift-Right` | — |
| Rearrange row down | `Ctrl-Shift-Down` | `Cmd-Shift-Down` | — |
| Rearrange row up | `Ctrl-Shift-Up` | `Cmd-Shift-Up` | — |
| Select cell | `Esc` | `Esc` | While cell contents are selected |
| Select cell contents | `Esc` | `Esc` | — |
| Select current-to-first cell | `Ctrl-Shift-Left` | `Cmd-Shift-Left` | — |
| Select current-to-last cell | `Ctrl-Shift-Right` | `Cmd-Shift-Right` | — |

## Selecting cell ranges

Multiple cells can be selected using:

- **Shift + Arrow keys** (e.g., `Shift-Down` to select the current cell and the cell below).
- **Mouse cursor** by clicking and dragging across desired cells.
- **Table Cell Formatting Toolbar** buttons.
- **Hovering on exterior table borders** to select entire rows or columns.

### After selecting a cell range, you can:

- Apply text and cell formatting and styling.
- Remove cell contents, formatting, or entire rows/columns using `Backspace`.
- Copy cell information or paste new content.

**Note:** You can reorder rows and columns from any cell without selecting the entire range.

## Inserting media and other types of formatting inside tables

Tables support all standard formatting options for cell contents:

- **Bold** / *italics* / strikethrough / highlighting / `inline code`
- Headings
- Bullet lists with sub-bullets
- Numbered lists with sub-items
- Links and Rich Footnotes
- Images with captions and alignment
- Code blocks

Insert supported content using the formatting bar as you would outside tables.

## Table styling and formatting options

When selecting a cell or multiple cells, a formatting bar appears with additional options.

**Tip:** Press `Esc` twice while the cursor is inside a cell to easily select it.

### Formatting text inside table cells

Two table-specific text formatting options are available: alignment and font color.

#### Changing text alignment

Three alignment options:

- Text aligned to the **right**
- **Center**-aligned
- Text aligned to the **left**

#### Changing text font color

Choose from the existing palette or paste a custom HEX color code.

**Note:** Custom colors remain the same all the time, while the preset options adjust with light/dark mode changes.

### Styling and resizing table cells

Cells can be customized by:

- Adding or removing cell borders
- Changing column widths
- Applying background colors

#### Changing cell borders

Using the Cell Formatting Toolbar:

- **Click** an option to add that border.
- **Click** again to remove it.
- **Alt-Click** or **Opt-Click** to only add that border to the boundary of the current selection.

Example cell configurations shown include:

- Cells with no borders
- Cells with full borders
- Rows with borders on the outside
- Rows with full borders
- Cells with only top and bottom borders
- Cells with only left and right borders

#### Changing column widths

By default, columns extend to fit content on a single line.

To adjust width, hover the mouse pointer over vertical cell borders and drag to the desired width.

To reset column width (fitting content with no wrapping), use the button in the Table Formatting bar.

When multiple cells are selected, each column resizes to fit the widest cell from that column.

**Custom-width column rules:**

- Never resized automatically to fit on screen.
- When the screen is insufficient, the table becomes horizontally scrollable.
- When converting to a full-width table, only columns without custom widths extend to fit the screen.
- If no such columns exist, custom-width columns extend while maintaining relative sizes.

#### Full-width tables and scrollable tables

Toggle between left-aligned (default) and full-width tables using the button in the regular toolbar (not the floating Table Toolbar).

**Default table behavior:** The table is left-aligned with columns sized to content.

**Full-width table behavior:** Columns extend to cover the page width.

When converting to full-width:

- Columns without custom width extend to cover the page.
- Columns with custom width maintain their assigned dimensions.
- If all columns have custom widths, they resize while maintaining relative proportions.

#### Applying cell background colors

Cell background colors work like text font colors: custom colors persist regardless of light/dark mode, while preset colors adjust dynamically.

### Removing formatting from a cell

Use the "Clear cell formatting" icon in the Table Toolbar to remove text color, cell color, text alignment, and border additions.

## Smart column sorting

Amplenote detects table contents, deduces their type, and allows sorting in ascending/descending order.

**Action:** Press once to sort ascending, press again to sort descending.

**Automatic header detection:** Amplenote automatically identifies your header row if you:

- Apply a different background color.
- Apply a different font text color.
- Use a different data type in the header row.
- Include numbers in data rows.

## 📌 Use cases for tables

As of October 2022, formula support is planned for tables' next iteration.

**Current appropriate uses:**

- Organizing large sets of related data (employees, inventory, concert set lists).
- Creating an Index of your Amplenote notebook.
- Visualizing daily habits.

**Planned sections** (marked as "coming soon"):

- Use case: Creating an Index of your Amplenote notebook
- Use case: Visualizing daily habits
- Use case: A Dashboard/Homepage
