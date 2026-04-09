# Hall(marks) of Humanity
An exhibit on humanity's relationship with our technology.

> \\\*Walk the halls. Touch the exhibits. Learn how ten technologies remade the world.\\\*

\---

## What This Is

An interactive, browser-based museum built entirely in ASCII graphics. The player walks through exhibition halls, approaches artifact displays, and reads museum-quality placards about the most paradigm-shifting technologies in human history — from controlled fire to artificial intelligence.

Built as a learning project and eventually intended as a teaching tool for an undergraduate course on human-technology relationships.

**Current status: Work in progress — Milestone 1 of 5**

\---

## How to Run It

No installation. No build step. No dependencies.

1. Download `museum.html`
2. Open it in any modern browser
3. Use the arrow keys to walk around

That's it.

\---

## How to Play

|Key|Action|
|-|-|
|← ↑ ↓ →|Move your character (`☺`)|
|`ENTER` or `SPACE`|Examine a nearby exhibit|
|`ESC`|Close the exhibit placard|

Walk toward a glowing `?` marker to find an exhibit. When you're close enough, the status bar at the bottom will tell you what you're looking at. Press `ENTER` to open the full placard — which includes an ASCII-rendered photograph, the museum description, a curator's note, and a suggested reading.

\---

## Exhibit List

|#|Technology|Era|
|-|-|-|
|I|Fire \& Controlled Combustion|c. 400,000 BCE|
|II|Agriculture \& Domestication|c. 10,000 BCE|
|III|The Wheel \& Mechanical Advantage|c. 3,500 BCE|
|IV|Writing \& Symbolic Records|c. 3,200 BCE|
|V|The Printing Press|1440 CE|
|VI|The Steam Engine \& Industrialization|1760s CE|
|VII|Electricity \& Telecommunications|1800s CE|
|VIII|Germ Theory \& Modern Medicine|1850s CE|
|IX|The Internet \& Networked Computing|1969–1990s|
|X|Artificial Intelligence|2020s CE|

*Honorable mentions wing in progress.*

\---

## Development Roadmap

* \[x] **Milestone 1** — Core engine: movement, collision, modal overlay, ASCII image renderer
* \[ ] **Milestone 2** — All 10 exhibits wired in with full placard data
* \[ ] **Milestone 3** — Multi-room hall layout with doors and transitions
* \[ ] **Milestone 4** — Honorable mentions wing, intro screen
* \[ ] **Milestone 5** — Polish: ambient effects, room labels, map screen

\---

## Technical Notes

Single HTML file — all game logic, exhibit data, and styles are self-contained. No frameworks, no build tools.

* **Renderer:** `<pre>` tag redrawn on each keypress via span-encoded color classes
* **Map format:** Rooms are arrays of strings; each character is one tile
* **ASCII image rendering:** Fetches exhibit photos, draws to a hidden canvas, samples brightness, maps to a character ramp
* **Exhibit data:** Structured JS objects converted from a YAML schema (`exhibits.yaml` in the repo)

\---

## Exhibit Data File

All exhibit records — including full placard text, authoritative links, suggested readings, image URLs, and ASCII art objects — live in `exhibits.yaml`. This file is the museum's database and is kept separate from the game engine so new exhibits can be added without touching the renderer.

\---

## Context

This project is being developed alongside *Humans in the Age of Bots*, a 3000-level interdisciplinary course exploring human-technology relationships, identity, and what it means to live alongside intelligent machines. The museum format was chosen deliberately: it asks visitors to slow down, read carefully, and place contemporary technology in deep historical context.

\---

## Credits

Built with: vanilla JS, monospace font, and an unreasonable fondness for the aesthetics of 1980s terminal software.

Exhibit text informed by: Richard Wrangham, James C. Scott, Elizabeth Eisenstein, Jenny Uglow, Katie Hafner, Brian Christian, and others — full reading list in `exhibits.yaml`.

Image sources: Wikimedia Commons (public domain / CC licenses).

\---

*Work in progress. Walls may be uneven. The player is a smiley face. This is intentional.*

