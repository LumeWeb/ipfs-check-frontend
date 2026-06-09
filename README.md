# ipfs-check-frontend

A fork of the [`web/`](https://github.com/ipfs/ipfs-check/tree/main/web) folder from [ipfs/ipfs-check](https://github.com/ipfs/ipfs-check), extracted with full commit history.

## Licensing

- This repository is licensed under the [MIT License](LICENSE) — Copyright (c) 2026 Hammer Technologies LLC
- The original upstream code is dual-licensed under Apache-2.0 OR MIT — see [ORIGINAL_LICENSE.md](ORIGINAL_LICENSE.md)

## Development

### Prerequisites

- Node.js and npm (only needed for modifying styles)

### Modifying Styles

The project uses Tailwind CSS for styling. If you need to make style changes:

1. Install dependencies (one-time setup):
   ```bash
   npm ci
   ```

2. For development with live CSS updates:
   ```bash
   npm run dev
   ```
   This watches `input.css` for changes and automatically rebuilds `output.css`

3. For production build (minified CSS):
   ```bash
   npm run build
   ```

4. **Important**: After making style changes, commit the updated `output.css` file

### Files

- `index.html` - Main HTML file
- `script.js` - JavaScript logic for the check interface
- `input.css` - Source Tailwind CSS file (modify this for style changes)
- `output.css` - Compiled CSS (auto-generated, but committed to git)
- `favicon.ico` - Site favicon
- `fonts/` - Custom fonts

### Notes

- The `output.css` file is intentionally committed to version control
- This allows the Go binary to embed and serve the web interface without requiring a build step
- Only run `npm ci` and `npm run build` if you're modifying the styles