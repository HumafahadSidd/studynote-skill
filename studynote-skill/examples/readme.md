# Study Notes Skill

Turns raw, messy class notes into clean, formatted weekly study notes.

## What It Does

Paste your raw notes into chat and ask for study notes. The skill:

1. Groups related points into topics (raw notes don't need any structure).
2. Gives each topic a heading and a short bold key-terms list.
3. Cleans up the notes under each topic: fixes spelling and grammar and removes filler, while keeping every fact, number, and formula exactly as given.
4. Ends the document with exactly three review questions covering the whole document.
5. Saves the result as a downloadable file.

It never invents content that isn't in your notes.

## How to Use It

Trigger it with a request such as:

- `/study-notes <topic>` followed by your pasted notes
- "Make study notes from this"
- "Turn these into weekly notes"
- "Clean up and organize my class notes"

### Example

**Input**

```
/study-notes density

density means how much mass is present in a certain volume
formula density = mass / volume
SI unit is kg per cubic metre
```

**Output**: a file with topic sections (heading, bold key terms, cleaned notes) followed by a `## Review Questions` section with three numbered questions.

## Output Format

Each topic follows this order:

```markdown
## Topic Name

**Term** — one-line meaning
**Term** — one-line meaning

- Cleaned-up note
- Cleaned-up note
```

The document closes with:

```markdown
## Review Questions

1. ...
2. ...
3. ...
```

## Settings

These can be edited in `SKILL.md`:

| Setting | Default |
|---|---|
| Review questions per document | 3 (exactly, for the whole document, never per topic) |
| Key terms per topic | 3 to 7, short and bold |
| File format | Markdown (`.md`); Word (`.docx`) only if you ask for it |

## Files

- Output is saved to `/mnt/user-data/outputs/` and named like `study-notes-<topic-or-date>.md`.
- The chat reply stays short (one or two sentences); the file is the deliverable.

## Rules the Skill Follows

- Topics are decided by the skill, based on lecture themes or concept clusters.
- Facts, numbers, and formulas are preserved exactly.
- Review questions ask you to recall or explain rather than answer yes/no.
- If the notes are thin, it still writes three questions, with at least one broader synthesis question.

## Location

`/mnt/skills/plugins/study-notes/SKILL.md`
