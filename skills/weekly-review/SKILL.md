---
name: Weekly Review
description: >
  Sunday planning and weekly reflection. Review what was studied, plan next week, track progress.
  MANDATORY TRIGGERS: Activate when user says "weekly review", "plan next week",
  "sunday planning", "ugentlig review", "how was my week", "week summary",
  "weekly plan", "plan my week", "this week", "next week plan".
---

# Weekly Review

Quick Sunday ritual: look back at the week, plan the next one. Under 5 minutes.

## Flow

### 1. Read Context

- Read `workspace/profile.md` for courses and schedule
- Read `workspace/pomodoro-log.md` for this week's study data (if exists)
- Read `workspace/deadlines.md` for upcoming deadlines (if exists)
- Read `workspace/Sessions/weekly-reviews.md` for last week's review (if exists)

### 2. Review the Week (2 min)

Present a quick summary:

```
--- WEEK IN REVIEW: [date range] ---

Study time: [X] sessions ([Y] hours)
  - [Course A]: [sessions] sessions
  - [Course B]: [sessions] sessions

Assignments completed: [list or "none tracked"]
Deadlines met/missed: [list or "none tracked"]
```

Then ask:
- **"What went well this week?"**
- **"What was hard?"**
- **"Anything you want to change?"**

Keep answers brief. One sentence each is perfect.

### 3. Plan Next Week (2 min)

Check deadlines for next 7-14 days, then help plan:

- **Priority assignments** — what's due soonest?
- **Courses needing attention** — any falling behind?
- **Study blocks** — suggest realistic blocks based on their schedule
- **Exam prep** — if exams are coming, flag them early

Present as a simple plan:

```
--- NEXT WEEK PLAN ---

Must do:
- [ ] [Assignment] — due [date]
- [ ] [Assignment] — due [date]

Study focus:
- [Course] — needs more time (only [X] sessions last week)
- [Course] — on track

Suggested study blocks:
- Mon/Wed/Fri: [Course A] (morning)
- Tue/Thu: [Course B] (afternoon)
```

### 4. Save

Append to `workspace/Sessions/weekly-reviews.md`:

```markdown
## Week of [date range]

### Review
- Study: [X] sessions ([Y] hours)
- Completed: [list]
- Went well: [user's answer]
- Was hard: [user's answer]
- Change: [user's answer]

### Plan
- Priority: [list]
- Focus courses: [list]
- Study blocks: [schedule]
```

## If No Data Exists

First time? No pomodoro logs? That's fine.

- Skip the data summary
- Still ask the reflection questions
- Still plan next week
- Mention: "If you use focus sessions this week, I can give you real numbers next Sunday."

## RULES

- NEVER overwrite `workspace/Sessions/weekly-reviews.md` — always append
- Read `workspace/profile.md` for context
- Keep the whole review under 5 minutes — students won't do it if it's long
- Be honest about the data. If they studied 2 hours all week, say so. Don't sugarcoat.
- Don't over-schedule. Students have lives.
- Suggest realistic plans based on what they actually did, not what they "should" do
- If last week's plan was ignored, don't guilt-trip. Just ask what happened.
- Mental health: if a student expresses serious distress, suggest professional resources (campus counseling, crisis lines). Don't try to be a therapist.
- Academic integrity: help students learn, never do their work for them
- Use `workspace/` prefix for all file paths
