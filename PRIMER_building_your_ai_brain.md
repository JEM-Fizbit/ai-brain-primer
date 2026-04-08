# Building Your AI Brain: A Practitioner's Guide

**A framework for creating a personal AI context system using plain Markdown files.**

*Created: March 2026. Based on primary research, practitioner accounts, and direct implementation experience.*

---

## What Is an AI Brain?

An AI Brain is a structured collection of Markdown files that give AI assistants persistent, reusable context about you — your identity, expertise, working style, projects, and goals. Instead of re-explaining yourself every session, you load the relevant files and the AI picks up where a well-briefed colleague would.

This is not a theoretical exercise. A well-built AI Brain measurably changes the quality of every interaction: writing is in your voice, analysis reflects your mental models, and recommendations account for your actual situation rather than generic advice.

## Why Markdown?

The industry spent millions on vector databases, RAG pipelines, and proprietary memory systems. Meanwhile, the most effective implementations — including the Manus AI agent and numerous Claude Code power users — converged on plain Markdown files. The reasons are practical:

- **Transparent.** You can read exactly what your AI "knows" about you. No black box.
- **Editable.** Fix an error in 10 seconds with any text editor. No API calls, no rebuilds.
- **Portable.** Works with Claude, ChatGPT, Codex, Cursor, Copilot, or any future tool. Zero lock-in.
- **Versionable.** Put it in Git. Track changes over time. Roll back mistakes.
- **Free.** No infrastructure, no subscriptions, no maintenance burden.

The constraint is context window size, which is why structure and discipline matter. You cannot dump everything into one file and hope for the best.

---

## Architecture: The Four-Layer Model

The most effective AI Brains organise context into four layers, each serving a different purpose and changing at a different cadence.

### Layer 1: Identity & Biography (What You've Done)
**Cadence:** Updates quarterly or when career changes occur.

This is the factual foundation: career history, education, credentials, publications, awards, board roles, public profiles. Think of it as a canonical CV that the AI can draw from for bios, introductions, applications, or background context.

**Key principle:** Source from primary documents (your actual CV, LinkedIn, award citations), not memory. Memory drifts; documents don't.

**Common files:**
- `01_identity.md` — Career arc, credentials, approved bios, public links.

### Layer 2: Skills & Domain Knowledge (What You Know)
**Cadence:** Updates quarterly.

A rated map of your expertise across domains. The ratings matter — they tell the AI when to explain something vs. when to assume competence, and they signal where you're an authority vs. where you're still learning.

**Recommended rating scale:**
- **Deep** — Can lead and teach. The AI should defer to your expertise and not over-explain.
- **Strong** — Working fluency. The AI can engage at an intermediate level.
- **Building** — Actively learning. The AI should explain more and flag when it's uncertain.

**Common files:**
- `02_expertise.md` — Domain knowledge map with depth ratings.

### Layer 3: Operating System (How You Work, Decide, and Think)
**Cadence:** Updates semi-annually. This is the most stable layer.

This is the layer most people skip and the one that creates the most value. It covers cognitive style, communication preferences, decision-making patterns, pet peeves, energy management, and explicit instructions for how the AI should behave.

Without this layer, the AI defaults to generic "helpful assistant" mode. With it, the AI adapts to your actual working style — leading with recommendations if that's what you prefer, pushing back when you want intellectual honesty, matching your register across contexts.

**What to capture:**
- Cognitive style (systems thinker? first-principles? intuitive? analytical?)
- Communication preferences (concise vs. detailed? structured vs. conversational?)
- Decision-making approach (bias toward action? consensus-builder? data-dependent?)
- Pet peeves and friction points (what wastes your time? what annoys you?)
- Strengths and genuine blindspots (honest self-assessment, not a job interview)
- Feedback preferences (how do you want to receive pushback or bad news?)
- Energy patterns (when are you sharpest? what drains you?)
- Learning style (how do you acquire new knowledge most effectively?)

**Common files:**
- `03_work_style.md` — Thinking, communication, decision-making preferences.
- `06_writing_voice.md` — Style guide for ghostwriting (tone, language rules, what to avoid).

### Layer 4: Aspirations & Mental Models (Where You're Going and What You Believe)
**Cadence:** Updates annually or after major life transitions.

This is what makes the Brain generalise across use cases. It captures your worldview, strategic goals, recurring intellectual themes, and the mental models you reach for when reasoning about novel problems.

An AI that knows your mental models can reason *like you* in new situations, not just recall facts about you.

**What to capture:**
- Strategic goals (1-year, 3-year, 10-year horizons)
- Core beliefs about your field, industry, or the world
- Recurring themes in your thinking and writing
- Intellectual influences (books, thinkers, frameworks)
- What you want to be known for (which may differ from your CV)
- Decision frameworks and mental models you actually use

**Common files:**
- `10_mental_models.md` — Decision frameworks, worldview, recurring themes.

---

## Supporting Files: The Operational Layer

Beyond the four core layers, several supporting files round out a production-quality Brain.

### NOW.md — The Current State File
**Cadence:** Weekly or more.

This is the single highest-ROI addition to any AI Brain. A short, high-density snapshot of what you're focused on right now: this week's priorities, active decisions, open loops, blockers. Unlike the other files (which are stable reference), this one gets overwritten frequently.

The research is emphatic on this point: after a context window reset, `NOW.md` is the first thing the AI should read. It's the "life raft" that re-orients the AI to your current state.

### Loader / Index File
**Cadence:** Updates whenever the file structure changes.

An entry point that tells the AI what files exist, what's in each one, and which files to load for different task types. This enables progressive disclosure — the AI loads only what's relevant rather than consuming your entire Brain every session.

A good loader includes:
- A one-paragraph summary of who you are.
- Core working principles (3-5 rules that apply to every interaction).
- A task-to-file navigation table.
- A complete file listing.
- Maintenance metadata (created date, last reviewed, review cadence).

### Journal — The Daily Capture File
**Cadence:** Daily entries, pruned weekly.

A flat file (`JOURNAL.md`) for capturing decisions, actions, and reflections as they happen. Think of it as a staging area — entries live here temporarily until they're either ingested into the relevant Brain file during a weekly review, or pruned as ephemeral. Not an archive; not a diary. If the file exceeds 200 lines, that's a signal you're not pruning aggressively enough (or it's time to switch to weekly files in a `journal/` folder).

### Task Queue — Operational To-Dos
**Cadence:** Updated as tasks arise; reviewed weekly alongside NOW.md.

`TASKS.md` tracks specific, actionable to-dos — distinct from the strategic priorities in `NOW.md`. NOW.md answers "what am I focused on?"; TASKS.md answers "what specifically needs doing?". Simple checkbox format. Future integration point for external task systems (Asana, Linear, etc.) via MCP or other automation.

### Context-Specific Packs
For domains that need deep, specialised context (e.g., a specific company you work for, a complex project, a brand voice), maintain separate sub-directories. These get loaded only when relevant and prevent the core Brain from bloating.

---

## The Interview Process: How to Capture Context

### Why Interview Yourself?
Most people, when asked to describe their working style or expertise, produce generic statements like "I'm detail-oriented" or "I value collaboration." These are useless to an AI. The interview process forces specificity.

### The Interview Framework

**Round 1: Facts & Foundation**
Start with primary documents — CV, LinkedIn, published bios, award citations. Extract and verify every factual claim. This is not a memory exercise; it's an archival one.

Key questions:
- What is the precise chronological order of your career? (Dates, titles, companies.)
- What have you built, raised, launched, or delivered? (Specific numbers.)
- What credentials, publications, patents, or awards do you hold?
- What are your approved public profiles and contact information?

**Round 2: Knowledge & Expertise**
Map your domains and rate them honestly.

Key questions:
- What could you teach a masterclass on tomorrow with no preparation?
- Where do you have working fluency but would defer to a specialist?
- What are you actively learning? Where are you a beginner?
- What cross-cutting skills or patterns connect your domains?

**Round 3: Operating System**
This is where the value compounds. Push past generic answers.

Key questions:
- When you face a hard decision with incomplete information, what's your actual process? Walk through a recent example.
- What specifically wastes your time or frustrates you in professional contexts?
- What are your genuine blindspots? Where do you over-rotate?
- How do you prefer to receive bad news or pushback?
- How do you learn new things most effectively? What sources do you trust?
- When are you at your sharpest? What drains your energy?

**Round 4: Aspirations & Mental Models**
This interview round surfaces the deeper layer.

Key questions:
- If the next 3 years go really well, what does your professional life look like?
- What do you believe that most people in your field get wrong?
- What books, thinkers, or frameworks have most shaped your thinking?
- What do you want to be known for — and is that different from how people know you now?
- What mental models or decision frameworks do you reach for repeatedly?
- What recurring themes show up in your writing, conversations, and thinking?

### Interview Tips

- **Use primary documents, not memory.** Your CV is more accurate than your recollection of dates and titles.
- **Push for specifics.** "I'm a systems thinker" becomes useful only when accompanied by an example of how that manifests in practice.
- **Iterate.** The first pass will miss things. Live with the Brain for a week, notice gaps, then run a focused follow-up.
- **Let the AI interview you.** AI assistants are surprisingly good interviewers when given a clear framework. They ask follow-ups that a self-assessment would miss.

---

## Design Principles

These principles emerged from both the research and direct implementation experience.

### 1. One Topic Per File
Each file should cover a single, coherent domain. If you find yourself scrolling past sections to find what you need, the file is too broad. Split it.

### 2. Under 200 Lines Per File
A hard limit that forces discipline. Context windows are finite and expensive. Every line should earn its place. If a file exceeds 200 lines, it either needs pruning or splitting.

### 3. Actionable Over Descriptive
"I'm detail-oriented" is descriptive and useless. "Double-check all numbers and calculations before presenting them" is actionable. Every instruction should change the AI's behaviour. Test each line: *Would removing this change how the AI responds?* If not, cut it.

### 4. Progressive Disclosure
Not every task needs every file. Use a loader/index file with a task-to-file navigation table. The AI loads the loader first, determines which files are relevant, and loads only those.

### 5. Source from Documents, Not Memory
Career dates, financial figures, award names, publication titles — all of these should come from primary documents (CV, LinkedIn, company records), not from memory. Memory drifts, especially on dates and numbers.

### 6. Prune Aggressively
Outdated context is worse than no context. Set a review cadence (monthly for dynamic files, quarterly for stable ones) and enforce it. Delete anything that's no longer true, relevant, or useful.

### 7. Separate Stable from Dynamic
Your career history changes rarely. Your current priorities change weekly. Don't put them in the same file. Stable reference files (identity, expertise, voice) should have long review cycles. Dynamic files (NOW.md, active projects) should update frequently.

### 8. Make It Portable
Write for any AI tool, not just your current one. Avoid tool-specific syntax or instructions. Plain Markdown with clear headers and consistent formatting works everywhere.

### 9. Use Backlinks for Navigation
Cross-reference files using `[[wikilinks]]` (Obsidian-compatible). Link on first significant mention per section. This creates a navigable knowledge graph that works in Obsidian (graph view, backlinks panel) and helps LLMs follow connections between files. During ingest, add backlinks between all affected files. During lint, flag content files with zero inbound links as orphans.

---

## Recommended File Structure

```
AI Brain/
├── 00_loader.md              # Entry point, navigation, core principles
├── 01_identity.md            # Career arc, credentials, approved bios
├── 02_expertise.md           # Domain knowledge map with depth ratings
├── 03_work_style.md          # Cognitive style, communication, decision-making
├── 04_active_roles.md        # Current professional positions
├── 05_projects.md            # Active projects (personal, side, open-source)
├── 06_writing_voice.md       # Style guide for ghostwriting
├── 07_interests_learning.md  # Active learning areas, intellectual interests
├── 08_personal.md            # Family, location, personal context
├── 09_tools_stack.md         # Tech stack, tools, workflows
├── 10_mental_models.md       # Decision frameworks, worldview, beliefs
├── NOW.md                    # Current focus, priorities, open decisions
├── JOURNAL.md                # Daily capture — decisions, actions, reflections
├── TASKS.md                  # Live task queue — operational to-dos
├── LOG.md                    # Append-only change log (ingests, updates, lints)
├── quanta.md                 # Entity hub — consolidates cross-cutting context
├── ref_career_chronology.md  # Split reference: career timeline, dates
├── ref_publications_media.md # Split reference: awards, publications, patents
├── ref_capital_deals.md      # Split reference: board roles, capital raised
└── [domain_context]/         # Separate packs for specific domains
    ├── company_brain/
    └── project_brain/
```

This structure is not prescriptive — adapt it to your situation. The important thing is that every file has a clear, single purpose and the loader provides navigation.

---

## Maintenance and Evolution

### Review Cadence

| File Type | Review Cadence | Trigger |
|-----------|---------------|---------|
| NOW.md | Weekly | Every Monday or start of sprint |
| Active roles / projects | Monthly | Role changes, project launches/completions |
| Identity / credentials | Quarterly | New publications, awards, career moves |
| Expertise map | Quarterly | New skills, reclassification of depth |
| Work style / voice | Semi-annually | Rarely changes; review for accuracy |
| Mental models | Annually | Major life transitions, new frameworks adopted |
| Loader | As needed | When file structure changes |

### Consolidation Process

Over time, your Brain will accumulate insights from conversations, projects, and decisions. Periodically (monthly is a good cadence), review recent work and ask:

- Did any conversation reveal something about my preferences or style that isn't captured?
- Did I make a decision that reflects a mental model worth documenting?
- Is any information in the Brain now stale or contradicted by recent events?
- Has a "Building" skill moved to "Strong"? Has a role ended?

Update the relevant files and prune what's no longer true.

### Version Control

If you use Git (recommended), commit changes with descriptive messages. This gives you a changelog of how your Brain — and by extension, your professional identity and thinking — evolves over time. It also provides a safety net: if you prune too aggressively, you can recover.

---

## Operational Patterns

As a Brain grows — from a personal system with 15 files to an enterprise knowledge base with hundreds — it needs formal processes for how information enters, how changes are tracked, and how consistency is maintained. These four patterns address that. They work at any scale but become essential as the Brain expands.

### Ingest: How New Information Enters

Without a formal ingest process, new information enters the Brain ad-hoc — someone edits a file, adds a paragraph, and moves on. This works at small scale but breaks down quickly: updates are inconsistent, related files get missed, and there's no record of what changed or why.

A formal ingest workflow:

1. **Analyse** — Read the source material and identify which Brain files it touches.
2. **Plan** — List the specific changes: which files to update, what to add or revise, whether any new files are needed.
3. **Review** — Present the plan to the human owner before making changes. The Brain is human-owned; the AI proposes, the human approves.
4. **Execute** — Make the changes across all affected files.
5. **Log** — Record the ingest (see below).

Sources can be anything: articles, meeting notes, CV updates, role changes, project milestones, customer feedback. At enterprise scale, sources might include Slack threads, meeting transcripts, or customer call summaries — the workflow stays the same.

**Source persistence:** Always save the original source to a `sources/` directory, organised by category (bios, cv, articles, meeting_notes, correspondence, etc.). Maintain a `SOURCES.md` index linking each source file to the Brain files it informed. This provides provenance — if a Brain fact is questioned, you can trace it back to the source document that produced it.

**Key principle: one source can touch many files.** A role change might update identity, active roles, projects, NOW.md, and the loader. The ingest process should surface all touchpoints, not just the obvious one.

**Cross-referencing:** When an ingest touches multiple files, add `[[backlinks]]` (Obsidian-style wikilinks) between them. Link format: `[[filename_without_extension]]`. This maintains a navigable knowledge graph. Over time, the link structure becomes as valuable as the content itself — it enables graph-based navigation in tools like Obsidian and helps LLMs discover related context by following links.

### Log: Tracking What Changed and When

Git provides version history, but it's not LLM-friendly — commit messages are terse, diffs are structural, and the timeline is hard to query conversationally. A Brain change log fills this gap.

`LOG.md` is an append-only file recording ingests, updates, lint passes, and structural changes:

```markdown
## [2026-04-04] INGEST | Updated active roles from board meeting notes
Files: 04_active_roles.md, NOW.md, 11_next_chapter_framework.md

## [2026-04-01] LINT | Quarterly health check
Files: (all files scanned)
```

The format is parseable (`grep "^## \[" LOG.md | tail -5` gives recent entries), human-readable, and gives the LLM timeline context for what changed and when. Operation types: INGEST, UPDATE, LINT, CREATE, SPLIT, PRUNE.

### Lint: Periodic Health Checks

Brains decay. Facts go stale, files bloat past limits, new content contradicts old claims, and files drift out of sync. A periodic lint check catches these problems before they mislead the AI.

**Structural checks** (automated):
- **Bloat** — Files exceeding the 200-line limit.
- **Staleness** — Files past their review cadence (e.g., NOW.md untouched for >7 days).
- **Orphans** — Content files with zero inbound `[[backlinks]]` from other files. Operational files (NOW, LOG, JOURNAL, TASKS, SOURCES) and the loader are exempt.
- **Drift** — Priorities in NOW.md that don't map to any active project or role.
- **Large domain packs** — Subdirectories growing unwieldy (>15 files).

**Semantic checks** (LLM-assisted):
- Contradictions between files (e.g., a role listed as active in one file but absent from another).
- Claims superseded by newer information.
- Important concepts mentioned but never elaborated.
- Missing cross-references between related files.

**Cadence:** Monthly at minimum. Also run after any ingest operation and before accuracy-sensitive work (writing, applications, fact-dependent tasks). Integrate lint triggers into your loader's instructions so the LLM runs it proactively.

### Entity Pages: Navigational Hubs

As a Brain grows, key entities (companies, organisations, major projects) get mentioned across many files. When an entity appears in 3+ files with scattered context, create a dedicated entity page — a lightweight summary (~30-40 lines) that consolidates key facts and links out to the detailed category files. Entity pages are hubs, not duplicates: they state facts and link to where the full story lives. Example: `quanta.md` linking to identity (career arc), expertise (domain depth), and reference files (investment details).

### Splitting Large Reference Files

When a reference file exceeds the 200-line limit, split it by natural category boundaries. Each split file gets the original provenance header, links to sibling splits via backlinks, and a note documenting the split. Example: a 237-line extracted facts file splitting into career chronology, publications/media, and capital/deals — each under 90 lines.

### Index: Navigating at Scale

At 15 files, a simple task-to-file navigation table suffices. At 100+ files across multiple domain packs, the LLM needs richer metadata to make smart loading decisions without reading everything.

An effective index includes:
- **Task routing** — Which files to load for which task types (the navigation table).
- **Content summaries** — One-line descriptions of what each file contains.
- **Operational files** — References to LOG.md and any other infrastructure files.

The index lives in the loader file (not a separate file) and should be updated whenever files are added, removed, or significantly restructured. The LLM reads the index on every session start and uses it to determine what to load.

---

## Common Mistakes

**1. Writing for humans, not AI.** Your Brain is read by machines. Be explicit and literal. "Authoritative but accessible" tells a human something; "Lead with the conclusion. Use specific numbers. Avoid jargon unless the audience is technical" tells an AI what to do.

**2. Including everything.** More context is not better context. Every irrelevant line dilutes the signal. If a fact doesn't change how the AI behaves or what it produces, it doesn't belong.

**3. Skipping the operating system layer.** Facts and skills are necessary but insufficient. The operating system (Layer 3) is what transforms generic AI assistance into personalised collaboration.

**4. Never updating.** A Brain that reflects who you were 6 months ago actively misleads the AI. Set calendar reminders for reviews.

**5. Making it tool-specific.** Writing instructions like "When using Claude Projects..." makes the Brain non-portable. Write for any AI tool.

**6. Trusting memory over documents.** Career dates, financial figures, award names — verify everything against primary sources. Your memory of when you started a role is probably wrong by a year.

---

## Getting Started

The fastest way to build your AI Brain is to have an AI do it with you. The process takes roughly 90 minutes for a functional first draft, then improves through iteration.

### Step 1: Gather Your Materials (~30 min)

Before starting a session, collect these into a single folder:

- Your CV / resume (PDF or Word)
- Your LinkedIn "About" section (copy-paste into a .txt file, or just have the URL ready)
- Any published bios (conference programmes, company website, speaker packs)
- Award citations or press coverage (if relevant)
- Writing samples that represent your voice (blog posts, articles, newsletters)

The more primary documents you provide, the more accurate the Brain will be. Memory is unreliable for dates, titles, and numbers — documents aren't.

### Step 2: Start a Session and Use This Prompt (~50 min)

Open a new Claude session (Cowork, Claude Code, or Projects). Attach this primer document and your gathered materials. Then paste the following prompt:

```
I want to build a personal "AI Brain" — a structured set of Markdown files that give
you persistent, reusable context about me across sessions and use cases.

I've attached a primer document (PRIMER_building_your_ai_brain.md) that describes the
framework, file structure, and methodology. Please read it carefully before proceeding.

I've also attached my primary documents [CV, bio, writing samples, etc.]. Use these as
the factual foundation — do not rely on my memory for dates, titles, or numbers.

Here's how I'd like to proceed:

1. **Extract facts from my documents first.** Read my CV and bio materials and produce
   a structured factual extract (career chronology with dates, education, credentials,
   awards, publications, capital raised, board roles). Show me the extract for
   verification before creating any files.

2. **Create the file structure.** Following the primer's recommended architecture,
   create the initial set of .md files: loader, identity, expertise map, work style,
   active roles, projects, writing voice, interests, personal context, tools/stack,
   mental models, and NOW.md.

3. **Interview me to fill gaps.** Use the four-round interview framework from the
   primer to capture what the documents can't tell you — my thinking style, decision
   frameworks, communication preferences, values, goals, and mental models. Interview
   me iteratively; don't try to capture everything in one pass.

4. **Review and refine.** After the first draft, walk me through each file so I can
   correct errors, add nuance, and flag anything that's wrong or missing.

Important principles for this session:
- Source facts from my documents, not from my memory or your training data.
- Be specific and actionable, not generic. "I'm detail-oriented" is useless;
  "Double-check all numbers before presenting them" is useful.
- Keep each file under 200 lines.
- Flag anything you're uncertain about rather than guessing.

Let's start with Step 1: read my documents and produce the factual extract.
```

This session will produce a functional Brain: loader, identity file, work style, and NOW.md at minimum. Everything else — expertise maps, writing voice guides, mental models, domain-specific packs — gets added iteratively as you use it and notice gaps.

### Step 3: Iterate (~10 min setup, then ongoing)

The first pass will be 70-80% right. That's fine. The value comes from iteration:

- **Correct factual errors immediately.** Wrong dates, missing roles, inaccurate numbers — fix these in the first session.
- **Live with the Brain for a week.** Use it in real work sessions. Notice where Claude still misunderstands you or lacks context.
- **Run follow-up interviews.** The Layer 3 (operating system) and Layer 4 (mental models) content often takes 2-3 sessions to get right, because self-knowledge is hard to articulate on the first attempt.
- **Update NOW.md weekly.** This is the only file that should change frequently. Everything else updates on a monthly or quarterly cadence.

### Step 4: Deploy Across Tools

Once your Brain is built, you can use it anywhere:

- **Claude Projects** — Add the relevant .md files as project knowledge.
- **Claude Cowork** — Keep the Brain in your mounted workspace folder. Claude reads it automatically.
- **Claude Code** — Place the loader as `CLAUDE.md` in your project root, or reference Brain files from your home directory.
- **ChatGPT / Custom GPTs** — Paste the loader and relevant files into custom instructions or knowledge.
- **Cursor / Copilot** — Add as context files or rules in your workspace.
- **Any other AI tool** — The files are plain Markdown. Copy-paste or attach as needed.

### Adaptation Prompt (For Existing Brains)

If you already have a personal context system and want to restructure it using this framework, use this prompt instead:

```
I have an existing personal context system that I'd like to restructure using a
proven AI Brain framework. I've attached my current files and a primer document
that describes the target architecture.

Please:
1. Read the primer to understand the target framework.
2. Read my existing context files.
3. Propose a migration plan: what content maps to which new file, what's missing,
   and what should be pruned.
4. Execute the migration, creating the new file structure.
5. Interview me to fill any gaps the migration reveals.
```

---

## Sources & Further Reading

- [AI Agent Memory Management: When Markdown Files Are All You Need](https://dev.to/imaginex/ai-agent-memory-management-when-markdown-files-are-all-you-need-5ekk)
- [Claude Code for Everything: The Best Personal Assistant Remembers Things About You](https://hannahstulberg.substack.com/p/claude-code-for-everything-the-best-personal-assistant-remembers-everything-about-you)
- [CLAUDE.md Best Practices: 10 Sections to Include](https://uxplanet.org/claude-md-best-practices-1ef4f861ce7c)
- [Why Your AI Agent Keeps Forgetting: A Practical Memory Architecture](https://huizhou92.com/p/why-your-ai-agent-keeps-forgetting-a-practical-memory-architecture-for-individual-users/)
- [Context Engineering for Personalization (OpenAI Agents SDK Cookbook)](https://cookbook.openai.com/examples/agents_sdk/context_personalization)
- [The Best Personal User Manual for Work (FlexOS)](https://www.flexos.work/learn/the-best-personal-user-manual-for-work-guide-template)
- [How to Create a Personal User Manual (Atlassian)](https://www.atlassian.com/team-playbook/plays/my-user-manual)
- [Claude AI Custom Instructions: Examples & Best Practices](https://www.jdhodges.com/blog/claude-ai-custom-instructions-a-real-example-that-actually-works/)
- [The LLM Context Problem in 2026 (LogRocket)](https://blog.logrocket.com/llm-context-problem/)
