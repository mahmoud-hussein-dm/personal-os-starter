# Personal OS Starter

Build your own AI executive assistant / second brain inside one local folder.

This is a public starter version of the system shown in the video. It is intentionally generic: no private context, no secrets, no personal business data. Clone it, open it in Claude Code or another coding agent, run the initialize prompt, and let the assistant interview you to personalize the system.

## What This Gives You

- A local folder structure for your life, business, projects, decisions, and reference material
- A `CLAUDE.md` brain file for Claude Code
- An `AGENTS.md` brain file for Codex or other coding agents
- Local override examples: `CLAUDE.local.example.md` and `AGENTS.local.example.md`
- A guided initialize prompt that interviews you and fills the system around your real life
- A decision log so your assistant compounds instead of forgetting
- A skills folder for workflows you repeat often

## Quick Start

```bash
git clone https://github.com/mahmoud-hussein-dm/personal-os-starter my-personal-os
cd my-personal-os
```

Then open the folder in Claude Code and paste:

```text
Read Executive Assistant Initialize Prompt.txt and run Phase 1. Then interview me section by section for Phase 2.
```

Do not paste private secrets into the repo. Use `.env` and `CLAUDE.local.md` for local/private details.

## How It Works

The system has four layers:

1. Context: who you are, what you do, goals, priorities, team, projects
2. Connection: tool integrations and references your assistant can use
3. Capability: rules, skills, templates, and workflows
4. Cadence: regular check-ins, reviews, decision logs, and repeated workflows

The key rule: always work inside this folder. That is what makes the assistant compound.

## File Map

```text
CLAUDE.md
AGENTS.md
CLAUDE.local.example.md
AGENTS.local.example.md
Executive Assistant Initialize Prompt.txt
lesson/lesson-instructions.md
lesson/youtube-description-and-chapters.md
context/
projects/
decisions/log.md
templates/session-summary.md
references/
archives/
.claude/
```

## What To Customize First

- `context/me.md`
- `context/work.md`
- `context/current-priorities.md`
- `context/goals.md`
- `CLAUDE.local.md`
- `.claude/rules/communication-style.md`

## Maintenance

- Monthly: update `context/current-priorities.md`
- Quarterly: update `context/goals.md`
- As needed: append meaningful decisions to `decisions/log.md`
- When you repeat a workflow 3+ times: turn it into a skill in `.claude/skills/`
