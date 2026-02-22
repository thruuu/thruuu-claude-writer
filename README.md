# thruuu Claude Writer

Turn your thruuu content briefs into article drafts using Claude Code.

thruuu generates data-driven content briefs from real SERP analysis. This repo gives you a Claude Code setup that reads those briefs, fetches external sources, applies your brand guidelines, and writes a full draft — section by section — ready for human review.

---

## How It Works

1. You generate a content brief in [thruuu](https://thruuu.com) and download it
2. You drop the file into the `briefs/` folder
3. You run Claude Code in this folder
4. Claude reads your brief, fetches the referenced URLs, follows your outline, and writes the draft
5. The finished draft lands in `drafts/` with a final review checklist

The quality of the output depends on two things: the brief and your `GUIDELINE.md`. The better both are, the better the draft.

---

## What's in This Repo

| File | Purpose |
|---|---|
| `CLAUDE.md` | The agent brain. Claude reads this automatically on startup. Defines the full writing workflow. |
| `GUIDELINE_MAKER.md` | An interview Claude runs with you to build your personal `GUIDELINE.md`. Run once per brand. |
| `GUIDELINE_EXAMPLE.md` | A reference example of a well-built guideline. Use it as inspiration when reviewing yours. |
| `briefs/` | Drop your downloaded thruuu briefs here. |
| `drafts/` | Claude saves finished drafts here. Created automatically if it doesn't exist. |

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

Start by saying "Hi" and Claude will greet you and walk you through the rest.

---

## First Run

On first run, Claude will check for a `GUIDELINE.md` file. Since you don't have one yet, it will offer to create one by running `GUIDELINE_MAKER.md` — an interview that asks about your brand, audience, writing style, and AI visibility preferences, then analyzes 3 URLs from your blog to capture your actual voice.

This takes about 5 minutes and significantly improves every draft from that point on. Do it before writing your first article.

---

## Writing Your First Article

### Step 1 — Generate your brief in thruuu

Go to your thruuu account, open a content brief, and click **Download**.

Don't have a thruuu account? [Start for free at thruuu.com](https://thruuu.com)

### Step 2 — Drop the file in the briefs folder

```
thruuu-claude-writer/
└── briefs/
    └── your-brief-filename.docx
```

### Step 3 — Tell Claude you're ready

In the Claude Code session, type:

```
start
```

Claude will confirm the brief it found and ask if you're ready to proceed.

### Step 4 — Wait for the draft

Claude will:
- Parse every element of the brief
- Fetch all referenced URLs
- Detect the article language
- Ask clarifying questions only if something is genuinely ambiguous
- Write the draft section by section
- Place all links
- Run a final review checklist
- Save the output to `drafts/[slug].md`

---

## Understanding the Brief Elements

thruuu briefs contain several elements that Claude handles differently. Here's a quick reference:

| Element | What Claude Does With It |
|---|---|
| **Writer Directive** | Highest priority writing instructions. Overrides GUIDELINE.md where they conflict. |
| **Article Summary** | Source of truth for title, slug, meta description, word count, and tone. |
| **Content Outline** | The heading structure Claude follows exactly — no headings are ever changed or reordered. |
| **Food For Thought** | URLs Claude reads (first 800 words each) to build expertise before writing. |
| **Top Topics** | Keywords to weave naturally into the content. |
| **Frequent Questions** | People Also Ask data. Claude answers these within the content, not as separate headings. |
| **Links** | Internal and external links Claude places in the draft at natural anchor points. |

---

## The GUIDELINE.md

Your `GUIDELINE.md` is the writing bible Claude applies to every draft. It defines:

- Brand voice and tone
- Intro style preferences
- AI visibility settings
- Formatting rules
- Taboos and non-negotiables
- Feature pages to link when mentioning your product

It's generated once via `GUIDELINE_MAKER.md` and stored locally. You can edit it manually at any time — it's just a markdown file. See `GUIDELINE_EXAMPLE.md` for a reference of what a complete guideline looks like.

---

## Keeping Up to Date

Pull the latest version of `CLAUDE.md` and `GUIDELINE_MAKER.md` when updates are released:

```bash
git pull origin main
```

Your `GUIDELINE.md` and anything in `briefs/` and `drafts/` are gitignored — updates will never overwrite your personal files.

---

## Resources

- [thruuu.com](https://thruuu.com) — generate your content briefs
- [How to create a content brief with thruuu](https://thruuu.com/content-brief-generator) — learn what goes into a great brief
- [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/getting-started) — install and configure Claude Code
- Video walkthrough — coming soon

---

## License

MIT — use freely, adapt as needed, attribution appreciated.
