# Continuity and Memory Reference

Long-form fiction fails when story state is left inside ephemeral prompts. Durable memory should be explicit, inspectable, and cheap to retrieve.

## 1. Canon layers

Mark every stored assertion with one of these states:

- **established** — appears in accepted manuscript or explicit author decision
- **planned** — intended future event, not yet canon in-world
- **provisional** — useful working assumption that may change
- **speculative** — brainstorm only
- **retconned** — no longer true, preserved only for history

Never let retrieval blur these states.

## 2. Canon hierarchy

When sources conflict, prefer:

1. explicit latest author decision
2. accepted manuscript
3. current-truth / canon file
4. structured character/world state
5. approved outline
6. chapter summary
7. research notes
8. semantic retrieval
9. model inference

A model's remembered phrasing is never authority.

## 3. Minimum durable ledgers

### Current truth

Keep a compact file containing:

- current date/time in story
- current locations of major characters
- current injuries/resources
- major relationship states
- active threats
- unresolved mysteries
- next committed events
- recent canon changes

### Event ledger

Each important event:

- event ID
- date/time
- location
- participants
- cause
- action
- consequence
- evidence / chapter
- canon status

### Character state

Track only dynamic facts that can matter later:

- location
- physical condition
- possessions
- obligations
- goals
- beliefs
- secrets held
- secrets exposed
- relationship deltas
- emotional commitments

### Knowledge matrix

Rows are facts/secrets; columns are characters or institutions.

State values may be:

- knows
- suspects
- false belief
- deliberately deceived
- unaware

Add source chapter and time.

### Resource ledger

For stories where logistics matter, track:

- power
- water
- propellant/fuel
- food
- medicine
- spare parts
- vehicles
- weapons/tools where relevant
- habitat capacity
- money/credit/political capital where relevant

Do not allow prose to spend the same scarce resource twice.

### Promise ledger

Track:

- mystery
- threat
- clue
- symbolic object
- relationship promise
- technical mechanism
- stated deadline
- prophecy/plan/mission objective

For each, mark open, partially paid, paid, abandoned intentionally, or accidental orphan.

## 4. Chapter summaries

A useful chapter summary is not a recap of every paragraph.

Capture:

- what changed
- decisions made
- newly established facts
- new knowledge by character
- relationship changes
- resource changes
- injuries/losses
- plants/payoffs
- open questions
- next-state constraints

Keep it concise enough to retrieve often.

## 5. Retrieval strategy

Build context in layers.

### Pinned context

Always include only what is truly global:

- premise/theme tension
- style constraints
- POV rule
- a compact current truth

### Exact retrieval

Use exact lookups for:

- dates
- names
- ages
- measurements
- resource quantities
- legal rules
- technology constraints
- relationship state
- who knows a specific fact

### Semantic retrieval

Use vector or hybrid retrieval for:

- similar prior scenes
- relevant descriptive details
- old conversations about a location
- thematic echoes
- historical research
- prior uses of a motif

### Recent context

Include the directly preceding scene or chapter excerpt when prose continuity matters.

## 6. RAG rules

RAG improves recall but creates two risks: irrelevant context and false authority.

Rules:

- retrieve few high-value chunks, not everything similar
- label the source and canon status
- prefer hybrid keyword + semantic retrieval for names and exact concepts
- rerank when possible
- avoid retrieving future-outline spoilers into a character-limited drafting context unless the writer role needs them
- never turn a retrieved brainstorm into canon automatically
- do not let an embedding hit override exact structured state

## 7. After-draft extraction

After a chapter is accepted, run a state extraction pass.

The extraction pass should not rewrite the chapter. It should produce proposed updates.

Validate:

- exact names
- time movement
- location movement
- new injuries
- items acquired/lost
- facts learned
- promises created/resolved
- relationship shifts
- numerical/resource changes

Only then merge into durable canon.

## 8. Contradiction handling

When a contradiction appears:

1. identify both claims
2. identify their authority level
3. determine whether the difference can be explained in-world
4. if not, choose a correction path
5. record the correction / retcon
6. inspect downstream dependencies

Never quietly "average" conflicting facts.

## 9. Memory compression

As the series grows, summarize in layers:

- scene -> scene summary
- chapter -> state delta
- book -> book-state snapshot
- series -> current truth

Keep raw manuscript available for retrieval. Do not repeatedly summarize summaries until nuance disappears.

## 10. Multi-agent safety

If several agents draft or research in parallel:

- give each an immutable canon snapshot
- assign non-overlapping scope
- require structured deltas
- merge through one canon-maintainer pass
- reject invented IDs or entities when exact identities exist
- preserve a decision log

Parallel generation is useful. Parallel canon mutation without arbitration is dangerous.

## 11. Local memory implementations

Useful implementation patterns seen in open-source writing systems include:

- editable memory banks
- character/world state surfaces
- lorebooks or World Info
- author's notes pinned near generation
- knowledge graphs of characters/events/relationships
- SQLite-backed canon with vector search
- chapter summaries plus dynamic state
- MCP-accessible memory services

The implementation can vary. The invariants above should not.
