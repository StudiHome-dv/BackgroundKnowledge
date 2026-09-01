# UNIVERSAL_CORE_CONSOLIDATION_v0.1

**Studio OS — Universal Core Consolidation & Parent Hierarchy**  
**Status:** `APPROVED_AS_UNIVERSAL_CONSOLIDATION_BASELINE`  
**Purpose:** `Universal Parent Audit / Genre Specialization Hierarchy / Layer Ownership / Double-Penalty Reduction`  
**Studio Core:** `Studio_OS_Evidence_Based_Core_Extraction_v0.3.md`  
**Genre Router:** `GENRE_CORE_MASTER_INDEX_v0.2.md`  
**Scale Router:** `SCALE_CORE_BASELINE_v0.2.md`  
**Genre × Scale:** `GENRE_SCALE_CORE_INTEGRATION_v0.1_APPROVED.md`  
**Canonical GSC Sync:** `GSC_CANONICAL_CONSOLIDATION_v0.1.md`  
**Canonical Change Policy:** `No source overwrite in this document. Required changes are recorded under CANONICAL_SYNC_REQUIRED.`  
**Next if approved:** `Canonical Universal Source Sync`

---

# 1. Executive Summary

이번 Consolidation의 핵심 결론은 다음과 같다.

1. **현재 Universal Design Core 5개를 유지한다.**
   - `UC-DESIGN-001` — KEEP PROVISIONAL / STRENGTHEN
   - `UC-DESIGN-002` — KEEP PROVISIONAL / STRENGTHEN BOUNDARY
   - `UC-DESIGN-003` — KEEP PROVISIONAL / STRENGTHEN
   - `UC-DESIGN-004` — KEEP PROVISIONAL / REFRAME
   - `UC-DESIGN-005` — KEEP PROVISIONAL / STRENGTHEN

2. **`UC-DESIGN-006`은 승격하지 않는다.**
   - Status: `KEEP AS CANDIDATE`
   - Audit: `REFRAME TITLE + RULE`
   - Canonical Title: `Progression Should Match Its Intended Promise`
   - 이유: RPG / Deck / Management / Roguelike에서 Progression이 Decision Space를 바꾸는 Mechanism은 반복되지만, `Vertical Power / Mastery Reward` 자체가 유효한 Product Promise라는 Counter Evidence가 강하다.
   - 따라서 “Progression은 반드시 새 결정을 만들어야 한다”가 아니라 **Progression이 어떤 Promise를 주장하는지에 따라 검증 질문이 달라져야 한다.**

3. **신규 Universal Design Core는 `0개`가 가장 적절하다.**
   - Failure Attribution
   - Recovery
   - Identity / Differentiation
   - Complexity / Compression
   모두 Cross-Genre Pattern은 존재하지만 현재 Parent 구조보다 새 UC를 만드는 편이 Rule 수와 중복을 증가시킨다.

4. **Failure Attribution은 새 UC가 아니다.**
   - `UC-DESIGN-005`는 이미 “의도한 판단 수행”뿐 아니라 “실패 원인을 학습할 수 있는 정보”까지 포함한다.
   - Action / Strategy / Roguelike / Simulation에서 반복되는 Failure Attribution은 `UC-DESIGN-005`의 **Outcome-time Learnability / Causal Attribution sub-mechanism**으로 정리하는 편이 더 정확하다.
   - `GC-ACTION-003`은 Action에서의 execution-specific cause taxonomy와 짧은 feedback loop라는 residual이 있으므로 Genre Candidate로 남긴다.

5. **Recovery도 독립 UC로 만들지 않는다.**
   - Management의 Loss Recovery
   - Strategy의 Recovery Window
   - Action의 Error Propagation / Recovery
   - Deduction의 missed-clue recovery
   는 모두 “Recovery”라는 단어를 쓰지만 동일 Design Mechanism은 아니다.
   - Recovery는 상황에 따라:
     - `UC-DESIGN-004`의 Response Agency
     - `UC-DESIGN-003`의 Consequence → Next Decision
     - Genre-specific Failure Structure
     아래에서 처리한다.

6. **Identity / Differentiation도 Universal Core로 승격하지 않는다.**
   - Deck Build Identity = future card value / synergy commitment.
   - Roguelike Run Identity = path dependence.
   - RPG Character Identity = persistent capability / role.
   - Narrative Identity = fictional self-expression / roleplay.
   - 공통 명사는 같지만 Mechanism이 다르다.
   - 일부는 `UC-DESIGN-002/003`으로 환원되며 Narrative self-expression은 별도 residual이다.

7. **Complexity / Compression도 단일 Universal Design Core로 만들지 않는다.**
   - Strategy compression
   - Simulation abstraction
   - Management responsibility level
   - Action minimal input
   - Solo production scope
   는 각각:
     - player-facing information complexity
     - causal model complexity
     - responsibility granularity
     - input complexity
     - production complexity
   를 다룬다.
   - `Relevance-preserving abstraction`이라는 Cross-Genre Pattern은 보이지만 현재는 Strategy / Simulation Evidence에 편중되어 있어 UC 승격하지 않는다.

8. **`UC-DESIGN-004`는 Canonical Rule wording Reframe이 필요하다.**
   - 현재 Title은 `Uncertainty Requires Response Agency`인데 Canonical Rule은 RNG에 좁게 쓰여 있다.
   - Deck RNG와 Strategy reserve evidence를 함께 설명하려면 다음 수준으로 넓히는 것이 적절하다.

```text
중요한 결과가 플레이어가 직접 통제할 수 없는 불확실성에 크게 의존할수록,
Preparation / Manipulation / Avoidance / Reserve / Recovery 중
하나 이상의 의미 있는 Response Agency가 존재하는지 평가한다.
```

   - 단 deterministic telegraph / 모든 Action threat를 자동 포함하지 않는다.

9. **`UC-DESIGN-005`는 새 Rule이 아니라 Substructure를 명확히 해야 한다.**

```text
Decision-time Actionability
+
Outcome-time Learnability / Attribution
```

   - Management Diagnosis
   - Strategy Prediction
   - Simulation Causal Diagnosis
   - Action Threat Readability
   - Action Failure Attribution
   이 한 Parent 아래에서 중복 감점 없이 작동한다.
   - Deduction Inference Ownership은 여기에 흡수하지 않는다.

10. **Narrative Recontextualization은 `UC-DESIGN-002`와 완전 병합하지 않는다.**
    - Mechanical Value Shift와 Narrative Meaning Shift는 관련되지만 동일 Mechanism이 아니다.
    - `GC-NARR-009`는 `UC-DESIGN-002`와 `GC-NARR-001`의 경계에 있는 specialization / merge candidate로 유지.
    - `GC-NARR-001`은 독립 Narrative Core로 유지한다.

11. **`SC-SOLO-001 — Risk-first Prototype`은 Validation Parent 가능성이 매우 높지만 이번 단계에서 Scale Core를 retire하지 않는다.**
    - 일반 원칙:
      > Highest-uncertainty / highest-impact claim을 최소 실행 모델로 먼저 검증한다.
    - Solo residual:
      > No Parallel Capacity 때문에 잘못된 prototype breadth의 opportunity cost가 더 크다.
    - 현재 Library는 Solo/Micro production evidence가 강하고 larger-team direct comparison은 부족하다.
    - 따라서 `RECLASSIFICATION CANDIDATE → Validation Methodology Parent + Solo Amplification`으로 기록하고 Canonical Status는 당장 바꾸지 않는다.

12. **`SC-SOLO-004 — Never Copy Post-success Scope`도 Reference Analysis Parent 가능성이 높지만 즉시 이동하지 않는다.**
    - 일반 원칙은 team size와 무관하게 타당해 보인다.
    - 그러나 현재 direct evidence가 Layer 3 Solo/Micro에 편중되어 있다.
    - `RECLASSIFICATION CANDIDATE → Reference Analysis Methodology + Solo Amplification`으로 기록한다.

13. **Universal Reviewer Default Set은 5개를 유지한다.**
    - `UC-DESIGN-001~005`
    - 단 모두 Applicability Gate를 먼저 통과해야 한다.
    - `UC-DESIGN-006`은 Progression이 실제 Product Promise일 때만 conditional diagnostic로 로드한다.

14. Consolidation 후 Parent 구조는 다음으로 정리된다.

```text
Project Mechanism
↓
Universal Applicability
↓
Universal Parent
↓
Genre Specialization / Residual
↓
Scale
↓
Handoff
↓
Optional GSC
↓
ONE ROOT ISSUE
↓
ONE SEVERITY
↓
Validation Handoff
```

15. **Canonical Source Sync가 필요하다.**
    - `UC-DESIGN-004` wording Reframe
    - `UC-DESIGN-005` two-phase substructure
    - `UC-DESIGN-006` promise-conditional Reframe
    - Genre Master의 Parent / Specialization / Failure Attribution mapping
    - SC-SOLO-001/004 Layer Ownership metadata
    를 다음 Source Sync에서 반영해야 한다.
    - 이번 문서는 Source를 직접 변경하지 않는다.

---

# 2. Universal Layer Purpose

Universal Core는:

> **모든 게임에 강제로 적용하는 공통 Checklist**

가 아니다.

정확한 목적은:

> **서로 다른 Genre에서 반복되는 동일 Mechanism을 하나의 Parent Issue로 묶고, Genre-specific Trigger / Verb / State / Failure Mode / Reviewer Action은 Child specialization으로 보존하는 것**

이다.

따라서 Universal Layer의 성공 기준은:

```text
Universal Rule 수 증가
```

가 아니라:

```text
Duplicate Reviewer Question 감소
+
Parent / Child 책임 분리
+
Severity 중복 제거
```

다.

---

# 3. Canonical Source Hierarchy

이번 Consolidation은 다음 Source ownership을 유지한다.

## Tier 1 — Universal / Scale / Historical GSC

`Studio_OS_Evidence_Based_Core_Extraction_v0.3.md`

소유:
- `UC-DESIGN-001~006`
- `SC-SOLO-*`
- Validation Core
- Historical retired GSC

## Tier 2 — Genre Routing / Parent Map

`GENRE_CORE_MASTER_INDEX_v0.2.md`

소유:
- 9 Genre routing
- Universal Parent → Genre Specialization
- Double Penalty rule
- GSC optional layer
- Scale / Handoff loading sequence

## Tier 3 — Genre Canonical Rule

각 Approved Genre Baseline 9개.

Child Rule / Counter Evidence / Boundary를 판단할 때 Master 요약만으로 결정하지 않고 해당 Genre source까지 내려간다.

## Tier 4 — Scale Layer

`SCALE_CORE_BASELINE_v0.2.md`

특히:
- `SC-SOLO-001`
- `SC-SOLO-004`
의 Layer Ownership Audit를 사용한다.

## Tier 5 — Cross-layer Integration

- `GENRE_SCALE_CORE_INTEGRATION_v0.1_APPROVED.md`
- `GSC_CANONICAL_CONSOLIDATION_v0.1.md`

GSC retirement는 이번 단계에서 재판단하지 않는다.

---

# 4. Universal Core Definition

Universal Design Core는 최소 다음을 만족해야 한다.

1. 최소 2개 독립 Genre에서 같은 Mechanism.
2. 가능하면 3개 이상.
3. 같은 단어 / Feature가 아니라 같은 Cause → Decision 구조.
4. Genre 명사를 제거해도 Rule이 의미 있게 남음.
5. Parent를 만들면 Reviewer 질문 수 / 중복 Severity가 실제 감소.
6. Counterexample / Product Promise boundary가 존재.
7. Validation path가 있음.
8. Child residual을 삭제하지 않아도 됨.

다음은 Universal 근거가 아니다.

```text
여러 Genre 문서에 "Recovery"라는 단어가 있다.
```

필요한 것은:

```text
Recovery가 같은 Trigger,
같은 Player problem,
같은 Reviewer Decision
을 만드는가?
```

다.

---

# 5. Promotion / Reduction Tests

각 Current / New Candidate에 다음을 적용한다.

## A. Cross-Genre Independence

서로 다른 Genre에서 같은 Mechanism이 반복되는가?

## B. Genre Removal Test

Genre 명사를 제거해도 Rule이 성립하는가?

## C. Parent Value Test

Parent가 실제 질문 수 / issue duplication을 줄이는가?

## D. Child Residual Test

Genre-specific:
- Trigger
- Verb
- State
- Failure mode
- execution window
- inference ownership
등이 남는가?

## E. Counterexample Test

특정 Product Promise에서 Rule이 약화되는가?

## F. Validation Test

Machine / Simulation / Player Telemetry / Human 중 검증 경로가 존재하는가?

## G. Evidence Independence Test

여러 Genre 문서가 같은 Reference 한두 개를 반복 인용한 것은 독립 Evidence로 과대계산하지 않는다.

---

# 6. Current Universal Registry

| ID | Current Status | Current Confidence | Audit Decision | Final Recommendation |
|---|---|---:|---|---|
| `UC-DESIGN-001` | PROVISIONAL CORE | VERY HIGH | `STRENGTHEN` | **KEEP PROVISIONAL** |
| `UC-DESIGN-002` | PROVISIONAL CORE | HIGH | `STRENGTHEN BOUNDARY` | **KEEP PROVISIONAL** |
| `UC-DESIGN-003` | PROVISIONAL CORE | HIGH | `STRENGTHEN` | **KEEP PROVISIONAL** |
| `UC-DESIGN-004` | PROVISIONAL CORE | HIGH | `REFRAME` | **KEEP PROVISIONAL — wording sync required** |
| `UC-DESIGN-005` | PROVISIONAL CORE | HIGH | `STRENGTHEN / SUBSTRUCTURE` | **KEEP PROVISIONAL** |
| `UC-DESIGN-006` | KEEP AS CANDIDATE | MEDIUM-HIGH | `REFRAME TITLE + RULE` | **KEEP CANDIDATE — no promotion** |

## Current Universal Count after Audit

```text
Provisional Universal Design Core:
5

Universal Design Candidate:
1

New Universal Design Core:
0
```

---

# 7. UC-DESIGN-001 Audit — Consequence Density over Input Count

## Current

`PROVISIONAL CORE — VERY HIGH`

## Audit Decision

`STRENGTHEN`

## Why It Survives Universal Test

Direct source evidence already demonstrates:
- Reigns
- Papers, Please
- Loop Hero

에서 적은 입력이 복수 상충 결과를 만들 때 Decision Depth가 생긴다는 공통 Mechanism을 보여준다.

Genre Layer에서도:
- Management priority conflict
- automation
- Deck content-count anti-pattern
- Strategy option consequence
- Action minimal-input specialization

이 같은 Parent를 반복한다.

## Action Specialization

`GC-ACTION-007 — Removed Input Must Leave Meaningful Action Agency Elsewhere`

는 자연스러운 Child다.

Parent:

> 입력 수가 Depth가 아니다.

Action residual:

> 자동화된 직접 Input 대신 Timing / Movement / Position / Target 등 다른 consequence-bearing Action axis가 남아야 한다.

Parent만으로는 `무슨 Action axis가 남아야 하는가`까지 충분하지 않으므로 Child residual을 유지한다.

## Management Specialization Candidate

`GC-MGMT-003 — Automation Should Remove Execution, not Decisions`

도 같은 Parent와 매우 가깝다.

Management residual:
- priority setting
- exception handling
- responsibility level

을 보존한다.

## Counterexample / Boundary

- Rhythm
- Precision Action
- Fighting
- execution mastery

처럼 Input / execution vocabulary 자체가 Product Value인 경우.

이 경우도 `버튼이 많으면 깊다`는 주장은 자동으로 성립하지 않지만,
Input Complexity를 무조건 제거하는 것도 잘못이다.

## Final

```text
KEEP PROVISIONAL
STRENGTHEN Parent hierarchy
Canonical Rule wording change: NOT REQUIRED
```

---

# 8. UC-DESIGN-002 Audit — Contextual Value Shift

## Current

`PROVISIONAL CORE — HIGH`

## Audit Decision

`STRENGTHEN BOUNDARY`

## Strong Specializations

### Deckbuilding
`GC-DECK-001 — Contextual Card Value`

카드 가치가:
- build
- encounter
- phase
에 따라 변한다.

### Management
`GC-MGMT-006 — Routine Must Be Recontextualized`

같은 관리 Verb가:
- rule
- demand
- state
- constraint
변화 때문에 다른 priority를 요구한다.

### Roguelike
`GC-ROGUE-003 — Meaningful Run Variation Must Force Adaptation`

Seed / reward / route 변화가 실제 전략 가치를 바꿀 때만 의미 있는 variation.

## Narrative Audit

`GC-NARR-009 — Repeated Core Verbs Need Narrative Recontextualization`

은 UC-DESIGN-002와 관련되지만 완전히 동일하지 않다.

Mechanical Parent:

```text
Context changes option value
```

Narrative residual:

```text
Context changes human / fictional meaning
```

그리고 `GC-NARR-001 — State-reactive Recontextualization over Branch Count`는:
- state-reactive narrative
- history / character / world meaning
이라는 독립 Narrative Mechanism을 가진다.

따라서:

```text
UC-DESIGN-002
≠
GC-NARR-001 전체 흡수
```

## Boundary

현재 Canonical Boundary:

> Replayability가 Product Promise일 때 적용.

유지한다.

- Obra Dinn형 one-shot deduction
- short authored experience

는 낮은 replayability 자체가 결함이 아니다.

## Final

```text
KEEP PROVISIONAL
No broad Narrative merge
GC-NARR-009 = dual relation:
  UC-DESIGN-002 related specialization
  + GC-NARR-001 merge/sub-rule candidate
```

---

# 9. UC-DESIGN-003 Audit — Consequence-to-Next-Decision Coupling

## Current

`PROVISIONAL CORE — HIGH`

## Audit Decision

`STRENGTHEN`

## Key Clarification

핵심은:

```text
State persists
```

가 아니다.

핵심은:

```text
State persists
↓
future option / priority / risk / availability changes
↓
next decision changes
```

이다.

## Strong Genre Specializations

### Management
`GC-MGMT-004 — Persistent State Must Reprioritize`

부상 / 상태가 다음:
- assignment
- treatment
- resource
- team composition
을 바꾼다.

### Strategy
- `GC-STRAT-001 — Key Strategic Decisions Should Change Future Option Value`
- `GC-STRAT-002 — Decision-Relevant State Changes Must Trigger Re-evaluation`

Strategy residual은 planning / future option value / re-evaluation이다.

### Simulation
`GC-SIM-002 — System States Should Propagate through Causal Dependencies`

Simulation residual은 Player choice가 아니라 World causal propagation 자체다.

### RPG
`GC-RPG-005 — Persistent Character Consequences Should Change Future Play`

RPG residual은:
- character identity
- capability
- availability
- risk
에 persistent state가 반영되는가다.

### Roguelike
`GC-ROGUE-004 — Run Choices Must Create Path Dependence`

Run state / investment가 future choice value를 바꾼다는 점에서 같은 Parent에 매우 가깝지만:
- reset boundary
- run identity
- pivot / lock-in
이라는 Roguelike residual이 존재한다.

## Narrative

`GC-NARR-003 — Delayed Consequences Need Persistent State and Causal Legibility`

두 Parent에 걸친다.

- persistence → future consequence = `UC-DESIGN-003`
- causal understanding = `UC-DESIGN-005`

Narrative residual:
- delayed authored payoff
- story memory
- agency without perfect foresight

따라서 하나의 Universal에 완전히 merge하지 않는다.

## Final

```text
KEEP PROVISIONAL
STRENGTHEN:
Persistence alone is not value.
Future decision effect is the parent test.
```

---

# 10. UC-DESIGN-004 Audit — Uncertainty Requires Response Agency

## Current

`PROVISIONAL CORE — HIGH`

Title은 `Uncertainty`지만 Canonical Rule wording은 RNG에 좁게 작성되어 있다.

## Audit Decision

`REFRAME — KEEP PROVISIONAL`

## Why Reframe

Direct Deck Evidence:
- Dicey Dungeons
- FTL
- Slay the Spire

는 RNG manipulation / preparation / recovery를 지지한다.

Strategy:
`GC-STRAT-009 — Reserve / Flexibility Can Be Strategic Value`

는 uncertainty가 있을 때:
- reserve
- flexible position
- unused option
자체가 response agency가 됨을 보여준다.

따라서 Parent Mechanism은 RNG 자체보다 넓다.

## Proposed Canonical Reframe

> **중요한 결과가 플레이어가 직접 통제할 수 없는 불확실성에 크게 의존할수록, Preparation / Manipulation / Avoidance / Reserve / Recovery 중 하나 이상의 의미 있는 Response Agency가 존재하는지 평가한다.**

## What It Does NOT Absorb

### Deterministic Action Telegraph
`GC-ACTION-002`의 모든 Threat Readability는 UC-DESIGN-004가 아니다.

이미 공개된 deterministic threat에서:
- timely cue
- response window
문제는 주로 `UC-DESIGN-005 + Action specialization`.

### Management Future Pressure
Known deadline / forecast는 uncertainty가 아닐 수 있다.

Management planning 자체를 UC004에 억지로 넣지 않는다.

## Recovery Position

Recovery는 UC004의 가능한 response path 중 하나다.

하지만 모든 Recovery Core가 UC004에 흡수되지는 않는다.

## Counterexample

- Chaos fantasy
- party game
- spectacle randomness
- 일부 horror uncertainty

에서 unpredictability 자체가 Product Value일 수 있다.

## Canonical Sync

`REQUIRED`

Status는 Provisional 유지.  
Rule wording만 Title / actual Parent coverage와 맞춘다.

---

# 11. UC-DESIGN-005 Audit — Actionable Information

## Current

`PROVISIONAL CORE — HIGH`

Canonical Rule은 이미:
- intended decision 수행
- failure cause 학습

두 축을 포함한다.

## Audit Decision

`STRENGTHEN / FORMALIZE SUBSTRUCTURE`

새 UC로 split하지 않는다.

## Parent Substructure

### A. Decision-time Actionability

질문:

> 플레이어가 현재 의도된 판단을 수행할 수 있을 만큼 필요한 State / Trend / Threat / Intent를 알 수 있는가?

Genre specialization:
- `GC-MGMT-007` — Diagnosis / Priority
- `GC-STRAT-004` — Prediction / Commitment
- `GC-ACTION-002` — Threat cue → response window

### B. Outcome-time Learnability / Attribution

질문:

> 중요한 결과가 발생한 뒤 플레이어가 무엇 때문에 그런 결과가 나왔는지 이해하고 다음 행동을 수정할 수 있는가?

Genre specialization / pattern:
- `GC-SIM-004` — Major outcome causal diagnosis
- `GC-ACTION-003` — execution failure attribution
- Strategy failure attribution
- `GC-ROGUE-006` — failure → next-run hypothesis
- Management diagnosis / failure-cause telemetry

## Deduction Exception

Deduction은 정보가 중요하더라도 다음은 별도다.

### `GC-DEDUCT-001`
UI는 Memory / Search를 외부화할 수 있지만 Inference는 player-owned.

### `GC-DEDUCT-003`
Evidence relation이 Conclusion을 논리적으로 reachable하게 해야 함.

### `GC-DEDUCT-004`
Validation design이 reasoning을 leak하지 않아야 함.

### `GC-DEDUCT-005`
Evidence sufficiency와 human accessibility는 별도.

따라서:

```text
Information exists / readable
≠
Player owns inference
```

## Human / Machine Boundary

```text
Cause trace exists
≠
Player understands cause
```

```text
Threat cue exists
≠
Player recognizes threat
```

```text
AI state access
≠
Player knowledge
```

## Final

```text
KEEP PROVISIONAL
No new Failure Attribution UC
Formalize:
  Decision-time Actionability
  Outcome-time Learnability / Attribution
```

---

# 12. UC-DESIGN-006 Audit — Progression Should Match Its Intended Promise

## Current

`KEEP AS CANDIDATE — MEDIUM-HIGH`

Former Title:

`Progression Should Alter Decisions`

## Audit Decision

`REFRAME — KEEP CANDIDATE`

## Canonical Title Recommendation

`Progression Should Match Its Intended Promise`

## Supporting Cross-Genre Evidence

### RPG
`GC-RPG-001 — Character Investment Should Change Available Solutions`

Character-build promise에서는:
- capability
- solution
- role value
가 progression으로 달라져야 한다는 strong specialization.

### Management
`GC-MGMT-008 — Growth Must Transform Constraints, not Erase Management`

Growth가 모든 management question을 제거하면 decision collapse 가능.

### Deckbuilding
`GC-DECK-012 — Vertical Power vs Decision Preservation`

Power explosion은 유효할 수 있지만 reward / encounter decision이 사라지는 시점을 별도 점검.

### Roguelike
`GC-ROGUE-010 — Meta Progression Type Must Match Product Promise`

Vertical / Horizontal / Knowledge meta를 구분해야 함.

## Counter Evidence

- Vampire Survivors-like Vertical Power
- Power Fantasy RPG
- 일부 Tycoon / Creative Sandbox

에서:
> 더 강해지는 느낌
자체가 정상 reward.

## Problem with Current Title

`Progression Should Alter Decisions`를 절대 규칙처럼 읽으면
Vertical Power를 과도하게 감점할 수 있다.

## Proposed Reframe

> **Progression이 Build / Role / Capability / Strategic Expansion을 Product Promise로 주장한다면 실제 Choice Space나 Solution Value를 변화시키는지 검토한다. Progression의 주 목적이 Vertical Power / Mastery Reward라면 Decision Expansion을 강제하지 않되, 다른 Core Decision을 의도치 않게 제거하는지는 별도로 확인한다.**

## Promotion Decision

현재는 Provisional로 승격하지 않는다.

이유:
- Product Promise conditionality가 큼.
- Vertical growth의 정당한 Counterexample가 강함.
- RPG evidence breadth 자체가 제한적.
- 실제 player motivation / progression meaning 비교 evidence 부족.

## Final

```text
KEEP AS CANDIDATE
REFRAME
Confidence:
MEDIUM-HIGH 유지
```

---

# 13. Universal Reclassification Candidate Audit

| Genre Candidate | Current Relation | Universal Audit | Final Treatment |
|---|---|---|---|
| `GC-ACTION-003` | Universal Reclassification Candidate — Failure Attribution | UC005가 이미 outcome learnability를 소유 | **Keep Action Candidate as UC005 outcome-attribution specialization; no new UC** |
| `GC-STRAT-004` | Possible UC005 sub-rule | Prediction / commitment residual 존재 | **Genre Specialization 유지** |
| `GC-SIM-004` | Possible UC005 sub-rule | Causal-model diagnosis residual 존재 | **Genre Specialization 유지** |
| `GC-ACTION-002` | UC005 strengthening | Response-window / timing residual 존재 | **Genre Specialization 유지** |
| `GC-ACTION-007` | UC001 strengthening | Removed-input / residual action-axis residual | **Genre Specialization 유지** |
| `GC-RPG-001` | UC006 strengthening | Persistent character investment / solution residual | **Genre Specialization Candidate 유지** |
| `GC-RPG-005` | UC003 overlap | Character persistence / role / availability residual | **Genre Specialization Candidate 유지** |

## General Rule

Parent가 존재한다고 Child를 삭제하지 않는다.

Child가 유지되는 이유는:

> Parent가 발견하는 Root Issue는 같아도 Genre-specific Reviewer Action이 다르기 때문.

---

# 14. Failure Attribution Audit

## Question

> 실패를 학습으로 연결하려면 Player가 failure cause를 actionable decision / execution / state chain과 연결할 수 있어야 하는가?

## Observed Cross-Genre Pattern

### Action
`GC-ACTION-003`
- telegraph miss
- position
- dodge timing
- commitment
- target
- control mismatch

### Strategy
Strategy Inclusion / Human validation에서:
> 어떤 판단 또는 계획을 바꿨어야 했는가?
를 요구.

### Roguelike
`GC-ROGUE-006`
> 다음 Run에서 무엇을 바꿀 것인가?
라는 hypothesis generation.

### Simulation
`GC-SIM-004`
중요한 outcome의 cause chain diagnosis.

### Management
Diagnosis / bottleneck / recovery telemetry가 failure-cause 이해와 연결.

## Why No New UC

`UC-DESIGN-005` Canonical Rule에 이미:

> 실패 원인을 학습할 수 있을 만큼의 정보

가 포함되어 있다.

새 UC를 만들면:

```text
UC-DESIGN-005
+
UC-FAILURE-ATTRIBUTION
+
GC-ACTION-003
+
GC-SIM-004
```

가 같은 Root Issue를 중복 생성할 가능성이 높다.

## Design / Validation Split

### Design
Game이 causal signal / feedback / inspectability를 제공하는가?

### Validation
Tester / log가:
- formal cause
- perceived cause
를 별도로 기록하는가?

둘은 별도 Layer다.

## Decision

```text
Status:
CROSS_GENRE_PATTERN

Parent:
UC-DESIGN-005 — Outcome-time Learnability / Attribution

New UC:
NO
```

---

# 15. Recovery Audit

## Observed

- `GC-MGMT-002 — Loss Needs Recovery Structure`
- `GC-STRAT-007 — Recovery Decision after Error`
- `GC-ACTION-006 — Error Propagation / Recovery`
- Simulation cascade recovery
- Deduction missed-clue recovery
- Roguelike reset / restart structures

## Same Word, Different Mechanism

### Management
Loss가 다음 allocation / repair / replacement decision을 만든다.

주 Parent:
- `UC-DESIGN-003`
- 일부 `UC-DESIGN-004`

### Strategy
Error 이후 sacrifice / retreat / reposition의 decision window.

주 Parent:
- `UC-DESIGN-004` related
- Strategy-specific recoverability.

### Action
Execution error 이후 input agency / stunlock / recovery window.

Action-specific timing mechanism.

### Deduction
Critical clue miss가 unrecoverable dead-end를 만드는가.

Information accessibility / puzzle graph mechanism.

### Roguelike
Failure가 terminal run reset이어도 정상일 수 있다.

즉 recovery가 항상 run 내부 continuing state일 필요는 없다.

## Decision

```text
New Universal Core:
NO

Status:
CROSS_GENRE_PATTERN

Routing:
- UC-DESIGN-004 when recovery is a response to uncertainty/adverse state
- UC-DESIGN-003 when persistent loss should create a next decision
- Genre Core when timing / reset / inference graph is genre-specific
```

---

# 16. Identity / Differentiation Audit

## Observed Labels

- Deck Build Identity
- Roguelike Run Identity
- RPG Character / Build Identity
- Narrative Roleplay Identity

## Mechanism Comparison

### Deck
이전 카드 선택이 future reward / synergy value를 바꿈.

Primary parents:
- UC002
- UC003

### Roguelike
run choices create path dependence.

Primary parent:
- UC003
- UC002 related

### RPG
persistent capability / role / equipment / skill formation.

Primary:
- UC006 candidate
- UC003 related

### Narrative
fictional / moral self-expression.

Mechanism:
- meaning
- relationship
- authored consequence
- roleplay.

Mechanical build identity와 동일하지 않다.

## Decision

```text
New Universal Core:
NO

Status:
CROSS_GENRE_PATTERN

Reason:
"Identity" is an outcome label, not a single shared mechanism.
```

---

# 17. Complexity / Compression Audit

## Terms that must remain separate

```text
Player-facing Complexity
Production Complexity
State Complexity
Input Complexity
Content Complexity
Information Complexity
```

## Related Genre Findings

### Strategy
`GC-STRAT-011 — Strategic Compression Should Preserve Decision-relevant State`

### Simulation
- `GC-SIM-001 — Selective Simulation`
- abstraction should preserve experience-relevant causality pattern.

### Management
Responsibility level can limit management granularity.

### Action
Minimal input can preserve agency.

### Narrative
State-reactive recontextualization can reduce branch breadth.

### Scale
`SC-SOLO-002` concerns production complexity, not player-facing design complexity.

## Cross-Genre Residual

Strategy + Simulation에서 다음 Pattern은 보인다.

> Representation / model detail을 줄여도 decision-relevant state / experience-relevant causality를 보존해야 한다.

하지만:
- Strategy / Simulation Evidence에 편중.
- Management / Action / Narrative는 다른 compression axis.
- Scale complexity를 섞으면 Layer Error.

## Decision

```text
New Universal Core:
NO

Cross-Genre Pattern:
Relevance-preserving Abstraction / Compression

Promotion Blocker:
Evidence breadth + layer ambiguity
```

---

# 18. SC-SOLO-001 Layer Ownership Audit

## Current

`SC-SOLO-001 — Risk-first Prototype`  
`PROVISIONAL CORE — VERY HIGH`

Scale v0.2:

`UNIVERSAL_VALIDATION_PARENT_CANDIDATE`

## General Mechanism

> 가장 높은 불확실성 × 가장 높은 실패 비용을 가진 claim부터 최소 실행 모델로 검증한다.

이 원칙은 논리적으로 Solo에만 국한되지 않는다.

## Solo-specific Residual

Solo에서는:
- no parallel capacity
- context switching
- one-owner opportunity cost

때문에 잘못된 prototype breadth가 다른 모든 작업을 직접 밀어낸다.

## Evidence Boundary

현재 strong production evidence는:
- Buckshot Roulette
- Thronefall
- Jam → product cases
등 Solo/Micro에 집중.

Large team에서의 direct comparative evidence는 부족.

## Audit Decision

```text
Canonical Status:
KEEP CURRENT SC-SOLO-001 for now

Layer Ownership:
RECLASSIFICATION CANDIDATE

Proposed Parent:
Universal Validation Methodology

Solo Residual:
Opportunity-cost amplification under no parallel capacity
```

## Important

`VAL-004 — Structural Pre-validation First`와 자동 merge하지 않는다.

VAL-004는:
- validation stage order
를 말한다.

SC-SOLO-001 general parent candidate는:
- which risk to test first
를 말한다.

관련되지만 동일 Rule은 아니다.

---

# 19. SC-SOLO-004 Layer Ownership Audit

## Current

`SC-SOLO-004 — Never Copy Post-success Scope`  
`PROVISIONAL CORE`

Scale v0.2:

`REFERENCE_ANALYSIS_PARENT_RECLASSIFICATION_CANDIDATE`

## General Mechanism

Reference를 비교할 때:
- Prototype
- early commercial
- 1.0
- current
- post-success update

를 구분해야 초기 Production viability를 왜곡하지 않는다.

이 원칙 자체는 Solo에 한정될 이유가 약하다.

## Solo Residual

작은 팀에서:
- capacity gap
- opportunity cost
- post-success expansion imitation
의 피해가 더 직접적.

## Evidence Boundary

현재 Layer 3가 Solo/Micro production reference에 강하다.

Cross-scale production benchmarking evidence는 부족.

## Audit Decision

```text
Canonical Status:
KEEP CURRENT SC-SOLO-004 for now

Layer Ownership:
RECLASSIFICATION CANDIDATE

Proposed Parent:
Reference Analysis / Production Benchmarking Methodology

Solo Residual:
Post-success benchmark misuse is more dangerous under limited capacity.
```

---

# 20. Validation Layer Boundary

Universal Design과 Validation Methodology를 섞지 않는다.

현재 Validation Core:

- `VAL-001 — Machine Structural Evidence ≠ Human Experience`
- `VAL-002 — Hypothesis / Metric / Criteria Separation`
- `VAL-003 — Evidence Accumulation`
- `VAL-004 — Structural Pre-validation First`

이들은 Game Design Rule이 아니다.

## Failure Attribution Example

### Design Layer
Player가 cause를 이해하고 행동을 수정할 수 있는 feedback인가?

### Validation Layer
Formal cause trace와 player-reported cause를 별도 Evidence로 수집했는가?

두 문장은 서로 다른 Owner를 가진다.

## Risk-first Prototype

`SC-SOLO-001`의 General Parent 후보 역시 Validation Methodology에 가깝지만:
- 현재는 reclassification candidate.
- 이번 문서에서 새로운 `VAL-*` ID를 만들지 않는다.

---

# 21. Reference Analysis Layer Boundary

이번 Consolidation에서 별도 Core Family를 만들지 않는다.

Registry:

```text
Candidate:
Never Copy Post-success Scope

Current Owner:
SC-SOLO-004

Layer Ownership:
REFERENCE_ANALYSIS_CANDIDATE

Potential Parent:
Reference Analysis / Production Benchmarking Methodology

Canonical Move:
DEFERRED — evidence / namespace sync required
```

Reference 성공 여부 / 현재 content count를 Design Quality와 동일시하지 않는 기존 Studio OS 원칙과도 일관된다.

---

# 22. Universal Parent Hierarchy

## UC-DESIGN-001 — Consequence Density

```text
UC-DESIGN-001
↓
GC-ACTION-007 — Removed Input must leave Action Agency
↓
Action-specific timing / movement / position residual

UC-DESIGN-001
↓
GC-MGMT-003 — Automation removes Execution, not Decisions
↓
Management priority / exception-handling residual
```

Deck `More Cards = Depth`와 같은 항목은 Parent routing example이지 별도 Universal child가 아니다.

---

## UC-DESIGN-002 — Contextual Value Shift

```text
UC-DESIGN-002
├─ GC-DECK-001 — Contextual Card Value
├─ GC-MGMT-006 — Routine Recontextualization
├─ GC-ROGUE-003 — Run Variation forces Adaptation
└─ GC-NARR-009 — Related specialization / dual parent candidate
                      ↓
                  GC-NARR-001 narrative meaning residual
```

`GC-NARR-001` 전체를 UC002에 merge하지 않는다.

---

## UC-DESIGN-003 — Consequence → Next Decision

```text
UC-DESIGN-003
├─ GC-MGMT-004 — Persistent State must Reprioritize
├─ GC-ROGUE-004 — Run Choices create Path Dependence
├─ GC-STRAT-001 — Strategic decisions change Future Option Value
├─ GC-STRAT-002 — State change triggers Re-evaluation
├─ GC-SIM-002 — State propagates through Causal Dependencies
├─ GC-RPG-005 — Persistent Character Consequence changes Future Play
└─ GC-NARR-003 — Partial parent: persistence / later consequence
```

---

## UC-DESIGN-004 — Uncertainty Response Agency

```text
UC-DESIGN-004
├─ GC-DECK-003 — Availability / RNG Control
├─ GC-STRAT-009 — Reserve / Flexibility
└─ Recovery Pattern — only when response to uncertainty/adverse state
```

모든 Recovery / Action Threat를 자동 child로 넣지 않는다.

---

## UC-DESIGN-005 — Actionable & Learnable Information

```text
UC-DESIGN-005

Decision-time Actionability
├─ GC-MGMT-007 — Diagnosis / Priority
├─ GC-STRAT-004 — Prediction / Commitment
└─ GC-ACTION-002 — Timely Threat Readability / Response Window

Outcome-time Learnability
├─ GC-SIM-004 — Causal Diagnosis
├─ GC-ACTION-003 — Execution Failure Attribution
├─ Strategy Failure Attribution pattern
└─ GC-ROGUE-006 — Next-run Hypothesis (related)
```

Deduction:
- `GC-DEDUCT-001/003/004` independent residual.
- `GC-DEDUCT-005` is related accessibility boundary, not inference ownership replacement.

---

## UC-DESIGN-006 — Progression Promise Candidate

```text
UC-DESIGN-006 CANDIDATE
├─ GC-RPG-001 — Character investment changes solutions
├─ GC-DECK-012 — Vertical power vs decision preservation [RELATED]
├─ GC-MGMT-008 — Growth transforms constraints [RELATED]
└─ GC-ROGUE-010 — Meta type matches promise [RELATED]
```

UC006가 안정화되기 전 Related findings를 전부 child로 강제하지 않는다.

---

# 23. Parent Coverage Matrix

Legend:
- `DIRECT` — current Universal source itself has strong direct evidence relevant to this Genre mechanism.
- `SPECIALIZATION` — explicit / strong Genre child.
- `RELATED` — adjacent mechanism; do not double-penalize automatically.
- `N/A` — normally not loaded without project-specific reason.
- `COUNTEREXAMPLE` — major product boundary evidence.

| Universal Parent | Deck | Mgmt | Rogue | Deduct | Narr | Strat | Sim | RPG | Action |
|---|---|---|---|---|---|---|---|---|---|
| `UC-001 Consequence Density` | RELATED | SPECIALIZATION | RELATED | N/A | RELATED | RELATED | RELATED | RELATED | SPECIALIZATION |
| `UC-002 Contextual Value` | SPECIALIZATION | SPECIALIZATION | SPECIALIZATION | COUNTEREXAMPLE / N/A | SPECIALIZATION* | RELATED | RELATED | RELATED | CONDITIONAL |
| `UC-003 Consequence → Next Decision` | RELATED | SPECIALIZATION | SPECIALIZATION | N/A | SPECIALIZATION | SPECIALIZATION | SPECIALIZATION | SPECIALIZATION | RELATED |
| `UC-004 Uncertainty Response` | SPECIALIZATION | RELATED | RELATED | N/A | RELATED | SPECIALIZATION | RELATED | RELATED | CONDITIONAL |
| `UC-005 Actionable Information` | RELATED | SPECIALIZATION | RELATED | RELATED / EXCEPTION | SPECIALIZATION | SPECIALIZATION | SPECIALIZATION | RELATED | SPECIALIZATION |
| `UC-006 Progression Promise` | RELATED | RELATED | RELATED | N/A | RELATED | N/A | N/A | SPECIALIZATION | CONDITIONAL |

`* Narrative`: `GC-NARR-009`은 specialization 성격이 있으나 `GC-NARR-001` 전체는 independent narrative residual.

## Matrix Interpretation

이 Matrix는 Universal 적용 강도를 자동 점수화하지 않는다.

먼저:

```text
Applicable?
YES / CONDITIONAL / N/A
```

를 판단한다.

---

# 24. Genre Specialization Registry

| Universal Parent | Genre Child / Pattern | Child Residual | Treatment |
|---|---|---|---|
| UC001 | `GC-ACTION-007` | direct input removal 후 timing/movement/position agency | KEEP SPECIALIZATION |
| UC001 | `GC-MGMT-003` | priority setting / exception handling | KEEP CANDIDATE SPECIALIZATION |
| UC002 | `GC-DECK-001` | card / build / encounter value | KEEP GENRE CORE |
| UC002 | `GC-MGMT-006` | routine → priority re-evaluation | KEEP GENRE CORE |
| UC002 | `GC-ROGUE-003` | seed/run variation → adaptation | KEEP GENRE CORE |
| UC002 | `GC-NARR-009` | human / narrative meaning shift | DUAL RELATION; possible merge into NARR001 |
| UC003 | `GC-MGMT-004` | reprioritization / allocation | KEEP GENRE CORE |
| UC003 | `GC-ROGUE-004` | run identity / path dependence | KEEP GENRE CORE |
| UC003 | `GC-STRAT-001/002` | planning / future option value | KEEP GENRE CORE |
| UC003 | `GC-SIM-002` | world causal propagation | KEEP GENRE CORE |
| UC003 | `GC-RPG-005` | character state / role / availability | KEEP CANDIDATE SPECIALIZATION |
| UC003 + UC005 | `GC-NARR-003` | delayed narrative payoff / causal memory | KEEP GENRE CORE |
| UC004 | `GC-DECK-003` | draw / availability manipulation | KEEP GENRE CORE |
| UC004 | `GC-STRAT-009` | reserve / flexibility | KEEP CANDIDATE SPECIALIZATION |
| UC005 | `GC-MGMT-007` | diagnosis / priority | KEEP GENRE CORE |
| UC005 | `GC-STRAT-004` | prediction / commitment | KEEP CANDIDATE SPECIALIZATION |
| UC005 | `GC-SIM-004` | causal-model diagnosis | KEEP CANDIDATE SPECIALIZATION |
| UC005 | `GC-ACTION-002` | threat cue / response window | KEEP CANDIDATE SPECIALIZATION |
| UC005 | `GC-ACTION-003` | execution failure cause | KEEP CANDIDATE SPECIALIZATION |
| UC005 related | `GC-DEDUCT-005` | accessibility vs sufficiency | KEEP DEDUCTION CANDIDATE |
| UC006 | `GC-RPG-001` | character investment / available solutions | KEEP CANDIDATE SPECIALIZATION |

---

# 25. Cross-Genre Pattern Registry

## Pattern — Failure Attribution

**Observed In:** Action / Strategy / Roguelike / Simulation / Management  
**Status:** `CROSS_GENRE_PATTERN`  
**Why Not New UC:** already covered by UC005 outcome-time learnability; direct Human evidence is uneven.  
**Runtime:** UC005 Root + Genre cause taxonomy.

---

## Pattern — Recovery as Continuing Decision

**Observed In:** Management / Strategy / Action / Deduction / Simulation  
**Status:** `CROSS_GENRE_PATTERN`  
**Why Not New UC:** different trigger / timing / terminality; routed through UC003/004 + Genre rules.

---

## Pattern — Identity through Path-dependent Differentiation

**Observed In:** Deck / Roguelike / RPG / Narrative  
**Status:** `CROSS_GENRE_PATTERN`  
**Why Not New UC:** identity is an outcome label; underlying mechanisms differ.

---

## Pattern — Relevance-preserving Abstraction / Compression

**Observed In:** Strategy / Simulation; adjacent Management / Action / Narrative  
**Status:** `CROSS_GENRE_PATTERN`  
**Why Not New UC:** evidence concentrated in Strategy/Simulation and complexity layers differ.

---

## Pattern — Progression Promise Fit

**Observed In:** RPG / Deck / Management / Roguelike  
**Status:** `CURRENT UC006 CANDIDATE REGION`  
**Why Not Promote:** Vertical Power counterexamples + conditional promise.

---

# 26. Double / Triple Penalty Registry

| Root Issue | Universal Parent | Genre Child | Runtime Treatment |
|---|---|---|---|
| Threat information cannot drive response | UC005 | `GC-ACTION-002` | Severity once; Action child adds cue→response-window check |
| Management data does not support diagnosis | UC005 | `GC-MGMT-007` | Severity once; child adds priority / capacity diagnosis |
| Strategy information does not change plan | UC005 | `GC-STRAT-004` | Severity once; child adds prediction / commitment |
| Simulation outcome has hidden cause | UC005 | `GC-SIM-004` | Severity once; child adds causal-chain diagnosis |
| Action failure is not learnable | UC005 | `GC-ACTION-003` | Severity once; child adds execution-cause taxonomy |
| Run variation does not change choices | UC002 | `GC-ROGUE-003` | Severity once; child adds seed / route / build adaptation |
| Card value is context-invariant | UC002 | `GC-DECK-001` | Severity once; child adds build / encounter context |
| Persistent management state does not change next priority | UC003 | `GC-MGMT-004` | Severity once |
| Persistent simulation state propagates but does not matter to player plan | UC003 | `GC-SIM-002` + project Genre | One root; simulation residual = causal propagation |
| RNG/availability has no player response | UC004 | `GC-DECK-003` | Severity once; deck child adds draw/pool intervention |
| Uncertainty consumes all resources with no flexibility | UC004 | `GC-STRAT-009` | Severity once; strategy child adds reserve/flexible-position test |

## Triple Penalty Example — Management × Simulation

잘못된 방식:

```text
UC-DESIGN-003 HIGH
+
GC-MGMT-004 HIGH
+
GC-SIM-002 HIGH
```

올바른 방식:

```text
ROOT ISSUE:
Persistent state does not create useful future decisions / causal consequences.

Universal:
UC-DESIGN-003

Management residual:
Does it reprioritize allocation?

Simulation residual:
Does state propagate through real causal dependencies?

Severity:
ONE
```

## Triple Penalty Example — Narrative Delayed Consequence

`GC-NARR-003`이:
- UC003 persistence
- UC005 causal learnability
두 Parent를 동시에 trigger할 수 있다.

두 Universal이 서로 다른 Root Cause일 때만 두 Issue로 분리한다.

예:
1. Flag persists but never changes later state → UC003.
2. Later consequence exists but player cannot connect cause → UC005.

동일 symptom 하나를 두 번 감점하지 않는다.

---

# 27. Universal Metric Classification

## UC-DESIGN-001

### Structural / Machine
- Action / Input Definition Count
- Outcome Axis Count
- State Delta by Action
- Distinct Decision Candidate Count

### Structural / model-dependent
- Consequence Conflict Count
- Consequence Density
- Decision-equivalence between actions

### Simulation
- Choice Concentration
- Action Usage Distribution
- Policy diversity under same state

### Player Telemetry
- Choice Distribution
- Repeated Command Rate
- Automation Override

### Human
- Decision Tension
- Perceived Agency

### Hybrid
- Meaningful Choice Quality

---

## UC-DESIGN-002

### Structural
- Context State Definitions
- Action / reward availability by context

### Structural / model-dependent
- Contextual Value Variance

### Simulation
- Same Persona / Different Context Policy Divergence
- Strategy Concentration by Phase / Seed
- Context-triggered Action Shift

### Player Telemetry
- Choice Rate by Context
- Build / route change

### Human
- Perceived Variety
- Replay Intent
- “같은 문제를 반복했다” perception

### Hybrid
- Context → Perceived Value Agreement

---

## UC-DESIGN-003

### Structural
- Persistent State Definitions
- Cross-system dependency edges
- State duration

### Structural / model-dependent
- State → Decision Dependency
- Cross-system Plan Change condition

### Simulation
- State-triggered Assignment / Route / Build change
- Plan revision rate
- Recovery / replacement usage where relevant

### Player Telemetry
- Choice change after persistent consequence

### Human
- Consequence Ownership
- “과거 선택이 현재 판단을 바꿨는가?”

### Hybrid
- Consequence-to-next-decision coupling quality

---

## UC-DESIGN-004

### Structural
- Uncertainty Sources
- Response Option Definitions
- Reserve / Reroll / Avoid / Recovery availability

### Structural / model-dependent
- Uncontrollable Outcome Candidate
- Unavoidable Failure Candidate
- Response Coverage

### Simulation
- Response Option Usage
- RNG-triggered Plan Change
- Reserve Usage
- Recovery Rate

### Player Telemetry
- Reroll / retreat / reserve / avoid actions

### Human
- Perceived Control
- Fairness
- “대응할 방법이 있었는가?”

### Hybrid
- Structural response opportunity ↔ perceived agency

---

## UC-DESIGN-005

### Structural / Machine
- State → Presentation Mapping Coverage
- Cause → Effect Trace Availability
- Critical Information Availability
- Threat Cue Availability

### Structural / model-dependent
- Information → Possible Action mapping
- Hidden Dependency / unexplained transition
- Cue → Response Window

### Simulation
AI GameState access 자체를 information usage로 계산하지 않는다.
UI / observation policy를 명시한 Agent Test에서만:
- information check → action change
- forecast use
를 사용할 수 있다.

### Player Telemetry
- Info panel / notebook / alert usage
- Check → Action Change
- Retry / inspect behavior

### Human
- Diagnosis Accuracy
- Threat Recognition
- Prediction Explanation
- Failure Attribution
- Cause Recognition
- Rule Understanding

### Hybrid
- Formal Cause ↔ Perceived Cause Agreement
- Structural Cue ↔ Human Recognition

---

## UC-DESIGN-006

### Structural
- Progression State
- Unlock / Capability Definition
- Skill / equipment / meta option availability

### Structural / model-dependent
- Solution Space Change
- Capability Coverage
- Decision Expansion

### Simulation
- Progression Stage → Action Distribution
- Build / strategy emergence
- late-game choice concentration

### Player Telemetry
- progression choice
- respec / equipment swap
- unlock usage

### Human
- Progression Meaning
- Power Fantasy Satisfaction
- “성장 후 새롭게 할 수 있게 된 것”

### Hybrid
- Progression Promise Fit
- Vertical Power vs Decision Preservation

---

# 28. AI Tester Interpretation Guardrails

다음을 Universal 수준에서 고정한다.

```text
AI State Access
≠
Player Knowledge
```

```text
AI Success
≠
Human Usability
```

```text
Machine Cause Trace
≠
Human Failure Attribution
```

```text
Optimal Choice Diversity
≠
Perceived Meaningful Choice
```

추가:

```text
Response Option Exists
≠
Human can perceive / execute it in time
```

```text
Progression Unlock Exists
≠
Player perceives meaningful growth
```

```text
State Persists
≠
State changes future decisions
```

AI Tester는:
- structural impossibility
- policy convergence
- causal trace
- distribution
검증에는 강하다.

다음은 Human / Hybrid 필요:
- readability
- fairness
- attribution
- tension
- identity
- meaning
- power fantasy.

---

# 29. Universal Anti-Patterns

## AP-UC-001 — Shared Word = Shared Mechanism
Recovery / Identity / Progression이라는 단어만 보고 merge.

## AP-UC-002 — Universal Parent Deletes Genre Specificity
Parent가 있다고 threat timing / inference ownership / causal simulation을 삭제.

## AP-UC-003 — Parent + Child Double Penalty
같은 Root Issue에 두 Severity.

## AP-UC-004 — Universal Core Applied to N/A Product Promise
Replay / progression / control fantasy가 없는 게임에 억지 적용.

## AP-UC-005 — Human Experience Inferred from Machine Metric
AI success / cause trace를 Human readability로 간주.

## AP-UC-006 — Scope Rule Classified as Design Rule
Production complexity를 Design complexity와 혼합.

## AP-UC-007 — Validation Method Classified as Design Core
Risk-first test planning을 player-facing design rule로 취급.

## AP-UC-008 — Counterexample Ignored for Broader Coverage
Vertical Power / Chaos / one-shot deduction 경계를 무시.

## AP-UC-009 — Candidate Promoted because Many Genre Documents Mention It
동일 Reference가 여러 Genre 문서에 재사용될 수 있다.

## AP-UC-010 — Universal Checklist Explosion
모든 Genre 질문을 Universal에 끌어올려 20~30개 공통 체크 생성.

---

# 30. Universal Reviewer Default Set

Default는 **5개**로 유지한다.

## Q1 — Consequence Density

> 이 시스템 / 입력은 다른 질문과 다른 consequence를 만드는가, 아니면 입력·기능 수만 늘리는가?

`UC-DESIGN-001`

---

## Q2 — Contextual Value

> 반복 / 변화가 Product Promise라면 Context 변화가 기존 선택의 가치나 우선순위를 실제로 바꾸는가?

`UC-DESIGN-002`

---

## Q3 — Consequence Coupling

> 이전 결과 / persistent state가 이후 어떤 판단을 실제로 바꾸는가?

`UC-DESIGN-003`

---

## Q4 — Response to Uncertainty

> 중요한 불확실성에 대해 준비·조작·회피·reserve·recovery 중 의미 있는 response가 있는가?

`UC-DESIGN-004`

---

## Q5 — Actionable / Learnable Information

> 플레이어가 현재 판단을 할 수 있고, 중요한 결과 뒤 원인을 학습할 수 있을 만큼의 정보를 받는가?

`UC-DESIGN-005`

---

## Conditional Q6 — Progression Promise

Progression이 실제 Product Promise일 때만 load.

> 이 Progression은 어떤 성장 약속을 하는가? Build / Role / Capability 확장이라면 실제 Choice Space를 바꾸는가? Vertical Power라면 다른 Core Decision을 의도치 않게 지우는가?

`UC-DESIGN-006 — CANDIDATE`

---

# 31. Universal Runtime Schema

```text
UNIVERSAL_CORE_CHECK

Core:
Applicability:
- YES
- CONDITIONAL
- N/A

Parent Rule:

Triggered Genre Specializations:
- ...

Observed Issue:

Root Cause:

Severity:
- CRITICAL / HIGH / MEDIUM / LOW

Evidence Confidence:
- Core confidence
- Project evidence confidence
별도 기록

Machine Evidence:
- ...

Human Evidence:
- ...

Recommended Action:
- modify / remove / merge / prototype test

Validation Handoff:
- ...

Double-Penalty Guard:
- same root already owned by another Parent/Child?
```

---

# 32. Promotion Decision Table

| ID / Pattern | Current | Audit | Cross-Genre | Counter Evidence | Final Recommendation |
|---|---|---|---|---|---|
| `UC-DESIGN-001` | PROVISIONAL / VERY HIGH | STRENGTHEN | Strong | motor-skill products | **KEEP PROVISIONAL** |
| `UC-DESIGN-002` | PROVISIONAL / HIGH | STRENGTHEN BOUNDARY | Strong in replay/system games | one-shot / authored products | **KEEP PROVISIONAL** |
| `UC-DESIGN-003` | PROVISIONAL / HIGH | STRENGTHEN | Strong | over-coupling / snowball | **KEEP PROVISIONAL** |
| `UC-DESIGN-004` | PROVISIONAL / HIGH | REFRAME | Deck + Strategy + adjacent | chaos / unpredictability fantasy | **KEEP PROVISIONAL — REFRAME** |
| `UC-DESIGN-005` | PROVISIONAL / HIGH | STRENGTHEN SUBSTRUCTURE | Very broad | inference / deliberate opacity boundaries | **KEEP PROVISIONAL** |
| `UC-DESIGN-006` | CANDIDATE / MEDIUM-HIGH | REFRAME TITLE + RULE | RPG + adjacent progression | Vertical Power valid | **KEEP CANDIDATE** |
| Failure Attribution | Action reclass candidate / cross-genre | REDUCE TO UC005 | Broad but uneven Human evidence | chaos / opaque fantasy | **NO NEW UC** |
| Recovery | Cross-genre pattern | SPLIT BY PARENT | Broad words, mixed mechanism | terminal failure valid | **NO NEW UC** |
| Identity / Differentiation | Cross-genre label | REJECT AS SINGLE MECHANISM | Multiple genres | mechanisms differ | **NO NEW UC** |
| Complexity / Compression | Cross-genre pattern | KEEP PATTERN | Strategy/Simulation strongest | layer ambiguity | **NO NEW UC** |
| `SC-SOLO-001` Layer | Scale Provisional | RECLASS CANDIDATE | General logic plausible | non-Solo direct evidence weak | **KEEP STATUS; Validation Parent candidate** |
| `SC-SOLO-004` Layer | Scale Provisional | RECLASS CANDIDATE | General logic plausible | cross-scale direct evidence weak | **KEEP STATUS; Reference Analysis candidate** |

---

# 33. CANONICAL_SYNC_REQUIRED Registry

이번 문서는 Source를 직접 수정하지 않는다.

승인 후 별도 Sync 단계에서 다음을 반영한다.

## Sync 1 — Studio Core

### `UC-DESIGN-004`
Status는 유지.

Canonical Rule wording을 RNG-only에서 broader uncertainty response로 Reframe.

### `UC-DESIGN-005`
Status / Rule essence 유지.

Substructure 추가:
- Decision-time Actionability
- Outcome-time Learnability / Attribution

### `UC-DESIGN-006`

Status:
`KEEP AS CANDIDATE`

Canonical Title:
`Progression Should Match Its Intended Promise`

Canonical Rule:
Promise-conditional wording으로 Reframe.

Confidence:
`MEDIUM-HIGH` 유지.

### `SC-SOLO-001`
Status 유지.
Layer metadata:
`Validation Parent Reclassification Candidate / Solo Amplification`

### `SC-SOLO-004`
Status 유지.
Layer metadata:
`Reference Analysis Reclassification Candidate / Solo Amplification`

---

## Sync 2 — Genre Master

Universal Parent map 수정:

- `GC-ACTION-003`
  - `Universal Reclassification Candidate`
  - → `UC-DESIGN-005 Outcome-time Attribution specialization / CROSS_GENRE_PATTERN`
- `GC-ACTION-002`
  - UC005 Decision-time specialization 유지.
- `GC-ACTION-007`
  - UC001 specialization 유지.
- `GC-STRAT-004`
  - UC005 prediction specialization.
- `GC-SIM-004`
  - UC005 causal diagnosis specialization.
- `GC-RPG-001`
  - reframed UC006 specialization.
- `GC-RPG-005`
  - UC003 specialization.
- `GC-NARR-009`
  - UC002 related + NARR001 merge/sub-rule candidate.
- `GC-NARR-001`
  - independent Narrative Core 유지.

Double / Triple penalty examples를 이번 Registry에 맞춰 Sync.

---

## Sync 3 — Runtime Metadata

Universal Default Check:
- 5 Active defaults
- UC006 conditional diagnostic

Applicability Gate:
- YES / CONDITIONAL / N/A

---

# 34. No-change Registry

이번 Consolidation에서 변경하지 않는다.

- 9 Genre Evidence Base
- 28 Provisional Genre Core status
- Genre Candidate status 자체
- 51 Scale Handoff
- Active Independent GSC = 0
- Retired Historical GSC = 3
- Routing Specialization = 2
- `SC-SOLO-002`
- `SC-SOLO-003`
- `SC-MICRO-001`
- Market Core
- Selection Core
- Validation Core status
- Small / Mid+ Evidence Boundary

특히:
`GC-ACTION-003`의 Genre Candidate status를 이번 단계에서 삭제하지 않는다.

Parent mapping만 재정리한다.

---

# 35. Evidence Gaps

## Universal Design

1. Failure Attribution의 cross-genre Human evidence
2. Formal cause trace ↔ perceived cause agreement
3. Recovery mechanism이 Parent-independent한지 확인할 evidence
4. Vertical Power vs Decision-expanding progression 비교
5. Contextual mechanical value vs narrative meaning의 경계
6. Relevance-preserving abstraction beyond Strategy / Simulation
7. one-shot / low-replay games에서 UC002 applicability
8. chaos / horror / surprise products에서 UC004 boundary

## Layer Ownership

9. Risk-first Prototype outside Solo/Micro
10. Post-success benchmarking across team scales
11. larger-team prototype prioritization postmortem
12. reference scope misuse and production outcomes

---

# 36. Additional Research Targets

| Candidate / Question | Missing Mechanism Evidence | Missing Counter Evidence | Best Reference Type |
|---|---|---|---|
| UC004 Reframe | non-RNG uncertainty response across genres | chaos/surprise products | design postmortem / telemetry |
| UC006 | progression promise vs actual choice-space change | vertical-power satisfaction | RPG/action/roguelite progression telemetry + interviews |
| Failure Attribution | player-reported cause across multiple genres | intentional opacity / chaos | playtest study / postmortem / telemetry |
| Recovery | same mechanism across management/strategy/action? | terminal failure products | failure/recovery telemetry |
| Compression Pattern | abstraction preserving decision-relevant state | genres where detail itself is fantasy | UI/system design talks |
| SC-SOLO-001 ownership | risk-first prototype in 6+ teams | cases where broad prototype was useful | prototype postmortem |
| SC-SOLO-004 ownership | post-success scope benchmarking beyond solo | cases where current scope is valid benchmark | production timeline / scope postmortem |

Research Target의 목적은 Reference 수 증가가 아니라:

> Promotion / Reclassification Decision을 바꿀 Evidence

를 찾는 것이다.

---

# 37. Self-Review

| Check | Result | Note |
|---|---|---|
| UC001~006 전부 Audit? | PASS | 5 Provisional + 1 Candidate |
| Shared Word = Shared Mechanism 방지? | PASS | Recovery / Identity / Complexity 분리 |
| Genre residual 보존? | PASS | Action timing, Deduction inference, Narrative meaning 등 |
| Deduction을 UC005에 과흡수하지 않았는가? | PASS | Inference ownership / reachability / validation 독립 |
| Recovery 독립 UC 억지 승격? | PASS | Cross-Genre Pattern |
| Failure Attribution Design/Validation 분리? | PASS | UC005 design + Validation evidence boundary |
| UC006 Vertical Power counterexample 반영? | PASS | Promise-conditional reframe |
| SC-SOLO-001 Layer Ownership Audit? | PASS | Validation Parent candidate |
| SC-SOLO-004 Layer Ownership Audit? | PASS | Reference Analysis candidate |
| Parent/Child Double Penalty 제거? | PASS | Registry 작성 |
| Hybrid Triple Penalty 확인? | PASS | Management×Simulation / Narrative examples |
| Machine vs Human 분리? | PASS | Metric + guardrails |
| Universal N/A 허용? | PASS | Applicability gate |
| 신규 UC 적어도 정상? | PASS | New UC 0 |
| Canonical Sync 별도 Registry? | PASS | Source overwrite 없음 |

---

# 38. Final Position

## A. UC-DESIGN-001~005는 그대로 Provisional Core로 유지해야 하는가?

**YES.**

단:
- 001 — strengthen
- 002 — boundary strengthen
- 003 — strengthen
- 004 — **reframe**
- 005 — substructure strengthen

상태는 모두 `PROVISIONAL CORE` 유지.

---

## B. 어떤 UC는 Reframe이 필요한가?

### 반드시 Reframe
`UC-DESIGN-004`

RNG-only wording → broader important uncertainty / response agency.

### Candidate Reframe
`UC-DESIGN-006`

Canonical Title:
`Progression Should Match Its Intended Promise`

Absolute decision-expansion reading → Product Promise conditional rule.

### Structure Clarification
`UC-DESIGN-005`

Decision-time Actionability + Outcome-time Learnability.

---

## C. UC-DESIGN-006은 Candidate 유지인가, 승격 가능한가?

**Candidate 유지.**

Canonical Title은 `Progression Should Match Its Intended Promise`로 Reframe한다.

현재 승격하지 않는다.

Vertical Power / mastery reward라는 정상 Counterexample가 강하고,
RPG evidence breadth와 Human progression evidence가 충분하지 않다.

---

## D. 새 Universal Design Core가 필요한가?

**현재 `0개`.**

새 UC를 추가하는 것보다 existing Parent hierarchy를 정리하는 편이 Reviewer를 더 단순하게 만든다.

---

## E. Failure Attribution은 Universal인가?

**Cross-genre Universal-level pattern은 맞지만 독립 Universal Core는 아니다.**

Runtime Owner:

`UC-DESIGN-005 — Outcome-time Learnability / Attribution`

Action / Simulation / Strategy / Roguelike residual은 Child에서 보존한다.

---

## F. Recovery는 독립 Universal인가?

**NO.**

Recovery는:
- UC004 Response Agency
- UC003 Consequence → Next Decision
- Genre-specific Failure Structure
중 하나 또는 복합으로 처리한다.

---

## G. Identity / Differentiation은 Universal화 가능한가?

**현재는 NO.**

공통 outcome label이지 동일 Mechanism이 아니다.

---

## H. Complexity / Compression에서 실제 공통 Mechanism이 존재하는가?

**제한적인 Cross-Genre Pattern은 있다.**

`Relevance-preserving Abstraction`

하지만 현재 Strategy / Simulation Evidence 편중과 layer ambiguity 때문에 UC 승격하지 않는다.

---

## I. SC-SOLO-001은 Validation Parent로 이동해야 하는가?

**장기적으로 가능성이 높지만 현재 즉시 이동하지 않는다.**

판정:

`RECLASSIFICATION CANDIDATE → Universal Validation Methodology Parent + Solo Amplification`

현재 Canonical SC status는 유지.

---

## J. SC-SOLO-004는 Reference Analysis Parent로 이동해야 하는가?

**장기적으로 가능성이 높지만 현재 즉시 이동하지 않는다.**

판정:

`RECLASSIFICATION CANDIDATE → Reference Analysis / Production Benchmarking + Solo Amplification`

현재 Canonical SC status 유지.

---

## K. 어떤 Genre Core가 Universal Parent 아래 정리되어야 하는가?

강한 예:

- UC001 → `GC-ACTION-007`, `GC-MGMT-003`
- UC002 → `GC-DECK-001`, `GC-MGMT-006`, `GC-ROGUE-003`, `GC-NARR-009` related
- UC003 → `GC-MGMT-004`, `GC-ROGUE-004`, `GC-STRAT-001/002`, `GC-SIM-002`, `GC-RPG-005`, `GC-NARR-003` partial
- UC004 → `GC-DECK-003`, `GC-STRAT-009`
- UC005 → `GC-MGMT-007`, `GC-STRAT-004`, `GC-SIM-004`, `GC-ACTION-002`, `GC-ACTION-003`
- UC006 candidate → `GC-RPG-001`; Deck/Management/Rogue progression findings related

---

## L. 어떤 Genre Core는 비슷해 보여도 독립 Genre Mechanism으로 반드시 남아야 하는가?

대표적으로:

### Deduction
- `GC-DEDUCT-001`
- `GC-DEDUCT-003`
- `GC-DEDUCT-004`

정보 문제처럼 보여도 Inference Ownership / Evidence Reachability / Validation Leakage는 UC005와 동일하지 않다.

### Narrative
`GC-NARR-001`

Context 변화와 관련되어도 Narrative Meaning / State-reactive Story Mechanism은 UC002에 완전 흡수하지 않는다.

### Simulation
`GC-SIM-001`

Scope / compression과 관련되어도 selective causal modeling 자체는 Simulation-specific core.

### Action
`GC-ACTION-001` 등 direct input/response control 후보는 Universal 정보/agency와 별개 Action evidence gap을 가진다.

---

## M. Universal Consolidation 이후 기본 Universal Check 수는?

**5개.**

`UC-DESIGN-001~005`

`UC-DESIGN-006`은 conditional diagnostic.

---

## N. Canonical Source Sync가 필요한가?

**YES.**

다음 단계에서:

1. Studio Core universal wording / metadata
2. Genre Master Parent hierarchy
3. Layer ownership metadata
4. Runtime default / applicability
를 Sync해야 한다.

---

## O. 그 다음 단계는 무엇이어야 하는가?

의존성 순서:

```text
1. Canonical Universal Source Sync
2. Reviewer Runtime Specification
3. Validation Planner Specification
4. AI Tester Persona / Metric Routing Specification
```

이유:

Reviewer Runtime은 어떤 Rule이 Parent이고 어떤 Child가 specialization인지 Canonical 상태가 먼저 잠겨야 안정적으로 생성할 수 있다.

Validation Planner와 AI Tester routing은 Runtime이:
- 어떤 Issue를 하나로 묶는지
- 어떤 Metric type을 요구하는지
정해진 뒤 연결하는 편이 중복을 줄인다.

---

# 39. Source Trace

## Universal / Scale Canonical
- `Studio_OS_Evidence_Based_Core_Extraction_v0.3.md`

## Genre Router
- `GENRE_CORE_MASTER_INDEX_v0.2.md`

## Scale Router
- `SCALE_CORE_BASELINE_v0.2.md`

## Genre × Scale
- `GENRE_SCALE_CORE_INTEGRATION_v0.1_APPROVED.md`
- `GSC_CANONICAL_CONSOLIDATION_v0.1.md`

## Approved Genre Baselines
- `DECKBUILDING_CORE_CANDIDATES_v0.1.md`
- `MANAGEMENT_CORE_CANDIDATES_v0.1.md`
- `ROGUELIKE_CORE_CANDIDATES_v0.1.md`
- `DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1.md`
- `NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1.md`
- `STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md`
- `SIMULATION_CORE_CANDIDATES_v0.1_APPROVED.md`
- `RPG_CORE_CANDIDATES_v0.1_APPROVED.md`
- `ACTION_CORE_CANDIDATES_v0.1_APPROVED.md`

## Evidence Boundary

이번 Consolidation은 기존 Approved Sources의 Rule / Evidence / Boundary를 재배치한 것이다.

외부 신규 Reference를 추가하지 않았다.

Canonical Source는 이번 문서에서 직접 수정하지 않았으며,
승인 후 `CANONICAL_SYNC_REQUIRED`를 별도 Source Sync 단계에서 반영한다.
