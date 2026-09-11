# FITS Header Editor

> A fast, secure, browser-based tool to inspect, edit, add, and export astronomical **FITS** (`.fits`, `.fit`, `.fts`) header metadata directly on client-side.
>
> 🔗 **Online Tool**: [https://abctool.info/fits-header-editor-online/](https://abctool.info/fits-header-editor-online/)
>
> 🌐 **English** | [Español](README.es.md) | [中文](README.zh.md) | [日本語](README.ja.md)

---

## Overview

Traditionally, viewing and editing astronomical FITS metadata required installing heavyweight desktop software (such as SAOImage DS9, AstroImageJ, PixInsight) or running Python scripts with `astropy.io.fits`. 

**[FITS Header Editor Online](https://abctool.info/fits-header-editor-online/)** brings full FITS header viewing and editing capabilities directly into your web browser:
- **100% Client-Side & Private**: Files are parsed and processed purely inside your browser. No astronomical data is ever uploaded to any external server.
- **Zero Installation**: Works out of the box on any device (Windows, macOS, Linux, tablet) with a modern web browser.
- **Real-Time Header Editing**: Add, update, reorder, or delete 80-character standardized FITS cards in real time.
- **Export Flexibility**: Save and download modified `.fits` files instantly, or export metadata to JSON and TXT formats.

---

## How to Use

### 1. Load Your FITS File

Open [FITS Header Editor Online](https://abctool.info/fits-header-editor-online/). You will see the initial upload screen:

![FITS Header Editor Online - Upload Screen](./src/img/1-fits-header-viewer-editor.png)

- **Select or Drop File**: Drag and drop your `.fits`, `.fit`, or `.fts` file into the dashed box, or click **Select FITS File**.
- **Sample File**: Want to try it first? Click **Load Sample FITS** to load pre-configured astronomical sample data (`13838SgrA.fits`) with one click.

---

### 2. Inspect & Search Metadata

Once loaded, the full interactive header editor table appears:

![FITS Header Editor Online - Editor UI](./src/img/2-fits-header-editor-ui.png)

- **File Summary**: The top banner displays essential file info, including the file name, file size, total number of header cards, and HDU type (e.g., `Primary HDU`).
- **Instant Search**: Use the search input (`Search keywords, values, comments...`) to quickly locate specific cards by keyword name, value, or comment.
- **Category Filters**: Filter cards by standardized functional categories:
  - **All**: View all existing cards in order.
  - **Target & Coord**: Object names, RA/DEC coordinates, equinox, etc.
  - **Camera & Optics**: Exposure time, gain, filter name, focal length, pixel dimensions.
  - **WCS Coordinates**: Astrometric projection standards (CRVAL, CRPIX, CD matrix).
  - **Structural**: Standard FITS structural cards (SIMPLE, BITPIX, NAXIS, EXTEND).

---

### 3. Edit, Add, and Organize Keywords

The editor table offers full granular control over each card:

- **Edit Values & Types**: Update values with dedicated input widgets. Boolean values feature intuitive dropdown toggles (`T (True)` / `F (False)`), while strings and numeric values can be adjusted inline.
- **Quick Helpers**: Click commonly used astronomical shortcut buttons to immediately inject essential keywords:
  - `+ OBJECT` (Target name)
  - `+ EXPTIME` (Exposure time in seconds)
  - `+ FILTER` (Optical filter name)
  - `+ BAYERPAT` (Bayer color pattern)
  - `+ GAIN` (Sensor gain)
  - `+ FOCALLEN` (Telescope focal length)
  - `+ PIXSIZE` (Pixel physical size)
  - `+ OBSERVER` (Observer / Astrophotographer name)
- **Custom Keywords**: Click **+ Add Keyword** to create any custom FITS keyword card with custom types, values, and comments.
- **Reorder & Remove**: Use the up/down arrows (`↑`, `↓`) on the right to adjust card order, or click (`✕`) to delete unnecessary cards.
- **Reset**: Click **Reset** at any time to discard unsaved edits and restore the original file state.

---

### 4. Save & Export

When your edits are complete:
- **Save & Download FITS**: Click **Save & Download FITS** to repackage the updated header with the raw binary image data into a clean, compliant `.fits` file and download it to your device.
- **Export JSON**: Export all header cards as a structured JSON key-value document for scripting and automation.
- **Export TXT**: Export the clean standard text representation of the FITS header cards.

---

## Supported Formats & Compatibility

| Feature | Details |
| :--- | :--- |
| **Supported File Extensions** | `.fits`, `.fit`, `.fts` |
| **HDU Support** | Primary HDU & Standard Image Extensions |
| **Standard Compliance** | Standard 80-column FITS card format (NASA / IAU FITS standard) |
| **Security & Privacy** | 100% In-browser execution (WebAssembly / JavaScript); no cloud uploads |

---

## Visit Tool

👉 Launch tool directly in your browser: **[https://abctool.info/fits-header-editor-online/](https://abctool.info/fits-header-editor-online/)**


**[https://fits-kit.github.io/fits-header-editor/](https://fits-kit.github.io/fits-header-editor/)**
