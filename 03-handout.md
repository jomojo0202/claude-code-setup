# Claude Code on Windows — Setup Cheatsheet

> Keep this open. Follow it step by step. ~15 minutes start to finish.

---

## What you're installing and why

| Thing | What it is |
|---|---|
| **Windows Terminal** | The window with tabs. Already on Windows 11. |
| **PowerShell** | The "language" you type inside the window. Already there. |
| **Node.js** | A piece of software that includes `npm`, the installer Claude Code uses. |
| **Claude Code** | The AI assistant itself. |

**Why PowerShell and not something else?**
PowerShell is built into Windows, modern, and Microsoft maintains it. CMD is the old one — skip it. Git Bash is fine but an extra install. WSL2 (Linux on Windows) is the most powerful option — try it once you're comfortable.

---

## Step 1 — Install Node.js

1. Open your browser. Go to **https://nodejs.org**
2. Click the **LTS** download button (the green one on the left).
3. Run the downloaded installer.
4. Click **Next** on every screen. Defaults are correct.
5. Click **Install**. Wait until it finishes.
6. Close any PowerShell windows that were open. Open a fresh one.

**Test it worked.** Open PowerShell (press `Win`, type "Terminal", press Enter). Paste:

```powershell
node --version
npm --version
```

You should see two version numbers like `v20.11.0` and `10.2.4`. If you see "not recognized" — close PowerShell and open a new window.

---

## Step 2 — Install Claude Code

In PowerShell, paste this and press Enter:

```powershell
npm install -g @anthropic-ai/claude-code
```

Wait 30–60 seconds. When the prompt comes back, test it:

```powershell
claude --version
```

**If you get a permission error:** Close PowerShell. Right-click the PowerShell icon and choose **Run as administrator**. Try the install command again.

---

## Step 3 — Sign in

In PowerShell, type:

```powershell
claude
```

A first-run screen appears. Choose **"Sign in with Claude account."**

A browser window opens. Log in with your Claude.ai account, click **Authorize**, then go back to PowerShell. You're in.

> **No Claude.ai account?** Sign up free at **claude.ai**. To use Claude Code regularly, get the Pro plan ($20/mo).

---

## Step 4 — Try it

1. On your Desktop, make a folder called `claude-test`.
2. In PowerShell, run:
   ```powershell
   cd $HOME\Desktop\claude-test
   claude
   ```
3. At the prompt, type:
   > "Make me a simple HTML page that lists my top 3 favorite books with a one-sentence review for each. Open it in my browser when done."

Watch what happens. Claude will create a file, ask permission, and open it for you.

---

## Useful commands

| Command | What it does |
|---|---|
| `claude` | Start Claude in the current folder |
| `claude --resume` | Continue your last conversation |
| `/help` | Inside Claude, shows all commands |
| `/clear` | Inside Claude, start a fresh conversation |
| `/skills` | Inside Claude, see available pre-built experts |
| `cd path\to\folder` | Move PowerShell to a folder |
| `exit` (or Ctrl+D) | Leave Claude |

---

## Common problems and fixes

| Problem | Fix |
|---|---|
| `node` is "not recognized" after install | Close PowerShell. Open a new window. Try again. |
| `npm install` fails with permission error | Run PowerShell as Administrator (right-click → Run as admin). |
| `claude` won't start | Make sure Node installed. Run `npm install -g @anthropic-ai/claude-code` again. |
| Browser doesn't open during sign-in | Copy the URL it printed and paste into your browser manually. |
| Emoji or special characters look like boxes | In Windows Terminal: Settings → Profiles → PowerShell → Appearance → Font face → "Cascadia Mono". |
| Want to start over | Run `claude` then type `/logout`. Then `claude` again to sign in fresh. |

---

## What to learn next

- **CLAUDE.md** — Drop a text file called `CLAUDE.md` in any folder. Whatever you write inside teaches Claude your preferences for that folder. Example: "I run a Shopify store. Always answer in Arabic. Never edit files in /backups."
- **Skills** — Pre-built experts. Type `/skills` inside Claude to see them.
- **MCP servers** — Connect Claude to outside tools (Gmail, Google Drive, Shopify, etc.).
- **WSL2** — Run real Linux inside Windows. More powerful, more setup. Worth it once you're comfortable.

---

## Where to get help

- Inside Claude, type `/help`
- Docs: **https://docs.claude.com/claude-code**
- Report bugs: **https://github.com/anthropics/claude-code/issues**
