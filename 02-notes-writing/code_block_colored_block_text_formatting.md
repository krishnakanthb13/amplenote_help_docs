# Code block & colored block text formatting

> [← Help Index](../00-index.md) · Category: [Notes & Writing](./index.md) · [Source ↗](https://www.amplenote.com/help/code_block_colored_block_text_formatting)

## Creating code blocks

Amplenote provides a built-in code editor accessible by clicking the "Code block" icon in Notes view or typing triple backticks (```` ``` ````) on a new line. The triple backtick method works across Jots, Notes, Tasks, Calendar mode, and Rich Footnotes.

## Code block editor (built-in IDE)

Amplenote's code editor uses CodeMirror, the same text editor found in Chrome Dev Tools, Obsidian.md, CodePen, Adobe Brackets, Firefox Developer Tools, and jsfiddle.

**Example code block structure:**

- Constants (defaultSystemPrompt, pluginName, etc.)
- insertText functions (lolz, code, complete, lookup, sum)
- noteOption functions (revise, summarize)

The language specification on the first line can be removed without affecting syntax coloring.

## Supported languages

The editor supports syntax highlighting and bracket matching for:

- Javascript
- C, C++, C#
- CSS, SCSS
- HTML (with embedded Javascript/CSS)
- Python
- Ruby
- Rust
- XML
- Plain

Language tokens are case-insensitive. Users can specify language by mentioning it in the first line (e.g., `# python` or `// C`).

## Code-editing features

- **Automatic bracket/element closing:** Creates closing brackets and HTML elements automatically.
- **Automatic language detection:** Recognizes language from functional signatures.
- **Syntax highlighting:** Highlights related symbols and elements.
- **Tab depth retention:** Maintains indentation within functions/methods.
- **Formatting in published notes:** Colored syntax persists for public viewers.
- **Copy function:** Icon in upper right copies entire code block.

## Extending code blocks

Press Enter twice normally to exit a code block. To add multiple blank lines, hold Shift while pressing Enter.

## Styled block text (rainbow gradients)

Five gradient options available:

1. **Rainbow1:** Top-to-bottom blue and gray gradient
2. **Rainbow2:** Top-to-bottom orange palette gradient
3. **Rainbow3:** Left-to-right green-to-blue gradient
4. **Rainbow4:** 45-degree angle orange-and-blue gradient
5. **Rainbow5:** Animating gradient (processor-intensive)

Usage: Enter the rainbow keyword on the first line, then add text. The keyword can be removed after implementation.
