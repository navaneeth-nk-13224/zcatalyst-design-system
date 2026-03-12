# ZCatalyst Design System — Setup Guide

> Step-by-step guide to get AI-powered Figma page building working from scratch.

---

## What You'll Have When Done

An AI assistant (GitHub Copilot / Claude) that can **build complete Figma pages** using the ZCatalyst Design System — buttons, inputs, badges, cards, layouts — all from natural language prompts.

---

## What You Need

| Requirement | Why |
|---|---|
| **VS Code** | Editor with Copilot + MCP support |
| **Node.js 18+** | Runs the MCP server |
| **Figma Desktop app** | The bridge plugin only works in the desktop app |
| **Figma account** (Professional or above) | To publish libraries |
| **ZCatalyst DS Figma file** | The design system components + variables (shared by your team) |
| **Git** | To clone this repo |

---

## Step 1: Install VS Code

1. Download from [https://code.visualstudio.com](https://code.visualstudio.com)
2. Install and open it

### Install Required Extensions

Open VS Code → click the **Extensions** icon in the left sidebar (or press `Cmd+Shift+X` on Mac / `Ctrl+Shift+X` on Windows) → search and install:

| Extension | What it does |
|---|---|
| **GitHub Copilot** | AI assistant that runs the workflow |
| **GitHub Copilot Chat** | Chat interface to talk to Copilot |

> You need a **GitHub Copilot subscription** (free for students, or paid). Sign in with your GitHub account when prompted.

---

## Step 2: Install Node.js

1. Check if you already have it — open VS Code's terminal and run:
   ```bash
   node --version
   ```
   If it shows `v18.x.x` or higher, skip to Step 3.

2. If not installed, download from [https://nodejs.org](https://nodejs.org) (pick the **LTS** version)
3. Install it, then restart VS Code
4. Verify again with `node --version`

---

## Step 3: Clone This Repo into VS Code

1. Open VS Code
2. Press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows) to open the Command Palette
3. Type **"Git: Clone"** and select it
4. Paste the repo URL:
   ```
   https://github.com/navaneeth-nk-13224/zcatalyst-design-system.git
   ```
5. Choose a folder on your computer to save it
6. Click **"Open"** when VS Code asks to open the cloned repo

### Install Dependencies

Open the terminal in VS Code and run:
```bash
npm install
```

---

## Step 4: Get Your Figma Access Token

The MCP server needs a token to talk to Figma.

1. Open Figma Desktop → click your **profile icon** (top-left) → **Settings**
2. Scroll down to **Personal access tokens**
3. Click **"Generate new token"**
4. Name it: `ZCatalyst MCP`
5. Set these scopes:
   - **File content**: Read and Write
   - **Variables**: Read and Write
6. Click **"Generate token"**
7. **Copy the token immediately** — it starts with `figd_` and you won't see it again

> Save this token somewhere safe (a password manager, or a note). If you lose it, you'll need to generate a new one.

---

## Step 5: Set Up the ZCatalyst DS File in Figma

> If you already have the DS file in your Figma team, skip to step 5.3.

### 5.1 Get the DS File

Ask your team lead for access to the **ZCatalyst Design System** Figma file, or duplicate it to your account if shared.

### 5.2 Publish as Library

1. Open the DS file in Figma Desktop
2. Click the **Figma icon** (top-left) → **Libraries** → **Publish**
3. Make sure all components, styles, and variables are included
4. Click **"Publish"**

### 5.3 Enable in Your Working File

1. Create a new Figma file (or open the one you'll build pages in)
2. Click the **Assets** panel (left sidebar) → **Libraries icon** (book icon at top)
3. Find **"ZCatalyst Design System"** and toggle it **ON**
4. Keep this file open — this is where pages will be built

---

## Step 6: Install the Desktop Bridge Plugin

The bridge plugin lets the MCP server execute code inside Figma.

1. In Figma Desktop, go to **Plugins** → **Development** → **Import plugin from manifest...**
2. Navigate to the cloned repo folder → `figma-desktop-bridge` → select `manifest.json`
3. The plugin appears under **Plugins → Development → Figma Desktop Bridge**
4. **Run the plugin** in your working file — click **Plugins → Development → Figma Desktop Bridge**
5. You'll see a small panel — it auto-connects via WebSocket

> This is a one-time setup. The plugin stays in your Development plugins list.

---

## Step 7: Connect the MCP Server to VS Code

### 7.1 Open MCP Settings

1. In VS Code, press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows)
2. Type **"MCP: Open User Configuration"** and select it
3. This opens a JSON file — your MCP config

> **If the file is empty or has no content**, paste the full block below.
> **If it already has entries**, add the `"figma-console"` entry inside the existing `"mcpServers"` object.

### 7.2 Paste This Configuration

```json
{
  "mcpServers": {
    "figma-console": {
      "command": "npx",
      "args": ["-y", "figma-console-mcp@latest"],
      "env": {
        "FIGMA_ACCESS_TOKEN": "figd_PASTE_YOUR_TOKEN_HERE",
        "ENABLE_MCP_APPS": "true"
      }
    }
  }
}
```

### 7.3 Replace the Token

Replace `figd_PASTE_YOUR_TOKEN_HERE` with the actual token you copied in Step 4.

### 7.4 Save and Restart

1. Save the file (`Cmd+S` / `Ctrl+S`)
2. **Restart VS Code** completely (close and reopen)

---

## Step 8: Verify Everything Works

### 8.1 Check MCP Connection

1. Open Copilot Chat in VS Code (click the Copilot icon in the sidebar, or press `Cmd+Shift+I`)
2. Switch to **Agent** mode (dropdown at top of chat — select "Agent" instead of "Ask" or "Edit")
3. Type:
   ```
   list all available MCP tools
   ```
   You should see Figma tools like `figma_execute`, `figma_capture_screenshot`, etc.

### 8.2 Check Figma Connection

Make sure:
- Your **working Figma file is open** in Figma Desktop
- The **Desktop Bridge plugin is running** (Step 6)

Then in Copilot Chat (Agent mode), type:
```
take a screenshot of the current Figma page
```

If it returns a screenshot, everything is connected.

### 8.3 Test Page Creation

```
Create a new page called "Test Page" with a card that says "Hello World"
```

If a page appears in your Figma file — you're all set!

---

## Step 9: Start Building

The repo's `.github/copilot-instructions.md` is **auto-loaded by Copilot** in every chat session. It contains all the component keys, helper functions, and building patterns.

Just open Copilot Chat in **Agent mode** and describe what you want:

```
Create a dashboard page with stat cards showing Total Users: 1,250
and Active Sessions: 342, a table section, and an action bar with
Save and Cancel buttons
```

Copilot will:
1. Import the Layout component from the DS
2. Set up the Sub Header
3. Build all the content using DS components
4. Bind all colors to design variables

### Reference Docs

| File | What's in it |
|---|---|
| `docs/rules.md` | 20 mandatory rules — read if builds are failing |
| `docs/zcatalyst-design-system.md` | All 59 components with keys, variants, and props |
| `docs/zcatalyst-styles.md` | All text styles and color variable keys |
| `.github/copilot-instructions.md` | Full workflow (auto-loaded, no need to open) |

---

## Troubleshooting

| Problem | Fix |
|---|---|
| **"Could not find variable"** error | The DS library isn't enabled in your working file. Go to Assets → Libraries → toggle ZCatalyst ON |
| **"Cannot move node into instance"** | The layout wasn't detached. This is handled automatically — report if it happens |
| **MCP tools not showing in chat** | Restart VS Code. Check that your MCP config JSON is valid (no trailing commas, no syntax errors) |
| **Screenshot returns nothing** | Make sure the Desktop Bridge plugin is running in your Figma file |
| **Token error / 403** | Your Figma token may have expired. Generate a new one (Step 4) and update the MCP config |
| **`figma_execute` timeout** | Normal for large pages. Copilot will automatically continue from where it stopped |
| **Node.js not found** | Restart VS Code after installing Node.js. On Mac, you may need to restart your terminal too |
| **Agent mode not available** | Make sure GitHub Copilot Chat extension is installed and you're signed in |

---

## Config File Locations (Other Editors)

If you're using a different AI editor instead of VS Code + Copilot:

| App | macOS | Windows |
|---|---|---|
| **Cursor** | `~/.cursor/mcp.json` | `%USERPROFILE%\.cursor\mcp.json` |
| **Windsurf** | `~/.codeium/windsurf/mcp_config.json` | `%USERPROFILE%\.codeium\windsurf\mcp_config.json` |
| **Claude Desktop** | `~/Library/Application Support/Claude/claude_desktop_config.json` | `%APPDATA%\Claude\claude_desktop_config.json` |

Paste the same JSON from Step 7.2 into the relevant file.
