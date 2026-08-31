# MANAGEMENT_CORE_CANDIDATES_v0.1

**Studio OS — Management Genre Core Deep Extraction**  
**Document:** `MANAGEMENT_CORE_CANDIDATES_v0.1`  
**Status:** `APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE`  
**Purpose:** 신규 Management / Operations / City / Colony / Roster / Survival / Network Management 기획 평가용 Genre-specific Reviewer Knowledge Base  
**Baseline:** `STUDIO_CORE_CANDIDATES_v0.2`  
**Extraction Prompt:** `Studio OS — Management Genre Core Deep Extraction Prompt v0.1`  
**Provisional Genre Cores:** `GC-MGMT-001`, `GC-MGMT-002`, `GC-MGMT-004 ~ GC-MGMT-009`  
**Candidates:** `GC-MGMT-003`, `GC-MGMT-010 ~ GC-MGMT-015`  
**Merged:** `GC-MGMT-016 → GC-MGMT-001 Sub-rule`  
**Pending:** `Additional Evidence / Prototype Validation / Internal Evidence`  
**Evidence Rule:** Tier A Primary Management Evidence를 Provisional Core 승격의 중심 근거로 사용하며, Tier B/C는 강화·반례·Boundary 설정에 사용한다.

---

# 1. Executive Summary

이번 Deep Extraction의 핵심 결론은 다음과 같다.

1. **Management의 핵심은 관리 대상의 수가 아니라 `Priority Conflict`다.**
   - 여러 Meter가 있어도 항상 같은 순서로 채우면 깊은 Management가 아니다.
   - 제한된 Capacity 때문에 동시에 해결할 수 없는 문제가 존재하고, Context에 따라 우선순위가 바뀌어야 한다.

2. 기존 `GC-MGMT-001 — Management Depth Comes from Priority Conflict`는 **STRENGTHEN / PROVISIONAL CORE 유지**가 맞다.

3. 기존 `GC-MGMT-002 — Loss Needs Recovery Structure` 역시 **STRENGTHEN / PROVISIONAL CORE 유지**가 타당하다.
   - 다만 `Death Spiral Control`은 별도 Candidate로 분리한다.
   - Loss가 있다는 것과 Recovery가 재미있는 관리 문제를 만든다는 것은 같은 문제가 아니다.

4. 기존 `GC-MGMT-003 — Automation Should Remove Execution, not Decisions`는 **KEEP AS CANDIDATE**가 맞다.
   - 논리적으로 강하지만 현재 Primary Management Reference에서 직접적인 자동화 전후 행동 Evidence가 부족하다.
   - Loop Hero 등 Secondary Evidence 비중이 높다.

5. 신규 Provisional Management Core로 다음을 추가한다.
   - `GC-MGMT-004 — Persistent State Must Reprioritize`
   - `GC-MGMT-005 — Future Pressure Must Compete with Present Efficiency`
   - `GC-MGMT-006 — Routine Must Be Recontextualized`
   - `GC-MGMT-007 — Information Must Support Diagnosis and Priority`
   - `GC-MGMT-008 — Growth Must Transform Constraints, not Erase Management`
   - `GC-MGMT-009 — Crisis Should Test the Existing Management State`

6. Management의 반복 Anti-Pattern은 다음과 같다.
   - More Meters = More Depth
   - Scarcity without Choice
   - One Priority Dominates Everything
   - Punishment without Recovery
   - Death Spiral without Counterplay
   - Growth Removes Management
   - Maintenance Click Inflation
   - Alert Spam
   - Dashboard without Decisions
   - Automation Removes Agency
   - Micromanagement without Fantasy
   - Crisis as Detached Mini-game
   - Fake Policy Choice
   - Infinite Positive Snowball
   - Content Count as Management Variety

7. AI Tester는 Management에서 특히 유용하다.
   - Resource
   - Capacity
   - Allocation
   - Priority
   - Recovery
   - Snowball
   - Strategy concentration
   - State transition

   을 구조적으로 측정할 수 있다.

8. 그러나 다음은 Human Evidence 없이는 결론 내리지 않는다.
   - Fun
   - Tension
   - Perceived Control
   - Job Fantasy
   - Administrative Fatigue
   - Crisis Fairness
   - Information Readability

9. Management Reviewer의 가장 중요한 한 문장은 다음과 같다.

> **“현재 가장 중요한 문제가 무엇인지 읽고, 제한된 Capacity를 어디에 배분할지 결정하며, 그 결과 때문에 다음 우선순위가 실제로 달라지는가?”**

10. 현재 Evidence Gap 중 가장 큰 것은:
   - 실제 Priority Switching telemetry
   - Automation 전후 의사결정 데이터
   - Death Spiral / Recovery telemetry
   - Administrative Fatigue
   - Management UI 행동 데이터
   - 안정기와 위기 리듬
   - 실패한 Economy / Management Control Case
   - Entity Growth와 Decision Growth의 관계

---

# 2. Management Genre Definition

Studio OS에서 `Simulation`과 `Management`를 동일하게 취급하지 않는다.

## 2.1 Simulation

시스템이 상태를 변화시키고 세계가 작동하는 구조.

예:
- 주민이 이동한다.
- 생산물이 생성된다.
- 날씨가 변화한다.
- AI Agent가 욕구에 따라 행동한다.

이러한 Simulation이 존재한다는 사실만으로 Management Evidence가 되는 것은 아니다.

## 2.2 Management

플레이어가:

1. 상태를 읽고,
2. 문제를 식별하고,
3. 우선순위를 정하고,
4. 제한된 Capacity를 배분하고,
5. 일부 문제를 해결 / 지연 / 감수하고,
6. 그 결과로 바뀐 상태를 다시 읽고,
7. 다음 우선순위를 재설정하는

구조.

## 2.3 Management Inclusion Test

Primary Management Evidence로 분류하기 위해 다음을 확인한다.

### A. Managed State
지속적으로 관리해야 하는 상태가 존재하는가?

### B. Scarcity / Capacity
모든 문제를 동시에 해결할 수 없게 하는 제한이 존재하는가?

### C. Allocation
제한된 자원·시간·인력·공간·처리량을 어디에 사용할지 선택하는가?

### D. Opportunity Cost
한 문제 해결이 다른 문제 해결 가능성을 실제로 낮추는가?

### E. Persistent Consequence
현재 선택이 다음 관리 상태를 변경하는가?

### F. Reprioritization
상태 변화 때문에 다음 Priority가 실제로 달라지는가?

## 2.4 Management Core Loop

```text
Observe State
     ↓
Identify Problems
     ↓
Set Priority
     ↓
Allocate Limited Capacity
     ↓
Resolve / Delay / Accept Loss
     ↓
State Changes
     ↓
New Constraint / New Opportunity
     ↓
Reprioritize
```

다음 구조만 반복된다면 깊은 Management Evidence로 자동 인정하지 않는다.

```text
숫자 증가
→ Upgrade 구매
→ 숫자 증가
```

---

# 3. Source Classification

## 3.1 Tier A — Primary Management Evidence

### REF-01 — Papers, Please

**Subtype:** Operations / Desk Management  
**Evidence Strength:** VERY HIGH — Priority / Time / Information / Routine

강한 Evidence 영역:
- Time Pressure
- Rule Processing
- Information Prioritization
- Income / Family Cost
- Error Cost
- Repeated Job Verb
- Efficiency vs Human Exception
- Progressive Complexity

핵심 관찰:
같은 승인/거절 입력이 시간·돈·가족·정치·도덕 결과를 동시에 만들며, 매일 바뀌는 규칙 때문에 같은 업무의 Priority와 의미가 바뀐다.

---

### REF-06 — Darkest Dungeon

**Subtype:** Roster / Long-term Consequence Management  
**Evidence Strength:** VERY HIGH — Persistent State / Loss / Recovery

강한 Evidence 영역:
- Roster State
- Stress / Injury / Disease
- Recovery Cost
- Replacement
- Retreat
- Long-term Consequence
- Short-term Success vs Long-term Cost

핵심 관찰:
전투의 작은 손실이 다음 원정의 인력·비용·파티 구성 Priority를 바꾼다. 영구 손실만 있는 것이 아니라 치료·교체·철수라는 중간 관리 선택이 존재한다.

---

### REF-07 — Against the Storm

**Subtype:** Roguelite Settlement Management  
**Evidence Strength:** VERY HIGH — Adaptation / Constraint / Session

강한 Evidence 영역:
- Limited Tools
- Resource Adaptation
- Settlement Priority
- Production Chain
- Environmental Constraint
- Run-specific Planning
- Session Reset

핵심 관찰:
모든 건물·자원·종족을 항상 확보할 수 없기 때문에 같은 최적 도시를 복제하기보다 현재 조건에 맞춰 Priority를 재설정해야 한다.

---

### REF-08 — Frostpunk

**Subtype:** Survival City Management  
**Evidence Strength:** VERY HIGH — Future Pressure / Policy / Crisis

강한 Evidence 영역:
- Resource Pressure
- Workforce Allocation
- Future Threat
- Law / Policy
- Heat / Infrastructure
- Moral Economy
- Crisis Escalation

핵심 관찰:
다가오는 추위를 미리 보여줘 현재 효율과 미래 준비를 충돌시키며, 정책 선택을 실제 생산·질서 문제와 결합한다.

---

### REF-13 — RimWorld

**Subtype:** Colony Simulation / Story-generating Management  
**Evidence Strength:** HIGH — Character State / Story / Selective Simulation

강한 Evidence 영역:
- Character State
- Work Priority
- Event Pressure
- Persistent Consequence
- Wealth / Threat interaction
- Emergent Story
- Selective Simulation

핵심 관찰:
관리 목표가 완벽한 최적화만이 아니라 사건과 캐릭터 상태가 만드는 이야기이므로 동일한 손실도 어떤 주민에게 발생했는지에 따라 관리 의미가 달라진다.

---

### REF-14 — Mini Metro

**Subtype:** Network / Flow Management  
**Evidence Strength:** HIGH — Capacity / Bottleneck / Information

강한 Evidence 영역:
- Capacity
- Bottleneck
- Network Reconfiguration
- Demand Growth
- Limited Routes / Cars / Tunnels
- Information Readability

핵심 관찰:
문제는 단순히 자원이 부족하다는 것이 아니라 수요와 처리 Capacity의 불균형이 특정 지점에 병목을 만들고, 제한 자원을 어디에 배치할지 지속적으로 재판단하게 하는 것이다.

---

### REF-15 — This War of Mine

**Subtype:** Survival / Household Management  
**Evidence Strength:** HIGH — Scarcity / Human Cost / Recovery

강한 Evidence 영역:
- Scarcity
- Character State
- Risk / Resource Allocation
- Survival Trade-off
- Moral Cost
- Recovery / Attrition

핵심 관찰:
같은 식량·약품도 캐릭터 상태와 사건에 따라 가치가 달라지며, 결핍은 선택을 만들지만 회복 가능성을 완전히 없애면 통제감도 사라진다.

---

# 3.2 Tier B — Management Hybrid / Secondary Evidence

### REF-02 — FTL
Use:
- Resource allocation
- Repair
- Crew
- Persistent damage
- Recovery
- Route choice
- Crisis management

### REF-18 — Loop Hero
Use:
- Automation
- Risk placement
- Indirect management
- Repeated execution reduction

### REF-19 — Cultist Simulator
Use:
- Time / Slot allocation
- Common grammar
- State management
- Cognitive load

### REF-22 — Stacklands
Use:
- Resource conversion
- Common grammar
- Production chains
- Card representation of management state

### REF-23 — Citizen Sleeper
Use:
- Limited action allocation
- Time pressure
- Character condition
- Narrative resource management

Tier B는 Core 강화와 Boundary 설정에 사용하지만 Tier B만으로 Management Provisional Core를 승격하지 않는다.

---

# 3.3 Tier C — Adjacent / Control Evidence

- Reigns
- Into the Breach
- 80 Days
- Dorfromantik
- Vampire Survivors

Use:
- Multi-axis consequence
- Information structure
- Route / future cost
- Growth / pressure contrast
- Input simplification

Tier C만으로 Management Provisional Core를 승격하지 않는다.

---

# 3.4 Control Limitation

현재 Reference Pool에는:

- 상업적으로 실패한 Management game
- 운영 UI가 과도해 이탈이 발생한 사례
- Automation으로 Agency가 제거된 사례
- Economy death spiral이 실제 플레이어 이탈을 만든 사례

의 상세 Postmortem이 부족하다.

따라서 일부 Anti-Pattern은 성공작의 Warning과 구조 분석에서 도출된 Candidate Mechanism이다.

---

# 4. Existing Core Audit

# GC-MGMT-001 — Management Depth Comes from Priority Conflict

**Decision:** `STRENGTHEN`  
**Status:** `PROVISIONAL CORE`  
**Origin:** `EXISTING GC REFINEMENT`

## Refined Rule

> **Management의 깊이는 관리 대상의 수보다, 동시에 해결할 수 없는 문제 사이에서 Priority를 선택하고 그 Priority가 Context에 따라 바뀌는지로 평가한다.**

## Mechanism

Management에서 Scarcity나 Meter는 독립적으로 깊이를 만들지 않는다.

다음이 필요하다.

```text
문제 A를 해결하면
→ Capacity가 소비되고
→ 문제 B 해결이 늦어지며
→ B의 상태가 악화되어
→ 다음 Priority가 바뀐다.
```

Priority가 항상 동일하다면 Meter가 많아도 실질적 Decision은 하나다.

## Primary Evidence

### Papers, Please
정확성·처리량·가족 생계·도덕적 예외가 같은 판정에서 충돌한다.

### Frostpunk
난방·식량·의료·인력·미래 추위 준비가 동시에 해결될 수 없으며 현재 생존과 미래 대비가 충돌한다.

### Darkest Dungeon
현재 원정 승리와 장기 로스터 보존·치료비가 충돌한다.

### This War of Mine
식량·약품·위험 행동을 누구에게 / 언제 사용할지가 캐릭터 상태와 도덕적 비용에 따라 달라진다.

## Secondary Evidence

- Against the Storm
- Mini Metro
- FTL

## Counter Evidence

Optimization Puzzle처럼 특정 Priority의 최적화 자체가 Product Promise인 게임에서는 Priority 다양성이 낮아도 성립할 수 있다.

단, 그 경우 Management Depth를 “다양한 우선순위 판단”으로 홍보해서는 안 된다.

## Applies To

- Operations
- Roster
- City
- Survival
- Network
- Roguelite Management

## Observed Metric

현재 Reference에서 Priority Switching Rate 같은 공통 원시 Telemetry는 제공되지 않는다.

## Candidate Metric — Machine

- Concurrent Critical Problems
- Priority Switching Rate
- Action Allocation Distribution
- Problem Neglect Duration
- Dominant Priority Rate
- Priority Reversal by Context

## Candidate Metric — Human

- Priority Tension
- “왜 이것을 먼저 해결했는가?” Explanation
- Perceived Opportunity Cost

## Validation Type

Hybrid.

## AI Tester Applicability

VERY HIGH for allocation/priority distribution.

## Confidence

**VERY HIGH**

## Reviewer Action

관리 자원이나 Meter가 많다면:

> “상황이 달라졌을 때 최우선 지표가 실제로 바뀌는가?”

를 묻는다.

항상 같은 답이면 `ONE_PRIORITY_DOMINATES_RISK`.

---

# GC-MGMT-002 — Loss Needs Recovery Structure

**Decision:** `STRENGTHEN`  
**Status:** `PROVISIONAL CORE`  
**Origin:** `EXISTING GC REFINEMENT`

## Refined Rule

> **지속되는 손실을 Management에 사용할 경우, 손실 후 상태가 새로운 배분·복구·교체·철수 판단을 만들어야 하며 단순 Power 감소로 끝나서는 안 된다.**

## Mechanism

Loss가 존재한다고 관리 깊이가 생기지 않는다.

좋은 Recovery Structure는:

```text
손실 발생
→ 어떤 것을 포기할지 결정
→ 제한된 Recovery Capacity 배분
→ 회복 / 교체 / 철수
→ 다음 운영 상태 변화
```

를 만든다.

## Primary Evidence

### Darkest Dungeon
영구 손실이 강하지만:
- 철수
- 치료
- 신규 모집
- 로스터 교체

가 존재해 성공/실패 이분법 사이에 관리 공간을 만든다.

### This War of Mine
굶주림·질병·상처·우울이 누적되지만 치료·식량·행동 배분이 회복 판단을 만든다. Reference는 결핍이 선택을 만들더라도 회복 가능성을 완전히 없애면 통제감도 사라진다고 정리한다.

### Frostpunk
질병·자원 위기·사회 수치 문제를 인력·시설·정책·비축을 통해 수습하는 구조가 존재하며, 예고된 위기가 사전 준비 Window를 제공한다.

## Secondary Evidence

FTL:
Repair / Crew / Retreat / System Recovery.

## Counter Evidence

- Permadeath 자체가 Run reset의 핵심인 짧은 Roguelike
- 실패 후 즉시 새 판을 시작하는 게임

에서는 개별 손실 Recovery가 필수는 아니다.

## Candidate Metric — Machine

- Recovery Option Usage
- Recovery Success Rate
- Time to Recovery
- Replacement Rate
- Retreat Rate
- Unrecoverable State Rate

## Candidate Metric — Human

- Recovery Legibility
- Perceived Hopelessness
- Perceived Fairness

## Validation Type

Hybrid.

## AI Tester Applicability

HIGH.

## Confidence

**HIGH**

## Reviewer Action

영구부상·피로·고장·사망을 발견하면:

> “이 상태는 다음에 어떤 Recovery Decision을 만드는가?”

를 묻는다.

답이 단순히 “효율이 감소한다”라면 Punishment System일 가능성을 우선 검토한다.

---

# GC-MGMT-003 — Automation Should Remove Execution, not Decisions

**Decision:** `KEEP`  
**Status:** `CANDIDATE`  
**Origin:** `EXISTING GC REFINEMENT`

## Rule Candidate

> **Automation은 이미 해결된 반복 Execution을 줄이되, 플레이어의 핵심 Priority Setting과 Exception Handling까지 제거해서는 안 된다.**

## Supporting Evidence

### Tier B — Loop Hero
자동 전투 / 진행을 사용하면서 플레이어는:
- 타일 배치
- 위험 생성
- 철수
- 장비 / 전략

에 집중한다.

### Tier A 간접 Evidence — Mini Metro
개별 승객을 직접 이동시키지 않고 Network Level에서 노선과 차량을 배치한다. 이는 “세부 실행보다 관리 레벨의 결정”이라는 Boundary를 지지한다.

## Promotion Blocker

Primary Management 사례에서:

- Automation 전후 Manual Action Reduction
- Decision Diversity 변화
- Player Agency 변화

를 직접 비교한 Evidence가 부족하다.

## Candidate Metric

### Machine
- Manual Action Reduction
- Decision Diversity before / after Automation
- Automation Override Rate
- Reconfiguration Frequency

### Human
- Perceived Agency
- Administrative Fatigue
- “Automation 이후 무엇을 관리한다고 느끼는가?”

## Confidence

**MEDIUM**

## Reviewer Action

Automation을 편의 기능이라고 자동 승인하지 않는다.

> “이 기능이 없애는 것은 이미 해결된 Execution인가, 아직 중요한 Management Decision인가?”

를 확인한다.

---

# 5. Provisional Management Cores

# GC-MGMT-004 — Persistent State Must Reprioritize

**Status:** `PROVISIONAL CORE`  
**Origin:** `GENRE SPECIALIZATION OF UC-DESIGN-003`

## Pattern

Management에서 지속 상태의 가치가 높은 사례들은 단순 Penalty Stack이 아니라 다음 Priority와 Allocation을 바꾼다.

## Management Context

- Roster Management
- Survival Management
- Colony Management
- Long-form Operations

## Rule

> **Persistent State를 추가할 때는 그 상태가 이후 어떤 Priority / Assignment / Resource Allocation을 바꾸는지 확인한다. 다음 판단을 바꾸지 않는 지속 상태는 관리 깊이보다 추적 부담이 될 수 있다.**

## Mechanism

```text
부상
→ 현재 효율 -10%
```

보다:

```text
부상
→ 해당 인력 투입 위험 증가
→ 치료 Capacity 경쟁
→ 대체 인력 필요
→ 다음 임무 구성 변경
```

일 때 Management가 된다.

## Primary Evidence

### Darkest Dungeon
스트레스·부상·질병·기벽이 다음 파티 편성·치료·교체 판단에 직접 연결된다.

### RimWorld
주민의 특성·관계·부상·욕구가 생산·구조·사건 대응의 Priority를 바꾼다.

### This War of Mine
캐릭터의 질병·상처·우울 상태가 같은 자원의 가치와 야간 파견 판단을 바꾼다.

## Counter Evidence

짧은 Session에서 상태가 한두 번만 사용되고 종료되는 게임에서는 Persistence가 필요하지 않을 수 있다.

## Candidate Metric — Machine

- Persistent State Frequency
- State → Assignment Change Rate
- State → Resource Allocation Change Rate
- State Duration
- State Ignored Rate

## Candidate Metric — Human

- Consequence Ownership
- State Meaning Recognition

## AI Tester Applicability

HIGH structurally.

## Confidence

**HIGH**

## Reviewer Action

상태 이상 종류가 많다면 개수보다:

> “상태 X 때문에 실제로 어떤 다음 선택이 달라지는가?”

를 하나씩 매핑한다.

---

# GC-MGMT-005 — Future Pressure Must Compete with Present Efficiency

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

Management에서 장기 계획이 강한 사례는 Future Threat / Demand가 현재 행동과 실제 Resource Competition을 만든다.

## Rule

> **Forecast / Deadline / Future Threat를 사용할 경우, 플레이어가 현재 문제 해결에 자원을 쓸지 미래 대비를 위해 Reserve할지 고민하게 만들어야 한다. 단순 Countdown만 추가하지 않는다.**

## Mechanism

미래 위기가 알려져도 현재 행동을 바꾸지 않는다면 정보일 뿐이다.

```text
현재 소비
vs
미래 비축
```

이 실제 Opportunity Cost가 될 때 Planning이 발생한다.

## Primary Evidence

### Frostpunk
다가오는 추위를 명확히 예고하여 현재 생산/확장과 석탄·식량·인프라 대비를 충돌시킨다.

### Mini Metro
현재 병목과 미래 Network 확장을 위해 제한 노선·차량·터널을 어디에 사용할지가 충돌한다. 수요는 계속 증가해 완전한 안정 상태를 허용하지 않는다.

### Against the Storm
현재 부족 해결과 장기 생산 체인, 위험 Glade, 폭풍 / Impatience 압력이 함께 Future-oriented Resource Planning을 요구한다.

## Counter Evidence

Relaxed sandbox / creative management에서는 장기 Threat 없이도:
- 효율화
- 미학
- 확장

이 Motivation이 될 수 있다.

## Candidate Metric — Machine

- Reserve Level
- Pre-crisis Preparation Rate
- Current Spend vs Reserve Ratio
- Forecast Usage
- Preparation Failure Rate
- Future-pressure-triggered Allocation Change

## Candidate Metric — Human

- Future Threat Legibility
- “미래 때문에 현재 계획을 바꿨는가?”
- Perceived Preparation Window

## AI Tester Applicability

HIGH.

## Confidence

**HIGH**

## Reviewer Action

재난 타이머가 있다면:

> “이 타이머를 보고 5분 전에 무엇을 다르게 해야 하는가?”

를 묻는다.

답이 없다면 `COUNTDOWN_WITHOUT_PLANNING_RISK`.

---

# GC-MGMT-006 — Routine Must Be Recontextualized

**Status:** `PROVISIONAL CORE`  
**Origin:** `GENRE SPECIALIZATION OF UC-DESIGN-002`

## Pattern

Management는 반복 Verb가 많다. 강한 사례는 반복 행동을 없애는 대신 Context 변화로 같은 행동의 Priority와 의미를 바꾼다.

## Rule

> **반복 업무를 Core Loop로 사용할 경우, 동일 행동이 새로운 규칙·수요·상태·제약 때문에 다른 판단을 요구해야 한다. 같은 판단을 같은 방식으로 반복하면 Routine이 Management가 아니라 행정 노동으로 변한다.**

## Primary Evidence

### Papers, Please
승인/거절과 문서 대조는 유지되지만 매일:
- 규칙
- 문서 종류
- 정치 상황
- 인간적 예외

가 바뀌어 같은 판정의 의미가 달라진다.

### Mini Metro
노선 연결/수정 Verb는 동일하지만 역·수요·병목 위치가 계속 바뀌어 네트워크를 완성할 수 없다.

### Against the Storm
건설·생산·배치 Verb는 반복되지만 바이옴·종족·청사진·자원 조건이 달라 동일한 완성 공략을 재현하기 어렵다.

## Counter Evidence

Idle / Relaxing / Repetitive Craft 게임처럼 반복 자체가 리듬과 만족감인 Product Promise에는 약하게 적용한다.

## Candidate Metric — Machine

- Same Action Context Variance
- Action Priority Shift by State
- Repeated Action Sequence Concentration
- Last Context-driven Plan Change

## Candidate Metric — Human

- Routine Fatigue
- “같은 일을 반복한다” vs “같은 도구로 다른 문제를 푼다” 인식

## Confidence

**HIGH**

## Reviewer Action

반복 클릭이 많다면 입력 수를 줄이기 전에:

> “이 클릭은 새로운 Context를 읽은 결과인가, 이미 결정된 업무를 재실행하는 것인가?”

를 구분한다.

---

# GC-MGMT-007 — Information Must Support Diagnosis and Priority

**Status:** `PROVISIONAL CORE`  
**Origin:** `GENRE SPECIALIZATION OF UC-DESIGN-005`

## Pattern

Management UI의 핵심은 정보량이 아니라 “무엇이 문제이며 어디에 Capacity를 투입해야 하는가”를 판별하는 데 있다.

## Rule

> **Management 정보는 상태를 나열하는 것보다 문제의 위치·원인·추세·우선순위를 판단하는 데 사용되어야 한다. 표시되지만 행동을 바꾸지 않는 Dashboard 정보는 UI 비용으로 취급한다.**

## Primary Evidence

### Mini Metro
도형과 선으로 수요·노선·병목을 공간적으로 읽게 하며, 시각 가독성이 Core Loop를 지원한다.

### Papers, Please
정보 위치·규칙집·문서 대조 UI 자체가 판단 도구이며, 무엇을 검사해야 하는지 학습하는 것이 Gameplay다.

### Frostpunk
열 지도·자원 흐름·사회 수치가 현재 위기와 미래 생존 판단에 사용된다.

### RimWorld
다양한 주민 상태와 업무 Priority를 관리하기 때문에 정보 필터링이 중요하며, 높은 시스템 복잡도는 UI 부담을 직접 만든다.

## Counter Evidence

Information Discovery 자체가 Mystery / Investigation Fantasy라면 원인을 즉시 명확하게 보여줄 필요가 없다.

## Candidate Metric — Machine

- Information Check → Action Change Rate
- Alert → Action Rate
- Ignored Alert Rate
- Forecast Usage

## Candidate Metric — Human / Hybrid

- State Diagnosis Accuracy
- Priority Explanation
- Information Readability
- Information Overload

## AI Tester Applicability

MEDIUM-HIGH for usage, Human needed for readability.

## Confidence

**HIGH**

## Reviewer Action

화면에 표시되는 지표마다:

> “이 정보를 본 뒤 어떤 다른 결정을 내릴 수 있는가?”

를 요구한다.

---

# GC-MGMT-008 — Growth Must Transform Constraints, not Erase Management

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

지속적으로 의미 있는 Management를 유지하는 사례는 성장 후 모든 부족을 해결해 끝내기보다 성장과 함께 새로운 병목·수요·위협을 만들어 Priority 문제를 변형한다.

## Rule

> **성장이 Core Management Constraint를 영구히 제거한다면 후반 Decision Collapse 위험을 검토한다. 성장 후에는 단순 Workload 증가가 아니라 다른 종류의 Priority Conflict가 나타나야 한다.**

## Mechanism

나쁜 형태:

```text
생산 증가
→ 모든 자원 풍족
→ 모든 문제 자동 해결
→ 남는 것은 Upgrade 반복
```

좋은 형태 후보:

```text
생산 증가
→ 규모 / 수요 / 위험 증가
→ 새 Constraint 발생
→ 새로운 Priority
```

## Primary Evidence

### Mini Metro
시간이 지날수록 역·승객이 늘어 더 높은 Network Complexity와 병목을 만든다.

### RimWorld
기지 성장과 부가 위협을 연결하여 단순 축적이 항상 안전한 최선이 되지 않게 한다.

### Frostpunk
기술·인프라가 성장해도 인구·질병·추위·시나리오 위기가 새로운 압박을 만든다.

### Against the Storm
정착 성장과 Reputation 진행 속에서도 폭풍·Impatience·생산 체인·새 목표가 관리 문제를 지속한다.

## Counter Evidence

- Power Fantasy Management
- Creative Sandbox
- Tycoon에서 후반 “완전 자동화”가 의도된 보상

은 Core Tension 소멸 자체가 성공 상태일 수 있다.

## Candidate Metric — Machine

- Resource Overflow Rate by Phase
- Priority Switching Rate by Phase
- Decision Entropy by Phase
- Constraint Count / Type by Phase
- Idle Capacity
- Dominant Strategy Concentration late-game

## Candidate Metric — Human

- Growth Satisfaction
- “성장 후에도 관리할 이유가 남는가?”
- Late-game Fatigue

## Confidence

**HIGH**

## Reviewer Action

업그레이드가 Problem을 없애는지 볼 때:

> “이 문제가 사라진 뒤 어떤 새로운 Management Question이 생기는가?”

를 묻는다.

---

# GC-MGMT-009 — Crisis Should Test the Existing Management State

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

강한 Management Crisis는 평소 Loop와 분리된 전투/미니게임이 아니라 평소:
- Reserve
- Roster
- Infrastructure
- Policy
- Allocation

결과를 시험한다.

## Rule

> **Crisis는 평소 Management 선택의 누적 결과를 시험하고 같은 자원·Capacity·상태를 재배치하게 해야 한다. Crisis 전용 별도 시스템이 평소 의사결정을 무효화한다면 연결성을 재검토한다.**

## Primary Evidence

### Frostpunk
추위·질병·사회 위기는 평소 석탄 비축·인력·난방·정책 선택을 직접 시험한다.

### RimWorld
습격·정신 붕괴·사건은 기존 주민·기지·자원 상태와 상호작용하며 동일 사건도 Colony 상태에 따라 다른 결과를 만든다.

### This War of Mine
습격·질병·겨울·자원 고갈은 평소 제작·식량·파견·치료 결정의 결과 위에 발생한다.

## Counter Evidence

장르 하이브리드에서 Crisis 전용 Combat 자체가 중요한 Product Promise라면 별도 시스템도 가능하다.

단, Management와 전투 사이의 결과 연결은 별도 검토해야 한다.

## Candidate Metric — Machine

- Pre-crisis Preparation Rate
- Crisis Resource Cost
- Crisis Outcome vs Pre-state Correlation
- Cascading Failure Count
- Crisis-specific System Dependency

## Candidate Metric — Human

- Crisis Fairness
- Consequence Ownership
- “준비할 수 있었다” 인식

## Confidence

**HIGH**

## Reviewer Action

Crisis가 등장하면:

> “평소 Management를 잘한 플레이어가 Crisis에서 무엇을 다르게 할 수 있는가?”

를 확인한다.

---

# 6. Management Core Candidates

# GC-MGMT-010 — Death Spiral Needs an Intervention Window

**Status:** `CANDIDATE`  
**Origin:** `SPLIT FROM GC-MGMT-002`

## Rule Candidate

> 손실이 추가 손실을 만드는 Negative Feedback Chain을 사용할 경우, 플레이어가 악순환을 인식하고 일부 비용을 감수해 끊을 수 있는 Intervention Window가 필요하다.

## Mechanism

```text
손실
→ 생산력 감소
→ 자원 부족
→ 추가 손실
→ 생산력 추가 감소
```

이 자동 진행되면 관리가 아니라 지연된 Game Over가 될 수 있다.

## Supporting Evidence

- Darkest Dungeon — 복합 페널티가 겹치면 통제감이 급격히 줄 수 있다는 Warning.
- This War of Mine — 결핍과 상태 악화가 누적되지만 회복 가능성을 완전히 없애면 통제감도 사라진다는 분석.
- Frostpunk — 예고된 위기가 Preparation Window를 제공.

## Promotion Blocker

실제:
- Death Spiral Frequency
- Restart-optimal State
- Player recovery telemetry

가 부족하다.

## Candidate Metrics

- Snowball Rate
- Death Spiral Frequency
- Intervention Success Rate
- Restart-optimal State Frequency
- Time from First Loss to Unrecoverable State

## Confidence

**MEDIUM-HIGH**

---

# GC-MGMT-011 — Bottleneck Diagnosis is Distinct from Resource Scarcity

**Status:** `CANDIDATE`

## Rule Candidate

> Flow / Production Management에서는 총 자원량과 처리 Capacity를 별도로 평가한다. 충분한 총량이 있어도 Queue / Route / Facility Capacity 때문에 시스템이 실패할 수 있어야 Bottleneck Management가 성립한다.

## Primary Evidence

Mini Metro에서 매우 강함.

Against the Storm의 Production Chain이 보조 Evidence를 제공하지만 현재 Bottleneck telemetry는 부족하다.

## Applies To

- Network Management
- Factory / Production Management
- Hospital / Queue Management
- Logistics

## Boundary

Roster / Desk / Narrative Management 전체에는 적용하지 않는다.

## Candidate Metric

- Capacity Utilization
- Queue Length
- Bottleneck Duration
- Throughput
- Idle Upstream / Starved Downstream Rate

## Confidence

**MEDIUM**

---

# GC-MGMT-012 — Structural Policy Should Change Future Management, not only Add Efficiency

**Status:** `CANDIDATE`

## Rule Candidate

> Policy / Law / Permanent Upgrade를 “전략 방향 선택”으로 제시한다면 이후 Resource / Priority / Risk 구조를 바꿔야 하며 단순 +X% 효율 비교로 끝나서는 안 된다.

## Primary Evidence

Frostpunk에서 매우 강함:
법이 생산·질서·사회 방향을 실제로 바꾼다.

Against the Storm의 Cornerstone / Blueprint는 간접 강화 Evidence.

## Promotion Blocker

두 번째 독립 Primary 사례의 Policy-specific Evidence 부족.

## Candidate Metric

- Policy Concentration
- Policy → Action Distribution Change
- Policy → Resource Priority Change
- Universal Policy Rate

## Confidence

**MEDIUM**

---

# GC-MGMT-013 — Management Target Growth Must Add Decisions, not Workload

**Status:** `CANDIDATE`

## Rule Candidate

> 직원·도시·시설·지역·Queue 수의 증가는 새로운 Priority 관계를 만들 때만 Management Depth 증가로 평가한다. 동일 명령 반복량만 증가하면 Workload Inflation이다.

## Supporting Evidence

- RimWorld — Entity와 상태가 늘면 emergent interaction도 늘지만 UI / 학습 / QA 비용 폭증.
- Mini Metro — 역/수요 증가는 네트워크 병목 관계를 바꾸므로 새로운 판단을 만든다.
- Against the Storm — 시스템 규모가 커질수록 정보량과 Balance 부담 증가.

## Candidate Metrics

### Machine
- Entity Count vs Priority Switching
- Repeated Action Count
- Decision Diversity per Entity
- Automation Need Growth

### Human
- Administrative Fatigue
- Cognitive Load
- “새 문제” vs “같은 일 증가” 평가

## Confidence

**MEDIUM-HIGH**

---

# GC-MGMT-014 — Micromanagement Must Match the Player's Responsibility Level

**Status:** `CANDIDATE`

## Rule Candidate

> Direct Control의 세부 수준은 현실성보다 Player Job Fantasy가 책임지는 의사결정 레벨에 맞춰야 한다.

## Evidence

### Papers, Please
개별 문서의 직접 조작 자체가 심사관 Job Fantasy이므로 Micro input가 Core다.

### Mini Metro
개별 승객을 직접 움직이지 않고 Network level에서 관리한다.

### RimWorld
개별 주민을 직접 조작하기보다 Work Priority와 건설/배치로 간접 관리하는 부분이 크다.

## Hidden Variable

`Player Responsibility Scope`

## Candidate Metrics

- Manual Actions per Decision
- Repeated Command Rate
- Direct Override Rate
- Administrative Fatigue

## Confidence

**MEDIUM**

---

# GC-MGMT-015 — Stable Phase / Crisis Phase Pacing

**Status:** `CANDIDATE`

## Rule Candidate

> 지속 압박형 Management에서도 모든 순간을 Crisis로 만들기보다 준비·안정·압박·복구가 서로 다른 판단을 제공하는지 검토한다.

## Evidence

Frostpunk / This War of Mine / RimWorld가 리듬의 중요성을 시사하지만 Reference에 직접적인 pacing telemetry 부족.

## Candidate Metrics

- Stability Phase Duration
- Crisis Phase Duration
- Recovery Phase Duration
- Crisis Frequency
- Time Between Critical Events

## Human
- Tension Curve
- Fatigue
- “쉴 틈이 없다 / 할 일이 없다” 인식

## Confidence

**MEDIUM**

---

# GC-MGMT-016 — Scarcity Should Create Alternatives, not Waiting

**Status:** `CANDIDATE`

## Rule Candidate

> 자원 부족이 발생했을 때 플레이어가 대체·연기·전환·희생 중 무엇을 선택할지 고민해야 하며, 유일한 해결이 생산 완료를 기다리는 것이라면 Scarcity를 Meaningful Choice로 과대평가하지 않는다.

## Evidence

- Against the Storm — 모든 생산 체인을 확보할 수 없어 대체재 판단이 중요.
- This War of Mine — 같은 부족 자원을 누구에게 배분할지 선택.
- Frostpunk — 인력/자원/열을 서로 다른 용도로 배분.

## Promotion Blocker

Mechanism은 강하지만 `GC-MGMT-001 Priority Conflict`와 중복 가능성이 높다.

## Recommendation

현재는 `GC-MGMT-001`의 Sub-rule로 유지할 가능성이 높다.

## Confidence

**MEDIUM-HIGH**

---

# 7. Management Anti-Patterns

# AP-MGMT-001 — More Meters = More Depth

## Trigger
- Resource / Meter 종류만 증가
- Meter 간 우선순위 관계는 변하지 않음

## Mechanism
관리 상태가 많아도 모두 같은 방향으로 움직이면 실제 Decision은 하나다.

## Consequence
- UI 복잡도 증가
- 학습비 증가
- false depth

## Detection
- Dominant Priority Rate
- Meter Correlation
- Priority Switching Rate
- Unused / ignored state count

## Mitigation
Meter를 추가하기 전:

> “이 지표가 기존 Priority를 어떤 상황에서 뒤집는가?”

를 요구한다.

---

# AP-MGMT-002 — Scarcity without Choice

## Trigger
항상 부족하지만 해결법이 하나뿐.

## Consequence
- 기다림
- 반복 grind
- resource starvation frustration

## Detection
- Resource Starvation Rate
- Alternative Response Count
- Waiting Time
- Action Concentration

## Mitigation
- substitute
- defer
- convert
- sacrifice
- reroute

---

# AP-MGMT-003 — One Priority Dominates Everything

## Trigger
어떤 상황에서도 같은 Resource / Meter가 최우선.

## Consequence
많은 관리 요소가 존재해도 실제 전략은 하나.

## Detection
- Dominant Priority Rate
- Context-specific Priority Shift
- Allocation Concentration

## Mitigation
다른 문제의 시간 민감도 / 비용 / Recovery profile을 차별화한다.

---

# AP-MGMT-004 — Punishment without Recovery

## Trigger
부상·고장·피로·사망을 추가하지만:
- 치료
- 교체
- 철수
- 우회

가 없음.

## Consequence
Power 감소와 restart incentive만 증가.

## Detection
- Unrecoverable State Rate
- Recovery Option Count
- Restart-optimal State Frequency

## Mitigation
Loss를 새로운 관리 상태로 전환한다.

---

# AP-MGMT-005 — Death Spiral without Counterplay

## Trigger

```text
Loss
→ Capacity 감소
→ 추가 Loss
→ Capacity 추가 감소
```

가 개입 없이 자동 진행.

## Consequence
Delayed Game Over.

## Detection
- Death Spiral Frequency
- Intervention Success
- Time to Unrecoverable

## Mitigation
Emergency resource / retreat / downgrade / sacrifice / replacement.

---

# AP-MGMT-006 — Growth Removes Management

## Trigger
성장 후 모든 Resource가 Overflow하고 모든 문제가 자동 해결.

## Consequence
후반 Decision Collapse.

## Detection
- Resource Overflow Rate
- Priority Switching decline by phase
- Decision Entropy decline
- Idle Capacity

## Mitigation
성장과 함께 Constraint Type을 변화시키거나 Product Promise에 맞춰 게임을 종료한다.

---

# AP-MGMT-007 — Maintenance Click Inflation

## Trigger
규모가 커질수록 이미 정해진 업무의 반복 명령 수만 증가.

## Consequence
Administrative Fatigue.

## Detection
- Repeated Action Count
- Manual Actions per Meaningful Decision
- Reassignment Frequency without strategic reason

## Mitigation
Batch command / policy / automation / default behavior.

---

# AP-MGMT-008 — Alert Spam

## Trigger
모든 상태 변화가 긴급 알림으로 표시.

## Consequence
Priority 신호 소실.

## Detection
- Alert Frequency
- Ignored Alert Rate
- Alert → Action Rate

## Mitigation
Severity / cause / urgency를 분리하고 actionable alert만 상위 노출.

---

# AP-MGMT-009 — Dashboard without Decisions

## Trigger
많은 수치와 그래프가 존재하지만 실제 행동 변화와 연결되지 않음.

## Consequence
UI complexity without agency.

## Detection
- Information Check → Action Change Rate
- Ignored Panel Rate
- Panel-open duration vs action

## Mitigation
정보마다 연결되는 Decision을 명시한다.

---

# AP-MGMT-010 — Automation Removes Agency

## Trigger
Automation이 execution뿐 아니라 핵심 Priority까지 자동 최적화.

## Consequence
플레이어는 결과를 관찰할 뿐 관리하지 않음.

## Detection
- Decision Diversity before / after Automation
- Override Rate
- Reconfiguration Rate

## Mitigation
자동화는 실행을 맡고 예외·목표·우선순위는 플레이어에게 남긴다.

---

# AP-MGMT-011 — Micromanagement without Fantasy

## Trigger
Player Job Fantasy와 관계없는 단위 조작 증가.

## Consequence
현실성은 높지만 관리자로서의 책임 수준과 불일치.

## Detection
- Manual Action Count
- Job-relevance survey
- Administrative Fatigue

## Mitigation
Responsibility Level에 맞는 abstraction.

---

# AP-MGMT-012 — Crisis as Detached Mini-game

## Trigger
평소 자원·인력·시설 상태와 거의 무관한 별도 Crisis 시스템.

## Consequence
평소 Management의 준비 가치 약화.

## Detection
- Crisis Outcome vs Pre-crisis State Correlation
- Crisis-only Resource Dependency

## Mitigation
평소 상태와 동일 Capacity를 Crisis에서도 사용.

---

# AP-MGMT-013 — Fake Policy Choice

## Trigger
정책 이름은 다르지만 모두 동일 효율축의 +X% 비교.

## Consequence
전략 방향 선택처럼 보이지만 단순 Upgrade.

## Detection
- Policy Concentration
- Policy-induced Action Shift
- Universal Policy Rate

## Mitigation
정책이 Resource / Risk / Rule relationship을 바꾸도록 설계.

---

# AP-MGMT-014 — Infinite Positive Snowball

## Trigger

```text
Success
→ Production 증가
→ 더 큰 Success
→ Resource Overflow
→ 모든 문제 소멸
```

## Consequence
후반 Management 소멸.

## Detection
- Growth Rate
- Resource Overflow
- Late-game Constraint Count
- Dominant Strategy Concentration

## Mitigation
새 Demand / upkeep / exposure / risk를 추가하되 단순 숫자 Scaling으로만 해결하지 않는다.

---

# AP-MGMT-015 — Content Count as Management Variety

## Trigger
건물·직원·사건 수는 많지만 같은 Priority Rule 반복.

## Consequence
콘텐츠 제작비는 증가하지만 Decision Variety는 증가하지 않음.

## Detection
- Context-specific Strategy Shift
- Priority Reversal
- Content item → new decision mapping

## Mitigation
새 콘텐츠는 기존 Priority 관계를 바꿀 때 우선 추가.

---

# 8. Conflicting Findings

# CF-MGMT-001 — Scarcity vs Abundance

## Evidence A
Frostpunk / This War of Mine:
지속적인 결핍이 Core Tension.

## Evidence B
Creative / Tycoon Management에서는 성장 후 풍요 자체가 보상일 수 있음.

## Hidden Variable
- Player Fantasy
- Session Arc
- Product Promise
- Crisis Frequency
- End Condition

## Resolution
항상 부족해야 한다는 Core를 만들지 않는다.

질문:

> **Scarcity 또는 Abundance가 의도한 Priority Decision을 어떻게 바꾸는가?**

---

# CF-MGMT-002 — Direct Control vs Automation

## Evidence A
Papers, Please:
세부 문서 조작 자체가 Job Fantasy.

## Evidence B
Mini Metro:
개별 승객을 조작하지 않고 Network level에서 설계.

## Hidden Variable
`Player Responsibility Level`

## Resolution
Direct Control의 양이 아니라:

> 플레이어가 맡은 Job에서 어떤 레벨의 판단이 핵심인가?

를 본다.

---

# CF-MGMT-003 — Permanent Loss vs Recovery

## Evidence A
Darkest Dungeon:
Permadeath / persistent damage가 장기 비용을 만듦.

## Evidence B
짧은 Session / reset 구조에서는 개별 영구 손실 없이도 Management 성립 가능.

## Hidden Variable
- Run Reset
- Roster Size
- Replacement Cost
- Character Attachment
- Narrative Value

## Resolution
Permanent Loss를 장르 필수 요소로 두지 않는다.

---

# CF-MGMT-004 — Optimization vs Story Generation

## Evidence A
Mini Metro:
병목 최적화 자체가 Core Fantasy.

## Evidence B
RimWorld:
완벽한 최적화보다 사건과 실패가 만드는 Story가 상위 목표.

## Hidden Variable
`Product Promise`

## Resolution
RimWorld의 불확실성을 Mini Metro에, Mini Metro의 완전 효율 기준을 RimWorld에 강제하지 않는다.

---

# CF-MGMT-005 — Perfect Information vs Forecast Uncertainty

## Evidence A
Mini Metro:
현재 상태를 극도로 읽기 쉽게 공개.

## Evidence B
RimWorld / Against the Storm:
향후 사건 / 청사진 / 일부 조건이 불확실.

## Hidden Variable
- Planning Game
- Prediction Game
- Story Generation
- Risk Management

## Resolution
정보량보다 `GC-MGMT-007 Diagnosis and Priority`를 적용한다.

---

# CF-MGMT-006 — Large Management Scope vs Focused Job

## Evidence A
RimWorld / Frostpunk:
큰 시스템 범위.

## Evidence B
Papers, Please / Mini Metro:
극단적으로 압축된 Responsibility Scope.

## Hidden Variable

> **World Size가 아니라 Player Responsibility Scope.**

## Resolution
Management Depth를 세계 크기로 평가하지 않는다.

---

# CF-MGMT-007 — Stable Economy vs Constant Crisis

## Evidence A
Frostpunk / This War of Mine:
지속적인 Survival Pressure가 Core Fantasy.

## Evidence B
일부 Optimization / Builder는 안정 상태 자체가 성취.

## Hidden Variable
- Relaxation
- Optimization
- Survival Pressure
- Session Arc

## Resolution
“항상 Crisis가 있어야 한다”는 Core를 만들지 않는다.

대신 Stability가 오면:
- 게임 종료인가?
- 성장 보상인가?
- 새 Constraint 전환점인가?

를 본다.

---

# 9. AI Tester Metric Map

Metric은 Criteria가 아니다. Threshold를 여기서 고정하지 않는다.

## 9.1 Priority Metrics

| Metric | Type | Purpose |
|---|---|---|
| Concurrent Critical Problems | Machine | 동시 관리 압박 |
| Priority Switching Rate | Machine | 상태 변화에 따른 우선순위 전환 |
| Action Allocation Distribution | Machine | Capacity 배분 분포 |
| Problem Neglect Duration | Machine | 미처리 문제 지속 |
| Dominant Priority Rate | Machine | 동일 우선순위 지배 |
| Priority Reversal by Context | Machine | Contextual priority shift |

---

## 9.2 Resource Metrics

| Metric | Type |
|---|---|
| Resource Starvation Rate | Machine |
| Resource Overflow Rate | Machine |
| Reserve Level | Machine |
| Source / Sink Balance | Machine |
| Emergency Spend Rate | Machine |
| Resource Conversion Usage | Machine |
| Resource Waste | Machine |

---

## 9.3 Capacity Metrics

| Metric | Type |
|---|---|
| Capacity Utilization | Machine |
| Queue Length | Machine |
| Bottleneck Duration | Machine |
| Idle Capacity | Machine |
| Overload Duration | Machine |
| Throughput | Machine |

---

## 9.4 Workforce / Roster Metrics

| Metric | Type |
|---|---|
| Worker Utilization | Machine |
| Assignment Distribution | Machine |
| Reassignment Rate | Machine |
| Idle Rate | Machine |
| Injury / Fatigue Rate | Machine |
| Replacement Rate | Machine |
| Recovery Time | Machine |
| Skill Utilization | Machine |

---

## 9.5 Loss / Recovery Metrics

| Metric | Type |
|---|---|
| Recovery Option Usage | Machine |
| Recovery Success | Machine |
| Time to Recovery | Machine |
| Unrecoverable State Rate | Machine |
| Snowball Rate | Machine |
| Death Spiral Frequency | Machine |
| Restart-optimal State Frequency | Machine / model-dependent |

---

## 9.6 Economy Stability Metrics

| Metric | Type |
|---|---|
| Net Resource Trend | Machine |
| Upkeep Burden | Machine |
| Growth Rate | Machine |
| Reserve Volatility | Machine |
| Insolvency Rate | Machine |
| Positive Feedback Strength | Machine |
| Negative Feedback Strength | Machine |

---

## 9.7 Crisis Metrics

| Metric | Type |
|---|---|
| Crisis Frequency | Machine |
| Response Time | Machine |
| Preventable Failure Rate | Machine / model-dependent |
| Crisis Resource Cost | Machine |
| Cascading Failure Count | Machine |
| Pre-crisis Preparation Rate | Machine |

---

## 9.8 Information Metrics

| Metric | Type |
|---|---|
| Information Check → Action Change Rate | Machine / instrumented |
| Alert → Action Rate | Machine |
| Ignored Alert Rate | Machine |
| Forecast Usage | Machine |
| State Diagnosis Accuracy | Human / Hybrid |

---

## 9.9 Automation Metrics

| Metric | Type |
|---|---|
| Manual Action Reduction | Machine |
| Decision Diversity before / after Automation | Machine |
| Automation Override Rate | Machine |
| Automation Failure Rate | Machine |
| Player Reconfiguration Frequency | Machine |

---

## 9.10 Strategy Metrics

| Metric | Type |
|---|---|
| Strategy Concentration | Machine |
| Policy Concentration | Machine |
| Economy State Diversity | Machine |
| Dominant Strategy Success | Machine |
| Context-specific Strategy Shift | Machine |

---

## 9.11 Run / Session Metrics

| Metric | Type |
|---|---|
| Average Session Length | Machine |
| Failure Cause Distribution | Hybrid |
| Stability Phase Duration | Machine if state-defined / Hybrid for experience |
| Crisis Phase Duration | Machine if state-defined / Hybrid for experience |
| Recovery Phase Duration | Machine if state-defined / Hybrid for experience |
| Last Meaningful Policy Change | Hybrid |
| Last Meaningful Priority Change | Hybrid |

---

# 9.12 AI Tester Interpretation Limits

AI Tester가 직접 결론내릴 수 있는 것:

```text
Resource
Capacity
Allocation
Distribution
Failure
Recovery
Snowball
Priority
Strategy
State Transition
```

AI Tester가 직접 결론내리지 않는 것:

- 재미
- 긴장감
- 관리하는 느낌
- 스트레스가 즐거운가
- 위기가 불공정하게 느껴지는가
- 캐릭터 애착
- Job Fantasy
- UI 편안함
- 반복 관리 피로

---

# 10. Human Validation Map

## H-MGMT-001 — Priority Tension

> 동시에 해결하고 싶은 두 개 이상의 문제가 실제로 존재했는가?

관찰:
- 고민한 Priority
- 포기한 문제
- 선택 이유

---

## H-MGMT-002 — Perceived Control

> 실패했을 때 다음에는 무엇을 다르게 해야 할지 설명할 수 있는가?

---

## H-MGMT-003 — Recovery Legibility

> 손실 이후 복구 방법과 비용을 이해할 수 있는가?

---

## H-MGMT-004 — Information Readability

> 현재 가장 중요한 문제가 무엇인지 파악할 수 있는가?

---

## H-MGMT-005 — Administrative Fatigue

> 판단보다 반복 입력에 시간을 더 많이 쓰고 있지 않은가?

---

## H-MGMT-006 — Crisis Fairness

> 위기를 사전에 준비하거나 발생 후 수습할 수 있었다고 느끼는가?

---

## H-MGMT-007 — Growth Satisfaction

> 성장하면서 새로운 관리 판단이 생기는가, 단순히 일이 많아지거나 모든 문제가 사라지는가?

---

## H-MGMT-008 — Job Fantasy

> 플레이어는 자신이 무엇을 관리하는 사람인지 명확히 설명할 수 있는가?

---

## H-MGMT-009 — Consequence Ownership

> 현재 문제를 자신의 이전 선택 결과로 이해하는가?

---

## H-MGMT-010 — Stability / Pressure Pacing

> 안정·준비·위기·복구 사이의 리듬이 의도한 경험과 맞는가?

---

## H-MGMT-011 — Routine Recontextualization

> 같은 행동을 반복하고 있다고 느끼는가, 같은 도구로 새로운 문제를 해결한다고 느끼는가?

---

## H-MGMT-012 — Micromanagement Relevance

> 반복 조작이 자신의 Job에 필요한 판단이라고 느끼는가, UI 노동이라고 느끼는가?

---

# 11. Scale Handoff Candidates

이번 문서에서는 Scale Core로 승격하지 않는다.

# SCALE_HANDOFF-MGMT-001 — Entity × State × Event QA Explosion

## Finding

Management의 숨은 Production Cost는 Entity 수만이 아니라:

```text
Entity
× Persistent State
× Event
× Resource
× Policy
× Recovery Rule
```

조합에서 폭증할 수 있다.

## Evidence

- RimWorld — 방대한 상태 조합 / UI / QA
- Darkest Dungeon — 상태·클래스·적·캠페인 조합 QA
- Against the Storm — 자원·건물·종족·청사진 조합 Balance
- Frostpunk — 생산·인구·시나리오 Balance

## Handoff

`Genre × Scale Deep Extraction`에서 팀 규모별 QA Capacity와 함께 검토.

---

# SCALE_HANDOFF-MGMT-002 — Management UI State Cost

## Finding

작은 화면이나 추상 그래픽이라도 Management UI는:
- state visibility
- filtering
- alert
- forecast
- batch control
- exception handling

때문에 높은 polish 비용을 가질 수 있다.

## Evidence

Mini Metro:
미니멀한 시각 스타일에도 Balance와 UX polish 비용이 예상보다 컸다.

RimWorld / Against the Storm:
상태 수 증가가 UI / onboarding 비용으로 연결.

---

# SCALE_HANDOFF-MGMT-003 — Automation Tooling ROI

## Finding

Entity / Routine가 많아질수록 Automation은 UX Feature가 아니라:
- simulation tooling
- behavior rules
- exception handling
- debugging

Production System이 된다.

현재 Evidence는 부족하므로 Scale Candidate로만 전달한다.

---

# SCALE_HANDOFF-MGMT-004 — Content Authoring Cost

Scenario / Event / Character reaction을 Management Variety로 사용하는 경우:

- Event Count
- Character State reaction
- Localization
- QA

비용이 빠르게 증가한다.

Evidence:
- RimWorld
- This War of Mine
- Frostpunk

---

# GSC-MGMT-SOLO-HANDOFF-001 — Simulate the Player's Job, not the Whole World

기존 Studio Candidate를 이번 Genre 분석이 **강화**한다.

## Supporting Evidence

### Papers, Please
국가의 국경정책을 검문대 하나의 Job으로 압축.

### Mini Metro
도시 전체 교통을 실제 차량 Simulation이 아니라 노선망과 승객 수요로 추상화.

### This War of Mine
전쟁 전체가 아니라 소수 민간인의 은신처 생존에 집중.

## Counter / Boundary

### RimWorld
넓은 Simulation이 Story Generator라는 Product Promise에 직접 기여하므로 “항상 축소”가 답은 아니다.

## Handoff Decision

`Genre × Scale` 단계에서 **강한 Provisional Candidate**로 유지할 가치가 있다.

---

# 12. Universal Reclassification Candidates

이번 단계에서는 Universal로 직접 승격하지 않는다.

# UC-RECLASS-MGMT-001 — Capacity Mismatch vs Workload

## Candidate Universal Rule

> 문제의 총량보다 요구량과 처리 Capacity의 불일치가 플레이어 선택을 만드는 경우가 많다.

Management에서는 강하지만:
- tactical AP
- inventory slots
- attention budget

등 다른 장르에도 확장 가능성이 있다.

**Status:** `UNIVERSAL RECLASSIFICATION CANDIDATE`

---

# UC-RECLASS-MGMT-002 — Recovery Window

## Candidate Universal Rule

> 실패가 연쇄적으로 확대되는 시스템에서는 플레이어가 원인을 읽고 개입할 Window가 필요하다.

`UC-DESIGN-004 Uncertainty Response Agency`와 병합 가능성이 있으므로 별도 Universal 승격 금지.

---

# UC-RECLASS-MGMT-003 — Automation Should Preserve Decision Level

Management 밖에서도:
- auto combat
- crafting
- pathing
- batch operation

에 적용될 수 있다.

현재 Automation Evidence가 부족하므로 Universal 후보에만 등록.

---

# UC-RECLASS-MGMT-004 — Growth Should Not Accidentally Delete the Core Decision

Management에서 강하게 발견되지만:
- RPG
- deckbuilding
- strategy

에도 적용 가능성이 있다.

현재는 Management Evidence에 편중되어 있으므로 Universal 승격 금지.

---

# 13. Evidence Gaps

# GAP-MGMT-001 — Priority Switching Telemetry

부족:
- 실제 Priority Switching Rate
- Context별 우선순위 전환
- Player-reported priority

현재 Reference는 설계 구조 분석은 강하지만 Raw Behavior Telemetry가 약하다.

---

# GAP-MGMT-002 — Resource Starvation / Overflow Telemetry

필요:
- 어느 Resource가 항상 부족한가?
- 어느 Resource가 후반 Overflow하는가?
- Resource 중요도가 Phase별로 바뀌는가?

---

# GAP-MGMT-003 — Automation Before / After Data

필요:
- manual action count
- decision diversity
- override
- administrative fatigue

`GC-MGMT-003` 승격의 핵심 Gap.

---

# GAP-MGMT-004 — Death Spiral / Recovery Data

필요:
- Snowball onset
- recovery rate
- restart-optimal state
- intervention success

`GC-MGMT-010` 승격 핵심.

---

# GAP-MGMT-005 — Administrative Fatigue

현재 Reference는 반복 피로를 언급하지만:
- 클릭 수
- 화면 전환
- batch command usage
- fatigue survey

가 부족하다.

---

# GAP-MGMT-006 — Management UI Behavior Telemetry

필요:
- panel open
- alert click
- ignored warning
- diagnosis error
- forecast use

---

# GAP-MGMT-007 — Underperforming Economy Controls

성공 사례 중심이라:
- 하나의 Resource가 모든 것을 지배한 사례
- Resource Sink 실패
- Economy runaway
- permanent shortage
- late-game surplus collapse

의 상세 Postmortem이 부족하다.

---

# GAP-MGMT-008 — Management Target Growth

Entity 수 증가가:
- Decision Variety
- Administrative Burden
- Automation Need

에 미치는 실제 데이터 부족.

---

# GAP-MGMT-009 — Stable / Crisis Pacing

필요:
- stability duration
- event frequency
- player fatigue
- boredom
- perceived tension

---

# GAP-MGMT-010 — Job Fantasy / Responsibility Level

세부 조작 수준이:
- immersion
- control
- fatigue

와 어떻게 연결되는지 정량 Evidence 부족.

---

# 14. Additional Management References Needed

아래는 **향후 Research Target**이며 현재 Core Evidence가 아니다.

## P0 — Factorio

### 강화 대상
- `GC-MGMT-003 Automation`
- `GC-MGMT-011 Bottleneck`
- `GC-MGMT-013 Target Growth`
- `GC-MGMT-008 Growth Constraints`

### Research Questions
- Automation 전후 Player Decision level은 어떻게 변하는가?
- Throughput / bottleneck diagnosis가 핵심 판단인가?
- 규모 증가가 workload가 아니라 higher-order design으로 이동하는가?

### 찾을 Evidence
- Developer postmortem
- factory telemetry
- player behavior / automation design talks

---

## P0 — Oxygen Not Included

### 강화 대상
- Persistent State
- Bottleneck / Capacity
- Death Spiral
- Information Diagnosis
- System Coupling

### Research Questions
- 열·산소·압력·인력 상태가 어떻게 연쇄 실패를 만드는가?
- 플레이어에게 Recovery Window가 어떤 방식으로 제공되는가?

---

## P0 — Two Point Hospital

### 강화 대상
- Queue / Capacity
- Workforce
- Automation / delegation
- Administrative burden

### Research Questions
- 환자 Queue와 시설 Capacity가 Resource 부족과 어떻게 다른가?
- Staff assignment가 언제 meaningful decision이고 언제 반복 업무가 되는가?

---

## P0 — Banished

### 강화 대상
- Death Spiral
- Future Pressure
- Resource Reserve
- Population Growth

### Research Questions
- 겨울 / 인구 / 식량 악순환이 어떻게 발생하는가?
- Recovery가 가능한 상태와 사실상 끝난 상태의 경계는 무엇인가?

---

## P1 — Prison Architect

### 강화 대상
- Policy
- Workload
- Crisis
- Automation

### Research Questions
- Policy / regime scheduling이 행동을 어떻게 바꾸는가?
- Prison growth가 Decision과 Workload를 어떻게 변화시키는가?

---

## P1 — Football Manager

### 강화 대상
- Delegation
- Roster State
- Job Fantasy
- Information filtering

### Research Questions
- 무엇을 직접 하고 무엇을 Staff에게 위임하게 만드는가?
- 깊은 Management에서 Automation이 어떻게 Agency를 보존하는가?

---

## P1 — Dwarf Fortress

### 강화 대상
- Optimization vs Story Generation
- Selective Simulation
- Entity growth
- Information load

### Research Questions
- Simulation complexity가 어떤 순간 Player Value가 되고 어떤 순간 administrative burden이 되는가?

---

## P1 — Workers & Resources: Soviet Republic

### 강화 대상
- Production / Logistics
- Bottleneck
- System coupling
- Complexity scaling

### Research Questions
- 높은 현실성이 실제 Priority Decision과 어떤 관계가 있는가?
- Simulation detail이 Management value로 변환되는 조건은 무엇인가?

---

## P1 — Timberborn

### 강화 대상
- Future pressure
- drought planning
- reserve
- positive growth / new constraints

### Research Questions
- Drought forecast가 현재 resource allocation을 어떻게 바꾸는가?

---

## P2 — Game Dev Tycoon

### 강화 대상
- Focused Job Fantasy
- Policy / strategy
- Content variety vs same decisions

### Research Questions
- 추상화된 경영이 어떤 minimum state로도 Management fantasy를 유지하는가?

---

# 15. Promotion Table

| ID | Name | Decision | Status | Confidence |
|---|---|---|---|---|
| GC-MGMT-001 | Priority Conflict | STRENGTHEN | **PROVISIONAL CORE** | VERY HIGH |
| GC-MGMT-002 | Loss Needs Recovery Structure | STRENGTHEN | **PROVISIONAL CORE** | HIGH |
| GC-MGMT-003 | Automation Removes Execution, not Decisions | KEEP | CANDIDATE | MEDIUM |
| GC-MGMT-004 | Persistent State Must Reprioritize | NEW | **PROVISIONAL CORE** | HIGH |
| GC-MGMT-005 | Future Pressure vs Present Efficiency | NEW | **PROVISIONAL CORE** | HIGH |
| GC-MGMT-006 | Routine Must Be Recontextualized | NEW | **PROVISIONAL CORE** | HIGH |
| GC-MGMT-007 | Information Supports Diagnosis / Priority | NEW | **PROVISIONAL CORE** | HIGH |
| GC-MGMT-008 | Growth Transforms Constraints | NEW | **PROVISIONAL CORE** | HIGH |
| GC-MGMT-009 | Crisis Tests Existing Management State | NEW | **PROVISIONAL CORE** | HIGH |
| GC-MGMT-010 | Death Spiral Intervention Window | SPLIT | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-MGMT-011 | Bottleneck vs Resource Scarcity | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-MGMT-012 | Structural Policy | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-MGMT-013 | Target Growth vs Workload | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-MGMT-014 | Micromanagement vs Responsibility Level | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-MGMT-015 | Stable / Crisis Pacing | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-MGMT-016 | Scarcity Should Create Alternatives | MERGE | **MERGED INTO GC-MGMT-001 SUB-RULE** | MEDIUM-HIGH |

---

# 16. Management Reviewer Default Set

신규 Management 기획을 검토할 때 우선 적용할 15개 질문.

## Q1 — Management Inclusion

> **플레이어는 State를 읽고 Priority를 정해 Limited Capacity를 배분한 뒤 결과 때문에 다시 Priority를 바꾸는가?**

---

## Q2 — Priority Conflict

> **동시에 해결할 수 없는 문제가 실제로 존재하며 상황에 따라 최우선 문제가 달라지는가?**

관련:
`GC-MGMT-001`

---

## Q3 — Scarcity Quality

> **Resource 부족은 실제 선택을 만드는가, 아니면 기다리거나 같은 행동을 반복하게 할 뿐인가?**

관련:
`GC-MGMT-001 / GC-MGMT-016`

---

## Q4 — Persistent Consequence

> **현재 손실·상태가 다음 Assignment / Resource / Priority를 실제로 바꾸는가?**

관련:
`GC-MGMT-004`

---

## Q5 — Recovery

> **손실 후 복구·대체·철수·우회 중 어떤 Management Decision이 생기는가?**

관련:
`GC-MGMT-002`

---

## Q6 — Death Spiral

> **연쇄 손실을 플레이어가 알아차리고 개입할 Window가 있는가?**

관련:
`GC-MGMT-010`

---

## Q7 — Future Pressure

> **미래 위협 / 수요 때문에 현재 소비와 비축 사이에 실제 갈등이 발생하는가?**

관련:
`GC-MGMT-005`

---

## Q8 — Routine

> **반복 Verb는 새로운 Context에서 다른 판단을 요구하는가, 아니면 같은 명령을 다시 입력하는가?**

관련:
`GC-MGMT-006`

---

## Q9 — Information

> **Dashboard / Alert / Forecast 정보가 실제 Diagnosis와 Priority 변경에 사용되는가?**

관련:
`GC-MGMT-007`

---

## Q10 — Growth

> **성장 후에도 새로운 Trade-off가 남는가, 아니면 모든 Resource가 넘치며 Management가 사라지는가?**

관련:
`GC-MGMT-008`

---

## Q11 — Crisis

> **Crisis는 평소 Management 상태와 준비를 시험하는가, 별도 Mini-game으로 분리되어 있는가?**

관련:
`GC-MGMT-009`

---

## Q12 — Automation

> **Automation은 반복 Execution을 줄이는가, 핵심 Priority Decision까지 대신하는가?**

관련:
`GC-MGMT-003`

---

## Q13 — Management Target Growth

> **직원·시설·지역 수 증가는 새로운 Decision을 만드는가, 동일 Workload만 증가시키는가?**

관련:
`GC-MGMT-013`

---

## Q14 — Job Fantasy / Control Level

> **현재 Micromanagement 수준은 플레이어가 맡은 역할의 책임 수준과 일치하는가?**

관련:
`GC-MGMT-014`

---

## Q15 — Machine vs Human Evidence

> **Resource·Allocation·Snowball은 AI Tester로 측정하고, Fun·Control Feeling·Fatigue·Job Fantasy는 Human Test로 분리했는가?**

---

# 17. Default Metric Bundle

Metric은 Criteria가 아니다.

게임별 Threshold는 Validation Planner가 별도로 확정한다.

## Structural — Machine

- Concurrent Critical Problems
- Priority Switching Rate
- Action Allocation Distribution
- Dominant Priority Rate
- Problem Neglect Duration
- Resource Starvation Rate
- Resource Overflow Rate
- Reserve Level
- Source / Sink Balance
- Emergency Spend Rate
- Capacity Utilization
- Queue Length
- Bottleneck Duration
- Throughput
- Worker Utilization
- Reassignment Rate
- Injury / Fatigue Rate
- Replacement Rate
- Recovery Option Usage
- Recovery Success Rate
- Time to Recovery
- Unrecoverable State Rate
- Snowball Rate
- Death Spiral Frequency
- Net Resource Trend
- Upkeep Burden
- Growth Rate
- Insolvency Rate
- Crisis Frequency
- Response Time
- Crisis Resource Cost
- Cascading Failure Count
- Pre-crisis Preparation Rate
- Alert → Action Rate
- Ignored Alert Rate
- Forecast Usage
- Manual Action Reduction
- Automation Override Rate
- Strategy Concentration
- Policy Concentration
- Context-specific Strategy Shift

## Human

- Priority Tension
- Perceived Control
- Recovery Legibility
- Information Readability
- Administrative Fatigue
- Crisis Fairness
- Job Fantasy
- Consequence Ownership
- Micromanagement Relevance
- Character Attachment

## Hybrid

- Failure Cause Distribution
- State Diagnosis Accuracy
- Crisis Pacing
- Stability / Pressure Pacing
- Recovery Quality
- Snowball Severity
- Growth Satisfaction
- Information Overload
- Management Tension
- Last Meaningful Policy Change
- Last Meaningful Priority Change

---

# 18. Self-Review Result

## Check 1 — Simulation ≠ Management
**PASS**

Simulation complexity 자체를 Management Core로 올리지 않았다.

## Check 2 — Resource Count ≠ Management Depth
**PASS**

Meter / Resource 증가를 Anti-Pattern으로 분리했다.

## Check 3 — Scarcity ≠ Meaningful Choice
**PASS**

Scarcity가 Priority Conflict / Alternative Response를 만드는 경우만 가치가 있다고 정리했다.

## Check 4 — Universal Core 중복
**PASS**

Persistent Consequence, Information, Routine은 각각 UC의 Management 특수화로 Origin을 표시했다.

## Check 5 — Solo Scope Rule contamination
**PASS**

Entity / UI / QA 비용은 Scale Handoff로 분리했다.

## Check 6 — Subtype overgeneralization
**PASS WITH GAPS**

Bottleneck / Policy / Automation 등 Subtype 의존성이 큰 항목은 Candidate 유지.

## Check 7 — Permanent Loss mandatory
**PASS**

Permanent Loss는 장르 필수 요소로 만들지 않았다.

## Check 8 — Optimization vs Story Generator
**PASS**

Mini Metro와 RimWorld의 Product Promise를 Conflict로 분리했다.

## Check 9 — AI Metric → Human Experience
**PASS**

Perceived Control / Fatigue / Job Fantasy / Fairness는 Human 또는 Hybrid로 분류했다.

## Check 10 — Metric ≠ Criteria
**PASS**

Threshold를 만들지 않았다.

## Check 11 — Automation always good
**PASS**

Automation은 Candidate이고 Agency Loss Anti-Pattern도 별도 유지했다.

## Check 12 — Target Growth ≠ Depth
**PASS**

Entity 증가와 Decision 증가를 분리했다.

## Check 13 — Counter Evidence
**PASS**

Sandbox / Story Generator / Reset-based 구조 등의 Boundary를 보존했다.

## Check 14 — Reviewer usability
**PASS**

최종 15개 Reviewer Default Question으로 압축했다.

---

# 19. Final Position

현재 Studio OS Management Knowledge Base에서 우선 `Provisional Core`로 사용할 항목은 다음 8개다.

1. `GC-MGMT-001 — Priority Conflict`
2. `GC-MGMT-002 — Loss Needs Recovery Structure`
3. `GC-MGMT-004 — Persistent State Must Reprioritize`
4. `GC-MGMT-005 — Future Pressure Must Compete with Present Efficiency`
5. `GC-MGMT-006 — Routine Must Be Recontextualized`
6. `GC-MGMT-007 — Information Must Support Diagnosis and Priority`
7. `GC-MGMT-008 — Growth Must Transform Constraints, not Erase Management`
8. `GC-MGMT-009 — Crisis Should Test the Existing Management State`

Candidate는 다음과 같다.

- `GC-MGMT-003 — Automation`
- `GC-MGMT-010 — Death Spiral Intervention`
- `GC-MGMT-011 — Bottleneck vs Scarcity`
- `GC-MGMT-012 — Structural Policy`
- `GC-MGMT-013 — Target Growth vs Workload`
- `GC-MGMT-014 — Micromanagement vs Responsibility`
- `GC-MGMT-015 — Stable / Crisis Pacing`

`GC-MGMT-016 — Scarcity Should Create Alternatives`는 별도 Core에서 제거하고 `GC-MGMT-001 Priority Conflict`의 Sub-rule로 **병합 확정**한다.

현재 가장 중요한 Evidence Gap은:

> **Priority Switching / Automation / Death Spiral / Administrative Fatigue / Management UI behavior / Target Growth**

이다.

따라서 다음 Reference 확장은 “유명한 경영게임을 더 많이 추가”하는 방식보다:

> **Automation이 언제 Agency를 제거하는가?  
> Death Spiral은 어디서 Recoverable → Unrecoverable로 넘어가는가?  
> Entity 수 증가는 언제 새로운 Decision이고 언제 Workload인가?  
> Management UI에서 어떤 정보가 실제 행동을 바꾸는가?**

에 실제 Telemetry 또는 개발자 Postmortem이 존재하는 사례를 우선 조사하는 편이 효율적이다.

---

# 20. Source Trace

## Primary Management Evidence
- REF-01 — Papers, Please
- REF-06 — Darkest Dungeon
- REF-07 — Against the Storm
- REF-08 — Frostpunk
- REF-13 — RimWorld
- REF-14 — Mini Metro
- REF-15 — This War of Mine

## Secondary / Hybrid
- REF-02 — FTL
- REF-18 — Loop Hero
- REF-19 — Cultist Simulator
- REF-22 — Stacklands
- REF-23 — Citizen Sleeper

## Adjacent / Control
- REF-09 — Reigns
- REF-03 — Into the Breach
- REF-10 — 80 Days
- REF-24 — Dorfromantik
- REF-12 — Vampire Survivors

## Baseline
- STUDIO_CORE_CANDIDATES_v0.2
- Studio OS — Evidence-Based Core Extraction Master Prompt v0.2
- Studio OS — Management Genre Core Deep Extraction Prompt v0.1

---

# 21. Traceability Rule

Core는 원본 Reference를 대체하지 않는다.

신규 프로젝트 Review에서 Core가 위험 신호를 발생시키면:

```text
Core
↓
Primary Reference
↓
Design Problem
↓
Reference Solution
↓
Context
↓
Trade-off
↓
Current Project Applicability
```

순서로 다시 내려가 확인한다.

`MANAGEMENT_CORE_CANDIDATES_v0.1`은 Studio OS Reviewer가 원본 Case Study를 더 빠르고 일관되게 호출하기 위한 압축된 Genre 판단 계층이다.
