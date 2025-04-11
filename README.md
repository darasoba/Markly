# Paste from Markdown - Figma Plugin

## Description

This Figma plugin allows users to convert Markdown-formatted text into styled, rich text layers within Figma. It streamlines the workflow for designers who draft content in Markdown (using tools like Notion, Obsidian, or plain text editors) and need to bring it into Figma designs efficiently.

The plugin provides a simple UI where users can paste or type Markdown text, see a live preview, map Markdown elements (like headings, paragraphs, list items) to existing Figma text styles, and then generate corresponding text layers on the Figma canvas.

## Features

*   **Markdown Input:** Accepts standard Markdown syntax in a text area.
*   **Live Preview:** Displays an HTML preview of the formatted Markdown in real-time using `marked.js`.
*   **Figma Text Style Mapping:** Allows users to select local Figma text styles to apply to H1, H2, H3, Paragraphs, and List Items. Falls back to default styling if no style is mapped.
*   **Layer Creation:** Generates individual Figma text layers for each parsed Markdown block (headings, paragraphs, list items, standalone links).
*   **Basic Styling Fallbacks:** Applies default font sizes for unmapped headings and attempts to use a bold font weight for all headers (H1, H2, H3).
*   **Robust Font Handling:** Attempts to load required fonts (from styles or defaults) and falls back to common system fonts if necessary, providing notifications for missing fonts.
*   **Error Handling:** Displays messages in the UI and Figma notifications for issues like empty input, font loading failures, or style fetching problems.

## Supported Markdown Syntax (Current)

*   Headings: `# H1`, `## H2`, `### H3`
*   Paragraphs: Regular text lines.
*   Unordered Lists: `- List item` or `* List item`
*   Ordered Lists: `1. List item` (Basic numbering applied)
*   Standalone Links: `[Link Text](https://example.com)` (Displayed as a text layer, URL added to layer name)
*   *Note: Inline formatting like **bold** or *italic* is visible in the preview but not yet applied as rich text segments within Figma layers.*

## Setup & Installation

1.  **Clone or Download:** Get the plugin code onto your local machine.
2.  **Install Dependencies:** Open a terminal in the project directory and run:
    ```bash
    npm install
    ```
    This installs TypeScript and Figma plugin typings.
3.  **Build the Plugin:** Compile the TypeScript code into JavaScript:
    ```bash
    npm run build
    ```
    Alternatively, use `npm run watch` to automatically recompile when you save changes to `code.ts`. This will generate the `code.js` file required by Figma.
4.  **Add to Figma:**
    *   Open Figma (desktop app recommended).
    *   Go to Plugins > Development > Import plugin from manifest...
    *   Navigate to the project directory and select the `manifest.json` file.
    *   The plugin "Paste as Markdown" should now appear in your Development plugins list.

## How to Use

1.  **Run the Plugin:** In Figma, go to Plugins > Development > Paste as Markdown.
2.  **Enter Markdown:** Type or paste your Markdown text into the text area.
3.  **Preview:** See the live HTML preview update as you type.
4.  **(Optional) Map Styles:** Use the dropdown menus to map Markdown elements (H1, P, etc.) to your desired local Figma text styles. Select "Default (No Style)" to use the plugin's default formatting.
5.  **Convert:** Click the "Convert" button.
6.  **Result:** The plugin will create new text layers on your current Figma page, positioned near the center of your viewport, styled according to your mappings or the defaults.

## File Structure
