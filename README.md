# Gemini Print & PDF Exporter

A simple Javascript bookmarklet to reformat the [Google Gemini web application](https://gemini.google.com/) for a clean print-to-PDF output.

## How It Works

The Gemini web application is not designed for printing. It uses multiple nested containers with fixed heights and hidden overflow properties, which causes content to be cut off when trying to print.

This bookmarklet injects a small CSS stylesheet into the page to fix these issues by:
1.  **Hiding UI Elements**: It removes non-essential interface components like the sidebar, input prompt, and action buttons.
2.  **Overriding Container Styles**: It forces every container in the content hierarchy to have a visible overflow and an automatic height, allowing the content to flow naturally across pages.
3.  **Resetting Content Height**: It specifically targets the main conversation container to unset the large `min-height` that Gemini's JavaScript adds, eliminating the blank page issue.

## Installation

You can install this tool as a bookmarklet in any modern web browser.

#### Chrome, Firefox, Edge, etc.

1.  Press `Ctrl+Shift+B` (or `Cmd+Shift+B` on Mac) to ensure your bookmarks bar is visible.
2.  Right-click the bookmarks bar and select **"Add page..."** or **"Add bookmark..."**.
3.  In the **Name** field, enter something memorable like `Print Gemini`.
4.  In the **URL** (or **Address**) field, copy and paste the entire Javascript code from the `gemini-print.js` file in this repository.
5.  Click **Save**. The bookmarklet will now appear on your bookmarks bar.

## Usage

1.  Open the Google Gemini conversation you wish to export.
2.  Click the `Print Gemini` bookmarklet you created. The page will instantly reformat.
3.  Press `Ctrl+P` (or `Cmd+P` on Mac) to open the print dialog.
4.  Select **"Save as PDF"** as the destination and click **Save**.

## License

This project is licensed under the [MIT License](LICENSE).
