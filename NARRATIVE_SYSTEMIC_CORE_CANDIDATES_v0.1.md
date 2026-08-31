# NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1

**Studio OS — Narrative / Systemic Narrative Genre Core Deep Extraction**  
**Document:** `NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1`  
**Status:** `APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE`  
**Purpose:** 신규 Choice-based Narrative / Interactive Fiction / Narrative RPG / Narrative Management / State-reactive Narrative / Systemic Narrative / Emergent Narrative / Narrative Adventure / Narrative Hybrid 기획 평가용 Genre-specific Reviewer Knowledge Base  
**Baseline:** `STUDIO_CORE_CANDIDATES_v0.2`  
**Extraction Prompt:** `Studio OS — Narrative / Systemic Narrative Genre Core Deep Extraction Prompt v0.1`  
**Provisional Genre Cores:** `GC-NARR-001`, `GC-NARR-002`, `GC-NARR-003`  
**Candidates:** `GC-NARR-005 ~ GC-NARR-008`, `GC-NARR-010 ~ GC-NARR-011`  
**Merge Candidates:** `GC-NARR-004 → GC-NARR-001`, `GC-NARR-009 → GC-NARR-001 / UC-DESIGN-002`  
**Pending:** `Additional Evidence / Prototype Validation / Internal Evidence`  
**Evidence Rule:** Narrative Promise와 Subtype을 먼저 구분하며, Authored / State-reactive / Systemic / Emergent Narrative의 동일 Mechanism이 확인될 때만 Genre Core로 승격한다. Scope / Branch efficiency / localization cost는 Genre Mechanic과 분리한다.

---

# 1. Executive Summary

이번 Deep Extraction의 핵심 결론은 다음과 같다.

1. **Narrative Depth는 Text / Branch / Ending 수가 아니라 `Player Action → Persistent State → Later Response → Changed Meaning`의 연결 품질로 평가해야 한다.**

2. 기존 `GC-NARR-001 — Recontextualization over Branch Count`는 **STRENGTHEN / PROVISIONAL CORE 유지**가 맞다.
   - 다만 기존 문장에 섞여 있던 `State-reactive Narrative가 제작비 효율이 좋다`는 Production 주장은 Genre Core에서 제거하고 Scale Handoff로 보낸다.
   - Genre Core에 남는 것은:
     > **Branch 수가 아니라 Player History와 현재 State가 이후 Content의 의미·조건·결과를 실제로 바꾸는가**
     이다.

3. 신규 Provisional Core로 가장 강한 두 축은:
   - `GC-NARR-002 — Core Actions Should Carry Both Systemic and Narrative Meaning`
   - `GC-NARR-003 — Delayed Consequences Need Persistent State and Causal Legibility`

4. 따라서 현재 우선 Provisional Narrative Core는 총 3개다.
   1. `GC-NARR-001 — State-reactive Recontextualization over Branch Count`
   2. `GC-NARR-002 — System / Narrative Choice Coupling`
   3. `GC-NARR-003 — Persistent and Legible Consequence`

5. 다음은 중요하지만 현재 Evidence / Human Telemetry가 부족해 Candidate로 유지한다.
   - Branch Convergence with Memory
   - Character / World Memory
   - Roleplay Choice vs Dominant Utility
   - Failure-as-Content
   - Relationship State Depth
   - Repeated Verb Recontextualization
   - Emergent Story Coherence
   - Narrative Decision Density / Pacing

6. Source Weight는 다음처럼 재분류한다.
   - `REF-10 80 Days` → **Tier A / Primary**
   - `REF-09 Reigns` → **Tier A / Primary**
   - `REF-23 Citizen Sleeper` → **Tier B / Strong Specialized Narrative Evidence**
   - `REF-01 Papers, Please` → **Tier B / System-Narrative Hybrid**
   - `REF-15 This War of Mine` → **Tier B / Systemic Human-cost Narrative**
   - `REF-13 RimWorld` → **Tier B / Emergent Narrative**
   - `REF-19 Cultist Simulator` → **Tier B / Experimental State-driven Narrative**

   Citizen Sleeper는 구조 분석은 강하지만 현재 Studio Reference의 직접 Source 깊이가 80 Days / Reigns보다 약해 Tier A로 올리지 않는다.

7. Narrative에서 특히 중요한 구분은 다음이다.

```text
Branch Width
≠
Narrative Agency
```

```text
State Count
≠
Narrative Reactivity
```

```text
Resource Change
≠
Narrative Meaning
```

```text
Random Event
≠
Emergent Story
```

8. Structural / Machine Validation은 매우 유용하지만 주로 다음을 검증한다.
   - State
   - Trigger
   - Reachability
   - Branch
   - Consequence Activation
   - Continuity
   - Coverage
   - Contradiction
   - Repetition

   다음은 Human Evidence 없이는 결론내리지 않는다.
   - Narrative Agency
   - Meaningful Choice
   - Emotional Impact
   - Character Coherence
   - Story Ownership
   - Recontextualization Quality
   - Consequence Fairness

9. Narrative Reviewer의 가장 중요한 질문은 다음과 같다.

> **“플레이어의 행동이 단순히 다음 장면을 고르는가, 아니면 게임 상태와 세계의 기억을 바꾸어 이후 같은 사건·행동·관계의 의미까지 바꾸는가?”**

10. 현재 가장 큰 Evidence Gap은:
   - Choice → Later Consequence actual telemetry
   - Consequence Recall
   - Branch / State Reachability
   - Character Continuity
   - Cosmetic vs Persistent Choice
   - Roleplay Choice Distribution
   - Event Repetition Fatigue
   - Failure-as-Content
   - Emergent Story Recall
   - Localization / State QA postmortem
   - Underperforming Narrative Control Case

---

# 2. Narrative / Systemic Narrative Genre Definition

모든 Story-heavy Game을 같은 Narrative Core로 평가하지 않는다.

## 2.1 Linear Authored Narrative

작가가 작성한 Sequence와 Payoff가 주요 상품이다.

```text
Scene A
↓
Scene B
↓
Scene C
```

플레이어가 Story State를 크게 바꾸지 않아도 성립한다.

---

## 2.2 Branching Narrative

명시적 Choice로 Authored Path가 갈라진다.

```text
Choice
├─ Path A
└─ Path B
```

Branch 자체가 Product Value일 수 있다.

---

## 2.3 State-reactive Narrative

같은 Content가 현재 State에 따라:
- 문구
- 접근성
- 관계
- Outcome
- Meaning

을 바꾼다.

```text
Same Event
+
Different Player State
↓
Different Meaning / Response
```

---

## 2.4 Narrative RPG

Player Role, Resource, Relationship, Character State와 Story Choice가 결합한다.

---

## 2.5 Narrative Management

돈·시간·식량·업무·인력 같은 관리 Choice가 동시에 Story Meaning을 만든다.

---

## 2.6 Systemic Narrative

게임의 반복 System과 Narrative State가 서로를 지속적으로 바꾼다.

```text
Player Action
↓
System State
↓
Narrative Response
↓
Future System / Choice Context
↓
New Narrative Meaning
```

---

## 2.7 Emergent Narrative

작가가 특정 Sequence를 직접 작성하지 않아도:
- Character
- Event
- Resource
- Failure
- Relationship
- World State

상호작용을 플레이어가 Story로 해석한다.

---

## 2.8 Discovery Narrative

플레이어가 Story Path를 직접 “선택”하기보다:
- World
- Text
- Environment
- Evidence

를 탐색하면서 서사를 구성한다.

Systemic Narrative Core를 자동 적용하지 않는다.

---

# 3. Narrative Inclusion Test

강한 Narrative Agency / Reactivity Core를 적용하기 전에 다음을 확인한다.

## A. Narrative Promise

이 게임이 약속하는 Narrative Experience는 무엇인가?

- authored story participation
- roleplay
- relationship
- consequence
- own story
- world discovery
- emergent story

---

## B. Player Action

플레이어가 실제로 Story State를 변경하는 행동을 하는가?

---

## C. State Persistence

선택 결과가 후속 Event까지 남는가?

---

## D. Recontextualization

같은:
- 장소
- Character
- Action
- Event

가 현재 State 때문에 다른 의미를 갖는가?

---

## E. Consequence

선택이 최소 하나 이상의 후속 State를 바꾸는가?

- Relationship
- Resource
- Access
- Character
- Event
- World
- Ending

---

## F. Recognition

플레이어가:

> “현재 이 결과가 왜 발생했는가?”

를 이전 Choice와 연결할 수 있는가?

---

## G. Narrative Agency

Systemic / State-reactive Narrative를 약속한다면 플레이어가:

> “이 상황이 이렇게 된 이유 중 일부는 내가 이전에 한 행동 때문이다.”

라고 설명할 수 있는가?

---

# 4. Studio OS Narrative Core Loop

State-reactive / Systemic Narrative의 기본 구조 후보:

```text
Observe Narrative Context
        ↓
Choose / Act
        ↓
System + Narrative State Change
        ↓
Immediate Response
        ↓
Persistent Consequence
        ↓
Later Event
        ↓
State-dependent Recontextualization
        ↓
Player Re-evaluates Next Choice
```

다음만으로는 강한 Systemic Narrative로 인정하지 않는다.

```text
Dialogue Choice
↓
+1 Affection
↓
Next Dialogue
↓
+1 Affection
```

또는:

```text
Choice A
↓
Different Line
↓
Main Path
↓
No Later Effect
```

단, Linear / Authored Narrative에서는 이 구조가 곧 결함이라는 뜻이 아니다.

---

# 5. Source Classification

# 5.1 Tier A — Primary Narrative / Systemic Narrative Evidence

## REF-10 — 80 Days

**Subtype:** `Adaptive Interactive Fiction / State-reactive Narrative`  
**Evidence Strength:** VERY HIGH

### Strong Evidence Areas
- Route-as-Story
- Adaptive Narrative
- State-reactive Content
- Resource → Narrative Choice
- Location / Time / Previous Event Condition
- Content Selectivity
- Replay Variation
- Narrative State QA
- System / Story Integration

### Key Source-derived Observation

이동 경로와 돈·시간·건강·수하물 선택이 곧 어떤 Story와 Resource Problem을 만날지를 결정한다.

Reference의 핵심 Lesson:

> 이동 / 자원 선택을 곧 서사 선택으로 만들면 게임과 이야기가 통합된다.

Primary Warning:

> 상태 반응형 구조 없이 Branch / Text 양만 늘리면 강점이 재현되지 않는다.

### Evidence Quality

Developer Postmortem / GDC Narrative Talk 기반이 포함되어 있어 현재 Narrative Reference 중 가장 강하다.

---

## REF-09 — Reigns

**Subtype:** `Choice-based Adaptive Narrative`  
**Evidence Strength:** HIGH

### Strong Evidence Areas
- Binary Choice
- Long-term State
- Resource Consequence
- Narrative Card Grammar
- Failure-as-Content
- Adaptive Narrative
- Low-input / multi-axis outcome

### Key Source-derived Observation

매우 작은 입력 문법에서도 하나의 Choice가 여러 State와 장기 결과에 연결되면 복합적인 판단이 가능하다.

또한 결과가 단순히 예측 불가능하기만 하면:

> 전략 / Roleplay가 아니라 Guess

가 될 수 있으므로 신호와 학습 가능성이 필요하다는 Warning이 있다.

### Evidence Quality

Developer-authored adaptive narrative analysis와 developer interview가 포함된 Primary Reference.

---

# 5.2 Tier B — Strong Narrative / System Hybrid

## REF-23 — Citizen Sleeper

**Subtype:** `Narrative RPG / Narrative Economy`  
**Evidence Strength:** HIGH as Specialized Support

### Strong Evidence Areas
- Dice / Action Allocation
- Relationship
- Clock
- Limited Action
- Narrative Opportunity Cost
- Daily Routine
- Character Condition
- System / Story Coupling

### Key Source-derived Observation

주사위라는 제한 행동 자원을:
- 생존
- 노동
- 관계
- Story

가 함께 경쟁하게 만들어 텍스트 Choice를 전략 Choice와 같은 체계에 묶는다.

### Classification Reason

Studio Secondary Reference의 분석은 강하지만 현재 직접 Source가 Official Page 중심이므로 Tier A보다 낮게 둔다.

---

## REF-01 — Papers, Please

**Subtype:** `Operations / Narrative Bureaucracy Hybrid`

### Use
- Repeated Player Verb
- Moral / Political Context
- Family State
- Delayed Consequence
- Resource Cost
- System → Narrative Integration

### Strong Source-derived Observation

같은 승인/거절 입력에:
- 돈
- 시간
- 가족
- 정치
- 인간적 예외

를 겹쳐 업무와 Story를 하나의 판단으로 만든다.

### Boundary

Pure Narrative Game이 아니다.

Narrative Core 전체를 단독 지지하지 않는다.

---

## REF-15 — This War of Mine

**Subtype:** `Survival Management / Systemic Human-cost Narrative`

### Use
- Character State
- Scarcity
- Human Cost
- Moral Consequence
- Attrition
- Failure
- Theme-System Integration

### Strong Source-derived Observation

Reference의 Core Principle:

> 테마는 플레이어가 반복하는 행동에 내장될 때 가장 강하다.

또:

> 우울한 분위기와 잔혹한 Choice만 복제하는 것이 아니라 실제 생존 System이 Choice의 원인이 되어야 한다.

### Boundary

Management Resource Rule 자체는 Narrative Core로 복제하지 않는다.

Narrative에서는:

> Resource Decision이 인간적 / 관계적 의미를 갖는가?

만 사용한다.

---

## REF-13 — RimWorld

**Subtype:** `Emergent Story / Colony Simulation`

### Use
- Character State
- Event
- Persistent Consequence
- Loss
- Relationship
- Emergent Story
- Selective Simulation

### Boundary

Authored Branching Narrative의 Evidence로 사용하지 않는다.

RimWorld의 핵심 Narrative Value는:
- 작가가 정해둔 Path
보다
- Character / State / Event Interaction

에 가깝다.

---

## REF-19 — Cultist Simulator

**Subtype:** `Experimental Systemic Narrative / Card Simulation`

### Use
- Discovery
- Text Fragment
- Common System Grammar
- Interpretation
- State-driven Story

### Limitation

현재 Studio Reference는 UI Grammar / Discovery / cognitive load 비중이 높으므로 Narrative Core 승격의 중심 Evidence로 사용하지 않는다.

---

# 5.3 Tier C — Adjacent / Control Evidence

특정 Mechanism의 Boundary에만 사용한다.

- Deduction / Discovery Game
- Linear Adventure
- Roguelike Narrative
- Management / Strategy
- Exploration Narrative

Tier C만으로 Provisional Narrative Core를 승격하지 않는다.

---

# 6. Existing Core Audit

# GC-NARR-001 — State-reactive Recontextualization over Branch Count

**Decision:** `STRENGTHEN / REFRAME`  
**Status:** `PROVISIONAL CORE`  
**Origin:** `EXISTING GC REFINEMENT`

## Previous Rule

> 분기 수를 늘리는 것보다 동일 사건이 Player State와 이전 선택 때문에 다른 의미와 결과를 갖도록 하는 편이 시스템 내러티브와 Scope 양쪽에서 효율적일 수 있다.

## Audit Result

Genre Mechanic과 Production Claim을 분리한다.

### Genre Core에 유지
- State Reactivity
- Player History
- Recontextualization
- Branch Convergence with persistent state

### Scale Handoff로 이동
- Branch Tree보다 제작비가 효율적이다.
- 작문량 감소.
- QA 비용 감소 / 증가.

## Refined Pattern

Narrative Agency는:
- Path 수
- Ending 수
- Dialogue Choice 수

보다 과거 Choice와 현재 State가 이후 콘텐츠의:
- Meaning
- Access
- Response
- Choice Value
- Outcome

를 바꾸는 정도에서 발생할 수 있다.

## Rule

> **Narrative Choice의 깊이를 Branch 수로 판단하지 않는다. State-reactive / Systemic Narrative를 약속한다면 Player History와 현재 State가 이후 Content의 의미·조건·결과를 실제로 바꾸는지를 평가한다. Branch가 다시 합쳐져도 History가 남아 있으면 자동 Fake Choice로 보지 않는다.**

## Mechanism

Weak Branching:

```text
Choice A
├─ Text A
└─ Text B
     ↓
Same State
↓
Same Later Meaning
```

State-reactive:

```text
Choice A
↓
Persistent State
↓
Later Shared Event
↓
Different Response / Meaning / Option
```

## Primary Evidence

### 80 Days
- Route / Time / Resource / Previous Event가 콘텐츠를 재구성.
- Branch Tree 자체보다 adaptive state structure가 핵심.
- 이동 / 자원 선택이 Story Selection이 됨.

### Reigns
- 작은 이진 Choice가 여러 State / 장기 결과와 연결.
- Reused event grammar가 State와 consequence로 재맥락화될 수 있음.

## Secondary Evidence

### Papers, Please
같은 승인/거절 입력이:
- 정치
- 생계
- 인간적 예외
때문에 다른 의미를 가짐.

### This War of Mine
같은 식량 / 약품 / 행동이 Character 상태와 생존 상황에 따라 다른 인간적 의미를 가짐.

## Counter Evidence

### Pure Visual Novel / Authored Branching
Distinct Route 자체가:
- Character Arc
- Theme
- authored payoff

의 Product Value일 수 있다.

이 경우 State reuse보다 Branch Width가 의도된 가치다.

## Applies To

강하게:
- State-reactive Narrative
- Systemic Narrative
- Narrative RPG
- Adaptive Interactive Fiction

조건부:
- Branching Narrative

약하게:
- Linear Authored Narrative

## Boundary / Exceptions

“Branch를 만들지 말라”는 Rule이 아니다.

핵심은:

> Branch 수를 Agency의 Proxy로 사용하지 않는다.

## Observed Metric

Source에서 공통 telemetry 없음.

## Candidate Metric — Structural / Machine

- State-reactive Event Rate
- State-reactive Text Rate
- Branch Convergence with State Persistence
- Event Condition Diversity
- Action → Persistent State Rate
- Recontextualized Event Candidate Rate

`Recontextualized Event`의 의미 판단은 model-dependent / Hybrid.

## Candidate Metric — Human

- Recontextualization Recognition
- Narrative Agency
- “같은 장면이 내 상태 때문에 다르게 느껴졌다” 평가

## Validation Type

Structural + Human / Hybrid.

## AI Tester Applicability

HIGH for state / trigger integrity.  
LOW for narrative meaning.

## Confidence

**VERY HIGH**

## Reviewer Action

Branch / Ending 수를 들으면 먼저:

> **“이 선택이 나중에 어떤 State / Meaning으로 남는가?”**

를 묻는다.

---

# 7. Provisional Narrative Cores

# GC-NARR-002 — Core Actions Should Carry Both Systemic and Narrative Meaning

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

강한 Systemic Narrative / Narrative Hybrid 사례에서는 Story Choice가 별도 Dialogue Layer에만 존재하지 않는다.

플레이어가 반복하는:
- 이동
- 일
- 자원 배분
- 승인 / 거절
- 식량 사용

같은 Core Action이 동시에:
- System Outcome
- Relationship
- Moral Meaning
- Story State

를 바꾼다.

## Narrative Context

- Systemic Narrative
- Narrative Management
- Narrative RPG
- Adaptive Interactive Fiction

## Rule

> **Systemic Narrative를 약속한다면 핵심 Gameplay Action 중 일부가 동시에 System State와 Narrative Meaning을 바꾸어야 한다. Story Choice가 Core Play와 완전히 분리된 별도 메뉴로만 존재하는지 검토한다.**

## Mechanism

Separated Structure:

```text
Gameplay
↓
Resource Result
↓
Cutscene
↓
Narrative Choice
↓
Gameplay
```

Coupled Structure:

```text
Core Action
↓
Resource / Time / Risk Change
+
Relationship / Story / Moral State Change
↓
Future Choice Context
```

Coupling의 핵심은:

> 하나의 행동이 두 시스템을 동시에 진행한다.

는 것이다.

## Primary Evidence

### 80 Days

Reference의 가장 직접적 Lesson:

> 이동 / 자원 선택을 곧 서사 선택으로 만들면 게임과 이야기가 통합된다.

Route 선택이:
- 시간
- 돈
- 건강
- 다음 장소
- 만날 Story

를 동시에 결정한다.

### Reigns

단순 좌우 Choice가:
- State resource
- political consequence
- future narrative context

를 동시에 변경한다.

## Secondary Evidence

### Citizen Sleeper

하루의 제한 Dice를:
- 생존
- 관계
- 노동
- Story

가 공유하여 Narrative Choice에 Opportunity Cost를 부여한다.

### Papers, Please

승인 / 거절이라는 동일 행동이:
- 임금 / 벌금
- 가족 생존
- 정치
- 도덕적 선택

을 동시에 진행한다.

### This War of Mine

식량 / 약품 / 야간 행동이라는 생존 Choice가:
- Character 상태
- 죄책감 / 인간적 비용
- 생존 이야기

를 동시에 만든다.

## Counter Evidence

### Linear Authored Narrative

Gameplay와 Story가 분리되어도:
- pacing
- authored scene quality
- character arc

가 Product Promise라면 성립한다.

### Narrative Adventure

Core Gameplay가 이동 / 퍼즐이고 Story는 authored reward일 수 있다.

## Applies To

강하게:
- Systemic Narrative
- Narrative Management
- Narrative RPG

조건부:
- Adaptive Interactive Fiction

약하게:
- Linear Authored Narrative

## Boundary / Exceptions

모든 Gameplay Action에 Story 의미를 강제하지 않는다.

핵심은:

> Product Promise가 “플레이 자체가 Story를 만든다”라면 대표 Core Action에서 그 약속이 실제로 성립해야 한다.

## Observed Metric

현재 Reference에 공통 정량 telemetry 없음.

## Candidate Metric — Structural / Machine

- Action → System State Change Rate
- Action → Narrative State Change Rate
- Shared Action Coupling Rate
- Narrative Event → System State Change Rate
- System State → Narrative Event Activation Rate

`Meaning` 자체는 Machine으로 판정하지 않는다.

## Candidate Metric — Human

- System / Story Unity
- “Gameplay를 하다가 Story를 보는가, 플레이 자체가 Story인가?”
- Choice Meaning
- Narrative Agency

## Validation Type

Structural + Human.

## AI Tester Applicability

HIGH for state coupling.  
LOW for narrative meaning.

## Confidence

**HIGH**

## Reviewer Action

Narrative System이 있다면:

> **“이 게임의 가장 많이 반복하는 Player Verb가 Story를 어떻게 바꾸는가?”**

를 묻는다.

답이 없다면 `STORY_CORE_PLAY_SEPARATION_RISK`.

---

# GC-NARR-003 — Delayed Consequences Need Persistent State and Causal Legibility

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

강한 Choice Narrative 사례에서는 모든 Consequence를 즉시 보여주지 않는다.

Delayed Consequence는:
- surprise
- long-term payoff
- natural story

를 만들 수 있다.

그러나 과거 선택과 현재 결과를 연결할 수 없다면:
- agency
- roleplay
- learning

대신 Guess로 인식될 수 있다.

## Rule

> **Narrative Consequence가 지연될수록 원인 State는 지속되어야 하며, 결과가 나타났을 때 플레이어가 과거 Choice와 현재 Outcome의 인과를 되짚어 이해할 수 있어야 한다. 모든 결과를 사전 공개할 필요는 없지만 Consequence가 사후에도 임의 처벌처럼 보여서는 안 된다.**

## Mechanism

Too Immediate:

```text
Choice
↓
+10 / -10 표시
```

Narrative Choice가 계산 문제처럼 보일 수 있다.

Too Opaque:

```text
Choice
↓
20분 후 큰 처벌
↓
No clue / no memory
```

Agency보다 Guess가 된다.

Legible Delayed Consequence:

```text
Choice
↓
Persistent Flag / State
↓
World / Character Memory
↓
Later Trigger
↓
Recognizable Payoff
```

## Primary Evidence

### Reigns

Reference의 Warning:

> 결과가 예측 불가능하기만 하면 전략이 아니라 찍기가 된다. 신호와 학습 가능성이 필요하다.

즉:
- Consequence uncertainty는 가능하지만
- 완전한 causal opacity는 위험하다.

### 80 Days

Location / Time / Resource / Previous Event가 후속 Narrative Content 조건에 사용되는 State-reactive 구조가 장기 consequence를 지지한다.

## Secondary Evidence

### Papers, Please

- 판정 오류는 비교적 빠르게 알려 학습 가능.
- 인간적 / 정치적 장기 결과는 지연해 기대값 계산을 어렵게 함.

즉:
- immediate system feedback
- delayed narrative consequence

를 섞는다.

### Citizen Sleeper

Clock과 장기 관계 진행은 현재 행동을 미래 사건과 연결하는 legibility mechanism으로 분석된다.

## Counter Evidence

### Mystery / Tragedy / Horror

의도적으로 원인이 늦게 밝혀지거나 오해를 만드는 것이 Narrative Promise일 수 있다.

### Pure Roleplay

결과를 계산하지 못하는 선택이 자연스러운 Story를 만들 수도 있다.

## Applies To

- Choice-based Narrative
- State-reactive Narrative
- Narrative RPG
- Narrative Management

## Boundary / Exceptions

Causal Legibility는:

> 결과를 선택 시점에 수치로 미리 보여준다.

와 같지 않다.

다음도 Signal이 될 수 있다.

- Character reaction
- prior information
- tone
- relationship history
- world rule
- visible state
- recalled promise

## Observed Metric

공통 telemetry 없음.

## Candidate Metric — Structural / Machine

- Delayed Consequence Activation
- Consequence Latency
- Unresolved Consequence Count
- Choice → Later Trigger Dependency
- Forgotten Flag Candidate Rate
- Consequence State Duration

`Forgotten`의 의미 판단은 model-dependent.

## Candidate Metric — Instrumented

- Consequence Recall Prompt
- Choice Reversal / Reload after Consequence
- Time from Choice to Consequence

## Candidate Metric — Human

- Consequence Recognition
- Consequence Fairness
- Delayed Payoff Recognition
- “왜 이 일이 발생했는가?” Explanation

## Validation Type

Structural + Instrumented + Human.

## AI Tester Applicability

HIGH for trigger chain.  
Human required for causal understanding.

## Confidence

**HIGH**

## Reviewer Action

Delayed Consequence가 있다면:

> **“결과가 왔을 때 플레이어는 어떤 정보로 과거 선택과 연결하는가?”**

를 묻는다.

---

# 8. Narrative Core Candidates

# GC-NARR-004 — Branch Convergence Can Preserve Agency if History Persists

**Status:** `CANDIDATE`  
**Origin:** `SUB-RULE / POSSIBLE MERGE INTO GC-NARR-001`

## Rule Candidate

> **서로 다른 Branch가 같은 Main Event로 합쳐지더라도 Relationship / Flag / Resource / Character State가 남아 이후 Context를 바꾸면 자동 Fake Choice로 판정하지 않는다.**

## Evidence

80 Days의 State-reactive structure가 강하게 지지.

Reigns도 작은 Content Grammar에서 long-term State를 유지하는 방식이 간접 지지.

## Why Candidate

`GC-NARR-001`과 중복 가능성이 높다.

추가 Evidence 없이는 독립 Core보다 Sub-rule 병합이 적절할 가능성이 높다.

## Candidate Metric

- Converged Branch State Divergence
- Later Reactive Content after Convergence
- Cosmetic-only Convergence Rate

## Confidence

**MEDIUM-HIGH**

---

# GC-NARR-005 — Character / World Memory Should Reflect Consequential History

**Status:** `CANDIDATE`

## Rule Candidate

> **관계·배신·도움·죽음·부상처럼 Narrative적으로 중요한 State를 저장했다면 Character와 World가 이후 적절한 맥락에서 이를 기억해야 한다. Flag 존재와 실제 Reactivity를 분리한다.**

## Evidence

### 80 Days
Previous Event Condition / State-reactive content가 세계 기억의 구조를 지지.

### RimWorld
Character state / loss / relationship / event의 persistent interaction이 emergent story의 기반으로 사용됨.

### Citizen Sleeper
Relationship / Clock이 장기 진행 State를 만든다.

## Promotion Blocker

현재 Reference에서:
- contradiction telemetry
- player continuity perception

직접 Evidence 부족.

## Candidate Metric — Structural

- Relevant State → Response Coverage
- Invalid Character Reference
- Dead Character Appears
- Relationship Contradiction
- Missing Prerequisite State
- Forgotten Flag Candidate

## Human

- Character Continuity
- World Memory Perception

## Confidence

**MEDIUM-HIGH**

---

# GC-NARR-006 — Roleplay Choice Needs Value Conflict, not a Universal Utility Winner

**Status:** `CANDIDATE`

## Rule Candidate

> **Choice를 moral / roleplay 표현으로 제시한다면 한 선택이 모든 System 축에서 명백히 우월해 Roleplay를 단순 Optimization으로 축소하지 않는지 검토한다.**

## Supporting Evidence

### Papers, Please
규칙 준수 / 생계 / 인간적 예외가 충돌.

### This War of Mine
Scarcity가 실제 생존 비용을 만들어 moral choice가 시스템에서 발생.

### Reigns
여러 결과축이 동시에 움직이므로 작은 Choice도 단일 효율값으로 환원되기 어렵다.

## Boundary

일부 Character Arc에서 “옳은 선택”이 명확한 것이 의도될 수 있다.

## Candidate Metric

### Structural
- Choice Outcome Axis Count
- Dominant Utility Choice Rate
- Roleplay Option → System Trade-off Map

### Instrumented
- Choice Distribution
- Decision Time

### Human
- Roleplay Expression
- Choice Reflection
- “최적 선택 때문에 캐릭터 표현을 포기했다” 인식

## Confidence

**MEDIUM-HIGH**

---

# GC-NARR-007 — Failure Can Become Narrative State

**Status:** `CANDIDATE`

## Rule Candidate

> **Failure-as-Content를 약속하는 Narrative에서는 실패가 항상 History를 삭제하는 Reload가 아니라 새로운 Character / Resource / Relationship / World State로 이어질 수 있는지 검토한다.**

## Supporting Evidence

### Reigns
Failure-as-Content가 Reference Design Tag로 명시.

### RimWorld
Loss / incident가 emergent story의 재료.

### This War of Mine
상처 / 굶주림 / 상실이 장기 Character / Survival State에 남는다.

## Counter Evidence

- Linear Action Adventure
- Puzzle
- tightly authored tragedy

에서는 Reload가 정상적일 수 있다.

## Candidate Metric

- Failure → Continue Rate
- Failure → Persistent State Change
- Failure-specific Event Reachability
- Reload Requirement Rate

## Human

- Failure-as-Story Perception
- Loss Meaning
- Narrative Ownership

## Confidence

**MEDIUM**

---

# GC-NARR-008 — Relationship State Must Change Future Context

**Status:** `CANDIDATE`

## Rule Candidate

> **Relationship System을 Narrative Agency로 제시한다면 Affection / Trust 수치가 증가하는 것 이상으로 Future Access / Dialogue / Obligation / Risk / Choice Meaning을 바꾸는지 검토한다.**

## Evidence

### Citizen Sleeper
Relationship quests를 Clock / resource와 연결해 장기 narrative opportunity cost를 만든다.

### RimWorld
relationship / character state가 emergent event meaning을 바꿀 수 있는 구조의 보조 Evidence.

## Promotion Blocker

Primary Narrative Evidence 2개 이상에서 relationship-specific 분석 부족.

## Candidate Metric

- Relationship State → Event Condition Rate
- Relationship State → Choice Availability
- Relationship State → Resource / Risk Change
- Affection-only Content Rate

## Human

- Relationship Continuity
- Attachment
- Relationship Choice Meaning

## Confidence

**MEDIUM**

---

# GC-NARR-009 — Repeated Core Verbs Need Narrative Recontextualization

**Status:** `CANDIDATE`  
**Origin:** `UC-DESIGN-002 SPECIALIZATION / POSSIBLE MERGE`

## Rule Candidate

> **Narrative Game에서 같은 Core Verb를 반복한다면 Character / Rule / Resource / History 변화가 그 행동의 인간적·서사적 의미를 바꾸는지 검토한다.**

## Evidence

### Papers, Please
같은 승인 / 거절이:
- 법
- 생계
- 정치
- 연민

Context에 따라 다른 의미를 가짐.

### This War of Mine
같은 식량 / 약품 / 약탈 선택이 Character State와 Survival Context 때문에 다르게 느껴짐.

### 80 Days
같은 Route / Resource 선택 문법이 위치와 이전 사건에 따라 다른 Story를 만듦.

## Why Candidate

`GC-NARR-001`과 `UC-DESIGN-002` 중복 가능성이 높다.

## Confidence

**MEDIUM-HIGH**

---

# GC-NARR-010 — Emergent Narrative Needs Interpretable Causal Chains

**Status:** `CANDIDATE`

## Rule Candidate

> **Random/System Event가 많다는 사실만으로 Emergent Narrative가 되지 않는다. Character State와 Event의 인과가 연결되어 플레이어가 “무슨 일이 있었는지” 하나의 History로 설명할 수 있어야 한다.**

## Evidence

### RimWorld
Story-generating management, character state, long-term consequence, emergent story가 강한 보조 Evidence.

### This War of Mine
Character state와 survival decisions가 인간적 story로 해석되는 다른 형태의 systemic support.

## Promotion Blocker

Emergent Narrative Primary Reference가 사실상 RimWorld 한 사례에 집중.

## Candidate Metric — Structural

- Character Event Chain Length
- State-linked Event Rate
- Orphan Random Event Rate
- Causal State Dependency

## Human

- Story Recall
- Emergent Story Coherence
- Narrative Ownership

## Confidence

**MEDIUM**

---

# GC-NARR-011 — Narrative Decision Density Should Be Evaluated Separately from Text Volume

**Status:** `CANDIDATE`

## Rule Candidate

> **긴 Narrative Experience에서 Text / Scene 길이보다 가치·Roleplay·전략 판단이 발생하는 빈도와 그 사이의 reflection / payoff를 별도로 평가한다.**

## Evidence

Citizen Sleeper의 limited action allocation은 Text Choice에 opportunity cost를 만든다.

Reigns는 낮은 Text / input volume에서도 높은 consequence density 가능성을 보임.

80 Days는 route / resource / text interaction을 결합.

## Promotion Blocker

Narrative pacing / human fatigue telemetry 부족.

## Candidate Metric

### Structural
- Choice Frequency
- Choice → Persistent State Rate
- Exposition Span between Decisions

### Human / Hybrid
- Narrative Decision Density
- Narrative Pacing
- Reflection Quality

## Confidence

**MEDIUM**

---

# 9. Narrative Anti-Patterns

# AP-NARR-001 — Branch Count = Narrative Depth

## Trigger
Branch / Ending 수를 Agency의 주된 근거로 사용.

## Mechanism
경로 수가 많아도:
- State 변화 없음
- Choice 의미 반복
- Outcome 차이 없음

이면 Agency가 낮을 수 있다.

## Consequence
- false depth
- authored cost
- QA growth

## Evidence
80 Days의 Primary Warning:
State-reactive structure 없이 Branch 수만 늘리는 것은 핵심 강점이 아니다.

## Detection
- Branch Count vs Persistent State Change
- Branch Convergence State Divergence
- Cosmetic-only Branch Rate

## Mitigation
Branch마다:
> “어떤 History / State가 남는가?”
를 정의.

---

# AP-NARR-002 — Cosmetic Choice Presented as Consequence

## Trigger
문구만 다르고 후속 State 없음.

## Mechanism
Choice UI는 존재하지만 Narrative History는 동일.

## Consequence
Player trust / agency 약화 가능.

## Detection
- Action → State Change
- Action → Later Reactive Event
- Cosmetic Choice Rate

## Mitigation
모든 Choice를 Persistent하게 만들 필요는 없지만:
- Cosmetic
- Local
- Persistent
- Structural

을 명시적으로 구분.

---

# AP-NARR-003 — State without Reactivity

## Trigger
Flag / Relationship 수는 많지만 후속 Event 조건에 거의 사용되지 않음.

## Consequence
State complexity만 증가.

## Detection
- Active Flag Count
- State → Event Response Rate
- Never-read Flag Count

## Mitigation
State마다 Consumer / future effect를 매핑.

---

# AP-NARR-004 — Reactivity without Meaning

## Trigger
이름 / 한 줄 대사만 바뀌지만 Future Choice / Relationship / Meaning은 동일.

## Consequence
Reactivity metric은 높아도 Human Agency가 낮음.

## Detection
Structural-only로 확정 불가.

후보:
- Reactive Text Rate
- Human recontextualization recognition

## Mitigation
Text variation보다:
- option
- relationship
- consequence
- roleplay meaning
변화를 우선.

---

# AP-NARR-005 — Consequence without Signal

## Trigger
Choice 당시 판단 근거가 없고 Later Punishment가 임의적으로 보임.

## Consequence
Agency → Guess.

## Evidence
Reigns Warning:
예측 불가능성만 있으면 전략성이 아니라 찍기가 됨.

## Detection
- Consequence Recognition
- Cause Explanation
- Reload / reversal after consequence

## Mitigation
결과 수치를 공개하기보다:
- context
- character attitude
- known rules
- history
- warning
중 적절한 Signal 제공.

---

# AP-NARR-006 — Forgotten Choice

## Trigger
중요한 Choice Flag가 이후 사실상 사용되지 않음.

## Consequence
World가 Player History를 기억하지 않는 느낌.

## Detection
- Persistent Choice → Later Response Coverage
- Forgotten Flag Candidate
- Consequence activation

## Mitigation
중요 Choice만 State로 저장하고 Response Consumer 정의.

---

# AP-NARR-007 — Contradictory Character State

## Trigger
- 죽은 Character 등장
- 배신 후 동일 친밀 Dialogue
- 부상 / 관계 상태 무시

## Consequence
Narrative coherence 붕괴.

## Detection
- Invalid Character Reference
- Dead Character Appears
- Relationship Contradiction
- Missing Prerequisite

## Mitigation
Formal state validation + fallback.

---

# AP-NARR-008 — Story Choice Separated from Core Play

## Trigger

```text
Gameplay
→ Story Menu
→ Gameplay
→ Story Menu
```

두 체계가 서로 거의 영향 없음.

## Consequence
Systemic Narrative Promise가 약화.

## Evidence
80 Days / Papers, Please / Citizen Sleeper는 반대 구조의 강한 Evidence.

## Detection
- Shared Action Coupling
- System State → Narrative Response
- Narrative Event → System State

## Mitigation
핵심 Player Verb 일부에 Narrative consequence 통합.

---

# AP-NARR-009 — System Consequence without Human Meaning

## Trigger
Resource 숫자는 바뀌지만 Character / Story Context에는 의미 없음.

## Consequence
Narrative theme와 system 분리.

## Evidence
This War of Mine:
Resource decision이 인간적 cost를 가질 때 theme-system integration이 강함.

## Detection
Human-heavy:
- Choice Meaning
- Story Recall
- Character impact

## Mitigation
모든 Resource에 Story를 붙이지 말고 핵심 가치 Resource만 Character / Context와 연결.

---

# AP-NARR-010 — Narrative Consequence without System Impact

## Trigger
Story에서는 “큰 사건”인데 gameplay state / access / risk가 전혀 변하지 않음.

## Consequence
Systemic Narrative 약화.

## Boundary
Linear authored story에서는 정상일 수 있음.

## Detection
- Major Event → System State Change
- Major Event → Choice Availability

## Mitigation
Product Promise에 따라 selective system consequence.

---

# AP-NARR-011 — Moral Choice with Dominant Utility

## Trigger
윤리적 choice처럼 보이나 한 Option이:
- resource
- safety
- relationship
- future access

모두 우월.

## Consequence
Roleplay보다 optimization.

## Evidence
Papers, Please / This War of Mine은 실제 cost conflict를 반대 Evidence로 제공.

## Detection
- Dominant Utility Rate
- Choice Distribution
- Human reason for choice

## Mitigation
가치축 / 비용축 충돌.

---

# AP-NARR-012 — Failure Erases Story

## Trigger
모든 실패가 즉시 Reload로 History 삭제.

## Consequence
Fail-forward Promise가 있다면 Failure Meaning 손실.

## Boundary
Action / Puzzle / authored sequence에는 정상일 수 있음.

## Detection
- Failure → Continue
- Failure → State Change
- Reload Requirement

## Mitigation
필요한 Failure만 persistent consequence화.

---

# AP-NARR-013 — Branch Explosion

## Trigger

```text
Choice
× State
× Character
× Time
× Location
```

조합이 콘텐츠 Scope를 폭증.

## Consequence
- writing cost
- QA
- localization
- unreachable states

## Detection
- State Combination
- Condition Count
- Low-reach Content

## Mitigation
Scale Handoff:
- shared scenes
- state-reactive variants
- tooling
- condition simplification

---

# AP-NARR-014 — Unreachable Narrative Content

## Trigger
Trigger condition가 모순되거나 path가 끊김.

## Consequence
authored cost wasted / progression bug.

## Detection
- Event Reachability
- Ending Reachability
- Dead Branch
- Missing prerequisite

## Mitigation
Coverage explorer / formal state graph.

---

# AP-NARR-015 — Repeated Event without Recontextualization

## Trigger
같은 Event가 동일 Meaning으로 반복.

## Consequence
Content reuse가 fatigue로 전환.

## Detection
- Identical Context Repeat
- Repeat before State Change
- Human repetition perception

## Mitigation
반복 시:
- state
- consequence
- option
- response
중 하나를 변화시키거나 repeat cap 적용.

---

# AP-NARR-016 — Exposition Detached from Decisions

## Trigger
Lore / Text가 많지만 이후 Player Judgment에 사용되지 않음.

## Consequence
Text volume을 depth로 오인.

## Detection
- Exposition → Later Choice Reference
- Human recall / use

## Mitigation
모든 lore를 mechanicalize하지 말고 핵심 exposition이:
- roleplay
- relationship
- risk interpretation
에 기여하는지 구분.

---

# AP-NARR-017 — Emergence without Coherence

## Trigger
Random Event와 상태 변화는 많지만 인과가 약함.

## Consequence
플레이어가 incident list는 기억하지만 story로 연결하지 못함.

## Detection
- Orphan Event Rate
- Causal Chain Length
- Story Recall

## Mitigation
Character / place / relationship / state persistence를 통해 연결점 강화.

---

# 10. Conflicting Findings

# CF-NARR-001 — Branch Tree vs State-reactive Narrative

## Branch Tree

Strength:
- authored precision
- distinct character arc
- strong route payoff

Cost:
- authored content
- QA
- low exposure possible

## State-reactive

Strength:
- history persistence
- shared content recontextualization
- combinatorial response

Cost:
- condition logic
- continuity QA
- potential shallow text variants

## Hidden Variable

`Narrative Promise`

## Resolution

어느 쪽도 Universal 정답이 아니다.

`GC-NARR-001`은 Branch Tree를 금지하지 않는다.

---

# CF-NARR-002 — Immediate vs Delayed Consequence

## Immediate
- causal clarity
- learning
- strategy legibility

## Delayed
- natural story
- surprise
- long-term payoff

## Hidden Variable
`Consequence Recognition`

## Resolution
지연 길이보다:

> 나중에 원인을 이해할 수 있는가?

를 본다.

---

# CF-NARR-003 — Explicit vs Hidden Consequence

## Explicit
- strategic clarity
- lower surprise

## Hidden
- roleplay
- discovery
- naturalism

## Hidden Variable
- Strategy Promise
- Roleplay Promise
- Discovery Promise

## Resolution
모든 choice 결과를 숫자로 미리 공개하지 않는다.

---

# CF-NARR-004 — Authored Coherence vs Emergent Ownership

## Authored
80 Days 등:
작가가 강한 content / theme / sequence를 설계.

## Emergent
RimWorld:
character / system / event가 예상하지 못한 history를 만듦.

## Resolution
Authored Game을 Emergent 기준으로, Emergent Game을 authored arc 기준으로 감점하지 않는다.

---

# CF-NARR-005 — Fail-forward vs Reload

## Fail-forward
Failure가 future state를 만든다.

## Reload
실패를 제거하고 authored pacing / mechanical challenge 유지.

## Hidden Variable
Failure가 Product Promise에서:
- story material인지
- invalid play인지

구분.

---

# CF-NARR-006 — High Reactivity vs Strong Main Arc

Reacting to every choice는:
- agency
를 높일 수 있지만
- pacing / thematic control
을 약화시킬 수 있다.

## Resolution
중요한 State만 반응시키는 Selective Reactivity도 유효.

---

# CF-NARR-007 — Replay Variety vs First-play Impact

Narrative Game이 반드시 replayable할 필요는 없다.

Mechanism과:
- Product value
- authored content consumption
을 분리한다.

---

# CF-NARR-008 — Roleplay Freedom vs Mechanical Legibility

모든 outcome을 명확히 보여주면:
- optimization puzzle

이 될 수 있다.

아무 signal도 없으면:
- guess

가 된다.

## Resolution
`GC-NARR-003 Causal Legibility`를 적용하되 outcome certainty를 요구하지 않는다.

---

# 11. Structural / Machine Validation Map

Narrative에서 Machine의 강한 역할은:

> **State Integrity / Reachability / Coverage / Trigger / Continuity**

다.

AI가 Story의 감정 품질을 평가하는 것은 목적이 아니다.

---

## 11.1 Narrative State Metrics

| Metric | Type |
|---|---|
| Narrative State Count | Structural |
| Active Flag Count | Structural |
| Relationship State Distribution | Structural |
| State Transition Count | Structural |
| Persistent State Duration | Structural |
| State Combination Coverage | Structural / model-dependent |

---

## 11.2 Event Reachability

| Metric | Type |
|---|---|
| Event Reachability | Structural |
| Ending Reachability | Structural |
| Unreachable Event Count | Structural |
| Dead Branch Count | Structural |
| Required State Dependency | Structural |
| Mutually Exclusive State Check | Structural |

---

## 11.3 Choice Metrics

| Metric | Type |
|---|---|
| Choice Frequency | Structural |
| Choice Distribution | Instrumented / Simulation |
| Action → Persistent State Rate | Structural |
| Local Choice Rate | Structural / model-dependent |
| Cosmetic Choice Rate | Structural / model-dependent |
| Structural Choice Rate | Structural / model-dependent |

### Rule

`Cosmetic / Local / Persistent / Structural`은 Project-specific Formal Definition을 먼저 만든다.

---

## 11.4 Consequence Metrics

| Metric | Type |
|---|---|
| Action → State Change Rate | Structural |
| Action → Narrative Response Rate | Structural |
| Delayed Consequence Activation | Structural |
| Consequence Latency | Structural |
| Unresolved Consequence Count | Structural |
| Forgotten Flag Rate | Structural / model-dependent |

---

## 11.5 Reactivity Metrics

| Metric | Type |
|---|---|
| State-reactive Event Rate | Structural |
| State-reactive Text Rate | Structural |
| Relationship-reactive Content Rate | Structural |
| Repeat Event with Different State Rate | Structural |
| Recontextualized Event Rate | Hybrid / model-dependent |

---

## 11.6 Continuity Metrics

| Metric | Type |
|---|---|
| Invalid Character Reference | Structural |
| Dead Character Appears | Structural |
| Relationship Contradiction | Structural / model-dependent |
| Impossible Timeline State | Structural |
| Mutually Exclusive Dialogue Trigger | Structural |
| Missing Prerequisite State | Structural |

---

## 11.7 Content Coverage

| Metric | Type |
|---|---|
| Event Exposure Rate | Instrumented / Simulation |
| Unique Scene Exposure | Instrumented / Simulation |
| Choice Path Coverage | Structural / Simulation |
| Ending Coverage | Structural / Simulation |
| Low-reach Content Count | Structural / model-dependent |
| Never-seen Content | Instrumented / Simulation |

---

## 11.8 Repetition Metrics

| Metric | Type |
|---|---|
| Event Repeat Rate | Instrumented / Simulation |
| Identical Context Repeat | Structural / model-dependent |
| Dialogue Repeat | Instrumented |
| Repeat before State Change | Structural |
| Repetition Cluster | Structural / model-dependent |

---

# 12. Model-dependent Narrative Metric Rule

다음은 일반 Machine Metric으로 자동 사용하지 않는다.

- Meaningful Choice Rate
- Recontextualization Quality
- Recontextualized Event Rate
- Structural Choice Rate
- Cosmetic Choice Rate
- Local Choice Rate
- Forgotten Choice / Forgotten Flag
- Narrative Relevance
- Relationship Contradiction
- Character Coherence
- Emergent Story Event Chain
- Low-reach Content

이 항목은:

1. 프로젝트별 Formal Definition이 있으면 `Structural / model-dependent`
2. 의미 품질 판단이 필요하면 `Hybrid`
3. 체감 판단이면 `Human`

으로 분류한다.

---

# 13. Narrative Tester Profile Map

Human Taste Persona보다 구조 검증 Profile을 우선한다.

## P-NARR-001 — Coverage Explorer

### Behavior
가능한:
- Event
- State
- Branch
- Ending

을 최대한 탐색.

### Detects
- unreachable content
- dead branch
- low coverage
- missing trigger

---

## P-NARR-002 — Consequence Tracer

### Behavior
특정 Choice를 고정하고 그 State의 후속 Trigger를 추적.

### Detects
- forgotten flag
- broken consequence chain
- unexpected overwrite
- consequence latency

---

## P-NARR-003 — Contradiction Hunter

### Behavior
극단 / 희귀 State 조합을 의도적으로 생성.

### Detects
- dead character dialogue
- invalid relationship
- impossible timeline
- mutually exclusive trigger

---

## P-NARR-004 — Repetition Stress Tester

### Behavior
동일:
- route
- event family
- choice tendency

를 반복.

### Detects
- context-insensitive repetition
- repeated dialogue
- state-insensitive event

Human fatigue 자체는 결론내리지 않는다.

---

## P-NARR-005 — Divergent Path Tester

### Behavior
같은 Starting State에서 다른 Choice Policy를 적용.

### Detects
- actual state divergence
- cosmetic divergence
- branch convergence
- ending / event variation

---

## P-NARR-006 — State Memory Tester

### Behavior
중요한:
- promise
- betrayal
- death
- relationship change
- resource sacrifice

를 만든 후 관련 Character / Event를 재접촉.

### Detects
- forgotten history
- missing reactivity
- contradiction

---

# 14. AI Tester Interpretation Limits

Machine이 강하게 검증할 수 있는 것:

```text
State
Trigger
Branch
Reachability
Coverage
Continuity
Consequence activation
Frequency
Contradiction
```

Machine이 직접 결론내리지 않는 것:

- 이야기가 감동적이다.
- 선택이 의미 있다고 느낀다.
- Character가 매력적이다.
- 후회가 좋다.
- 이야기 흐름이 자연스럽다.
- Theme가 깊다.
- Recontextualization이 감정적으로 강하다.
- 플레이어가 자신의 Story라고 느낀다.

---

# 15. Human Validation Map

# H-NARR-001 — Narrative Agency

> 내 선택 때문에 이야기가 달라졌다고 느끼는가?

---

# H-NARR-002 — Consequence Recognition

> 현재 결과가 어떤 이전 Choice 때문인지 설명할 수 있는가?

---

# H-NARR-003 — Choice Meaning

> 선택지가 서로 다른 가치 / 목표 / 관계를 대표한다고 느끼는가?

---

# H-NARR-004 — Roleplay Expression

> 자신의 성격 / 가치 / 관계를 표현하는 선택이 가능한가?

---

# H-NARR-005 — Narrative Ownership

> 이 이야기가 “내 플레이의 이야기”라고 느껴지는가?

특히:
- systemic
- emergent
에서 중요.

---

# H-NARR-006 — Character Continuity

> Character가 과거 사건 / 관계 변화를 기억한다고 느끼는가?

---

# H-NARR-007 — Consequence Fairness

> 결과를 미리 정확히 알지는 못했어도, 결과 후 되돌아보면 납득 가능한가?

---

# H-NARR-008 — Delayed Payoff Recognition

> 과거 Choice가 나중에 돌아왔을 때 그 연결을 기억할 수 있었는가?

---

# H-NARR-009 — Recontextualization

> 현재 State 때문에 이전과 같은 행동 / 장소 / Character가 다르게 느껴졌는가?

---

# H-NARR-010 — Narrative Pacing

> 읽기 / 선택 / consequence / reflection / new conflict의 리듬이 적절한가?

---

# H-NARR-011 — Repetition

> 반복 Event가 Context 때문에 새롭게 느껴지는가, 같은 Content 재사용으로 느껴지는가?

---

# H-NARR-012 — Emotional Impact

Human-only.

- tension
- guilt
- attachment
- relief
- loss
- surprise

---

# H-NARR-013 — System / Story Unity

> Gameplay를 멈추고 Story를 보는 느낌인가, 플레이 자체가 Story를 만드는 느낌인가?

---

# H-NARR-014 — Choice Reflection

> 선택 후 다른 가치 / 관계 / 결과를 생각하거나 후회하게 되는가?

---

# H-NARR-015 — Story Recall

Playtest 후:

> “당신의 플레이에서 어떤 일이 있었나?”

를 자유롭게 설명하게 한다.

Emergent Narrative에서는 특히 중요하다.

---

# H-NARR-016 — Branch / State Awareness

> “다른 선택을 했다면 무엇이 달라졌을 것이라고 생각하는가?”

Agency가 실제 State change와 일치하는지 확인한다.

---

# 16. Scale Handoff Candidates

이번 단계에서는 Genre × Scale Core를 확정하지 않는다.

# SCALE_HANDOFF-NARR-001 — Branch / State Explosion

## Finding

Narrative Scope는 단순 Branch Count보다:

```text
Choice
× State
× Character
× Location
× Time
× Localization
```

조건 조합에서 폭증한다.

## Supporting Evidence

80 Days Reference가:
- 대량 작문
- 번역
- 상태 QA 복잡도

를 직접 Weakness로 명시한다.

---

# SCALE_HANDOFF-NARR-002 — Reactive Content QA

State-reactive Narrative는 Branch를 합쳐도 비용이 사라지지 않는다.

필요:
- trigger
- condition
- priority
- fallback
- contradiction
- state overwrite
- localization QA

---

# SCALE_HANDOFF-NARR-003 — Localization Multiplier

State와 Word Choice가:
- meaning
- clue
- relationship tone
- consequence signaling

에 연결되면 번역은 Text Cost를 넘어 Narrative Logic QA가 된다.

---

# SCALE_HANDOFF-NARR-004 — Voice-over Multiplier

Full Voice를:
- branch
- state variant
- reactive line

에 적용하면:
- recording
- localization
- patching
- content iteration

비용이 빠르게 증가할 수 있다.

현재 Reference의 직접 Voice-over production Evidence는 부족하므로 Handoff Candidate.

---

# SCALE_HANDOFF-NARR-005 — Authored Content Exposure

한 플레이에서 보지 않는 Content 비율과 Authoring Cost를 함께 검토한다.

단:

> 낮은 Exposure = 낭비

로 자동 판단하지 않는다.

80 Days처럼:
- 세계 규모감
- discovery
- replay variation

이 Product Value일 수 있다.

---

# SCALE_HANDOFF-NARR-006 — Narrative Tooling ROI

State-reactive Narrative가 늘어날수록 다음 Tool 가치가 증가할 수 있다.

- state preview
- trigger debugger
- dialogue condition viewer
- reachability test
- localization context
- branch graph
- save-state injection

현재 Production ROI 정량 Evidence는 부족.

---

# SCALE_HANDOFF-NARR-007 — State Count Can Hide Authoring Cost

`Flag 100개`가 저비용이라는 뜻이 아니다.

비용은:
- flag consumer
- interaction
- fallback
- contradiction
- test combination

에 따라 결정된다.

---

# 17. Universal Reclassification Candidates

이번 단계에서 Universal로 직접 승격하지 않는다.

# UC-RECLASS-NARR-001 — Delayed Consequence Needs Causal Legibility

Narrative 밖:
- strategy
- management
- economy
에서도 장기 consequence의 원인 추적은 중요할 수 있다.

현재 Narrative Evidence에 편중.

---

# UC-RECLASS-NARR-002 — System Should Remember Consequential Player Actions

다른 장르에서도:
- persistent world
- faction
- reputation
- campaign state

에 적용 가능.

현재는 Narrative-specific candidate 유지.

---

# UC-RECLASS-NARR-003 — Persistent State Should Alter Future Choice Meaning

이미 `UC-DESIGN-003 Consequence-to-Next-Decision Coupling`과 상당히 겹친다.

## Decision
새 Universal Core를 만들지 않는다.

Narrative에서는:

> State가 Future **Narrative Meaning**을 바꾸는가

만 특수화한다.

---

# UC-RECLASS-NARR-004 — Repetition Needs Contextual Value Shift

이미 `UC-DESIGN-002`와 중복.

## Decision
새 Core 생성 금지.

`GC-NARR-001 / 009`에서 Narrative-specific specialization으로만 사용.

---

# UC-RECLASS-NARR-005 — Formal State Integrity ≠ Human Narrative Agency

Validation methodology 전반에 확장 가능.

Machine coverage가 높아도:
- agency
- coherence
- emotion

은 Human Evidence가 필요하다는 Rule.

---

# 18. Evidence Gaps

# GAP-NARR-001 — Choice → Later Consequence Telemetry

필요:
- 어떤 Choice가 later event에 실제로 연결되는가
- activation
- latency
- player revisit

---

# GAP-NARR-002 — Consequence Recall

필요:
- 결과 발생 후 player가 원인 Choice를 기억하는가
- delayed payoff recognition

---

# GAP-NARR-003 — Cosmetic vs Persistent Choice

Formal classification뿐 아니라:
- player perception
- perceived fake choice

자료 필요.

---

# GAP-NARR-004 — Character Continuity

필요:
- contradiction bug
- forgotten state
- player trust loss
- state memory recognition

---

# GAP-NARR-005 — Roleplay Choice Distribution

필요:
- utility-max choice
- character-expression choice
- relationship choice
- moral choice

선택 이유 데이터.

---

# GAP-NARR-006 — Repetition Fatigue

필요:
- event repeat
- repeat context
- player fatigue
- state-reactive repeat perception

---

# GAP-NARR-007 — Failure-as-Content

필요:
- failure → continue
- reload
- story recall
- failure meaning

---

# GAP-NARR-008 — Emergent Story Recall

RimWorld 같은 emergent structure에서:
- 어떤 event chain을 player가 story로 기억하는가
- 단순 incident list와 narrative chain 차이

자료 부족.

---

# GAP-NARR-009 — Branch Reachability

필요:
- unreachable event
- dead branch
- ending coverage
- low-reach content

실제 Narrative tool / QA postmortem.

---

# GAP-NARR-010 — Narrative Decision Density

Text 시간 대비:
- meaningful choice
- roleplay choice
- reflection
비율 자료 부족.

---

# GAP-NARR-011 — System / Story Unity Human Data

Structure가 연결되어 있어도 player가 실제로:
> “플레이 자체가 이야기다”
라고 느끼는지 자료 부족.

---

# GAP-NARR-012 — Localization / State QA

State-dependent line 번역에서:
- pronoun
- tense
- relationship tone
- branch condition

오류가 어떻게 발생하는지 Postmortem 부족.

---

# GAP-NARR-013 — Underperforming Narrative Controls

필요:
- branch explosion
- fake choice backlash
- inconsistent state
- weak consequence signaling
- repeated storylet fatigue
- roleplay collapsed to utility

실패 사례.

---

# GAP-NARR-014 — Emergent Narrative Primary Evidence

현재 Emergent Narrative는 RimWorld에 편중.

Wildermyth / Crusader Kings 계열 Direct Design Evidence 필요.

---

# 19. Additional References Needed

아래는 Research Target이며 현재 Core Evidence가 아니다.

# P0 — Pentiment

## 강화 대상
- `GC-NARR-003 Consequence Legibility`
- `GC-NARR-005 Character / World Memory`
- Branch Convergence
- Community State

## Research
- delayed consequence
- community memory
- character continuity
- authored branching

## Needed Evidence
- developer talks
- narrative tool / state design
- playtest consequence recall

---

# P0 — Disco Elysium

## 강화 대상
- Roleplay Expression
- Failed Check as Content
- Internal State Reactivity
- Narrative / System Coupling

## Research
- skill voices
- failure
- political / identity expression
- stat → narrative response

---

# P0 — Roadwarden

## 강화 대상
- state-heavy text
- time / route / relationship
- authored scope
- branch / state efficiency

## Needed Evidence
- authoring tool
- condition count
- production postmortem

---

# P0 — Wildermyth

## 강화 대상
- `GC-NARR-010 Emergent Narrative`
- Character Continuity
- Procedural Authored Event
- Long-term Memory

## Research
- event template + character state
- legacy character
- relationship continuity

---

# P0 — I Was a Teenage Exocolonist

## 강화 대상
- Long-term State
- Recontextualization
- Relationship
- Repeated-life memory
- Ending

## Research
- repeated timeline knowledge
- state-dependent scene
- relationship memory

---

# P1 — Crusader Kings III

## 강화 대상
- Emergent Story Recall
- Systemic Relationship
- Character state chains

## Boundary
Grand Strategy Core와 분리.

---

# P1 — Failbetter / Fallen London / Sunless Sea

## 강화 대상
- Quality / State Narrative
- Storylet
- Content gating
- Repetition
- state explosion

## Research
- storylet architecture
- quality-based condition
- repeated content mitigation
- authoring QA

---

# P1 — ChoiceScript Cases

## 강화 대상
- Branch / State architecture
- Stat-reactive text
- Roleplay expression
- authored scope

---

# 20. Promotion Table

| ID | Name | Decision | Status | Confidence |
|---|---|---|---|---|
| GC-NARR-001 | State-reactive Recontextualization over Branch Count | STRENGTHEN / REFRAME | **PROVISIONAL CORE** | VERY HIGH |
| GC-NARR-002 | System / Narrative Choice Coupling | NEW | **PROVISIONAL CORE** | HIGH |
| GC-NARR-003 | Persistent + Causally Legible Consequence | NEW | **PROVISIONAL CORE** | HIGH |
| GC-NARR-004 | Branch Convergence with Persistent History | NEW | MERGE CANDIDATE → GC-NARR-001 | MEDIUM-HIGH |
| GC-NARR-005 | Character / World Memory | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-NARR-006 | Roleplay Choice vs Dominant Utility | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-NARR-007 | Failure Can Become Narrative State | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-NARR-008 | Relationship State Changes Future Context | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-NARR-009 | Repeated Verb Recontextualization | NEW / UC SPECIALIZATION | MERGE CANDIDATE → GC-NARR-001 / UC-DESIGN-002 | MEDIUM-HIGH |
| GC-NARR-010 | Emergent Narrative Needs Causal Chains | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-NARR-011 | Narrative Decision Density / Pacing | NEW | KEEP AS CANDIDATE | MEDIUM |

---

# 21. Narrative Reviewer Default Set

신규 Narrative / Systemic Narrative 기획에서 우선 적용할 15개 질문.

## Q1 — Narrative Promise

> **이 게임은 authored story 참여, roleplay, consequence, relationship, own story, emergent story 중 무엇을 약속하는가?**

---

## Q2 — Player Action

> **플레이어 행동이 실제 Story State를 바꾸는가?**

---

## Q3 — State Persistence

> **중요 Choice 결과가 후속 Event까지 남는가?**

관련:
`GC-NARR-003`

---

## Q4 — Recontextualization

> **같은 Event / Character / Action이 현재 State와 History 때문에 다른 의미를 갖는가?**

관련:
`GC-NARR-001`

---

## Q5 — Branch Quality

> **Branch 수보다 Branch 이후 남는 State 차이가 존재하는가?**

관련:
`GC-NARR-001 / 004`

---

## Q6 — Consequence Recognition

> **Later Consequence가 발생했을 때 Player가 원인 Choice를 이해할 수 있는가?**

관련:
`GC-NARR-003`

---

## Q7 — System / Story Unity

> **Core Gameplay Action 중 무엇이 동시에 Narrative State를 바꾸는가?**

관련:
`GC-NARR-002`

---

## Q8 — Narrative → System

> **Story Event가 Resource / Access / Character / Risk / Rule을 다시 바꾸는가?**

관련:
`GC-NARR-002`

---

## Q9 — World Memory

> **Character와 World가 배신 / 약속 / 죽음 / 관계 변화 같은 중요한 History를 기억하는가?**

관련:
`GC-NARR-005`

---

## Q10 — Roleplay vs Utility

> **Roleplay Choice가 하나의 압도적 System 최적해로 축소되지 않는가?**

관련:
`GC-NARR-006`

---

## Q11 — Failure

> **Failure는 이 Product에서 Story State인가, invalid play라서 Reload해야 하는가?**

관련:
`GC-NARR-007`

---

## Q12 — Repetition

> **반복 Event / Verb가 Context 때문에 새로운 의미를 얻는가?**

관련:
`GC-NARR-001 / 009`

---

## Q13 — Emergent Narrative

> **Random/System Event가 Character State와 인과적으로 연결되어 Player가 하나의 Story로 회상할 수 있는가?**

관련:
`GC-NARR-010`

---

## Q14 — Machine vs Human

> **State / Trigger / Reachability / Continuity는 Machine으로, Agency / Coherence / Emotion / Ownership은 Human으로 분리했는가?**

---

## Q15 — Scope

> **Branch / Reactive State / Character / Localization 조합이 Production Scope와 QA Capacity에 맞는가?**

Scale Handoff.

---

# 22. Default Metric Bundle

Metric은 Criteria가 아니다.

Threshold는 프로젝트별 Validation Planner가 잠근다.

## Structural / Machine

- Narrative State Count
- Active Flag Count
- State Transition Count
- Persistent State Duration
- Event Reachability
- Ending Reachability
- Unreachable Event Count
- Dead Branch Count
- Required State Dependency
- Mutually Exclusive State Check
- Choice Frequency
- Action → Persistent State Rate
- Action → State Change Rate
- Action → Narrative Response Rate
- Delayed Consequence Activation
- Consequence Latency
- Unresolved Consequence Count
- State-reactive Event Rate
- State-reactive Text Rate
- Relationship-reactive Content Rate
- Repeat Event with Different State Rate
- Invalid Character Reference
- Dead Character Appears
- Impossible Timeline State
- Mutually Exclusive Dialogue Trigger
- Missing Prerequisite State
- Repeat before State Change

---

## Structural / model-dependent

- State Combination Coverage
- Local Choice Rate
- Cosmetic Choice Rate
- Structural Choice Rate
- Forgotten Flag Rate
- Relationship Contradiction
- Low-reach Content Count
- Identical Context Repeat
- Repetition Cluster
- Emergent Story Event Chain
- Narrative State Divergence

Project-specific Formal Definition 없이 자동 사용하지 않는다.

---

## Instrumented Player Telemetry

- Choice Reversal / Reload Rate
- Ending Exposure
- Repeated Event Exposure
- Dialogue Skip Rate
- Decision Time
- Relationship Path Distribution
- Failure → Continue / Reload Behavior
- Time from Choice to Delayed Consequence

## Instrumented / Simulation

- Choice Distribution
- Event Exposure Rate
- Unique Scene Exposure
- Event Repeat Rate
- Dialogue Repeat Rate

## Structural / Simulation

- Choice Path Coverage
- Ending Coverage

### Interpretation Rule

`Simulation Coverage`와 `Observed Player Exposure`를 동일한 Evidence로 취급하지 않는다.

예를 들어:

```text
AI Tester 10,000회 실행
→ Event Exposure 72%
```

는 구조적 도달 가능성과 Tester Policy 분포를 반영한다.

반면:

```text
실제 플레이어 30명
→ Event Exposure 72%
```

는 Human Choice, 이해, 선호, 이탈을 포함한 실제 행동 분포다.

동일한 숫자라도 Evidence Type과 해석 범위를 분리한다.

---

## Human

- Narrative Agency
- Consequence Recognition
- Choice Meaning
- Roleplay Expression
- Narrative Ownership
- Character Continuity
- Consequence Fairness
- Delayed Payoff Recognition
- Recontextualization
- Narrative Pacing
- Emotional Impact
- System / Story Unity
- Choice Reflection
- Story Recall
- Character Attachment
- Perceived Repetition

---

## Hybrid

- Meaningful Choice
- Narrative Variation Quality
- Consequence Legibility
- Character Coherence
- Story Reactivity
- Repetition Quality
- Failure-as-Content Quality
- Emergent Story Coherence
- Narrative Decision Density
- Delayed Payoff Quality
- Recontextualization Quality
- Narrative State Divergence Quality

---

# 23. Self-Review Result

## Check 1 — Story Presence ≠ Narrative Core
**PASS**

Text / Story 존재 자체를 Core로 만들지 않았다.

## Check 2 — Branch Count ≠ Agency
**PASS**

`GC-NARR-001`, `AP-NARR-001`에 직접 반영.

## Check 3 — Text Volume ≠ Narrative Depth
**PASS**

Decision / state / meaning 관계로 평가했다.

## Check 4 — Authored vs Emergent
**PASS**

80 Days / Reigns와 RimWorld를 동일 기준으로 평가하지 않았다.

## Check 5 — Branch Convergence ≠ Fake Choice
**PASS**

State history가 남는 경우 유효할 수 있다고 Candidate / Conflict에 명시했다.

## Check 6 — Every Choice Must Persist
**PASS**

Cosmetic / Local / Persistent / Structural을 분리했다.

## Check 7 — Delayed Consequence always good
**PASS**

Causal Legibility가 없으면 Guess가 될 수 있다고 정리했다.

## Check 8 — Management Resource Duplicate
**PASS**

Resource의 scarcity / priority 자체가 아니라 human / narrative meaning만 사용했다.

## Check 9 — State Count ≠ Reactivity
**PASS**

State Consumer / Event Response를 별도 검토한다.

## Check 10 — Machine Coverage ≠ Human Agency
**PASS**

명시적으로 분리했다.

## Check 11 — AI Story Evaluation
**PASS**

Emotion / ownership / coherence는 Human Evidence로 유지했다.

## Check 12 — Linear Authored Narrative unfairly penalized
**PASS**

Systemic Narrative Rule의 Boundary를 명시했다.

## Check 13 — Scope vs Genre Rule
**PASS**

Branch efficiency / localization / QA는 Scale Handoff로 이동했다.

## Check 14 — Character Continuity
**PASS**

Candidate / Structural QA / Anti-pattern으로 포함했다.

## Check 15 — Reviewer Usability
**PASS**

15개 Default Question으로 압축했다.

---

# 24. Final Position

현재 Studio OS Narrative / Systemic Narrative Knowledge Base에서 우선 `Provisional Genre Core`로 사용할 항목은 **3개**다.

1. `GC-NARR-001 — State-reactive Recontextualization over Branch Count`
2. `GC-NARR-002 — Core Actions Should Carry Both Systemic and Narrative Meaning`
3. `GC-NARR-003 — Delayed Consequences Need Persistent State and Causal Legibility`

Candidate는 다음과 같다.

- `GC-NARR-004 — Branch Convergence with Persistent History`
- `GC-NARR-005 — Character / World Memory`
- `GC-NARR-006 — Roleplay Choice vs Dominant Utility`
- `GC-NARR-007 — Failure Can Become Narrative State`
- `GC-NARR-008 — Relationship State Changes Future Context`
- `GC-NARR-009 — Repeated Verb Recontextualization`
- `GC-NARR-010 — Emergent Narrative Needs Causal Chains`
- `GC-NARR-011 — Narrative Decision Density / Pacing`

`GC-NARR-004`는 `GC-NARR-001`의 Sub-rule로 병합 가능성이 높다.

`GC-NARR-009`도 독립 Genre Core라기보다:
- `GC-NARR-001`
- `UC-DESIGN-002`

의 Narrative-specific Sub-rule일 가능성이 높으므로 Candidate 상태를 유지한다.

이번 Extraction의 가장 중요한 정리점은:

> **Narrative Agency를 Branch 수로 측정하지 않는다. Player Action이 Persistent State를 만들고, 그 State가 나중의 Response와 Choice Meaning을 바꾸며, Player가 그 인과를 이해할 수 있을 때 State-reactive Narrative가 작동한다.**

Systemic Narrative에서는 여기에 한 가지가 더 필요하다.

> **Story는 Core Play 이후 붙는 보상이 아니라, 가능하면 Core Player Action과 같은 State Change를 공유해야 한다.**

반대로 Linear / Authored Narrative에서는 이 Rule을 강제하지 않는다.

현재 가장 중요한 Evidence Gap은:

> **Consequence Recall / Character Continuity / Cosmetic-vs-Persistent Choice / Roleplay Distribution / Emergent Story Recall / Repetition Fatigue / State QA**

이다.

따라서 다음 Reference 확장은 Narrative Game 수를 늘리는 것보다:

> **플레이어가 과거 Choice와 나중 결과를 실제로 연결하는가?  
> World가 Player History를 언제 기억하지 못하는가?  
> Fail-forward는 언제 Story가 되고 언제 불필요한 복잡도인가?  
> Emergent Event는 언제 “이야기”로 기억되고 언제 Random Incident로 끝나는가?**

를 직접 다루는 Postmortem / Telemetry가 있는 사례를 우선 조사하는 편이 효율적이다.

---

# 25. Source Trace

## Primary Narrative / Systemic Narrative Evidence
- REF-10 — 80 Days
- REF-09 — Reigns

## Strong Narrative / System Hybrid
- REF-23 — Citizen Sleeper
- REF-01 — Papers, Please
- REF-15 — This War of Mine
- REF-13 — RimWorld
- REF-19 — Cultist Simulator

## Baseline
- STUDIO_CORE_CANDIDATES_v0.2
- Studio OS — Evidence-Based Core Extraction Master Prompt v0.2
- Studio OS — Narrative / Systemic Narrative Genre Core Deep Extraction Prompt v0.1

---

# 26. Traceability Rule

Core는 원본 Reference를 대체하지 않는다.

Narrative 위험 신호가 발생하면:

```text
Genre Core
↓
Primary Reference
↓
Player Action
↓
Narrative State
↓
Consequence
↓
Recontextualization
↓
Boundary / Trade-off
↓
Current Project
```

순서로 다시 내려가 검토한다.

`NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1`은 Studio OS Reviewer가 Story의 양이나 Branch의 수가 아니라 **Player History, State Reactivity, System / Narrative Coupling, Consequence Legibility**를 기준으로 신규 Narrative 기획을 평가하기 위한 압축된 Genre 판단 계층이다.
