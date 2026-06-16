# Code block & colored block text formatting

> [← Help Index](../00-index.md) · Category: [Notes & Writing](./index.md) · [Source ↗](https://www.amplenote.com/help/code_block_colored_block_text_formatting)

## Creating code blocks

Amplenote provides a built-in code editor accessible by clicking the "Code block" icon in Notes view or typing triple backticks (```` ``` ````) on a new line. The triple backtick method works across Jots, Notes, Tasks, Calendar mode, and Rich Footnotes.

![The "Code block" icon in the formatting toolbar](https://images.amplenote.com/a97c2516-f9ba-11ed-bb5d-46cd9704ac56/7f58bffc-b7d1-4d5f-9fac-ca5a4e6687b2.png)

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

![The copy icon in the upper right of a code block](https://images.amplenote.com/a97c2516-f9ba-11ed-bb5d-46cd9704ac56/e5e6fc8d-de01-4e13-8233-6489dabebbc6.png)

## Extending code blocks

Press Enter twice normally to exit a code block. To add multiple blank lines, hold Shift while pressing Enter.

## Styled block text (rainbow gradients)

Five gradient options available:

1. **Rainbow1:** Top-to-bottom blue and gray gradient
2. **Rainbow2:** Top-to-bottom orange palette gradient
3. **Rainbow3:** Left-to-right green-to-blue gradient
4. **Rainbow4:** 45-degree angle orange-and-blue gradient
5. **Rainbow5:** Animating gradient (processor-intensive)

![Rainbow1 styled block text: top-to-bottom blue and gray gradient](https://images.amplenote.com/a97c2516-f9ba-11ed-bb5d-46cd9704ac56/824d5570-a3fd-489a-8d99-cf38bd588cfd.png)

![Rainbow2 styled block text: top-to-bottom orange palette gradient](https://images.amplenote.com/a97c2516-f9ba-11ed-bb5d-46cd9704ac56/cf2e6c73-3c77-43c5-b1ae-b305beb9bb2c.png)

Usage: Enter the rainbow keyword on the first line, then add text. The keyword can be removed after implementation.
