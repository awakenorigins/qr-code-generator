# QR Code Generator

Generate QR codes from text, URLs, or data. Outputs PNG, SVG, or terminal display.

## Triggers
- qr code, QR, mã QR, tạo mã, barcode, scan code

## Dependencies
- `qrencode` CLI (system package, already installed)

## Usage

### Generate QR code PNG:
```bash
qrencode -o output.png -s 10 -m 2 "https://example.com"
```

### Options:
- `-s <size>` — pixel size per module (default 3, recommend 8-12 for print)
- `-m <margin>` — margin in modules (default 4, recommend 2)
- `-l <level>` — error correction: L(7%), M(15%), Q(25%), H(30%)
- `-t <type>` — output type: PNG, SVG, UTF8, ANSI
- `-o <file>` — output file path

### High quality for print/ebook:
```bash
qrencode -o qr.png -s 12 -m 2 -l H "https://example.com"
```

### SVG output (scalable):
```bash
qrencode -o qr.svg -t SVG -m 2 "https://example.com"
```

### With custom colors (via ImageMagick post-process):
```bash
qrencode -o qr.png -s 12 "URL" 
convert qr.png -fill "#C9A96E" -opaque black qr-gold.png
```

## Notes
- For EPUB: use `-s 8 -l H` (high error correction for small screens)
- Max URL length: ~4296 characters
- Always test scan with phone before publishing
