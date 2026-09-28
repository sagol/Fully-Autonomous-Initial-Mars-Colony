# Source Map and Design Provenance

Survey date: 2026-09-28.

This skill is an original synthesis. It does not copy any one project's workflow. The repositories below were surveyed for transferable patterns in long-form fiction, editorial practice, agent skills, memory, RAG, and local inference. Repositories evolve; re-check current documentation before relying on implementation details.

## Agent skill structure

### agentskills/agentskills
https://github.com/agentskills/agentskills

Transferable idea:
- portable skill folder centered on `SKILL.md`
- progressive disclosure through references and assets
- concise trigger description plus deeper supporting material

### jtydhr88/screenwriting-skills
https://github.com/jtydhr88/screenwriting-skills

Transferable ideas:
- modular craft skills instead of one giant prompt
- character revealed by pressure and choice
- scene wants, obstacles, escalations, decisions, consequences
- "who knows what when" information design
- hooks rooted in character jeopardy and turning points
- references separated from operational skill instructions

### PenglongHuang/chinese-novelist-skill
https://github.com/PenglongHuang/chinese-novelist-skill

Transferable ideas:
- explicit initialization and resumption
- planning before drafting
- chapter-by-chapter workflow
- post-draft validation
- preference and state persistence

## Long-form fiction workspaces

### iLearn-Lab/NovelClaw
https://github.com/iLearn-Lab/NovelClaw

Transferable ideas:
- dynamic-memory-first long-form workflow
- editable memory banks
- manuscript, world, and character surfaces
- chapter monitoring and inspectable artifacts
- repeated continuation from durable state rather than a one-shot prompt

### heider-x/vela
https://github.com/heider-x/vela

Transferable ideas:
- local-first novel IDE
- character state across chapters
- local RAG
- outline -> chapter drafting
- rewrite / refine / review separation
- revisions exposed as changes rather than silently replacing text

### tallman2014/fiction-project-scaffold
https://github.com/tallman2014/fiction-project-scaffold

Transferable ideas:
- project-management layer
- `CURRENT_TRUTH`
- story bible, chapter cards, dialogue system
- writing-state tracking
- research boundaries and isolated research workflow
- ordinary files as durable project infrastructure

### adaumann/speckit-preset-fiction-book-writing
https://github.com/adaumann/speckit-preset-fiction-book-writing

Transferable ideas:
- treat fiction as a multi-stage production workflow
- templates for characters, worlds, timelines, scenes, revisions, and exports
- explicit POV and style modes
- separate planning, drafting, revision, and submission operations

### dylanhogg/gptauthor
https://github.com/dylanhogg/gptauthor

Transferable idea:
- long-form, multi-chapter generation benefits from explicit structure above individual chapter prompts

### raestrada/storycraftr
https://github.com/raestrada/storycraftr

Transferable idea:
- reusable story-planning agents and outline stages

### Lanerra/saga
https://github.com/Lanerra/saga

Transferable ideas:
- structured character/event/relationship extraction
- scene-scoped context retrieval
- canonical identity checks
- quality acceptance records and recoverable workflow state

### emberspun/longform-memory
https://github.com/emberspun/longform-memory

### emberspun/longform-memory-mcp
https://github.com/emberspun/longform-memory-mcp

Transferable idea:
- long-form memory can be externalized as its own service rather than trapped inside the writer model.

## Creative-writing interaction patterns

### p-e-w/arrows
https://github.com/p-e-w/arrows

Transferable ideas:
- paragraph as a natural completion unit
- two alternatives at a decision point
- author selects the branch
- backend kept separate from writing UI
- concurrent generation can exploit a shared prompt

### SillyTavern/SillyTavern
https://github.com/SillyTavern/SillyTavern

Transferable ideas:
- World Info / lorebook
- Author's Note
- context inserted at controlled positions
- constant, keyed, and vectorized lore
- checkpoints

### LostRuins/koboldcpp
https://github.com/LostRuins/koboldcpp

Transferable ideas:
- writer-oriented local inference
- memory, World Info, Author's Note, characters, scenarios
- storywriter mode
- OpenAI/Ollama-compatible APIs
- local RAG / text database features
- MCP/tool integration

### nhaouari/obsidian-textgenerator-plugin
https://github.com/nhaouari/obsidian-textgenerator-plugin

Transferable idea:
- AI capability can sit on top of ordinary Markdown notes instead of owning the project format.

### theJayTea/WritingTools
https://github.com/theJayTea/WritingTools

Transferable idea:
- local LLMs can provide lightweight writing assistance without a cloud-only workflow.

## Editorial / style analysis

### blader/humanizer
https://github.com/blader/humanizer

Transferable ideas:
- structural AI-writing habits are more useful editing signals than word blacklists
- preserve source meaning
- match an established author voice
- inspect paragraph shape and rhetorical repetition, not only vocabulary

Patterns worth checking include staged openers, redundant dramatic closers, forced triads, repeated templates, excessive dash use, empty aphorisms, and fake objections. These are signals for editing, not proof of authorship.

### conorbronsdon/avoid-ai-writing
https://github.com/conorbronsdon/avoid-ai-writing

Transferable ideas:
- detection does not automatically authorize rewriting
- preserve source fidelity
- use voice profiles and iterate with controlled scope
- treat "AI tells" as fallible quality signals

### lechmazur/writing
https://github.com/lechmazur/writing

Transferable ideas:
- evaluate whether required story elements are meaningfully integrated rather than merely mentioned
- separate prose, coherence, character, originality, and overall effectiveness

### lechmazur/writing_styles
https://github.com/lechmazur/writing_styles

Transferable editorial axes:
- voice and diction
- concreteness
- rhythm and syntax
- POV and narrative distance
- structure and pacing
- tone
- imagery
- dialogue and subtext
- experimentation
- closure

The project's model rankings are not imported into this skill. The useful part is the multidimensional evaluation framework.

## Local inference

### ggml-org/llama.cpp
https://github.com/ggml-org/llama.cpp

Transferable ideas:
- local GGUF inference across broad hardware
- quantization
- CPU/GPU hybrid execution
- OpenAI-compatible server
- batching and prompt reuse

### ollama/ollama
https://github.com/ollama/ollama

Transferable ideas:
- simple local model management
- REST API
- easy integration point for writing apps and agents

### theroyallab/tabbyAPI
https://github.com/theroyallab/tabbyAPI

Transferable ideas:
- OpenAI-compatible local API
- ExLlamaV3 backend
- concurrent / continuous batching
- embeddings and constrained outputs
- model load/unload

### turboderp-org/exllamav2
https://github.com/turboderp-org/exllamav2

Historical / architectural ideas:
- paged attention
- dynamic batching
- prompt caching
- GPU-focused quantized inference

The repository states that ExLlamaV2 is archived and development continues with ExLlamaV3, so new workflows should not be designed around V2 as the future-facing backend.

### open-webui/open-webui
https://github.com/open-webui/open-webui

Transferable ideas:
- self-hosted multi-model workspace
- persistent memory
- local RAG and hybrid retrieval
- model comparison and reusable project context

## What this skill intentionally does not import

- rigid "every novel must use this beat sheet" formulas
- automatic canon mutation by drafting agents
- model leaderboard rankings as universal writing truth
- prose "humanization" as synonym substitution
- full-manuscript prompt stuffing
- agent swarms without one canonical merge authority
- one-shot whole-novel generation as the default workflow

## Synthesis principles adopted here

Across the surveyed systems, the strongest repeated ideas were:

1. externalize canon and dynamic state
2. retrieve only relevant context
3. separate planning, drafting, extraction, critique, and editing
4. keep every revision inspectable
5. make character choice and scene state change the unit of drama
6. track information state as carefully as event state
7. treat research uncertainty explicitly
8. use local models for high-volume structured work when appropriate
9. keep inference backends swappable behind standard APIs
10. preserve author agency at consequential creative branches
