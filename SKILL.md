---
name: cross-runtime-handoff
description: Coordinate async work with Claude or another AI runtime through a project-local HANDOFF.md. Use when AGENTS.md references cross-runtime-handoff, when a HANDOFF.md exists in the active project, or when the user asks for native conversation or coordination between runtimes (open set).
---

# Cross-Runtime Handoff

## Purpose

Use this skill to collaborate with another runtime through a shared project file. The protocol lets each runtime leave compact working notes, questions, disagreements, and next-step requests without making the user relay context manually.

The handoff file is a conversation between runtimes, not a status report for the user. Write like a capable peer leaving a note on the bench: short, specific, and useful.

## Session Start

When the active project contains `HANDOFF.md`, read it near session start before making project decisions. Treat it as live collaboration context for that project.

If `AGENTS.md` references `cross-runtime-handoff`, use this skill as the protocol definition for that reference.

If the user asks for native conversation with Claude, cross-runtime coordination, or a handoff, create or update the project-local `HANDOFF.md` using the format below.

## HANDOFF.md Location

Place `HANDOFF.md` at the root of the active project folder unless the user names a different coordination file.

One project = one handoff log. Use project-relative paths inside entries when they are clear; use absolute paths only when ambiguity matters.

## Entry Format

Append entries in this shape:

```md
---
**[Runtime] — [Date] [Time]**
**Touched:** [files modified or reviewed]
**Did:** [what changed or what was checked]
**Assessment:** [current judgment, uncertainty, disagreement, or confidence]
**For next runtime:** [specific request, question, or next useful angle]
---
```

Use the user's local date/time when practical. If exact local time is not available, use the current date and a clear runtime label.

Runtime labels should be concise: `Codex`, `Claude`, `[Runtime Name]` (open set).

## Writing Rules

Append only. Preserve previous entries exactly. The accumulation is the shared memory for that project.

Keep entries short. Aim for under ~500 characters unless the handoff itself is the work. Put detailed reasoning in the touched file, commit message, PR, or user-facing response; summarize only the useful coordination point in `HANDOFF.md`.

Name the actual judgment. If the previous runtime's approach seems wrong, fragile, incomplete, or excellent, say that plainly and ground it in files or behavior.

Write a new entry only when it adds useful information. Agreement without new evidence is noise.

Make `For next runtime` actionable. Ask for a specific check, pressure test, implementation angle, or decision point.

When acting on a previous request, reference it directly:

```md
**Did:** Re: [Runtime]'s [Date] note on [topic] — [resolution].
```

## When To Write

Write after substantive edits to shared project files, after reviewing another runtime's work, when you identify a question better suited to another runtime, or when the user explicitly asks for cross-runtime coordination.

Skip entries for tiny typo fixes, purely local scratch work, and changes the user scoped to one runtime.

## Codex Tool Translation

Other runtimes may mention tools Codex does not have. Translate tool names into outcomes.

Claude/Desktop Commander `read_multiple_files` → use `Get-Content -Raw`, `rg`, targeted shell reads, or parallel shell reads.

Claude/Desktop Commander `edit_block` → use `apply_patch` for surgical edits.

Claude/Desktop Commander `write_file append/rewrite` → use `apply_patch` for durable Markdown changes.

Claude-specific "memory files" → do not create memory files. Use the project files, `HANDOFF.md`, a relevant skill, or the Forge when the user has established one.

Reference work by file path and result, not by tool name. Prefer "updated `SKILL.md` entry format" over "used edit_block."

## Conflict Handling

When runtimes disagree, keep both views in the log. Do not erase or rewrite another runtime's entry.

If the disagreement affects user intent, project direction, destructive edits, or irreversible work, leave the conflict in `HANDOFF.md` and ask the user to decide.

If the disagreement is technical and reversible, make the best local judgment, explain it in the entry, and leave a concrete review request for the next runtime.

## Template

Use this compact template when creating a new `HANDOFF.md`:

```md
# HANDOFF

Append-only cross-runtime notes for this project. Keep entries short, specific, and useful.

---
**[Runtime] — [Date] [Time]**
**Touched:** [files modified or reviewed]
**Did:** [what changed or what was checked]
**Assessment:** [current judgment, uncertainty, disagreement, or confidence]
**For next runtime:** [specific request, question, or next useful angle]
---
```
