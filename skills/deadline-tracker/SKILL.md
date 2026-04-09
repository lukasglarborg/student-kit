---
name: Deadline Tracker
description: >
  Track assignment deadlines, due dates, and upcoming deliverables with urgency color-coding.
  MANDATORY TRIGGERS: Activate when user says "deadline", "due date", "when is X due",
  "add deadline", "what's due", "afleveringer", "assignment due", "hand in",
  "submission", "aflevering", "upcoming deadlines", "what do I need to submit".
---

# Deadline Tracker

Keep track of every deadline so nothing slips through the cracks.

## Data File

Maintain `workspace/deadlines.md`:

```markdown
# Deadlines

| Assignment | Course | Due Date | Status | Priority | Notes |
|-----------|--------|----------|--------|----------|-------|
| Essay on X | History | 2025-03-15 | in progress | high | 2000 words |
| Problem Set 4 | Math | 2025-03-12 | not started | high | Ch. 7-8 |
| Group Project | CS | 2025-04-01 | in progress | medium | Meeting Thu |
| Lab Report | Physics | 2025-03-20 | done | - | Submitted |
```

### Status Values
- `not started`
- `in progress`
- `done`

### Priority
- `high` — due within 3 days or high-weight assignment
- `medium` — due within 7 days
- `low` — due in 7+ days
- Auto-update priority based on time remaining

## Adding Deadlines

When user mentions a deadline (explicitly or in conversation):

1. Extract: assignment name, course, due date
2. Confirm with user: **"Adding: [assignment] for [course], due [date]. Correct?"**
3. Add to `workspace/deadlines.md`

If info is incomplete, ask only what's missing. Don't make them fill out a form.

### Auto-Detection

If user mentions something like "I have an essay due Friday" in normal conversation, flag it:
**"Sounds like a deadline — want me to track it?"**

Don't add without confirmation.

## Viewing Deadlines

When asked "what's due" or similar, show upcoming deadlines sorted by date:

```
--- UPCOMING DEADLINES ---

🔴 Problem Set 4 (Math) — due in 2 days (Mar 12)
   Status: not started

🟡 Essay on X (History) — due in 5 days (Mar 15)
   Status: in progress

🟢 Group Project (CS) — due in 21 days (Apr 1)
   Status: in progress

✅ Lab Report (Physics) — submitted
```

### Urgency Color-Coding

- 🟢 Green: more than 7 days away
- 🟡 Yellow: 3-7 days away
- 🔴 Red: less than 3 days away
- 🔴 **OVERDUE**: past due date, not marked done

## Updating Status

When user says they finished something or started working on it, update the status. Quick confirmation: **"Marked [assignment] as done."**

## Integration

- Weekly review skill pulls from this file for planning
- Daily briefings can reference upcoming deadlines
- Pomodoro sessions can link to specific assignments

## RULES

- NEVER overwrite `workspace/deadlines.md` — edit specific rows or append new ones
- Read `workspace/profile.md` for course context
- Keep responses SHORT — just show what's relevant
- Sort by due date, closest first
- Remove completed items after 7 days (move to an archive section at bottom)
- Don't nag. Show deadlines when asked or when relevant.
- If a deadline is overdue and not done, mention it once. Don't repeat.
- Always confirm before adding a new deadline
- Mental health: if a student expresses serious distress about deadlines, suggest professional resources (campus counseling, crisis lines). Don't try to be a therapist.
- Academic integrity: help students learn, never do their work for them
- Use `workspace/` prefix for all file paths
