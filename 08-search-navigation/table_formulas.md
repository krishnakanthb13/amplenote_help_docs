# Working with table formulas

> [← Help Index](../00-index.md) · Category: [Search, Lookup & Navigation](./index.md) · [Source ↗](https://www.amplenote.com/help/table_formulas)

## Overview

Amplenote allows users to perform calculations on table cells. The formulas follow a simplified syntax designed to avoid the complexity of traditional spreadsheet applications.

## Specifying a Range

The basic formula structure is:

```
= operation([optional number of cells] [direction])
```

Valid examples include:

- `= sum(5 right)` — adds the five cells to the right
- `= mode(above)` — finds the most common value above
- `= median(3 below)` — calculates median of three cells below

## Transitive Operations Not Supported

Currently, if a range includes a formula cell, that formula's result is ignored in calculations. This limitation exists because "most spreadsheets allow aggregating formulas" but Amplenote avoids this complexity until range specification becomes more sophisticated.

The rationale acknowledges that users often want to apply multiple operations to single datasets without needing to specify which columns to exclude from calculations.

## Supported Operations

- **average/mean** — (Sum of values) / (Count of values)
- **max** — Greatest value in range
- **median** — Middle value; for even-numbered sets, the average of two middle values
- **min** — Lowest value in range
- **mode** — Most frequently occurring value
- **product** — Multiply all values together
- **sum** — Add all values

## Automatic Result Formatting

The system infers formatting based on input values:

- **Currency symbols** ($, €) are preserved in results
- **Numeric separators** follow user input conventions
- **Decimal precision** matches input (maximum three digits)

Users can suggest additional formulas through the feature voting board.
