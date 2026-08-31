# DECKBUILDING_CORE_CANDIDATES_v0.1

**Studio OS — Deckbuilding Genre Core Deep Extraction**  
**Document:** `DECKBUILDING_CORE_CANDIDATES_v0.1`  
**Status:** `APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE`  
**Purpose:** 신규 Deckbuilding / Deckbuilding Hybrid 기획 평가용 Genre-specific Reviewer Knowledge Base  
**Baseline:** `STUDIO_CORE_CANDIDATES_v0.2`  
**Provisional Genre Cores:** `GC-DECK-001 ~ GC-DECK-005`  
**Candidate:** `GC-DECK-006 ~ GC-DECK-012`  
**Pending:** `Additional Evidence / Prototype Validation / Internal Evidence`

---

# 0. Executive Summary

이번 Deep Extraction의 핵심 결론은 다음과 같다.

1. **Deckbuilding의 핵심은 카드 수가 아니라 Pool Composition이 이후 Availability와 Choice Value를 바꾸는 구조다.**
2. `GC-DECK-001 Contextual Card Value`는 **Provisional Core로 강화**한다.
3. 기존 `GC-DECK-002 Build Identity / Pivotability`는 분리한다.
   - **Build Identity Formation** → Provisional Core
   - **Pivotability** → Candidate
4. `GC-DECK-003 RNG Control`은 `UC-DESIGN-004 Uncertainty Response Agency`의 Deckbuilding 특수화로 유지한다.
5. 신규 Provisional Core:
   - `GC-DECK-004` — Synergy Must Change Decisions, not only Multiply Numbers
   - `GC-DECK-005` — Pool Growth Needs Quality Control
6. Reward Choice, Build Pivot, Encounter Pressure, Synergy Readability, Build Formation Timing, Sequencing은 중요하지만 현재 Primary Evidence가 부족해 Candidate로 유지한다.
7. Deckbuilding의 반복 Anti-Pattern:
   - More Cards = More Depth
   - Forced Archetype / Early Build Lock
   - Excessive Pivot / Identityless Build
   - Auto-pick Reward
   - Dead Card Inflation
   - Uncontrolled Availability RNG
   - Universal Best Card
   - Synergy Obscurity
   - Build Forms Too Late / Solves Too Early
   - Dominant Engine removes decisions
8. AI Tester는 **수렴·편향·빈도·성공률·Availability**를 검증한다. Fun, Build Fantasy, Synergy Discovery Satisfaction, Fairness는 Human Test가 필요하다.
9. 가장 중요한 Reviewer 질문:

> **“이 카드를 넣는 선택이 덱에 들어간 순간뿐 아니라 이후 Draw Pool, Reward Value, Encounter 대응, 다른 카드의 가치까지 바꾸는가?”**

10. 현재 가장 큰 Evidence Gap:
   - Build Pivot 실제 데이터
   - Reward Skip / Regret 데이터
   - Removal 필요 조건
   - Build Formation Timing
   - Underperforming Deckbuilder Control Case
   - Human Cognitive Load / Synergy Readability Telemetry

---

# 1. Deckbuilding Genre Definition

Studio OS에서 Deckbuilding으로 분류하기 위해 단순히 카드 UI를 사용하는지는 보지 않는다.

## 1.1 Composition
Run / Session 동안 플레이어가 자신의 카드·심볼·효과 Pool 구성을 변경하는가?

## 1.2 Acquisition
새로운 구성요소를 획득하거나 기존 것을 제거·변환·강화·복제할 수 있는가?

## 1.3 Availability
Pool 구성에 따라 실제 사용할 수 있는 선택지가 확률적 또는 제한적으로 제공되는가?

## 1.4 Interaction
개별 카드의 가치가 다른 카드, 현재 자원, 적, Encounter, 순서, 상태, Relic / Modifier와 상호작용하는가?

## 1.5 Build Formation
Run이 진행되면서 초기 상태와 구별되는 Build Identity가 형성되는가?

## 1.6 Inclusion Rule

```text
Pool 구성 변경
→ Draw/Availability 변화
→ 현재 선택 변화
→ 다른 카드 가치 변화
→ Run 중 Build 형성
```

단순히 “카드를 UI 오브젝트로 사용한다”는 이유만으로 Primary Deckbuilding Evidence로 분류하지 않는다.

---

# 2. Source Classification

## 2.1 Tier A — Primary Deckbuilding Evidence

### REF-04 — Slay the Spire
**Subtype:** Combat Roguelike Deckbuilder  
**Evidence Strength:** VERY HIGH — Design / Balance / Metric

강한 Evidence 영역:
- Contextual Card Value
- Card Acquisition
- Removal / Pool 품질
- Build Diversity
- Enemy / Path / Relic가 카드 가치에 미치는 영향
- Choice Rate + Win Rate 병행 분석
- Early Access 반복 Balance

핵심 관찰:
카드 수와 RNG를 늘리는 것만으로는 깊이가 생기지 않으며, 적·경로·제거·유물 등 카드 선택 가치를 바꾸는 Context가 필요하다.

### REF-05 — Balatro
**Subtype:** Poker / Score Engine Deckbuilder  
**Evidence Strength:** VERY HIGH — Engine / Synergy / Onboarding

강한 Evidence 영역:
- Engine Building
- Limited Slot Pressure
- Modifier Interaction
- Familiar Rule Base
- Explosive Scaling
- Synergy Discovery

핵심 관찰:
핵심은 포커 자체가 아니라 제한된 슬롯 안에서 Joker와 Modifier가 서로 결합하여 점수 계산 규칙을 변화시키는 Engine Building이다.

### REF-20 — Dicey Dungeons
**Subtype:** Dice / Input Allocation Deckbuilder  
**Evidence Strength:** HIGH — RNG Control / Rule Variant

강한 Evidence 영역:
- Visible RNG
- RNG Manipulation
- Input Allocation
- Character별 동일 Core Rule 재해석
- Compact Combat

핵심 관찰:
Randomness의 양보다 플레이어가 그것을 변환·재굴림·분할하는 선택을 가질 수 있는지가 중요하다.

### REF-34 — Peglin
**Subtype:** Orb / Physics Deckbuilding Hybrid  
**Evidence Strength:** MEDIUM for Design / HIGH for Prototype-Production

강한 Evidence 영역:
- Game Jam → Product
- 작은 한 문장 Core Mechanic
- Data Content와 Meta 확장

제한:
현재 Reference 문서는 Production 중심이므로 Removal, Reward Choice, Draw Consistency, Build Pivot, Enemy Pressure 등 세부 Deckbuilding Core를 Peglin 하나로 지지하지 않는다.

---

## 2.2 Tier B — Deckbuilding Hybrid / Secondary Evidence

### REF-18 — Loop Hero
Use:
- Self-authored Risk
- 자동화 후 플레이어에게 남기는 결정
- Synergy가 환경 위험을 바꾸는 구조

### REF-22 — Stacklands
Use:
- 공통 카드 Grammar
- 조합 Recipe
- 가독성
- Card representation ≠ Deckbuilding 경계 확인

---

## 2.3 Tier C — Adjacent Build-System Evidence

- `REF-19 — Cultist Simulator`
  - Common Card Grammar
  - Discovery
  - Onboarding 부담
- `REF-26 — Luck be a Landlord`
  - Symbol Pool Building
  - Synergy
  - Data-driven expansion
- `REF-36 — Brotato`
  - Build Identity
  - Character Rule
  - Item/Weapon data
- `REF-12 — Vampire Survivors`
  - Reward Loop
  - Vertical Power
  - Build Choice

**Rule:** Tier C만으로 Deckbuilding Provisional Core를 승격하지 않는다.

---

# 3. Existing Core Audit

## GC-DECK-001 — Contextual Card Value

**Status:** `PROVISIONAL CORE`  
**Origin:** `EXISTING GC REFINEMENT`

### Refined Rule

> **카드의 설계 가치는 단일 Power가 아니라, 서로 다른 Build / Encounter / Run Phase에서 선택 가치와 성과가 어떻게 변하는지로 평가한다.**

### Mechanism

카드가 모든 Context에서 동일하게 강하면:
- Universal Pick
- Build Convergence
- Reward Auto-pick

이 발생한다.

Context에 따라 가치가 바뀌면 현재 Build, 적, 자원, 경로, 앞으로의 위험을 함께 판단하게 된다.

### Primary Evidence
- Slay the Spire — 현재 덱과 상황에 따라 카드 가치가 달라져야 하며 선택률과 승률을 함께 보아야 함.
- Balatro — 제한된 Joker Slot과 Modifier 관계로 “좋은 카드”와 “지금 교체할 가치가 있는 카드”가 달라지는 Engine Pressure.

### Counter Evidence
Power Fantasy 중심 게임에서는 일부 Universal Strong Reward가 의도적일 수 있다. 단, Universal Strong Choice가 많아질수록 Deckbuilding Decision은 약해진다.

### Observed Metric
- Pick / Choice Rate
- Win Rate

### Candidate Metric — Machine
- Card Pick Rate by Context
- Conditional Win Rate
- Usage Rate
- Universal Pick Rate
- Contextual Value Variance
- Build-specific Pick Rate

### Candidate Metric — Human
- “이 카드가 언제 좋은가” Explanation Accuracy

### AI Tester Applicability
HIGH.

### Confidence
**VERY HIGH**

### Reviewer Action

> “어떤 상황에서 이 카드를 고르지 않아야 하는가?”

답이 없다면 `UNIVERSAL_BEST_CARD_RISK`.

---

## GC-DECK-002 — Build Identity Formation

**Status:** `PROVISIONAL CORE`  
**Origin:** `SPLIT / REFINEMENT OF EXISTING GC-DECK-002`

### Rule

> **Build Identity는 이름 붙은 Archetype의 존재보다, 이전 선택 때문에 이후 특정 카드·자원·행동의 가치가 체계적으로 달라지는 상태로 정의한다.**

### Mechanism

```text
Choice A 획득
→ Choice B 가치 상승
→ Choice C 가치 하락
→ Reward 우선순위 변화
→ Encounter 대응 방식 변화
```

### Primary Evidence
- Slay the Spire — 현재 덱·Relic·경로·적이 미래 카드 가치를 바꿈.
- Balatro — 제한된 Joker Slot과 계산 Modifier가 서로 결합해 점수 Engine 형성.

### Secondary Evidence
- Dicey Dungeons — Character Rule Variant가 동일 Core를 다른 use pattern으로 재해석.
- Brotato — Character Modifier와 Item/Weapon data가 Build Identity를 강제하는 Adjacent Evidence.

### Boundary
Pre-constructed Deck / Fixed Archetype 게임에서는 Run 중 Build “형성”보다 Build “실행·정제”가 핵심일 수 있다.

### Candidate Metric — Machine
- Build Cluster Separation
- Build-specific Card Pick Rate
- Early Choice → Later Choice dependency
- Archetype Diversity
- Build Convergence
- Effect Family Concentration

### Candidate Metric — Human
- Build Identity Recognition Turn
- “현재 내 덱이 무엇을 잘하는가?” Explanation Accuracy
- Build Fantasy Strength

### Confidence
**HIGH**

### Reviewer Action
“불덱 / 독덱 / 방어덱” 같은 명칭만으로 Build Identity가 있다고 인정하지 않는다.

> 그 Build를 선택한 뒤 실제로 어떤 미래 Reward의 가치가 달라지는가?

를 확인한다.

---

## GC-DECK-003 — Availability / RNG Control

**Status:** `PROVISIONAL CORE`  
**Origin:** `GENRE SPECIALIZATION OF UC-DESIGN-004 + EXISTING GC REFINEMENT`

### Rule

> **Availability가 확률적으로 제한되는 Deckbuilding에서는 플레이어가 Draw Distribution 또는 Candidate Availability에 개입할 수 있는 하나 이상의 전략적 수단을 검토한다.**

가능한 수단:
- Draw
- Discard
- Retain
- Search
- Select
- Scry
- Transform
- Remove
- Reroll
- Duplicate
- Cost Manipulation

### Mechanism

Pool Composition과 실제 Action Availability 사이의 간극이 너무 크면:

> Build를 만들었지만 사용할 수 없다.

가 된다.

반대로 모든 Combo를 안정적으로 Search할 수 있다면 Pool RNG가 무의미해지고 고정 Combo Sequence로 수렴할 수 있다.

### Primary Evidence
- Dicey Dungeons — Randomness를 보여주고 변환·재굴림·분할 수단을 제공.
- Slay the Spire — 단순 RNG 증가가 깊이를 만들지 않는다는 경고.

### Counter Evidence
고변동성 자체가 Player Fantasy인 Score Chase / Chaos Builder에서는 높은 Variance가 의도된 재미일 수 있다.

### Candidate Metric — Machine
- Dead Draw Rate
- Key Card Availability
- Draw Consistency
- Hand Clog Rate
- Reroll Usage
- Search Usage
- Removal Impact on Availability
- Combo Completion Probability

### Candidate Metric — Human
- Perceived Fairness
- “내 덱이 작동하지 않은 이유” Attribution

### AI Tester Applicability
VERY HIGH for structural distribution.

### Confidence
**HIGH**

### Reviewer Action
RNG가 문제라고 판단되면 Randomness를 줄이는 것부터 하지 않는다.

> **플레이어가 확률 구조를 조절할 방법이 있는가?**

를 먼저 본다.

---

# 4. Provisional Deckbuilding Cores

## GC-DECK-004 — Synergy Must Change Decisions, not only Multiply Numbers

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

### Rule

> **Synergy는 최종 Power 증가량만 보지 말고, Synergy가 존재함으로써 이후 Card Acquisition / Removal / Sequencing / Resource Allocation 판단이 달라지는지 평가한다.**

### Mechanism
단순 Multiplier만 존재하면 같은 최고 수치 조합을 반복하기 쉽다.

Rule Interaction이:
- 특정 카드 가치 상승
- 특정 카드 가치 하락
- 자원 사용 순서 변경
- 슬롯 우선순위 변경

을 만들면 Engine Identity가 생긴다.

### Primary Evidence
- Balatro — 제한 슬롯 안 Modifier 결합으로 Engine을 만드는 과정이 핵심.
- Slay the Spire — 카드 선택 가치가 현재 덱과 상황에 따라 달라져야 함.

### Secondary Evidence
- Loop Hero — 타일 간 상호작용이 콘텐츠 하나의 재사용 가치를 높임.

### Candidate Metric — Machine
- Synergy Pair / Family Usage
- Synergy Presence → Reward Choice Shift
- Synergy Presence → Removal Choice Shift
- Engine Concentration
- Decision Entropy before / after Engine Completion

### Candidate Metric — Human
- Synergy Discovery Recognition
- Synergy Explanation Accuracy

### Confidence
**HIGH**

### Reviewer Action

> “그래서 이후 어떤 선택이 달라지는가?”

숫자만 커지고 이후 판단이 변하지 않으면 `POWER_WITHOUT_DECISION_RISK`.

---

## GC-DECK-005 — Pool Growth Needs Quality Control

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

### Rule

> **Pool 성장 구조에서는 Acquisition만큼 Pool Quality를 관리하는 선택이 존재하는지 검토한다. 단, Removal이라는 특정 Feature를 의무화하지 않는다.**

Pool Quality Control 후보:
- Remove
- Transform
- Upgrade
- Duplicate
- Selective Reward
- Skip
- Retain / Search
- Pool Cap
- Replacement

### Mechanism

모든 Reward를 자동으로 Pool에 추가하면:

```text
Progression
= 카드 수 증가
= Draw Variance 증가
= Build Consistency 감소
```

가 될 수 있다.

Deckbuilding에서는 “더 얻음”과 “더 좋아짐”이 같은 뜻이 아니다.

### Primary Evidence
- Slay the Spire — 제거가 카드 선택 가치를 바꾸는 Context 중 하나로 명시됨.
- Balatro — 제한 Slot / Engine / Deck manipulation이 Pool과 Engine 품질 Pressure를 만듦.

### Counter Evidence
- 매 턴 전체 Pool을 사용할 수 있는 Tableau Builder
- 카드 자동 소멸 구조
- Replacement/Cap 중심 구조

에서는 별도 Removal 필요성이 낮다.

### Candidate Metric — Machine
- Average Pool Size
- Removal / Transform / Skip Rate
- Dead Draw Rate by Pool Size
- Key Card Availability by Pool Size
- Pool Growth → Outcome Curve
- Reward Acceptance Rate

### Candidate Metric — Human
- Deck Ownership
- Reward Regret
- Perceived Deck Bloat

### Confidence
**MEDIUM-HIGH**

### Reviewer Action

> “이 보상을 받지 않는 것이 좋은 상황이 존재하는가?”

를 확인한다.

---

# 5. Deckbuilding Core Candidates

## GC-DECK-006 — Reward Choice Must Compete with Future Consistency

**Status:** `CANDIDATE`

### Rule Candidate

> Reward는 현재 Power만 비교하는 선택이 아니라 현재 Build 강화, 미래 Pivot 가능성, Pool Dilution 사이의 Trade-off를 만들 때 Deckbuilding Decision으로 기능한다.

### Candidate Metrics
- Reward Skip Rate
- Reward Choice Concentration
- Reward Replacement Rate
- Reward Regret
- Pick → Never Used Rate

### Confidence
**MEDIUM**

---

## GC-DECK-007 — Build Pivotability

**Status:** `CANDIDATE`

### Rule Candidate

> Build Identity가 형성되어도 새로운 Reward / Enemy Pressure에 대응해 방향을 수정할 수 있어야 하지만, Pivot 비용이 너무 낮아 모든 Build가 즉시 최적 카드 묶음으로 수렴해서도 안 된다.

### Too Hard to Pivot
- Early Choice Lock
- Run이 초반 RNG로 결정
- 이후 Reward Choice 의미 감소

### Too Easy to Pivot
- Build Identity 약화
- 모든 Reward가 단기 효율 비교
- Commitment 없음

### Candidate Metrics
- Build Pivot Rate
- Early Choice → Final Build Correlation
- Pivot Success Rate
- Pivot Cost
- Post-Pivot Recovery Time

### Confidence
**MEDIUM**

---

## GC-DECK-008 — Encounter Pressure Should Test Different Parts of the Build

**Status:** `CANDIDATE`

### Rule Candidate

> Encounter 차이는 HP/공격력 증가만이 아니라 서로 다른 카드·자원·Sequencing의 가치를 바꾸어야 한다.

### Evidence
Slay the Spire의 “적·경로가 카드 선택 가치에 영향을 준다”는 명시적 원칙이 강한 근거지만 두 번째 독립 Primary Evidence가 부족하다.

### Candidate Metrics
- Encounter별 Card Usage Shift
- Encounter-specific Failure Cause
- Build Matchup Variance
- Universal Strategy Success Rate

### Confidence
**MEDIUM**

---

## GC-DECK-009 — Synergy Readability

**Status:** `CANDIDATE`

### Rule Candidate

> 강한 Synergy가 존재하더라도 플레이어가 관계를 발견·예측·설명할 수 없다면 Build Agency가 아니라 외부 Wiki 의존으로 이동할 수 있다.

### Evidence
- Balatro — 익숙한 Poker Rule이 새로운 Modifier를 이해할 인지 여유 제공.
- Stacklands — 카드 조합 규칙의 가독성 경고.
- Cultist Simulator — Discovery 중심 Card Grammar의 높은 온보딩 비용.

### Candidate Metrics — Human
- Synergy Discovery Rate
- Tooltip Dependency
- Build Explanation Accuracy
- First Synergy Recognition Time

### Confidence
**MEDIUM**

---

## GC-DECK-010 — Build Formation Timing

**Status:** `CANDIDATE`

### Rule Candidate

> Build가 너무 늦게 형성되면 Run 대부분을 Generic Deck으로 플레이하고, 너무 빨리 완성되면 후반 Reward Decision이 사라질 수 있다.

### Candidate Metrics
- Build Formation Turn / Floor
- First Synergy Turn
- Last Meaningful Build Change
- Power Spike Timing
- Post-Engine Decision Entropy

### Confidence
**MEDIUM-LOW**

---

## GC-DECK-011 — Sequencing Value

**Status:** `CANDIDATE`

### Rule Candidate

> 카드 순서가 중요하다면 순서 변경이 새로운 판단을 만들어야 하며, 항상 같은 고정 Combo Sequence를 재생하는 구조로 수렴하지 않아야 한다.

### Candidate Metrics
- Sequence Diversity
- Fixed Combo Repetition
- Order-dependent Outcome Variance

### Confidence
**LOW-MEDIUM**

---

## GC-DECK-012 — Vertical Power vs Decision Preservation

**Status:** `CANDIDATE`

### Rule Candidate

> 후반 Power Explosion이 Player Fantasy라면 허용할 수 있지만, Power가 커질수록 Reward / Encounter Decision이 사라지는 시점을 별도로 점검한다.

### Evidence
- Balatro — Explosive Scaling이 의도된 Fantasy.
- Vampire Survivors — Vertical Power Reward의 Adjacent Evidence.

### Candidate Metrics
- Decision Entropy by Run Phase
- Overkill / Excess Score Ratio
- Universal Reward Acceptance after Power Spike

### Confidence
**MEDIUM-LOW**

---

# 6. Deckbuilding Anti-Patterns

## AP-DECK-001 — More Cards = More Depth

**Trigger**
- Context / Interaction 변화 없이 카드 수만 확대

**Consequence**
- QA 증가
- Tooltip 증가
- Dead Pick 증가
- 초보자 학습비 증가
- 실제 Decision은 유지될 수 있음

**Evidence**
- Slay the Spire — 카드 수와 RNG 증가만으로 깊이가 생기지 않는다는 Warning.
- Balatro — 조합 QA 폭증.

**Detection**
- New Card당 New Decision Context
- Dead Pick Rate
- Universal Pick Rate
- Effect Family Redundancy

**Mitigation**
새 Card 추가 시:

> “어떤 기존 카드의 가치가 달라지는가?”

를 요구한다.

---

## AP-DECK-002 — Forced Archetype / Early Build Lock

**Trigger**
초반 핵심 Reward 하나가 이후 모든 선택을 결정.

**Consequence**
- 초기 RNG 의존
- Reward Auto-pick
- Pivot 불가

**Detection**
- Early Choice → Final Build Correlation
- Pivot Rate
- Off-archetype Pick Rate
- Early Key Item Dependency

**Mitigation**
- Soft Synergy
- Bridge Card
- Multi-role Reward
- Pivot Window

---

## AP-DECK-003 — Excessive Pivot / Identityless Build

**Trigger**
Commitment Cost가 거의 없음.

**Consequence**
Build가 Engine이 아니라 현재 최고 Power Pick의 모음이 됨.

**Detection**
- Build Cluster Separation
- Card Pick Distribution across Builds
- Universal Card Usage

**Mitigation**
Synergy dependence / limited slots / resource specialization.

---

## AP-DECK-004 — Auto-pick Reward

**Trigger**
특정 Reward가 거의 모든 상황에서 최선.

**Consequence**
Reward Screen은 존재하지만 Decision은 사라짐.

**Detection**
- Reward Choice Concentration
- Universal Pick Rate
- High Pick + High Conditional Win Rate
- Skip Rate near zero

**Mitigation**
Contextual value / Opportunity Cost / Slot pressure.

---

## AP-DECK-005 — Dead Card Inflation

**Trigger**
Pool 확대와 함께 특정 Build/Encounter에서 완전히 무가치한 카드 증가.

**Consequence**
- Reward frustration
- Draw clog
- false variety

**Detection**
- Dead Pick Rate
- Never-used Pick Rate
- Dead Draw Rate
- Pool Size vs Actionable Card Ratio

**Mitigation**
- Pool curation
- Transform
- Skip
- multi-context utility
- reward filtering

---

## AP-DECK-006 — Uncontrolled Availability RNG

**Trigger**
Build 핵심요소가 Draw/Roll에 강하게 의존하지만 조작 수단이 없음.

**Consequence**
“덱을 만들었다”보다 “필요 카드가 안 나왔다”가 패배 원인으로 인식됨.

**Evidence**
Dicey Dungeons의 Primary Warning.

**Detection**
- Key Card Availability
- Uncontrollable Failure Rate
- Hand Clog
- Availability control option count

**Mitigation**
Draw / Discard / Search / Retain / Removal / Reroll.

---

## AP-DECK-007 — Universal Best Card

**Trigger**
Build/Encounter와 무관하게 높은 Pick과 Outcome을 유지.

**Consequence**
- Build convergence
- Reward auto-pick
- 가짜 다양성

**Detection**
- Universal Pick Rate
- Conditional Win Rate across Build clusters
- Deck Inclusion Rate

**Mitigation**
Context-dependent cost / slot pressure / downside / encounter variation.

---

## AP-DECK-008 — Synergy Obscurity / Keyword Inflation

**Trigger**
상호작용이 너무 많은 Keyword, 예외 Rule, 숨은 관계에 의존.

**Consequence**
Build Agency가 플레이어 이해보다 Wiki knowledge로 이동.

**Detection — Human**
- Synergy Explanation Accuracy
- Tooltip Open Rate
- External Note / Wiki Dependence
- Rule Recall

**Mitigation**
- Effect Family 제한
- Progressive Disclosure
- Common Grammar
- Clear Feedback

---

## AP-DECK-009 — Build Forms Too Late

**Trigger**
Run 후반까지 Reward가 Generic Value 중심.

**Consequence**
Deckbuilding Fantasy를 경험하기 전에 Run 대부분이 끝남.

**Detection**
- Build Formation Turn
- First Synergy Turn / Run Length
- Replay Intent before first build

**Mitigation**
초반에 방향을 강제하지 않으면서 Synergy Seed를 빠르게 제공.

---

## AP-DECK-010 — Build Solves Too Early

**Trigger**
초반 Engine 완성 후 후반 Reward/Encounter가 새 질문을 만들지 못함.

**Consequence**
- 후반 Decision Density 하락
- Auto-pick
- 반복 실행

**Detection**
- Last Meaningful Build Change
- Decision Entropy by Phase
- Reward Diversity after Power Spike

**Mitigation**
Encounter pressure / limited slots / trade-off upgrades / counter-context.

---

## AP-DECK-011 — Dominant Engine Removes Decisions

**Trigger**
한 Engine이 완성된 뒤 거의 모든 Encounter/Reward를 같은 방식으로 해결.

**Consequence**
Power Fantasy와 동시에 Deckbuilding Decision이 종료될 수 있음.

**Detection**
- Strategy Concentration
- Encounter-specific Strategy Shift
- Decision Entropy after Engine completion

**Mitigation**
- Encounter variation
- resource pressure
- slot pressure
- situational counter

---

# 7. Conflicting Findings

## CF-DECK-001 — Small Deck vs Large Deck

### Hidden Variable
- Draw model
- Reshuffle
- Exhaust/Fatigue
- Search ability
- Encounter diversity
- Combo dependence

### Resolution

> **Deck Size 자체를 Core로 만들지 않는다.**

평가 질문:

> “현재 Availability Model에서 Pool Size 증가가 어떤 장점과 비용을 동시에 만드는가?”

---

## CF-DECK-002 — Strong Archetype vs Flexible Build

### Strong Archetype Advantages
- Build Fantasy 선명
- Synergy 발견 쉬움
- Reward 의미 명확

### Flexible Build Advantages
- Pivot 가능
- RNG 회복
- Encounter 적응

### Hidden Variable
- Run length
- Reward frequency
- Encounter variability
- Early information
- Class pre-definition

### Resolution
`Build Commitment × Pivot Cost × Run Information`을 함께 본다.

---

## CF-DECK-003 — High RNG vs Controlled RNG

### Hidden Variable

> **RNG를 플레이어가 읽고 조작하는 행위가 Core Decision인가?**

### Resolution
높은 RNG 자체는 문제도 장점도 아니다.

`RNG Response Agency`를 평가한다.

---

## CF-DECK-004 — Horizontal Choice vs Vertical Power

### Evidence A
Slay the Spire — Contextual value / Build diversity.

### Evidence B
Balatro — Explosive scoring Engine.

### Adjacent
Vampire Survivors — Vertical Power Reward.

### Hidden Variable
Product Promise.

### Resolution
Power Explosion을 금지하지 않는다. Power가 증가한 뒤에도 Deckbuilding 판단이 남아 있어야 하는가는 게임의 Promise에 따라 별도 검토한다.

---

## CF-DECK-005 — Card Removal Mandatory vs Optional

### Hidden Variable
- Draw limitation
- Pool dilution
- Replacement model
- Deck cycling
- Card permanence

### Resolution

> **Removal Feature가 아니라 Pool Quality Control 수단의 존재를 검토한다.**

---

## CF-DECK-006 — Perfect Balance vs Broken Engine Fantasy

### Evidence A
Slay the Spire — Pick Rate + Win Rate 기반 Balance.

### Evidence B
Balatro — 강한 Synergy 발견의 재미가 완벽한 균형보다 중요할 수 있음.

### Hidden Variable
- Competitive vs Single-player
- Engine Fantasy
- Run Reset
- Exploit Permanence
- Strategy가 Decision을 제거하는가

### Resolution
모든 Build의 Win Rate를 동일하게 맞추는 것을 Genre Core로 두지 않는다.

대신:
1. Universal Best가 되는가?
2. 발견 후 Decision이 사라지는가?
3. 다른 Build가 실질적으로 무의미해지는가?

를 본다.

---

# 8. AI Tester Metric Map

Metric은 Criteria가 아니다. Threshold는 각 게임별 Validation Planner가 잠근다.

## 8.1 Build Metrics

| Metric | Type | Purpose |
|---|---|---|
| Build Diversity | Machine | Build Cluster 분포 |
| Build Convergence | Machine | 특정 Build 집중도 |
| Build Pivot Rate | Machine | Run 중 Build 변경 빈도 |
| Early Choice → Final Build Correlation | Machine | 초반 Lock 정도 |
| Build Formation Turn | Hybrid | Build가 나타나는 시점 |
| First Synergy Turn | Hybrid | 최초 Synergy 시점 |

**Guardrail:** Build Diversity 증가 ≠ Human Replayability 증가.

## 8.2 Card Metrics

| Metric | Type |
|---|---|
| Pick Rate | Machine / Observed-capable |
| Usage Rate | Machine |
| Conditional Win Rate | Machine / Observed-capable |
| Dead Pick Rate | Machine |
| Dead Draw Rate | Machine |
| Universal Pick Rate | Machine |
| Never-used Pick Rate | Machine |

## 8.3 Deck / Pool Metrics

| Metric | Type |
|---|---|
| Average Deck / Pool Size | Machine |
| Removal Rate | Machine |
| Transform Rate | Machine |
| Draw Consistency | Machine |
| Key Card Availability | Machine |
| Hand Clog Rate | Machine |
| Actionable Card Ratio | Machine |
| Pool Size → Outcome Curve | Machine |

## 8.4 Strategy Metrics

| Metric | Type |
|---|---|
| Dominant Strategy Concentration | Machine |
| Strategy Success Distribution | Machine |
| Archetype Diversity | Machine |
| Encounter-specific Strategy Shift | Machine |
| Decision Entropy by Run Phase | Machine |

## 8.5 Reward Metrics

| Metric | Type |
|---|---|
| Skip Rate | Machine |
| Reward Choice Concentration | Machine |
| Reward Replacement Rate | Machine |
| Reward Never-used Rate | Machine |
| Reward Regret | Human / Hybrid |

## 8.6 Run Metrics

| Metric | Type |
|---|---|
| Average Run Length | Machine |
| Build Formation Turn | Hybrid |
| First Synergy Turn | Hybrid |
| Power Spike Timing | Machine + Human Interpretation |
| Last Meaningful Build Change | Hybrid |
| Failure Cause Distribution | Hybrid |

## 8.7 RNG / Availability Metrics

| Metric | Type |
|---|---|
| Key Piece Miss Rate | Machine |
| Combo Completion Probability | Machine |
| Reroll Usage | Machine |
| Search Usage | Machine |
| Retain Usage | Machine |
| Uncontrollable Failure Rate | Machine + Human Attribution |
| Draw Variance | Machine |

## 8.8 AI Tester Interpretation Limits

AI Tester가 직접 결론내리지 않는 항목:
- 재미
- Build 만족감
- Synergy 발견의 짜릿함
- Replay Desire
- 공정성
- 카드 텍스트 가독성
- Power Fantasy 충족

AI Tester는:

```text
분포
편향
수렴
성공률
빈도
Availability
State Transition
```

을 측정한다.

Human Test는 그것이 좋은 경험인지 판단한다.

---

# 9. Human Validation Map

## H-DECK-001 — Build Recognition
> 플레이어가 현재 자신의 Build가 무엇을 잘하는지 설명할 수 있는가?

## H-DECK-002 — Reward Tension
> 카드 Reward에서 실제로 둘 이상을 고민하는가?

관찰:
- Decision Time
- Reason for Pick
- Skip Reason
- Regret

## H-DECK-003 — RNG Fairness
> 패배를 “내 덱/판단의 문제”와 “그냥 안 나옴” 중 어떻게 해석하는가?

## H-DECK-004 — Synergy Readability
> 강한 조합을 발견했을 때 왜 강한지 이해하는가?

## H-DECK-005 — Build Commitment
> 초반 선택 때문에 미래 보상이 달라지는 것을 “내가 빌드를 만들었다”고 느끼는가, “처음 선택에 묶였다”고 느끼는가?

## H-DECK-006 — Pivot Legibility
> Build를 바꿀 기회와 비용을 인식하는가?

## H-DECK-007 — Late-run Decision Preservation
> Engine 완성 후에도 새로운 판단이 남는가?

## H-DECK-008 — Cognitive Load
관찰:
- 카드 Text 이해
- Keyword Recall
- Tooltip Dependency
- 카드 관계 설명
- 신규 카드 노출 속도

---

# 10. Scale Handoff Candidates

이번 문서에서는 Scale Core로 승격하지 않는다.

## SCALE_HANDOFF-DECK-001 — Interaction Regression Explosion

Deckbuilding의 실제 QA 비용은 카드 수보다:
- Effect Family
- Status
- Relic
- Enemy
- Sequence
- Upgrade

상호작용 조합에서 폭증할 수 있다.

Supporting Evidence:
- Slay the Spire — 높은 QA 비용 / 조합 복잡도
- Balatro — 조합 QA 폭증
- Peglin — 작은 Core 이후 Data/Meta 확장

추후 `Genre × Scale Deep Extraction`에서 재검토.

---

## SCALE_HANDOFF-DECK-002 — Data Content is Cheap Only Until Balance/Tooltip Cost Dominates

Adjacency:
- Luck be a Landlord
- Brotato

Data-only Content는 Asset 비용을 낮추지만:
- Balance
- Tooltip
- Regression
- Discovery

비용을 제거하지 않는다.

---

## SCALE_HANDOFF-DECK-003 — Familiar Rule Base as Cognitive Budget

Balatro의 강한 Lesson:

> 익숙한 Rule Base가 새로운 Modifier를 학습할 인지 예산을 만든다.

이는 Deckbuilding Genre Core라기보다 `Novel Grammar × Content Complexity × Team Scope` 교차 분석 가치가 높다.

---

# 11. Universal Reclassification Candidates

## UC-RECLASS-CAND-001 — Usage Metric must be paired with Outcome / Context

Slay the Spire의 “선택률과 승률을 함께 본다”는 원리는 Deckbuilding을 넘어 아이템, 스킬, 정책, 행동, 유닛 평가에도 적용 가능하다.

### Candidate Universal Rule

> **선택 빈도만으로 설계 가치를 판단하지 않고, Context와 Outcome을 함께 본다.**

**Status:** `UNIVERSAL RECLASSIFICATION CANDIDATE`

---

## UC-RECLASS-CAND-002 — Pool Growth ≠ Quality Growth

Deckbuilding에서 분명하지만 Inventory, Roster, Skill Pool, Tool Set에도 확장 가능성이 있다.

현재 Evidence가 Deckbuilding에 치우쳐 있으므로 Universal 승격 금지.

---

# 12. Evidence Gaps

## GAP-DECK-001 — Build Pivot Telemetry
부족:
- Pivot Rate
- Pivot Success
- Early Lock
- Player-perceived lock

## GAP-DECK-002 — Reward Skip / Regret
부족:
- Reward Skip Rate
- “받지 않는 것이 성장”인 구조의 실제 데이터
- Pick 후 교체/미사용 비율

## GAP-DECK-003 — Removal Requirement Boundary
Removal이 좋은 사례는 있으나 Removal이 필요 없는 Primary Deckbuilder와 비교한 명확한 Evidence가 부족하다.

## GAP-DECK-004 — Build Formation Timing
Build가 언제 형성되어야 좋은지에 대한:
- Telemetry
- Human Satisfaction
- Run Length Correlation

이 부족하다.

## GAP-DECK-005 — Underperforming Deckbuilder Controls
성공작 중심 Reference라 실패 구조의 실제 사례가 부족하다.

## GAP-DECK-006 — Synergy Readability
Primary 사례의:
- Tooltip Use
- Keyword Recall
- Newcomer Comprehension
- Wiki Dependence

정량 자료 부족.

## GAP-DECK-007 — Encounter Pressure
Slay the Spire는 강한 근거지만 두 번째 독립 Primary Source 부족.

## GAP-DECK-008 — Peglin Design Depth
현재 REF-34는 Production Case 중심이다. Orb Pool Lifecycle, Relic Synergy, Reward/Removal, Encounter Pressure, Run Pacing을 다루는 별도 Design Case Study가 필요하다.

---

# 13. Additional Deckbuilding References Needed

아래는 **향후 Research Target**이며 현재 Core Evidence가 아니다.

## P0 — Monster Train
Research:
- Strong Archetype
- Unit/Card Upgrade
- Duplication
- Multi-floor Encounter Pressure
- Pivotability
- Build Formation Timing

목적:
`GC-DECK-002 / 007 / 008 / 010` 강화.

## P0 — Vault of the Void
Research:
- Draw / Discard Control
- Deck Editing
- Availability Consistency
- Removal Boundary

목적:
`GC-DECK-003 / 005` 강화.

## P0 — Wildfrost
Research:
- Sequencing
- Turn Timing
- Draw Control
- Enemy Pressure
- Synergy Readability

목적:
`GC-DECK-008 / 009 / 011` 강화.

## P1 — Griftlands
Research:
- Dual Deck Systems
- Build Identity across Combat/Negotiation
- Reward Competition
- Narrative Hybrid

## P1 — Roguebook
Research:
- Deck Size Pressure
- Exploration / Reward Routing
- Card Acquisition
- Build Formation Timing

## P1 — Inscryption
Research:
- Deckbuilding Hybrid
- Rule Shifts
- Onboarding
- Content / Replay Boundary

주의: Narrative Hybrid가 강하므로 pure Deckbuilding Primary Evidence로 바로 사용하지 않는다.

## P1 — Dominion / Digital Implementations
Research:
- Pool Lifecycle
- Acquisition Economy
- Deck Thinning
- Engine Balance
- Deck Size

---

# 14. Promotion Table

| ID | Name | Status | Confidence |
|---|---|---|---|
| GC-DECK-001 | Contextual Card Value | **PROVISIONAL CORE** | VERY HIGH |
| GC-DECK-002 | Build Identity Formation | **PROVISIONAL CORE** | HIGH |
| GC-DECK-003 | Availability / RNG Control | **PROVISIONAL CORE** | HIGH |
| GC-DECK-004 | Synergy Changes Decisions | **PROVISIONAL CORE** | HIGH |
| GC-DECK-005 | Pool Growth Needs Quality Control | **PROVISIONAL CORE** | MEDIUM-HIGH |
| GC-DECK-006 | Reward Choice vs Future Consistency | KEEP AS CANDIDATE | MEDIUM |
| GC-DECK-007 | Build Pivotability | KEEP AS CANDIDATE | MEDIUM |
| GC-DECK-008 | Encounter Pressure | KEEP AS CANDIDATE | MEDIUM |
| GC-DECK-009 | Synergy Readability | KEEP AS CANDIDATE | MEDIUM |
| GC-DECK-010 | Build Formation Timing | KEEP AS CANDIDATE | MEDIUM-LOW |
| GC-DECK-011 | Sequencing Value | KEEP AS CANDIDATE | LOW-MEDIUM |
| GC-DECK-012 | Vertical Power vs Decision Preservation | KEEP AS CANDIDATE | MEDIUM-LOW |

## Existing Core Audit Summary

| Previous Core | Decision |
|---|---|
| GC-DECK-001 Contextual Card Value | **KEEP + STRENGTHEN** |
| GC-DECK-002 Build Identity / Pivotability | **SPLIT** |
| GC-DECK-003 RNG Control | **KEEP + REFRAME AS UC SPECIALIZATION** |

---

# 15. Deckbuilding Reviewer Default Set

신규 Deckbuilding / Deckbuilding Hybrid 기획을 검토할 때 우선 적용할 12개 질문.

1. **Contextual Value**  
   모든 상황에서 좋은 카드가 존재하는가, 아니면 현재 Build/적/자원에 따라 카드 가치가 실제로 바뀌는가?

2. **Build Identity**  
   Run이 진행되면서 이전 선택 때문에 미래 선택 가치가 달라지는 Build Identity가 실제로 형성되는가?

3. **Availability Agency**  
   좋은 카드를 Pool에 넣은 뒤 실제로 사용할 가능성을 플레이어가 조절할 수 있는가?

4. **Synergy Decision**  
   시너지는 숫자만 키우는가, 아니면 이후 카드·자원·순서 선택을 바꾸는가?

5. **Pool Quality**  
   카드를 더 얻는 것 외에 Pool의 품질·일관성을 관리하는 방법이 있는가?

6. **Reward Choice**  
   Reward에서 ‘받지 않는 것’ 또는 다른 방향을 택하는 것이 합리적인 상황이 있는가?

7. **Commitment / Pivot**  
   Build에 투자한 대가가 있으면서도 잘못된 초반 선택에서 회복할 경로가 있는가?

8. **Encounter Questions**  
   적/Encounter가 다른 Build와 카드에 다른 질문을 던지는가, 아니면 HP와 공격력만 증가하는가?

9. **Synergy Readability**  
   플레이어가 강한 조합을 발견하고 왜 강한지 설명할 수 있는가?

10. **Build Pacing**  
    Build가 Run의 어느 시점에 형성되며, 너무 늦거나 너무 빨리 해결되지 않는가?

11. **Dominant Strategy**  
    특정 카드·유물·Engine이 모든 Build에 들어가거나 모든 Encounter를 같은 방법으로 해결하지 않는가?

12. **Machine vs Human Evidence**  
    수렴·편향은 AI Tester로 측정하고, Fun·Build Fantasy·Readability·Fairness는 Human Test로 분리했는가?

---

# 16. Default Metric Bundle for Deckbuilding Validation

정식 Criteria는 게임별 Validation Planner가 잠근다.

## Structural — Machine
- Pick Rate
- Conditional Win Rate
- Universal Pick Rate
- Dead Pick Rate
- Dead Draw Rate
- Build Diversity
- Build Convergence
- Build Pivot Rate
- Early Choice → Final Build Correlation
- Reward Choice Concentration
- Skip Rate
- Average Pool Size
- Removal Rate
- Key Card Availability
- Hand Clog Rate
- Dominant Strategy Concentration

## Human
- Build Recognition
- Build Satisfaction
- Synergy Readability
- Reward Decision Tension
- Perceived Fairness
- RNG Attribution
- Cognitive Load
- Replay Intent

## Hybrid
- Build Formation Turn
- First Synergy Turn
- Last Meaningful Build Change
- Power Spike Timing
- Failure Cause Distribution
- Perceived Variety
- Difficulty
- Run Pacing
- Build Formation Quality
- Frustration

---

# 17. Self-Review Result

- **Check 1 — Card UI ≠ Deckbuilding:** PASS
- **Check 2 — Single-game Generalization:** PASS WITH GAPS
- **Check 3 — Universal Duplicate:** PASS
- **Check 4 — Solo Rule contamination:** PASS
- **Check 5 — Adjacent Evidence Weight:** PASS
- **Check 6 — Card Count ≠ Depth:** PASS
- **Check 7 — Metric ≠ Criteria:** PASS
- **Check 8 — Machine ≠ Human Fun:** PASS
- **Check 9 — Counter / Subtype:** PASS
- **Check 10 — Reviewer Usability:** PASS

---

# 18. Final Position

현재 Studio OS Deckbuilding Knowledge Base에서 우선 Provisional Core로 사용할 항목은 5개다.

1. `GC-DECK-001 — Contextual Card Value`
2. `GC-DECK-002 — Build Identity Formation`
3. `GC-DECK-003 — Availability / RNG Control`
4. `GC-DECK-004 — Synergy Must Change Decisions`
5. `GC-DECK-005 — Pool Growth Needs Quality Control`

다음 단계 Candidate:
6. Reward Choice
7. Pivotability
8. Encounter Pressure
9. Synergy Readability
10. Build Formation Timing
11. Sequencing
12. Vertical Power vs Decision Preservation

현재 가장 중요한 Evidence Gap은:

> **Pivot / Reward / Removal Boundary / Build Timing / Underperforming Control**

이다.

다음 Reference 확장은 성공작 수를 늘리는 것보다:

> **왜 덱이 고착되는가 / 언제 Pivot이 가능한가 / Reward가 언제 Auto-pick이 되는가 / Pool Quality를 어떻게 관리하는가**

에 실제 개발자 분석 또는 Telemetry가 존재하는 사례를 우선 추가하는 편이 가치가 높다.

---

# 19. Source Trace

## Primary
- REF-04 — Slay the Spire
- REF-05 — Balatro
- REF-20 — Dicey Dungeons
- REF-34 — Peglin

## Secondary
- REF-18 — Loop Hero
- REF-22 — Stacklands

## Adjacent
- REF-19 — Cultist Simulator
- REF-26 — Luck be a Landlord
- REF-36 — Brotato
- REF-12 — Vampire Survivors

## Baseline
- STUDIO_CORE_CANDIDATES_v0.2
- Studio OS — Evidence-Based Core Extraction Master Prompt v0.2
- Studio OS — Deckbuilding Genre Core Deep Extraction Prompt v0.1

**Traceability Rule:**  
Core는 원본 Reference를 대체하지 않는다. 신규 프로젝트 Review에서 Core가 위험 신호를 발생시키면 해당 Core의 Primary Reference로 다시 내려가 문제-해결 조건과 Trade-off를 확인한다.
