---
name: "study-notes"
description: Turns raw class notes into formatted weekly study notes. Use when the user asks for "study notes" or "weekly notes", or pastes raw class notes and asks to clean them up, organize them, or make them something to study from. Groups the notes into topics, gives each topic a heading and a short bold key-terms list, and ends with exactly three review questions. Always use this skill for that request instead of improvising a format.
---

# Weekly Study Notes

## Settings (edit these to make it yours)

- Review questions at the end: 3 (exactly this many, for the whole document)
- Key terms per topic: 3 to 7, short and bold
- Default file format: Markdown (.md). Use Word (.docx) only if the user asks for it

## Instructions

When asked for study notes or weekly notes:

1. Take the raw class notes the user pastes in chat.
2. Group related points into topics yourself. The raw notes will not have clean
   sections, so decide what counts as one topic (a lecture theme or concept cluster).
3. For each topic, in this order:
   - A heading (`## Topic Name`)
   - A short bold key-terms list: `**Term** — one-line meaning`
   - The topic's notes, cleaned up (fix spelling and grammar, remove filler, keep
     every fact, number, and formula exactly as given)
4. After all topics, add one final section, `## Review Questions`, with exactly
   three numbered questions covering the whole document. Never three per topic and
   never a different count. Prefer questions that ask the user to recall or explain,
   not yes/no.
5. Save the result as a downloadable file in `/mnt/user-data/outputs/` (named like
   `study-notes-<topic-or-date>.md`) and share it with `present_files`. For a Word
   file, read `/mnt/skills/public/docx/SKILL.md` first and follow it.
6. Keep the chat reply to one or two sentences. The file is the deliverable.
7. Never invent content that is not in the user's notes. If the notes are too thin
   for three good questions, still write three, making at least one a broader
   synthesis question.

## Example

User: "Weekly notes: cell resp has glycolysis first, no oxygen needed, then krebs
in mitochondria, then ETC makes most ATP. french rev, big debt from wars, third
estate paid most tax, estates general 1789."
Result: A file with two topics (Cellular Respiration, The French Revolution: Causes),
each with a heading, a bold key-terms list, and cleaned notes, followed by a
Review Questions section with exactly three numbered questions.
