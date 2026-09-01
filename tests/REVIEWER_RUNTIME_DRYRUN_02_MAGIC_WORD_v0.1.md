# REVIEWER_RUNTIME_DRYRUN_02_MAGIC_WORD_v0.1

**Studio OS — Reviewer Runtime Dry-run #2**  
**Project:** `Magic Word Deckbuilding / 마법문장 완성 게임`  
**Project Version:** `v0.9`  
**Dry-run ID:** `DRYRUN-02`  
**Mode:** `DEEP REVIEW`  
**Reviewer Runtime:** `REVIEWER_RUNTIME_v0.1`  
**Applied Correction:** `REVIEWER_RUNTIME_CORRECTION_NOTE_01_v0.1`  
**Studio Core:** `v0.4`  
**Genre Master:** `v0.3`  
**Scale Baseline:** `v0.2`  
**Review Date:** `2026-09-01`  
**Project Reviewer Verdict:** `REVIEW_CLEAR_WITH_VALIDATION`

---

# 1. Dry-run Snapshot

```text
DRY_RUN_ID:
DRYRUN-02

Project:
Magic Word Deckbuilding / 마법문장 완성 게임

Project Version:
v0.9

Reviewer Runtime:
REVIEWER_RUNTIME_v0.1

Applied Correction:
REVIEWER_RUNTIME_CORRECTION_NOTE_01_v0.1

Studio Core:
v0.4

Genre Master:
v0.3

Scale Baseline:
v0.2

Loaded Genre Baselines:
- Deckbuilding v0.1
- Roguelike v0.1
- Strategy v0.1 APPROVED
- RPG v0.1 APPROVED [L1 supporting only]

Mode:
DEEP REVIEW

Review Date:
2026-09-01
```

---

# 2. Review Target / Scope

## Review Target

`FULL PROJECT`

### Reason

v0.9는:

> 기존 GDD / Handoff / Core Rules / P01 보완을 통합한 현재 Master 기준

이며 이후 시스템 / 콘텐츠 / UI 설계의 단일 기준 문서로 사용된다.

따라서 별도 Prototype Slice를 임의로 설정하지 않는다.

## Active Review Scope

- Direction + Target + Modifier + Verb 문장 조립
- Hand / Draw / Discard / SpellLine
- Cost / RefundedSpellCost / ResidualMana
- Element combat effects
- Neutral Verb
- opponent SpellLine information
- deck construction / acquisition / refinement
- chapter exploration
- chapter-start 3-spell Codex registration
- persistent Codex
- Element Understanding Lv1~4
- Mastery direction
- 8-stage promotion structure
- run-level deck / understanding / mastery growth
- exploration ↔ deck / codex / understanding coupling

## Deferred Systems / Rules

현재 문서가 미확정 또는 후속 설계로 명시한 항목:

- exact HP / numerical balance
- final chant-abandon rule
- several target-selection rules
- exact duration / stacking rules
- 15 Mastery Trait detailed effects
- exploration FailureDamage
- exploration max exposed spell count
- 2-stage situation branch limit
- understanding EXP values
- chapter failure / retry / checkpoint
- chapter-to-chapter HP / deck persistence
- exact test themes / opponents
- 204 spell names / descriptions

## Prototype-only Simplifications

- `48-card Standard Test Deck`
- `Starting HP 10 — test value`
- chant abandon = current test-priority rule

## Out-of-Scope Systems

Project Source에서 기본 제작 범위 밖으로 명시:

- long-form main scenario
- 204 unique dedicated illustrations / VFX / animations
- mobile-first implementation

## Scope Guard Applied

```text
Full Product Feature
≠
Prototype Test Value
```

```text
Deferred Rule
≠
Current Structural Failure
```

---

# 3. Input Integrity

## INPUT_INTEGRITY_REPORT

### Active Source

`Magic_Word_Deckbuilding_Master_GDD_v0.9.md`

Document status:
`현재까지의 기획 확정안 통합본`

Priority rule:
이전 문서와 충돌하면 v0.9 우선.

### Locked / Current Rules

v0.9에서 최신 변경으로 명시된 주요 항목:

- chapter-start 3-spell Codex registration
- exploration does not recheck CurrentDeck at situation time
- 2C/3C Verb usable before understanding; unresolved effect tiers become `???`
- Lv4 = mastery, not 4C unlock
- Self + Clause allowed
- 204-spell Codex maintained

### Deprecated / Superseded Rules

v0.9에 의해 명시적으로 대체된 것:

- combat-first-completion auto-Codex registration emphasis
- low-understanding 2C/3C acquisition lock
- Lv4 = 4C unlock interpretation
- Self + Clause prohibition

이전 rule을 Active Review에 사용하지 않는다.

### Conflicts

`NONE FOUND at current Master-rule level`

### Important Unknowns

- run failure / reset / checkpoint semantics
- chapter persistence rules
- exact target selection for several effects
- exact mastery trait implementation

### Input Integrity Status

`CLEAR`

---

# 4. Project Mechanism Profile

## PROJECT_MECHANISM_PROFILE

### Core Player Fantasy

> 완성된 주문 카드를 쓰는 것이 아니라 마법 어휘를 모으고 이해하여, 상황과 상대를 읽고 직접 주문 문장을 만든다.

### Primary Player Verbs

- draw / hold cards
- select Direction
- place Target
- place Modifier
- place Verb
- commit Cost
- read opponent SpellLine
- alter current plan
- abandon incomplete spell
- build / refine deck
- register Codex spells
- choose exploration spell
- invest Understanding
- select Mastery

### Core Battle Grammar

```text
Direction
+
Target
+
Modifier
+
Verb
↓
Spell
```

Direction is free choice.

Actual deck cards:
- Target
- Modifier
- Verb

### Core Battle Loop

```text
Hand observation
↓
Own sentence plan
↓
Opponent SpellLine observation
↓
Place one or more words under Cost constraint
↓
Opponent progress changes
↓
Maintain / change / abandon plan
↓
Spell completes
↓
State changes
↓
Next sentence decision
```

### Chapter / Run Loop

```text
Deck
↓
Register 3 constructible spells
↓
Exploration / card acquisition / understanding
↓
Battle
↓
Refine
↓
Battle
↓
Final promotion battle
↓
Promotion
↓
Next chapter
```

### Active Mechanisms

- mandatory grammar-slot composition
- card availability
- hand retention
- multi-turn commitment
- public opponent spell construction
- directional targeting
- resource carry / residual mana
- cost manipulation
- deck refinement
- element-specific effects
- neutral grammar/cost manipulation
- Codex-based exploration response
- understanding-gated effect revelation
- mastery differentiation
- chapter/run growth

### Deferred Mechanisms

- final exact balance
- detailed Mastery traits
- complete run failure/reset
- exact retry/checkpoint semantics
- unresolved effect-selection details

### Context-only Mechanisms

- short exam narrative
- Steam-first UI target
- future mobile consideration

### Decision Types

- sentence composition
- target direction
- timing / commitment
- resource reserve
- deck composition
- card acquisition / removal
- exploration response
- knowledge / mastery investment
- build concentration vs breadth

### Persistent States — Battle

- Hand
- DrawPile
- Discard
- SpellLine
- HP
- shields / statuses
- RuntimeCostDelta
- PlacementCostOverride
- ResidualMana
- RefundedSpellCost
- NextSpellZeroCostState
- opponent public SpellLine

### Persistent States — Run / Meta

- current deck
- chapter
- HP
- understanding
- selected mastery
- Codex registration
- promotion record

### Main Resources

- card availability
- hand slots
- General Cost
- RefundedSpellCost
- ResidualMana
- HP
- deck slots / composition
- understanding investment
- Codex registration opportunity

### Failure Structure

Battle:
- HP 0 Hard Terminal
- deck exhaustion attrition / HP compare

Exploration:
- zero valid registered spell → automatic failure / damage

Run / chapter failure:
`UNKNOWN / DEFERRED`

### Recovery Structure

- spell abandonment
- deck refinement
- hand exchange / return / removal
- cost reserve
- future acquisition / understanding growth

### Information Structure

Player sees:
- own Hand
- own SpellLine
- opponent SpellLine
- Direction
- costs
- resources
- statuses
- `???` for unlearned effect tiers

Core information promise:

> opponent's incomplete spell should be important public information.

### Product-critical Dependencies

```text
Deck Composition
↓
Hand Availability
↓
Sentence Options
↓
Commitment
↓
Opponent Read
↓
Plan Change
↓
Spell Resolution
↓
Future Hand / Cost / State
```

and:

```text
Current Deck
↓
3-spell Registration
↓
Persistent Codex
↓
Exploration Options
↓
Understanding / Cards
↓
Future Deck / Battle
```

### Production-heavy Areas

- grammar validation
- effect resolution ordering
- cost-state interactions
- 204 spell definitions / labels / exploration tags
- five-element effect family
- neutral grammar manipulation
- opponent interaction
- tooltip / `???` state
- event logging
- regression across zones / overrides / terminal checks
- exploration rule/content authoring

---

# 5. Product Promise

## Promise A — Spell Construction

> **“주문을 외우지 않는다. 문장을 만든다.”**

Core promise:
Target / Modifier / Verb should create decisions that feel like constructing magic, not merely filling required UI slots.

## Promise B — Read and React

Project explicitly identifies:

> 상대가 공개된 어휘로 무엇을 완성하려는지 읽고 자신의 계획을 바꾸는 것

as one of two core fun pillars.

## Promise C — Contextual Build Identity

Final desired self-description is not:

> 어떤 카드를 모았는가?

but:

> 어떤 마법을 이해하고 어떤 주문 체계를 완성했는가?

This creates a strong build / mastery identity claim.

## Promise D — Deck / Exploration Coupling

Chapter-start registration connects:
- current deck
- Codex
- exploration response
- understanding / reward

## Promise E — Learn / Master Magic

Understanding and Mastery are intended as:
- knowledge
- capability
- specialization

not simple level numbers.

## Promise F — Run Adaptation

Across chapter exploration / battle / refinement:
- the deck changes
- understanding changes
- tests escalate

and the player should adapt rather than repeat a fixed solution.

---

# 6. Claim Registry

| Claim | Claim Type | Evidence State | Current Support | Status | Validation Needed | Suggested Evidence Type |
|---|---|---|---|---|---|---|
| Sentence assembly itself creates meaningful choices | DESIGN / EXPERIENCE | KNOWN | grammar, target/modifier/verb effects are specified | PARTIALLY SUPPORTED | YES | HUMAN TEST |
| Reading opponent SpellLine changes own plan | DESIGN / EXPERIENCE | KNOWN | opponent partial sentence is public and multi-turn spells exist | VALIDATION_REQUIRED | YES | HUMAN TEST |
| Context changes word/card value | DESIGN | KNOWN | Direction, Target, element, Modifier, opponent state alter outcome | STRUCTURALLY SUPPORTED | YES | HUMAN TEST |
| Deck construction produces recognizable build identity | DESIGN / EXPERIENCE | KNOWN | free ratios, elements, mastery, cost manipulation | PARTIALLY SUPPORTED | YES | HUMAN TEST |
| Availability uncertainty is manageable rather than pure grammar bricking | DESIGN / EXPERIENCE | KNOWN | hand retention, deck size choice, exchange/cost tools exist | PARTIALLY SUPPORTED | YES | HYBRID |
| Persistent Codex supports exploration without trivializing current-run decisions | DESIGN / EXPERIENCE | KNOWN | Codex persists and situations use registration rather than CurrentDeck | VALIDATION_REQUIRED | YES | HYBRID |
| Understanding/Mastery feels like learning magic, not only power gating | EXPERIENCE | KNOWN | partial effect reveal + Lv4 traits | VALIDATION_REQUIRED | YES | HUMAN TEST |
| Progression matches Build/Capability/Mastery promise | DESIGN | KNOWN | understanding changes effect resolution and mastery changes specialization | PARTIALLY SUPPORTED | YES | HUMAN TEST |
| Common grammar makes 204 spells producible without 204 independent systems | PRODUCTION | KNOWN | shared grammar/data and reused assets explicitly defined | STRUCTURALLY SUPPORTED | NO | NONE |
| 204-spell surface remains readable/testable | PRODUCTION / EXPERIENCE | KNOWN | common schema/logging exists, but content/tooltip burden remains | PARTIALLY SUPPORTED | YES | HYBRID |
| Run/reset structure supports roguelike replay motivation | DESIGN | UNKNOWN | run data exists but failure/retry/checkpoint rules remain unresolved | UNKNOWN | YES | SELF TEST |

## Enum Conformance Note

All canonical enum fields above use exactly one defined value.

Additional meaning is kept in prose rather than enum strings.

---

# 7. Universal Applicability

## UC-DESIGN-001 — Consequence Density over Input Count

**Applicability:** `YES`

Relevant Mechanism:
- Target
- Modifier
- Verb
- Direction

Question:

> 각 단어 선택이 실제 다른 consequence와 future decision을 만드는가, 아니면 완성 주문 하나를 세 카드로 분해한 절차인가?

---

## UC-DESIGN-002 — Contextual Value Shift

**Applicability:** `YES`

Relevant Mechanism:
- Self / Opponent
- Target
- element
- understanding
- opponent SpellLine
- chapter/exploration situation

Question:

> 같은 카드/어휘의 가치가 현재 Hand, opponent plan, build, encounter, exploration context에 따라 실제로 바뀌는가?

---

## UC-DESIGN-003 — Consequence-to-Next-Decision Coupling

**Applicability:** `YES`

Relevant Mechanism:

```text
Spell choice
→ Hand / Cost / State change
→ next sentence option

Deck / understanding choice
→ future chapter option
```

Question:

> 현재 주문 / 탐험 / 성장 선택이 다음 선택공간을 바꾸는가?

---

## UC-DESIGN-004 — Uncertainty Requires Response Agency

**Applicability:** `YES`

Relevant Mechanism:
- draw order
- mandatory card-type availability
- reward / exploration uncertainty
- opponent action sequence

Question:

> 원하는 문장을 즉시 만들 수 없을 때 player가 deck composition / hand retention / exchange / reserve / pivot로 대응할 수 있는가?

---

## UC-DESIGN-005 — Actionable Information

**Applicability:** `YES`

Relevant Mechanism:
- own Hand
- opponent SpellLine
- Cost states
- public effect text
- `???` understanding state

Question:

> 정보가 실제 planning / replanning으로 이어지고, 실패 원인을 이해할 수 있는가?

---

## UC-DESIGN-006 — Progression Should Match Its Intended Promise

**Applicability:** `CONDITIONAL`

### Knowledge Status

`CANDIDATE`

### Applicability Note

Progression is a real Product Promise.

Specifically:
- understanding
- mastery
- apprentice → high wizard progression
- deck/build formation

therefore UC006 is loaded as:

`CONDITIONAL DIAGNOSTIC`

not Universal Provisional.

Question:

> Understanding / Mastery가 Build / Capability / Strategic Expansion promise를 실제로 바꾸는가, 아니면 숫자·효과 해금만 누적하는가?

Vertical Power itself is not treated as a defect.

---

# 8. Genre Routing

## Mechanism Contribution Scores

| Genre | Core Loop | Player Verb | State | Decision | Product Promise | Total | Level | Runtime |
|---|---:|---:|---:|---:|---:|---:|---|---|
| Deckbuilding | 2 | 2 | 2 | 2 | 2 | **10** | **L3** | PRIMARY |
| Roguelike / Roguelite | 2 | 1 | 2 | 2 | 1 | **8** | **L2** | SECONDARY |
| Strategy | 1 | 2 | 2 | 2 | 1 | **8** | **L2** | SECONDARY |
| RPG | 0 | 0 | 1 | 1 | 2 | **4** | **L1** | SUPPORTING |
| Deduction / Information | 0 | 0 | 1 | 1 | 0 | **2** | L0 | NOT LOADED |
| Narrative | 0 | 0 | 0 | 0 | 1 | **1** | L0 | NOT LOADED |
| Management | 0 | 0 | 0 | 0 | 0 | **0** | L0 | NOT LOADED |
| Simulation | 0 | 0 | 0 | 0 | 0 | **0** | L0 | NOT LOADED |
| Action | 0 | 0 | 0 | 0 | 0 | **0** | L0 | NOT LOADED |

---

## Primary — Deckbuilding L3

Why:
- deck composition directly controls sentence availability
- acquisition/removal/refinement are loop elements
- hand/pool quality matters
- build identity is explicit product promise
- card value depends on context
- synergy and word relationships alter later options

This is not loaded because cards are visible in UI.

It is loaded because deck composition and availability are core decision machinery.

---

## Secondary — Roguelike / Roguelite L2

Why:
- current run data exists
- deck changes over chapter progression
- understanding/mastery are run-level growth
- exploration/reward/battle cycles repeat
- persistent Codex is meta-like progression

Why not L3:
- failure/retry/checkpoint/reset semantics remain unresolved
- exact run boundary is not fully locked

Therefore Roguelike mechanism is substantial but not yet fully canonicalized at project level.

---

## Secondary — Strategy L2

Why:
- multi-turn sentence commitment
- opponent public intent
- future option value
- reserve / residual mana
- plan change based on information
- hand/cost state affects future decisions

Not loaded merely because "card game = strategy".

---

## Supporting — RPG L1

Why:
- apprentice → high wizard framing
- element understanding
- mastery
- persistent capability formation

Why not L2/L3:
- no strong character-role / class / roleplay loop
- progression mainly supports Deck/Build/Mastery
- current RPG Evidence Base has limited breadth

Runtime treatment:
2 supporting questions only.

---

## Not Loaded

- Deduction: reading opponent intent is not evidence inference puzzle.
- Narrative: story is explicitly lightweight.
- Action: no execution-action core.
- Management / Simulation: no management-state or world simulation core.

## HYBRID_SCOPE_WARNING

`NO`

L3 1 + L2 2 is a meaningful hybrid but not a broad five-genre scope.

---

# 9. Genre Core Loading

## Deckbuilding — L3

### Active Provisional

- `GC-DECK-001 — Contextual Card Value`
- `GC-DECK-002 — Build Identity Formation`
- `GC-DECK-003 — Availability / RNG Control`
- `GC-DECK-004 — Synergy Must Change Decisions`
- `GC-DECK-005 — Pool Growth Needs Quality Control`

### Watch — Risk Signal Present

- `GC-DECK-006 — Reward Choice vs Future Consistency`
- `GC-DECK-007 — Build Pivotability`
- `GC-DECK-008 — Encounter Pressure`
- `GC-DECK-009 — Synergy Readability`
- `GC-DECK-010 — Build Formation Timing`
- `GC-DECK-012 — Vertical Power vs Decision Preservation`

### Not Activated

`GC-DECK-011 — Sequencing Value`

Reason:
Placement order is free and current Source does not yet establish sequencing itself as a major product promise.

---

## Roguelike — L2

### Active Provisional

- `GC-ROGUE-003 — Meaningful Run Variation Must Force Adaptation`
- `GC-ROGUE-004 — Run Choices Must Create Path Dependence`
- `GC-ROGUE-005 — Escalation Must Preserve Decisions`

### Conditional / Needs Info

- `GC-ROGUE-001 — Meta Progression Cannot Rescue a Weak Reset Loop`

Reason:
reset/failure loop is not fully specified.

### Watch

- `GC-ROGUE-010 — Meta Progression Type Must Match Product Promise`
- `GC-ROGUE-011 — Unlock Expansion Can Create Pool Dilution`

---

## Strategy — L2

### Active Provisional

- `GC-STRAT-001 — Key Decisions Change Future Option Value`
- `GC-STRAT-002 — State Changes Trigger Re-evaluation`
- `GC-STRAT-003 — Objectives Change Action Value`

### Watch

- `GC-STRAT-004 — Information Supports Prediction / Commitment`
- `GC-STRAT-007 — Recovery Decision after Error`
- `GC-STRAT-009 — Reserve / Flexibility`

---

## RPG — L1 Supporting

No Active RPG Core.

All current RPG entries are Candidates.

Supporting questions:

1. `GC-RPG-001`  
   Does Understanding / Mastery change available solutions, not just output magnitude?

2. `GC-RPG-003`  
   Does element mastery create persistent differentiation the player can recognize?

### RPG Evidence Boundary

Current RPG source has:
- no Provisional RPG Core
- limited direct evidence breadth

Therefore RPG Candidate questions cannot dominate the Project verdict unless Project evidence independently supports the risk.

---

# 10. Hybrid Resolver

## Deckbuilding × Roguelike

**Interaction Type:** `TYPE-A — Reinforcing`

Shared Verb:
- acquire
- remove
- refine
- specialize

Shared State:
- current deck
- understanding
- mastery
- Codex

Shared Consequence:
- future card value
- exploration options
- battle sentence availability

Risk:
persistent Codex can grow independently of current run deck and weaken run-specific adaptation.

---

## Deckbuilding × Strategy

**Interaction Type:** `TYPE-A — Reinforcing`

Shared Verb:
- commit a word
- reserve resource
- change plan
- abandon spell
- construct future sentence

Shared State:
- Hand
- SpellLine
- Cost
- opponent SpellLine

Shared Consequence:
- future option value
- opponent response window
- availability

Risk:
if sentence construction is mostly slot completion, Strategy layer collapses into execution of a preselected skill.

---

## Exploration × Deck

Not a separate Genre pair.

It is a cross-system relation inside Deck / Roguelike.

```text
Current Deck
↓
3-spell Registration
↓
Persistent Codex
↓
Exploration response
```

This coupling is reviewed as a Root Mechanism rather than inventing an "Exploration Genre".

---

## Deckbuilding × RPG-supporting Progression

**Interaction Type:** `TYPE-C — Conditional`

Understanding / Mastery strengthens Deck identity if:
- it changes future solution value
- supports specialization
- does not become a universal vertical tax

RPG remains L1 and does not create duplicate Severity.

---

# 11. Scale Routing

## Source Evidence

Current Master GDD does **not** state:

- team headcount
- sustained FTE
- external contractors
- AI-assisted production
- ownership lanes

## Scale Evidence State

`UNKNOWN`

## Canonical Scale Field

`NOT POPULATED`

Reason:

Canonical Runtime currently defines:

```text
SOLO
MICRO
SMALL
MID+
```

but no `UNKNOWN` Scale enum.

Correction RD-003 prohibits inventing a new enum value.

Therefore this Dry-run does **not** assign a Scale class.

## Runtime Consequence

- `SC-SOLO-*` not loaded
- `SC-MICRO-001` not loaded
- Small/Mid assumptions not made

Production Handoffs may still be used as genre-specific Production Risk Routing because they are not Scale Core and do not require a guessed team classification.

This exposes a new Minor Runtime schema gap, recorded in Defect Log #2.

---

# 12. Loaded Handoffs

## `SCALE_HANDOFF-DECK-001 — Interaction Regression Explosion`

**Loaded:** YES

Relevant Surface:

```text
Target
× Modifier
× Verb
× Direction
× Element
× Understanding
× Runtime Cost
× Status
× Opponent State
× Zone / Override
```

---

## `SCALE_HANDOFF-DECK-002 — Data Content Is Cheap Only Until Balance / Tooltip Cost Dominates`

**Loaded:** YES

Reason:
204 spells share grammar and assets, but still require:
- names
- descriptions
- tags
- tooltips
- effect QA
- discovery / Codex UI

---

## `SCALE_HANDOFF-DECK-003 — Familiar Rule Base as Cognitive Budget`

**Loaded:** YES

Reason:
Magic Word uses a novel grammar rather than familiar poker/card rank grammar.

Therefore UI / onboarding must carry more cognitive burden.

Handoff is used as a Production / UX risk route, not a Design Core.

---

## `SCALE_HANDOFF-ROGUE-001 — Run Content Matrix QA Explosion`

**Loaded:** YES — bounded

Reason:
8 exams × exploration situations × opponents × rewards × build states can multiply QA.

The exact run generator / node volume remains incomplete, so this Handoff is not expanded beyond the confirmed interaction surface.

---

## `SCALE_HANDOFF-ROGUE-003 — Unlock / Meta Content Cost`

**Loaded:** YES

Reason:
persistent Codex up to 204 + progression records + mastery content create:
- data
- UI
- balance
- tutorial/tooltip
- regression cost.

---

## Not Loaded

- procedural generation cost: no committed procedural generator
- Strategy map/pathfinding: no spatial map core
- RPG equipment/companion handoffs: not present
- multiplayer balance: PvE project

---

# 13. Reviewer Set

## Question Count Audit

```text
Universal:
6
(UC001~005 + UC006 conditional)

Deckbuilding:
10

Roguelike:
4

Strategy:
4

RPG Supporting:
2

Scale Core:
0

Handoff:
5

Hybrid:
3

Before Dedup:
34

After Dedup:
14

Reduction:
20
```

No numeric acceptance threshold is attached.

## Final Deduped Questions

### Q-01 — Sentence Construction Decision Density

Sources:
- UC001
- GC-DECK-004
- Deck × Strategy

> Target / Modifier / Verb 선택이 실제 다른 리스크·효과·후속 선택을 만드는가, 아니면 완성된 주문을 세 슬롯으로 나눈 것인가?

### Q-02 — Opponent Read → Plan Change

Sources:
- UC005
- GC-STRAT-004
- GC-STRAT-002

> 상대 SpellLine 공개정보 때문에 내 문장·Direction·Cost 사용·영창 유지 여부가 실제로 바뀌는가?

### Q-03 — Contextual Word Value

Sources:
- UC002
- GC-DECK-001

> 같은 Target / Modifier / Verb가 현재 build, opponent line, element understanding, resource state에 따라 실제 다른 가치가 되는가?

### Q-04 — Grammar Availability Agency

Sources:
- UC004
- GC-DECK-003
- GC-DECK-005

> 필수 카드종류가 손에 없을 때 deck 구성·hand retention·exchange·residual mana·pivot으로 대응할 수 있는가, 아니면 필수 비율 유지가 deckbuilding을 지배하는가?

### Q-05 — Build Identity

Sources:
- GC-DECK-002
- GC-DECK-007
- GC-RPG-003 supporting

> Run이 진행되며 특정 element / grammar / cost manipulation 중심의 build identity가 실제로 형성되는가?

### Q-06 — Codex / Current-run Coupling

Sources:
- UC002
- UC003
- GC-ROGUE-003
- GC-ROGUE-004

> persistent Codex가 쌓여도 현재 덱과 이번 run의 등록 선택이 exploration decision을 계속 바꾸는가?

### Q-07 — Reward / Pool Quality

Sources:
- GC-DECK-005
- GC-DECK-006

> 카드를 더 받는 것 외에 deck quality를 유지·정제하는 선택이 실제 가치가 있는가?

### Q-08 — Encounter Pressure

Sources:
- GC-DECK-008
- GC-STRAT-003

> Battle 1/2/3의 상대 성향이 서로 다른 card / sentence / build 질문을 만드는가?

### Q-09 — Understanding / Mastery Promise

Sources:
- UC006 CANDIDATE
- GC-RPG-001 supporting
- GC-DECK-012 related

> Understanding / Mastery가 단순 vertical power가 아니라 solution / build / role value를 바꾸는가?

### Q-10 — Unknown Effects / Synergy Readability

Sources:
- UC005
- GC-DECK-009

> `???`, runtime cost, zero-cost states, statuses가 늘어도 player가 왜 주문이 강하거나 약한지 이해할 수 있는가?

### Q-11 — Replanning / Commitment

Sources:
- UC003
- GC-STRAT-001
- GC-STRAT-007

> multi-turn spell commitment 후 상대 공개정보나 draw 변화가 계획 변경 / 유지 / 파기라는 실제 선택을 만드는가?

### Q-12 — Run Escalation / Adaptation

Sources:
- GC-ROGUE-003
- GC-ROGUE-005

> 8단계 진행이 숫자 상승이 아니라 build weakness와 decision을 다시 시험하는가?

### Q-13 — Interaction Regression

Sources:
- DECK-001
- ROGUE-001

> grammar / cost / status / understanding / neutral effects 조합의 regression surface가 현재 common rule architecture로 통제 가능한가?

### Q-14 — Data / Tooltip / Codex Production Surface

Sources:
- DECK-002
- DECK-003
- ROGUE-003

> 204조합을 공통 시스템으로 만들더라도 naming / tag / tooltip / Codex / understanding presentation 비용이 독립적으로 폭증하지 않는가?

---

# 14. Raw Finding Summary

```text
Raw Findings:
18
```

Major raw signals:

1. sentence grammar is structurally distinct but subjective decision value unvalidated.
2. mandatory Target/Modifier/Verb can create availability tax.
3. 30~40 free deck composition can amplify grammar starvation.
4. persistent hand and residual mana provide partial availability response.
5. opponent SpellLine is public but plan-change value unvalidated.
6. multi-turn strong spell rule creates telegraph opportunity.
7. 3C total low-tier sentence can resolve in one turn, reducing react window for weak spells.
8. context strongly changes card effects through Direction/Target/element.
9. understanding changes actual effect tier.
10. mastery aims at build identity but detailed traits are deferred.
11. persistent Codex grows beyond current run deck.
12. exploration does not recheck CurrentDeck.
13. zero valid exploration choice causes automatic damage.
14. future situation visibility is not fully specified.
15. run reset/retry semantics are unresolved.
16. 204 spells reuse common grammar/assets.
17. effect / cost / zone / terminal interactions create large regression surface.
18. Codex names/tags/tooltips create authored-data workload despite shared mechanics.

---

# 15. Root Merge / Split

## Root A — Sentence Assembly Decision Space

Merged:
- UC001
- Deck synergy-decision
- Deck × Strategy composition

Not merged with availability.

Reason:
- "Are assembled words meaningful choices?"
and
- "Can the needed word types be accessed?"
have different Root / Fix / validation.

---

## Root B — Opponent Read / Replanning

Merged:
- UC005 decision-time
- Strategy information/commitment
- state-triggered reevaluation

Not merged with sentence assembly because public-information response is a distinct promise.

---

## Root C — Persistent Codex / Run Coupling

Merged:
- UC002 contextual value
- UC003 future decision coupling
- Rogue variation/path dependence

Not merged with progression meaning.

Reason:
Codex accumulation affects exploration/run adaptation.
Understanding/Mastery affects character/build growth.

---

## Root D — Grammar Availability

Merged:
- UC004
- Deck availability
- pool quality
- hand state

Not merged with build identity.

Reason:
Availability can be unhealthy even if the final build is recognizable.

---

## Root E — Understanding / Mastery Promise

Merged:
- UC006 candidate
- Deck build identity related
- RPG supporting candidate

No duplicate Severity from RPG.

---

## Root F — Combinatorial Production Surface

Merged:
- DECK-001 regression
- DECK-002 tooltip/data
- ROGUE-001/003 relevant surfaces

Within the final RF, two Production Drivers are retained:
1. logic/regression
2. authored/UI data

They remain one Root because the current mitigation architecture is the same:
common grammar + shared data + explicit event/state model + reuse.

If later authoring and logic pipelines diverge, they may split in production review.

---

## Duplicate Audit

```text
Duplicate RF:
0
```

## Over-Merge Audit

```text
Over-merged RF:
0
```

No current pair shares different fixes/validation strongly enough to require further split.

---

# 16. Critical / High Findings

## RF-MW-001 — Sentence Assembly Must Be More Than Slot Completion

**Status:** `VALIDATION_REQUIRED`  
**Category:** `DESIGN`  
**Severity:** `HIGH`  
**Project Evidence Strength:** `PARTIAL`  
**Knowledge Status:** `MULTI-SOURCE`  
**Knowledge Confidence:** `HIGH`

### Confidence Note

Parent cluster contains `UC001` and high-confidence Deck rules.

### Affected Promise

> 주문을 외우지 않는다. 문장을 만든다.

### Evidence

The grammar is real:
- Direction
- Target
- Modifier
- Verb
- costs and element effects differ

But structural variety does not prove that assembly itself feels like choosing a spell sentence.

### Root Mechanism

```text
If component choice
only reconstructs
an already-obvious desired spell
↓
grammar becomes procedural UI

If each component
changes risk / timing / future option
↓
sentence construction becomes decision
```

### Recommended Action

Do not add new word types first.

Use the existing:
- Direction
- 3 Targets
- 3 Modifiers
- current Verb set
- Cost / SpellLine

to determine whether assembly creates distinct decisions.

### Action Class

`VALIDATE FIRST`

### Validation Need

`VALIDATION_REQUIRED`

### Suggested Evidence Type

`HUMAN TEST`

### Claim

Sentence assembly itself produces meaningful decision tension rather than mandatory slot filling.

---

## RF-MW-002 — Opponent SpellLine Must Actually Change the Player's Plan

**Status:** `VALIDATION_REQUIRED`  
**Category:** `DESIGN`  
**Severity:** `HIGH`  
**Project Evidence Strength:** `PARTIAL`  
**Knowledge Status:** `MULTI-SOURCE`  
**Knowledge Confidence:** `HIGH`

### Affected Promise

Second explicit core-fun pillar:

> 상대가 무엇을 완성하려는지 읽고 자신의 계획을 바꾼다.

### Evidence

Strong spells can require multi-turn commitment.
Opponent SpellLine is public.
Direction is always visible.

But:
- low-cost sentences may complete in one turn
- public information may be obvious but irrelevant
- player may simply continue own optimal line

### Root Mechanism

```text
Information visible
≠
Information changes commitment
```

### Recommended Action

Preserve open SpellLine.

Do not increase hidden information first.

The core question is whether current public state produces:
- change plan
- continue plan
- abandon
- counter
- reserve

decisions.

### Action Class

`VALIDATE FIRST`

### Validation Need

`VALIDATION_REQUIRED`

### Suggested Evidence Type

`HUMAN TEST`

---

## RF-MW-003 — Persistent Codex Can Decouple Exploration from the Current Run

**Status:** `VALIDATION_REQUIRED`  
**Category:** `DESIGN`  
**Severity:** `HIGH`  
**Project Evidence Strength:** `CONFIRMED`  
**Knowledge Status:** `MULTI-SOURCE`  
**Knowledge Confidence:** `HIGH`

### Affected Promise

- Deck / Exploration Coupling
- Run Adaptation
- Mastery / knowledge progression

### Confirmed Structure

```text
Current Deck
→ register 3 constructible spells

Later Situation
→ CurrentDeck not checked

Persistent Codex
→ all registered spells can be candidates
```

### Root Mechanism

As Codex breadth increases:

```text
Current Run Deck
may matter less
for Exploration Option Space
```

This does not prove the system fails.

It proves that current-run coupling is progressively weakened by design.

### Why It Matters

The GDD wants both:
- long-term magical knowledge
- current run deckbuilding relevance

These promises can compete.

### Recommended Action

Do not add additional exploration layers first.

Evaluate whether:
- three new registrations
- situation tags
- element relation
- modifier hierarchy

keep current-run choices relevant as Codex grows.

### Action Class

`VALIDATE FIRST`

### Validation Need

`VALIDATION_REQUIRED`

### Suggested Evidence Type

`HYBRID`

### Do Not Infer

Persistent knowledge is not automatically bad meta progression.

The risk is only:
> current-run decisions stop changing exploration value.

---

## RF-MW-006 — Common Grammar Reduces Asset Cost but Not Regression / UI Surface

**Status:** `ACCEPTED_RISK`  
**Category:** `PRODUCTION`  
**Severity:** `HIGH`  
**Project Evidence Strength:** `CONFIRMED`  
**Knowledge Status:** `MULTI-SOURCE`  
**Knowledge Confidence:** `HIGH`

### Confirmed Surface

```text
204 Spell combinations
+
5 Element effect families
+
Neutral grammar manipulation
+
Understanding levels
+
Cost override states
+
SpellLine
+
Statuses
+
Zone movement
+
Terminal checks
+
Exploration tags
```

### Relevant Handoffs

- DECK-001
- DECK-002
- DECK-003
- ROGUE-001
- ROGUE-003

### Current Mitigation

- common grammar
- shared CardDefinition / SpellDefinition
- explicit resolver order
- CombatEvent logging
- no 204 unique art/VFX
- data reuse

### Mitigation State

`CURRENTLY_MITIGATED`

### Why It Matters

`204 spells` are not 204 independent mechanics.

But the project still owns:
- tooltip correctness
- tag correctness
- UI states
- effect interaction
- regression
- naming/description content

### Recommended Action

Protect the current common grammar / data-driven architecture.

Do not create per-spell special-case logic unless a proven rule gap requires it.

### Action Class

`NO ACTION YET`

### Validation Need

`NONE`

### Scale Note

Team scale is UNKNOWN, so this Dry-run does not convert this Production Surface into a solo/small-team feasibility verdict.

---

# 17. Medium Findings

## RF-MW-004 — Mandatory Grammar Types Can Become a Deck Ratio Tax

**Status:** `VALIDATION_REQUIRED`  
**Category:** `DESIGN`  
**Severity:** `MEDIUM`  
**Project Evidence Strength:** `PARTIAL`  
**Knowledge Status:** `MULTI-SOURCE`  
**Knowledge Confidence:** `HIGH`

### Structure

Every normal spell requires:
- Target
- Modifier
- Verb

Actual deck ratios are free.

Hand:
- start 5
- draw 1
- retain at turn end
- max 10

### Risk

If successful decks are forced toward narrow type ratios primarily to avoid unplayable hands, then:

> build freedom may collapse into grammar maintenance.

### Existing Response Agency

- deck size choice
- hand retention
- water hand manipulation
- return/remove effects
- residual mana draw

Therefore this is not a confirmed structural failure.

### Recommended Action

Do not add guaranteed wildcards or new cycling system before evidence.

First determine whether current availability tools create a meaningful consistency tradeoff.

### Action Class

`VALIDATE FIRST`

### Validation Need

`VALIDATION_REQUIRED`

### Suggested Evidence Type

`HYBRID`

---

## RF-MW-005 — Understanding / Mastery Must Feel Like Learning a Magic System

**Status:** `VALIDATION_REQUIRED`  
**Category:** `DESIGN`  
**Severity:** `MEDIUM`  
**Project Evidence Strength:** `PARTIAL`  
**Knowledge Status:** `CANDIDATE`  
**Knowledge Confidence:** `MEDIUM-HIGH`

### Status Note

Primary Universal trace:
`UC006 — CANDIDATE`

RPG supporting evidence is not promoted into a separate finding.

### Product Promise

> 어떤 마법을 이해하고 어떤 주문 체계를 완성했는가?

### Current Support

- high-cost cards can be acquired early
- hidden higher-tier effects remain `???`
- actual effect tier uses understanding
- Lv4 grants specialization trait
- max two mastered elements per run

This is stronger than simple level-number progression.

### Remaining Risk

If the main experience becomes:

> same spell, larger effect after EXP

then the "understanding" fantasy may reduce to vertical power.

### Recommended Action

Do not add more progression currencies.

Use current:
- partial effect revelation
- mastery choice
- two-element cap

to test whether growth changes build/solution identity.

### Action Class

`VALIDATE FIRST`

### Validation Need

`VALIDATION_REQUIRED`

### Suggested Evidence Type

`HUMAN TEST`

---

# 18. Needs Info

## NI-MW-001 — Run Failure / Reset Boundary

### Known

- current run data exists
- eight promotion stages
- persistent Codex direction
- chapter loop exists

### Unknown

- failure/retry
- checkpoint
- run restart
- chapter persistence
- HP/deck persistence across chapter

### Blocked Judgment

- full Roguelike L3 routing
- `GC-ROGUE-001`
- restart motivation
- meta/core relation

### Treatment

`UNKNOWN ≠ FAIL`

---

## NI-MW-002 — Exploration Foresight Before Zero-choice Failure

### Known

- zero valid spell → automatic failure / damage
- information / observation node is only a candidate

### Unknown

How much the player knows about:
- upcoming situation tags
- element
- modifier requirement
- route consequences

before chapter registration / node choice.

### Blocked Judgment

Whether zero-choice exploration failure is:
- fair commitment consequence
or
- unresponsive hidden punishment.

### Related Parent

`UC004`

No RF is created until foresight structure is clearer.

---

## NI-MW-003 — Team / Scale

### Known

No team-size statement in current Master GDD.

### Unknown

- headcount
- sustained FTE
- contractor support
- AI assistance
- ownership lanes

### Blocked Judgment

Scale Core applicability and team-relative production feasibility.

---

# 19. Validation Required

Detailed Validation Plan is not created.

## V-MW-001

```text
Claim:
Sentence assembly creates meaningful decisions rather than slot completion.

Suggested Evidence Type:
HUMAN TEST
```

## V-MW-002

```text
Claim:
Opponent SpellLine information changes the player's current plan.

Suggested Evidence Type:
HUMAN TEST
```

## V-MW-003

```text
Claim:
Persistent Codex growth does not erase current-run exploration relevance.

Suggested Evidence Type:
HYBRID
```

## V-MW-004

```text
Claim:
Mandatory grammar types create consistency tension without becoming a rigid deck ratio tax.

Suggested Evidence Type:
HYBRID
```

## V-MW-005

```text
Claim:
Understanding and Mastery create a recognizable magic-system identity.

Suggested Evidence Type:
HUMAN TEST
```

## V-MW-006

```text
Claim:
Run escalation and opponent variety force adaptation rather than only higher numbers.

Suggested Evidence Type:
HUMAN TEST
```

Detailed criteria / run counts / persona / threshold:

`DEFERRED`

---

# 20. Supported Structures

## SS-MW-001 — Clear Grammar Boundary

### Structure

```text
Direction = free decision
Cards = Target + Modifier + Verb
```

### Supported By

- UC001
- Deck contextual-value structure

### Why It Works

The project separates sentence grammar roles instead of making every card a complete skill.

### Product Promise Protected

Spell construction.

### Do Not Accidentally Remove

Do not solve availability issues by turning every card into a standalone spell unless core tests reject the grammar.

### Validation Still Needed

`YES`

---

## SS-MW-002 — Public Opponent SpellLine

### Structure

Opponent incomplete spell is public information.

### Supported By

- UC005
- Strategy information/commitment

### Why It Works

Strong spells becoming readable creates a direct path from:
information → counterplanning.

### Product Promise Protected

Read / react.

### Do Not Accidentally Remove

Do not default to hidden opponent intent to create difficulty.

### Validation Still Needed

`YES`

---

## SS-MW-003 — Acquisition Is Not Hard-gated by Understanding

### Structure

2C/3C cards can be acquired and used before full understanding.

Only advanced effect tiers remain `???` / inactive.

### Supported By

- UC006 candidate boundary
- Deck build flexibility

### Why It Works

It avoids a hard progression gate where interesting cards are unavailable until a level threshold.

### Product Promise Protected

Discovery → learning → mastery.

### Do Not Accidentally Remove

Do not convert understanding into simple card-tier permission unless testing shows necessity.

### Validation Still Needed

`YES`

---

## SS-MW-004 — Combat and Exploration Element Rules Are Separated

### Structure

Exploration elemental cycle does not modify combat damage.

### Why It Works

Prevents one element relation table from dominating two different systems.

### Product Promise Protected

Combat build diversity + exploration readability.

### Do Not Accidentally Remove

Do not import exploration weaknesses into combat for thematic consistency alone.

### Validation Still Needed

`NO`

---

## SS-MW-005 — Common Grammar Instead of 204 Independent Systems

### Structure

204 spells are generated from shared grammar and shared effect families.

Unique assets are explicitly not required per spell.

### Supported By

- DECK-002
- production reuse principle

### Why It Works

Content identity can grow without requiring 204 unique implementation lanes.

### Do Not Accidentally Remove

Avoid per-spell exception logic that breaks shared grammar.

### Validation Still Needed

`NO`

---

## SS-MW-006 — Explicit State / Resolution Ordering

### Structure

- PlaceCard order
- terminal checks
- cost source order
- CombatEvent logging

are explicitly separated.

### Why It Works

Reduces ambiguity in a system with:
- refunds
- zero-cost overrides
- pending decisions
- terminal interruption

### Product Promise Protected

Reliable strategic rules.

### Do Not Accidentally Remove

Do not hide special-case state changes outside the central resolver/event model.

### Validation Still Needed

`NO`

---

# 21. Evidence Boundary

1. No playable test results are supplied.
2. No player behavior data is supplied.
3. No AI Tester output is generated.
4. Scale is unresolved from the Project Source.
5. Roguelike reset/failure boundary is incomplete.
6. RPG is supporting only; all RPG Core entries remain Candidate.
7. UC006 remains Candidate and is only a Conditional Diagnostic.
8. Exact mastery traits / many effect details are deferred and not treated as current violations.
9. Market / Award goals are not specified; PASS 9 = `N/A`.
10. Steam PC is a platform direction, not a market-success claim.

---

# 22. Enum Conformance Result

## ENUM_CONFORMANCE_CHECK

```text
Evidence State:
PASS

Claim Status:
PASS

Validation Needed:
PASS

Applicability:
PASS

Knowledge Status:
PASS

Knowledge Confidence:
PASS

Project Evidence Strength:
PASS

Issue Severity:
PASS

RF Status:
PASS

Action Class:
PASS

Validation Need:
PASS

Suggested Evidence Type:
PASS

Reviewer Verdict:
PASS
```

### Scale Schema Note

Canonical Scale classification field was not populated because Project evidence is UNKNOWN and the existing enum has no UNKNOWN value.

This is recorded as a new Runtime defect rather than inventing a value.

### RD-003 Regression

`NO`

No canonical enum field was modified by adding explanatory text.

---

# 23. Reviewer Verdict

## Qualitative Precedence Guard

### Step A — Blocking Unknown?

`NO`

Run reset / scale are unknown, but core battle / deck / exploration structure is still reviewable.

### Step B — Confirmed Critical or multiple unmitigated High Structural Roots?

`NO`

### Step C — HIGH + STRUCTURAL FIX FIRST before next stage?

`NO`

High Project risks are primarily:
`VALIDATE FIRST`

Production High is currently recognized and mitigated by common grammar / state architecture.

### Step D — Main remaining uncertainty is VALIDATE FIRST?

`YES`

## Project Reviewer Verdict

`REVIEW_CLEAR_WITH_VALIDATION`

### Reason

The project has a coherent and differentiated structural core:

```text
Deck
→ words
→ sentence
→ public opponent intent
→ commitment / replanning
→ understanding / mastery
```

No confirmed Structural Root currently requires design revision before testing.

However the product's core promises remain experience-dependent:

- sentence assembly decision depth
- read/react behavior
- grammar availability
- Codex/run coupling
- mastery identity

Therefore validation is materially required.

This is not a Project investment / kill decision.

---

# 24. Source Trace

## Project Source

`Magic_Word_Deckbuilding_Master_GDD_v0.9.md`

## Runtime

`REVIEWER_RUNTIME_SPECIFICATION_v0.1_APPROVED.md`

## Applied Correction

`REVIEWER_RUNTIME_CORRECTION_NOTE_01_v0.1.md`

## Canonical

- `Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`
- `GENRE_CORE_MASTER_INDEX_v0.3.md`
- `SCALE_CORE_BASELINE_v0.2.md`

## Loaded Genre

- `DECKBUILDING_CORE_CANDIDATES_v0.1.md`
- `ROGUELIKE_CORE_CANDIDATES_v0.1.md`
- `STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md`
- `RPG_CORE_CANDIDATES_v0.1_APPROVED.md` — L1 supporting only

## Audit Snapshot

```text
Review Target:
FULL PROJECT

Universal:
UC001~005 YES
UC006 CONDITIONAL

Genre:
Deckbuilding L3
Roguelike L2
Strategy L2
RPG L1

Scale:
UNRESOLVED FROM SOURCE

Questions:
34 → 14

Raw Findings:
18

Root Issues:
6

Final RF:
6

Duplicate RF:
0

Over-merged RF:
0

RD-001 Regression:
NO

RD-002 Regression:
NO

RD-003 Regression:
NO

Validation Planner:
NOT INVOKED
```
