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

## 🎯 Learning Objectives

After completing this slideshow, students will be able to:

1. **Understand** the difference between user-mode and system-mode emulation
2. **Analyze** security implications of cross-architecture execution
3. **Evaluate** performance trade-offs in binary translation
4. **Implement** basic syscall translation mechanisms
5. **Identify** potential attack vectors in emulation layers

## 🛠️ Hands-On Exercises

The slideshow includes practical exercises:

1. **Basic Emulation**: Run x86 programs on ARM systems
2. **Security Analysis**: Identify and analyze attack vectors
3. **Performance Profiling**: Measure emulation overhead

## 🔧 Development

### Editing the Slideshow

1. **Install Quarto extension for your editor:**
   - VS Code: Install "Quarto" extension
   - Vim/Neovim: Install quarto-vim plugin

2. **Live preview while editing:**
   ```bash
   quarto preview qemu-slideshow.qmd --watch-inputs
   ```

### Customization

- **Modify styling**: Edit `custom.css`
- **Add new slides**: Edit `qemu-slideshow.qmd`
- **Change theme**: Update YAML frontmatter in `.qmd` file

## 📊 Features

- **Interactive diagrams** using Mermaid
- **Syntax highlighting** for code blocks
- **Responsive design** for different screen sizes
- **Print-friendly** CSS for handouts
- **Chalkboard mode** for live annotations

## 🎓 Educational Context

Designed for undergraduate computer science courses covering:
- Systems programming
- Computer architecture
- Security engineering
- Virtualization technologies

## 🔍 Troubleshooting

### Common Issues

1. **Mermaid diagrams not rendering:**
   ```bash
   npm install -g @mermaid-js/mermaid-cli
   ```

2. **PDF export issues:**
   ```bash
   sudo apt-get install chromium-browser
   ```

3. **Font issues:**
   ```bash
   sudo apt-get install fonts-liberation
   ```

### Getting Help

- **Quarto documentation**: https://quarto.org/docs/
- **Mermaid documentation**: https://mermaid-js.github.io/
- **Course forum**: Check your course management system

## 📄 License

This educational material is provided under the MIT License for educational use.
