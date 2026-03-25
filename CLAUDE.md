# Claude Instructions for This Obsidian Vault

## About the Owner
- **Name:** Somya Chaniyara
- **Grade:** 12th grade, honor roll (As and Bs)
- **Athletics:** Varsity football + wrestling
- **School classes:** English 4, Film and Literature
- **Fiverr service:** SEO blog posts & email sequences
- **Fiverr goal:** $1,000 in the first month
- **Full profile:** [[Profile]]

## Writing Style (for all school work)
- Sound natural and student-like — never AI-stiff or overly formal
- Concise and direct — no unnecessary padding
- Once direction is given, handle full execution
- Always include cited quotes when required

This is an Obsidian vault used for two main purposes:
1. **School** — tracking assignments, notes, research, and deadlines
2. **Fiverr Business** — building and running a freelance business on Fiverr

## Vault Structure

```
/
├── School/
│   ├── Assignments/       ← one note per assignment
│   ├── Subjects/          ← notes and resources per subject/class
│   ├── Research/          ← research notes and sources
│   └── Daily/             ← daily study logs (YYYY-MM-DD.md)
│
├── Fiverr/
│   ├── Gigs/              ← one note per Fiverr gig/service
│   ├── Clients/           ← one note per client
│   ├── Projects/          ← active project notes
│   ├── Templates/         ← reusable templates (proposals, messages, briefs)
│   └── Business/          ← strategy, pricing, goals, income tracking
│
├── Templates/             ← Obsidian note templates
└── Attachments/           ← images, PDFs, files
```

## Note Format

### Frontmatter (Properties)
Always add YAML frontmatter to new notes. Use the relevant template below:

**School assignment:**
```yaml
---
title: Assignment Title
subject: Subject Name
due: YYYY-MM-DD
status: not started | in progress | done
tags: [school, subject-name]
---
```

**Fiverr gig:**
```yaml
---
title: Gig Name
category: (e.g. writing, design, video)
price: $X
status: active | draft | paused
tags: [fiverr, gig]
---
```

**Fiverr client:**
```yaml
---
title: Client Name/Username
platform: fiverr
status: lead | active | completed | repeat
tags: [fiverr, client]
---
```

### Markdown Conventions
- Use `[[wikilinks]]` for internal links — never convert to markdown links
- Use `#tags` inline or in frontmatter
- Use `## ` headings (H2 and below) inside notes
- Obsidian callouts: `> [!note]`, `> [!tip]`, `> [!warning]`, `> [!important]`

## Working with Notes

### When creating notes
- Place in the correct subfolder based on context (School vs Fiverr)
- Always add relevant frontmatter using the templates above
- Link related notes with `[[wikilinks]]` (e.g. link an assignment to its subject)

### When editing notes
- Preserve existing frontmatter — only update fields if asked
- Preserve all `[[wikilinks]]`
- Do not reformat entire notes unless explicitly asked

### When searching
- Use Grep to search note contents
- Use Glob `**/*.md` to find notes by name pattern
- Filter by folder (e.g. `School/**/*.md` or `Fiverr/**/*.md`)

## Priorities
- School deadlines come first — always flag overdue or upcoming due dates
- For Fiverr, focus on helping build systems (templates, client workflows, gig copy) that scale

## Obsidian Settings
- **Sync** is enabled — do not bulk-rename or delete files without confirming
- **Enabled:** Daily Notes, Templates, Canvas, Backlinks, Tags, Properties, Bases
- Do not touch `.obsidian/` config files
- Do not add HTML — keep everything in clean Markdown
