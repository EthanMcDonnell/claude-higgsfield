# Higgsfield Seedance 2.0 — Claude Skills Setup Guide

A collection of Claude skills for generating AI video prompts on [Higgsfield](https://higgsfield.ai) using Seedance 2.0. These skills help Claude craft production-grade prompts across 15 video styles — cinematic, 3D CGI, anime, fashion, food, real estate, and more.

---

## Getting Started

Choose one of two setup paths:

### Option A — Claude Code (quickest)

Clone or download this repo into your project directory:

**Git clone:**

```bash
git clone https://github.com/EthanMcDonnell/claude-higgsfield.git
```

**Or download ZIP:** go to [github.com/EthanMcDonnell/claude-higgsfield](https://github.com/EthanMcDonnell/claude-higgsfield) → **Code → Download ZIP** and unzip it.

That's it — open Claude Code in the project directory and start prompting. The `.mcp.json` in the repo configures Playwright MCP automatically.

---

### Option B — Manual setup / Claude Desktop

Follow each step below from scratch.

#### Prerequisites

- [Claude Desktop](https://claude.ai/download)
- Node.js installed (for Playwright MCP)

#### Step 1 — Configure Playwright MCP

Playwright MCP lets Claude control a browser to interact with Higgsfield directly.

1. Open **Claude Desktop** → Settings → Developer → Edit Config
2. Add the following to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp@latest", "--browser", "chrome"]
    }
  }
}
```

3. Save the file and **restart Claude Desktop**

#### Step 2 — Install the Skills

1. Download the ZIP from [github.com/beshuaxian/higgsfield-seedance2-jineng](https://github.com/beshuaxian/higgsfield-seedance2-jineng) → **Code → Download ZIP**
2. Unzip the file
3. Copy the contents of the `skills/` folder into your Claude skills directory (`.claude`)

> Your skills directory should now contain folders like `01-cinematic`, `02-3d-cgi`, `03-cartoon`, etc.

---

## Step 3 — Start Prompting

Open Claude and describe the video you want to create. Claude will automatically pick the right skill based on your description.

### Example prompts

```text
Generate a cinematic scene of a lone samurai walking through a foggy forest at dawn
```

```text
Create a 3D CGI product reveal for a luxury watch with dramatic lighting
```

```text
Make an anime action sequence with two characters fighting in the rain
```

```text
Create a fashion lookbook video for a summer collection on a rooftop in golden hour
```

```text
Generate a real estate walkthrough of a modern minimalist penthouse
```

Claude will craft a Seedance 2.0 prompt optimized for Higgsfield and can use Playwright to open the browser and submit it for you.

---

## Available Skills

| # | Skill | Use For |
|---|-------|---------|
| 01 | Cinematic | Film-style, Hollywood, dramatic scenes |
| 02 | 3D CGI | Product reveals, abstract visuals |
| 03 | Cartoon | Animated, playful, colorful content |
| 04 | Comic to Video | Transform comic panels into motion |
| 05 | Fight Scenes | Action, martial arts, combat sequences |
| 06 | Motion Design Ad | Kinetic typography, brand motion |
| 07 | Ecommerce Ad | Product ads, conversion-focused video |
| 08 | Anime Action | Japanese animation style sequences |
| 09 | Product 360 | 360° product showcase |
| 10 | Music Video | Beat-synced, visual narrative |
| 11 | Social Hook | Short-form, attention-grabbing clips |
| 12 | Brand Story | Narrative-driven brand content |
| 13 | Fashion Lookbook | Editorial fashion and styling video |
| 14 | Food & Beverage | Culinary, drink, restaurant content |
| 15 | Real Estate | Property walkthroughs, architectural video |
