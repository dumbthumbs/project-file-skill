---
name: Project file
description: >-
  Use when starting or resuming any task that will span multiple days,
  decisions, or steps, or when the user says 'multi-day project' or 'project
  file'.
---
# Steps
1. At the start, create a project file (.md) under /workspace/projects/<short-slug>.md with sections: Goal, Decisions (what and why, dated PT), Rejected (options considered, why they were dropped, and `revisit if` or `never`, dated PT), Done, Next step, Open questions.
2. Save one memory note with the project name and the file's path, and say to read it first when resuming.
3. After every step or decision, update the file (keep it short; replace stale lines rather than appending forever). When a path is rejected, log it under Rejected with why and `revisit if` (the condition under which it is worth trying again, or `never` if it is truly dead).
4. When resuming, read the file first instead of relying on chat history. Skip anything marked `revisit if: never`. If a revisit condition is now true, move that item to Next step or Open questions instead of retrying it blindly or ignoring it.
5. When the project is finished, mark it done, move it to /workspace/projects/archive/, and update the memory note. Offer a Page only if the user wants a nicer record.
