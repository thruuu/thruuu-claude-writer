# thruuu Claude Writer

Turn your thruuu content briefs into article drafts using Claude Code.

thruuu generates data-driven content briefs from real SERP analysis. This repo gives you a Claude Code multi-agent setup that researches your topic, writes a full draft, humanizes it, places all links, and runs a final editorial review — ready for human review.

---

## How It Works

1. You generate a content brief in [thruuu](https://thruuu.com) and download it
2. You drop the file into the `briefs/` folder
3. You run Claude Code in this folder
4. A team of specialized agents runs in sequence — researching, writing, humanizing, linking, and reviewing
5. The finished draft lands in `drafts/` with a final review checklist

The quality of the output depends on two things: the brief and your `GUIDELINE.md`. The better both are, the better the draft.

---

## The Agent Team

Each article runs through a pipeline of six specialized agents:

| Agent | Role |
|---|---|
| **researcher** | Spawned in parallel for each research scope. Fetches URLs, extracts insights, quotes from real people, and stats. |
| **head-of-research** | Compiles all researcher outputs, scans the `knowledge/` folder, analyzes search intent, and produces a strategic research brief for the writer. |
| **writer** | Reads the full brief and research brief. Follows the Content Outline exactly. Writes the first draft. |
| **humanizer** | Removes AI writing patterns, adds voice and personality, improves flow between sections. |
| **linker** | Places all links from the brief and research naturally in the draft with minimal text adaptation. |
| **editor-in-chief** | Runs the final review checklist, fixes what it can, presents the draft and checklist to you. |

---

## What's in This Repo

| File / Folder | Purpose |
|---|---|
| `CLAUDE.md` | The orchestrator brain. Claude reads this automatically on startup. Coordinates all agents. |
| `.claude/agents/` | The six specialized agents. |
| `GUIDELINE_MAKER.md` | An interview Claude runs with you to build your personal `GUIDELINE.md`. Run once per brand. |
| `GUIDELINE_EXAMPLE.md` | A reference example of a well-built guideline. |
| `briefs/` | Drop your downloaded thruuu briefs here. |
| `drafts/` | Finished drafts saved here. Created automatically. |
| `knowledge/` | Drop any extra context here — notes, reports, founder quotes, proprietary data. Agents read this automatically. |

Your `GUIDELINE.md` is not included — it's personal to your brand and created locally when you run the setup.

---

## Setup

### 1. Install Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

You need Node.js 18+ and an Anthropic API key. Full installation guide: [docs.anthropic.com/claude-code](https://docs.anthropic.com/en/docs/claude-code/getting-started)

### 2. Clone this repo

```bash
git clone https://github.com/thruuu/thruuu-claude-writer.git
cd thruuu-claude-writer
```

### 3. Run Claude Code

```bash
claude
```

Type **create article** to begin or **create guideline** to set up your brand voice first.

---

## First Run

On first run, Claude will check for a `GUIDELINE.md` file. Since you don't have one yet, it will offer to create one — an interview that asks about your brand, audience, writing style, and AI visibility preferences, then analyzes 3 URLs from your blog to capture your actual voice.

This takes about 5 minutes and significantly improves every draft from that point on. Do it before writing your first article.

---

## The knowledge/ Folder

Drop any extra context into the `knowledge/` folder before running. The head-of-research agent reads everything in it automatically. Good candidates:

- Founder quotes or positioning statements
- Proprietary research or data
- Internal notes on the topic
- Brand differentiators you want included

Anything in `knowledge/` is treated as high-priority context — proprietary data and quotes from founders are flagged to the writer explicitly.

---

## Writing Your First Article

### Step 1 — Generate your brief in thruuu

Go to your thruuu account, open a content brief, and click **Download**.

Don't have a thruuu account? [Start for free at thruuu.com](https://thruuu.com)

### Step 2 — Drop the brief in the briefs folder

```
thruuu-claude-writer/
└── briefs/
    └── your-brief-filename.docx
```

### Step 3 — Tell Claude you're ready

```
create article
```

Claude confirms the brief it found and asks if you're ready to proceed.

### Step 4 — Wait for the draft

The pipeline runs automatically:
- Researchers fetch all referenced URLs in parallel
- Head of research compiles findings and briefs the writer
- Writer produces a first draft
- Humanizer removes AI patterns and improves flow
- Linker places all links naturally
- Editor-in-chief runs the final review and presents the checklist

The finished draft is saved to `drafts/[slug].md`.

---

## Understanding the Brief Elements

thruuu briefs contain several elements that each agent handles differently:

| Element | What the agents do with it |
|---|---|
| **Writer Directive** | Highest priority writing instructions. Overrides GUIDELINE.md where they conflict. |
| **Article Summary** | Source of truth for title, slug, meta description, word count, and tone. |
| **Content Outline** | The heading structure — followed exactly by all agents. No heading is ever changed. |
| **Food For Thought** | URLs the researcher reads (first 800 words each) to build expertise. |
| **Top Topics** | Keywords woven naturally into the content. |
| **Frequent Questions** | PAA data. Answered within body copy, never as headings. |
| **Links** | Internal and external links placed naturally by the linker agent. |

---

## The GUIDELINE.md

Your `GUIDELINE.md` is the writing bible all writing agents apply to every draft. It defines:

- Brand voice and tone
- Intro style preferences
- AI visibility settings (Ski Ramp, entity density, sentiment target, etc.)
- Formatting rules
- Taboos and non-negotiables

Generated once via the built-in interview and stored locally. Edit it manually at any time — it's just a markdown file. See `GUIDELINE_EXAMPLE.md` for a complete reference.

---

## Keeping Up to Date

```bash
git pull origin main
```

Your `GUIDELINE.md` and anything in `briefs/`, `drafts/`, and `knowledge/` are gitignored — updates will never overwrite your personal files.

---

## Resources

- [thruuu.com](https://thruuu.com) — generate your content briefs
- [How to create a content brief with thruuu](https://thruuu.com/content-brief-generator) — learn what goes into a great brief
- [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/getting-started) — install and configure Claude Code
- Video walkthrough — coming soon

---

## License

MIT — use freely, adapt as needed, attribution appreciated.
