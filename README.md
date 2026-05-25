# Sketch Agent

&gt; Your AI design partner inside Sketch. Turn words into interfaces.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Sketch Version](https://img.shields.io/badge/Sketch-100+-orange.svg)](https://www.sketch.com)
[![macOS](https://img.shields.io/badge/macOS-13%2B-black.svg)](https://www.apple.com/macos)

Sketch Agent embeds a conversational AI panel directly into Sketch's Inspector sidebar, enabling you to **generate complete UI layouts** from text descriptions or **modify selected layers** through simple chat commands—without ever leaving your canvas.

---

## ✨ Features

- **🎨 Generate UI from Text** — Describe any interface (e.g., *"a login page with email, password, and social login buttons"*) and watch AI build the layer structure on your artboard.
- **⚡ Modify by Chatting** — Select any layer and instruct changes (*"make this button #1890FF with 8px radius"*). Changes apply instantly.
- **🔄 Multi-turn Iteration** — Refine designs conversationally. Every command builds on previous context.
- **👁️ Smart Preview Mode** — Simple edits apply immediately; complex creations show an SVG preview for approval before writing to canvas.
- **🤖 Multi-Model Support** — Bring your own API key. Compatible with **OpenAI (GPT)**, **Anthropic (Claude)**, **DeepSeek (V4)**, and **Zhipu AI (GLM)**.
- **🧠 Canvas Context Awareness** — Automatically feeds selected layer properties, artboard dimensions, color variables, and text styles into the AI prompt.
- **↩️ Native Undo Support** — Every AI action is fully reversible via Sketch's native `Cmd+Z`.
- **🔒 Privacy First** — Your API key is AES-encrypted and stored locally. Design data never leaves your machine.

---

## 📦 Installation

### From Release (Recommended)

1. Download the latest `.sketchplugin` from [Releases](../../releases).
2. Double-click to install.
3. Restart Sketch if already running.

### From Source

```bash
git clone https://github.com/yourusername/sketch-agent.git
cd sketch-agent
npm install
npm run build
# Or watch for changes during development
npm run watch
