---
title: Home
layout: home
nav_order: 1
---

# Claude Code on Windows — Playbook
{: .fs-9 }

A complete kit for teaching non-developers how to install and start using Claude Code on Windows in 30 minutes.
{: .fs-5 .fw-300 }

[Open the walkthrough](./01-walkthrough.html){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [Download PDFs](https://github.com/jomojo0202/claude-code-setup/tree/main/pdfs){: .btn .fs-5 .mb-4 .mb-md-0 }

---

> **Why PowerShell?** It's the modern, Microsoft-supported shell built into Windows 11. Together with Windows Terminal it gives you a zero-install starting point. CMD is legacy. Git Bash is an extra install. WSL2 is the power-user path — worth a follow-up session, but overkill for a 30-min beginner workshop.

## What's in this site

| Page | What it's for |
|---|---|
| [Live Walkthrough](./01-walkthrough.html) | **Live demo script** — minute-by-minute instructions for the instructor, with exact commands, what to say, and what NOT to do live. |
| [Slide Outline](./02-outline.html) | **Slide outline + talking points** — 8-slide structure you can paste into Keynote, Google Slides, or PowerPoint. |
| [Attendee Handout](./03-handout.html) | **Attendee handout** — a clean cheatsheet attendees keep after the session so they can repeat the install on their own. |
| [PDFs](https://github.com/jomojo0202/claude-code-setup/tree/main/pdfs) | PDF versions of all three documents, ready to print or share. |

---

## Audience this is built for

- **Non-developers** — marketers, founders, ops, support staff.
- **Windows 11** users who have never touched a terminal.
- **30 minutes** of session time (with the option to expand to 60 if you add WSL2).

---

## How to run the session

1. Skim [`01-walkthrough.md`](./01-walkthrough.md) the day before — it tells you what to install on your demo machine ahead of time.
2. Build your slides from [`02-outline.md`](./02-outline.md).
3. Email or print [`03-handout.md`](./03-handout.md) (or [`pdfs/03-handout.pdf`](./pdfs/03-handout.pdf)) for attendees.
4. Run the session. Stick to the time budget in the walkthrough.

---

## What gets installed during the session

- **Node.js LTS** (provides `npm`)
- **Claude Code** (`npm install -g @anthropic-ai/claude-code`)
- **Authentication** via Claude.ai account (no API key for beginners)

That's it. No Docker, no WSL, no Visual Studio.

---

## Where to go after the session

- `/help` inside Claude — explore commands.
- `claude --resume` — pick up your last conversation.
- **CLAUDE.md** — drop a text file in any folder to teach Claude your preferences.
- **Skills** — type `/skills` inside Claude to see pre-built experts.
- **WSL2** — the next step once attendees are comfortable. Worth a follow-up session.

---

## Credits

Built for an instructor-led mentorship session. PRs welcome — if you ran the workshop and learned something, send a fix.
