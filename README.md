# ARYSIG — File Signature Toolkit

> A browser-based tool for viewing and modifying file magic bytes (file signatures), built for cybersecurity research, CTF challenges, and forensics work.

🔗 **Live Tool:** [https://giriaryan694-a11y.github.io/ARYSIG/](https://giriaryan694-a11y.github.io/ARYSIG/)

---

## What is ARYSIG?

Every file format has a unique sequence of bytes at the start of the file called a **magic byte** or **file signature**. These bytes tell the operating system and applications what kind of file it is — independently of the file extension.

ARYSIG lets you load any file, inspect its raw hex header, overwrite the magic bytes with a different format's signature, and download the modified file. This is useful for:

- Bypassing naive file-type filters that only check magic bytes
- CTF (Capture The Flag) challenges involving file format manipulation
- Digital forensics and file carving research
- Understanding how file identification actually works under the hood

---

## Features

- **Drag & drop or browse** to load any file
- **Live hex viewer** — displays the first 32 bytes of the original file
- **Signature selector** — choose from 6 common formats with one click
- **Modified header preview** — see exactly which bytes changed, highlighted in yellow
- **Extension control** — choose YES to rename the extension on download (auto-filled or custom), or NO to keep the original
- **System log** — timestamped activity log for every action
- **Works entirely in the browser** — no uploads, no server, no data leaves your device
- **Fully responsive** — works on desktop and mobile

---

## Supported Signatures

| Format | Magic Bytes | Extension |
|--------|-------------|-----------|
| PNG    | `89 50 4E 47 0D 0A 1A 0A` | `.png` |
| GIF    | `47 49 46 38 39 61`       | `.gif` |
| JPEG   | `FF D8 FF E0`             | `.jpg` |
| PDF    | `25 50 44 46 2D`          | `.pdf` |
| ZIP    | `50 4B 03 04`             | `.zip` |
| ELF    | `7F 45 4C 46`             | `.elf` |

---

## How to Use

1. Open the tool at the link above
2. Drag & drop a file onto the dropzone, or click **Browse File**
3. The original magic bytes appear in the hex viewer
4. Select a target signature from the signature cards
5. Choose whether to change the file extension on download (YES/NO)
6. Click **Convert Signature** — the modified header preview appears
7. Click **Download Modified** to save the patched file

---

## How File Signatures Work

File signatures (also called magic numbers) are defined byte sequences at the beginning of a file. Unlike file extensions — which are just part of the filename and can be changed freely — magic bytes are embedded in the file's actual binary content.

Tools like `file` on Linux and many security scanners use these bytes to determine file type. A file named `photo.jpg` with PNG magic bytes (`89 50 4E 47...`) will be identified as a PNG by such tools, regardless of the extension.

ARYSIG patches only these header bytes, leaving the rest of the file's content intact.

---

## Disclaimer

This tool is intended for **educational and authorized security research purposes only**. Using it to bypass security controls on systems you do not own or have permission to test is illegal and unethical. Always ensure you have proper authorization before testing.

---

## Author

Made by **Aryan Giri**
