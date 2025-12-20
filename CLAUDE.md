# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal resume repository for Harsha Vardhan Yellela. It contains a single-page HTML resume and PDF exports.

## File Structure

- `resume.html` - Main resume document (self-contained HTML with embedded CSS)
- `*.pdf` - PDF exports for different purposes (e.g., MLE/SDE roles, specific companies)

## Working with the Resume

### Editing
The resume is a single HTML file with all styling inline in a `<style>` block. No build tools or dependencies are required.

### Generating PDFs
Open `resume.html` in a browser and use the browser's Print to PDF feature. The CSS includes print-specific styles (`@media print`) for proper rendering.

### Key CSS Considerations
- Uses `page-break-inside: avoid` to keep entries together when printing
- `page-break-before: always` is used to force page breaks between sections
- Table-layout CSS is used for header/subheader alignment (left content, right dates)
- User-select properties are carefully set to allow text copying while excluding bullet markers
