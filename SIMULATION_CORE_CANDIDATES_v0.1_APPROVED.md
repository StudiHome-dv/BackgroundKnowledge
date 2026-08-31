# SIMULATION_CORE_CANDIDATES_v0.1

**Studio OS — Simulation / Systemic Simulation Genre Core Deep Extraction**  
**Document:** `SIMULATION_CORE_CANDIDATES_v0.1`  
**Status:** `APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE`  
**Purpose:** 신규 Colony Simulation / Systemic Simulation / Agent Simulation / Life / Character Simulation / Economy / Production Simulation / Network Simulation / Survival Simulation / Abstract Simulation / Simulation Hybrid 기획 평가용 Genre-specific Reviewer Knowledge Base  
**Baseline:** `STUDIO_CORE_CANDIDATES_v0.2`  
**Extraction Prompt:** `Studio OS — Simulation / Systemic Simulation Genre Core Deep Extraction Prompt v0.1`  
**Deduplication Baselines:** `MANAGEMENT_CORE_CANDIDATES_v0.1`, `NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1`, `STRATEGY_CORE_CANDIDATES_v0.1`  
**Provisional Genre Cores:** `GC-SIM-001`, `GC-SIM-002`  
**Candidates:** `GC-SIM-003 ~ GC-SIM-008`  
**Merge Candidate:** `GC-SIM-009 → GC-SIM-001 Sub-rule`  
**Evidence Boundary:** `Colony / Systemic / Network / Abstract Simulation 중심. Vehicle / Sports / Physics / Large-scale Economy / Social / Hardcore Realism Simulation은 Additional Evidence 전까지 제한 적용.`  
**Pending:** `Additional Evidence / Prototype Validation / Internal Evidence`  
**Evidence Rule:** 현재 Direct Evidence는 Colony / Systemic / Network / Abstract Simulation에 편중되어 있으므로 Vehicle / Sports / Physics / Large-scale Economy / Social / Hardcore Realism Simulation 전체로 자동 일반화하지 않는다.

---

# 1. Executive Summary

이번 Deep Extraction의 핵심 결론은 다음과 같다.

1. **Simulation의 핵심은 State 수가 아니라 `Rule에 의해 State가 변하고, 그 변화가 다른 State로 전파되는 Causal Model`이다.**
   - 숫자가 많아도 서로 독립이면 Simulation Depth가 낮을 수 있다.
   - State가 적어도 하나의 변화가 다른 System의 조건과 Outcome을 바꾸면 강한 Systemic Simulation이 될 수 있다.

2. **Management와 Simulation을 분리한다.**
   - Management:
     `Observe → Prioritize → Allocate → Reprioritize`
   - Simulation:
     `State + Rule + Interaction → New State`
   - 둘은 자주 결합하지만 동일한 Core가 아니다.

3. **Realism과 Simulation Quality도 분리한다.**
   - Physical Fidelity가 높다고 좋은 Simulation이라고 자동 판정하지 않는다.
   - Simulation에서 중요한 것은:
     - 어떤 Cause / Effect를 모델링하는가
     - 그 관계가 일관적인가
     - Player Experience에서 의미가 있는가
     이다.

4. 현재 Source Weight는 다음이 가장 안전하다.
   - `REF-13 RimWorld` → **Tier A / Primary Simulation Evidence**
   - `REF-02 FTL` → **Tier A / Primary Systemic Simulation Evidence**
   - `REF-14 Mini Metro` → **Tier B / Strong Network & Abstraction Support**
   - `REF-15 This War of Mine` → **Tier B / Character-state Survival Support**
   - `REF-22 Stacklands` → **Tier B / Abstract Production Support**
   - `REF-19 Cultist Simulator` → **Tier B / Abstract State-model Support**
   - `REF-07 Against the Storm` → **Tier B / Management-Simulation Hybrid**

5. 현재 Provisional Simulation Core는 **2개**로 제한하는 것이 타당하다.
   - `GC-SIM-001 — Selective Simulation Should Preserve Experience-Relevant Causality`
   - `GC-SIM-002 — System States Should Propagate through Causal Dependencies`

6. 다음은 중요하지만 현재 Evidence가 한 Subtype 또는 한 사례에 더 편중되어 Candidate로 유지한다.
   - `GC-SIM-003 — Emergence Requires Persistent Rule Interaction`
   - `GC-SIM-004 — Major Outcomes Need Diagnosable Causes`
   - `GC-SIM-005 — Agent Differences Should Change Behavior / Interaction`
   - `GC-SIM-006 — Autonomous Systems Need Meaningful Observation / Intervention`
   - `GC-SIM-007 — Stable / Runaway / Cascade States Need Explicit Boundaries`
   - `GC-SIM-008 — Event Directors Should Modulate, not Replace, Simulation`
   - `GC-SIM-009 — Abstraction Can Preserve Simulation through Causal Fidelity`

7. `GC-SIM-009`는 `GC-SIM-001`과 중복 가능성이 높아 장기적으로 **Merge Candidate**다.
   - `Selective Simulation`
   - `Abstraction`
   는 결국:
     > 무엇을 생략하고 어떤 Causal Relationship을 보존할 것인가?
     라는 동일 문제의 다른 표현일 수 있다.

8. `Model Legibility`는 매우 중요하지만 독립 Core 승격을 보수적으로 처리한다.
   - RimWorld는 공간과 주민 행동.
   - FTL은 함선 단면도 / Room / Oxygen / System Damage.
   - Mini Metro는 노선도 abstraction.
   모두 Cause를 읽는 구조를 지지한다.
   - 그러나 `UC-DESIGN-005 — Actionable Information` 및 Management Information Core와 중복이 있으므로 `GC-SIM-004` Candidate로 유지한다.

9. `Emergence`는 Random Event 수와 동일하지 않다.
   - RimWorld의 Reference Warning 자체가:
     > 시스템 수와 Random Event를 많이 넣는 것 자체가 Story Generator를 만들지 않는다.
     고 정리한다.
   - FTL에서도 위기의 다양성은 Random Event 수보다 Fire / Oxygen / Crew / Damage / Power 같은 연결된 System이 같은 규칙 위에서 결합하는 데서 나온다.

10. Simulation Reviewer에서 가장 중요한 두 질문은 다음이다.

> **“이 State가 무엇 때문에 변하고, 변한 뒤 어떤 다른 State를 바꾸는가?”**

그리고:

> **“이 Cause / Effect를 왜 Simulation해야 하는가? Player Fantasy 또는 핵심 경험에 어떤 가치가 있는가?”**

11. AI Tester는 Simulation에서 특히 강하다.
   - State Transition
   - Dependency
   - Cascade
   - Edge State
   - Deadlock
   - Feedback Loop
   - Distribution
   - Coverage
   를 대량 검증할 수 있다.

12. 하지만 다음은 Machine이 직접 판정하지 않는다.
   - 세계가 살아 있다고 느껴지는가
   - Model이 자연스럽게 느껴지는가
   - Emergent Outcome이 재미있는가
   - Agent가 믿을 만한가
   - Detail이 가치 있는가
   - Realism이 적절한가

13. `Simulation State Log`와 `Player Observation Telemetry`를 명시적으로 분리한다.

```text
World changed
≠
Player noticed
≠
Player understood
≠
Player intervened correctly
```

14. 현재 가장 큰 Evidence Gap은:
   - Oxygen Not Included형 물질 / 열 / 가스 Causal Simulation
   - Factorio형 Production / Logistics
   - The Sims형 Social / Life Simulation
   - Dwarf Fortress형 Large Agent / Emergence
   - Player Mental Model telemetry
   - Cascade diagnosis
   - Stable / Runaway state
   - Director vs natural simulation
   - Physics / Vehicle / Sports Simulation
   - Underperforming Simulation Control Cases

---

# 2. Simulation Genre Definition

Studio OS에서 Simulation은 다음과 같이 정의한다.

> **게임 내부의 Entity / State / Rule이 일관된 Causal Model에 따라 작동하여, 시간 또는 Trigger를 통해 새로운 State를 생성하는 구조.**

기본 형태:

```text
State
+
Rule
+
Interaction
+
Time / Trigger
↓
New State
```

Simulation은 반드시:
- 현실적 그래픽
- 수많은 Entity
- 실제 물리
를 요구하지 않는다.

---

# 3. Simulation vs Management

이 구분은 필수다.

## 3.1 Management

```text
State 관찰
↓
Priority 결정
↓
Limited Capacity 배분
↓
결과
↓
Reprioritize
```

핵심은 **Player Decision Structure**다.

예:

```text
Food 부족
↓
누구에게 배급할지 결정
```

---

## 3.2 Simulation

```text
Nutrition ↓
↓
Health ↓
↓
Work Capacity ↓
↓
Production ↓
↓
Food Supply ↓
```

핵심은 **World Causal Model**이다.

---

## 3.3 Deduplication Rule

다음은 Simulation Core로 복제하지 않는다.

- Priority Conflict
- Resource Scarcity
- Workforce Allocation
- Automation UX
- Management Target Growth

Simulation에서는:

> **State가 어떤 Rule로 변하고 다른 State에 어떻게 영향을 미치는가**

에만 집중한다.

---

# 4. Simulation vs Realism

Simulation Quality를 Reality Detail과 동일시하지 않는다.

```text
More Variables
≠
Better Simulation
```

```text
More Realistic Detail
≠
More Useful Model
```

```text
More Entities
≠
More Emergence
```

## 4.1 Fidelity 분류

### Physical Fidelity

현실 물리와 얼마나 유사한가.

### Behavioral Fidelity

Agent / System 행동이 기대되는 행동과 얼마나 유사한가.

### Causal Fidelity

플레이어가 이해한 Cause → Effect가 일관되게 작동하는가.

## Reviewer Principle

> **Simulation Promise에 필요한 Fidelity가 무엇인지 먼저 정의한다.**

RimWorld 같은 Story Generator에 Vehicle-level Physics Fidelity를 요구하지 않는다.

Mini Metro 같은 Abstract Network Game에 개별 시민 전체 생활 AI를 요구하지 않는다.

---

# 5. Evidence Scope / Limitation

## Stronger Coverage

- Colony Simulation
- Character-state Simulation
- Story-generating Simulation
- Systemic Ship / Crisis Simulation
- Network / Flow Simulation
- Abstract Production / Process Simulation
- Management-Simulation Hybrid
- Selective / Small-state Simulation

## Weak Coverage

- Vehicle Simulation
- Sports Simulation
- Physics Sandbox
- Industrial Process Simulation
- Large-scale Economy Simulation
- Social / Life Simulation
- Detailed Historical Simulation
- Hardcore Realism Simulation

따라서:

> **RimWorld / FTL에서 추출된 Causal Interaction Rule을 모든 Simulation Subtype의 Product Promise로 강제하지 않는다.**

현재 문서의 Core는:
- Causal Model
- Selective Modeling
- Cross-system Propagation
같은 비교적 저수준 Mechanism에 한정한다.

---

# 6. Source Classification

# 6.1 Tier A — Primary Simulation Evidence

## REF-13 — RimWorld

**Subtype:** `Colony / Character / Story-generating Simulation`  
**Evidence Strength:** VERY HIGH

### Strong Evidence Areas

- Selective Simulation
- Character State
- Relationship
- Persistent Consequence
- System Interaction
- Event Director
- Emergent Outcome
- State Memory
- Spatial Cause Visibility

### Key Evidence

Reference의 Primary Lesson은:

- 모든 현실적 기능을 구현하지 않는다.
- “어떤 이야기를 생성할 것인가”에 기여하는 System을 선택한다.
- Character trait / relationship / injury / need가 사건을 개인적 맥락으로 바꾼다.
- Storyteller는 사건 빈도와 압박을 조절한다.

Primary Warning:

> 시스템 수와 Random Event를 많이 넣는 것 자체가 Story Generator를 만들지는 않는다. 사건이 Character State와 장기 기억에 연결되어야 한다.

### Why Primary

Simulation Purpose / Selective Modeling / Persistent State / Interaction / Director의 경계를 직접 다루는 Developer GDC 기반 Reference다.

---

## REF-02 — FTL: Faster Than Light

**Subtype:** `Systemic Ship / Crisis Simulation`  
**Evidence Strength:** VERY HIGH

### Strong Evidence Areas

- System Damage
- Oxygen
- Fire
- Crew
- Power
- Repair
- Room / Spatial State
- Cascading Crisis
- System Interaction
- Abstract Representation

### Key Evidence

FTL은 우주선 내부를 상태 머신처럼 표현한다.

같은 기본 규칙에서:
- Fire
- Oxygen loss
- Crew displacement
- System damage
- Power allocation
이 결합해 서로 다른 Crisis를 만든다.

Reference의 직접 Lesson:

> **서로 연결된 단순 시스템은 많은 독립 콘텐츠보다 큰 상황 다양성을 만든다.**

### Boundary

FTL의:
- Roguelike Reset
- Route Risk
- Meta
는 Simulation Core로 복제하지 않는다.

---

# 6.2 Tier B — Strong Simulation / Hybrid Evidence

## REF-14 — Mini Metro

**Subtype:** `Network / Demand Simulation`

### Use

- Demand generation
- Flow
- Bottleneck
- Capacity
- Network state
- Procedural demand
- Visual abstraction

### Evidence Decision

Simulation 구조는 명확하다.

```text
station / passenger generation
↓
network flow
↓
congestion
↓
failure pressure
```

하지만 현재 Reference의 가장 강한 Primary Lesson은 Scope / Production Constraint다.

따라서 Tier A로 승격하지 않고 **Strong Tier B**로 유지한다.

---

## REF-15 — This War of Mine

**Subtype:** `Survival / Character-state Simulation Hybrid`

### Use

- Character state
- Injury / attrition
- Survival condition
- Persistent consequence
- Human-state interaction

### Boundary

Reference의 가장 강한 Lesson은:
- Theme-System Alignment
- Survival / Moral Choice
다.

따라서:
- scarcity
- moral trade-off
를 Simulation Core로 복제하지 않는다.

Simulation에서는:

> Character State가 지속되고 다른 행동 가능성과 생존 상태에 영향을 미친다.

는 범위만 보조 Evidence로 사용한다.

---

## REF-22 — Stacklands

**Subtype:** `Abstract Production / Village Simulation`

### Use

- Resource transformation
- Recipe
- Production chain
- Spatial combination
- Common interaction grammar

### Boundary

카드 UI 자체는 Simulation Evidence가 아니다.

강한 보조 질문:

> **현실적 표현 없이도 일관된 Transformation Rule만으로 World Model을 만들 수 있는가?**

---

## REF-19 — Cultist Simulator

**Subtype:** `Abstract State / Process Simulation`

### Use

- person
- emotion
- knowledge
- time
- action
의 추상 State Modeling.

### Boundary

현재 Reference의 핵심은:
- common UI grammar
- discovery
- cognitive load
이다.

따라서 Abstraction Conflict의 보조 Evidence로만 사용.

---

## REF-07 — Against the Storm

**Subtype:** `Management / Settlement Simulation Hybrid`

### Use

- Environment State
- Production
- Population
- Resource coupling
- State variation

### Boundary

Management의:
- priority
- economy
- run adaptation
을 Simulation Core로 복제하지 않는다.

---

# 6.3 Tier C — Adjacent / Control

필요한 특정 Mechanism 비교에만 사용한다.

- Papers, Please
- Loop Hero
- Reigns
- Invisible, Inc.
- Dorfromantik
- Citizen Sleeper
- Into the Breach

Tier C만으로 Provisional Simulation Core를 승격하지 않는다.

---

# 7. Universal / Existing Genre Core Audit

# 7.1 UC-DESIGN-003 — Consequence-to-Next-Decision Coupling

Simulation에서 그대로 복제하지 않는다.

Strategy / Management 관점:
> 결과가 다음 판단을 바꾸는가?

Simulation 관점:
> **한 State 변화가 어떤 다른 State에 Rule-based consequence를 전파하는가?**

따라서 `GC-SIM-002`는 World Model 쪽 specialization이다.

---

# 7.2 UC-DESIGN-005 — Actionable Information

`Model Legibility`와 중복 가능성이 높다.

Simulation specialization:

> **결과의 주요 Cause Chain을 Player가 관찰하고 자신의 Mental Model과 비교할 수 있는가?**

독립 Provisional로 만들지 않고 Candidate 유지.

---

# 7.3 Management Core Audit

복제 금지:
- Priority Conflict
- Loss Recovery decision
- Information for priority
- Growth / Constraint
- Automation

Simulation은:
- State transition
- dependency
- causal propagation
만 본다.

---

# 7.4 Narrative Core Audit

Emergent Story가 좋다는 결론은 Narrative/Human 영역이다.

Simulation에서:
- event chain
- persistent state
- rule interaction
까지만 구조적으로 본다.

---

# 7.5 Strategy Core Audit

Future Option / Replanning을 Simulation Core로 복제하지 않는다.

Simulation에서는:
> Player가 계획을 바꾸는가
보다 먼저
> World State가 실제로 어떤 Rule로 바뀌는가
를 본다.

---

# 8. Provisional Simulation Cores

# GC-SIM-001 — Selective Simulation Should Preserve Experience-Relevant Causality

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

강한 Simulation 사례는 “현실 전체”를 구현하지 않는다.

대신 Player Fantasy / Core Experience에 필요한:
- State
- Relationship
- Flow
- Damage
- Need
- Transformation

만 선택하고 그 Cause → Effect를 일관되게 모델링한다.

## Simulation Context

- Colony Simulation
- Systemic Simulation
- Network Simulation
- Abstract Simulation
- Simulation Hybrid

## Rule

> **Simulation Detail은 현실에서 존재하는가가 아니라, 의도한 Player Experience를 만들기 위해 어떤 Cause / Effect를 반드시 모델링해야 하는가로 선택한다. 생략된 Detail이 많아도 핵심 Causal Promise가 유지되면 Simulation은 성립할 수 있다.**

## Mechanism

Feature-first:

```text
현실에 존재
↓
Stat / System 추가
↓
State Count 증가
```

Experience-first:

```text
Simulation Promise
↓
필요한 Cause / Effect 선정
↓
State / Rule 구현
↓
불필요한 Detail 제외
```

## Primary Evidence

### RimWorld

가장 강한 직접 Evidence.

Reference는:
- 모든 현실적 기능을 구현하지 않고
- “어떤 이야기를 생성할 것인가”에 기여하는 시스템만 선택

한다는 설계 원칙을 정리한다.

Character:
- Trait
- Relationship
- Injury
- Need
는 Story-generating Purpose에 기여하기 때문에 모델링된다.

### FTL

FTL은 3D 우주 전투의 물리적 정밀성보다:
- Power
- Oxygen
- Fire
- Crew
- Room Damage
를 모델링해 `Captain Fantasy`를 압축한다.

Reference는 기능 목록보다 핵심 판타지를 먼저 고정하고, Ship cutaway와 연결된 System에 비용을 집중한 점을 주요 Lesson으로 둔다.

## Secondary Evidence

### Mini Metro

도시를:
- 도로
- 건물
- 개별 Citizen Life
전체로 모델링하지 않고

```text
Station
Passenger Demand
Line
Train
Tunnel
Congestion
```

으로 압축한다.

### Stacklands

현실적인 마을 Simulation 대신:
- resource
- recipe
- spatial stack
으로 생산 관계를 추상화한다.

### Cultist Simulator

사람 / 감정 / 지식 / 시간 / 행동을 공통 카드와 슬롯으로 추상화한다.

## Counter Evidence

### Hardcore Realism Simulation

정확한 물리 / 차량 / 산업 Process 자체가 Product Promise라면 Detail은 그 자체로 Player Value일 수 있다.

이 경우 “줄이는 것”이 정답이 아니다.

## Applies To

강하게:
- Systemic Simulation
- Colony Simulation
- Abstract Simulation
- Network Simulation

조건부:
- Survival Simulation
- Economy / Production Simulation

Evidence Gap:
- Vehicle
- Physics
- Sports
- Historical

## Boundary / Exceptions

Selective Simulation은:

> 최소 시스템이 항상 좋다.

가 아니다.

정확한 질문은:

> **이 Detail이 Promise에 필요한 Causality를 추가하는가?**

다.

## Observed Metric

Reference에 공통 정량 Metric 없음.

## Candidate Metric — Structural

- Modeled State Count
- Dependency Edge Count
- Unused State Count
- State with No Downstream Effect
- Simulation Feature → Core Outcome Mapping

마지막 두 항목은 project-specific definition이 필요할 수 있다.

## Candidate Metric — Human

- Simulation Fantasy
- Detail Value
- Abstraction Acceptance
- “빠져서 Fantasy가 깨진 요소” 설명

## Validation Type

Structural / model-dependent + Human.

## AI Tester Applicability

MEDIUM.

Machine은:
- state dependency
- unused state
를 찾을 수 있지만

> 어떤 Cause가 Experience에 필요한가

는 Human / design judgment가 필요하다.

## Confidence

**VERY HIGH**

## Reviewer Action

새 Stat / AI / Physics Detail마다:

> **“이 State를 제거하면 어떤 Player-visible Cause / Effect가 사라지는가?”**

를 묻는다.

답이 없으면 `REALISM_WITHOUT_VALUE_RISK`.

---

# GC-SIM-002 — System States Should Propagate through Causal Dependencies

**Status:** `PROVISIONAL CORE`  
**Origin:** `UC-DESIGN-003 SIMULATION SPECIALIZATION`

## Pattern

Systemic Simulation의 깊이는 System 수보다:
- State A 변화가
- State B / C 조건을 바꾸고
- 그 결과가 다시 후속 State를 변화시키는

Dependency에서 발생한다.

## Rule

> **핵심 Simulation State는 고립된 Meter로 존재하기보다 적어도 일부가 다른 State의 Transition Condition 또는 Outcome에 영향을 주어야 한다. System 수보다 Causal Dependency와 Propagation을 평가한다.**

## Mechanism

Isolated:

```text
Hunger -10
Mood -10
Temperature -10
```

서로 독립적으로 감소.

Systemic:

```text
Hunger ↓
↓
Health / Work Capacity ↓
↓
Production ↓
↓
Resource State 변화
```

또는:

```text
Fire
↓
Oxygen ↓
+
System Damage
+
Crew Reposition
↓
Repair Capacity 변화
```

## Primary Evidence

### FTL

가장 강한 직접 Systemic Evidence.

Reference는:

> 연결된 소수 시스템이 독립 콘텐츠보다 큰 상황 다양성을 만든다.

고 정리한다.

- Fire
- Oxygen
- Doors / Rooms
- Crew
- Power
- System Damage

가 같은 공간에서 서로 영향을 준다.

### RimWorld

- Character Need
- Injury
- Relationship
- Production
- Event
- Wealth / Threat
등이 장기 State로 이어져 같은 사건도 Colony 상태에 따라 다른 결과를 만든다.

## Secondary Evidence

### Mini Metro

```text
Demand
↓
Passenger accumulation
↓
Network congestion
↓
Station overload
```

의 Flow dependency가 단일 Network System 안에서 발생한다.

### This War of Mine

Character 상태와 생존 Resource가 지속적인 attrition 구조에 연결되는 보조 사례.

### Against the Storm

환경 / 생산 / 주민 / 자원의 coupling이 정착 State를 바꾸는 Hybrid 사례.

## Counter Evidence

### Pure Process / Toy Simulation

한 개의 독립 모델을 관찰하는 것이 Product Promise라면 Cross-system interaction이 적어도 성립할 수 있다.

예:
- single mechanical toy
- focused physics demonstration

## Applies To

강하게:
- Systemic Simulation
- Colony Simulation
- Survival Simulation
- Production / Logistics Simulation
- Network Simulation

조건부:
- Agent / Life Simulation

약하게:
- Focused Physics Toy

## Boundary

모든 System이 모든 System과 연결될 필요는 없다.

오히려 과도한 coupling은:
- diagnosis
- QA
- balancing
을 악화시킬 수 있다.

핵심은:

> **Player-visible Outcome에 기여하는 dependency가 실제 존재하는가?**

다.

## Observed Metric

공통 Source telemetry 없음.

## Candidate Metric — Structural / Simulation

- Dependency Edge Count
- Cross-system Transition Rate
- Multi-system Event Rate
- Causal Chain Depth
- Causal Chain Frequency
- Isolated System Rate
- Secondary State Change Count
- Interaction Coverage

`Causal Chain`, `Isolated System`, `Meaningful Interaction`은 Formal Definition 필요.

## Candidate Metric — Human

- Cause Recognition
- Mental Model Accuracy
- Cascade Legibility

## AI Tester Applicability

**VERY HIGH**

## Confidence

**VERY HIGH**

## Reviewer Action

각 핵심 State에 대해 두 줄을 강제로 작성한다.

```text
What changes this state?
What does this state change?
```

두 번째가 비어 있다면:
`ISOLATED_STATE_RISK`.

---

# 9. Simulation Core Candidates

# GC-SIM-003 — Emergence Requires Persistent Rule Interaction, not Event Count

**Status:** `CANDIDATE`  
**Origin:** `NEW GENRE CORE`

## Rule Candidate

> **Emergence를 Random Event 수나 Procedural Content 수로 평가하지 않는다. Persistent State와 반복 Rule이 결합해 직접 Script하지 않은 Outcome Chain을 생성하는지 본다.**

## Primary Evidence

### RimWorld

Primary Warning:

> 시스템 수와 Random Event를 많이 넣는 것 자체가 Story Generator를 만들지 않는다. 사건이 Character State와 장기 기억에 연결되어야 한다.

### FTL

Fire / Oxygen / Damage / Crew / Power가 결합해:
개별 Crisis Script보다 System combination으로 다양한 위기를 만든다.

## Secondary Evidence

### Stacklands

Recipe / Resource / Spatial Combination이 같은 Rule grammar로 여러 생산 Outcome을 만든다.

## Promotion Blocker

`Emergence`의 의미가:
- story
- physics
- economy
- social
- production
Subtype마다 크게 다르다.

현재 Direct Evidence는 Story/Systemic Crisis 쪽에 편중.

## Candidate Metric — Structural / Simulation

- System-generated Outcome Count
- Multi-system Event Rate
- Event Chain Length
- State-conditioned Outcome Diversity
- Same Rules / Different State Outcome Divergence
- Orphan Random Event Rate

`System-generated Event`는 Formal Definition 필요.

## Human

- Emergent Outcome Recognition
- “예상하지 못했지만 규칙상 납득 가능했다” 평가

## Confidence

**MEDIUM-HIGH**

---

# GC-SIM-004 — Major Outcomes Need Diagnosable Causes

**Status:** `CANDIDATE`  
**Origin:** `UC-DESIGN-005 SPECIALIZATION`

## Rule Candidate

> **Simulation의 중요한 Outcome은 Player가 주요 Cause Chain을 추적할 수 있어야 한다. 모든 내부 State를 노출할 필요는 없지만, 실패 / 붕괴 / 변화가 무엇 때문에 발생했는지 확인할 수 있어야 Intervention과 Mental Model이 형성된다.**

## Evidence

### FTL

Ship cutaway 하나가:
- Crew
- Oxygen
- System
- Damage
를 공간적으로 보여준다.

### Mini Metro

노선도 abstraction이:
- station
- passenger
- route
- congestion
을 직접 보이게 한다.

### RimWorld

기지 공간과 주민 행동이 복잡한 Colony State를 관찰하게 한다.

## Duplicate Risk

- `UC-DESIGN-005`
- `GC-MGMT-007 Information Supports Diagnosis`
와 중복이 강하다.

Simulation-specific 차이는:

> Priority가 아니라 **Causal Model diagnosis**에 정보가 쓰인다는 점.

## Candidate Metric

### Structural
- Cause → Effect Trace Availability

### Structural / model-dependent
- Hidden Dependency Count
- Unexplained Transition Count

### Instrumented
- State Panel View
- Diagnostic Screen Usage
- State Lookup
- Time to Diagnose

### Human
- Mental Model Accuracy
- Cause Recognition
- Diagnostic Burden
- Model Trust

## Confidence

**HIGH as specialization / MEDIUM need for independent GC**

---

# GC-SIM-005 — Agent Differences Should Change Behavior or Interaction

**Status:** `CANDIDATE`

## Rule Candidate

> **Trait / Need / Relationship / Skill을 Agent Specificity로 제시한다면 그 차이가 Behavior, Interaction 또는 Outcome을 실제로 바꾸어야 한다. Cosmetic label만 늘리는 것은 Agent Simulation Depth로 평가하지 않는다.**

## Primary Evidence

### RimWorld

가장 강한 Evidence.

Reference는:
- Trait
- Relationship
- Injury
- Need
가 시스템 사건을 개인적 사건으로 바꾼다고 정리한다.

## Secondary Evidence

This War of Mine:
Character 상태와 생존 결과의 차이가 의미 있는 보조 사례.

## Promotion Blocker

Agent / Social / Life Simulation의 두 번째 강한 Direct Primary 부족.

## Candidate Metric — Structural / Simulation

- Agent State Diversity
- Behavior Distribution
- Trait → Behavior Shift
- Trait → Outcome Shift
- Relationship Interaction Rate
- Homogeneous Behavior Rate

`Trait → Behavior Shift`는 Formal Definition 필요.

## Human

- Agent Believability
- Character Specificity Recognition

## Confidence

**MEDIUM-HIGH**

---

# GC-SIM-006 — Autonomous Systems Need Meaningful Observation / Intervention

**Status:** `CANDIDATE`

## Rule Candidate

> **Autonomous System이 많이 움직인다는 사실만으로 Simulation Agency가 생기지 않는다. Product Promise가 Intervention을 포함한다면 Player가 World State를 관찰하고 Rule / Environment / Priority / Configuration 수준에서 의미 있게 개입할 수 있어야 한다.**

## Evidence

### RimWorld
주민이 자율적으로 행동하지만 Player는:
- work
- environment
- priority
- construction
을 통해 간접 개입한다.

### Mini Metro
승객 Flow는 자동이지만 Player가 Network를 재구성한다.

### FTL
일부 system behavior는 자동 진행되지만 Player가:
- crew
- doors
- power
- repair
에 개입한다.

## Counter Evidence

Observation Sandbox / Aquarium-like Simulation에서는 개입이 핵심이 아닐 수 있다.

## Candidate Metric

- Autonomous Transition Rate
- Player-triggered Transition Rate
- Intervention Frequency
- Intervention → State Change
- Manual Override Rate

## Human

- Intervention Understanding
- Alive-world Perception
- Agency

## Confidence

**MEDIUM-HIGH**

---

# GC-SIM-007 — Stable / Runaway / Cascade States Need Explicit Boundaries

**Status:** `CANDIDATE`

## Rule Candidate

> **Simulation은 안정 상태, Positive Feedback, Cascade를 만들 수 있다. 이 상태를 자동 결함으로 보지 않되, 어떤 조건에서 시작·유지·회복·붕괴하는지 Formal하게 정의하고 Player Experience에 맞는지 검증한다.**

## Evidence

### FTL
작은 Damage가:
- Fire
- Oxygen
- Crew injury
- Repair loss
로 연쇄될 수 있다.

### RimWorld
부상 / 자원 / mood / event가 복합적으로 Colony 위기를 확대할 수 있다.

### Mini Metro
수요 증가와 congestion이 지속되면 특정 station failure로 이어진다.

## Why Candidate

Stable / Runaway / Cascade의 적정성은 Subtype / Product Promise 차이가 큼.

## Candidate Metric

- Cascade Frequency
- Cascade Depth
- Cascade Size
- Runaway State Entry
- Stable State Entry
- Time to Stability
- Stability Duration
- Recovery after Cascade
- Simulation Collapse

대부분 project-specific model 필요.

## Human

- Cascade Fairness
- Stable-state Experience
- Diagnostic Burden

## Confidence

**MEDIUM-HIGH**

---

# GC-SIM-008 — Event Directors Should Modulate, not Replace, Simulation

**Status:** `CANDIDATE`

## Rule Candidate

> **Storyteller / Director / Pacing Controller를 사용할 경우 Simulation에서 발생 가능한 State와 압력을 조정해야지, World Rule을 무시한 결과를 반복적으로 강제해 Simulation Cause를 대체하지 않는지 검토한다.**

## Primary Evidence

### RimWorld

AI Storyteller가:
- 사건 빈도
- 압박
을 조절하지만 Character / Colony State와 결합해 Story가 만들어진다.

Reference Warning은:
Random Event 수만으로 Story Generator가 되지 않는다고 명시한다.

## Promotion Blocker

현재 Direct Director Evidence가 RimWorld에 강하게 편중.

## Candidate Metric

- Director-triggered Event Rate
- State-conditioned Director Event Rate
- Director Override Count
- Director Event → Existing State Interaction Rate

## Human

- “조작당했다” perception
- Event Fairness
- Story / Simulation coherence

## Confidence

**MEDIUM**

---

# GC-SIM-009 — Abstraction Can Preserve Simulation through Causal Fidelity

**Status:** `CANDIDATE / MERGE CANDIDATE → GC-SIM-001`

## Rule Candidate

> **현실적 표현을 줄여도 핵심 State와 Cause / Effect가 유지되면 Simulation Fantasy가 성립할 수 있다. Abstraction의 품질은 Detail 손실보다 Causal Fidelity 보존으로 평가한다.**

## Evidence

- FTL — ship cutaway abstraction.
- Mini Metro — schematic network.
- Stacklands — card/resource transformation.
- Cultist Simulator — card/slot process abstraction.

## Why not Provisional

`GC-SIM-001 Selective Simulation`과 중복 가능성이 매우 높다.

독립 Core보다:
`GC-SIM-001 Sub-rule`
로 통합 가능성이 높다.

## Candidate Metric

- Decision / Fantasy-relevant State Coverage
- Hidden Cause Count after abstraction
- Representation → State Mapping

## Human

- Abstraction Acceptance
- Simulation Fantasy
- Model Legibility

## Confidence

**HIGH as sub-rule**

---

# 10. Simulation Anti-Patterns

# AP-SIM-001 — More Variables = Better Simulation

## Trigger
Stat / State 종류를 계속 증가.

## Mechanism
State 간 Dependency 없이 독립 Meter만 늘어남.

## Consequence
- cognitive load
- UI cost
- QA
- false depth

## Evidence
RimWorld / FTL의 강점은 단순 State Count보다 Purpose / Interaction에 있다.

## Detection
- State Count
- Dependency Edge Count
- Isolated State Rate
- State with No Downstream Effect

## Mitigation
새 State마다:
```text
What changes it?
What does it change?
Why is it modeled?
```
를 작성.

---

# AP-SIM-002 — Realism without Player Value

## Trigger
“현실에 있으니까” System 추가.

## Consequence
- scope 증가
- diagnosis complexity
- no meaningful experience gain

## Evidence
RimWorld Selective Simulation.
FTL fantasy-first abstraction.

## Detection
- Feature → Core Experience Mapping
- unused state
- human detail value

## Mitigation
Player Fantasy / Causal Promise 기준으로 제거.

---

# AP-SIM-003 — Systems without Interaction

## Trigger
System은 많지만 독립적으로 값만 변함.

## Consequence
Complexity without emergence.

## Evidence
FTL의 반대 사례:
연결된 소수 시스템이 Crisis variety를 만든다.

## Detection
- Isolated System Rate
- Cross-system Transition Rate
- Interaction Coverage

## Mitigation
새 System보다 dependency 먼저 검토.

---

# AP-SIM-004 — Random Events as Emergence

## Trigger
Random Event pool 수를 Emergence로 간주.

## Consequence
결과는 달라도 World History와 Rule interaction은 약함.

## Evidence
RimWorld Primary Warning.

## Detection
- Random / Scripted Event Rate
- State-conditioned Event Rate
- Event → Persistent State
- Event chain dependency

## Mitigation
Event가 기존 State를 읽고 후속 State를 남기게 한다.

---

# AP-SIM-005 — Scripted Outcome Disguised as Simulation

## Trigger
같은 시스템처럼 보이지만 대부분 예외 Script.

## Consequence
Player Mental Model 붕괴.

## Detection
- Rule coverage
- exception count
- special-case transition rate

## Mitigation
공통 Rule로 가능한 Outcome과 authored exception을 구분.

---

# AP-SIM-006 — Invisible Causal Chain

## Trigger
결과는 보이지만 원인 Dependency를 확인할 수 없음.

## Consequence
- diagnosis failure
- random-feeling outcome
- weak intervention learning

## Detection
- Unexplained Transition
- Time to Diagnose
- Cause Recognition

## Mitigation
state trace / visualization / event log.

---

# AP-SIM-007 — State Explosion without Meaning

## Trigger
State combination만 늘어나고 Player-visible outcome은 비슷함.

## Consequence
QA / save / debugging 비용만 증가.

## Detection
- State Combination Coverage
- Outcome Diversity
- Low-impact State Count

## Mitigation
State를 outcome / behavior difference와 연결.

---

# AP-SIM-008 — Homogeneous Agents with Cosmetic Traits

## Trigger
Trait 이름은 다르지만 behavior / interaction 동일.

## Consequence
Agent count는 많아도 Simulation variety 낮음.

## Detection
- Trait → Behavior Shift
- Behavior Distribution
- Trait → Outcome Shift

## Mitigation
Trait 수보다 behavior rule difference 우선.

---

# AP-SIM-009 — Detail below Responsibility Level

## Trigger
Player Promise와 관계없는 미세 State까지 이해 / 관리 요구.

## Consequence
administrative burden.

## Boundary
Hardcore realism은 예외 가능.

## Detection
- panel usage
- manual intervention
- human detail value
- ignored state

## Mitigation
abstraction / aggregation / automation.

---

# AP-SIM-010 — Autonomous System without Intervention

## Trigger
World는 복잡하게 움직이지만 Player influence가 거의 없음.

## Consequence
Intervention-based Simulation에서는 관전 게임화.

## Boundary
Observation Sandbox는 예외.

## Detection
- autonomous vs player-triggered transition
- intervention effect size

## Mitigation
constraint / environment / policy / direct intervention channel.

---

# AP-SIM-011 — Intervention without Feedback

## Trigger
Player가 설정을 바꾸지만 결과 확인이 어려움.

## Consequence
mental model formation 실패.

## Detection
- intervention → observable state
- feedback latency
- human intervention understanding

## Mitigation
before / after state exposure.

---

# AP-SIM-012 — Stable State = No Game

## Trigger
한번 균형을 만들면 더 이상 meaningful change 없음.

## Consequence
Goal-driven Simulation에서는 decision collapse 가능.

## Boundary
Relaxation / sandbox에서는 stable state 자체가 reward일 수 있음.

## Detection
- Stable State Entry
- Stability Duration
- intervention frequency after stability
- human stable-state experience

## Mitigation
Product Promise에 따라:
- end
- expand
- experiment
- new objective
중 선택.

---

# AP-SIM-013 — Cascading Failure without Diagnosis

## Trigger
Chain reaction은 크지만 start cause가 안 보임.

## Consequence
Crisis가 systematic하지 않고 arbitrary하게 느껴짐.

## Detection
- Cascade Depth
- Failure Chain Source
- Cause Recognition

## Mitigation
cause trace / warning / state log / gradual propagation.

---

# AP-SIM-014 — Simulation Detail as Content Count

## Trigger
Entity / Recipe / Stat 수를 Variety로 사용.

## Consequence
Content cost만 증가하고 interaction pattern 동일.

## Detection
- content count vs interaction type
- behavior / outcome diversity

## Mitigation
새 data보다 new causal relationship 우선.

---

# AP-SIM-015 — Director Overrides Simulation

## Trigger
Director가 World State와 관계없이 위기 / 보상을 강제.

## Consequence
Player Mental Model보다 external scripting이 결과를 지배.

## Evidence
RimWorld의 Director는 강하지만 Random Event만으로 Story Generator가 되지 않는다는 Warning이 Boundary를 제공한다.

## Detection
- director state dependency
- override count
- impossible-state event

## Mitigation
Director가 pressure를 선택하되 World Rule은 유지.

---

# 11. Conflicting Findings

# CF-SIM-001 — Realism vs Abstraction

## Abstraction Evidence

- FTL
- Mini Metro
- Stacklands
- Cultist Simulator

## Selective Realism

RimWorld:
일부 Character / Colony State는 세밀하지만 전체 현실을 재현하지 않는다.

## Hidden Variable

`Simulation Promise`

## Resolution

Physical Fidelity가 아니라:
- Causal Fidelity
- Behavioral Fidelity
- Player Fantasy
를 먼저 정의한다.

---

# CF-SIM-002 — Direct vs Indirect Control

## Direct / tactical intervention

FTL:
crew / doors / power / repair.

## Indirect

RimWorld:
priority / environment / work.

Mini Metro:
network configuration.

## Hidden Variable

`Player Responsibility Level`

## Resolution

Control 방식이 아니라:
> Player가 어떤 State에 어떤 수준으로 개입해야 Simulation Fantasy가 성립하는가?
를 본다.

---

# CF-SIM-003 — Deterministic vs Probabilistic Simulation

확률은 Emergence의 필수 조건이 아니다.

Deterministic rule도 interaction으로 복잡한 outcome을 만들 수 있다.

## Resolution
Probability 비율을 Simulation Quality로 사용하지 않는다.

---

# CF-SIM-004 — Autonomous Simulation vs Player-driven System

Autonomy가 높을수록 alive-world perception이 늘 수 있으나:
- agency
- diagnosis
- control
이 줄 수도 있다.

Observation Sandbox와 Intervention Simulation을 구분한다.

---

# CF-SIM-005 — Accuracy vs Readability

상세 Model은 정확할 수 있지만 Player가 Cause를 이해하기 어려울 수 있다.

FTL / Mini Metro는 추상화를 통해 State를 압축한다.

## Resolution
Accuracy와 Mental Model Formation을 별도 검증.

---

# CF-SIM-006 — Emergence vs Authored Control

## Emergent-heavy
RimWorld.

## Authored thematic control
This War of Mine.

## Hybrid
Event + Simulation State.

## Resolution
Scripted Event가 있다는 이유로 Simulation 품질을 감점하지 않는다.

중요한 것은:
> Event가 World Rule / State와 어떤 관계를 갖는가?
다.

---

# CF-SIM-007 — Stable System vs Constant Disruption

Stable State가:
- achievement
- sandbox playground
일 수 있다.

Goal-driven survival에서는:
- solved state
가 될 수 있다.

## Hidden Variable
Product Promise.

---

# CF-SIM-008 — Large Entity Count vs Rich Entity State

100 homogeneous agents와 10 heterogeneous agents 중 어느 쪽이 더 좋은 Simulation인지 일반화하지 않는다.

평가:
- behavior diversity
- interaction
- performance
- readability
- player fantasy.

---

# 12. Structural / Simulation Validation Map

# 12.1 State Metrics

| Metric | Type |
|---|---|
| State Count | Structural |
| State Transition Count | Structural / Simulation |
| State Duration | Simulation |
| State Distribution | Simulation |
| State Combination Coverage | Simulation / model-dependent |
| Impossible State Count | Structural |
| Contradictory State Count | Structural / model-dependent |
| Invalid Transition Count | Structural |

---

# 12.2 Causal Metrics

| Metric | Type |
|---|---|
| Cause → Effect Transition Rate | Simulation |
| Dependency Edge Count | Structural |
| Causal Chain Depth | Structural / model-dependent |
| Causal Chain Frequency | Simulation / model-dependent |
| Trigger → Outcome Distribution | Simulation |
| Unexplained Transition Count | Structural / model-dependent |

---

# 12.3 Interaction Metrics

| Metric | Type |
|---|---|
| Cross-system Interaction Count | Structural / model-dependent |
| Cross-system Transition Rate | Simulation |
| Isolated System Rate | Structural / model-dependent |
| Multi-system Event Rate | Simulation / model-dependent |
| Interaction Coverage | Simulation / model-dependent |

---

# 12.4 Agent Metrics

Subtype 해당 시:

| Metric | Type |
|---|---|
| Agent State Diversity | Simulation |
| Behavior Distribution | Simulation |
| Trait → Behavior Shift | Structural / model-dependent |
| Relationship Interaction | Simulation |
| Agent Survival / Failure | Simulation |
| Agent Idle Rate | Simulation |

---

# 12.5 Cascade Metrics

| Metric | Type |
|---|---|
| Cascade Frequency | Simulation / model-dependent |
| Cascade Depth | Structural / model-dependent |
| Cascade Size | Simulation / model-dependent |
| Recovery after Cascade | Simulation |
| Failure Chain Source | Structural / model-dependent |
| Secondary Failure Count | Simulation |

---

# 12.6 Feedback Loop Metrics

| Metric | Type |
|---|---|
| Positive Feedback Strength | Structural / model-dependent |
| Negative Feedback Strength | Structural / model-dependent |
| Runaway State Entry | Structural / model-dependent |
| Stable State Entry | Structural / model-dependent |
| Time to Stability | Simulation / model-dependent |
| Stability Duration | Simulation / model-dependent |

---

# 12.7 Intervention Metrics

| Metric | Type |
|---|---|
| Player Intervention Frequency | Player Telemetry / Simulation only if explicit action |
| Intervention → State Change | Simulation / Instrumented |
| Intervention Success | Model-dependent |
| Intervention Delay | Player Telemetry / Simulation if explicit |
| Intervention Reversal | Player Telemetry / Simulation |
| Automated Resolution Rate | Simulation |

---

# 12.8 Autonomy Metrics

| Metric | Type |
|---|---|
| Autonomous Transition Rate | Simulation |
| Player-triggered Transition Rate | Simulation |
| Agent Self-resolution | Simulation / model-dependent |
| Unobserved State Change | Simulation Log only |

### Interpretation Rule

`Unobserved State Change`는:
> World가 Player에게 안 보였다
가 아니라
> State Log상 Player Interaction 없이 변화했다
를 의미한다.

실제 Player가 그 변화를 보았는지는 Player Telemetry / Human Test가 필요하다.

---

# 12.9 Event Metrics

| Metric | Type |
|---|---|
| Scripted Event Rate | Structural / model-dependent |
| System-generated Event Rate | Structural / model-dependent |
| Hybrid Event Rate | Structural / model-dependent |
| Event Repeat | Simulation |
| State-conditioned Event Rate | Simulation |

Classification Formal Definition 필요.

---

# 12.10 Edge-state Metrics

- Zero-resource stability
- No-path behavior
- Max-entity behavior
- All-agent-disabled state
- Full-storage behavior
- State deadlock
- Infinite loop
- Oscillation
- Invalid transition
- State corruption

모두 Structural / Simulation 테스트 대상.

---

# 13. Simulation Tester Profile Map

Human Persona보다 System Stress Profile을 우선한다.

# P-SIM-001 — Baseline Observer

## Policy

최소 개입.

## Purpose

- autonomous behavior
- natural equilibrium
- default collapse
- autonomous transition

---

# P-SIM-002 — Optimizer

## Policy

효율 / 안정 최대화.

## Purpose

- stable solved state
- dominant configuration
- positive feedback exploit
- production runaway

---

# P-SIM-003 — Stress Inducer

## Policy

극단 State 의도 생성.

예:
- resource depletion
- overpopulation
- blocked routes
- injury cluster
- full storage
- no path

## Purpose

- cascade
- recovery
- state stability
- invalid transition

---

# P-SIM-004 — Random Intervention

## Policy

Seeded non-optimal intervention.

## Purpose

- robustness
- unexpected combination
- hidden dependency
- recovery

---

# P-SIM-005 — Explorer

## Policy

저사용:
- system
- configuration
- entity
- recipe
- route
를 탐색.

## Purpose

- coverage
- dead state
- unused feature
- rare interaction

---

# P-SIM-006 — No-recovery Profile

## Policy

Repair / Recovery 행동 최소화.

## Purpose

- failure chain
- simulation collapse boundary
- natural recovery

---

# 14. AI Tester Interpretation Limits

Machine이 강한 영역:

```text
State
Transition
Rule
Dependency
Cascade
Distribution
Deadlock
Edge Case
Coverage
Feedback Loop
```

Machine이 직접 결론내리지 않는 영역:

- 세계가 살아 있는 것 같다.
- Character가 믿을 만하다.
- Simulation이 깊게 느껴진다.
- Emergent Outcome이 재미있다.
- 결과가 자연스럽다.
- 현실적으로 느껴진다.
- 관찰하는 재미가 있다.
- Detail이 의미 있다.

또한:

```text
Complex state distribution
≠
Deep simulation experience
```

```text
High emergence count
≠
Good emergence
```

---

# 15. Player Telemetry vs Simulation Log

매우 중요한 운영 규칙.

## Simulation Log

보여주는 것:

> **World가 무엇을 했는가**

예:
- Temperature 500 transitions
- 20 cascade chains
- 300 autonomous agent actions

---

## Player Telemetry

보여주는 것:

> **Player가 무엇을 보고 / 확인하고 / 개입했는가**

예:
- Temperature panel opened 3 times
- warning inspected
- intervention after alert
- pause used

---

## Human Test

보여주는 것:

> **Player가 무엇을 이해했다고 생각하는가**

예:
- “왜 죽었는가?”
- “어떤 System이 원인이었는가?”
- “무엇을 바꾸면 되는가?”

---

## Interpretation Rule

```text
Simulation State Changed
≠
Player Observed It
≠
Player Understood It
≠
Player Correctly Attributed Cause
```

이 네 층을 분리한다.

AI Tester의 direct internal `GameState` access를:
- Player Inspect
- Player Diagnosis
로 기록하지 않는다.

---

# 16. Human Validation Map

# H-SIM-001 — Mental Model

> **왜 이 결과가 발생했는지 설명할 수 있는가?**

---

# H-SIM-002 — Cause Recognition

> 어떤 State / Rule이 원인이라고 생각하는가?

실제 Rule과 비교한다.

---

# H-SIM-003 — Intervention Understanding

> 상황을 바꾸려면 무엇을 조작해야 하는지 알았는가?

---

# H-SIM-004 — Feedback Quality

> 개입 후 어떤 변화가 발생했는지 확인할 수 있었는가?

---

# H-SIM-005 — Model Trust

> 같은 조건이면 비슷한 원리로 결과가 나온다고 느끼는가?

---

# H-SIM-006 — Simulation Fantasy

> 자신이 기대한 세계 / 조직 / 시스템이 작동한다고 느끼는가?

---

# H-SIM-007 — Detail Value

> 어떤 Detail은 의미 있고 어떤 Detail은 불필요했는가?

---

# H-SIM-008 — Emergent Outcome

> 예상하지 못했지만 규칙상 납득 가능한 사건이 있었는가?

---

# H-SIM-009 — Alive / Dynamic Perception

> 세계가 자신의 개입 없이도 작동한다고 느껴졌는가?

Subtype-dependent.

---

# H-SIM-010 — Diagnostic Burden

> 문제를 해결하는 것보다 원인을 찾는 데 더 많은 노력이 들었는가?

---

# H-SIM-011 — Cascade Legibility

> 연쇄 실패가 어디서 시작됐는지 이해했는가?

---

# H-SIM-012 — Abstraction Acceptance

> 생략된 현실 요소 때문에 Simulation Fantasy가 깨졌는가?

---

# H-SIM-013 — Stable-state Experience

> 안정 상태가 성취감인가, 할 일이 없어진 상태인가?

---

# H-SIM-014 — Agent Specificity

Agent subtype에서:

> 서로 다른 Agent가 실제로 다른 존재처럼 행동한다고 느끼는가?

---

# 17. Scale Handoff Candidates

이번 단계에서는 Genre × Scale Core를 확정하지 않는다.

# SCALE_HANDOFF-SIM-001 — Entity × State Matrix

```text
Entity
× State
× Behavior
× Relationship
× Environment
```

이 QA 조합을 폭증시킨다.

RimWorld가 강한 경고 사례.

---

# SCALE_HANDOFF-SIM-002 — Cross-system Interaction Matrix

```text
System A
× System B
× System C
```

Rule 수보다 Combination Test가 빠르게 증가한다.

FTL은 적은 시스템으로도 높은 interaction value를 만들지만 QA 비용은 남는다.

---

# SCALE_HANDOFF-SIM-003 — Agent AI Cost

Autonomy가 증가할수록:

- AI
- pathfinding
- scheduling
- conflict resolution
- debugging
- fallback behavior

비용 증가.

---

# SCALE_HANDOFF-SIM-004 — Persistent State / Save Cost

많은 State가:

- Save
- Load
- Versioning
- Migration
- Replay
- Debug snapshot

비용을 증가시킨다.

---

# SCALE_HANDOFF-SIM-005 — Observability Tooling

Simulation은 다음 Tool ROI가 높다.

- state inspector
- timeline
- event log
- replay
- deterministic seed
- scenario injection
- dependency trace

Prototype부터 일부 필요할 수 있다.

---

# SCALE_HANDOFF-SIM-006 — Procedural Content Is Not Free Content

System이 Outcome을 생성해도:

- invalid state
- repetition
- balance
- edge case
- debug
- save compatibility

비용이 발생한다.

---

# SCALE_HANDOFF-SIM-007 — Simulation Detail × UI Cost

State가 늘면 표시해야 할:
- panel
- alert
- filter
- tooltip
- visualization
도 증가한다.

Simulation Scope와 UI Scope를 분리 계산하지 않는다.

---

# 18. Universal Reclassification Candidates

# UC-RECLASS-SIM-001 — Complexity Should Be Causal, not Merely Additive

Candidate Rule:

> 새로운 요소가 다른 State / Decision / Outcome과 연결되지 않는다면 Complexity 증가를 Depth 증가로 간주하지 않는다.

## Duplicate Risk

`UC-DESIGN-001 Consequence Density`와 강하게 중복.

## Decision

새 Universal 승격보다 `UC-DESIGN-001` 강화 후보.

---

# UC-RECLASS-SIM-002 — Player-visible Outcomes Need Diagnosable Causes

Strategy / Management / Narrative에도 확장 가능.

## Duplicate Risk

`UC-DESIGN-005 Actionable Information`.

## Decision

Universal 새 Core보다 UC-DESIGN-005 specialization 후보.

---

# UC-RECLASS-SIM-003 — Abstraction Should Preserve Experience-relevant Causality

Simulation 밖:
- Strategy map
- Management dashboard
- narrative state
에도 확장 가능.

현재 Simulation Evidence에 편중.

---

# UC-RECLASS-SIM-004 — Simple Rules Can Create Complex Outcomes through Interaction

Simulation에서 강한 원칙.

FTL이 매우 강한 Evidence.

하지만:
> complex outcome이 항상 좋은 player experience인가?
는 별개.

Universal 승격은 보류.

---

# 19. Evidence Gaps

# GAP-SIM-001 — Direct Simulation Design Postmortem Breadth

RimWorld / FTL 외에 동일 깊이의 Simulation-specific Developer Evidence가 부족.

---

# GAP-SIM-002 — Player Mental Model

필요:
- cause explanation
- expected rule
- actual rule
- misconception
- correction

---

# GAP-SIM-003 — Cause Attribution Telemetry

필요:
- failure cause
- player inspect
- diagnosis sequence
- intervention selection

---

# GAP-SIM-004 — Emergence Telemetry

필요:
- system-generated event
- scripted event
- state-conditioned outcome
- player surprise / recall

---

# GAP-SIM-005 — Dependency Structure

실제:
- dependency graph
- system interaction coverage
- isolated state
data 부족.

---

# GAP-SIM-006 — Agent Behavior Diversity

필요:
- trait / need
- behavior policy
- interaction
- actual outcome
관계.

---

# GAP-SIM-007 — Director vs Simulation Interaction

필요:
- director trigger
- current state
- selected event
- outcome
- perceived manipulation

---

# GAP-SIM-008 — Cascade Recovery

필요:
- cascade source
- propagation depth
- intervention point
- recovery success

---

# GAP-SIM-009 — Stable-state Behavior

필요:
- time to stability
- post-stability intervention
- boredom vs satisfaction

---

# GAP-SIM-010 — Edge-state Failure

필요:
- no path
- zero resource
- max entity
- all disabled
- full storage
- extreme environment

---

# GAP-SIM-011 — Realism vs Abstraction

Human data:
- fantasy break
- model trust
- detail value
- readability
가 부족.

---

# GAP-SIM-012 — Underperforming Simulation Controls

필요:
- over-simulation
- hidden cause
- broken autonomy
- director cheating perception
- runaway economy
- state explosion
실패 사례.

---

# GAP-SIM-013 — Production / Logistics Simulation

Factorio / factory-style causal flow Evidence 부족.

---

# GAP-SIM-014 — Social / Life Simulation

The Sims류:
- autonomy
- relationship
- needs
- mental model
Evidence 부족.

---

# GAP-SIM-015 — Physics / Vehicle / Sports Simulation

현재 Core를 이 영역에 직접 적용하기에는 부족.

---

# 20. Additional References Needed

Reference 수를 늘리기 위한 조사가 아니다.

Evidence Gap을 메우는 Target만 제안한다.

# P0 — Oxygen Not Included

## 강화 대상

- `GC-SIM-002 Causal Propagation`
- `GC-SIM-004 Diagnosis`
- `GC-SIM-007 Cascade`
- Feedback Loop

## Research

- gas
- liquid
- heat
- oxygen
- resource loop
- cascade
- recovery

## Direct Evidence Needed

- Developer postmortem
- simulation architecture talk
- debugging / telemetry
- player diagnosis findings

---

# P0 — Dwarf Fortress

## 강화 대상

- `GC-SIM-003 Emergence`
- `GC-SIM-005 Agent`
- Large state interaction
- information burden

## Counter Evidence

RimWorld의 selective simplification과 비교해:
> 극단적 depth / detail이 언제 실제 Product Value가 되는가?

---

# P0 — Factorio

## 강화 대상

- `GC-SIM-002`
- Production / Logistics
- bottleneck
- feedback
- automation / intervention

## Boundary

Management / Strategy의:
- Priority
- Plan
과 분리하여

> material / production state가 어떻게 propagate되는가

를 조사.

---

# P0 — The Sims

## 강화 대상

- `GC-SIM-005 Agent Difference`
- `GC-SIM-006 Autonomy`
- Social interaction
- Player mental model

## Research

- needs
- autonomy
- social state
- intervention
- player attribution

---

# P1 — Prison Architect

## 강화 대상

- Agent behavior
- schedule
- environment
- crowd / path
- policy

---

# P1 — Cities: Skylines

## 강화 대상

- Traffic / flow
- zoning
- demand
- aggregate vs agent simulation
- abstraction

---

# P1 — Workers & Resources: Soviet Republic

## 강화 대상

- Realism
- logistics
- causal detail
- complexity value
- diagnosis

---

# P1 — Timberborn

## 강화 대상

- environment
- water
- drought
- colony causal chain
- stable / crisis state

---

# P2 — Amazing Cultivation Simulator / Similar Dense Colony Case

## 강화 대상

- dense interaction
- onboarding
- emergence
- state explosion
- information burden

---

# 21. Promotion Table

| ID | Name | Decision | Status | Confidence |
|---|---|---|---|---|
| GC-SIM-001 | Selective Simulation Preserves Experience-relevant Causality | NEW | **PROVISIONAL CORE** | VERY HIGH |
| GC-SIM-002 | System States Propagate through Causal Dependencies | NEW / UC SPECIALIZATION | **PROVISIONAL CORE** | VERY HIGH |
| GC-SIM-003 | Emergence Requires Persistent Rule Interaction | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-SIM-004 | Major Outcomes Need Diagnosable Causes | UC SPECIALIZATION | KEEP AS CANDIDATE / POSSIBLE UC SUB-RULE | HIGH |
| GC-SIM-005 | Agent Differences Change Behavior / Interaction | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-SIM-006 | Autonomy Needs Observation / Intervention | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-SIM-007 | Stable / Runaway / Cascade Boundaries | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-SIM-008 | Director Modulates, Not Replaces Simulation | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-SIM-009 | Abstraction Preserves Causal Fidelity | NEW | MERGE CANDIDATE → GC-SIM-001 | HIGH |

---

# 22. Simulation Reviewer Default Set

신규 Simulation 기획을 검토할 때 우선 사용할 15개 질문.

## Q1 — Simulation Purpose

> **이 게임은 정확히 무엇의 어떤 Cause / Effect를 Simulation하는가?**

---

## Q2 — Detail Value

> **왜 이 State를 모델링해야 하는가? 제거하면 어떤 Player-visible 결과가 사라지는가?**

관련:
`GC-SIM-001`

---

## Q3 — Selective Simulation

> **Player Fantasy와 무관한 현실 Detail을 장르 관습 때문에 넣고 있지 않은가?**

관련:
`GC-SIM-001`

---

## Q4 — Causal Dependency

> **이 State는 무엇 때문에 변하고, 무엇을 다시 변화시키는가?**

관련:
`GC-SIM-002`

---

## Q5 — Cross-system Interaction

> **System들이 실제로 서로 영향을 주는가, 독립 Meter가 병렬로 존재하는가?**

관련:
`GC-SIM-002`

---

## Q6 — Persistence

> **Simulation 결과가 다음 State에 남아 후속 Rule에 영향을 주는가?**

---

## Q7 — Emergence

> **Outcome 다양성이 Random Event 수가 아니라 Persistent State / Rule Interaction에서 발생하는가?**

관련:
`GC-SIM-003`

---

## Q8 — Diagnosis

> **중요한 결과의 주요 Cause Chain을 Player가 추적할 수 있는가?**

관련:
`GC-SIM-004`

---

## Q9 — Agent Specificity

> **Trait / Need / Relationship 차이가 실제 Behavior와 Interaction을 바꾸는가?**

Agent subtype에서만 적용.

관련:
`GC-SIM-005`

---

## Q10 — Autonomy / Intervention

> **World가 스스로 움직이는 부분과 Player가 개입하는 부분의 경계가 Product Promise와 맞는가?**

관련:
`GC-SIM-006`

---

## Q11 — Cascade

> **작은 State 변화가 연쇄될 때 시작 Cause와 Intervention Point를 확인할 수 있는가?**

관련:
`GC-SIM-007`

---

## Q12 — Stable / Runaway

> **안정 / 폭주 상태는 어떤 조건에서 시작되고 Product Promise에서 보상인가, 붕괴인가?**

관련:
`GC-SIM-007`

---

## Q13 — Abstraction

> **생략된 현실 Detail이 아니라 보존된 Causal Relationship을 기준으로 Simulation Fidelity를 평가했는가?**

관련:
`GC-SIM-001 / 009`

---

## Q14 — Machine vs Player

> **Simulation State Log와 Player Observation / Diagnosis Telemetry를 분리했는가?**

---

## Q15 — Scope

> **Entity × State × Behavior × System 조합을 현재 개발 / QA 규모가 감당할 수 있는가?**

Scale Handoff.

---

# 23. Default Metric Bundle

Metric은 Criteria가 아니다.

Threshold는 프로젝트별 Validation Planner가 확정한다.

## Structural / Machine

- State Count
- State Transition Definition Count
- Dependency Edge Count
- Impossible State Count
- Invalid Transition Count
- Deadlock Count
- Agent Count
- Trigger Count
- System Rule Coverage
- Explicit Dependency Coverage

---

## Structural / model-dependent

- Causal Chain Depth
- Cascade Depth
- Isolated System Rate
- Meaningful Interaction Count
- Runaway State Entry
- Stable State Entry
- Feedback Strength
- Emergent Event Count
- Intervention Success
- Simulation Collapse
- Trait → Behavior Shift
- Unexplained Transition
- Contradictory State Count
- Cross-system Interaction Count
- Failure Chain Source
- Director Override Count

Project-specific Formal Definition 없이 일반 Machine Metric으로 자동 사용하지 않는다.

---

## Simulation

- State Distribution
- State Transition Count
- State Duration
- Cause → Effect Transition Rate
- Cross-system Transition Rate
- Recovery after Cascade
- Autonomous Transition Rate
- Player-triggered Transition Rate
- Agent Behavior Distribution
- Agent Idle Rate
- Event Distribution
- State-conditioned Event Rate
- Edge-case Outcome Distribution
- Secondary Failure Count
- Automated Resolution Rate

## Simulation / model-dependent

- State Combination Coverage
- Multi-system Event Rate
- Cascade Frequency
- Cascade Size
- Time to Stability
- Stability Duration

### Interpretation Rule

`Cascade`, `Stable State`, `Multi-system Event`처럼 의미 경계가 프로젝트마다 달라질 수 있는 항목은 Formal Definition 없이 일반 Simulation Metric으로 사용하지 않는다.

예를 들어:

```text
A → B → C
```

와

```text
A → B
A → C
```

중 어느 구조를 하나의 `Cascade`로 계산할지는 프로젝트별 정의가 필요하다.

---

## Instrumented Player Telemetry

- State Panel View
- Inspect Rate
- Diagnostic Screen Usage
- Intervention Frequency
- Intervention Timing
- Alert Response
- Pause / Speed Change
- Manual Override
- State Lookup
- Reload after Cascade
- Time to Diagnose

### Interpretation Rule

AI Tester의 direct internal State access는 위 Player Telemetry에 포함하지 않는다.

---

## Instrumented / Simulation

다음이 **명시적 Game Action / Interaction**일 경우에만 AI Simulation과 Player Telemetry 양쪽에서 비교 가능하다.

- Scan
- Inspect
- Diagnose
- Probe
- Test
- Configure
- Re-route

측정:
- usage
- timing
- state before
- state after
- follow-up action

`AI reads hidden GameState`는 Inspect로 취급하지 않는다.

---

## Human

- Mental Model Accuracy
- Cause Recognition
- Intervention Understanding
- Feedback Quality
- Model Trust
- Simulation Fantasy
- Detail Value
- Emergent Outcome Recognition
- Alive-world Perception
- Diagnostic Burden
- Cascade Legibility
- Abstraction Acceptance
- Stable-state Experience
- Agent Specificity Recognition

---

## Hybrid

- Simulation Depth
- Emergence Quality
- Causal Legibility
- Model Legibility
- Agent Believability
- Cascade Fairness
- Stable-state Quality
- Abstraction Quality
- Realism Value
- System Interaction Quality
- Director Fairness
- Autonomy Quality

---

# 24. Self-Review Result

## Check 1 — More State ≠ Simulation Depth
**PASS**

State Count를 Core 승격 근거로 사용하지 않았다.

## Check 2 — Realistic Detail ≠ Good Simulation
**PASS**

`GC-SIM-001`에서 Experience-relevant Causality를 기준으로 삼았다.

## Check 3 — Management duplication
**PASS**

Priority / allocation이 아니라 World State dependency에 집중했다.

## Check 4 — Random Event ≠ Emergence
**PASS**

`GC-SIM-003`, `AP-SIM-004`에서 직접 분리했다.

## Check 5 — RimWorld overgeneralization
**PASS WITH GAPS**

Storyteller / Agent Specificity는 Candidate로 유지하고 Vehicle / Sports / Physics Evidence Gap을 명시했다.

## Check 6 — Agent Count ≠ Agent Complexity
**PASS**

Behavior / Interaction Shift를 별도 Candidate로 두었다.

## Check 7 — Cross-system Interaction
**PASS**

`GC-SIM-002`의 핵심 Rule이다.

## Check 8 — Causal Chain Human Legibility
**PASS**

Formal transition과 Human Mental Model을 분리했다.

## Check 9 — AI Log vs Player Telemetry
**PASS**

별도 운영 규칙으로 명시했다.

## Check 10 — Model-dependent Metric
**PASS**

Formal Definition 없는 의미 판단을 일반 Machine Metric으로 두지 않았다.

## Check 11 — Abstraction
**PASS**

Simulation 부족으로 자동 감점하지 않고 `GC-SIM-001 / 009`에서 Causal Fidelity로 처리했다.

## Check 12 — Stable State
**PASS**

Sandbox / relaxation에서 보상이 될 수 있는 Boundary를 유지했다.

## Check 13 — Director vs Simulation
**PASS**

`GC-SIM-008` Candidate와 Anti-pattern으로 분리했다.

## Check 14 — Genre Rule vs Scope Cost
**PASS**

Entity / State / AI / save / tooling은 Scale Handoff로 이동했다.

## Check 15 — Evidence Boundary
**PASS**

현재 Evidence가 Colony / Systemic / Network / Abstract 중심임을 명시했다.

---

# 25. Final Position

현재 Studio OS Simulation / Systemic Simulation Knowledge Base에서 우선 `Provisional Genre Core`로 사용할 항목은 **2개**다.

1. `GC-SIM-001 — Selective Simulation Should Preserve Experience-Relevant Causality`
2. `GC-SIM-002 — System States Should Propagate through Causal Dependencies`

Candidate는 다음과 같다.

- `GC-SIM-003 — Emergence Requires Persistent Rule Interaction`
- `GC-SIM-004 — Major Outcomes Need Diagnosable Causes`
- `GC-SIM-005 — Agent Differences Should Change Behavior / Interaction`
- `GC-SIM-006 — Autonomous Systems Need Meaningful Observation / Intervention`
- `GC-SIM-007 — Stable / Runaway / Cascade States Need Explicit Boundaries`
- `GC-SIM-008 — Event Directors Should Modulate, not Replace, Simulation`
- `GC-SIM-009 — Abstraction Can Preserve Simulation through Causal Fidelity`

`GC-SIM-009`는 현재 독립 Core보다:

> `GC-SIM-001 Selective Simulation`

의 Sub-rule로 병합될 가능성이 높다.

이번 Extraction의 가장 중요한 정리점은:

> **Simulation Depth는 얼마나 많은 것을 모델링했는가가 아니라, 의도한 Experience에 필요한 State를 선택하고 그 State들이 일관된 Rule을 통해 서로 어떤 Causal Outcome을 만드는가로 평가한다.**

또한:

> **Emergence를 Random Event 수로 측정하지 않는다.**

RimWorld가 보여주는 가장 중요한 Warning은:
- Event 자체가 아니라
- Character / persistent state / system interaction
이 Event를 하나의 World History로 바꾼다는 점이다.

FTL은 다른 방식으로 같은 문제를 보여준다.
- 적은 System
- 강한 dependency
를 통해 Fire / Oxygen / Crew / Damage가 예상치 못한 위기 조합을 만든다.

그리고 Studio OS 운영에서는 다음을 고정한다.

```text
Simulation Log
→ World behavior evidence

Player Telemetry
→ Observation / interaction evidence

Human Validation
→ Mental model / fantasy evidence
```

서로 대체하지 않는다.

현재 가장 중요한 Evidence Gap은:

> **Oxygen Not Included형 Cascade / Factorio형 Production Flow / The Sims형 Agent Autonomy / Dwarf Fortress형 Large-scale Emergence / Player Mental Model**

이다.

따라서 다음 Reference 확장은 유명 Simulation 게임을 더 모으는 방식보다:

> **Cause Chain을 Player가 실제로 어디까지 이해하는가?  
> State 하나의 변화가 몇 System까지 propagate되는가?  
> Random Event 없이도 Emergent Outcome이 발생하는가?  
> Stable / Runaway / Cascade State는 어디서 시작되고 어떻게 회복되는가?  
> Agent Trait가 실제 행동 분포를 바꾸는가?**

에 Direct Developer Evidence / Telemetry가 있는 사례를 우선 조사하는 편이 효율적이다.

---

# 26. Source Trace

## Primary Simulation Evidence
- REF-13 — RimWorld
- REF-02 — FTL: Faster Than Light

## Strong Simulation / Hybrid Support
- REF-14 — Mini Metro
- REF-15 — This War of Mine
- REF-22 — Stacklands
- REF-19 — Cultist Simulator
- REF-07 — Against the Storm

## Adjacent / Control
- REF-01 — Papers, Please
- REF-18 — Loop Hero
- REF-09 — Reigns
- REF-16 — Invisible, Inc.
- REF-24 — Dorfromantik
- REF-23 — Citizen Sleeper
- REF-03 — Into the Breach

## Baseline / Deduplication
- STUDIO_CORE_CANDIDATES_v0.2
- MANAGEMENT_CORE_CANDIDATES_v0.1
- NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1
- STRATEGY_CORE_CANDIDATES_v0.1
- Studio OS — Simulation / Systemic Simulation Genre Core Deep Extraction Prompt v0.1

---

# 27. Traceability Rule

Core는 원본 Reference를 대체하지 않는다.

Simulation 위험 신호가 발견되면:

```text
Simulation Core
↓
Primary Reference
↓
Modeled State
↓
Rule
↓
Interaction
↓
Causal Chain
↓
Player Observation / Intervention
↓
Boundary / Trade-off
↓
Current Project
```

순서로 다시 내려가 검토한다.

`SIMULATION_CORE_CANDIDATES_v0.1`은 Studio OS Reviewer가 State 수, Entity 수, Realism Detail 같은 표면적 복잡도가 아니라 **Selective Modeling, Causal Dependency, Persistent Interaction, Diagnosis**를 중심으로 신규 Simulation 기획을 평가하기 위한 압축된 Genre 판단 계층이다.
