# Markly – Markdown ↔ Figma Text Layers

A Figma plugin for seamless conversion between Markdown and Figma text layers. Easily paste Markdown as styled layers, copy selected text layers as Markdown, or map Markdown syntax to your local text styles.

## Features

- **Convert from Markdown:** Paste or type Markdown and instantly generate styled Figma text layers
- **Copy as Markdown:** Select Figma text layers and export them as Markdown, ready to share elsewhere
- **Style Mapping:** Map Markdown elements to your local Figma text styles for consistent, branded imports
- **Live Preview:** See a rendered HTML preview of your Markdown input as you type
- **Theme Support:** Automatically adapts to your Figma theme (light or dark mode)
- **Smart Font Handling:** Automatically loads required fonts with fallbacks for reliable text rendering

## Supported Markdown Syntax

| Feature | Support | Notes |
|---------|---------|-------|
| Headings | ✅ | `# H1`, `## H2`, `### H3` |
| Paragraphs | ✅ | Regular text lines |
| Lists (Unordered) | ✅ | `- Item` or `* Item` |
| Lists (Ordered) | ✅ | `1. Item`, `2. Item`, etc. |
| Links | ✅ | `[Link Text](https://example.com)` |
| Bold/Italic | ✅ | `**bold**`, `*italic*` |
| Code blocks | ⚠️ | Visible in preview only |
| Blockquotes | ⚠️ | Visible in preview only |
| Tables | ⚠️ | Visible in preview only |

## Installation

### Development Build

1. Clone or download this repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. If using TypeScript, compile the code:
   ```bash
   npm run build
   ```
4. In Figma desktop app:
   - Go to Plugins → Development → Import plugin from manifest...
   - Select the `manifest.json` from this directory

## Usage

### Convert from Markdown

1. Select a text layer with Markdown or open the plugin UI
2. Paste your Markdown content in the text area
3. Map elements to text styles (optional)
4. Click "Convert from Input"
5. The plugin creates styled text layers on your canvas

### Copy as Markdown

1. Select one or more text layers
2. Run "Copy as Markdown" from the plugin menu
3. Use the copy button or Ctrl+C/Cmd+C to copy the generated Markdown

### Style Mapping

1. Open the full UI from "Match Styles ↔ Markdown"
2. Select local text styles for each Markdown element
3. Preview how your content will look
4. Convert when satisfied

## File Structure

├── code.js         # Main Figma plugin logic
├── ui.html         # Plugin UI with theme support and preview
├── manifest.json   # Plugin configuration
├── README.md       # Documentation

Clipboard Limitations

Due to Figma and browser security restrictions, direct clipboard copy can only occur via a user action in the UI.

For "Copy as Markdown," you must manually copy the text from the UI dialog—simply click the "Copy" button or use Ctrl+C/Cmd+C.

Development & Customization

Tailwind CSS and Google Fonts are included in the plugin UI via CDN for rapid UI development.

The UI supports both light and dark themes using Figma's injected class and CSS variables.

Easily extend Markdown support or add more mapping controls as needed.

## Technical Notes

- Uses marked.js for Markdown preview rendering
- Built with Tailwind CSS for responsive UI
- Supports both light and dark Figma themes
- Handles clipboard operations respecting browser security constraints

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve the plugin.

## License

MIT

---

Built with ❤️ for the Figma community