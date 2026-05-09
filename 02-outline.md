# Slide Outline + Talking Points — Claude Code on Windows (30 min)

> 8 slides. ~3-4 min per slide on average. Demo is the longest section.

---

## Slide 1 — Title

**Visual:** Big title, your name, the date.

> **Title:** Get Claude Code Running on Your Windows Machine — in 30 Minutes
> **Subtitle:** From zero to "AI is now editing my files"

**Talking points:**
- Welcome. By the end of this session you'll have an AI assistant that can read your files, edit them, and run things for you.
- This is hands-on. Open your laptop. We're installing it together.

---

## Slide 2 — What is Claude Code (and why should you care)

**Visual:** Side by side — left: ChatGPT chat window. Right: a terminal with Claude Code editing a file.

> **One-liner:** Claude Code is ChatGPT with hands.

**Talking points:**
- ChatGPT can talk about your files. Claude Code can actually open, read, and change them.
- Three concrete things it does that chat can't:
  1. Read every file in a folder.
  2. Edit files directly (with your permission).
  3. Run commands and report back.
- Examples for non-devs:
  - "Summarize 50 customer emails in this folder."
  - "Pull dates and dollar amounts out of this contract."
  - "Build me a one-page website by tonight."

---

## Slide 3 — The Window You'll Live In

**Visual:** Screenshot of Windows Terminal with PowerShell open.

> **Heading:** Terminal vs. Shell — what's the difference?

**Talking points:**
- **Terminal** = the window (the app with tabs).
- **Shell** = the language you type inside it.
- On Windows you have choices. Here's the simple answer:
  - **Use Windows Terminal** as the app — preinstalled on Windows 11.
  - **Use PowerShell** as the shell — Microsoft's modern, supported one.
- What about the alternatives?
  - **CMD** — old. Skip.
  - **Git Bash** — works, but extra install.
  - **WSL2** (real Linux inside Windows) — more powerful, but 30 min of setup. That's a future session.
- For today: Windows Terminal + PowerShell. Already on your machine. Zero extra install.

---

## Slide 4 — Step 1: Install Node.js

**Visual:** nodejs.org homepage with the LTS download button circled.

> **Heading:** Get the engine

**Talking points:**
- Claude Code is delivered through "npm" — it ships with Node.js.
- Go to **nodejs.org**.
- Download the **LTS** version (left button, says "LTS").
- Run installer. Click Next on every screen. Defaults are correct.
- Close any open PowerShell windows after install. Open a fresh one.

**Verify:**
```powershell
node --version
npm --version
```

---

## Slide 5 — Step 2: Install Claude Code

**Visual:** A single line of code, big text.

```powershell
npm install -g @anthropic-ai/claude-code
```

**Talking points:**
- One command. Paste it. Wait 30–60 seconds.
- The `-g` means "global" — you can run `claude` from any folder on your computer.
- Verify: `claude --version`.

---

## Slide 6 — Step 3: Sign In

**Visual:** Screenshot of the first-run auth screen.

> **Heading:** Two ways to sign in. Pick the easy one.

**Talking points:**
- Type `claude` in PowerShell. First run shows an auth screen.
- **Option 1 (recommended):** Sign in with your Claude account (uses your Claude.ai Pro subscription).
- **Option 2 (advanced):** Use an API key from console.anthropic.com — pay-per-use. Skip for today.
- Browser opens, log in, click Authorize, tab back. Done.

---

## Slide 7 — LIVE DEMO

**Visual:** Just a black slide that says "DEMO" — focus moves to your screen.

**Talking points:**
- Pick the demo from the walkthrough doc that fits your audience.
- Narrate what's happening on screen as Claude works.
- Highlight: "It asked permission before editing." — that's important.

**If the demo fails:**
- Have a screen recording of a successful run as a backup. Play that.

---

## Slide 8 — Where to Go From Here

**Visual:** Bullet list with icons.

**Talking points:**
- `/help` inside Claude — explore commands.
- `claude --resume` — continue your last conversation.
- **CLAUDE.md** — drop a file in any folder to teach Claude your preferences.
- **Skills** — pre-built experts for marketing, ads, copywriting, etc.
- **Next session:** WSL2 setup for serious users.

**Close with:**
> "What's the first thing in your work you'd want to hand to Claude?"
> Collect answers. You just sourced your next session topic.

---

## Speaker notes — overall

- **Don't apologize for the terminal.** Non-devs are nervous about it. Frame it as "just a different kind of window." Confidence transfers.
- **Pause after each command** for ~5 seconds. Let attendees catch up. They will fall behind without it.
- **Use a big font** in PowerShell during the demo (Ctrl+Plus to zoom). Default size is unreadable on a projector.
- **Have water nearby.** 30 min talking is more than you think.
