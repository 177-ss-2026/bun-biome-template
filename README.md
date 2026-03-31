# Bun Biome Template

## Installing Dependencies

This project uses **Bun** as the package manager. Bun is a modern JavaScript runtime that's significantly faster than Node.js.

### Prerequisites

First, make sure you have Bun installed on your machine. Visit [bun.sh](https://bun.sh) for installation instructions.

### Installation Steps

To install the project dependencies:

```bash
bun install
```

This command reads the `package.json` file and installs all required packages (called `devDependencies` in this project) into a `node_modules` folder.

**What gets installed?**

From `package.json`, Bun will install:

- **@biomejs/biome** (v2.3.12) — A fast code formatter and linter

### Verify Installation

After installation, you can verify everything is set up correctly by running:

```bash
bun run start
```

This executes the `start` script defined in `package.json`, which runs `index.js`.

---

## Editor Configuration (settings.json)

The `.vscode/settings.json` file configures Visual Studio Code to work seamlessly with this project.

### Key Settings Explained

**Formatting & Linting:**

- `editor.defaultFormatter`: Set to `biomejs.biome` — Uses Biome to automatically format your code
- `editor.formatOnSave`: `true` — Automatically formats code whenever you save a file
- `source.fixAll.biome`: `always` — Automatically fixes linting issues on save
- `source.organizeImports.biome`: `always` — Automatically organizes imports on save

**Code Editing Features:**

- `editor.bracketPairColorization.enabled`: `true` — Highlights matching bracket pairs with colors
- `editor.linkedEditing`: `true` — When you edit an opening tag, the closing tag updates automatically
- `editor.autoClosingBrackets`: `beforeWhitespace` — Automatically closes brackets intelligently
- `editor.autoClosingComments`: `always` — Automatically closes block comments

**Language-Specific Rules:**

- `[javascript]` and `[json]` blocks ensure Biome is used as the formatter for these file types
- `javascript.format.enable: false` and `json.format.enable: false` — Disables VS Code's built-in formatters to avoid conflicts

**Project Settings:**

- `biome.requireConfiguration: true` — Requires a Biome configuration file (biome.json) to be present in the project

**File Auto-Save:**

- `files.autoSave: onFocusChange` — Automatically saves files when you switch away from them

### Why These Settings Matter

These settings create a **consistent, automated workflow**:

1. You write code
2. On save, Biome automatically formats and fixes issues
3. No manual formatting needed—focus on logic, not style

This ensures your code stays clean and follows project standards automatically.
