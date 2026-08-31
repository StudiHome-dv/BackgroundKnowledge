# STRATEGY_CORE_CANDIDATES_v0.1

**Studio OS — Strategy Genre Core Deep Extraction**  
**Document:** `STRATEGY_CORE_CANDIDATES_v0.1`  
**Status:** `APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE`  
**Purpose:** 신규 Turn-based Strategy / Tactical Strategy / Systemic Strategy / Stealth Tactics / Network Strategy / Spatial Strategy / Strategy Roguelike / Strategy Hybrid 기획 평가용 Genre-specific Reviewer Knowledge Base  
**Baseline:** `STUDIO_CORE_CANDIDATES_v0.2`  
**Extraction Prompt:** `Studio OS — Strategy Genre Core Deep Extraction Prompt v0.1`  
**Provisional Genre Cores:** `GC-STRAT-001`, `GC-STRAT-002`, `GC-STRAT-003`  
**Candidates:** `GC-STRAT-004 ~ GC-STRAT-011`  
**Evidence Boundary:** `Tactical / Systemic / Small-state 중심. RTS / 4X / Grand Strategy / Multiplayer는 Additional Evidence 전까지 제한 적용.`  
**Pending:** `Additional Evidence / Prototype Validation / Internal Evidence`  
**Evidence Rule:** 현재 Reference Pool의 강점이 Tactical / Systemic / Stealth / Network / Small-state Strategy에 편중되어 있으므로 RTS / 4X / Grand Strategy / Multiplayer 전체로 자동 일반화하지 않는다.

---

# 1. Executive Summary

이번 Deep Extraction의 핵심 결론은 다음과 같다.

1. **Strategy의 핵심은 행동 수가 아니라 `현재 행동이 Future State와 Future Option Value를 어떻게 바꾸는가`다.**
   - 가능한 행동이 50개여도 45개가 명백히 열등하면 깊은 Strategy가 아니다.
   - 행동 수가 4개뿐이어도 현재 이득, 미래 위치, Resource, Objective, Risk를 서로 다르게 바꾸면 전략적 판단이 성립할 수 있다.

2. Strategy 전용 Core를 만들기 전에 기존 Universal Core와 중복을 강하게 제거해야 한다.
   - `UC-DESIGN-001 — Consequence Density over Input Count`
   - `UC-DESIGN-003 — Consequence-to-Next-Decision Coupling`
   - `UC-DESIGN-004 — Uncertainty Requires Response Agency`
   - `UC-DESIGN-005 — Actionable Information`

   Strategy Core는 이 규칙을 복제하지 않고:
   - Planning Horizon
   - Future Option Value
   - Plan Revision
   - Objective-conditioned Value
   로 특수화한다.

3. 현재 Primary Strategy Evidence는 다음 3개로 정리하는 것이 타당하다.
   - `REF-03 Into the Breach` — Perfect-information Tactical Strategy
   - `REF-02 FTL` — Systemic / Uncertainty Strategy
   - `REF-16 Invisible, Inc.` — Turn-based Stealth / Escalation Strategy

4. `Mini Metro`, `Against the Storm`, `Dorfromantik`는 강한 보조 사례다.
   - Mini Metro: Network reconfiguration / current bottleneck vs future demand.
   - Against the Storm: variable inputs / adaptive planning.
   - Dorfromantik: spatial commitment / future option value / low-stress opportunity cost.
   그러나 다른 Genre Core와의 중복 또는 Source focus 때문에 Tier B로 유지한다.

5. 신규 Provisional Strategy Core는 **3개**로 제한한다.
   - `GC-STRAT-001 — Key Strategic Decisions Should Change Future Option Value`
   - `GC-STRAT-002 — Decision-Relevant State Changes Must Trigger Re-evaluation`
   - `GC-STRAT-003 — Objectives Must Change Action Value`

6. 다음은 매우 중요하지만 현재 Subtype 편향 또는 Evidence 부족 때문에 Candidate로 유지한다.
   - `GC-STRAT-004 — Information Must Support Prediction / Commitment`
   - `GC-STRAT-005 — Position Should Change Future Action Value`
   - `GC-STRAT-006 — Escalation Should Change State, not only Count Down`
   - `GC-STRAT-007 — Recovery Window after Error`
   - `GC-STRAT-008 — Counterplay Should Add Cost, not Hard-ban Strategy`
   - `GC-STRAT-009 — Reserve / Flexibility as Strategic Hedge`
   - `GC-STRAT-010 — Late-game Solved State`
   - `GC-STRAT-011 — Strategic Compression`

7. 특히 `Information`은 중요한 Strategy 축이지만 독립 Genre Core로 과도 승격하지 않는다.
   - Into the Breach는 Perfect Information.
   - FTL / Invisible, Inc.는 Partial / Hidden / Future Uncertainty.
   - 공통점은 정보량이 아니라:
     > **현재 보이는 정보가 계획과 행동을 실제로 바꾸는가**
     다.
   - 이는 `UC-DESIGN-005`의 Strategy specialization으로 유지한다.

8. `Position` 역시 전체 Strategy Universal로 승격하지 않는다.
   - Into the Breach / Invisible, Inc. / Dorfromantik에는 매우 강함.
   - FTL / Macro Strategy에는 다른 형태로 나타남.
   따라서 Spatial/Tactical Candidate로 제한한다.

9. Strategy의 반복 Anti-Pattern은 다음과 같다.
   - More Actions = More Depth
   - One Best Opening
   - Perfect Information without Trade-off
   - Hidden Information without Response
   - Position without Consequence
   - Numeric Difficulty Only
   - Objective = Kill Everything
   - Dominant Upgrade
   - Local Optimum Solves Global Game
   - No Recovery Window
   - Information Overload as Difficulty
   - Complexity without Interaction
   - Counter as Hard Ban
   - Escalation without Replanning
   - Late-game Solved State

10. AI Tester와 매우 궁합이 좋은 장르다.
    - Action distribution
    - Strategy convergence
    - Opening convergence
    - Route / Position
    - Objective performance
    - Scenario divergence
    - Plan revision
    - Recovery
    를 반복 Simulation으로 검증할 수 있다.

11. 그러나 Machine이 직접 결론내리지 않는 것은:
    - 계획이 만족스러운가
    - 전략가가 된 느낌인가
    - 실수가 공정한가
    - Decision Tension이 있는가
    - 승리가 영리하게 느껴지는가

12. Strategy Reviewer의 가장 중요한 질문은:

> **“지금 가장 좋아 보이는 행동과, 미래 선택지를 보존하는 행동이 실제로 충돌하는가?”**

그리고:

> **“새 State가 생겼을 때 계획을 바꿀 이유가 있는가?”**

13. 현재 Evidence Gap 중 가장 큰 것은:
    - RTS / 4X / Grand Strategy Primary Evidence
    - Multiplayer Counterplay
    - Human Planning Horizon
    - Strategy Switching Telemetry
    - Recovery Window
    - Error Propagation
    - Position Value Formalization
    - Dominant Opening
    - Late-game Solved State
    - Underperforming Strategy Control Cases

---

# 2. Strategy Genre Definition

Studio OS에서 Strategy를:

> 많은 선택지가 있는 게임

으로 정의하지 않는다.

기본 정의는 다음이다.

> **현재 State와 미래 Consequence를 읽고, 제한된 Action / Resource / Position / Time을 배분하여 여러 가능한 미래 중 하나를 의도적으로 만들어가는 게임 구조.**

## 2.1 Core Strategic Loop

```text
Observe State
↓
Form Goal / Priority
↓
Predict Consequence
↓
Commit Action / Resource / Position
↓
Opponent / System Responds
↓
State Changes
↓
Re-evaluate Plan
```

---

# 2.2 Strategy Inclusion Test

## A. Multiple Viable Actions

현재 State에서 합리적인 행동 후보가 둘 이상 존재하는가?

단순히 버튼 수가 많은지를 보지 않는다.

---

## B. Consequence Difference

선택에 따라 Future State가 실제로 달라지는가?

---

## C. Planning

현재 행동 가치가:
- 즉시 결과
뿐 아니라
- 다음 Turn
- Encounter
- Route
- Campaign

의 Future State와 연결되는가?

---

## D. Trade-off

하나를 얻으면 다른:
- Position
- Resource
- Time
- Target
- Objective
- Future Option

을 포기하는가?

---

## E. State-dependent Value

같은 Action이 Context에 따라 가치가 달라지는가?

---

## F. Adaptation

새:
- Enemy response
- Demand
- Alarm
- Damage
- Resource state
때문에 Plan을 수정하는가?

---

## G. Failure Attribution

실패 후:

> 어떤 판단 또는 계획을 바꿨어야 했는가?

를 분석할 수 있는가?

---

# 3. Evidence Scope / Limitation

현재 Studio Reference Library에서 Strategy Evidence는 균등하지 않다.

## Strong Coverage

- Turn-based Tactics
- Perfect-information Tactics
- Systemic Strategy
- Stealth Strategy
- Network Strategy
- Spatial Placement
- Strategy Roguelike
- Small-state Strategy

## Weak Coverage

- RTS
- 4X
- Grand Strategy
- Multiplayer Competitive Strategy
- Diplomacy-heavy Strategy
- Large-scale Warfare
- Economy-heavy Macro Strategy

따라서 본 문서의 Provisional Core는:

> 현재 Tactical / Systemic / Small-state Evidence에서 반복되는 Mechanism

까지만 강하게 적용한다.

RTS / 4X / Grand Strategy에 적용할 때는 `EVIDENCE GAP` 상태를 유지한다.

---

# 4. Source Classification

# 4.1 Tier A — Primary Strategy Evidence

## REF-03 — Into the Breach

**Subtype:** `Turn-based Tactical / Perfect-information Strategy`  
**Evidence Strength:** VERY HIGH

### Strong Evidence Areas

- Perfect Information
- Prediction
- Position Manipulation
- Objective Protection
- Small State Space
- Decision Density
- Multi-purpose Action
- Consequence Clarity
- Partial Failure / Damage Minimization

### Key Observations

- 정보를 많이 공개해도 Strategy가 사라지지 않는다.
- Enemy Intent가 공개되면 판단이:
  - “무슨 일이 일어날까?”
  보다
  - “어떤 미래를 만들 것인가?”
  로 이동한다.
- Kill보다 Objective Protection을 중심에 두면 같은 Ability의 가치가 달라진다.
- Position manipulation이:
  - damage
  - block
  - collision
  - protection
  - future position
  을 동시에 변화시킨다.
- 작은 Board / 적은 Unit도 높은 Consequence Density를 만들 수 있다.

### Critical Boundary

Perfect Information을 그대로 복제하면 전투가 Puzzle-like optimization으로 바뀔 수 있다.

즉:
- prediction / calculation fantasy
에는 강하지만
- chaos / improvisation fantasy
에는 부적합할 수 있다.

---

## REF-02 — FTL: Faster Than Light

**Subtype:** `Systemic / Roguelike Strategy`  
**Evidence Strength:** VERY HIGH

### Strong Evidence Areas

- System Interaction
- Resource Allocation
- Route Planning
- Reserve
- Crew Assignment
- Adaptation
- Persistent Damage
- Uncertainty Response
- Long-horizon preparation

### Key Observations

- 현재 Scrap을 수리에 쓸지 Upgrade에 쓸지 결정하는 것처럼 즉시 이득과 미래 준비가 충돌한다.
- 현재 적과 함선 상태에 따라:
  - 전력
  - Crew
  - Weapon
  - Repair
  Priority가 바뀐다.
- RNG는:
  - 준비
  - 경로
  - 비축
  - 복구
  수단이 있을 때 전략 자원이 된다.
- 특정 적/시스템/자원 State가 현재 Upgrade의 미래 가치를 바꾼다.

### Boundary

Roguelike Reset / Meta는 Strategy Core로 복제하지 않는다.

---

## REF-16 — Invisible, Inc.

**Subtype:** `Turn-based Stealth Strategy`  
**Evidence Strength:** HIGH

### Strong Evidence Areas

- Information
- Alarm
- Escalation
- Position
- Stealth Recovery
- Time Pressure
- Risk
- Replanning
- Objective / Escape

### Key Observations

- 턴제로 시야와 행동 결과를 명확하게 보여준다.
- Alarm은 단순 Timer가 아니라 시간이 지나면:
  - 적 대응
  - Threat State
  를 변화시킨다.
- 무한 Wait / 완벽 탐색이라는 지배 전략을 Escalation으로 억제한다.
- 발각이 즉시 실패가 아니기 때문에:
  - 계획 실패
  - 복구
  - 탈출
  의 전략 공간이 남는다.

### Tier Decision

Secondary Reference Library 소속이지만:
- Direct Design Lesson
- Core Loop
- Failure / Recovery
- Alarm Mechanism
이 충분히 구체적이므로 이번 Strategy Extraction에서는 `Tier A Specialized Primary`로 사용한다.

---

# 4.2 Tier B — Strong Strategy / Hybrid Evidence

## REF-14 — Mini Metro

**Subtype:** `Network / Flow Strategy`

### Use

- Current Bottleneck vs Future Demand
- Network Reconfiguration
- Limited Upgrade
- Route / Capacity
- Readable Abstraction
- Short-term disruption vs long-term efficiency

### Evidence Weight

Design structure는 강하지만 Reference의 Primary lesson이 Scope/Postmortem 비중이 크므로 Tier B 유지.

---

## REF-07 — Against the Storm

**Subtype:** `Management / Strategy Hybrid`

### Use

- Variable Inputs
- Adaptation
- Strategic Commitment
- Future Pressure
- Tool / Resource constraint

### Boundary

Management의:
- Priority Conflict
- Economy
- workforce
Core를 Strategy에 중복하지 않는다.

Strategy 관점에서는:

> Current State 변화로 Plan이 실제 바뀌는가?

만 사용한다.

---

## REF-24 — Dorfromantik

**Subtype:** `Spatial Placement / Puzzle Strategy`

### Use

- Irreversible / costly placement
- Spatial Opportunity Cost
- Future Option Value
- Low-pressure Strategy
- Local gain vs future board shape

### Key Observation

한 번 놓은 타일이 미래 선택 공간을 바꾸며, 강한 처벌 없이도 Opportunity Cost로 장기 판단을 만든다.

### Evidence Weight

Secondary design evidence로 강하지만 Spatial subtype 한정이라 Tier B 유지.

---

# 4.3 Tier C — Adjacent / Control

## REF-21 — Mark of the Ninja

Use:
- Information readability
- planning → execution
- failure attribution

Action / Stealth execution 비중이 높아 Strategy Core 단독 승격 근거로 사용하지 않는다.

---

## REF-18 — Loop Hero

Use:
- indirect control
- player-authored risk
- placement
- strategic timing

Roguelike overlap 주의.

---

## REF-28 — Thronefall

Production 중심.

Use:
- minimal strategy scope
- prototype
- simplified control

Design Core 승격 Evidence로 사용하지 않는다.

---

# 5. Universal / Existing Core Audit

현재 Strategy 전용 `GC-STRAT-*` baseline은 확정되어 있지 않다.

따라서 신규 Core 생성 전에 Universal과 중복을 검사한다.

---

## UC-DESIGN-001 — Consequence Density over Input Count

### Strategy Specialization

복제하지 않는다.

Strategy에서는:

> **행동 수가 아니라 한 Action이 Future State / Position / Resource / Objective에 어떤 서로 다른 결과를 만드는가**

로 사용한다.

Into the Breach가 가장 강한 Evidence.

---

## UC-DESIGN-003 — Consequence-to-Next-Decision Coupling

### Strategy Specialization

Strategy에서는:

> 현재 Action 결과가 다음 Turn / Encounter의 Option Value와 Plan을 바꾸는가?

로 사용한다.

이는 `GC-STRAT-001`의 상위 원리다.

---

## UC-DESIGN-004 — Uncertainty Requires Response Agency

### Strategy Specialization

별도 Core로 복제하지 않는다.

Strategy에서는:
- Scout
- Reserve
- Flexible Position
- Reroute
- Retreat
- Backup Plan

같은 Planning Verb로 구체화한다.

FTL / Invisible, Inc.가 강한 사례.

---

## UC-DESIGN-005 — Actionable Information

### Strategy Specialization

별도 Core로 복제하지 않는다.

Strategy에서는:

> Information Check 이후 Plan / Target / Position / Resource가 실제 바뀌는가?

로 사용한다.

---

## Management overlap

다음은 Strategy Core로 복제하지 않는다.

- Priority Conflict
- Resource Economy
- Capacity Management

Strategy에서는:
- Position
- Target
- Tempo
- Objective
- Future Option
과 연결되는 경우만 다룬다.

---

## Roguelike overlap

다음은 복제하지 않는다.

- Reset
- Run Variation
- Meta
- Run Restart

Strategy에서는:
> 현재 Scenario / State에 대응해 Plan을 바꾸는 부분
만 사용한다.

---

# 6. Provisional Strategy Cores

# GC-STRAT-001 — Key Strategic Decisions Should Change Future Option Value

**Status:** `PROVISIONAL CORE`  
**Origin:** `UC-DESIGN-003 SPECIALIZATION`

## Pattern

전략의 핵심 의사결정 중 일부는 현재 점수 / 피해 / 보상만 바꾸는 것이 아니라 다음 State에서 가능한 선택의 가치나 범위를 변화시킨다.

## Strategy Context

- Tactical Strategy
- Systemic Strategy
- Network Strategy
- Spatial Strategy
- Strategy Hybrid

## Rule

> **Strategy의 핵심 의사결정 중 일부는 현재 결과뿐 아니라 Future Option Value를 변화시켜야 한다. 매 Turn 즉시 최고 효율 행동을 고르는 것만으로 전체 게임이 해결된다면 Long-horizon Strategy가 약할 수 있다.**

## Mechanism

Weak Strategy:

```text
Turn N
→ 가장 큰 Damage
→ Turn N+1
→ 다시 가장 큰 Damage
```

Strong strategic dependency:

```text
Action
→ Current Gain
+
Position / Resource / Route / Objective State 변화
↓
Future Options 가치 변화
↓
다음 계획 변화
```

## Primary Evidence

### Into the Breach

한 공격이:
- 피해
- 밀기
- 건물 보호
- 충돌
- 다음 위치
를 동시에 바꾼다.

현재 최대 Damage보다:
> 다음 Enemy Intent와 Objective를 어떻게 바꿀지
가 중요하다.

### FTL

Scrap을:
- Repair
- Weapon
- Shield
- System
중 어디에 쓰는지가 이후 Threat 대응 범위를 바꾼다.

현재 적을 이기는 것뿐 아니라 Future Sector의 약점을 만든다.

### Invisible, Inc.

현재:
- 더 탐색
- 목표 확보
- 탈출
중 선택이 Alarm / Position / Future Safety를 바꾼다.

## Secondary Evidence

### Mini Metro

현재 병목을 임시 해결하는 선택과 미래 확장에 유연한 network 구조가 충돌한다.

### Dorfromantik

현재 완벽 연결과 미래 Placement Option을 보존하는 배치가 충돌할 수 있다.

## Counter Evidence

- Pure Tactical Puzzle
- very short encounters
에서는 현재 Turn optimality 자체가 Product Promise일 수 있다.

## Boundary

모든 Action을 irreversible하게 만들 필요는 없다.

핵심은:

> 일부 핵심 Action이 다음 판단 조건을 실제로 변화시킨다.

는 것이다.

## Observed Metric

공통 Source telemetry 없음.

## Candidate Metric — Structural / Simulation

- State Transition after Action
- Action → Future Option Count
- Action → Future Option Value Shift
- Setup Action Rate
- Reserve Action Rate
- Position Preservation
- Long-horizon Action Usage

`Future Option Value`는 project-specific formal model 필요.

## Candidate Metric — Human

- Future Thinking
- “현재 이득보다 미래 때문에 선택을 바꿨다” 설명
- Plan Formation

## Validation Type

Structural / model-dependent + Simulation + Human.

## AI Tester Applicability

HIGH.

## Confidence

**VERY HIGH**

## Reviewer Action

각 핵심 Action마다 묻는다.

> **“이 행동은 지금 무엇을 얻고, 다음에 무엇을 가능/불가능하게 만드는가?”**

후자가 없다면 `LOCAL_OPTIMUM_RISK`.

---

# GC-STRAT-002 — Decision-Relevant State Changes Must Trigger Re-evaluation

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE / UC-DESIGN-002 + UC-DESIGN-003 SPECIALIZATION`

## Pattern

전략 게임에서 State 변화가 많아도 Player Policy가 변하지 않으면 실질적인 Adaptation은 없다.

강한 사례는:
- enemy intent
- damage
- alarm
- demand
- resource
- route
가 변할 때 Target / Position / Allocation / Timing을 바꾸게 한다.

## Rule

> **Decision-relevant Opponent / System State가 변하면 기존 Plan / Target / Position / Resource Policy의 가치도 다시 평가되어야 한다. 항상 Plan Revision이 발생할 필요는 없지만, 중요한 State가 크게 달라져도 같은 Policy가 항상 최적이라면 Strategy Variation을 과대평가하고 있을 수 있다.**

## Mechanism

Fake Adaptation:

```text
Enemy type changes
↓
same opening
same target priority
same resource use
```

Meaningful Re-evaluation:

```text
Decision-relevant State change
↓
existing plan value is re-evaluated
↓
new threat / opportunity identified
↓
plan is maintained or target / position / resource priority shifts
```

## Primary Evidence

### FTL

적:
- Shield
- Weapon
- Crew
- System
과 내 함선 상태가 달라질 때 전력 / 공격 목표 / Crew priority가 바뀐다.

### Invisible, Inc.

경보가 상승하고 경비 / Threat State가 변하면:
- 추가 탐색
- 위험 감수
- 탈출
Plan이 바뀐다.

### Into the Breach

Enemy Intent가 공개되고 매 Turn Board State가 달라져:
- 공격 대상
- 희생
- displacement
- objective protection
계획을 다시 계산한다.

## Secondary Evidence

### Mini Metro

새 역 / 수요 / bottleneck이 생기면 기존 노선을 재구성해야 한다.

### Against the Storm

새 자원 / 건물 / 주민 조건이 기존 정착 계획을 수정하게 한다.

## Counter Evidence

Long-horizon strategy에서:
- 미리 세운 강한 plan을 끝까지 실행하는 만족감
자체가 가치일 수 있다.

하지만 그런 경우에도:
> plan이 왜 강한지, 어떤 state에서 취약한지
는 존재해야 한다.

## Candidate Metric — Simulation

- Strategy Change Rate
- Target Priority Shift
- Position Policy Shift
- Resource Reallocation
- Route Change
- Plan Revision Rate
- Same Policy / Different Scenario Similarity

## Candidate Metric — Instrumented

- Strategy Switching
- Undo / Reload after State Change
- Information View → Plan Change

## Candidate Metric — Human

- Adaptation Recognition
- “계획을 바꾼 순간과 이유”
- Strategy Identity

## Validation Type

Simulation + Instrumented + Human.

## AI Tester Applicability

VERY HIGH.

## Confidence

**VERY HIGH**

## Reviewer Action

Scenario variation이 있다면:

> **“State가 달라졌을 때 무엇을 다르게 해야 하는가?”**

에 구체적 답이 있는지 확인한다.

---

# GC-STRAT-003 — Objectives Must Change Action Value

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

같은 Unit / Ability / Map도 Objective가 다르면 합리적인 Action Value가 달라질 수 있다.

전략적 목표는:
- Kill
- Protect
- Escape
- Hold
- Route
- Optimize Flow
- Survive
중 어떤 것을 우선하는지 결정한다.

## Rule

> **Objective를 별도 Mission Label로만 두지 말고, Objective가 Target / Position / Resource / Tempo / Sacrifice 판단을 실제로 바꾸는지 평가한다. 다양한 Objective를 제공해도 항상 Enemy Elimination이 최적이면 Objective Diversity는 약하다.**

## Mechanism

Weak:

```text
Mission: Protect
↓
but best strategy = kill all enemies
```

Meaningful:

```text
Objective changes
↓
Damage / Position / Tempo value changes
↓
different action priority
```

## Primary Evidence

### Into the Breach

가장 강한 Evidence.

게임의 Player Fantasy는:
> 가장 많이 죽이는 지휘관
보다
> 예고된 재난을 최소 피해로 해결하는 위기 관리자

에 가깝다.

Objective Protection이:
- displacement
- block
- sacrifice
- damage
의 우선순위를 바꾼다.

### Invisible, Inc.

목표는:
- 모든 경비 제거
가 아니라
- 정보 / 자원 확보 후 탈출

이다.

따라서:
- 우회
- 기절
- 추가 탐색
- 탈출 Timing
가 Kill과 다른 전략 가치를 가진다.

### FTL

각 전투는 적 제거가 중요하지만 전체 전략 목표는:
- 현재 전투 최대 성과
보다
- 함선/자원 보존 후 장기 생존

까지 포함한다.

Current kill efficiency보다 Hull / Fuel / Missile / Crew 보존이 Future Strategy에 영향을 준다.

## Secondary Evidence

### Mini Metro

Objective가 enemy kill이 아니라 throughput / congestion control이므로 network modification이 핵심 Action이 된다.

## Counter Evidence

전투 자체의 제거 효율이 Product Promise인 Strategy도 존재한다.

예:
- extermination tactics
- score attack

이 경우 Kill Everything이 문제가 아니다.

## Candidate Metric — Simulation

- Objective-specific Strategy Shift
- Objective-preserving Action Rate
- Kill Count vs Objective Outcome
- Sacrifice Rate
- Partial Success Rate
- Optional Objective Completion
- Universal Strategy Survival across Objectives

## Candidate Metric — Human

- Objective Meaning
- “목표 때문에 평소와 다른 전략을 썼는가?”
- Strategic Goal Clarity

## AI Tester Applicability

VERY HIGH.

## Confidence

**HIGH**

## Reviewer Action

Mission Type이 여러 개라면:

> **“Objective가 바뀌었을 때 같은 Unit / Action의 가치 순위가 어떻게 달라지는가?”**

를 비교한다.

---

# 7. Strategy Core Candidates

# GC-STRAT-004 — Information Must Support Prediction / Commitment

**Status:** `CANDIDATE`  
**Origin:** `UC-DESIGN-005 SPECIALIZATION`

## Rule Candidate

> **Strategy Information은 State를 많이 보여주는 것이 아니라 Prediction / Target / Position / Commitment를 바꾸는 정보여야 한다.**

## Evidence

### Into the Breach
Enemy Intent 공개가 실제 Action planning에 직접 사용된다.

### Invisible, Inc.
Guard vision / tile risk를 명확히 보여 숨은 규칙보다 판단으로 난이도를 이동시킨다.

### FTL
현재 Ship / Enemy state는 많이 공개하지만 future route/event는 일부 불확실하다.

## Why Candidate

상위 `UC-DESIGN-005`와 중복이 강하다.

독립 Strategy Core보다 Reviewer Sub-rule로 사용할 가능성이 높다.

## Candidate Metrics

- Information Check → Action Change
- Intent-based Action Change
- Scout Usage
- Forecast Usage
- Information Ignored Rate

## Confidence

**HIGH as specialization / LOW need for independent GC**

---

# GC-STRAT-005 — Position Should Change Future Action Value

**Status:** `CANDIDATE`

## Rule Candidate

> **Spatial / Tactical Strategy에서 Position은 단순 이동 거리보다 Future Attack / Defense / Route / Blocking / Objective Value를 변화시키는 State여야 한다.**

## Primary Evidence

### Into the Breach
Position manipulation은 Core Mechanic.

### Invisible, Inc.
Agent position / vision / route가 risk와 escape possibility를 바꾼다.

## Secondary Evidence

### Dorfromantik
Tile placement가 future placement space를 바꾼다.

### Mini Metro
노선 구조가 future demand absorption을 바꾼다.

## Boundary

Non-spatial Strategy에는 직접 적용하지 않는다.

## Candidate Metrics

- Position Distribution
- Movement Frequency
- Blocking Usage
- Displacement Usage
- Terrain Interaction
- Position → Future Action Change

`Positional Value`는 formal definition 필요.

## Confidence

**HIGH for Spatial/Tactical subtype**

---

# GC-STRAT-006 — Escalation Should Change State, not only Count Down

**Status:** `CANDIDATE`

## Rule Candidate

> **Timer / Alarm / Threat Escalation을 사용할 경우 단순 숫자 감소보다 시간이 지날수록 Threat State와 합리적인 Plan이 실제로 변화해야 한다.**

## Primary Evidence

### Invisible, Inc.
가장 강함.

Alarm은 무한 Wait / exploration을 억제하고 실제 Enemy response를 변화시킨다.

## Secondary Evidence

### Mini Metro
시간 증가 → demand / station growth → network state 변화.

### FTL
sector progression → enemy response requirement 증가.

## Why Candidate

Invisible, Inc. 의존도가 높고:
- score timer
- turn limit
- survival timer
등 Subtype 차이가 큼.

## Candidate Metrics

- Threat State by Time
- Plan Revision after Escalation
- Alarm Level at Completion
- Delay Action Rate
- Strategy Shift by Escalation Stage

## Confidence

**MEDIUM-HIGH**

---

# GC-STRAT-007 — Error Should Leave a Recovery Decision before Defeat

**Status:** `CANDIDATE`

## Rule Candidate

> **전략 판단 실수가 발생했을 때 즉시 deterministic defeat로 이어지기보다, 일부 Subtype에서는 sacrifice / retreat / reposition / emergency resource를 사용해 손실을 관리할 Recovery Window가 전략 공간을 확장할 수 있다.**

## Evidence

### Invisible, Inc.
발각이 즉시 실패가 아니며:
- recover
- abandon loot
- escape
Decision을 만든다.

### FTL
Damage / fire / crew loss 후:
- repair
- power redistribution
- retreat-like resource preservation
등 대응이 존재.

### Into the Breach
Objective 일부 Damage를 감수하고 완전 패배를 피하는 partial failure 판단.

## Counter Evidence

Puzzle-like perfect play Strategy에서는:
- one error → fail
이 의도될 수 있다.

## Candidate Metrics

- Recovery Opportunity Usage
- Recovery Success
- Error → Defeat Latency
- Sacrifice Rate
- Partial Failure Rate
- Emergency Resource Spend

## Human

- Recovery Perception
- Error Fairness

## Confidence

**MEDIUM-HIGH**

---

# GC-STRAT-008 — Counterplay Should Add Costs, not Only Hard-ban Strategies

**Status:** `CANDIDATE`

## Rule Candidate

> **상대 / Environment의 Counter가 특정 Strategy를 무조건 금지하기보다 Cost / Position / Timing / Resource를 바꾸어 Adaptation을 요구하는지 검토한다.**

## Evidence

FTL:
특정 Enemy defense가 Weapon / System priority를 바꾸지만 하나의 strategy를 항상 영구 금지하지는 않는다.

Into the Breach:
Enemy Intent / position이 현재 action priority를 바꾼다.

## Promotion Blocker

Multiplayer / adaptive opponent evidence 부족.

## Candidate Metrics

- Counter Strategy Usage
- Strategy Success by Opponent Type
- Hard-ban Matchup Rate
- Strategy Switching after Counter

## Confidence

**MEDIUM**

---

# GC-STRAT-009 — Reserve / Flexibility Can Be Strategic Value

**Status:** `CANDIDATE`

## Rule Candidate

> **Uncertainty가 있는 Strategy에서는 Resource를 즉시 모두 쓰지 않고 Reserve / Flexible Position / unused option을 남기는 것이 Future Risk 대응 가치가 될 수 있다.**

## Evidence

FTL:
- Scrap
- fuel
- missiles
- repair
의 미래 대비.

Invisible, Inc.:
- Power
- movement / escape position
- time
의 여유.

Mini Metro:
현재 bottleneck에 모든 upgrade를 소진할지 future expansion에 남길지.

## Duplicate Risk

`UC-DESIGN-004`와 매우 강하게 겹친다.

## Confidence

**MEDIUM-HIGH as sub-rule**

---

# GC-STRAT-010 — Late-game Solved State Should Be Bounded

**Status:** `CANDIDATE`

## Rule Candidate

> **전략적 우위가 사실상 확정된 뒤 결과 정리만 남는 구간이 길어지는지 검토한다.**

## Supporting Evidence

Mini Metro Reference는 후반 반복을 Weakness로 기록.

Against the Storm / Roguelike Core에서도 late-loop decision collapse 위험이 존재.

## Promotion Blocker

Strategy-specific direct telemetry 부족.

## Candidate Metrics

- Outcome Certainty
- Last Plan Revision
- Late Strategy Change Rate
- Cleanup Duration
- Late-game Decision Entropy

## Human

- “이미 이긴/진 상태를 정리했다” 인식

## Confidence

**MEDIUM**

---

# GC-STRAT-011 — Strategic Compression Should Preserve Decision-relevant State

**Status:** `CANDIDATE`

## Rule Candidate

> **복잡한 세계를 단순화할 때 Simulation detail보다 Player decision에 필요한 State를 보존하는지 평가한다.**

## Evidence

Into the Breach:
small board / clear intent.

Mini Metro:
노선도 수준 abstraction.

FTL:
ship cutaway로:
- crew
- oxygen
- system
- damage
를 한 화면에 압축.

Invisible, Inc.:
grid / sight / alarm abstraction.

## Duplicate Risk

`UC-DESIGN-005 Actionable Information`과 Scope Core에 일부 중복.

## Candidate Metric

- Decision-relevant State Coverage
- Inspection Count
- Information-to-Action Change
- State Lookup Burden

## Human

- Strategic Readability
- Information Burden

## Confidence

**MEDIUM-HIGH**

---

# 8. Strategy Anti-Patterns

# AP-STRAT-001 — More Actions = More Depth

## Trigger
Action / Unit / Ability 수만 증가.

## Mechanism
대부분 명백히 열등하면 Search Space만 커진다.

## Consequence
- cognitive load
- balance cost
- false complexity

## Evidence
Into the Breach:
작은 Board와 적은 Unit에서도 높은 consequence density 가능.

## Detection
- Action Usage Concentration
- Low-use Action Rate
- Context-specific Action Shift
- Universal Action Rate

## Mitigation
새 Action마다:
> 어떤 Context에서 기존 Action보다 가치가 높고 낮은가?
를 정의.

---

# AP-STRAT-002 — One Best Opening

## Trigger
Scenario / opponent와 무관하게 동일 Opening 반복.

## Consequence
초반 Plan Formation 소멸.

## Detection
- Opening Strategy Distribution
- Dominant Opening Rate
- Same Opening Success across scenarios

## Mitigation
시작:
- objective
- information
- terrain
- resource
- threat
중 일부가 opening value를 바꾸게 한다.

---

# AP-STRAT-003 — Perfect Information without Trade-off

## Trigger
모든 정보 공개.

하지만 합리적 행동은 사실상 하나.

## Consequence
정보 공개를 전략 깊이로 과대평가.

## Evidence
Into the Breach는 반대 사례:
완전 정보 + multiple consequence trade-off.

## Detection
- viable action count
- action concentration
- alternate solution count

## Mitigation
정보 숨김보다 consequence trade-off 먼저 검토.

---

# AP-STRAT-004 — Hidden Information without Response

## Trigger
위협 정보는 숨겨지지만:
- scout
- hedge
- reserve
- retreat
없음.

## Consequence
Strategy → Guess.

## Evidence
FTL / Invisible, Inc.가 반대 사례.

## Detection
- Hidden Threat Failure
- Scout Usage
- Recovery Usage
- Uncontrollable Failure

## Mitigation
response channel 제공.

---

# AP-STRAT-005 — Position without Consequence

## Trigger
Map은 있지만 위치가:
- range
- blocking
- defense
- route
- objective
에 거의 영향 없음.

## Consequence
Spatial UI가 cosmetic.

## Detection
- Position → Outcome / Action shift
- Movement concentration
- terrain usage

## Mitigation
Future action value와 연결.

---

# AP-STRAT-006 — Numeric Difficulty Only

## Trigger
Enemy HP / Damage / speed만 증가.

## Consequence
새 판단보다 error margin 축소.

## Detection
- Difficulty → Strategy Shift
- New Constraint Count
- Universal Strategy Survival

## Mitigation
Subtype에 맞는:
- objective
- enemy behavior
- information
- resource
- tempo
변화 검토.

---

# AP-STRAT-007 — Objective = Kill Everything

## Trigger
Mission 이름은 다르나 Kill이 항상 best strategy.

## Consequence
Objective variation은 cosmetic.

## Evidence
Into the Breach / Invisible, Inc.가 반대 사례.

## Detection
- Objective-specific Strategy Shift
- Kill Count vs objective result
- non-kill action usage

## Mitigation
Objective success rule가 action value를 바꾸게 한다.

---

# AP-STRAT-008 — Dominant Upgrade

## Trigger
Context와 무관한 universal best upgrade.

## Consequence
장기 planning 수렴.

## Detection
- Upgrade selection concentration
- Conditional success by state
- universal first-upgrade rate

## Mitigation
현재 weakness / future plan과 trade-off.

---

# AP-STRAT-009 — Local Optimum Solves Global Game

## Trigger
매 Turn 가장 큰 즉시 value를 선택하면 장기적으로도 항상 최적.

## Consequence
Planning horizon 축소.

## Detection
Greedy Persona vs Long-horizon Persona outcome 비교.

## Mitigation
- setup
- reserve
- position
- resource timing
- objective
로 future option value 생성.

---

# AP-STRAT-010 — No Recovery Window

## Trigger
한 실수 → deterministic defeat.

## Consequence
strategy보다 perfect execution / puzzle restart 중심.

## Boundary
Puzzle Tactics에서는 의도 가능.

## Detection
- Error → Defeat Latency
- Recovery Opportunity
- Partial Failure

## Mitigation
sacrifice / retreat / reposition / emergency spend.

---

# AP-STRAT-011 — Information Overload as Difficulty

## Trigger
판단 자체보다 state lookup가 어려움.

## Consequence
cognitive burden ≠ strategic depth.

## Evidence
FTL은 ship cutaway로 복잡 state를 압축.
Invisible, Inc.는 sight / risk를 명시.

## Detection
- information inspect rate
- decision time
- error caused by missed UI state
- human information burden

## Mitigation
Strategic Compression / hierarchy.

---

# AP-STRAT-012 — Complexity without Interaction

## Trigger
Unit / Resource / Stat이 많지만 서로 독립.

## Consequence
기능 수 증가, decision coupling 없음.

## Evidence
FTL의 반대 사례:
단순 system interaction이 상황 다양성을 만듦.

## Detection
- cross-system state dependency
- action consequence dimensions
- isolated system rate

## Mitigation
새 system보다 existing interaction 우선.

---

# AP-STRAT-013 — Counter as Hard Ban

## Trigger
Opponent X → Strategy A unusable.

## Consequence
adaptation이 아니라 forced answer.

## Detection
- matchup win collapse
- strategy availability
- counter response diversity

## Mitigation
hard prohibition보다 cost / timing / risk pressure.

---

# AP-STRAT-014 — Escalation without Replanning

## Trigger
Timer / alarm 증가하지만 plan은 동일.

## Consequence
시간 압박은 숫자 stress만 생성.

## Evidence
Invisible, Inc. Warning:
Alarm 숫자만 추가한다고 긴장이 생기지 않는다.

## Detection
- escalation stage → action shift
- plan revision
- target shift

## Mitigation
escalation이 actual state / threat response를 바꾸게 한다.

---

# AP-STRAT-015 — Late-game Solved State

## Trigger
승패가 사실상 확정되었지만 긴 cleanup 지속.

## Consequence
Decision Density 급락.

## Detection
- outcome certainty
- last plan revision
- cleanup duration

## Mitigation
- accelerate conclusion
- surrender
- end-state
- new constraint
중 Product Promise에 맞는 방식 검토.

---

# 9. Conflicting Findings

# CF-STRAT-001 — Perfect vs Hidden Information

## Perfect

Into the Breach:
- calculation
- prediction
- puzzle mastery

## Partial / Hidden

FTL / Invisible, Inc.:
- adaptation
- scout
- reserve
- risk management

## Hidden Variable

`Prediction Fantasy vs Adaptation Fantasy`

## Resolution
정보 공개량을 Depth Score로 만들지 않는다.

---

# CF-STRAT-002 — Small State Space vs Large Strategic Space

작은 Board도 깊을 수 있다.

Into the Breach:
small state + dense consequence.

Mini Metro:
minimal representation + network interaction.

## Resolution
State Count가 아니라 interaction / trade-off를 본다.

---

# CF-STRAT-003 — Tactical Precision vs Strategic Uncertainty

Into the Breach:
정밀한 visible state optimization.

FTL:
future uncertainty + reserve / adaptation.

둘 모두 Strategy이나 Player Fantasy가 다르다.

---

# CF-STRAT-004 — Reversible vs Irreversible Choice

Dorfromantik:
placement commitment가 future option을 만든다.

Mini Metro:
network 수정은 가능하지만 disruption cost가 있다.

## Resolution
Irreversibility 자체를 깊이로 평가하지 않는다.

중요한 것은:
> reversal cost가 planning에 의미를 만드는가?

---

# CF-STRAT-005 — Kill vs Objective-based Play

Kill all이 나쁜 것이 아니다.

Into the Breach / Invisible, Inc.는:
다른 objective가 action value를 바꾼다는 Evidence.

Product Promise가 elimination이면 Kill objective 정상.

---

# CF-STRAT-006 — Direct vs Indirect Control

Into the Breach:
direct unit action.

Loop Hero / Network hybrid:
indirect placement / configuration.

Hidden Variable:
Player Responsibility Fantasy.

---

# CF-STRAT-007 — Deterministic vs Probabilistic Outcome

Determinism:
prediction / precision.

Probability:
risk management / hedge.

Probability 자체가 Strategy Depth를 만들지 않는다.

---

# CF-STRAT-008 — Long Planning Horizon vs Rapid Replanning

FTL:
run / sector preparation.

Into the Breach:
turn-to-turn recalculation.

Invisible, Inc.:
mission plan + escalating replanning.

## Resolution
길게 계획하는 것이 무조건 더 strategic한 것은 아니다.

핵심은:
> Product Promise에 맞는 horizon에서 current action과 future state가 연결되는가?

---

# 10. Structural / Simulation Validation Map

# 10.1 Action Metrics

| Metric | Type |
|---|---|
| Action Usage Rate | Structural / Simulation |
| Action Concentration | Simulation |
| Universal Action Rate | Simulation / model-dependent |
| Context-specific Action Shift | Simulation |
| Action Entropy | Simulation |

**Guardrail:** 높은 Entropy ≠ 좋은 Strategy.

---

# 10.2 Strategy Metrics

| Metric | Type |
|---|---|
| Strategy Concentration | Simulation |
| Strategy Success Distribution | Simulation |
| Opening Strategy Distribution | Simulation |
| Dominant Opening Rate | Model-dependent |
| Strategy Change Rate | Simulation |
| Strategy Convergence | Simulation |

---

# 10.3 Planning Metrics

| Metric | Type |
|---|---|
| Immediate Gain vs Future Value Choice | Model-dependent |
| Resource Reserve Rate | Simulation |
| Position Preservation | Model-dependent |
| Setup Action Rate | Model-dependent |
| Plan Revision Rate | Simulation / Instrumented |
| Future Option Value | Structural / model-dependent |

---

# 10.4 Spatial Metrics

| Metric | Type |
|---|---|
| Position Distribution | Simulation / Instrumented |
| Movement Frequency | Simulation / Instrumented |
| Zone Control | Structural / model-dependent |
| Blocking Usage | Simulation |
| Displacement Usage | Simulation |
| Terrain Interaction | Simulation |
| Positional Value | Structural / model-dependent |

---

# 10.5 Objective Metrics

| Metric | Type |
|---|---|
| Objective Damage / Loss | Structural / Simulation |
| Kill Count | Simulation |
| Objective-preserving Action Rate | Model-dependent |
| Optional Objective Completion | Simulation |
| Sacrifice Rate | Simulation |
| Partial Success Rate | Simulation |
| Objective-specific Strategy Shift | Simulation |

---

# 10.6 Information Metrics

| Metric | Type |
|---|---|
| Information Check → Action Change | Instrumented / Simulation — only when information access is explicitly modeled |
| Scout Usage | Simulation / Instrumented |
| Intent-based Action Change | Simulation |
| Hidden Threat Failure | Model-dependent |
| Forecast Usage | Simulation / Instrumented |
| Information View / Inspect Rate | Instrumented Player Telemetry |

### Information Access Interpretation Rule

AI Tester가 내부 `GameState`를 직접 읽는 것은 Player의 정보 획득 행동이 아니다.

Simulation에서 정보 사용을 측정하려면:
- Scout
- Scan
- Inspect
- Forecast
- Recon

처럼 정보 획득이 게임 규칙 안의 명시적 Action / Cost / State Transition으로 모델링되어 있어야 한다.

---

# 10.7 Uncertainty Metrics

| Metric | Type |
|---|---|
| Same Persona × Different Scenario Divergence | Simulation |
| Different Persona × Same Scenario Divergence | Simulation |
| Reserve Usage | Simulation |
| Recovery Usage | Simulation |
| Hedge Action Rate | Model-dependent |
| Risk Exposure | Structural / model-dependent |

---

# 10.8 Tempo Metrics

| Metric | Type |
|---|---|
| Turns / Time to Objective | Simulation / Instrumented |
| Alarm Level at Completion | Simulation / Instrumented |
| Escalation State | Structural |
| Delay Action Rate | Simulation |
| Initiative Loss | Model-dependent |
| Threat Accumulation | Structural / Simulation |

---

# 10.9 Failure Metrics

| Metric | Type |
|---|---|
| Failure Cause Distribution | Hybrid / model-dependent |
| First Unrecoverable State | Structural / model-dependent |
| Recovery Opportunity Usage | Simulation |
| Error Propagation Depth | Structural / model-dependent |
| Partial Failure Rate | Simulation |

---

# 10.10 Dominance Metrics

| Metric | Type |
|---|---|
| Universal Best Action | Structural / model-dependent |
| Universal Upgrade Rate | Simulation / model-dependent |
| Universal Route | Simulation / model-dependent |
| Strategy Win Concentration | Simulation |
| Counter Strategy Usage | Simulation |

---

# 11. Strategy Tester Persona Map

Persona는 게임 Rule을 바꾸지 않고 Choice Policy만 바꾼다.

## P-STRAT-001 — Greedy / Immediate Value

### Policy
- immediate damage
- current score
- current resource gain
최대화.

### Purpose
`AP-STRAT-009 Local Optimum` 검출.

---

## P-STRAT-002 — Long-horizon Planner

### Policy
- Future Option
- Reserve
- Position
- future threat
가중치 높음.

### Purpose
Long-horizon strategy가 실제 value를 갖는지 비교.

---

## P-STRAT-003 — Conservative

### Policy
- loss minimization
- variance minimization
- reserve
- recovery margin

### Purpose
survival / defensive viability.

---

## P-STRAT-004 — Aggressive

### Policy
- tempo
- damage
- objective pressure
- early commitment

### Purpose
aggression dominance / tempo check.

---

## P-STRAT-005 — Flexible / Adaptive

### Policy
Context 변화에 따라:
- target
- resource
- position
- route
weight를 적극 변경.

### Purpose
Adaptation value 측정.

---

## P-STRAT-006 — Explorer

### Policy
저사용:
- action
- route
- upgrade
- position
을 우선 시도.

### Purpose
coverage / dead option / hidden strategy 검출.

---

# 11.1 Persona Comparison

## Same Persona × Different Scenario

검토:
- scenario sensitivity
- state-dependent strategy
- environment influence

## Different Persona × Same Scenario

검토:
- strategy viability
- policy divergence
- dominant solution

### Interpretation Limit

Persona divergence가 크다고 해서 Human Strategy Diversity가 좋다는 뜻은 아니다.

---

# 12. Human Validation Map

# H-STRAT-001 — Plan Formation

> 행동 전에 실제 계획을 세웠는가?

---

# H-STRAT-002 — Future Thinking

> 현재 이득보다 미래 State 때문에 선택을 바꾼 적이 있는가?

---

# H-STRAT-003 — Failure Attribution

> 왜 실패했는지 어떤 판단 단위로 설명할 수 있는가?

---

# H-STRAT-004 — Information Sufficiency

> 판단에 필요한 정보가 충분했는가?

---

# H-STRAT-005 — Information Burden

> 전략보다 UI / State 확인이 더 어려웠는가?

---

# H-STRAT-006 — Adaptation

> 처음 계획을 바꾼 순간과 이유를 설명할 수 있는가?

---

# H-STRAT-007 — Positional Meaning

> 위치 때문에 Action Value가 달라졌다고 느꼈는가?

---

# H-STRAT-008 — Objective Meaning

> Objective 때문에 평소와 다른 전략을 사용했는가?

---

# H-STRAT-009 — Recovery

> 실수 후 만회할 방법을 인식했는가?

---

# H-STRAT-010 — Strategy Identity

> 자신의 전략을 한 문장으로 설명할 수 있는가?

---

# H-STRAT-011 — Dominant Solution

> 결국 항상 같은 Opening / Upgrade / Action으로 돌아갔는가?

---

# H-STRAT-012 — Decision Tension

> 둘 이상의 합리적인 선택 사이에서 고민했는가?

Human-only.

---

# H-STRAT-013 — Planning Satisfaction

> 계획이 실제 결과로 이어졌을 때 만족감을 느꼈는가?

Human-only.

---

# H-STRAT-014 — Error Fairness

> 실수와 결과 사이의 인과를 납득할 수 있었는가?

---

# 13. Structural / Model-dependent Metric Rule

다음은 Formal Definition 없이 일반 Machine Metric으로 쓰지 않는다.

- Meaningful Action Rate
- Strategic Choice Rate
- Positional Value
- First Critical Mistake
- First Unrecoverable State
- Future Option Value
- Dominant Strategy
- Dominant Opening
- Recovery Window
- Error Propagation Severity
- Universal Best Action
- Objective-preserving Action
- Risk Exposure

프로젝트별 Formal Definition이 있으면:

`Structural / model-dependent`

로 사용한다.

체감 품질은:
- Human
- Hybrid
로 처리한다.

특히:

```text
Turn 4 행동 A
→ Turn 8 패배
```

라는 사실만으로 행동 A를 `First Critical Mistake`로 판정하지 않는다.

Counterfactual 또는 명시적 Error Definition이 필요하다.

---

# 14. Scale Handoff Candidates

이번 단계에서는 Genre × Scale Core를 확정하지 않는다.

# SCALE_HANDOFF-STRAT-001 — Interaction QA Matrix

```text
Unit
× Ability
× Terrain
× Enemy
× Objective
× Difficulty
```

조합이 QA / balance를 폭증시킨다.

---

# SCALE_HANDOFF-STRAT-002 — Opponent AI Cost

Opponent AI가:
- deterministic
- readable
- probabilistic
- adaptive
중 무엇인지에 따라:
- behavior logic
- debugging
- test scenario
비용이 크게 달라진다.

---

# SCALE_HANDOFF-STRAT-003 — Map / Pathfinding Scope

Map Size 증가가:
- art
- pathfinding
- AI
- camera
- save
- test
비용에 연결된다.

Strategy Depth와 Map Size를 동일시하지 않는다.

---

# SCALE_HANDOFF-STRAT-004 — Scenario × Objective QA

Objective 종류가 늘면 같은 map / unit에서도:
- trigger
- win condition
- fail condition
- AI
- balance
가 달라질 수 있다.

---

# SCALE_HANDOFF-STRAT-005 — Multiplayer Balance Multiplier

현재 Direct Evidence 부족.

Multiplayer에서는:
- matchup
- exploit
- latency
- ranking
- meta
- patch
비용을 별도 Scale Core에서 조사해야 한다.

---

# SCALE_HANDOFF-STRAT-006 — Simulation / Replay Tooling ROI

Strategy는 AI Tester와 잘 맞기 때문에:
- deterministic seed
- replay
- state dump
- scenario injection
- policy runner

Tooling의 ROI가 높을 수 있다.

현재 제작비 정량 Evidence는 부족하므로 Handoff Candidate.

---

# 15. Universal Reclassification Candidates

이번 단계에서 Universal Core로 직접 승격하지 않는다.

# UC-RECLASS-STRAT-001 — Future Option Value

Candidate Universal Rule:

> 현재 행동은 즉시 결과뿐 아니라 미래 선택 가능성의 변화로 평가할 수 있다.

Strategy 밖:
- Deckbuilding
- Management
- Roguelike
에도 적용 가능.

하지만 `UC-DESIGN-003`과 중복 가능성이 높다.

## Decision
새 Universal Core 생성보다 `UC-DESIGN-003` 정밀화 후보.

---

# UC-RECLASS-STRAT-002 — Objective Changes Action Value

Strategy 밖:
- Action
- Puzzle
- Survival
에도 적용 가능.

현재 Strategy Evidence에 편중.

---

# UC-RECLASS-STRAT-003 — Escalation Should Change State

Management / Narrative / Roguelike에도 적용 가능.

현재 `GC-MGMT-005 / 009`, `GC-ROGUE-005`와 중복 가능성 큼.

Universal 승격 금지.

---

# UC-RECLASS-STRAT-004 — Formal State Complexity ≠ Strategic Depth

다른 장르에서도 적용 가능.

Candidate principle:

> 많은 Unit / State / Action이 있어도 viable trade-off가 증가하지 않으면 Depth 증가로 보지 않는다.

`UC-DESIGN-001`과 합치 가능.

---

# 16. Evidence Gaps

# GAP-STRAT-001 — RTS Primary Evidence

필요:
- scouting
- build order
- economy / army
- real-time adaptation
- execution vs planning
- information warfare

---

# GAP-STRAT-002 — 4X / Grand Strategy

필요:
- tech commitment
- diplomacy
- territory
- snowball
- campaign recovery
- long-horizon planning

---

# GAP-STRAT-003 — Multiplayer Competitive Strategy

필요:
- counterplay
- matchup
- meta
- dominant opening
- adaptation
- hidden information against humans

---

# GAP-STRAT-004 — Human Planning Horizon

필요:
- 몇 Turn / 단계 앞을 보는가
- plan formation transcript
- local vs long-term reasoning

---

# GAP-STRAT-005 — Strategy Switching Telemetry

필요:
- strategy cluster
- switch timing
- switch trigger
- success after switch

---

# GAP-STRAT-006 — Recovery Window

필요:
- error occurrence
- recovery opportunity
- recovery usage
- recovery success
- human perceived recoverability

---

# GAP-STRAT-007 — Error Propagation

필요:
- minor error → future disadvantage
- deterministic loss transition
- snowball depth

---

# GAP-STRAT-008 — Position Value

필요:
- position → future action
- route
- objective
- defense
formal model.

---

# GAP-STRAT-009 — Counter Strategy

특히:
- soft counter
- hard counter
- adaptation cost
자료 부족.

---

# GAP-STRAT-010 — Dominant Opening

실제 Player / high-level telemetry 부족.

---

# GAP-STRAT-011 — Late-game Solved State

필요:
- outcome certainty
- surrender
- cleanup duration
- late plan change

---

# GAP-STRAT-012 — Underperforming Strategy Controls

필요:
- excessive action count
- one build order
- AI exploit
- information overload
- hard counter
- long cleanup
실패 사례.

---

# 17. Additional References Needed

아래는 Research Target이며 현재 Core Evidence가 아니다.

# P0 — XCOM 2

## 강화 대상
- `GC-STRAT-005 Position`
- `GC-STRAT-007 Recovery`
- Partial Information
- Campaign / Tactical Coupling

## Research Questions
- Fog / hit chance가 planning과 hedge를 어떻게 바꾸는가?
- Soldier loss가 tactical choice와 campaign planning을 어떻게 연결하는가?
- bad tactical outcome 이후 recoverability는?

---

# P0 — Fights in Tight Spaces

## 강화 대상
- small state space
- position
- future option
- tactical puzzle / strategy boundary

## Research Questions
- 작은 board에서 action / position interaction은 어떻게 density를 만드는가?
- deckbuilding과 tactical positioning 역할은 어떻게 나뉘는가?

---

# P0 — Age of Empires II / IV

## 강화 대상
- RTS evidence
- scouting
- build order
- adaptation
- hidden information

## Research Questions
- 정보 부족이 실제 build / army switch를 어떻게 만든다?
- execution과 strategy를 어떻게 분리 측정할 수 있는가?

---

# P0 — Civilization VI

## 강화 대상
- 4X
- long-horizon commitment
- territory
- tech
- diplomacy
- snowball

## Research Questions
- early commitment와 pivot의 관계?
- late-game solved state / snowball?

---

# P0 — Old World

## 강화 대상
- 4X Action Economy
- Orders
- Character / politics
- strategic prioritization

## Research Questions
- 제한 Orders가 macro scale에서 opportunity cost를 어떻게 만드는가?

---

# P1 — Bad North

## 강화 대상
- simplified tactical strategy
- readable threat
- spatial commitment

---

# P1 — Battle Brothers

## 강화 대상
- tactical / campaign coupling
- roster loss
- positioning
- risk / recovery

---

# P1 — Slipways

## 강화 대상
- network strategy
- spatial commitment
- low execution
- optimization

---

# P1 — Northgard

## 강화 대상
- RTS / economy hybrid
- territory
- resource pressure
- timing

---

# 18. Promotion Table

| ID | Name | Decision | Status | Confidence |
|---|---|---|---|---|
| GC-STRAT-001 | Key Strategic Decisions Change Future Option Value | NEW / UC SPECIALIZATION | **PROVISIONAL CORE** | VERY HIGH |
| GC-STRAT-002 | Decision-Relevant State Changes Trigger Re-evaluation | NEW | **PROVISIONAL CORE** | VERY HIGH |
| GC-STRAT-003 | Objectives Change Action Value | NEW | **PROVISIONAL CORE** | HIGH |
| GC-STRAT-004 | Information Supports Prediction / Commitment | UC SPECIALIZATION | KEEP AS CANDIDATE / POSSIBLE UC SUB-RULE | HIGH |
| GC-STRAT-005 | Position Changes Future Action Value | NEW | KEEP AS CANDIDATE | HIGH — Spatial/Tactical only |
| GC-STRAT-006 | Escalation Changes State | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-STRAT-007 | Recovery Decision after Error | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-STRAT-008 | Counterplay Adds Costs, not Hard Ban | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-STRAT-009 | Reserve / Flexibility as Hedge | UC SPECIALIZATION | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-STRAT-010 | Late-game Solved State | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-STRAT-011 | Strategic Compression | UC SPECIALIZATION | KEEP AS CANDIDATE | MEDIUM-HIGH |

---

# 19. Strategy Reviewer Default Set

신규 Strategy 기획을 검토할 때 우선 사용할 15개 질문.

## Q1 — Strategic Goal

> **플레이어는 실제로 무엇을 최적화하거나 보호하는가?**

---

## Q2 — Viable Choice

> **현재 State에서 합리적인 행동 후보가 둘 이상 존재하는가?**

---

## Q3 — Future Option Value

> **현재 행동이 다음 Turn / Encounter에서 가능한 선택이나 그 가치에 영향을 주는가?**

관련:
`GC-STRAT-001`

---

## Q4 — Local vs Long-term

> **즉시 최고 이득과 미래 Option을 보존하는 행동이 실제로 충돌하는가?**

관련:
`GC-STRAT-001`

---

## Q5 — State-dependent Value

> **같은 Action의 가치가 Enemy / Resource / Position / Objective 때문에 달라지는가?**

---

## Q6 — Plan Re-evaluation

> **Decision-relevant State가 나타났을 때 기존 Plan의 가치를 다시 평가할 이유가 있는가? 필요하다면 실제 Revision으로 이어지는가?**

관련:
`GC-STRAT-002`

---

## Q7 — Information

> **보여주는 Information이 Target / Position / Resource / Plan을 실제로 바꾸는가?**

관련:
`UC-DESIGN-005 / GC-STRAT-004`

---

## Q8 — Uncertainty Response

> **불확실성에 Scout / Reserve / Retreat / Hedge / Flexible Position 같은 대응 수단이 있는가?**

관련:
`UC-DESIGN-004`

---

## Q9 — Position / Route

> **Position / Route가 Future Action Value를 실제로 바꾸는가?**

관련:
`GC-STRAT-005`

---

## Q10 — Objective

> **Objective가 Action Value를 바꾸는가, 결국 항상 Kill / Max Output이 최적인가?**

관련:
`GC-STRAT-003`

---

## Q11 — Escalation

> **시간 / Alarm / Threat 상승이 실제 State와 Plan을 변화시키는가?**

관련:
`GC-STRAT-006`

---

## Q12 — Dominance

> **Opening / Upgrade / Route / Strategy가 Context와 무관하게 하나로 수렴하지 않는가?**

---

## Q13 — Recovery

> **실수 후 만회할 Decision Window가 있는가, 아니면 사실상 즉시 패배인가?**

관련:
`GC-STRAT-007`

---

## Q14 — Machine vs Human

> **수렴 / 분포 / 위치 / Objective / Recovery는 Simulation으로, Plan Quality / Tension / Fairness는 Human으로 분리했는가?**

---

## Q15 — Evidence Boundary

> **현재 판단을 Tactical/Systemic Evidence에서 RTS / 4X / Grand Strategy 전체로 과도하게 일반화하고 있지 않은가?**

---

# 20. Default Metric Bundle

Metric은 Criteria가 아니다.

Threshold는 Validation Planner가 프로젝트별로 확정한다.

## Structural / Machine

- Action Usage Rate
- State Transition Count
- Objective Completion
- Partial Objective Loss
- Escalation State
- Required State Dependency
- Resource Usage
- Resource Reserve
- Recovery Option Availability
- Threat / Alarm State
- Scenario Outcome

---

## Structural / model-dependent

- Universal Best Action
- Dominant Opening
- Positional Value
- Future Option Value
- First Unrecoverable State
- Error Propagation Depth
- Recovery Window
- Strategic State Divergence
- Objective-preserving Action Rate
- Risk Exposure
- Meaningful Action Rate
- Strategic Choice Rate

Project-specific Formal Definition 없이 자동 사용하지 않는다.

---

## Simulation

- Action Concentration
- Opening Strategy Distribution
- Strategy Distribution
- Strategy Success Distribution
- Strategy Change Rate
- Strategy Convergence
- Route Distribution
- Position Distribution
- Resource Reserve Rate
- Recovery Option Usage
- Turns / Time to Objective
- Threat / Alarm Progression
- Same Persona × Different Scenario Divergence
- Different Persona × Same Scenario Divergence
- Strategy Concentration
- Counter Strategy Usage
- Objective-specific Strategy Shift
- Difficulty → Strategy Shift
- Universal Strategy Survival
- Blocking Usage
- Displacement Usage
- Terrain Interaction
- Partial Success Rate
- Sacrifice Rate

---

## Instrumented / Simulation

- Action Distribution
- Information Check → Action Change `[only when information access is explicitly modeled]`
- Scout Usage
- Forecast Usage
- Plan Revision
- Strategy Switching
- Upgrade / Route Selection

---

## Instrumented Player Telemetry

- Information View / Inspect Rate
- Decision Time
- Undo / Reload
- Retry
- Objective Failure Behavior
- Failure → Continue / Restart Behavior
- Manual Plan Marker / Waypoint Usage if present

### Information Access Interpretation Rule

AI Tester의 direct `GameState` access를 Player Information Acquisition으로 계산하지 않는다.

`Information View / Inspect Rate`는 실제 Player UI Telemetry에만 기본 적용한다.

Simulation에서는 정보 획득 자체가 다음처럼 **명시적인 Game Action 또는 modeled interaction**일 경우에만 측정한다.

- Scout
- Scan
- Inspect
- Forecast
- Recon
- Sensor / Reveal action

따라서:

```text
AI Tester reads full domain state
≠
Player opened information UI
```

로 취급한다.

---

## Human

- Plan Formation
- Future Thinking
- Failure Attribution
- Information Sufficiency
- Information Burden
- Adaptation Recognition
- Positional Meaning
- Objective Meaning
- Recovery Perception
- Strategy Identity
- Decision Tension
- Strategic Satisfaction
- Error Fairness

---

## Hybrid

- Meaningful Strategy Diversity
- Dominant Strategy Severity
- Difficulty Quality
- Planning Horizon
- Recovery Quality
- Counterplay Quality
- Strategic Readability
- Late-game Solved State
- Strategic Decision Density
- Local-vs-Long-term Tension
- Strategic Compression Quality

---

# 21. Self-Review Result

## Check 1 — Turn-based ≠ Strategy Core
**PASS**

Turn structure 자체를 Core로 만들지 않았다.

## Check 2 — More Actions ≠ Depth
**PASS**

Anti-pattern으로 명시했다.

## Check 3 — Perfect Information ≠ Easy
**PASS**

Into the Breach를 Prediction / Puzzle Strategy의 Evidence로 사용했다.

## Check 4 — Hidden Information ≠ Depth
**PASS**

FTL / Invisible, Inc.에서 response agency와 함께 평가했다.

## Check 5 — Position actually matters
**PASS**

Spatial subtype Candidate로 제한했다.

## Check 6 — Management Core duplication
**PASS**

Resource / priority 자체가 아니라 future plan / objective / position과 연결되는 부분만 사용했다.

## Check 7 — Roguelike adaptation duplication
**PASS**

Reset / run meta를 복제하지 않았다.

## Check 8 — Into the Breach overgeneralization
**PASS**

Perfect-information puzzle tactics의 Boundary를 명시했다.

## Check 9 — Dominant Strategy = Pick Rate
**PASS**

Success / scenario / context와 함께 검토한다.

## Check 10 — AI win rate = fun
**PASS**

Machine과 Human을 분리했다.

## Check 11 — RTS / 4X Gap
**PASS**

명시적으로 Evidence Gap 유지.

## Check 12 — Local vs Long-term
**PASS**

`GC-STRAT-001`의 핵심 구조.

## Check 13 — Recovery / Error Propagation
**PASS**

Candidate / model-dependent metric으로 포함.

## Check 14 — Objective changes Action Value
**PASS**

`GC-STRAT-003`으로 직접 검증.

## Check 15 — Reviewer Usability
**PASS**

15개 질문으로 압축.

---

# 22. Final Position

현재 Studio OS Strategy Knowledge Base에서 우선 `Provisional Genre Core`로 사용할 항목은 **3개**다.

1. `GC-STRAT-001 — Key Strategic Decisions Should Change Future Option Value`
2. `GC-STRAT-002 — Decision-Relevant State Changes Must Trigger Re-evaluation`
3. `GC-STRAT-003 — Objectives Must Change Action Value`

Candidate는 다음과 같다.

- `GC-STRAT-004 — Information Supports Prediction / Commitment`
- `GC-STRAT-005 — Position Changes Future Action Value`
- `GC-STRAT-006 — Escalation Changes State`
- `GC-STRAT-007 — Recovery Decision after Error`
- `GC-STRAT-008 — Counterplay Adds Costs`
- `GC-STRAT-009 — Reserve / Flexibility as Hedge`
- `GC-STRAT-010 — Late-game Solved State`
- `GC-STRAT-011 — Strategic Compression`

이번 Extraction의 가장 중요한 문장은:

> **Strategy Depth는 행동 수가 아니라, 핵심 의사결정이 미래 State와 Future Option Value를 바꾸고 Decision-relevant State 변화가 기존 Plan의 가치를 다시 평가하게 만드는 정도로 평가한다.**

또한:

> **Perfect Information과 Hidden Information 중 어느 것이 더 전략적인지는 정답이 아니다.**

중요한 것은:
- 어떤 Fantasy를 약속하는가
- Information이 실제 Action을 바꾸는가
- 불확실성에 대응 Channel이 있는가

다.

`Objective`도 중요하다.

> **Mission 이름이 다른 것이 아니라 Objective가 같은 Action의 가치 순위를 실제로 바꿔야 전략적 목표 차이가 발생한다.**

현재 가장 중요한 Evidence Gap은:

> **RTS / 4X / Multiplayer / Human Planning Horizon / Recovery Window / Error Propagation / Dominant Opening / Late-game Solved State**

이다.

따라서 다음 Reference 확장은 유명 Strategy Game 수를 늘리는 것보다:

> **Build Order가 언제 고정 Opening이 되는가?  
> Scout 정보가 실제 Strategy Switch를 만드는가?  
> 한 실수가 언제 Recoverable → Deterministic Loss로 넘어가는가?  
> 장기 우위가 언제 Game을 사실상 끝냈는데 플레이만 계속되는가?**

에 Direct Design Evidence / Telemetry가 존재하는 사례를 우선 조사하는 편이 효율적이다.

---

# 23. Source Trace

## Primary Strategy Evidence
- REF-03 — Into the Breach
- REF-02 — FTL: Faster Than Light
- REF-16 — Invisible, Inc.

## Strong Strategy / Hybrid
- REF-14 — Mini Metro
- REF-07 — Against the Storm
- REF-24 — Dorfromantik

## Adjacent / Control
- REF-21 — Mark of the Ninja
- REF-18 — Loop Hero
- REF-28 — Thronefall

## Baseline
- STUDIO_CORE_CANDIDATES_v0.2
- Studio OS — Evidence-Based Core Extraction Master Prompt v0.2
- Studio OS — Strategy Genre Core Deep Extraction Prompt v0.1

---

# 24. Traceability Rule

Core는 원본 Reference를 대체하지 않는다.

Strategy 위험 신호가 발생하면:

```text
Strategy Core
↓
Primary Reference
↓
Current State
↓
Player Goal
↓
Available Actions
↓
Future Consequence
↓
Trade-off
↓
Counterplay / Adaptation
↓
Current Project
```

순서로 다시 내려가 검토한다.

`STRATEGY_CORE_CANDIDATES_v0.1`은 Studio OS Reviewer가 Unit 수, Map 크기, Action 수 같은 표면적 복잡도가 아니라 **Future Option Value, Replanning, Objective-conditioned Action Value**를 중심으로 신규 Strategy 기획을 평가하기 위한 압축된 Genre 판단 계층이다.
