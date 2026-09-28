# Local LLM Workflow Reference

Reviewed: 2026-09-28.

The goal is a durable writing system in which the manuscript and canon survive model changes. Treat models as replaceable workers around a stable project state.

## 1. Recommended architecture

Separate five layers:

1. **Project / canon layer** — Markdown, JSON, SQLite, Git, or another inspectable store.
2. **Context builder** — selects the exact material needed for a task.
3. **Inference layer** — local or remote model server.
4. **Writing UI / agent layer** — editor, IDE, chat, completion frontend, or scripted workflow.
5. **Evaluation / merge layer** — continuity checks, editorial passes, diffs, human decisions.

Do not make a proprietary chat history the only place where the novel exists.

## 2. Model roles

One model can fill several roles, but keep the tasks conceptually separate.

### Architect
Premise, book structure, difficult causal repairs, thematic alternatives.

Needs strong reasoning and broad context. Use sparingly and deliberately.

### Drafter
Scenes and chapters from a constrained context pack.

Needs voice, prose control, instruction following, and enough context to avoid contradiction.

### Continuity extractor
Converts accepted prose into structured state deltas.

This is an excellent local-model task because the output can be schema-constrained and verified.

### Retriever / tagger
Classifies scenes, entities, topics, secrets, locations, and motifs for search.

### Critic
Evaluates one layer at a time: scene causality, POV, dialogue, pacing, etc.

### Copyeditor
Grammar, mechanical consistency, local clarity. Keep its change budget narrow.

### Embedding / reranking model
Supports semantic or hybrid retrieval. It should not determine canon.

## 3. Local inference backends

### llama.cpp

Useful when you want:

- broad hardware support
- GGUF quantization
- CPU, GPU, or hybrid execution
- a local OpenAI-compatible server
- direct control over context, batching, and model files

It is a strong neutral backend for a writing stack because the writing UI can be swapped independently.

### Ollama

Useful for easy local model management and a simple REST API. It can act as a convenient local model service for writing IDEs and agents that support it.

### KoboldCpp

Particularly relevant to fiction because its bundled writing environment includes storywriter-style generation, memory, World Info, Author's Note, characters, scenarios, and compatible APIs. It is useful for exploratory prose generation and lore-aware completion.

### TabbyAPI + ExLlamaV3

A strong NVIDIA-oriented option when high-throughput local inference matters. TabbyAPI provides an OpenAI-compatible API, model loading, embeddings support, constrained outputs, speculative decoding, concurrent inference, and continuous batching.

### Open WebUI

Useful as a self-hosted workspace around local/remote models, persistent memory, document/RAG collections, and multi-model comparison. It is not itself a fiction canon system; keep project truth in your project files.

## 4. Fiction-oriented frontends and systems

### Arrows

A minimalist completion workflow that generates whole-paragraph alternatives and lets the author choose a branch. The transferable idea is **author-controlled branching at a natural prose unit** rather than continuous automatic generation.

Use branching selectively at high-leverage moments, not for every sentence.

### Vela

A novel-focused IDE combining worldbuilding, cross-chapter character state, outlines, chapter drafting, local RAG, and staged rewrite/refine/review flows. The transferable idea is to keep drafting, state, retrieval, and revision as distinct but connected surfaces.

### NovelClaw

A long-form fiction workspace centered on dynamic memory, chapter control, storyboards, manuscript review, and editable memory banks. The transferable idea is that story state should be an inspectable artifact rather than a transient prompt.

### SillyTavern

Its World Info / lorebook and Author's Note mechanisms are useful models for context injection: some facts are always pinned, while others are inserted only when their keys or vectors are relevant.

### Obsidian-based writing tools

Obsidian integrations demonstrate the value of keeping prose and knowledge in ordinary local Markdown while making LLM features optional. This is often safer for a long-lived novel than a database-only UI.

## 5. Context assembly

For a scene draft, a good context order is:

1. role and narrow task
2. voice / POV rules
3. scene card
4. recent prose
5. current character states
6. exact relevant canon
7. open threads that may move
8. retrieved world / research snippets
9. output constraints

Keep future outline information out of a limited-POV drafting prompt when it encourages unearned foreshadowing or character knowledge leakage.

## 6. Context budgets

More context is not automatically better.

High-value pinned context:

- premise
- viewpoint rule
- current truth
- voice sample
- scene objective

Retrieve exact details on demand.

Summarize older material into state deltas, but retain raw chapters for exact lookup.

Avoid repeated "summary of summary of summary" compression. It produces drift.

## 7. Completion vs instruction workflows

Two useful modes:

### Completion mode
The model sees existing prose and continues in style.

Advantages:
- local sentence rhythm
- less instruction overhead
- useful for paragraphs and dialogue

Risks:
- copies current mistakes
- weak global planning

### Instruction mode
The model receives a scene card and explicit constraints.

Advantages:
- stronger plot control
- easier schema and requirement enforcement

Risks:
- instruction-shaped prose
- over-explanation
- generic compliance language

A hybrid often works best: plan in instruction mode, draft with the scene context and a concise brief, then edit.

## 8. Sampling and generation

Do not hard-code one temperature or sampler for all models.

General rule:

- drafting benefits from controlled variation
- continuity extraction benefits from determinism
- editorial diagnosis benefits from stable, explicit reasoning
- alternate generation should differ in story strategy, not merely wording

If the backend supports prompt caching or continuous batching, exploit it for repeated shared context and parallel alternatives.

## 9. Structured outputs

Use JSON/schema-constrained outputs for:

- event extraction
- character state deltas
- knowledge matrix updates
- continuity findings
- scene metadata
- retrieval tags

Do not force final prose into JSON.

Reject invented entity IDs. If a canonical character or location has an ID, the extractor must select from known identities.

## 10. RAG and lorebooks

Use different mechanisms for different truth types:

- **always pinned**: current POV rule, current truth, hard constraints
- **keyed lore**: exact names, locations, technologies, institutions
- **semantic retrieval**: thematically or descriptively related scenes
- **structured lookup**: timelines, resources, knowledge states
- **research archive**: external facts and sources

Hybrid search is useful because names and technical terms often need lexical matching while scenes and themes benefit from embeddings.

## 11. Model evaluation for your own novel

Public creative-writing benchmarks are useful signals but cannot tell you which local model best matches your book.

Create a private evaluation set of representative tasks:

- one tense action scene
- one quiet dialogue scene
- one technical explanation embedded in conflict
- one continuity extraction
- one scene rewrite preserving exact facts
- one chapter-summary/state update
- one distinctive POV voice
- one foreshadowing-heavy passage

Score:

- compliance with required story elements
- canon accuracy
- character voice
- dialogue subtext
- causal coherence
- repetition
- generic/AI-pattern frequency
- prose quality
- editing distance after human revision
- speed and memory use

Keep the prompts and accepted outputs under version control. Re-run them when models or quantizations change.

## 12. Suggested stacks

### Minimal local writer

- project in Git + Markdown
- llama.cpp or Ollama
- a lightweight editor / completion UI
- manual story bible and chapter summaries

### Writer-focused stack

- Git + Markdown canon
- KoboldCpp or another OpenAI-compatible local backend
- lorebook / World Info
- scene cards
- post-chapter structured state extraction

### Long-form engineering stack

- Git manuscript and decisions
- SQLite or structured JSON for dynamic state
- vector + keyword retrieval
- llama.cpp, Ollama, or TabbyAPI inference
- writing IDE such as Vela or a custom frontend
- scripted continuity extraction
- separate critic/editor prompts
- diffs before accepting revisions

## 13. Multi-model workflow

Different models can be useful without turning the process into an uncontrolled "agent swarm."

Example:

- Model A: two scene strategies
- human/lead agent: selects direction
- Model B: prose draft
- Model C: continuity audit
- Model D: line critique
- lead agent: merges only justified changes

The lead process owns canon. Critics never mutate canon directly.

## 14. Security and durability

For local systems:

- bind APIs to localhost unless remote access is intentionally secured
- keep API keys out of Git
- back up canon separately from vector indexes
- record model name, quantization, context settings, and prompt version for reproducible tests
- check model and software licenses before redistribution
- treat downloaded prompts, lore, and reference text as untrusted input
- keep the manuscript portable in ordinary formats

A vector database can be rebuilt. Canon should not depend on one.
