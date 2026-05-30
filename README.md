# Booklet Imposition Tool

A lightweight, client-side only web application that takes a standard PDF and automatically rearranges the pages ("imposition") so they can be printed double-sided on landscape A4 sheets, folded in half, and bound into an A5 booklet.

## Features
- **Client-Side Only:** No server required. PDF processing happens entirely in the browser using `pdf-lib` and `pdf.js`.
- **Animated Preview:** Visually verify the print spreads and folds before printing.
- **Smart Page Numbering:** Add page numbers to the exported PDF with customizable start pages and offset values.

## How to Format Your Input PDF
Your input document should be completely standard. Do **not** try to pre-format it for a booklet:
* **Page Size:** Standard Portrait (e.g., A4).
* **Order:** Normal reading order (Page 1, Page 2, Page 3...).
* **No Manual Blank Pages:** The tool automatically calculates and adds the necessary blank pages at the end to ensure the total page count is perfectly divisible by 4 (a physical requirement for folded booklets).
* **No page numbers required:** It's a pain in wWrd, the tool is more reliable.

## Printing
When printing the exported PDF, select:
- **Double-sided printing** (Duplex)
- **Flip on short edge** (Short-edge binding)
- **Landscape orientation** (usually auto-detected)
