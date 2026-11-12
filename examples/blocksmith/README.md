# Blocksmith

**Blocks to code to AI.** A visual coding school that starts you snapping blocks together, shows you the real code underneath, graduates you to writing real code, then teaches you to build your own AI agent.

## Why

Most beginners hit two walls: the jump from block coding to "real" code, and the jump from using AI to actually directing it well. Blocksmith is one path across both.

## The path

1. **Blocks**: drag-and-drop programs (print, variables, math). The real code is hidden behind a "peek" button so it's not scary.
2. **Hybrid**: loops, decisions, and counting, with the live code generated next to every block you place.
3. **Real code**: a full code editor. "Bring my blocks" turns your last block program into code you can edit.
4. **AI agents**: Agent Lab. Design an agent (role, personality, rules, context, format, example), see a live **prompt strength** score that teaches *why* each part matters, chat with it, and get the exact Python or JavaScript code to run it yourself.

Every lesson is checked automatically by running your program. Finishing a lesson earns XP.

## Features

- 5 languages from the same blocks: **JavaScript, Python, Lua, PHP, Dart**
- Runs JavaScript and **real Python (Pyodide)** right in the browser
- AI coach gives one Socratic hint at a time and never the answer
- Agent Lab exports a working ~20-line agent in Python or JavaScript
- Works with no account in demo mode. Add an Anthropic API key (stored only in your browser) for live AI hints and agents
- Progress saves automatically

## Run it

No build step. From this folder:

```
python -m http.server 8000
```

Then open http://localhost:8000. Needs internet for the CDN libraries.

## Built with

Blockly, Monaco Editor, Pyodide, canvas-confetti, and the Claude API. Single HTML file.
