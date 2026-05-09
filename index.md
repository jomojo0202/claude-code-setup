---
title: Home
layout: default
nav_order: 1
---

# Get Claude Code on your Windows in 30 minutes
{: .fs-9 }

An AI assistant that can read your files, edit them, run commands, and finish tasks for you — right from a single window. No coding background needed.
{: .fs-5 .fw-300 }

[Start the install](#step-1--install-nodejs){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [Download the cheatsheet (PDF)](https://github.com/jomojo0202/claude-code-setup/raw/main/pdfs/03-handout.pdf){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## What you'll have when you're done

- Claude Code installed and signed in on your computer.
- An AI you can ask to: read CSVs, summarize PDFs, write content, build a one-page website, automate small tasks — all by typing what you want.
- A cheatsheet you can come back to next time.

## Before you start

- A Windows 10 or 11 computer.
- A web browser.
- A **Claude.ai** account. Free is fine to test, **Pro ($20/mo) is recommended** for real use.

> **Heads up — what's a terminal?** During the install you'll use **PowerShell** — a window where you type commands instead of clicking buttons. It's already on your computer. We're not installing anything new for the terminal.

---

## Step 1 — Install Node.js

Claude Code is delivered through a tool that comes with Node.js.

1. Open your browser and go to **[nodejs.org](https://nodejs.org)**.
2. Click the **LTS** download button (the green one on the left). LTS = the stable version.
3. Run the installer. Click **Next** on every screen — defaults are correct.
4. When it finishes, **close any PowerShell window that was open** and open a fresh one.

**Open a fresh PowerShell:** press the Windows key, type `Terminal`, press Enter.

**Test it worked.** Paste this into the terminal and press Enter:

```powershell
node --version
npm --version
```

You should see two version numbers like `v20.11.0` and `10.2.4`. If you see "not recognized," close the terminal and open a new one.

---

## Step 2 — Install Claude Code

In the terminal, paste this and press Enter:

```powershell
npm install -g @anthropic-ai/claude-code
```

Wait 30–60 seconds. When you get a prompt back, test it:

```powershell
claude --version
```

> **Permission error?** Close the terminal. Right-click the terminal icon and choose **Run as administrator**. Try the install command again.

---

## Step 3 — Sign in

In the terminal, type:

```powershell
claude
```

A first-run screen appears. Choose **"Sign in with Claude account."**

A browser window opens. Log in with your Claude.ai account, click **Authorize**, then go back to the terminal.

You're in.

---

## Step 4 — Try it

Let's give Claude something real to do.

1. On your Desktop, make a new folder called `claude-test`.
2. In the terminal, run:

   ```powershell
   cd $HOME\Desktop\claude-test
   claude
   ```

3. At the prompt, type any of these:

   > "Make me a simple HTML page that lists my top 3 favorite books with a one-sentence review each. Open it in my browser when done."

   > "Write me three social media post ideas about coffee, in a friendly tone."

   > "Create a checklist for my morning routine, save it as a text file."

Watch what happens. Claude will create the file, ask permission, and open or save it for you.

---

## Useful commands

| Command | What it does |
|---|---|
| `claude` | Start Claude in the current folder |
| `claude --resume` | Continue your last conversation |
| `/help` | Inside Claude, see all commands |
| `/clear` | Inside Claude, start a fresh conversation |
| `cd path\to\folder` | Move the terminal to a folder |
| `exit` (or Ctrl+D) | Leave Claude |

---

## Stuck?

| Problem | Fix |
|---|---|
| `node` is "not recognized" after install | Close the terminal, open a new one, try again. |
| `npm install` fails with permission error | Run the terminal as Administrator (right-click → Run as admin). |
| `claude` won't start | Run `npm install -g @anthropic-ai/claude-code` again. |
| Browser doesn't open during sign-in | Copy the URL it printed, paste into your browser manually. |
| Want to start over | Run `claude`, type `/logout`. Then `claude` again to sign in fresh. |

---

## Where to go next

- Inside Claude, type **`/help`** — explore everything it can do.
- Drop a text file called **`CLAUDE.md`** into any folder. Whatever you write inside teaches Claude your preferences for that folder. Example:

  > "I run a Shopify store. Always answer in Arabic. Never edit files in the `/backups` folder."

- Type **`/skills`** inside Claude to see pre-built experts (marketing, copywriting, ads, and more).
- Read the official docs: **[docs.claude.com/claude-code](https://docs.claude.com/claude-code)**.

---

## Save this page

Bookmark this URL or download the [PDF cheatsheet](https://github.com/jomojo0202/claude-code-setup/raw/main/pdfs/03-handout.pdf) so you can come back to it.
