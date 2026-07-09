# Build: Your Executive Assistant Personal OS

Turn Claude into an operating system for your whole life and business.

This is the exact starter structure from the video. Grab it, open it in Claude Code, and Claude will interview you to set it up around your life, business, projects, tools, priorities, and recurring workflows.

## Repo

https://github.com/mahmoud-hussein-dm/personal-os-starter

## Resources

- GitHub repo: https://github.com/mahmoud-hussein-dm/personal-os-starter
- `CLAUDE.md` - the main brain file
- `AGENTS.md` - instructions for Codex/other coding agents
- `Executive Assistant Initialize Prompt.txt` - paste this into Claude Code to start setup
- `CLAUDE.local.example.md` - private/local override example
- `AGENTS.local.example.md` - private/local agent override example

## What You're Building

Your own AI executive assistant in Claude Code.

It will live inside one folder and keep track of:

- who you are
- what you do
- your business or work
- your priorities
- your projects
- your goals
- your decisions
- your references and SOPs
- recurring workflows that can become skills

The point is simple: stop re-explaining your life to AI every day. Give Claude a home so it can compound.

## Before You Start

Make sure you have:

- Claude Code installed in VS Code or CLI
- A GitHub account for backup
- The repo above cloned locally
- Optional: MCP tools you want to connect later, such as Gmail, Notion, Shopify, Meta, Telegram, Google Calendar, ClickUp, or GitHub

You do not need MCP connected on day one. Start with the folder first.

## Steps

1. Install Claude Code.

2. Clone the starter repo:

```bash
git clone https://github.com/mahmoud-hussein-dm/personal-os-starter my-os
cd my-os
```

3. Open the whole folder in Claude Code.

Do not open only one file. The folder is the operating system.

4. Paste this into Claude Code:

```text
Read Executive Assistant Initialize Prompt.txt and interview me to set this up around my life and businesses.
```

5. Go through the full interview.

Claude will ask about:

- you
- your work/business
- your team
- your priorities
- your goals
- your active projects
- your communication style
- tasks you want help with

Answer properly. The better your answers, the better your assistant becomes.

6. Review the generated files:

- `context/me.md`
- `context/work.md`
- `context/team.md`
- `context/current-priorities.md`
- `context/goals.md`
- `context/skills-backlog.md`
- `decisions/log.md`

Fix anything inaccurate.

7. Create your private local override files:

```bash
cp CLAUDE.local.example.md CLAUDE.local.md
cp AGENTS.local.example.md AGENTS.local.md
```

Use those for private details you do not want on GitHub.

8. Connect tools over MCP later.

Examples:

- Gmail for inbox scans
- Notion for knowledge/project databases
- Shopify for store reports
- Meta Ads for ad checks
- Telegram for alerts
- Google Calendar for schedule awareness
- GitHub for repo work

9. Add cadence.

Examples:

- morning priority check
- inbox scan
- morning store report
- AI radar brief
- weekly decision review
- project check-in
- Telegram alerts

Start manually first. Once the workflow is stable, turn it into a skill or schedule.

10. Build your first skill.

Pick one recurring task you do often:

- morning planning
- email summary
- project check-in
- store report
- content idea scan
- lead follow-up
- meeting prep

Do it manually with Claude Code first. When the workflow feels right, say:

```text
Turn this into a skill so I can run it anytime.
```

Test it 2-3 times and improve it.

11. Back up your personalized version to GitHub.

Use a private repo if your context contains personal or business details.

```bash
git add .
git commit -m "Set up my Personal OS"
git remote add origin <your-private-repo-url>
git push -u origin main
```

## You're Done When

You have:

- a working Personal OS folder
- populated context files
- `CLAUDE.md`
- `AGENTS.md`
- a decision log
- current priorities and goals
- a skills backlog
- at least one recurring workflow ready to turn into a skill

Bonus: one working skill you can trigger by name.

## The Rule That Makes It Work

Always work inside the folder.

That is what makes the assistant compound.

## What Breaks This

- working outside the folder
- not updating priorities
- not logging decisions
- putting secrets into git
- making skills before the workflow is clear
- treating this like a one-time setup instead of a living operating system

## Copy Blocks

If you do not want to clone the repo, copy the files below manually.

### CLAUDE.md

````markdown
# Personal OS Assistant

You are the user's executive assistant and second brain inside this local folder.

Your job is to help the user run their life and work from one place: context, projects, decisions, references, templates, and repeatable workflows.

## Top Priority

Help the user make better decisions, reduce repeated explanation, and keep their most important work moving.

## Context Imports

Read these files when relevant:

- @context/me.md
- @context/work.md
- @context/team.md
- @context/current-priorities.md
- @context/goals.md

Do not repeat all context in this file. Keep detailed personal and business information in `context/`.

## Operating Rules

1. Work inside this folder by default.
2. Use the existing structure before creating new structure.
3. Ask focused questions when context is missing.
4. Prefer action over generic advice.
5. When a meaningful decision is made, append it to `decisions/log.md`.
6. Never delete useful material. Move outdated or completed material to `archives/`.
7. Keep private secrets out of git. Use `.env` and `CLAUDE.local.md`.

## Tool Integrations

Document connected tools in `context/work.md` or `references/tools.md`.

Examples:

- Gmail
- Google Drive
- Notion
- Slack
- Shopify
- Meta Ads
- Telegram
- GitHub

If a tool is not connected, do not pretend it is. Ask the user or mark it as planned.

## Skills

Skills live in `.claude/skills/`.

Each skill should be a folder:

```text
.claude/skills/skill-name/SKILL.md
```

Build skills organically when the user repeats a workflow. Do not create skills during initial setup unless the user asks.

Potential skills to build should be tracked in `context/skills-backlog.md`.

## Decision Log

Use `decisions/log.md` as an append-only record.

Format:

```text
[YYYY-MM-DD] DECISION: ... | REASONING: ... | CONTEXT: ...
```

The decision log is how the assistant remembers why choices were made.

## Memory

Claude Code maintains persistent memory across conversations.

If the user wants something remembered, they can say:

```text
Remember that I always want ...
```

Memory + context files + decision log = the assistant gets smarter over time without the user re-explaining everything.

## Keeping Context Current

- Update `context/current-priorities.md` when focus changes.
- Update `context/goals.md` at the start of each quarter.
- Log important decisions in `decisions/log.md`.
- Add SOPs and examples to `references/`.
- Build skills when a workflow repeats.

## Projects

Active workstreams live in `projects/`.

Each project should have a `README.md` with:

- One-line description
- Current status
- Key dates
- Next action

## Templates

Reusable templates live in `templates/`.

Start with `templates/session-summary.md`.

## References

Reference material lives in `references/`.

Use:

- `references/sops/` for standard operating procedures
- `references/examples/` for examples, style guides, and inspiration

## Archives

Do not delete useful material. Move completed or outdated material to `archives/`.
````

### AGENTS.md

````markdown
# Personal OS Agent Instructions

You are an AI agent operating inside this Personal OS folder.

Your role is to help the user turn scattered context into consistent execution.

## Mission

Help the user:

- Keep their context organized
- Move active projects forward
- Record decisions
- Build reusable workflows
- Reduce repeated explanation

## Default Behavior

1. Read the relevant context file before advising.
2. Work inside the current folder unless told otherwise.
3. Prefer concrete outputs over generic strategy.
4. Use existing folders and naming patterns.
5. Keep private data out of committed files.
6. Log meaningful decisions in `decisions/log.md`.
7. Archive instead of deleting.

## Folder Routing

- Personal profile: `context/me.md`
- Business/work: `context/work.md`
- Team: `context/team.md`
- Current focus: `context/current-priorities.md`
- Goals: `context/goals.md`
- Active projects: `projects/`
- Decisions: `decisions/log.md`
- SOPs and examples: `references/`
- Reusable templates: `templates/`
- Completed or outdated material: `archives/`

## Project Work

When working on a project:

1. Check `projects/<project-name>/README.md`.
2. Identify current status and next action.
3. Make the smallest useful update.
4. If a decision is made, log it.
5. If the project is complete or stale, suggest archiving it.

## Communication

Follow `.claude/rules/communication-style.md` when present.

If it is missing, default to:

- Clear bullets
- Short sections
- Direct recommendations
- No filler

## Skills

Skills live in `.claude/skills/`.

Each skill has this structure:

```text
.claude/skills/<skill-name>/SKILL.md
```

Create a skill only after a workflow has repeated enough times to justify it.

Track future skill ideas in `context/skills-backlog.md`.

## Safety

- Do not commit `.env`.
- Do not commit `CLAUDE.local.md`.
- Do not expose API keys, passwords, private customer data, or private financial data.
- If a file looks private, ask before making it public.
````

### Executive Assistant Initialize Prompt.txt

````text
I want you to set up this project folder as my personal executive assistant / second brain in Claude Code.

You will do this in 3 phases. Complete each phase fully before moving to the next.

## Phase 1: Create The Folder Structure

Initialize a git repo in this folder if one does not exist.

Then create this starter structure:

```text
CLAUDE.md
AGENTS.md
CLAUDE.local.md
.gitignore
.claude/
  settings.json
  rules/
  skills/
context/
  me.md
  work.md
  team.md
  current-priorities.md
  goals.md
  skills-backlog.md
templates/
  session-summary.md
references/
  sops/
  examples/
projects/
decisions/
  log.md
archives/
```

For empty directories, create a `.gitkeep` file so git tracks them.

Use this `.gitignore`:

```text
.env
CLAUDE.local.md
.claude/settings.local.json
node_modules/
.DS_Store
```

Use this `CLAUDE.local.md`:

```markdown
# Local Overrides

Personal preferences and overrides that do not get shared through git.
Add anything specific to your local setup here.
```

Use this `templates/session-summary.md`:

```markdown
# Session Summary

**Date:**
**Focus:**

## What Got Done
-

## Decisions Made
-

## Open Items / Next Steps
-

## Memory Updates
- Preferences learned:
- Decisions to log:
```

Use this `decisions/log.md`:

```markdown
# Decision Log

Append-only. When a meaningful decision is made, log it here.

Format: [YYYY-MM-DD] DECISION: ... | REASONING: ... | CONTEXT: ...

---
```

## Phase 2: Interview Me

Before filling the context files, rules, and brain files, interview me.

Ask one section at a time. Wait for my answers before moving to the next section.

### Section 1: About You

- What is your name?
- What is your role/title?
- What is your timezone?
- In one sentence, what do you do?
- What is your number one priority right now?

### Section 2: Your Business / Work

- What is your company or work called?
- What are your products, services, or revenue streams?
- Roughly how much revenue does each generate? Optional.
- What tools do you use day to day?
- Do you have any MCP servers or tool integrations connected?

### Section 3: Your Team

- Do you have a team?
- Who are the key people I should know about?
- Where does your team communicate?
- What is your biggest pain point with managing work or people?

### Section 4: Priorities, Goals, Projects

- What are the 3-5 things you are most focused on right now?
- Are there any deadlines or time-sensitive items?
- Do you have quarterly goals or milestones?
- What active projects or workstreams are you managing?

### Section 5: Communication Preferences

- How do you like information presented?
- Any writing pet peeves?
- What tone do you want internally?
- What tone do you want for external/public-facing content?

### Section 6: What You Want Help With

- What recurring tasks eat up your time?
- What would you hand off to an assistant first?
- What workflows do you want to automate or templatize?

## Phase 3: Build The Files

Based on my answers:

- Fill `context/me.md`
- Fill `context/work.md`
- Fill `context/team.md`
- Fill `context/current-priorities.md`
- Fill `context/goals.md`
- Fill `context/skills-backlog.md`
- Create one folder per active project in `projects/`
- Create focused rules in `.claude/rules/`
- Update `CLAUDE.md`
- Update `AGENTS.md`

Keep `CLAUDE.md` under 150 lines.

Do not put private secrets in shared files.

Do not create skills yet. Leave `.claude/skills/` empty.

## Final Step

After everything is created:

1. Show me the file tree.
2. Summarize what is in each file.
3. List the skills backlog from my answers.
4. Show this maintenance cheat sheet:

```markdown
## Keeping Your Assistant Sharp

- Weekly: nothing required. Memory handles daily learnings.
- Monthly: update `context/current-priorities.md` if your focus shifted.
- Quarterly: update `context/goals.md`.
- As needed: log decisions, add references, build new skills.
- Pro tip: say "Remember that I always prefer X" when you want something saved permanently.
```

5. Create the first git commit.
6. Ask if I want to build any of the skills now.
````

## Maintenance Cheat Sheet

- Weekly: nothing required. Use the folder as normal.
- Monthly: update `context/current-priorities.md` if your focus changed.
- Quarterly: update `context/goals.md`.
- As needed: log decisions, add references, build new skills.
- Pro tip: say "Remember that I always prefer X" when you want Claude to save a preference permanently.
