# Tailwind CSS v4 From Scratch

KORSAT X PARMAGA is a small static games landing page built as a Tailwind CSS v4 from-scratch course project.

## Stack

- HTML
- Tailwind CSS v4
- Tailwind CLI
- Boxicons

## Project Structure

```text
.
├── dist/
│   ├── index.html
│   └── output.css
├── src/
│   └── input.css
├── package.json
├── package-lock.json
├── tailwind.config.js
└── README.md
```

## Install

```bash
npm install
```

## Build Tailwind CSS

Run a one-time build:

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./dist/output.css
```

Run in watch mode:

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./dist/output.css --watch
```

## Tailwind v4 Setup In This Course Project

The main stylesheet is `src/input.css`.

It uses:

- `@import "tailwindcss";` to load Tailwind
- `@config "../tailwind.config.js";` to connect the config file
- `@source` directives so Tailwind scans your HTML and source files
- `@theme` to define custom design tokens like colors and fonts

Example custom theme tokens already used in this project:

- `--font-bodyFont`
- `--color-primary`
- `--color-secondary-100`
- `--color-secondary-200`

These become utilities such as:

- `font-bodyFont`
- `text-primary`
- `bg-primary`
- `text-secondary-100`
- `bg-secondary-200`

## Notes

- Tailwind v4 prefers color opacity like `bg-black/50` instead of older utilities such as `bg-opacity-50`.
- If a utility is not generated, make sure the class exists in your HTML files matched by the `@source` directives.
- The compiled CSS file is written to `dist/output.css`.

## Preview

Open `dist/index.html` in your browser after building `dist/output.css`.
