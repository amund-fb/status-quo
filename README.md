# Getting Started with Claude Code on Windows
> For someone who has never coded before. You'll be fine.

## What you're about to do
1. Install Git (a tool Claude Code needs internally)
2. Install Claude Code (the AI coding assistant)
3. Open this project folder and start talking to it

Total time: ~10 minutes.

---

## Step 1: Install Git for Windows

Claude Code needs Git installed to work on Windows.

1. Go to **https://git-scm.com/download/win**
2. Download the installer
3. Run it — click **Next** on every screen (all defaults are fine)
4. Make sure **"Add Git to PATH"** is checked (it is by default)
5. Finish the install

---

## Step 2: Install Claude Code

1. Open **Terminal** from your Start menu
   - Search for "Terminal" or "PowerShell" and open it
   - You'll see a dark window with a blinking cursor — this is where you type commands

2. Copy-paste this command and press Enter:
   ```
   irm https://claude.ai/install.ps1 | iex
   ```

3. Wait for it to finish. You should see "Claude Code successfully installed!"

4. **Close the Terminal window completely and open a new one**
   (This refreshes the system so it can find the `claude` command)

5. Type `claude --version` and press Enter to verify it works

### If "claude" is not recognized:
This is a common Windows quirk. The fix:
- Press **Win + R**, type `sysdm.cpl`, press Enter
- Go to **Advanced** tab → **Environment Variables**
- Under "User variables", find **Path** → click **Edit** → click **New**
- Add: `C:\Users\YOUR_USERNAME\.local\bin` (replace YOUR_USERNAME with your actual Windows username)
- Click OK everywhere, then **restart Terminal**

---

## Step 3: Log in

1. In Terminal, type `claude` and press Enter
2. A browser window will open — sign in with your Claude account
3. You're in!

---

## Step 4: Open this project

1. Put this entire `friendly-beast-newsletter` folder somewhere on your computer
   (e.g., `C:\Users\YourName\Projects\friendly-beast-newsletter`)

2. In Terminal, navigate to the folder:
   ```
   cd C:\Users\YourName\Projects\friendly-beast-newsletter
   ```

3. Type `claude` and press Enter

4. Claude Code will read the CLAUDE.md file and understand the project

---

## Step 5: Start learning

Here are things to try, in order of difficulty:

### Week 1 — Understand
Talk to Claude Code like a person. Ask questions:
```
What does the ai-newsletter-generator.jsx file do?
Explain the generateSystemPrompt function to me like I'm a beginner
What is React?
What does the SECTIONS array control?
How does the API call work?
```

### Week 2 — Make changes
Ask Claude Code to modify the newsletter:
```
Add a "Copy to clipboard" button below the newsletter
Change the header color to match Friendly Beast brand — use black and a teal green accent
Add a fifth section called "What to build next" for internal tool ideas
Make the analyst note section more prominent with a bigger font
```

### Week 3 — Build context
```
/init
```
This generates or updates the CLAUDE.md. Start customizing it.
Also try:
```
/help
/doctor
/model
```

### Week 4 — Build something new
```
Build me a simple client onboarding checklist generator for Friendly Beast
Build a tool that takes a BigQuery table schema and generates a SKILL.md for Claude
```

---

## Useful commands inside Claude Code

| Command | What it does |
|---------|-------------|
| `/help` | Show all available commands |
| `/doctor` | Run diagnostics — check if everything is working |
| `/clear` | Clear conversation history |
| `/compact` | Summarize conversation to save context space |
| `/model` | Switch between Sonnet (fast/cheap) and Opus (powerful) |
| `/init` | Generate or update the CLAUDE.md file |
| `/cost` | Show how many tokens you've used this session |

---

## Tips for non-coders

- **You can't break anything permanently.** Claude Code asks before changing files. And Git (which you just installed) keeps a history of every change, so you can always go back.
- **Talk in plain English.** You don't need to know programming terms. "Make the text bigger" works just as well as "increase the font-size to 18px."
- **Start small.** Ask Claude Code to explain things before asking it to change things.
- **Use /plan for big changes.** Type `/plan` before a complex request and Claude Code will think through the approach before touching any files.
- **Your Pro subscription covers this.** No extra cost beyond your $20/month Claude plan.
