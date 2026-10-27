# qr-code-generator — Fast, print-ready QR codes from the CLI

> Generate QR codes for any text or URL instantly using the pre-installed `qrencode` CLI. PNG, SVG, or terminal output with full control over size, margin, and error correction.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
qr-code-generator wraps the `qrencode` CLI to produce scannable QR codes in multiple formats. Control module size, margin, and error correction to suit any use case — from a quick on-screen scan to a high-resolution print job. No additional installs needed; `qrencode` is pre-installed.

## Features
- **Output formats** — PNG, SVG, UTF8 (terminal), ANSI (`-t`)
- **Size control** — pixels per module via `-s` (8–12 for print)
- **Margin** — quiet-zone modules via `-m` (2 recommended)
- **Error correction** — L (7%) / M (15%) / Q (25%) / H (30%) via `-l`

## Usage / Quick Start
```bash
# Basic PNG
qrencode -o output.png -s 10 -m 2 "https://example.com"

# High quality for print
qrencode -o print.png -s 12 -m 2 -l H "https://example.com"

# SVG (scalable)
qrencode -t SVG -o output.svg -m 2 "https://example.com"

# Terminal preview
qrencode -t UTF8 "https://example.com"
```

## Trigger Keywords (OpenClaw)
qr code, QR, mã QR, tạo mã, barcode, scan code

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
