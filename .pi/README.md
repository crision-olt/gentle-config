# Configuration: Learning & Visibility

This directory holds Engram (persistent memory), MCP servers (documentation & tools), and persona variants for observing the harness at work.

## What's now configured

### 1. **Persistent Memory (Engram)**
- **Package**: `gentle-engram` v0.6.0
- **What it does**: Saves decisions, bugs, patterns, and discoveries across sessions so you don't lose learnings when context compacts
- **Visible in**: Memory tool calls (`mem_save`, `mem_search`) show what the harness is learning and storing
- **Side conversations**: `pi-btw` skill lets you ask side questions without interrupting main work

### 2. **MCP Servers (Tools)**
- **context7**: Fetches current documentation for libraries, frameworks, APIs, CLIs (React, Prisma, Django, etc.)
- **web-access**: Broader internet access for research and fact-checking

Both surface their searches and fetch operations so you see what sources the harness is consulting.

### 3. **Persona: Learner Variant**
Run with: `echo '{"mode":"gentleman","variant":"learner"}' > .pi/gentle-ai/persona.json`

This variant surfaces orchestrator decisions:
- **ODD phases**: Authorize → Explore → Resolve → Classify → Track → Implement → Verify → Close
- **Delegation triggers**: Why work moves to a subagent (evidence budget exceeded, writer reason, high-risk verification)
- **Task size**: Why something is small (inline, no tracking) vs. large (gets a feature doc, subagents, commits)
- **Memory operations**: When discoveries are saved, searched, or updated
- **Risk assessment**: What risk items apply to changes and why they matter
- **Decision reasoning**: Why the harness chooses one path over another

## How to use

1. **Keep learner variant on** while you're learning the harness patterns
2. **Use memory** (`mem_context`, `mem_search`) to see what survived from past sessions
3. **Watch the logs** when ODD phases change or delegation fires — that's when you learn what the harness is doing
4. **Ask side questions** with `/btw` when you want to explore without interrupting work

## Next: Try it

Switch to learner:
```bash
echo '{"mode":"gentleman","variant":"learner"}' > .pi/gentle-ai/persona.json
```

Or keep gentleman (default) and add visibility by asking questions like:
- "Why did you delegate this to a subagent?"
- "What's in memory about this project?"
- "Show me the ODD phase this work is entering"

---

**Risk**: none (configuration only; no code changes)
