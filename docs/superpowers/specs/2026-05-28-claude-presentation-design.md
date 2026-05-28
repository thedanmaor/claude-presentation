# Claude Presentation — Design Spec

**Date:** 2026-05-28  
**Format:** Reveal.js HTML (single file, keyboard-navigable)  
**Audience:** Dev team / engineers  
**Duration:** ~20–30 min (~27 slides)  
**Arc:** Problem → Solution  
**Theme:** Slate/Amber + terminal accents on code/token slides

---

## Visual System

| Element | Spec |
|---|---|
| Background | `#0f172a` (slate-900) |
| Primary accent | `#f59e0b` (amber-500) |
| Secondary accent | `#fbbf24` (amber-400) |
| Text primary | `#f8fafc` |
| Text muted | `#94a3b8` |
| Terminal slides bg | `#0a0a0a` |
| Terminal text | `#22c55e` / `#4ade80` |
| Meta/special slides | `#a78bfa` (violet) |
| Font body | Inter |
| Font code/terminal | JetBrains Mono / Fira Code |
| Top accent bar | `linear-gradient(90deg, #f59e0b, #fbbf24, #fde68a)` |

Terminal aesthetic applies to: tokens, models, pricing table, Claude Code CLI, caveman demo slides.

---

## Slide Structure

### Section 1 · Hook (2 slides)
1. **Title** — "Supercharged Development with Claude" · presenter name · date · amber gradient bar
2. **The Pain** — dev friction today: context switching, slow docs lookup, boilerplate, debugging loops

### Section 2 · Enter Claude (4 slides)
3. **What is Anthropic / Claude** — Anthropic mission, Claude as the product, safety-focused LLM
4. **AI Landscape** — visual comparison table: Claude vs GPT-4o/o3 vs Gemini vs Llama vs Mistral — axes: coding, context, safety, cost
5. **What makes Claude different** — Constitutional AI, character/values, 200k context, coding strength, tool use
6. **Adjacent tools** — Cursor · GitHub Copilot · Codeium · OpenAI Codex · Google Jules — where Claude Code sits relative to each

### Section 3 · Claude Code CLI (4 slides)
7. **Claude Code — what it is** — terminal slide: CLI tool, agentic, runs in your terminal, reads/writes files
8. **Agentic coding** — terminal slide: tools (bash, file R/W, web fetch), MCP servers, multi-step tasks
9. **Plugin ecosystem** — what plugins are, how they extend Claude Code, CLAUDE.md injection
10. **Plugin marketplace** — where to find plugins, how to install (`/install`), examples from marketplace

### Section 4 · The Cost (5 slides)
11. **Tokens explained** — terminal slide: what a token is, input vs output, context window, why it matters
12. **Models — Haiku / Sonnet / Opus** — terminal card style: speed/cost/capability tradeoff per tier
13. **Claude 4 family** — terminal table: Haiku 4.5 · Sonnet 4.6 · Opus 4.7 — IDs, pricing per MTok, best for
14. **Plans — Free / Pro / API / Teams / Enterprise** — comparison table, what each unlocks
15. **Pro plan deep dive** — $20/mo, 5× usage vs free, Claude Code access, what you actually get day-to-day

### Section 5 · My Stack (6 slides)
16. **My 14 plugins — overview** — amber card grid showing all plugins with version badges
17. **Superpowers** — skills system: TDD, debugging, brainstorming, planning, parallel agents · GitHub link
18. **Caveman + Smart Model Router** — terminal demo: token savings % + auto-routing haiku/sonnet/opus
19. **Compound Engineering** — code review agents, ce-correctness, ce-security, ce-performance, ce-brainstorm
20. **BuildPartner / Firecrawl / Morph / Codex** — brief card each: purpose + install command
21. **UI-UX Pro Max / Security Guidance / Skill Creator / Claude Powerline** — brief card each + links

### Section 6 · Real Projects (3 slides)
22. **Projects built with Claude** — RecipEasy · LiveTrigger · Petify · SamplePadManager-OSX — card grid with brief description each
23. **Workflow impact** — before/after: what changed in daily dev workflow, speed, scope of what's buildable
24. **What's next** — MCP expansion, multi-agent pipelines, where this is heading

### Section 7 · 🤯 Meta (2 slides)
25. **How this presentation was made** — screenshots from the visual companion browser session (the brainstorm UI itself), showing the iterative design process: theme selection → structure → approval
26. **The full loop** — prompt → brainstorm (this browser tool) → design spec → implementation plan → Reveal.js build → this slide

### Section 8 · Q&A (1 slide)
27. **Questions + resources** — links: claude.ai, claude.ai/code, plugins marketplace, superpowers GitHub, compound-engineering GitHub, personal plugin list

---

## Technical Spec

- **Single HTML file** — Reveal.js loaded via CDN; no local build step required
- **Slide transitions** — `fade` default, `slide` for section breaks
- **Speaker notes** — added to complex slides (models, pricing, plugins)
- **Plugin download links** — each plugin slide includes inline `code` install command
- **Screenshots** — meta slides embed browser screenshots of the visual companion UI at `localhost:50174` captured during this brainstorm session (visual-theme.html, approaches.html, slide-structure-v2.html)
- **Responsive** — works at 1920×1080 and 1280×720
- **No build step** — open `index.html` in browser, done

---

## Assets Needed

- Screenshots of this brainstorm session (visual-theme.html, approaches.html, slide-structure-v2.html)
- Project screenshots: RecipEasy, LiveTrigger, SamplePadManager-OSX, Petify (from README or screenshots if available)
- Plugin logos/icons (optional — fall back to styled text cards)

---

## Success Criteria

- Opens in browser, no build step required
- All 27 slides present, keyboard-navigable
- Plugin slides each have working install command/link
- Meta slide includes actual screenshots from this brainstorm session
- Looks professional at full-screen projection resolution
- Terminal-aesthetic slides clearly distinct from regular slides
