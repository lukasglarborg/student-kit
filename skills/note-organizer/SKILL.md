---
name: note-organizer
description: >
  Organize and enhance messy lecture notes.
  MANDATORY TRIGGERS: Use this skill when the user says "organize notes",
  "clean up notes", "lecture notes", "notes from today", "noter fra",
  "organize my notes", "fix my notes", "structure notes", "Notizen",
  "notes de cours", "apuntes", "appunti", "anteckningar", "tidy up notes",
  "my notes are a mess", "here are my notes", "I took notes",
  "class notes", "reading notes", "sort my notes", "summarize notes".
---

# Note Organizer — Clean Up & Enhance Lecture Notes

You take messy, incomplete, shorthand notes and turn them into clean, structured, useful study material. You fill gaps, add structure, and make notes actually useful for review.

## STARTUP
- Read `workspace/profile.md` for language, field, and study style
- Check `workspace/Notes/` for existing course notes and the cumulative summary

## WHEN THE STUDENT DUMPS NOTES

### Step 1: Identify course and topic
- Ask what course and topic (if not obvious from the content)
- Check if `workspace/Notes/[course]/` exists — if not, create it

### Step 2: Process the raw notes
Take the messy input and:

1. **Structure it** — add clear headings, subheadings, and bullet points
2. **Fill gaps** — where notes are incomplete or shorthand, expand to full sentences/ideas (mark expanded content so the student knows what you added)
3. **Highlight key concepts** — bold important terms, definitions, and formulas
4. **Add connections** — note how this topic connects to previous topics (if prior notes exist)
5. **Fix errors** — correct obvious factual errors, typos, broken sentences

### Step 3: Create the organized note

Format:
```markdown
# [Course] — [Topic]
**Date:** [date]
**Lecture/Session:** [number if known]

## Summary (TL;DR)
[3-5 bullet points covering the main takeaways]

## Key Concepts
- **[Term]** — [definition/explanation]
- **[Term]** — [definition/explanation]

## Detailed Notes

### [Subtopic 1]
[organized content]

### [Subtopic 2]
[organized content]

## Questions / Unclear Points
- [anything that was unclear or incomplete in the original notes, flagged for follow-up]

## Connections to Previous Topics
- Links to [previous topic] because [reason]

---
*Organized from raw notes. Sections marked with [expanded] were filled in by the assistant — verify these.*
```

Save to: `workspace/Notes/[course]/[YYYY-MM-DD]-[topic-slug].md`

### Step 4: Update cumulative course summary
Check if `workspace/Notes/[course]/course-summary.md` exists.

If YES — append the new topic:
```markdown
## [Topic] — [date]
- [key point 1]
- [key point 2]
- [key point 3]
```

If NO — create it:
```markdown
# [Course] — Cumulative Summary

This summary grows as new lecture notes are added throughout the semester.

## [Topic] — [date]
- [key point 1]
- [key point 2]
- [key point 3]
```

The cumulative summary is a living document — by the end of the semester, it becomes a full course overview.

## CROSS-REFERENCING

When organizing notes, check `workspace/Notes/[course]/` for existing notes:
- If the current topic builds on a previous one, add a link: "See also: [previous-note-file]"
- If a concept was mentioned in earlier notes, reference it
- Flag contradictions between current and previous notes (the student should verify which is correct)

## BATCH PROCESSING

If the student has multiple sets of notes to organize:
- Process them one at a time
- Ask if they want to dump them all at once or go through them
- For batch mode, show a brief confirmation after each one is processed

## READING NOTES

If the notes are from a textbook or reading (not a lecture):
- Same process, but label as "Reading notes" instead of "Lecture notes"
- Include page numbers or chapter references if provided
- Save to same location: `workspace/Notes/[course]/[date]-reading-[topic].md`

## RULES
- NEVER overwrite existing note files — create new files or append
- NEVER delete or modify the student's original meaning — enhance, don't change
- NEVER present expanded/filled content as if the student wrote it — always mark with [expanded]
- NEVER skip the summary at the top — it's the most valuable part for review
- All paths use workspace/ prefix
- Read profile.md for language and field
- If notes reference concepts you're not sure about, flag them as [verify] rather than guessing
- Keep the organized version close to the student's language and terminology
- The cumulative course summary is APPEND-ONLY — never remove previous entries
- If the student provides notes in a language different from their profile, use the notes' language (they may be taking a course in another language)
