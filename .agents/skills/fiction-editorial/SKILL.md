---
name: fiction-editorial
description: Plan, draft, continue, revise, and edit long-form fiction with durable canon, scene-level causality, character-state tracking, continuity control, research boundaries, and staged editorial passes. Use for novels, multi-book series, hard science fiction, story bibles, outlines, chapter/scene drafting, developmental edits, line edits, continuity audits, dialogue/voice work, foreshadowing, pacing, and local-LLM writing workflows.
license: CC-BY-4.0
metadata:
  version: "1.0.0"
  reviewed: "2026-09-28"
  scope: "long-form fiction and editorial workflows"
---

# Fiction Editorial

Use this skill as an operating system for serious long-form fiction. The manuscript is not a chat transcript. Canon, character state, unresolved promises, research boundaries, and editorial decisions must remain inspectable outside any one model context.

## Core rules

1. **Canon outranks conversational memory.** Treat project files and explicit user decisions as the source of truth. Never silently replace an established fact with a plausible invention.
2. **Separate creative roles.** Do not ask one pass to architect, draft, continuity-check, fact-check, line-edit, and proofread at once. Each pass gets a defined job and edit budget.
3. **Story is caused by choices under pressure.** A scene must change state. Events that merely happen are setup, texture, or exposition until a character must choose and pay a consequence.
4. **Track information, not only events.** For every important secret, threat, plan, and discovery, know who knows what, when they learned it, what they believe incorrectly, and what they are hiding.
5. **Theme is a contested question, not a slogan.** Build opposed humanly defensible answers into characters and institutions. Let consequences argue the theme.
6. **For hard SF, physics is dramatic structure.** Convert technical constraints into deadlines, resource conflicts, failure modes, and irreversible choices. Intelligence cannot erase mass, energy, latency, radiation, inventory, or time.
7. **Long context is not durable memory.** Keep a compact current truth plus structured ledgers; retrieve only what the current scene needs.
8. **RAG is recall, not authority.** Semantic retrieval can surface candidate context. Canonical files, exact timelines, and explicit state tables decide what is true.
9. **Preserve voice during editing.** A cleaner sentence is not automatically a better sentence. Keep deliberate awkwardness, fragments, repetition, dialect, punctuation, and rhythm when they belong to a character or established narrative voice.
10. **Revision proceeds from large to small.** Do not polish sentences in scenes that may be cut.

## Default workflow

### Phase 0 — Ingest and establish current truth

Before creating new prose, locate or create:

- premise / series promise
- current canon
- character roster and current states
- world and technology rules
- timeline
- unresolved threads and planted payoffs
- style/voice sample
- research boundary: established fact vs design assumption vs speculative invention
- manuscript and chapter summaries

If the project already exists, read before inventing.

For large projects, keep one compact `CURRENT_TRUTH.md` or equivalent that answers: where are we, what is definitely true now, what is unresolved, what changed most recently, and what must not be contradicted.

### Phase 1 — Premise, thematic engine, and series architecture

Define:

- external dramatic problem
- protagonist's conscious objective
- deeper need or false belief
- principal antagonistic forces
- thematic contradiction
- genre promise
- hidden question the reader slowly discovers
- end-state transformation

For a trilogy or series, each book must close a meaningful local arc while changing the state of the larger conflict irreversibly.

Use [story-architecture.md](references/story-architecture.md).

### Phase 2 — Characters and conflict

For major characters, track:

- public role
- private desire
- need / misbelief
- fear
- leverage
- moral boundary
- secret
- contradiction
- relationship vectors
- pressure response
- voice fingerprint
- starting and target state

True character is revealed by costly choice under pressure, not by profile prose. Antagonists need coherent goals and the power to force adaptation.

### Phase 3 — World, research, and constraint model

For research-heavy fiction, divide claims into:

- **fact** — externally supported
- **project canon** — chosen and fixed for the story
- **assumption** — plausible but uncertain
- **speculation** — intentionally invented
- **unknown** — unresolved and not to be guessed away

For hard SF, keep numerical and causal constraints stable. Prefer a real limitation that produces story pressure over a new technology invented solely to escape a corner.

### Phase 4 — Chapter and scene design

A chapter needs a dramatic movement, not just a topic.

Before drafting an important scene, know:

- POV
- time and location
- entering state
- viewpoint character's immediate want
- obstacle / opposing want
- escalation sequence
- critical information state
- decision or irreversible action
- consequence
- state change
- planted clue/payoff
- exit energy: question, danger, emotional reversal, discovery, or commitment

Use [scene-card-template.md](assets/scene-card-template.md).

A scene that contains no want, opposition, meaningful discovery, or state change should justify its existence as atmosphere, compression, transition, or deliberate pause.

### Phase 5 — Context assembly before drafting

Build a **small, deliberate context pack**:

1. style/voice guidance
2. current scene card
3. immediately previous prose or short summary
4. current states of characters actually present
5. exact canon facts relevant to the scene
6. unresolved threads that can plausibly move here
7. retrieved world/research material if needed

Do not dump the full story bible or full manuscript into every call.

At high-leverage turns, it is useful to generate two genuinely different options and choose deliberately. Do not branch every paragraph or outsource the final choice to the model.

### Phase 6 — Draft

Draft for causality and lived experience before polish.

Prefer:

- concrete perception over generic atmosphere
- action and dialogue that expose competing objectives
- subtext over explanatory dialogue
- specific physical consequences over abstract statements of danger
- selective technical detail with narrative function
- sentence rhythm that follows attention, stress, and POV

Avoid using an exposition scene to explain what two informed characters already know. Put facts inside disagreement, diagnosis, error, procedure, consequence, or discovery.

### Phase 7 — Post-chapter state update

After every completed chapter, update durable memory:

- event ledger
- character states
- relationship changes
- timeline
- locations
- injuries / possessions / resources
- knowledge matrix
- promises, clues, debts, mysteries
- technical/factual commitments
- unresolved threads
- chapter summary

Use [continuity-memory.md](references/continuity-memory.md).

### Phase 8 — Editorial passes

Run separate passes in this order unless the user asks otherwise:

1. developmental / structural
2. chapter and scene function
3. continuity / logic / factual consistency
4. character arc / POV / knowledge
5. dialogue and subtext
6. line and image
7. anti-generic / anti-AI-pattern pass
8. copyedit / proof

Never use a copyedit pass to solve a broken motive or a developmental pass to obsess over commas.

Use [editorial-workflow.md](references/editorial-workflow.md).

## Hard-SF action conversion

When adapting technical material into fiction, use this chain:

`constraint -> failure mode -> warning signs -> limited options -> human/machine disagreement -> costly choice -> consequence -> new state`

Good action arises when every available option preserves one thing by sacrificing another.

Examples of productive constraints:

- communications delay or blackout
- finite power
- storage boil-off
- maintenance inventory
- radiation dose
- landing geometry
- pressure integrity
- thermal limits
- launch windows
- biological contamination
- uncertain resource maps
- incompatible safety layers

Do not solve a crisis by revealing an unplanted capability.

## Hidden-idea discipline

A hidden idea should be visible in retrospect but not announced early.

Track it through:

- repeated choices with different surface causes
- mirrored scenes
- changes in vocabulary
- institutional rules that acquire new meanings
- technical mechanisms that later become moral mechanisms
- character decisions that first look tactical and later reveal a worldview

A reveal should reorganize prior events, not merely add new information.

## Prose quality checks

Before finalizing a scene or chapter, ask:

- Can I identify the viewpoint's immediate desire?
- What changes because this scene happened?
- What is the hardest choice?
- What does each speaker want from the other?
- Is the danger concrete?
- Did exposition enter through dramatic need?
- Is any paragraph repeating a conclusion the reader already inferred?
- Are multiple characters speaking in the same polished voice?
- Are there generic dramatic fragments, forced triads, stock aphorisms, excessive dashes, vague intensifiers, or repeated rhetorical templates?
- Does the ending create genuine forward pressure rather than a manufactured cliffhanger?

Use anti-AI-pattern rules as editing signals, not as a detector of authorship.

## Local LLM workflows

When local models are part of the process, decouple the manuscript/canon layer from the model and UI. Prefer standard APIs and swappable roles.

Good local roles include:

- continuity extraction
- chapter summaries
- entity/state updates
- alternate paragraph generation
- tagging and retrieval
- grammar/copy cleanup
- lightweight critique
- privacy-sensitive material

Use stronger reasoning/writing models for high-level architecture, difficult rewrites, and final developmental judgment when available.

See [local-llm-workflow.md](references/local-llm-workflow.md).

## Output behavior

When asked to brainstorm, provide choices and implications rather than pretending one formula is mandatory.

When asked to draft prose, draft prose rather than returning a craft lecture.

When asked to edit, state the scope of the pass and preserve facts and intentional voice.

When a contradiction is found, do not silently repair canon. Identify it and propose the smallest coherent resolution.

When the user has already made a creative decision, treat it as a constraint unless they explicitly reopen it.

## Reference files

- [story-architecture.md](references/story-architecture.md) — premise, trilogy structure, character, scene causality, suspense, hard-SF conversion
- [continuity-memory.md](references/continuity-memory.md) — canon layers, event/knowledge ledgers, RAG, retrieval, state updates
- [editorial-workflow.md](references/editorial-workflow.md) — staged revisions and concrete checklists
- [local-llm-workflow.md](references/local-llm-workflow.md) — local backends, writing frontends, model roles, context strategy
- [source-map.md](references/source-map.md) — GitHub projects surveyed and transferable ideas
- [story-bible-template.md](assets/story-bible-template.md)
- [scene-card-template.md](assets/scene-card-template.md)
- [editorial-report-template.md](assets/editorial-report-template.md)
