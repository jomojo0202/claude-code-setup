---
title: Live Walkthrough (instructor)
nav_exclude: true
---

# Live Walkthrough — Setting Up Claude Code on Windows (30 min)

> Audience: non-developers (marketers, founders, ops people). Native Windows + PowerShell. No WSL.
>
> Pre-session checklist (do this BEFORE attendees join):
> - Test the install on a clean account once so you know the time estimate.
> - Have your Claude.ai account ready to log in.
> - Open Notepad with the install commands so you can copy-paste live (don't type live — typos kill demos).
> - Pin Windows Terminal to the taskbar so you can launch it instantly.

---

## Time budget

| Block | Time | What happens |
|---|---|---|
| 1. Hook + what Claude Code is | 0:00 – 0:03 | Frame the value |
| 2. Why PowerShell (and what a terminal is) | 0:03 – 0:05 | Set context |
| 3. Install Node.js | 0:05 – 0:10 | Prerequisite |
| 4. Install Claude Code | 0:10 – 0:13 | One npm command |
| 5. Sign in | 0:13 – 0:15 | Browser-based auth |
| 6. Live demo: ask Claude to do something useful | 0:15 – 0:25 | The "wow" |
| 7. What's next + Q&A | 0:25 – 0:30 | Resources |

---

## 1. Hook + what is Claude Code (0:00 – 0:03)

**Say:**
> "In the next 30 minutes you'll have an AI that can read files on your computer, run commands, edit code or documents, and finish tasks for you — all from a single window. It's called Claude Code. By the end you'll have it running and you'll have used it once."

**One-line definition for non-devs:**
> "Claude Code is ChatGPT with hands. It doesn't just talk — it can open your files, edit them, run things, and report back."

**Concrete examples that land with non-devs:**
- "Open this folder of CSVs and tell me which products had the most refunds."
- "Read this contract PDF and pull out every date and dollar amount into a spreadsheet."
- "Look at my Shopify export and write me ad copy variations for my top 5 products."

---

## 2. Why PowerShell (and what is a terminal?) (0:03 – 0:05)

**Say:**
> "Claude Code lives in a window called a terminal. A terminal is just a window where you type commands instead of clicking buttons. On Windows there are a few options — let me show you the right one."

**Show on screen:**
- **Windows Terminal** = the app (the window with tabs).
- **PowerShell 7** = the shell that runs inside it (the language you type).

**Why this combo (drop these as quick bullets):**
- Built into Windows 11 — nothing extra to install for the terminal itself.
- PowerShell is what Microsoft maintains and updates — it's the modern default.
- Claude Code automatically detects PowerShell and adapts.
- The alternatives: **CMD** is the old black box from the 90s — skip it. **Git Bash** works but is an extra install. **WSL2** (real Linux inside Windows) is the gold standard but takes 20–30 min to set up — that's the "graduation" path once you're serious.

**Demo:** Press `Win` → type "Terminal" → open Windows Terminal. Show the tabs.

---

## 3. Install Node.js (0:05 – 0:10)

**Say:**
> "Claude Code is distributed through something called npm — it comes with Node.js. We install Node.js once, and then we get npm for free."

**Steps on screen:**
1. Open browser → go to **https://nodejs.org**
2. Download the **LTS** version (the green button on the left — "LTS" = Long Term Support, the stable one).
3. Run the installer. **Click Next on every screen** — defaults are fine. Make sure "Add to PATH" stays checked (it is by default).
4. When done, **close any open PowerShell windows** and open a fresh one.

**Verify it worked — paste this in PowerShell:**
```powershell
node --version
npm --version
```
You should see two version numbers (e.g. `v20.11.0` and `10.2.4`). If you see "not recognized," close PowerShell and open a new one.

**Common stumble:** If `node` isn't recognized after install, the user opened PowerShell *before* the install finished. Close and reopen.

---

## 4. Install Claude Code (0:10 – 0:13)

**Paste in PowerShell:**
```powershell
npm install -g @anthropic-ai/claude-code
```

**Say while it installs (~30–60 sec):**
> "The `-g` means 'install globally' — you'll be able to run `claude` from any folder on your computer, not just this one."

**Verify:**
```powershell
claude --version
```

**If you see a permission error:** Open PowerShell as Administrator (right-click → "Run as administrator") and rerun the install command.

---

## 5. Sign in (0:13 – 0:15)

**In PowerShell, type:**
```powershell
claude
```

**What happens:**
- A first-run setup appears.
- It asks how you want to authenticate. Pick **"Sign in with Claude account"** (easiest for non-devs — uses your Claude.ai subscription, no API key needed).
- It opens your browser. Log in with your Claude.ai account, click "Authorize."
- Tab back to PowerShell — you're logged in.

**If they don't have a Claude.ai account:** They can sign up free at claude.ai, but the Pro plan ($20/mo) is what makes Claude Code practical. The alternative is a pay-per-use API key from console.anthropic.com — mention but don't demo (more friction for non-devs).

---

## 6. Live demo (0:15 – 0:25)

> Pick ONE demo. Don't try multiple — you'll run out of time. Pick the one closest to your audience.

### Option A — for marketers/ecomm people (recommended for this audience)
1. Make a folder on Desktop called `demo`.
2. Drop 2–3 sample CSVs in it (orders, products — anything).
3. In PowerShell:
   ```powershell
   cd $HOME\Desktop\demo
   claude
   ```
4. Type:
   > "Look at the CSV files in this folder and tell me what each one contains. Then write me a 1-paragraph summary of what insights I could extract."

### Option B — for founders/ops
1. Drop a PDF (a contract, an invoice, anything) in a `demo` folder.
2. In Claude:
   > "Read the PDF in this folder and pull out every date, dollar amount, and the names of the parties. Put it in a clean table."

### Option C — pure "wow"
1. Empty folder.
2. In Claude:
   > "Build me a simple webpage that lists my top 3 favorite movies with a poster image and one-sentence review for each. Open it in my browser when you're done."

**Narrate while it works:**
- "Notice it's reading the file — that's the Read tool."
- "It asked permission before editing — that's the safety layer."
- "It's writing the file now — see the diff? That's what changed."

---

## 7. What's next + Q&A (0:25 – 0:30)

**Quick "where to go from here" slide:**
- **`/help`** inside Claude shows all built-in commands.
- **`claude --resume`** picks up your last conversation.
- **CLAUDE.md** — a file you put in any folder that teaches Claude your preferences (e.g. "always reply in Arabic," "this folder is a Shopify store, here's the structure").
- **Skills** — pre-built mini-experts (`/skills`).
- **Next level:** WSL2 (Linux on Windows) — smoother for heavy dev work. Worth a follow-up session.

**Ask:**
> "What's the first thing in your work you'd want to hand to Claude?" — collect answers, you now have content for follow-up sessions.

---

## Things to NOT do live (they kill demos)

- Don't install Node.js live — it takes 2–4 min and is boring. Either pre-install on the demo machine or screen-record this part.
- Don't pick the API-key auth path — it requires billing setup at console.anthropic.com and burns 5 min you don't have.
- Don't open multiple terminals — confuses non-devs. One window.
- Don't switch between Claude Code and other apps mid-demo. Stay in the terminal.
- Don't type commands from memory — copy-paste from your prepared notepad.

## If something breaks

| Problem | Fix |
|---|---|
| `node` not recognized | Close PowerShell, open a new one. |
| `npm install` permission error | Run PowerShell as Administrator. |
| `claude` hangs on first run | Make sure browser opened; check firewall isn't blocking. |
| Can't sign in | Use API key path: `claude` → "Use API key" → paste key from console.anthropic.com. |
| Unicode/emoji shows as boxes | Switch font in Windows Terminal settings to "Cascadia Code" or "Cascadia Mono". |
