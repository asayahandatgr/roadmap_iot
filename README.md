# Roadmap Smart Motorcycle Parking

This repository contains a **static web application** that visualises the roadmap for the Smart Motorcycle Parking project.

## Project structure

```
roadmap_projectiot/
│   package.json
│   vercel.json
│   README.md
│
└─ public/
    └─ index.html   ← main entry point (served as static site)
```

All static assets (HTML, CSS, JS, images) should be placed inside the `public/` folder.

## Development

The project uses the **serve** package to run a local static server.

```powershell
# Install dependencies (run once)
npm install

# Start the development server
npm run dev   # or npm start
```

The site will be available at `http://localhost:3000` (default port used by `serve`).

## Build

Because this is a static site, no build step is required. The `build` script is a placeholder:

```json
"build": "echo \"No build needed for static site\""
```

If you later add a build step (e.g., bundling with Vite, Webpack, etc.), replace the script accordingly.

## Deploy to Vercel

1. **Install the Vercel CLI** (if you haven't already):

   ```powershell
   npm i -g vercel
   ```

2. **Login** to your Vercel account:

   ```powershell
   vercel login
   ```

3. **Deploy** (production):

   ```powershell
   npm run deploy   # runs `vercel --prod`
   ```

   Vercel will read `vercel.json`, which points the output directory to `public/` and rewrites the root URL to `index.html`.

4. **Preview locally with Vercel** (optional):

   ```powershell
   npm run vercel-dev   # runs `vercel dev`
   ```

## VS Code integration

The repository includes a **VS Code tasks** configuration (`.vscode/tasks.json`) that provides two convenient tasks:

* **Deploy to Vercel** – runs `npm run deploy`.
* **Run dev server** – runs `npm run dev`.

You can trigger these tasks via the **Terminal → Run Task…** menu or the command palette (`Ctrl+Shift+P` → *Tasks: Run Task*).

---

Feel free to modify the scripts or add additional tooling as your project evolves.

---

*Created by the Copilot assistant.*
