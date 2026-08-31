# GENRE_CORE_MASTER_INDEX_v0.2

**Studio OS — Genre Core Master Index & Routing Integration**  
**Document:** `GENRE_CORE_MASTER_INDEX_v0.2`  
**Status:** `INTEGRATION_BASELINE`  
**Genre Baselines:** `9 Approved`  
**Purpose:** `Genre Core Routing / Deduplication / Reviewer Loading / Validation Routing / Scale Handoff Registry`  
**Canonical Source:** `Individual Approved Genre Core Documents`  
**GSC Sync:** `Active Independent GSC 0 / Retired Historical GSC 3 / Routing Specialization 2`  
**Completed:** `Scale Core Consolidation / Genre × Scale Integration / Canonical GSC Consolidation`  
**Next:** `Universal Core Consolidation`  
**Pending:** `Project Routing Validation / Universal Core Consolidation / Reviewer Runtime`

> 이 문서는 **Genre Knowledge를 저장하는 문서가 아니라 Genre Knowledge를 올바르게 호출하는 Router**다.  
> Canonical Rule, Core Status, Confidence, Boundary는 각 승인 Genre 문서가 소유한다.  
> 이 Index는 새 `GC-*`를 생성하거나 기존 Core를 승격·강등·재작성하지 않는다.


---

# 1. Executive Summary

현재 Studio OS에는 9개의 승인 Genre Core Candidate Baseline이 있다.

```text
Approved Genre Baselines: 9
Provisional Genre Cores: 28
Standard Candidates: 65
Formal Merge / Reclass entries in Promotion Tables: 6
Scale Handoffs: 51
RPG Provisional: NONE
Action Provisional: NONE
```

Router의 핵심 원칙:

1. **Genre Label보다 Mechanism을 먼저 판정한다.**
2. **Primary Genre는 기본 1~2개로 제한한다.**
3. **Universal Parent를 먼저 적용하고 Genre Specialization은 같은 Issue 아래 묶는다.**
4. **Candidate Evidence Confidence와 Project Issue Severity를 분리한다.**
5. **Genre Count를 Hybrid Quality 또는 Depth로 점수화하지 않는다.**

기본 실행 흐름:

```text
Project Concept
↓
Player Verbs / Core Loop / Persistent State
↓
Decision / Execution / Progression / Content Structure
↓
Genre Contribution Analysis
↓
Genre Routing Profile
↓
Universal Core Load
↓
Primary / Secondary Genre Load
↓
Cross-Genre Deduplication
↓
Scale Routing Profile
↓
Relevant Scale Core
↓
Active Scale Handoff
↓
Optional GSC Registry Check
↓
Routing Specialization Hint
↓
Dynamic PROJECT_REVIEWER_SET
↓
Project Review
```


---

# 2. Master Index Purpose

책임 범위:

- **Master Registry** — 승인 Genre 상태와 Trace를 한 곳에서 확인.
- **Genre Routing Layer** — 어떤 프로젝트에 어떤 Genre 문서를 어느 강도로 로드할지 결정.
- **Hybrid Genre Resolver** — Shared Mechanism과 Parallel System을 구분.
- **Reviewer Loading Rule** — Provisional / Candidate를 서로 다른 강도로 호출.
- **Cross-Genre Deduplication Map** — Universal / Genre 중복 Issue의 Double Penalty 방지.
- **Validation Routing Map** — Genre별 Machine / Human 검증 강점을 연결.

하지 않는 것:

- 새 `GC-*` 생성
- 기존 Core 승격 / 강등
- Canonical Rule 재작성
- Store Tag만으로 Genre 판정
- Hybrid에 모든 Genre Rule 로드
- Genre × Scale Core 신규 생성
- Validation Criteria / Threshold 확정


---

# 3. Canonical Source Hierarchy

```text
Level 1 — Universal Canonical Source
STUDIO_CORE_CANDIDATES_v0.3 (`Studio_OS_Evidence_Based_Core_Extraction_v0.3.md`)

Level 2 — Genre Canonical Sources
9 Approved Genre Core Candidate Baselines

Level 3 — Router
GENRE_CORE_MASTER_INDEX_v0.2

Level 4 — Project Runtime
PROJECT_GENRE_ROUTING_PROFILE
PROJECT_REVIEWER_SET

Level 5 — Review Output
RF-* Reviewer Findings
Validation Handoff
```

Core 문구 / Status가 충돌하면:

```text
Master Entry
↓
Canonical Genre Document
↓
Core / Promotion Section
↓
Source Trace
```

순서로 내려간다.


---

# 4. Approved Genre Baseline Registry

| Genre | Provisional | Candidate | Merge / Reclass* | Evidence Strength | Boundary |
| --- | --- | --- | --- | --- | --- |
| Deckbuilding | 5 | 7 | 0 | VERY HIGH / HIGH within deckbuilding | PvP/CCG/live-service balance and economy without additional evidence |
| Management | 8 | 7 | 1 | VERY HIGH / broad | Simulation/strategy merely because resources exist |
| Roguelike / Roguelite | 4 | 9 | 0 | VERY HIGH / HIGH | Any randomized or permadeath game without reset/mastery structure |
| Deduction / Information | 3 | 7 | 2 | HIGH; primary evidence concentrated | Mystery theme or information processing without player-owned inference |
| Narrative / Systemic Narrative | 3 | 6 | 2 | HIGH | Linear/authored narrative where state reactivity is not the promise |
| Strategy | 3 | 8 | 0 | HIGH within bounded scope | Macro/multiplayer strategy before additional evidence |
| Simulation | 2 | 6 | 1 | HIGH within bounded scope | Realism-heavy simulation subtypes before additional evidence |
| RPG | 0 | 8 | 0 | LOW-MEDIUM breadth; no provisional genre core | RPG-wide class/build/quest rules before additional evidence |
| Action | 0 | 7 | 0 | MEDIUM breadth; no provisional genre core | Action subtypes outside current evidence boundary |

`Merge / Reclass*`는 Promotion Table에서 일반 Candidate와 분리된 상태만 센다. Header의 Universal Strengthening 관계는 별도 Registry에서 관리한다.

| Genre | Canonical Document |
| --- | --- |
| Deckbuilding | `DECKBUILDING_CORE_CANDIDATES_v0.1` |
| Management | `MANAGEMENT_CORE_CANDIDATES_v0.1` |
| Roguelike / Roguelite | `ROGUELIKE_CORE_CANDIDATES_v0.1` |
| Deduction / Information | `DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1` |
| Narrative / Systemic Narrative | `NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1` |
| Strategy | `STRATEGY_CORE_CANDIDATES_v0.1` |
| Simulation | `SIMULATION_CORE_CANDIDATES_v0.1` |
| RPG | `RPG_CORE_CANDIDATES_v0.1` |
| Action | `ACTION_CORE_CANDIDATES_v0.1` |


---

# 5. Genre Mechanism Definitions

| Genre | Mechanism Test |
| --- | --- |
| Deckbuilding | Card Pool · Draw/Availability · Build Formation · Synergy · Contextual Card Value |
| Management | State Diagnosis · Priority Conflict · Limited Capacity Allocation · Reprioritization |
| Roguelike / Roguelite | Run Reset · Run Variation · Path Dependence · Repeated Mastery |
| Deduction / Information | Evidence · Relation · Hypothesis · Player-owned Inference |
| Narrative / Systemic Narrative | Player History · Persistent Narrative State · Consequence · Recontextualization |
| Strategy | State Reading · Future Consequence · Commitment · Planning · Re-evaluation |
| Simulation | Persistent State · Rule · Causal Dependency · Cross-system Interaction · Autonomous Transition |
| RPG | Persistent Character Formation · Capability · Role · Build · Character Identity |
| Action | Timing-sensitive Input · Direct Control · Immediate Response · Threat/Feedback · Adjustment |

### Routing Guardrail

```text
Theme / Store Tag
≠
Genre Mechanism
```

- Mystery theme만으로 Deduction을 L2/L3로 올리지 않는다.
- Resource meter만으로 Management/Simulation을 로드하지 않는다.
- Level/Stat만으로 RPG를 로드하지 않는다.
- Real-time combat tag만으로 Action Candidate 전체를 로드하지 않는다.


---

# 6. Genre Contribution Levels

| Level | Meaning | Loading Behavior |
| --- | --- | --- |
| L0 — Not Applicable | 실질 Mechanism 없음 | Genre Core 미로드. 관련 Core는 `N/A`. |
| L1 — Supporting | Feature / Moment 수준 | 필요한 Reviewer Question / Candidate만 선택 참조. |
| L2 — Secondary Genre | 반복 Core Loop를 보조 | Provisional 우선. Candidate는 Risk Signal 시 선택. |
| L3 — Primary Genre | Core Loop / Fantasy / Product Promise 중심 | Provisional + High-confidence Candidate + Default Questions 적극 적용. |

기본 권장:

```text
Primary Genre: 1~2
Secondary Genre: 0~3
```


---

# 7. Genre Routing Score

| Axis | 0 | 1 | 2 |
| --- | --- | --- | --- |
| Core Loop Dependency | 없음 | 보조 | 없으면 게임이 다른 게임이 됨 |
| Player Verb Dependency | 관련 Verb 없음 | 가끔 사용 | 반복 핵심 Verb |
| State Dependency | 관련 State 없음 | 일부 존재 | 장기/반복 핵심 State |
| Decision Dependency | 관련 판단 없음 | 보조 판단 | 주요 판단 |
| Product Promise Dependency | 무관 | 보조 Fantasy | 핵심 구매 이유 |

```text
0~2  → L0
3~5  → L1
6~8  → L2
9~10 → L3
```

점수는 Routing Aid다. 모든 L2/L3는 다음 설명을 필수로 기록한다.

```text
Why Loaded:
Which Player Verb:
Which State:
Which Core Loop:
Which Product Promise:
```


---

# 8. Genre Routing Profile Schema

```text
PROJECT_GENRE_ROUTING_PROFILE

Project:
Version:

Primary:
- Genre A — L3 — Score __/10
  Why Loaded:
  Player Verb:
  State:
  Core Loop:
  Product Promise:

Secondary:
- Genre B — L2 — Score __/10
  ...

Supporting:
- Genre C — L1
  Selective Questions:

Not Loaded:
- Genre D — L0

Hybrid Interaction:
- Genre A × Genre B — TYPE-?
  Shared Verb:
  Shared State:
  Shared Consequence:

Evidence Boundary:
- ...

HYBRID_SCOPE_WARNING:
YES / NO
```

`L0`는 `PASS`가 아니라 Applicability 없음이므로 `N/A`다.


---

# 9. Hybrid Genre Resolver

Hybrid는 단순 합산하지 않는다.

## Shared Player Verb

같은 반복 Verb가 두 Genre를 동시에 진행하는가?

## Shared State

하나의 Persistent State가 두 Genre의 판단 / 결과에서 실제 소비되는가?

## Shared Consequence

한 Genre의 결과가 다른 Genre의 다음 판단을 바꾸는가?

## Parallel Systems

```text
Combat
→ End
→ Dialogue
→ End
→ Management
```

처럼 State / Consequence 공유가 적으면 각 Phase를 독립 검토한다.

```text
Genre Count
≠
Genre Integration Quality

Many Systems
≠
Hybrid Depth
```


---

# 10. Genre Interaction Types

| Type | Meaning | Reviewer Use |
| --- | --- | --- |
| TYPE-A — Reinforcing | 같은 Decision / State를 함께 강화 | 질문 병합 우선 |
| TYPE-B — Sequential | 서로 다른 Phase에서 순차 작동 | 각 Phase 품질 + 전환 비용 |
| TYPE-C — Conditional | 특정 State에서만 다른 Genre 활성 | Trigger / coverage |
| TYPE-D — Competing | 한 Genre 요구가 다른 Genre 경험을 약화 | Hybrid Conflict 검토 |
| TYPE-E — Cosmetic Association | Theme/UI만 공유 | Genre Weight 낮춤 |


---

# 11. Cross-Genre Deduplication Registry

## Universal Parent Registry

| ID | Status | Confidence | Router Role |
| --- | --- | --- | --- |
| `UC-DESIGN-001` — Consequence Density over Input Count | PROVISIONAL | VERY HIGH | Input/feature count vs actual consequence density Parent |
| `UC-DESIGN-002` — Contextual Value Shift | PROVISIONAL | HIGH | Context-dependent value / recontextualization Parent |
| `UC-DESIGN-003` — Consequence-to-Next-Decision Coupling | PROVISIONAL | HIGH | Persistent consequence / next decision Parent |
| `UC-DESIGN-004` — Uncertainty Requires Response Agency | PROVISIONAL | HIGH | RNG / hidden threat / reserve / recovery Parent |
| `UC-DESIGN-005` — Actionable Information | PROVISIONAL | HIGH | Diagnosis / prediction / threat-readability Parent |
| `UC-DESIGN-006` — Progression Should Alter Decisions | CANDIDATE | — | RPG progression 및 인접 progression Parent Candidate |

## Parent → Genre Specialization Map

| Mechanism | Parent | Related Genre Entries | Routing Rule |
| --- | --- | --- | --- |
| Consequence Density | `UC-DESIGN-001` | Deckbuilding; Management; Strategy; `GC-ACTION-007` | 입력/기능 수 문제는 Parent 한 번. Removed-input은 Action child. |
| Contextual Value | `UC-DESIGN-002` | `GC-DECK-001`; `GC-MGMT-006`; `GC-NARR-001/009`; Strategy re-evaluation | 같은 선택 가치가 Context에 따라 안 변하면 Parent Issue로 통합. |
| Consequence → Next Decision | `UC-DESIGN-003` | `GC-MGMT-004`; `GC-NARR-003`; `GC-STRAT-001/002`; `GC-SIM-002` | 동일 State chain은 중복 Major Issue 금지. |
| Uncertainty Response | `UC-DESIGN-004` | `GC-DECK-003`; Roguelike RNG response; `GC-STRAT-009`; Action response verbs | “불확실하지만 대응 수단 없음” Parent + Genre response verb. |
| Actionable Information | `UC-DESIGN-005` | `GC-MGMT-007`; `GC-STRAT-004`; `GC-SIM-004`; `GC-ACTION-002`; Deduction 일부 | 정보량 문제는 Parent. Diagnosis/Prediction/Threat/Inference ownership의 고유 부분만 child. |
| Progression → Decisions | `UC-DESIGN-006` | `GC-RPG-001`; `GC-DECK-012`; Roguelike meta; Management growth | RPG에서 반복된다고 독립 RPG Core로 이중 승격 금지. |

### Deduction Exception

`GC-DEDUCT-001/003/004`는 정보와 관련되어도 단순 `UC-DESIGN-005`로 환원하지 않는다. Inference Ownership, Evidence Reachability, Validation Leakage는 별도 메커니즘이다.


---

# 12. Provisional Core Master Registry

총 `28`개. Canonical Rule 전문은 개별 Genre 문서를 참조한다.

| ID | Genre | Short Name | Origin | Confidence | Applies To |
| --- | --- | --- | --- | --- | --- |
| GC-DECK-001 | Deckbuilding | Contextual Card Value | Existing / strengthened | VERY HIGH | Deckbuilding / Deckbuilding Hybrid |
| GC-DECK-002 | Deckbuilding | Build Identity Formation | Existing / split-refined | HIGH | Deckbuilding / Deckbuilding Hybrid |
| GC-DECK-003 | Deckbuilding | Availability / RNG Control | Existing / UC specialization | HIGH | Deckbuilding / Deckbuilding Hybrid |
| GC-DECK-004 | Deckbuilding | Synergy Changes Decisions | New | HIGH | Deckbuilding / Deckbuilding Hybrid |
| GC-DECK-005 | Deckbuilding | Pool Growth Needs Quality Control | New | MEDIUM-HIGH | Deckbuilding / Deckbuilding Hybrid |
| GC-MGMT-001 | Management | Priority Conflict | STRENGTHEN | VERY HIGH | Management / Operations / Colony / Roster / Survival / Network Management |
| GC-MGMT-002 | Management | Loss Needs Recovery Structure | STRENGTHEN | HIGH | Management / Operations / Colony / Roster / Survival / Network Management |
| GC-MGMT-004 | Management | Persistent State Must Reprioritize | NEW | HIGH | Management / Operations / Colony / Roster / Survival / Network Management |
| GC-MGMT-005 | Management | Future Pressure vs Present Efficiency | NEW | HIGH | Management / Operations / Colony / Roster / Survival / Network Management |
| GC-MGMT-006 | Management | Routine Must Be Recontextualized | NEW | HIGH | Management / Operations / Colony / Roster / Survival / Network Management |
| GC-MGMT-007 | Management | Information Supports Diagnosis / Priority | NEW | HIGH | Management / Operations / Colony / Roster / Survival / Network Management |
| GC-MGMT-008 | Management | Growth Transforms Constraints | NEW | HIGH | Management / Operations / Colony / Roster / Survival / Network Management |
| GC-MGMT-009 | Management | Crisis Tests Existing Management State | NEW | HIGH | Management / Operations / Colony / Roster / Survival / Network Management |
| GC-ROGUE-001 | Roguelike / Roguelite | Meta Progression Cannot Rescue a Weak Reset Loop | STRENGTHEN | VERY HIGH | Roguelike / Roguelite / Hybrid |
| GC-ROGUE-003 | Roguelike / Roguelite | Meaningful Run Variation Must Force Adaptation | NEW | VERY HIGH | Roguelike / Roguelite / Hybrid |
| GC-ROGUE-004 | Roguelike / Roguelite | Run Choices Must Create Path Dependence | NEW | HIGH | Roguelike / Roguelite / Hybrid |
| GC-ROGUE-005 | Roguelike / Roguelite | Escalation Must Preserve Decisions | NEW | HIGH | Roguelike / Roguelite / Hybrid |
| GC-DEDUCT-001 | Deduction / Information | UI Externalizes Memory/Search, Not Inference | STRENGTHEN | VERY HIGH | Deduction / Investigation / Information Puzzle |
| GC-DEDUCT-003 | Deduction / Information | Evidence Relations Make Conclusion Reachable | NEW | VERY HIGH | Pure Deduction / Identification / Logic Investigation |
| GC-DEDUCT-004 | Deduction / Information | Validation Design Preserves Reasoning | NEW | HIGH | Deduction with explicit validation / answer commitment |
| GC-NARR-001 | Narrative / Systemic Narrative | State-reactive Recontextualization over Branch Count | STRENGTHEN / REFRAME | VERY HIGH | State-reactive / Systemic Narrative; conditional Branching Narrative |
| GC-NARR-002 | Narrative / Systemic Narrative | System / Narrative Choice Coupling | NEW | HIGH | Systemic Narrative / Narrative Management / Narrative RPG |
| GC-NARR-003 | Narrative / Systemic Narrative | Persistent + Causally Legible Consequence | NEW | HIGH | Choice-based / State-reactive Narrative / Narrative RPG |
| GC-STRAT-001 | Strategy | Key Strategic Decisions Change Future Option Value | NEW / UC SPECIALIZATION | VERY HIGH | Tactical / Systemic / Network / Spatial Strategy |
| GC-STRAT-002 | Strategy | Decision-Relevant State Changes Trigger Re-evaluation | NEW | VERY HIGH | Tactical / Systemic / adaptive Strategy |
| GC-STRAT-003 | Strategy | Objectives Change Action Value | NEW | HIGH | Objective-driven Tactical / Systemic Strategy |
| GC-SIM-001 | Simulation | Selective Simulation Preserves Experience-relevant Causality | NEW | VERY HIGH | Colony / Systemic / Network / Abstract Simulation |
| GC-SIM-002 | Simulation | System States Propagate through Causal Dependencies | NEW / UC SPECIALIZATION | VERY HIGH | Systemic / Colony / Survival / Production / Network Simulation |

Loading:
- L3 → 기본 `ACTIVE CHECK`.
- L2 → Project Mechanism에 적용되는 Provisional만 `ACTIVE CHECK`.
- L1/L0 → 자동 로드 금지.


---

# 13. Candidate Master Registry

총 `65`개. Candidate는 Provisional과 동일 Weight가 아니다.

| ID | Genre | Status | Confidence | Main Promotion Blocker |
| --- | --- | --- | --- | --- |
| GC-DECK-006 | Deckbuilding | KEEP AS CANDIDATE | MEDIUM | Future-consistency telemetry 부족 |
| GC-DECK-007 | Deckbuilding | KEEP AS CANDIDATE | MEDIUM | Pivot/lock-in 직접 Evidence 부족 |
| GC-DECK-008 | Deckbuilding | KEEP AS CANDIDATE | MEDIUM | Encounter-by-build pressure Evidence 부족 |
| GC-DECK-009 | Deckbuilding | KEEP AS CANDIDATE | MEDIUM | Human synergy-readability Evidence 필요 |
| GC-DECK-010 | Deckbuilding | KEEP AS CANDIDATE | MEDIUM-LOW | Formation timing telemetry 부족 |
| GC-DECK-011 | Deckbuilding | KEEP AS CANDIDATE | LOW-MEDIUM | Sequencing 직접 Evidence 약함 |
| GC-DECK-012 | Deckbuilding | KEEP AS CANDIDATE | MEDIUM-LOW | UC-DESIGN-006 중복 + vertical-power 경계 |
| GC-MGMT-003 | Management | CANDIDATE | MEDIUM | Automation boundary가 subtype-dependent |
| GC-MGMT-010 | Management | KEEP AS CANDIDATE | MEDIUM-HIGH | Intervention-window formalization 필요 |
| GC-MGMT-011 | Management | KEEP AS CANDIDATE | MEDIUM | Bottleneck vs scarcity 독립 Evidence 부족 |
| GC-MGMT-012 | Management | KEEP AS CANDIDATE | MEDIUM | Structural policy cross-title Evidence 부족 |
| GC-MGMT-013 | Management | KEEP AS CANDIDATE | MEDIUM-HIGH | Decision vs workload Human evidence 필요 |
| GC-MGMT-014 | Management | KEEP AS CANDIDATE | MEDIUM | Responsibility/micromanagement Human evidence 필요 |
| GC-MGMT-015 | Management | KEEP AS CANDIDATE | MEDIUM | Stable/crisis pacing telemetry 부족 |
| GC-ROGUE-002 | Roguelike / Roguelite | KEEP AS CANDIDATE | MEDIUM-HIGH | Player-selectable risk breadth 부족 |
| GC-ROGUE-006 | Roguelike / Roguelite | KEEP AS CANDIDATE | MEDIUM-HIGH | Failure→next-run hypothesis Human telemetry 필요 |
| GC-ROGUE-007 | Roguelike / Roguelite | KEEP AS CANDIDATE | MEDIUM-HIGH | Run length/failure-cost Human evidence 필요 |
| GC-ROGUE-008 | Roguelike / Roguelite | KEEP AS CANDIDATE | MEDIUM | Observed restart telemetry 필요 |
| GC-ROGUE-009 | Roguelike / Roguelite | KEEP AS CANDIDATE | MEDIUM | Early autopilot formalization 필요 |
| GC-ROGUE-010 | Roguelike / Roguelite | KEEP AS CANDIDATE | MEDIUM | Product promise 의존 |
| GC-ROGUE-011 | Roguelike / Roguelite | KEEP AS CANDIDATE | MEDIUM | Unlock dilution pool telemetry 부족 |
| GC-ROGUE-012 | Roguelike / Roguelite | KEEP AS CANDIDATE | MEDIUM-HIGH | Difficulty/mastery cross-title evidence 부족 |
| GC-ROGUE-013 | Roguelike / Roguelite | KEEP AS CANDIDATE | MEDIUM | Late-run telemetry 부족 |
| GC-DEDUCT-005 | Deduction / Information | KEEP AS CANDIDATE | MEDIUM-HIGH | Formal sufficiency vs Human accessibility 분리 필요 |
| GC-DEDUCT-006 | Deduction / Information | KEEP AS CANDIDATE | MEDIUM | Missed-clue recovery Evidence 부족 |
| GC-DEDUCT-007 | Deduction / Information | KEEP AS CANDIDATE | MEDIUM-HIGH | Hypothesis-space formal definition 필요 |
| GC-DEDUCT-008 | Deduction / Information | KEEP AS CANDIDATE | MEDIUM | Human stuck-recovery validation 필요 |
| GC-DEDUCT-010 | Deduction / Information | KEEP AS CANDIDATE | MEDIUM | 추가 Primary Evidence 필요 |
| GC-DEDUCT-011 | Deduction / Information | KEEP AS CANDIDATE | MEDIUM-LOW | Pacing Human telemetry 부족 |
| GC-DEDUCT-012 | Deduction / Information | KEEP AS CANDIDATE | MEDIUM | Multiple-path direct Evidence 부족 |
| GC-NARR-005 | Narrative / Systemic Narrative | KEEP AS CANDIDATE | MEDIUM-HIGH | Cross-title world-memory + Human continuity 부족 |
| GC-NARR-006 | Narrative / Systemic Narrative | KEEP AS CANDIDATE | MEDIUM-HIGH | Roleplay vs utility Human/choice telemetry 필요 |
| GC-NARR-007 | Narrative / Systemic Narrative | KEEP AS CANDIDATE | MEDIUM | Subtype dependence |
| GC-NARR-008 | Narrative / Systemic Narrative | KEEP AS CANDIDATE | MEDIUM | Relationship Primary Evidence 부족 |
| GC-NARR-010 | Narrative / Systemic Narrative | KEEP AS CANDIDATE | MEDIUM | Emergent evidence가 RimWorld 계열에 편중 |
| GC-NARR-011 | Narrative / Systemic Narrative | KEEP AS CANDIDATE | MEDIUM | Narrative pacing telemetry 부족 |
| GC-STRAT-004 | Strategy | KEEP AS CANDIDATE / POSSIBLE UC SUB-RULE | HIGH | UC-DESIGN-005 중복 |
| GC-STRAT-005 | Strategy | KEEP AS CANDIDATE | HIGH — Spatial/Tactical only | Spatial/Tactical 한정 |
| GC-STRAT-006 | Strategy | KEEP AS CANDIDATE | MEDIUM-HIGH | Invisible, Inc. 의존 비중 |
| GC-STRAT-007 | Strategy | KEEP AS CANDIDATE | MEDIUM-HIGH | Recovery cross-title/Human evidence 부족 |
| GC-STRAT-008 | Strategy | KEEP AS CANDIDATE | MEDIUM | Multiplayer/adaptive counter evidence 부족 |
| GC-STRAT-009 | Strategy | KEEP AS CANDIDATE | MEDIUM-HIGH | UC-DESIGN-004 중복 |
| GC-STRAT-010 | Strategy | KEEP AS CANDIDATE | MEDIUM | Late-game telemetry 부족 |
| GC-STRAT-011 | Strategy | KEEP AS CANDIDATE | MEDIUM-HIGH | UC-DESIGN-005/abstraction-scope 중복 |
| GC-SIM-003 | Simulation | KEEP AS CANDIDATE | MEDIUM-HIGH | Emergence subtype 차이 + Primary breadth 부족 |
| GC-SIM-004 | Simulation | KEEP AS CANDIDATE / POSSIBLE UC SUB-RULE | HIGH | UC-DESIGN-005/Management diagnosis 중복 |
| GC-SIM-005 | Simulation | KEEP AS CANDIDATE | MEDIUM-HIGH | Agent/Social second Primary 부족 |
| GC-SIM-006 | Simulation | KEEP AS CANDIDATE | MEDIUM-HIGH | Observation vs intervention promise 의존 |
| GC-SIM-007 | Simulation | KEEP AS CANDIDATE | MEDIUM-HIGH | Stable/runaway/cascade formal definition 필요 |
| GC-SIM-008 | Simulation | KEEP AS CANDIDATE | MEDIUM | Director evidence RimWorld 편중 |
| GC-RPG-001 | RPG | KEEP AS CANDIDATE | HIGH as specialization / MEDIUM independent | UC-DESIGN-006 specialization; 독립 Core evidence 부족 |
| GC-RPG-002 | RPG | KEEP AS CANDIDATE | MEDIUM-HIGH | CRPG/JRPG/Class evidence 추가 필요 |
| GC-RPG-003 | RPG | KEEP AS CANDIDATE | MEDIUM | Endgame differentiation evidence 부족 |
| GC-RPG-004 | RPG | KEEP AS CANDIDATE | MEDIUM-HIGH | Quest/Encounter solution-by-build evidence 부족 |
| GC-RPG-005 | RPG | KEEP AS CANDIDATE | HIGH cross-genre / LOW-MEDIUM independent | UC-DESIGN-003/Management/Narrative 중복 |
| GC-RPG-006 | RPG | KEEP AS CANDIDATE | MEDIUM-LOW | Equipment/loot direct evidence 부족 |
| GC-RPG-007 | RPG | KEEP AS CANDIDATE | LOW-MEDIUM | Respec/commitment telemetry 부족 |
| GC-RPG-008 | RPG | KEEP AS CANDIDATE | LOW | Action RPG/player-skill evidence 부족 |
| GC-ACTION-001 | Action | KEEP AS CANDIDATE | MEDIUM | Direct input/buffer/cancel/response source 부족 |
| GC-ACTION-002 | Action | KEEP AS CANDIDATE / POSSIBLE UC SUB-RULE | VERY HIGH as specialization | UC-DESIGN-005 specialization; 독립 GC 필요성 낮음 |
| GC-ACTION-003 | Action | KEEP AS CANDIDATE | HIGH stealth / MEDIUM broad Action | Mark of the Ninja 중심; broad Action evidence 부족 |
| GC-ACTION-004 | Action | KEEP AS CANDIDATE | MEDIUM-HIGH movement subtypes | Movement-centric subtype 한정 |
| GC-ACTION-005 | Action | KEEP AS CANDIDATE | LOW-MEDIUM | Commitment/cancel direct evidence 부족 |
| GC-ACTION-006 | Action | KEEP AS CANDIDATE | MEDIUM-LOW | Recovery/error-propagation direct evidence 부족 |
| GC-ACTION-007 | Action | KEEP AS CANDIDATE / POSSIBLE UC SUB-RULE | VERY HIGH as specialization | UC-DESIGN-001 specialization; 독립 GC 필요성 낮음 |

---

# 14. Merge / Reclassification Registry

| Entry | Canonical Relationship | Target / Parent | Router Treatment |
| --- | --- | --- | --- |
| `GC-MGMT-016` | MERGED | `GC-MGMT-001` Sub-rule | 독립 Check 금지. |
| `GC-DEDUCT-002` | RECLASSIFIED | Product / Content Consumption Candidate | Deduction Mechanic violation에서 제외. |
| `GC-DEDUCT-009` | MERGE CANDIDATE | `GC-DEDUCT-001` Sub-rule | Parent 아래 child check. |
| `GC-NARR-004` | MERGE CANDIDATE | `GC-NARR-001` | Branch convergence를 Parent 아래 판정. |
| `GC-NARR-009` | MERGE CANDIDATE / UC specialization | `GC-NARR-001` / `UC-DESIGN-002` | 반복 Verb recontextualization child. |
| `GC-SIM-009` | MERGE CANDIDATE | `GC-SIM-001` Sub-rule | Abstraction을 Selective Simulation 아래 판정. |
| `GC-RPG-001` | Universal Strengthening | `UC-DESIGN-006` | Parent-first; 독립 Provisional처럼 취급 금지. |
| `GC-ACTION-002` | Universal Strengthening / possible UC sub-rule | `UC-DESIGN-005` | Threat info = Parent Issue + Action specialization. |
| `GC-ACTION-007` | Universal Strengthening / possible UC sub-rule | `UC-DESIGN-001` | Removed input = Parent + residual agency specialization. |
| `GC-ACTION-003` | Universal Reclassification Candidate | Failure Attribution | 현재는 Action Candidate로 유지. |
| `GC-STRAT-004` | Candidate / possible UC sub-rule | `UC-DESIGN-005` | Information Double Penalty 금지. |
| `GC-SIM-004` | Candidate / possible UC sub-rule | `UC-DESIGN-005` | Causal diagnosis 특수성만 child. |
| `GC-DECK-003` | Existing Core Audit: UC specialization | `UC-DESIGN-004` related | Availability/RNG control의 deck-specific response만 유지. |

이 Registry는 Canonical Status를 변경하지 않는다.


---


# 14A. Canonical GSC Registry

## Active Independent GSC

`NONE`

## GSC Candidate

`NONE`

## Retired Historical GSC

| GSC | Former Status | New Canonical Status | Parent / Handoff Route | Runtime |
|---|---|---|---|---|
| `GSC-DECK-SOLO-001` | PROVISIONAL CORE | `RETIRED_AS_INDEPENDENT_GSC` | `GC-DECK-004/005 + SC-SOLO-002/003 + DECK-001/002` | Historical trace only; active load 금지 |
| `GSC-MGMT-SOLO-001` | PROVISIONAL CORE | `RETIRED_AS_INDEPENDENT_GSC` | `GC-MGMT-014 + SC-SOLO-002 (+003) + MGMT-001/002 (+003)`; `GC-SIM-001` only if Simulation routed | Historical trace + Routing Specialization |
| `GSC-DEDUCT-SOLO-001` | PROVISIONAL CORE | `RETIRED_AS_INDEPENDENT_GSC` | `GC-DEDUCT-003/005 + SC-SOLO-002 + DEDUCT-001/002/003/005` | Historical trace / routing example only |

## Routing Specialization Registry

Core가 아닌 Reviewer Action Hint다. 새 ID family를 만들지 않는다.

| Context | Name | Source | Runtime Use |
|---|---|---|---|
| Management × Solo | `Responsibility Level as Scope Cut Boundary` | `GC-MGMT-014 + SC-SOLO-002 + MGMT-001/002` | Player Responsibility 아래 Detail부터 Scope Cut 검토 |
| Action × Solo | `Iteration Throughput / Feel Polish Budgeting` | `SCALE_HANDOFF-ACTION-008 + SC-SOLO-002 Iteration-heavy Axis` | Animation/Input/Feedback/VFX 반복 Polish cycle을 Production Scope에 포함 |

## Optional GSC Layer State

```text
Universal
↓
Genre
↓
Scale
↓
Scale Handoff
↓
Optional GSC

Active Optional GSC:
0
```

GSC Namespace는 유지하지만 자동 Load하지 않는다.

---

# 15. Evidence Boundary Registry

| Genre | Strong Evidence | Weak Evidence | Do Not Generalize To | Additional Evidence Needed |
| --- | --- | --- | --- | --- |
| Deckbuilding | Deckbuilding core loop / contextual card value / build identity / availability control | PvP deckbuilding / CCG economy / very large live-service pools | PvP/CCG/live-service balance and economy without additional evidence | PvP deckbuilder telemetry; long-tail pool growth; live balance |
| Management | Operations / survival / colony / roster / network management | Large macro-economy / MMO-live operations / highly social management | Simulation/strategy merely because resources exist | Human priority telemetry; automation burden; larger-scale management controls |
| Roguelike / Roguelite | Run-based reset / variation / path-dependence / repeated mastery | Long campaign roguelikes / multiplayer / content-heavy procedural worlds | Any randomized or permadeath game without reset/mastery structure | Human restart telemetry; failure learning; late-run autopilot |
| Deduction / Information | Pure deduction / identification / information puzzle logic | Open-world investigation / social deduction / broad mystery adventure | Mystery theme or information processing without player-owned inference | More primary deduction cases; human inference/stuck telemetry |
| Narrative / Systemic Narrative | Adaptive / state-reactive / systemic narrative | Pure linear authored narrative / broad emergent narrative / VO-heavy branching production | Linear/authored narrative where state reactivity is not the promise | Consequence recall; character continuity; emergent story; state QA |
| Strategy | Tactical / systemic / stealth / network / small-state strategy | RTS / 4X / Grand Strategy / Multiplayer | Macro/multiplayer strategy before additional evidence | RTS; 4X; multiplayer counterplay; planning horizon; recovery telemetry |
| Simulation | Colony / systemic / network / abstract simulation | Vehicle / sports / physics / large economy / social / hardcore realism | Realism-heavy simulation subtypes before additional evidence | ONI cascades; Factorio logistics; Sims autonomy; DF emergence |
| RPG | Persistent character state / roster consequence; narrative-RPG support | Traditional CRPG / JRPG / Open-world / ARPG / Equipment / Companion | RPG-wide class/build/quest rules before additional evidence | Disco Elysium; BG3; DOS2; Mass Effect 2; representative JRPG |
| Action | Stealth Action / Survivors-like / Compact Action | Character Action / FPS / Fighting / Souls-like / Precision Platformer / Bullet Hell / PvP | Action subtypes outside current evidence boundary | Hades; Dead Cells; Sekiro; DOOM Eternal; Celeste |

`L3`는 Project Contribution Level이고, Confidence는 Knowledge Evidence Strength다. 서로 대체하지 않는다.


---

# 16. Reviewer Loading Rules

```text
STEP 0  Project Mechanism Extraction
        Player Verbs / State / Loop / Product Promise

STEP 1  PROJECT_GENRE_ROUTING_PROFILE 생성

STEP 2  Universal Core Load

STEP 3  L3 Primary Genre Provisional Load

STEP 4  L3 High-confidence Candidate → WATCH

STEP 5  L2 Secondary Provisional Load

STEP 6  L2 Candidate → Risk Signal 있을 때만

STEP 7  L1 Supporting → Question 2~4개 선택 참조

STEP 8  Cross-Genre Deduplication

STEP 9  PROJECT_SCALE_ROUTING_PROFILE / Relevant Scale Core Load

STEP 10 Active Genre Scale Handoff Load

STEP 11 Optional GSC Registry Check
        현재 Active Independent GSC = NONE
        Retired GSC는 Active / Diagnostic Load 금지

STEP 12 Routing Specialization은 필요 시 Reviewer Action Hint로만 사용

STEP 13 Market / Selection Layer는 해당 목적일 때만
```

### Ordering Principle

Genre Rule을 먼저 읽고 Project를 장르에 끼워 맞추지 않는다.

```text
Project Mechanism
→ Genre Contribution / Routing
→ Universal Parent
→ Relevant Genre Specialization
```

순서를 유지한다.

### RPG / Action Special Case

Provisional이 `NONE`이어도 L3 Routing 가능하다.

```text
Universal Parent
+
High-confidence Genre Candidate
+
Genre Default Reviewer Questions
+
Evidence Boundary Warning
```


---

# 17. Candidate Loading Severity

| Core Status / Confidence | Runtime Behavior |
| --- | --- |
| Provisional Core | `ACTIVE CHECK` |
| Candidate — VERY HIGH / HIGH | `WATCH / CHECK IF APPLICABLE` |
| Candidate — MEDIUM-HIGH / MEDIUM | `DIAGNOSTIC ONLY` |
| Candidate — LOW-MEDIUM / MEDIUM-LOW / LOW | `REFERENCE ONLY` |
| Merge Candidate | Parent 아래 child check |
| Reclassified | 원래 Genre violation에서 제외 |

```text
Evidence Confidence
≠
Project Issue Severity
```

Candidate Rule이라도 실제 Project에서 Core Loop Collapse를 만들면 CRITICAL/HIGH Issue가 될 수 있다.


---

# 18. Double-Penalty Prevention Rules

1. **Parent-first** — Universal → Genre Specialization.
2. **One Root Issue** — 같은 Mechanism은 한 Root Issue로 집계.
3. **Applicability before Violation** — 적용되지 않으면 `N/A`, `PASS`가 아님.
4. **Distinct subfinding allowed** — Parent가 같아도 실제 loop failure가 다르면 child evidence를 나눌 수 있음.

예:

```text
ISSUE:
Threat information is not actionable.

Parent:
UC-DESIGN-005

Action Specialization:
GC-ACTION-002

Evidence:
Cue exists, but structurally usable response window is unavailable.

Severity:
HIGH
```

`UC-DESIGN-005 HIGH` + `GC-ACTION-002 HIGH`처럼 두 Major Issue로 이중 집계하지 않는다.


---

# 19. Dynamic Reviewer Set Schema

질문 예산:

```text
Universal: 5~10
Primary Genre A: 5~8
Primary Genre B: 5~8
Secondary Genre: 각 2~4
Diagnostic Candidate: Risk Signal 있을 때만
```

```text
PROJECT_REVIEWER_SET

Universal:
- UC-...

Primary <Genre A>:
- GC-... [ACTIVE CHECK]
- Candidate ... [WATCH]

Primary <Genre B>:
- ...

Secondary <Genre C>:
- ...

Diagnostic Candidate:
- ...

Scale Handoff:
- SCALE_HANDOFF-...

N/A:
- ...

Merged Questions:
- Parent Issue:
  Universal:
  Genre Specialization:

Evidence Boundary Warnings:
- ...
```

Question Priority:
1. Provisional
2. Strong Universal
3. Product Promise-linked Candidate
4. Known Risk-linked Candidate
5. Scale Risk
6. Evidence Gap


---

# 20. Hybrid Conflict Registry

| Pair | Potential Conflict | Hidden Variable | Reviewer Question |
| --- | --- | --- | --- |
| Action × Strategy | Execution speed가 planning bandwidth 제거 | Execution vs Planning Fantasy | Reflex가 계획 가치를 지우는가, 계획이 execution을 실제 바꾸는가? |
| Management × Narrative | 최적 효율이 roleplay/human consequence를 압도 | Product promise / scarcity severity | 같은 선택이 관리 효율과 narrative meaning을 공유하는가? |
| RPG × Action | Player execution이 Character build를 무력화하거나 반대 | Player-skill vs character-skill promise | 어느 축이 outcome을 어느 정도 지배해야 하는가? |
| Simulation × Management | Model detail이 responsibility 아래까지 내려가 micromanagement화 | Responsibility / abstraction / automation | Player가 직접 관리해야 하는 State인가, world model로만 존재해야 하는가? |
| Roguelike × Narrative | Reset이 narrative persistence와 충돌 | Run fiction / meta continuity | 무엇이 Reset되고 무엇이 Story History로 남는가? |
| Deckbuilding × RPG | Card Build와 Character Build가 중복 progression layer | Build ownership / horizon | 두 Build가 서로 다른 결정을 만드는가? |
| Deckbuilding × Roguelike | Run build / unlock/meta가 variation 역할 중복 | Run identity / meta purpose | 별도 meta가 실제 새 결정을 만드는가? |
| Deduction × Narrative | Authored reveal이 player inference를 대체 | Authored payoff vs inference ownership | 결론은 evidence relation으로 플레이어가 만들었는가? |
| Strategy × Simulation | Simulation complexity가 plan diagnosis를 압도 | Model legibility / planning horizon | World state가 plan value를 바꾸며 cause를 읽을 수 있는가? |
| Action × Narrative | Narrative delivery가 cadence를 끊거나 action speed가 consequence recognition 제거 | Session rhythm / narrative promise | 두 loop가 shared state를 갖는가, 서로를 중단시키는가? |

이 Table은 Core가 아니라 Routing Aid다.


---

# 21. Validation Routing Registry

| Genre | Machine / Structural Strength | Human Strength | Routing Principle |
| --- | --- | --- | --- |
| Deckbuilding | pick/build/draw/pool/convergence/dominance | build identity, reward tension, synergy readability | 구조 수렴 제거 후 Human choice quality |
| Management | state/allocation/loss/recovery/bottleneck | priority clarity, burden, crisis perception | state failure와 diagnosis experience 분리 |
| Roguelike | run/variation/failure/adaptation | restart intent, failure learning, run identity | batch restart와 Human restart intent 분리 |
| Deduction | evidence graph/reachability/solution integrity | inference ownership, fairness, stuck reason | formal solver ≠ Human difficulty |
| Narrative | state/trigger/contradiction/coverage | agency, ownership, emotion, continuity | simulation coverage ≠ player exposure |
| Strategy | policy/convergence/position/resource/objective | planning, tension, failure attribution | AI policy success ≠ Human strategy quality |
| Simulation | state transition/causal chain/cascade/edge state | mental model, causal legibility, fantasy | Simulation Log / Telemetry / Human explanation 분리 |
| RPG | build/stat/skill/progression/content coverage | identity, ownership, fantasy, attachment | AI optimal build ≠ player understanding |
| Action | input/state/collision/threat/damage/recovery | responsiveness, readability, fairness, feel | AI reaction success ≠ Human response opportunity |


---

# 22. AI Tester Routing Registry

| Genre | Applicable Tester Profiles / Policy Families | Non-applicable by Default | Required Model Definitions |
| --- | --- | --- | --- |
| Deckbuilding | Named genre persona registry not canonical; metric/policy routing only | 다른 Genre Persona를 이름만 보고 import 금지 | Build identity; dead pick/draw; convergence; key availability; dominant engine |
| Management | Named genre persona registry not canonical; metric/policy routing only | Roguelike/Strategy Persona를 management identity로 자동 사용 금지 | Bottleneck; preventable failure; recovery opportunity; stable/crisis state |
| Roguelike / Roguelite | P-ROGUE-001 — Efficiency Persona; P-ROGUE-002 — Risk-seeking Persona; P-ROGUE-003 — Conservative Persona; P-ROGUE-004 — Explorer Persona; P-ROGUE-005 — General Persona | Batch auto-restart를 Human restart intent로 해석 금지 | Run boundary; failure cause; bad-seed concentration; preventable failure |
| Deduction / Information | P-DEDUCT-001 — Exhaustive Searcher; P-DEDUCT-002 — Minimal Evidence Solver; P-DEDUCT-003 — Full Evidence Verifier; P-DEDUCT-004 — Missed-clue Scenario; P-DEDUCT-005 — Wrong Hypothesis Tester | LLM solving speed를 Human difficulty로 사용 금지 | Validation leakage; first solvable state; stuck state; alternate reasoning path |
| Narrative / Systemic Narrative | P-NARR-001 — Coverage Explorer; P-NARR-002 — Consequence Tracer; P-NARR-003 — Contradiction Hunter; P-NARR-004 — Repetition Stress Tester; P-NARR-005 — Divergent Path Tester; P-NARR-006 — State Memory Tester | AI state access를 Player recall/agency로 사용 금지 | Cosmetic/local/persistent choice; recontextualization; forgotten flag; contradiction |
| Strategy | P-STRAT-001 — Greedy / Immediate Value; P-STRAT-002 — Long-horizon Planner; P-STRAT-003 — Conservative; P-STRAT-004 — Aggressive; P-STRAT-005 — Flexible / Adaptive; P-STRAT-006 — Explorer | AI full-state access를 Player information acquisition으로 사용 금지 | Future option value; dominant opening; recovery window; risk exposure |
| Simulation | P-SIM-001 — Baseline Observer; P-SIM-002 — Optimizer; P-SIM-003 — Stress Inducer; P-SIM-004 — Random Intervention; P-SIM-005 — Explorer; P-SIM-006 — No-recovery Profile | Internal state read를 Player inspect/diagnosis로 기록 금지 | Cascade; stable/runaway state; interaction; causal chain; director override |
| RPG | P-RPG-001 — Vertical Power Optimizer; P-RPG-002 — Specialist; P-RPG-003 — Generalist; P-RPG-004 — Roleplayer Policy; P-RPG-005 — Explorer; P-RPG-006 — Respec / Pivot Tester | AI optimal-build evaluation을 ownership/identity로 사용 금지 | Build identity/convergence; role overlap; dead investment; stat/skill contribution |
| Action | P-ACTION-001 — Aggressive; P-ACTION-002 — Defensive; P-ACTION-003 — Mobility; P-ACTION-004 — Greedy Damage; P-ACTION-005 — Survival; P-ACTION-006 — Explorer | Perfect reaction policy를 Human reaction time으로 사용 금지 | Reaction sensitivity; recovery window; safe space; threat cue mapping; error chain |

- L3 → 해당 Genre의 canonical profile family를 validation question에 맞게 선택.
- L2 → 필요한 profile만.
- L1/L0 → 자동 profile load 금지.
- Persona는 Rule을 바꾸지 않고 Choice Policy만 바꾼다.
- Persona parameter specification은 별도 AI Tester 문서가 소유한다.


---

# 23. Scale Handoff Registry

Genre 문서에서 총 `51`개 Handoff를 수집했다. Genre Core가 아니며 Solo/Micro Production Review로 전달한다.

| ID | Genre | Cost Driver | Risk Type |
| --- | --- | --- | --- |
| SCALE_HANDOFF-DECK-001 | Deckbuilding | Interaction Regression Explosion | QA / Logic / Balance |
| SCALE_HANDOFF-DECK-002 | Deckbuilding | Data Content is Cheap Only Until Balance/Tooltip Cost Dominates | Content / Balance / UI / QA |
| SCALE_HANDOFF-DECK-003 | Deckbuilding | Familiar Rule Base as Cognitive Budget | UI / Onboarding |
| SCALE_HANDOFF-MGMT-001 | Management | Entity × State × Event QA Explosion | QA / Logic |
| SCALE_HANDOFF-MGMT-002 | Management | Management UI State Cost | UI |
| SCALE_HANDOFF-MGMT-003 | Management | Automation Tooling ROI | Tooling / Technical |
| SCALE_HANDOFF-MGMT-004 | Management | Content Authoring Cost | Content |
| SCALE_HANDOFF-ROGUE-001 | Roguelike / Roguelite | Run Content Matrix QA Explosion | QA / Content |
| SCALE_HANDOFF-ROGUE-002 | Roguelike / Roguelite | Procedural Generation Is Not Free Content | Content / QA / Technical |
| SCALE_HANDOFF-ROGUE-003 | Roguelike / Roguelite | Unlock / Meta Content Cost | Content / Balance / QA |
| SCALE_HANDOFF-ROGUE-004 | Roguelike / Roguelite | Systemic Recombination as Content Multiplier | Logic / QA |
| SCALE_HANDOFF-DEDUCT-001 | Deduction / Information | Logic QA Cost | Logic / QA |
| SCALE_HANDOFF-DEDUCT-002 | Deduction / Information | Authored Relation Cost | Content / Logic |
| SCALE_HANDOFF-DEDUCT-003 | Deduction / Information | Localization Can Become Logic QA | Localization / Logic / QA |
| SCALE_HANDOFF-DEDUCT-004 | Deduction / Information | Visual Evidence Accessibility QA | Art / UI / QA |
| SCALE_HANDOFF-DEDUCT-005 | Deduction / Information | Limited Screens Do Not Mean Low Content Cost | Content / QA |
| SCALE_HANDOFF-NARR-001 | Narrative / Systemic Narrative | Branch / State Explosion | Content / Logic / QA |
| SCALE_HANDOFF-NARR-002 | Narrative / Systemic Narrative | Reactive Content QA | Logic / QA / Content |
| SCALE_HANDOFF-NARR-003 | Narrative / Systemic Narrative | Localization Multiplier | Localization / QA |
| SCALE_HANDOFF-NARR-004 | Narrative / Systemic Narrative | Voice-over Multiplier | Content / Localization / Audio |
| SCALE_HANDOFF-NARR-005 | Narrative / Systemic Narrative | Authored Content Exposure | Content |
| SCALE_HANDOFF-NARR-006 | Narrative / Systemic Narrative | Narrative Tooling ROI | Tooling / Logic |
| SCALE_HANDOFF-NARR-007 | Narrative / Systemic Narrative | State Count Can Hide Authoring Cost | Logic / QA / Content |
| SCALE_HANDOFF-STRAT-001 | Strategy | Interaction QA Matrix | QA / Logic / Balance |
| SCALE_HANDOFF-STRAT-002 | Strategy | Opponent AI Cost | AI / Technical / QA |
| SCALE_HANDOFF-STRAT-003 | Strategy | Map / Pathfinding Scope | Technical / Content |
| SCALE_HANDOFF-STRAT-004 | Strategy | Scenario × Objective QA | QA / Logic / Content |
| SCALE_HANDOFF-STRAT-005 | Strategy | Multiplayer Balance Multiplier | Balance / Technical / QA |
| SCALE_HANDOFF-STRAT-006 | Strategy | Simulation / Replay Tooling ROI | Tooling / Technical |
| SCALE_HANDOFF-SIM-001 | Simulation | Entity × State Matrix | QA / Logic / Technical |
| SCALE_HANDOFF-SIM-002 | Simulation | Cross-system Interaction Matrix | QA / Logic |
| SCALE_HANDOFF-SIM-003 | Simulation | Agent AI Cost | AI / Technical |
| SCALE_HANDOFF-SIM-004 | Simulation | Persistent State / Save Cost | Technical / Logic |
| SCALE_HANDOFF-SIM-005 | Simulation | Observability Tooling | Tooling / UI |
| SCALE_HANDOFF-SIM-006 | Simulation | Procedural Content Is Not Free Content | Content / QA / Technical |
| SCALE_HANDOFF-SIM-007 | Simulation | Simulation Detail × UI Cost | UI |
| SCALE_HANDOFF-RPG-001 | RPG | Class × Skill × Equipment Matrix | QA / Balance / Content |
| SCALE_HANDOFF-RPG-002 | RPG | Quest × Build Coverage | Content / Logic / Narrative |
| SCALE_HANDOFF-RPG-003 | RPG | Companion Cost | Content / Art / Animation / AI |
| SCALE_HANDOFF-RPG-004 | RPG | Equipment Content Cost | Content / Art / UI / QA |
| SCALE_HANDOFF-RPG-005 | RPG | Progression QA Matrix | QA / Logic / Balance |
| SCALE_HANDOFF-RPG-006 | RPG | Narrative Reactivity Multiplier | Narrative / Localization / QA |
| SCALE_HANDOFF-RPG-007 | RPG | Build-supporting Content Cost | Content / QA |
| SCALE_HANDOFF-ACTION-001 | Action | Animation State Matrix | Animation / QA |
| SCALE_HANDOFF-ACTION-002 | Action | Hitbox / Hurtbox QA | QA / Technical |
| SCALE_HANDOFF-ACTION-003 | Action | Enemy Pattern Matrix | QA / Content / AI |
| SCALE_HANDOFF-ACTION-004 | Action | VFX / SFX Feedback Cost | Art / Animation / Audio / UI |
| SCALE_HANDOFF-ACTION-005 | Action | Weapon / Skill Content Cost | Animation / Art / QA / Balance |
| SCALE_HANDOFF-ACTION-006 | Action | Control Scheme QA | UI / Technical / QA |
| SCALE_HANDOFF-ACTION-007 | Action | Performance Is a Design Constraint | Technical |
| SCALE_HANDOFF-ACTION-008 | Action | Feel Polish Is Iterative Production Cost | Animation / Art / Audio / Iteration |

현재 단계에서는:

```text
Genre
↓
Scale Handoff
↓
Solo / Micro Risk
```

연결만 유지한다. 새 `Genre × Scale Core`는 생성하지 않는다.


---

# 24. Missing Genre Detection

현재 9개 밖의 Project를 억지로 기존 Genre에 넣지 않는다.

예:
- Puzzle
- Survival
- Sports
- Racing
- Rhythm
- Horror

다음 조건이 반복 확인되면 `MISSING_GENRE_CANDIDATE`를 만든다.

1. 여러 Project에서 같은 독립 Mechanism 반복.
2. 기존 Universal / Genre Core로 설명되지 않음.
3. 별도 Reviewer Question군 필요.
4. 충분한 Reference 후보 존재.

이 단계에서 새 Genre Extraction은 시작하지 않는다.


---

# 25. Multi-Genre Scope Warning

다음 중 하나면:

```text
Primary Genre >= 3
```

또는:

```text
L2 이상 Genre >= 5
```

`HYBRID_SCOPE_WARNING`.

품질 점수가 아니다.

검토:
- System Integration
- Content
- UI
- Onboarding
- QA
- Cognitive Load
- Production Ownership


---

# 26. Routing Examples

## Deckbuilding Roguelite

```text
Deckbuilding — L3
Roguelike — L3
Strategy — L1/L2 if actual planning exists
RPG — L0/L1 unless persistent character formation exists
Narrative — L0/L1
```

## Narrative Management Simulation

```text
Management — L3
Narrative — L3
Simulation — L2
Strategy — L1/L2 depending on planning
```

Resource meter만으로 Simulation을 로드하지 않는다.

## Action RPG

```text
Action — L3
RPG — L3
Strategy — only if planning is structurally meaningful
Roguelike — only if run/reset exists
Narrative — only if persistent narrative state/reactivity contributes
```

Action/RPG는 Provisional 0이므로 Universal + Candidate + Boundary를 사용한다.

## Investigation Narrative Game

```text
Deduction — L3
Narrative — L2/L3
Management — L0
Strategy — L0/L1
RPG — only if persistent character formation exists
```

Mystery Theme만으로 Deduction을 로드하지 않는다.


---

# 27. Traceability / Versioning

## Traceability

```text
GC-ID
↓
Canonical Genre Document
↓
Core / Promotion / Reviewer Section
↓
Source Trace
↓
Original Reference
```

## Versioning

```text
Genre Document Version Up
↓
Master Index Sync Required
```

Master Index가 원본보다 먼저 Core Status를 변경하지 않는다.

Project Review Snapshot 권장:

```text
Master Index Version: `v0.2`
Universal Baseline Version:
Loaded Genre Baseline Versions:
Routing Profile Version:
Reviewer Set Version:
```


---

# 28. Self-Review

| Check | Result |
| --- | --- |
| Routing/Registry 중심인가? | PASS |
| 새 Core를 만들지 않았는가? | PASS |
| Candidate를 Provisional처럼 다루지 않는가? | PASS |
| Universal/Genre Double Penalty 방지? | PASS |
| Store Tag보다 Mechanism 우선? | PASS |
| Hybrid에 모든 Genre 자동 적용 금지? | PASS |
| L0~L3가 Verb/State/Decision/Promise 기반? | PASS |
| RPG/Action Provisional 0도 Routing 가능? | PASS |
| Evidence Boundary 유지? | PASS |
| Machine/Human Validation Routing 유지? | PASS |
| Scale Handoff와 Genre Core 분리? | PASS |
| Missing Genre 강제 편입 방지? | PASS |
| Hybrid Scope Warning을 품질 점수로 오용하지 않음? | PASS |
| Canonical Genre Document trace 가능? | PASS |
| Canonical Rule 재작성/상태 변경 없음? | PASS |


---

# 29. Final Position

## A. 9개 Genre Baseline은 Router로 사용 가능한가?

**YES — `INTEGRATION_BASELINE` 수준에서 사용 가능하다.**

조건:
- Mechanism-first Routing
- Applicability 선행
- Universal Parent → Genre Specialization
- Candidate Confidence ≠ Issue Severity
- Evidence Boundary 유지

## B. 반복 specialization되는 Universal Core는?

우선순위가 높은 반복 Parent:

1. `UC-DESIGN-005` — Management / Strategy / Simulation / Action / Deduction 일부.
2. `UC-DESIGN-003` — Management / Narrative / Strategy / Simulation.
3. `UC-DESIGN-002` — Deckbuilding / Management / Narrative / Strategy.
4. `UC-DESIGN-004` — Deckbuilding / Roguelike / Strategy / Action / Management.
5. `UC-DESIGN-001` — Deckbuilding / Management / Strategy / Action.
6. `UC-DESIGN-006` — RPG에서 가장 직접적으로 강화; Deck/Rogue progression에도 인접.

## C. Double Penalty 위험이 가장 큰 곳은?

가장 큰 Cluster:

```text
Management
Strategy
Simulation
Action
(+ Deduction 일부)
↓
UC-DESIGN-005
```

두 번째:

```text
Management
Narrative
Strategy
Simulation
↓
UC-DESIGN-003
```

## D. Hybrid Conflict 가능성이 높은 Pair는?

우선 경계:
1. Action × Strategy
2. Simulation × Management
3. Management × Narrative
4. RPG × Action
5. Roguelike × Narrative
6. Deckbuilding × RPG
7. Deduction × Narrative

이는 품질 순위가 아니라 Routing conflict priority다.

## E. 현재 Evidence가 가장 강한 Genre는?

**Management.**

Provisional 수 때문만이 아니라 Priority / Loss / Persistence / Future Pressure / Routine / Information / Growth / Crisis가 여러 독립 Reference에서 반복되고 Boundary까지 비교적 넓게 확보되어 있다.

`Deckbuilding`, `Roguelike / Roguelite`가 그 다음 강한 축이다.

## F. Evidence가 가장 약한 Genre는?

**RPG가 breadth 기준으로 가장 약하다.**

- Darkest Dungeon / Citizen Sleeper 편중.
- CRPG / JRPG / ARPG / Equipment / Companion 공백.
- Provisional `NONE`.

Action도 Provisional 0이지만 Mark of the Ninja와 Vampire Survivors의 직접 Action mechanism이 비교적 선명해 RPG보다는 특정 검증 축이 더 명확하다.

## G. Additional Reference 전까지 제한 적용할 Genre는?

가장 강한 제한:
- RPG
- Action

명시 Boundary 유지:
- Strategy — RTS / 4X / Grand Strategy / Multiplayer
- Simulation — Vehicle / Sports / Physics / Large Economy / Social / Hardcore Realism
- Deduction — broad open investigation / social deduction
- Narrative — pure linear authored / broad emergent narrative

## H. Master Index 이후 우선순위

### Completed

1. `Scale Core Consolidation / Routing Baseline` ✅
2. `Genre × Scale Core Integration` ✅
3. `Canonical GSC Consolidation / Source Sync` ✅

Canonical GSC 상태:

```text
Active Independent GSC: 0
Retired Historical GSC: 3
Routing Specialization: 2
```

### Next — Universal Core Consolidation

다음 단계에서는:

- `UC-DESIGN-001 ~ 006`의 반복 Genre specialization
- `SC-SOLO-001`의 Validation Parent 가능성
- `SC-SOLO-004`의 Reference Analysis Parent 가능성
- Failure Attribution / Recovery / Identity / Complexity 관련 cross-genre candidate
- Parent hierarchy와 Reviewer Double-Penalty

를 정리한다.

### After Universal Consolidation

1. Reviewer Runtime Specification
2. Validation Planner Specification
3. AI Tester Persona / Metric Routing Specification

## Integration Verdict

```text
GENRE_CORE_MASTER_INDEX_v0.2

Status:
INTEGRATION_BASELINE / GSC SYNCED

Approved Genre Baselines:
9

Router Readiness:
READY_WITH_BOUNDED_EVIDENCE

Active Independent GSC:
0

Retired Historical GSC:
3

Routing Specialization:
2

Primary Remaining Integration Risk:
- Universal / Genre Double Penalty
- RPG / Action Evidence Breadth
- Micro / Small Scale Evidence Breadth
```

최종 실행 원칙:

```text
Mechanism
↓
Genre Routing
↓
Universal Parent
↓
Genre Core / Candidate
↓
Deduplication
↓
Scale Routing
↓
Active Scale Handoff
↓
Optional GSC Check
↓
Routing Specialization Hint
↓
Dynamic Reviewer Set
```

현재 `Active Independent GSC = 0`이므로 Optional GSC Check는 Parent + Handoff가 충분한지 확인하는 Guardrail로 작동한다.

`Genre Tag → 모든 Rule Load` 방식으로 돌아가지 않는다.
