# Crazy Bob v5 🤪 — Dual-Core Memory + Sleep Cycle

Private on-device AI (WebLLM + WebGPU). Search tools from v4 remain intact.

## What is new (safe improvements only)

### 1. Dual-core memory
- **Working memory** — in-session slots: goal, project, mood
- **Episodic memory** — structured micro-episodes in IndexedDB
- **Semantic profile** — permanent user profile (unchanged, improved)

### 2. MemGPT-style self-edits
Bob may emit hidden tags such as:
`<memory_edit action="append" target="user_profile">fact</memory_edit>`
Targets: `user_profile`, `episode`, `working_goal`, `project`, `mood`

### 3. Sleep & dream idle cycle
While idle (model loaded, tab visible):
- Embed missing document vectors
- Consolidate duplicate rules
- Reflect on tool failures → new rules
- Optional **proactive goals** pulse

### 4. Proactive goals (opt-in)
Settings → enable Proactive goals, add goals, optionally Enable notifications.
Bob surfaces one due goal during idle — never spam.

### 5. Skills store (declarative only)
IndexedDB `skills` exists for HTTPS URL templates.
**No arbitrary JS eval** — that would break security and search stability.

## Intentionally NOT implemented
- Model-written executable JavaScript tools (unsafe on a phone PWA)

## Still included
All v4 search chips (news, research, web search, weather, currency, crypto, define, translate, URL summarise), CoT, team mode, RAG+RRF, token budget, auto model restore, API key test buttons.

## iPhone tip
Start with SmolLM2 360M. Load once; later opens restore from cache.
