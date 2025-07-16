# QEMU 0.1.0 Linux User-Mode Emulator Slideshow

A comprehensive Quarto slideshow explaining QEMU 0.1.0 Linux user-mode emulation for undergraduate computer science students focusing on systems programming and security.

## Overview

This slideshow provides a deep dive into QEMU's user-mode emulator, covering:
- **Architecture internals** and binary translation
- **Security implications** and attack vectors
- **Performance analysis** and optimization strategies
- **Hands-on exercises** for practical learning

## Quick Start

### Installation

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

### Usage

1. **Render the slideshow:**
   ```bash
   quarto render qemu-slideshow.qmd
   ```

2. **Preview in browser:**
   ```bash
   quarto preview qemu-slideshow.qmd
   ```

3. **Export to PDF:**
   ```bash
   quarto render qemu-slideshow.qmd --to pdf
   ```

4. **Export to HTML:**
   ```bash
   quarto render qemu-slideshow.qmd --to html
   ```

## 📁 Files

- `qemu-slideshow.qmd` - Main slideshow file
- `custom.css` - Custom styling for the presentation
- `quarto-requirements.txt` - Required dependencies
- `original_markdown_slides.md` - Original content source

