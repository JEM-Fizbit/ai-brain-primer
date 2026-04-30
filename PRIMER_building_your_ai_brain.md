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

### 9. Capture Outputs, Not Just Inputs
Most Brain implementations focus on ingesting *inputs* — CVs, bios, writing samples, documents. This misses half the value. The *outputs* you produce with an AI — decision memos, opportunity evaluations, strategy analyses, board prep, draft essays — also represent durable reasoning that should compound across sessions.

Without an output-capture habit, a 1,200-word analysis of "Should I accept this board seat?" lives only in a session transcript. Three months later, when the same decision framework would be useful for a different opportunity, the reasoning is gone.

**The protocol:**
- **Threshold:** Original reasoning of roughly ≥500 words, OR any written artifact the user would plausibly re-read (memos, decision frameworks, drafts). Skip routine answers and information retrieval.
- **Location:** A dedicated `sources/analysis/` directory for non-publication reasoning. Reserve `sources/writing_samples/` for publication-bound work.
- **Format pattern — mirrors input ingestion:** If the deliverable *is* the markdown (analysis, memo, written argument), save markdown-only. If the deliverable is a binary (.pptx, .docx, .pdf, .xlsx), save the binary alongside a markdown companion that captures the argument structure, decisions, and rationale — typically 300–800 words. The companion is a summary of *thinking*, not a mechanical conversion. The binary is provenance; the markdown is what future sessions query.
- **Linking:** Backlink each analysis from the relevant entity or topic file under a "Related Analyses" section.
- **Journal entry:** One-line note in `JOURNAL.md` capturing the analysis and its headline conclusion — searchable, scannable.
- **Prompt shape:** The AI should ask at a natural pause once thinking has stabilised, not mid-draft.

Inspired by Karpathy's observation that his knowledge base compounds when "outputs get filed back into the wiki to enhance it for further queries." The same principle applies to a professional context pack: reasoning produced in one session should be retrievable in the next.

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

## Client Workflow: Which Tool for Which Task

If you serve your Brain via MCP, you can access it from multiple Claude clients — Chat (claude.ai or Claude Desktop), Cowork, and Claude Code. Each client has different strengths, and matching the right client to the right task prevents friction.

### Day-to-day Brain usage → Chat (any client with MCP)

This is the primary interface and the whole point of the MCP architecture. Every read/write Brain tool works over stdio from any connected client. Use Chat for:

- Loading Brain context for conversations (writing, career, strategy, advice)
- Updating dynamic files (NOW.md, TASKS.md, JOURNAL.md)
- Running `brain_search` and `brain_lint`
- Small ingestions (under 500 words, passed directly via `source_content`)
- Committing and pushing changes via `brain_commit`

No manual file uploads, no copy-paste — the MCP server handles everything from within the conversation.

### Heavy document ingestion → Cowork or Claude Code

Large ingestions (CVs, articles, PDFs, writing samples) require a multi-step agentic workflow: saving files to the `sources/` directory, converting to Markdown, running `brain_ingest` with `dry_run=true`, updating multiple Brain files, then calling `brain_ingest_complete`. This needs direct filesystem access beyond what the MCP server exposes for writes (the server writes to `brain/` via `brain_update_file` and to `sources/` only via the ingest pipeline).

Both Cowork and Claude Code work here. Cowork is often more natural for document-driven work since you can drag-and-drop files into the conversation and the agent handles the rest. When completing ingestion, pass the `inbox_file` parameter to `brain_ingest_complete` so the original inbox file is automatically deleted after provenance is recorded.

**Note:** Claude Desktop Chat runs in a container with no host filesystem access. If you attempt large ingestion from Chat, the system will inform you to switch to Cowork or Claude Code.

### Inbox drop-folder

An `inbox/` directory at the Brain repo root serves as a drop-folder for pending sources. Users can drop files there at any time (via Finder, scripts, or automation). The MCP server's `brain_scan_inbox` tool lists pending files, and `brain_load_context` nudges when items are waiting. After ingestion, the `inbox_file` parameter on `brain_ingest_complete` automatically deletes the processed file from the inbox.

This is an alternative to attaching files directly in conversation — useful for batch processing or when files arrive between sessions.

### URL/webpage ingestion

Web content can be ingested as Brain sources without saving an original file. The workflow: fetch the page content (via WebFetch or equivalent), save the markdown to `sources/{category}/{YYYY-MM-DD}_{slug}.md`, update Brain files, then call `brain_ingest_complete` with the markdown path and URL noted in the source label.

### Recommended source categories

Organise source files into typed subfolders within `sources/`. A recommended taxonomy:

| Category | Purpose | Examples |
|---|---|---|
| `bios` | Published bios, speaker packs | LinkedIn about, conference bio |
| `cv` | Formal CVs/resumes only | The PDF you'd send to a recruiter |
| `career_history` | Supporting career evidence | Track records, deal sheets, directorships, publications |
| `assessments` | Psychometric & leadership data | Hogan, 360s, coaching notes |
| `writing_samples` | Published or draft writing | Articles, essays, blog posts |
| `analysis` | Original strategic thinking produced in-session | Decision memos, opportunity evaluations, competitive analyses, board/pitch prep |
| `meeting_notes` | Notes from meetings, calls, boards | Board minutes, advisory call notes |
| `correspondence` | Important emails, letters | Offer letters, key exchanges |
| `personal` | Identity docs, insurance, medical | **Gitignore this folder** — never commit sensitive docs |
| `research` | External articles, reports | Industry news, saved webpages |
| `travel` | Trip plans, bookings | Itineraries, travel docs |
| `favourites` | Personal preferences | Restaurants, hotels, venues |
| `photos` | Headshots, event photos | Speaker photos, press kit images |
| `other` | Genuine catch-all | Anything that doesn't fit above |

Adapt this to your situation — not every category will be needed immediately. The key principle is that `cv` stays narrow (formal CVs only) and everything else has a clear home.

### Vault vs. archive: read scope

The Brain has two read surfaces: the curated `brain/` vault (summarised, linked, kept lean) and the `sources/` archive (full original documents — bio variants, CVs, meeting notes, research). Both are Markdown. The vault is what Claude loads by default; the archive is available on demand.

`brain_read_file` and `brain_search` take a `scope` parameter (`brain` | `sources` | `all` — search only) so Claude can reach into the archive when the vault contains a pointer rather than the full text. `brain_list_sources` enumerates the archive by category. This separation keeps the vault lean (no 2,000-line bios stuffed into identity files) without sacrificing access — when the full source is needed, Claude can fetch it directly.

### Surgical edits with patch mode

The MCP server's `brain_update_file` tool supports three modes: `replace` (full overwrite), `append` (add to end), and `patch` (find-and-replace within a file using `old_content` and `content` parameters). Prefer `patch` for section-level edits — it avoids the risk of accidentally overwriting an entire file when you only need to change a paragraph.

### MCP server code maintenance → Claude Code

The MCP server itself is a TypeScript codebase — editing source files, running builds, testing, linting, and managing git. Claude Code is purpose-built for this kind of iterative software engineering workflow. Cowork can do it, but Code is more ergonomic for build-test cycles.

### Brain content repo maintenance → Claude Code

Git operations on the Brain repo (resolving merge conflicts, rebasing, pushing, managing branches) are best handled in Claude Code where you have direct shell access and git tooling.

### Summary

| Activity | Best client | Why |
|---|---|---|
| Using Brain in conversation | Chat (any client with MCP) | That's what the MCP server is for |
| Small updates (NOW, TASKS, etc.) | Chat | MCP tools handle it directly |
| Large document ingestion | Cowork or Code | Needs filesystem access to `sources/` |
| MCP server code changes | Code | Software engineering workflow |
| Brain repo git maintenance | Code | Shell access, git tooling |

The general principle: **use Chat for consuming and lightly editing Brain content, use Cowork or Code for operations that need filesystem access or agentic multi-step workflows, and use Code specifically for anything that involves software engineering.**

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
