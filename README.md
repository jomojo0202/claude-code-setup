# Claude Code on Windows —  Playbook

A complete kit for teaching non-developers how to install and start using **Claude Code** on Windows in 30 minutes.

> **Quick links:** [Live Walkthrough](./01-walkthrough.html) · [Slide Outline](./02-outline.html) · [Attendee Handout](./03-handout.html) · [Download PDFs](https://github.com/jomojo0202/claude-code-setup/tree/main/pdfs)

> **Why PowerShell?** It's the modern, Microsoft-supported shell built into Windows 11. Together with Windows Terminal it gives you a zero-install starting point. CMD is legacy. Git Bash is an extra install. WSL2 is the power-user path — worth a follow-up session, but overkill for a 30-min beginner workshop.

---

## What's in this repo

| File | What it's for |
|---|---|
| [`01-walkthrough.md`](./01-walkthrough.md) | **Live demo script** — minute-by-minute instructions for the instructor, with exact commands, what to say, and what NOT to do live. |
| [`02-outline.md`](./02-outline.md) | **Slide outline + talking points** — 8-slide structure you can paste into Keynote, Google Slides, or PowerPoint. |
| [`03-handout.md`](./03-handout.md) | **Attendee handout** — a clean cheatsheet attendees keep after the session so they can repeat the install on their own. |
| [`pdfs/`](./pdfs) | PDF versions of all three documents, ready to print or share. |

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
