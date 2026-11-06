# Project file

A reusable skill for AI agents on multi-day work. Instead of relying on chat history, the agent keeps a short project `.md` and reads that file first whenever it resumes.

## Why

Chat history is expensive and easy to lose after a summary. A project file keeps the durable parts small and easy to reopen: the goal, decisions, rejected options, what's done, the next step, and open questions.

## What goes in the file

- **Goal**
- **Decisions** — what you chose and why (dated, with timezone)
- **Rejected** — options considered, why they were dropped, and `revisit if` (the condition under which the path is worth trying again, or `never` if it is truly dead). On resume, skip `never`. If a revisit condition is now true, move that item to Next step or Open questions instead of retrying it blindly or ignoring it.
- **Done**
- **Next step**
- **Open questions**

Update the file after every step or decision. Keep it short: replace stale lines rather than appending forever. When the project is finished, archive the file.

## How to use it

1. Copy `SKILL.md` into your agent's skills folder (in Grok Bot, save it as a skill; in Cursor, put it under `.cursor/skills/project-file/`).
2. Tell the agent this is a multi-day project, or ask it to use the project file skill.
3. The agent should also save a memory note (or similar pointer) with the file path, and read the file first on resume.

In Grok Bot, project files live at `/workspace/projects/<short-slug>.md` and move to `/workspace/projects/archive/` when done.

## License

You're free to copy, share, and adapt this.
