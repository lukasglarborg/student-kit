---
name: setup
description: >
  Student onboarding and workspace setup.
  MANDATORY TRIGGERS: Use this skill when the user says "setup", "get started",
  "configure", "onboarding", "new student", "start", "install", "first time",
  "set up", "initialize", "init", or when no profile.md exists in workspace/.
---

# Setup — Student Onboarding

You are setting up a new student workspace. This is the user's first experience — make it smooth, fast, and friendly.

## FLOW (max 7 questions, strict order)

### Step 1: Language (ALWAYS FIRST)
Greet with a multilingual welcome:

```
Welcome! / Velkommen! / Willkommen! / Bienvenue! / Bienvenido! / Benvenuto! / Bem-vindo! / Welkom! / Välkommen!

What language do you prefer? Type it or pick a flag:
🇬🇧 English  🇩🇰 Dansk  🇩🇪 Deutsch  🇫🇷 Français  🇪🇸 Español
🇮🇹 Italiano  🇵🇹 Português  🇳🇱 Nederlands  🇸🇪 Svenska
(or type any other language)
```

From this point on, ALL communication is in the chosen language.

### Step 2: Name
Ask their first name. Keep it casual.

### Step 3: Field of study
Ask what they study — major, field, or program. Examples help: "Computer Science, Medicine, Business, Literature..."

### Step 4: Year/Level
Ask their year or level. Adapt to their system: "1st year", "semester 4", "bachelor", "master", "PhD", etc.

### Step 5: Biggest academic challenge
Ask what they struggle with most. Examples: "staying organized", "exam prep", "writing papers", "understanding concepts", "time management". This shapes how the assistant prioritizes help.

### Step 6: Current organization method
Ask how they currently organize their studies:
- Apps (which ones?)
- Paper/notebook
- Nothing / chaos
- Other

### Step 7: Study style
Ask their preferred learning style:
- Visual (diagrams, charts, mind maps)
- Reading/writing (textbooks, notes)
- Practice (exercises, problems, doing)
- Mixed

Also ask: do they prefer direct/blunt feedback or gentle/encouraging? (One sub-question, not a separate step.)

## AFTER QUESTIONS — CREATE WORKSPACE

### Create profile.md
Save to `workspace/profile.md`:

```markdown
# Student Profile

- **Name:** [name]
- **Language:** [language]
- **Field:** [field of study]
- **Level:** [year/level]
- **Challenge:** [biggest challenge]
- **Organization:** [current method]
- **Study style:** [style]
- **Communication:** [direct/encouraging]
- **Setup date:** [date]
```

### Create folder structure
```
workspace/
  profile.md
  Courses/
  Assignments/
  Notes/
  Exams/
  Inbox/
  Sessions/
```

Create a short `workspace/README.md` explaining each folder (2-3 words per folder, nothing more).

### Quick demo
After setup, show 3 quick examples of what they can do now:
1. "Try saying: **note: [something from today's lecture]**" (quick-capture)
2. "Try saying: **plan my week**" (study-planner)
3. "Try saying: **explain [a concept from your field]**" (concept-explainer)

Keep the demo to 3 lines. Don't over-explain.

## RULES
- NEVER overwrite an existing profile.md — if one exists, ask if they want to update it
- NEVER skip the language question — it is ALWAYS first
- NEVER ask more than 7 questions total
- Keep each question to 1-2 sentences max
- If user gives multi-part answers, skip already-answered questions
- All paths use workspace/ prefix
- After setup, confirm everything with a short summary (3-5 lines max)
- Read profile.md at the start to check if setup was already done
