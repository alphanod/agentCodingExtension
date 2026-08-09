# Agent Coding Extension

A VS Code extension scaffold.

## Project structure

```
agentCodingExtension/
├── .vscode/                  # VS Code workspace config (launch, tasks)
├── src/
│   └── extension.ts          # Extension entry point
├── .vscodeignore             # Files excluded from the .vsix package
├── .gitignore                # Files excluded from git
├── esbuild.js                # Bundler script (esbuild)
├── package.json              # Extension manifest + npm scripts
└── tsconfig.json             # TypeScript config
```

## Commands

| Command | What it does |
|---|---|
| `npm run compile` | Type-check + lint + bundle to `dist/` |
| `npm run watch` | Watch mode — rebuilds on file changes |
| `npm run package` | Type-check + lint + production bundle (for `.vsix`) |
| `npm run check-types` | Run `tsc --noEmit` only |
| `npm test` | Run tests (no tests yet) |

## Running the extension

1. Open this folder in VS Code.
2. Press **F5** (or `Run → Start Debugging`) — this opens a new VS Code window with the extension loaded.
3. In the new window, open the **Command Palette** (`Ctrl+Shift+P`) and run **Hello World**.
4. You should see a notification: *"Hello World from Agent Coding Extension!"*

## Bundling & publishing

The extension is bundled with [esbuild](https://esbuild.github.io/) into a single `dist/extension.js`. To package a `.vsix`:

```bash
npm install -g @vscode/vsce
vsce package
```
