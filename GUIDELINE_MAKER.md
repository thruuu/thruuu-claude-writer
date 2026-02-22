# GUIDELINE_MAKER.md — thruuu Writing Style Interview

Your job is to interview the user and build a personalized GUIDELINE.md file that Claude will use as its writing bible for every article draft.

Be conversational. Don't present all questions at once — follow the flow below. Ask one block at a time, wait for the answer, then move to the next.

---

## Opening

Say:

> "Let's build your writing guideline. This will take about 5 minutes and will significantly improve every draft I produce for you.
>
> I'll ask you about your brand, your audience, and your writing style — then analyze some examples from your blog to capture your actual voice. I'll also walk you through a few AI visibility principles so you can decide how you want to apply them.
>
> Ready? Let's start."

---

## Block 1 — The Brand

Ask:

> "First, tell me about your brand. What does your company do, and who do you write for? A sentence or two is fine."

Then ask:

> "How would you describe your brand voice? Pick the ones that feel right — you can choose more than one, or add your own:
>
> - Expert and authoritative
> - Conversational and approachable
> - Playful and witty
> - Direct and no-nonsense
> - Empathetic and supportive
> - Bold and opinionated
> - Neutral and informational
>
> Anything you'd add or remove from that list?"

---

## Block 2 — The Audience

Ask:

> "Who reads your content? Describe your typical reader — their job, their level of expertise, what they're usually trying to solve when they land on your blog."

Then ask:

> "One quick scale question: on a scale from 1 to 5, how technical is your audience?
> 1 = complete beginners, 5 = experts who hate being talked down to."

---

## Block 3 — Writing Preferences

Ask:

> "A few quick style questions — just answer what feels natural:
>
> 1. Long-form deep dives or concise and scannable?
> 2. Do you use first-person ('I've seen this work') or do you prefer to keep it impersonal?
> 3. Do you ever use humor or sarcasm, or do you keep it straight?
> 4. Any words, phrases, or expressions you never want to see in your content?"

---

## Block 4 — AI Visibility Calibration

Say:

> "Now let's talk about how your content should perform in AI search. I'll walk you through five principles and ask how strictly you want to apply each one."

Then present each principle one at a time and ask for their preference:

---

**Principle 1 — The Ski Ramp**

> "The ski ramp rule: put your most important insight in the first 20-30% of the article. AI systems are trained on journalism and academic writing — they expect the conclusion at the top, not the bottom.
>
> - Weak: A long intro that teases the insight across 5 paragraphs before revealing it
> - Strong: 'After analyzing 1.2M ChatGPT citations, I found one pattern so consistent it has a P-Value of 0.0.'
>
> How do you want to apply this?
> A) Always — lead with the insight, no exceptions
> B) Usually — front-load most articles but allow narrative intros for storytelling pieces
> C) Rarely — your brand voice relies on building context before the payoff"

---

**Principle 2 — H2s as User Prompts**

> "Framing H2 headings as literal questions makes them behave like search queries — AI systems treat the heading as the prompt and the first paragraph as the answer.
>
> - Weak: `## The History of SEO` followed by 'It began in the early 90s...'
> - Strong: `## When did SEO start?` followed by 'SEO started in...'
>
> How do you want to apply this?
> A) Always — every H2 should be a question
> B) When it fits naturally — use questions where they make sense, not forced
> C) Never — your brand uses declarative headings, not questions"

---

**Principle 3 — Definitive Language**

> "AI systems prefer 'X is defined as Y' sentence structures over vague openers. The word 'is' acts as a strong bridge that makes content easier to cite.
>
> - Weak: 'In this fast-paced world, automation is becoming key...'
> - Strong: 'Marketing automation is the process of using software to...'
>
> How do you want to apply this?
> A) Always — open every section with a direct declarative statement
> B) Usually — use it for definition-heavy sections, allow more narrative elsewhere
> C) Sometimes — only for technical or educational content"

---

**Principle 4 — Entity Richness**

> "Heavily cited content has around 20% entity density — that means naming brands, tools, people, and platforms specifically rather than speaking in generics.
>
> - Weak: 'There are many good tools for this task.' (0% entity density)
> - Strong: 'Top tools include Salesforce, HubSpot, and Pipedrive.' (30% entity density)
>
> How do you want to apply this?
> A) Aggressive — name everything, including competitors
> B) Moderate — name tools and platforms freely, be selective with competitors
> C) Conservative — focus on owned brand mentions, avoid naming competitors"

---

**Principle 5 — Balanced Sentiment**

> "The most-cited content sits at a sentiment score of around 0.47 — not dry facts, not pure opinion. Think of it as the analyst voice: state the fact, then explain what it means.
>
> - 0.0 (Pure Objectivity — avoid): 'The iPhone 15 was released in September 2023.'
> - 1.0 (Pure Subjectivity — avoid): 'The iPhone 15 is an absolutely stunning masterpiece that I love.'
> - 0.47 (Sweet Spot): 'While the iPhone 15 features a standard A16 chip, its performance in low-light photography makes it a superior choice for content creators.'
>
> Where does your brand naturally sit?
> A) We aim for the analyst voice — fact plus interpretation
> B) We lean more objective — data and facts, minimal editorializing
> C) We lean more opinionated — strong takes are part of our brand"

---

After all five principles, summarize the user's choices:

> "Got it. Here's your AI visibility profile:
>
> - Ski Ramp: [their answer]
> - H2s as prompts: [their answer]
> - Definitive language: [their answer]
> - Entity richness: [their answer]
> - Sentiment target: [their answer]
>
> I'll apply these as defaults across every draft. You can always override them in the Writer Directive of a specific brief."

---

## Block 5 — Competitor Awareness

Ask:

> "Are there any blogs or writers in your space whose style you admire — even competitors? I won't copy them, but knowing what you like helps me understand the benchmark you're aiming for."

---

## Block 6 — URL Analysis

Say:

> "Now the most important part. Share 3 URLs from your own blog — ideally articles you're proud of or that represent the style you want to replicate. I'll read them and extract your actual voice, not just what you described."

Wait for the 3 URLs.

For each URL:
- Fetch the page and read the first 1000 words
- Analyze and note: sentence length, paragraph length, use of first person, tone, use of humor or sarcasm, how technical the language is, how insights are structured, how the intro is written, any recurring phrases or patterns
- Note how closely the content already applies the five AI visibility principles

After reading all three, say:

> "Got it. Here's what I picked up from your content:"

Then summarize in plain language what you observed — 5 to 8 bullet points covering the patterns you found. Be specific. For example:
- "Your intros tend to open with a provocative question rather than a definition"
- "You use 'we' more than 'I' — the voice feels like a team, not a solo expert"
- "Sentences average around 12 words — short and punchy"
- "You name-drop tools and competitors freely, which gives the content high entity density"
- "There's a dry wit running through most pieces — not jokes, but observations with a raised eyebrow"
- "Your content already applies the ski ramp naturally — insights land early"

Then flag any gaps between their stated preferences (Blocks 1-4) and what you actually observed in the URLs. For example:

> "One thing worth flagging: you said you prefer the analyst voice, but the articles I read lean closer to 0.3 on the sentiment scale — quite factual, not much interpretation. I'll aim for 0.47 unless you tell me otherwise."

Then ask:

> "Does this feel accurate? Anything I missed or got wrong?"

Adjust based on their response.

---

## Block 7 — Taboos and Non-Negotiables

Ask:

> "Last thing. Any hard rules?
>
> - Topics or angles you never touch?
> - Competitor names you avoid mentioning?
> - Formatting rules (e.g., always use numbered lists, never use tables)?
> - Anything else that would make you cringe if you saw it in a draft?"

---

## Building the GUIDELINE.md

Once all blocks are complete, say:

> "Perfect. Building your GUIDELINE.md now."

Generate the GUIDELINE.md file with the following structure:

```markdown
# GUIDELINE.md — [Brand Name] Writing Style Guide

## Brand Context
[1-2 sentences describing what the company does and who they write for]

## Target Audience
[Description of the reader, their expertise level, their typical intent]
Expertise level: [1-5 scale answer]

## Brand Voice
[3-5 adjectives or phrases that define the voice, drawn from Block 1 answers and URL analysis]

## Tone
[Describe the tonal register — formal/informal, degree of humor, use of opinion vs. neutrality]

## Writing Style
[Specific patterns extracted from URL analysis + Block 3 answers]
- Sentence and paragraph length
- Use of first person
- How intros are structured
- How insights are delivered
- Any recurring structural patterns

## AI Visibility Settings
- Ski Ramp: [A/B/C + description of what this means in practice for this brand]
- H2s as User Prompts: [A/B/C + description]
- Definitive Language: [A/B/C + description]
- Entity Richness: [A/B/C + description]
- Sentiment Target: [A/B/C + target score + description]

## Entity and Reference Style
[How the brand handles naming tools, brands, competitors — freely or carefully]

## Formatting Rules
[Preferences for lists, headers, tables, bold text, etc.]

## Taboos
[Hard no's — words, phrases, topics, formats to never use]

## Benchmark Blogs
[Any competitor or reference blogs the user mentioned in Block 5]
```

Save the file as `GUIDELINE.md` in the current directory.

Then say:

> "Your GUIDELINE.md is ready. I'll apply it to every draft from now on — including your AI visibility settings. You can edit the file at any time, it's just a markdown file. Want to start on your first brief now?"
