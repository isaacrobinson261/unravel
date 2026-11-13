# Unravel

**X-ray any codebase.** Unravel reverse-engineers how a piece of software works and shows it to you: architecture map, entry points, API routes, dependencies, config, and security red flags.

It comes in two parts:

1. **The app**: drop a project folder into a web page and get an interactive, glowing architecture map plus a full breakdown. Everything runs in your browser and nothing is uploaded.
2. **The Claude Code add-on**: type `/unravel` in any project and Claude traces the real code paths and writes a `BLUEPRINT.md`, with a Mermaid diagram, the core flow with `file:line` references, and the three files to read first.

## Why

Joining a new codebase, inheriting a class project, or opening an old repo you forgot about usually costs hours of clicking around. Unravel gets that down to minutes, and it helps people learn by seeing how real software is built.

## Built to help, not harm

Unravel is for understanding code you wrote or are allowed to study (your own, your team's, open source, class work). The app asks you to confirm that before scanning. The add-on is told to refuse license, DRM, and auth bypasses. Secrets it finds are flagged with the value hidden, so you can rotate them, not leak them.

## The app

```
python -m http.server 8000
```

Open http://localhost:8000, check the permission box, and drop in a folder.

- **Architecture map**: a force-directed graph of every file, colored by language and sized by length. Hover a file to light up what it imports and what imports it, with animated flow showing direction. Drag, zoom, and click to inspect.
- **Overview**: languages, where the program starts, how to run it, and what it's built with.
- **API + Config**: detected HTTP routes (Express, Flask, FastAPI style) and every environment variable it reads.
- **Security**: hardcoded API keys, tokens, private keys, and passwords (values hidden), plus dependencies used but never declared.
- **Hotspots**: the core files everything depends on, the biggest files, and TODO/FIXME clusters.
- **Export blueprint**: a Markdown write-up with a Mermaid diagram.

Understands JavaScript, TypeScript, Python, HTML, and CSS imports, and counts more than 20 languages.

## The Claude Code add-on

```
/plugin marketplace add BigRob267/unravel
/plugin install unravel@unravel
```

Then, in any project:

```
/unravel                          # full blueprint of the current project
/unravel ./server                 # just one folder
/unravel how does login work?     # trace one flow
```

## Built with

Plain HTML, CSS, and JavaScript (single file, no dependencies, Canvas for the graph) and a Claude Code plugin.
