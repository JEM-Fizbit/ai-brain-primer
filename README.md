# AI Brain Primer

**A framework for building a personal AI context system using plain Markdown files.**

Most people re-explain themselves to AI assistants every session — their background, preferences, how they think, what they're working on. An AI Brain fixes that. It's a structured set of Markdown files that give any AI tool persistent, reusable context about you.

This repo contains a comprehensive primer covering the methodology, architecture, and implementation details.

## What's Inside

**[PRIMER_building_your_ai_brain.md](./PRIMER_building_your_ai_brain.md)** — The complete guide, covering:

- **The Four-Layer Model** — Identity, expertise, operating system (how you think and work), and mental models/aspirations. Each layer serves a different purpose and updates at a different cadence.
- **Interview Framework** — Four rounds of structured questions to capture context that documents alone can't provide. Designed to push past generic self-descriptions into specific, actionable instructions.
- **Design Principles** — One topic per file, under 200 lines each, actionable over descriptive, progressive disclosure, source from documents not memory.
- **Recommended File Structure** — A complete architecture with loader, identity, expertise map, work style, writing voice, projects, tools, mental models, and a dynamic `NOW.md` for current priorities.
- **Operational Patterns** — Four processes that keep a Brain healthy as it grows: Ingest (how new information enters), Log (tracking what changed and when), Lint (periodic health checks for staleness, contradictions, bloat), and Index (navigating at scale).
- **Maintenance Cadence** — When to update each file type, how to consolidate insights over time, and how to prune aggressively.
- **Getting Started** — A copy-paste prompt you can feed to Claude (or any AI assistant) to build your Brain in a single session, plus an adaptation prompt for migrating existing context systems.

## Quick Start

1. Gather your primary documents (CV, bios, writing samples) into a folder.
2. Open a Claude session (or any AI assistant).
3. Attach the [primer](./PRIMER_building_your_ai_brain.md) and your documents.
4. Paste the starter prompt from the "Getting Started" section of the primer.
5. Iterate — the first pass gets you 80% there; refinement over the next week finishes the job.

The primer includes detailed instructions for each step, including the exact prompts to use.

## Why Markdown?

Plain Markdown files beat complex memory infrastructure for personal AI context because they're transparent (you can read what the AI "knows"), editable (fix errors in seconds), portable (works with Claude, ChatGPT, Cursor, Copilot, or anything else), versionable (put it in Git), and free.

## Deploying Your Brain

### Recommended: MCP Server (automated, always in sync)

Use **[brain-mcp-server](https://github.com/JEM-Fizbit/brain-mcp-server)** — a generic MCP server that serves your Brain files to any MCP-compatible Claude client. Claude can read, write, search, and git-commit Brain files directly via tool calls. No manual uploading, no stale copies.

Works with Claude Code, Claude Desktop, and Claude Cowork. See the [brain-mcp-server README](https://github.com/JEM-Fizbit/brain-mcp-server#readme) for setup instructions.

### Manual alternatives

If MCP isn't available, your Brain still works anywhere:

| Tool | How to Use |
|------|-----------|
| Claude Projects | Add .md files as project knowledge |
| Claude Cowork | Keep in your mounted workspace folder |
| Claude Code | Place loader as `CLAUDE.md` in project root |
| ChatGPT / Custom GPTs | Paste into custom instructions or knowledge |
| Cursor / Copilot | Add as context files or workspace rules |

## License

[MIT](./LICENSE)

## Origin

This framework was developed through hands-on implementation — building a real AI Brain for daily professional use — and informed by research across practitioner accounts, AI memory architecture literature, and personal user manual methodologies. Sources are listed at the end of the primer.
