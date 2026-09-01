# REVIEWER_RUNTIME_SPECIFICATION_v0.1

**Studio OS — Design Reviewer Runtime Specification**  
**Status:** `APPROVED_AS_REVIEWER_RUNTIME_BASELINE`  
**Runtime Version:** `REVIEWER_RUNTIME_v0.1`  
**Purpose:** `Evidence-based Project Review / Dynamic Rule Loading / Root-risk Deduplication / Validation-Need Classification`  
**Studio Core:** `Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`  
**Genre Master:** `GENRE_CORE_MASTER_INDEX_v0.3.md`  
**Scale Baseline:** `SCALE_CORE_BASELINE_v0.2.md`  
**Active Independent GSC:** `0`  
**Next:** `Reviewer Runtime Dry-run #1`

---

# 1. Executive Summary

`REVIEWER_RUNTIME_SPECIFICATION_v0.1`은 Studio OS의 Canonical Knowledge를 실제 신규 게임 기획에 적용하기 위한 실행 규격이다.

이번 Runtime은 새로운 Core를 연구하지 않는다.

현재 Canonical Knowledge:

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
```

를 실제 Project 문서에 대해 다음처럼 실행한다.

```text
Project Documents
↓
Input Integrity
↓
Project Mechanism Extraction
↓
Product Promise / Claim Registry
↓
Universal Applicability
↓
Genre Routing
↓
Universal Parent → Genre Specialization
↓
Hybrid Resolver
↓
Scale Routing
↓
Relevant Scale Handoff
↓
Market / Selection when applicable
↓
Raw Findings
↓
Root Cause Merge / Split
↓
RF Findings
↓
Severity / Evidence Classification
↓
Structural Fix
or
VALIDATION_REQUIRED
↓
Evidence-based Design Review
```

핵심 원칙은 다음과 같다.

1. **Mechanism-first.**
   - Genre Tag부터 선택하지 않는다.
   - Player Verb / State / Decision / Loop / Product Promise를 먼저 구조화한다.

2. **Product Promise-first.**
   - 같은 Mechanism도 Product Promise에 따라 Applicability와 Risk가 달라진다.
   - Replay / Power Fantasy / Deduction / Reactive Narrative 등 Promise를 먼저 명시한다.

3. **Universal은 Applicability Gate를 통과한 것만 Load한다.**
   - Default candidate pool은 `UC001~005`.
   - `UC006`은 Progression이 핵심 Promise일 때만 `CONDITIONAL DIAGNOSTIC`.

4. **Genre는 L0~L3 Mechanism Contribution으로 Routing한다.**
   - Tag가 아니라 Core Loop / Verb / State / Decision / Promise 기여도를 본다.

5. **Candidate는 실제 Finding을 만들 수 있다.**
   - 다만 Knowledge Status를 `CANDIDATE`로 Trace한다.
   - Candidate Confidence와 Project Severity를 혼동하지 않는다.

6. **Scale / Content / Budget을 분리한다.**
   - Team Scale은 Production Capacity 정보다.
   - Content Scope와 동일하지 않다.
   - Solo Core를 Micro / Small / Mid+에 자동 적용하지 않는다.

7. **Handoff는 Core가 아니다.**
   - 51개 전체를 Load하지 않는다.
   - 현재 Genre + Mechanism에 관련된 Production Risk만 Routing한다.

8. **Active GSC는 현재 `0`.**
   - Retired GSC 3개는 Historical Trace일 뿐 Finding Source로 사용하지 않는다.
   - Routing Specialization 2개는 Reviewer Action Hint이며 Severity Source가 아니다.

9. **Core 하나 = Finding 하나가 아니다.**
   - Universal / Genre / Scale / Handoff의 여러 Raw Finding이 동일 Root Mechanism을 가리키면 하나의 `RF-*`로 Merge한다.

10. **세 축을 반드시 분리한다.**

```text
Knowledge Confidence
≠
Project Evidence Strength
≠
Issue Severity
```

11. **UNKNOWN은 FAIL이 아니다.**
   - 정보가 없으면 `NEEDS_INFO`.
   - 현재 확인된 사실과 Unknown이 막는 판단을 함께 기록한다.

12. **Reviewer는 재미를 가정하지 않는다.**
   - Tension / Fairness / Readability / Feel / Identity / Fatigue 같은 Experience Claim은 필요 시 `VALIDATION_REQUIRED`.

13. **Reviewer는 Validation Plan을 만들지 않는다.**
   - 허용:

```text
VALIDATION_REQUIRED
+
Claim
+
Suggested Evidence Type
```

   - 금지:
     - Test 횟수
     - Persona 세부값
     - Pass/Fail Threshold
     - Seed
     - Sample Size
     - AI Tester implementation

14. **Reviewer는 Project Kill / Investment Decision을 하지 않는다.**
   - `PROCEED / ITERATE / PIVOT / KILL` 금지.
   - 사용자-facing Verdict는 Review 상태만 표현한다.

15. Runtime은 다음 5개의 사용자-facing Review Verdict만 사용한다.

```text
REVIEW_CLEAR
REVIEW_CLEAR_WITH_VALIDATION
REVISION_REQUIRED
STRUCTURAL_RISK
INSUFFICIENT_SPEC
```

16. Reviewer Runtime v0.1은 Canonical Knowledge를 실제 프로젝트에 적용할 **Dry-run 준비 완료 상태**를 목표로 한다.
   - 다음 단계는 Dry-run #1.
   - Validation Planner는 현재 필수 Next Step이 아니다.

---

# 2. Reviewer Runtime Purpose

Reviewer Runtime의 목적은:

> **현재 프로젝트에 필요한 Evidence-Based Knowledge만 동적으로 호출하고, 기획서에서 관찰 가능한 문제를 Root Cause 수준으로 압축하여 수정 / 보존 / 추가 정보 / Validation 필요 상태를 분리하는 것**

이다.

Reviewer는 다음을 수행한다.

1. Project 문서 정합성 확인.
2. Mechanism 구조화.
3. Product Promise 추출.
4. Design / Experience / Production / Market / Selection Claim 분류.
5. Universal Applicability 판정.
6. Genre / Hybrid Routing.
7. Scale / Handoff Routing.
8. Dynamic Reviewer Question 생성.
9. Raw Finding 수집.
10. Root Issue Merge / Split.
11. Severity / Knowledge Confidence / Project Evidence Strength 분리.
12. Structural Fix vs Validation Need 분리.
13. 강한 구조를 `SUPPORTED_STRUCTURE`로 보존.
14. Evidence Boundary / Unknown 명시.
15. 최종 Review Summary 생성.

Reviewer의 핵심 산출물은:

```text
많은 Core Violation
```

이 아니라:

```text
적은 수의 중요한 Root Issue
+
보호해야 할 Supported Structure
+
검증이 필요한 Claim
```

이다.

---

# 3. Studio OS Core Boundary

현재 Studio OS Core의 본체:

```text
Reference / Evidence
↓
Universal / Genre / Scale Knowledge
↓
Reviewer Runtime
↓
Evidence-based Design Review
↓
기획 수정 / 유지 / 보류 판단 지원
```

현재 Validation은 **Optional downstream layer**다.

Reviewer가 Validation에 대해 할 수 있는 일:

```text
무엇이 아직 증명되지 않았는가?
무슨 Claim을 확인해야 하는가?
어떤 종류의 Evidence가 적합한가?
```

까지.

Reviewer Runtime 완료 후 정상 순서:

```text
Reviewer Runtime Specification
↓
Reviewer Runtime Dry-run #1
↓
Reviewer Runtime Dry-run #2
↓
Runtime Correction / Consolidation
↓
Reviewer Runtime v1.0
↓
Studio OS Canonical Document Manifest
↓
Studio OS Core Package v1.0
```

Optional Validation Planner / AI Tester는 현재 Core Package 완성의 필수 선행 단계가 아니다.

---

# 4. Canonical Dependencies

## Runtime Source Priority

### Level 1 — Universal / Studio Core

`Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`

Canonical Runtime:

```text
Universal Provisional:
UC-DESIGN-001~005

Universal Candidate:
UC-DESIGN-006

Universal Default Pool:
UC001~005

Universal Conditional:
UC006
```

### Level 2 — Genre Router / Parent Map

`GENRE_CORE_MASTER_INDEX_v0.3.md`

사용:
- Mechanism-first Routing
- L0~L3
- Universal Parent Mapping
- Genre specialization
- Candidate loading
- Hybrid interaction
- Parent / Child dedup
- Handoff registry
- Evidence Boundary

### Level 3 — Scale Router

`SCALE_CORE_BASELINE_v0.2.md`

사용:
- Scale taxonomy
- ownership / FTE / parallel lane
- 12 Production Cost Axes
- Cost Shape
- Externalization
- Internal Ownership
- 51 Scale Handoff
- Routing Specialization
- Solo / Micro / Small / Mid+ evidence boundary

### Level 4 — Approved Genre Baselines

상세 Rule / Boundary / Evidence가 필요할 때 개별 Genre Source로 내려간다.

### Level 5 — Historical Decision Sources

- `UNIVERSAL_CORE_CONSOLIDATION_v0.1_APPROVED.md`
- `UNIVERSAL_CANONICAL_SYNC_v0.1.md`
- `GENRE_SCALE_CORE_INTEGRATION_v0.1_APPROVED.md`
- `GSC_CANONICAL_CONSOLIDATION_v0.1.md`

역할:
`Historical Trace only`.

최신 Runtime Canonical Source보다 우선하지 않는다.

---

# 5. Runtime Responsibilities / Non-responsibilities

## Reviewer Responsibilities

- Mechanism interpretation
- Project source reconciliation
- Product Promise extraction
- Core Applicability
- Genre / Scale Routing
- Root cause synthesis
- project-specific reviewer question generation
- design / production / market category separation
- issue prioritization
- supported structure preservation
- validation need tagging

## Reviewer Non-responsibilities

다음은 하지 않는다.

### A. 기획서에 없는 기능 생성

```text
Unknown
→ Unknown
```

### B. Test Result Fabrication

- AI 결과 상상
- Human 반응 상상
- Win Rate 상상
- simulated play 결과 상상

### C. Numerical Success Prediction

```text
Success probability = 75%
```

금지.

### D. Final Investment / Kill Decision

```text
PROCEED
ITERATE
PIVOT
KILL
```

금지.

### E. Validation Plan Construction

다음은 별도 Layer:

- Test count
- Persona definitions
- Threshold
- Seed
- Sample size
- exact test matrix
- AI Tester implementation

### F. Genre Reclassification by Impression

Genre Tag가 비슷하다는 이유로 Core를 Load하지 않는다.

---

# 6. Input Contract

```text
PROJECT_REVIEW_INPUT

Project Name:
Project Version:

Concept:
Player Fantasy:
Target Platform:
Target Audience:

Core Loop:
Secondary Loops:

Player Verbs:
Persistent States:
Resources:
Progression:
Failure / Success:

Content Structure:
Session Structure:
Replay Structure:

Genre Claims:
Scale / Team:
External Support:
AI-assisted Production:

Market Goal:
Selection / Award Goal:

Known Constraints:
Known Risks:

Current Development Stage:
- CONCEPT
- PAPER PROTOTYPE
- CONCEPT TEST MODEL
- DIGITAL PROTOTYPE
- VERTICAL SLICE
- PRODUCTION
- PRE-LAUNCH

Attached Documents:
- ...

Locked Decisions:
- ...

Deprecated / Superseded Documents:
- ...
```

모든 Field가 채워져 있을 필요는 없다.

Runtime은 Missing Field를 자동 생성하지 않는다.

---

# 7. Missing Information Policy

모든 Project 정보는 세 상태 중 하나다.

```text
KNOWN
INFERRED
UNKNOWN
```

## KNOWN

Project Source에 직접 명시.

Trace:
- Document
- Version
- Section / quote position if available

## INFERRED

현재 구조에서 높은 가능성으로 추론되지만 직접 명시되지 않음.

필수 표기:

```text
Evidence State:
INFERRED
```

Inference는 Finding의 `Project Evidence Strength`를 자동 CONFIRMED로 만들 수 없다.

## UNKNOWN

판정에 필요한 정보가 없음.

원칙:

```text
UNKNOWN
≠
FAIL
```

UNKNOWN 때문에 핵심 판단이 막히면:

`NEEDS_INFO`.

---

# 8. Input Integrity

## PASS 0 — Input Integrity

먼저 확인:

1. 현재 Project Version은 무엇인가?
2. 최신 승인 문서가 무엇인가?
3. 서로 다른 Version이 섞였는가?
4. Locked Decision과 Draft가 충돌하는가?
5. Deprecated Rule이 살아 있는가?
6. Resource / State / Turn / Save / Failure 정의가 문서 간 충돌하는가?

## Source Priority

```text
1. Current approved project document
2. Current locked project decision
3. Earlier project document
4. Reviewer inference
```

## INTERNAL_CONSISTENCY Candidate

명백한 충돌은 Reference Core 없이도 Finding 가능.

예:

```text
GDD A:
부상은 Run 종료 시 초기화.

System Spec:
부상은 캠페인 동안 지속.
```

이 경우 Runtime은 먼저 Conflict를 기록하고, 어느 Rule을 Active로 가정할지 임의 결정하지 않는다.

---

# 9. Project Mechanism Profile

## PASS 1 — Project Mechanism Extraction

Genre를 선택하기 전에 다음을 작성한다.

```text
PROJECT_MECHANISM_PROFILE

Project:

Core Player Fantasy:

Primary Player Verbs:
- ...

Secondary Player Verbs:
- ...

Core Loop:
Loop Unit:
Loop Reset:

Decision Types:
- Resource
- Position
- Timing
- Build
- Information
- Risk
- Narrative
- Other

Persistent States:
- ...

Temporary States:
- ...

Main Resources:
- ...

Failure Structure:
- ...

Recovery Structure:
- ...

Progression Structure:
- ...

Information Structure:
- ...

Content Unit:
- ...

System Dependencies:
- ...

Production-heavy Areas:
- ...

Product Promises:
- ...
```

## Mechanism-first Rule

좋지 않은 Runtime:

```text
"Deckbuilder다"
→ Deck Rule 전체 Load
```

올바른 Runtime:

```text
Card draw
+
Build commitment
+
Run reset
+
Context-dependent reward
↓
Deck / Roguelike Contribution 계산
```

---

# 10. Product Promise / Claim Registry

## PASS 2 — Product Promise / Claim Registry

## Product Promise Extraction Timing

Product Promise는:

```text
Mechanism Profile 직후
Universal Applicability 전에
```

추출한다.

예:

- Replay Variety
- Strategic Planning
- Power Fantasy
- Player-owned Deduction
- Reactive Narrative
- Fast Action Feel
- Management Pressure
- Build Expression

## Claim Type Separation

### DESIGN CLAIM

> 매 Run 다른 전략이 필요하다.

### EXPERIENCE CLAIM

> 선택이 긴장감 있다.

### PRODUCTION CLAIM

> 데이터 중심이라 콘텐츠 제작비가 낮다.

### MARKET CLAIM

> 스트리머 친화적이다.

### SELECTION CLAIM

> 공모전에서 한 문장으로 설명 가능하다.

## Feature ≠ Claim Proven

```text
랜덤 이벤트 20개
≠
매 Run 다른 전략이 필요함이 증명됨
```

## PROJECT_CLAIM_REGISTRY

```text
CLAIM-ID:
Claim:

Claim Type:
- DESIGN
- EXPERIENCE
- PRODUCTION
- MARKET
- SELECTION

Source:

Current Support:

Evidence State:
- KNOWN
- INFERRED
- UNKNOWN

Status:
- STRUCTURALLY SUPPORTED
- PARTIALLY SUPPORTED
- UNSUPPORTED
- UNKNOWN
- VALIDATION_REQUIRED

Validation Needed:
YES / NO

Suggested Evidence Type:
- SIMPLE MODEL
- SELF TEST
- HUMAN TEST
- AI TESTER
- MARKET TEST
- HYBRID
- NONE
```

---

# 11. Universal Applicability

## PASS 3 — Universal Applicability

Default Pool:

- `UC-DESIGN-001`
- `UC-DESIGN-002`
- `UC-DESIGN-003`
- `UC-DESIGN-004`
- `UC-DESIGN-005`

각 Core:

```text
UNIVERSAL_APPLICABILITY

Core:
Applicability:
- YES
- CONDITIONAL
- N/A

Why:
Relevant Mechanism:
Relevant Product Promise:
Project Evidence:
```

## UC001

적용 질문:

> 입력 / 기능 수보다 실제 다른 Consequence와 Decision이 존재하는가?

보통 적용 가능하나 pure execution mastery에서는 질문 방향을 조정한다.

## UC002

Replay / repeated decision / systemic variation이 Promise일 때 강하게 적용.

One-shot authored product에는:

`CONDITIONAL / N/A`.

## UC003

Persistent State / delayed consequence가 실제 존재할 때 적용.

```text
State exists
≠
Meaningful consequence
```

## UC004

Meaningful uncertainty가 있을 때 적용.

Deterministic threat cue는 UC005 쪽.

## UC005

Decision-time information / Outcome-time learning이 필요한 시스템에 적용.

Deduction inference ownership은 UC005로 대체하지 않는다.

## UC006 — Conditional Universal

```text
Progression Promise?
NO → N/A
YES → CONDITIONAL DIAGNOSTIC
```

Knowledge Status:

`CANDIDATE`.

---

# 12. Genre Routing Runtime

## PASS 4 — Genre Routing

Mechanism Contribution Axes:

1. Core Loop Dependency
2. Player Verb Dependency
3. State Dependency
4. Decision Dependency
5. Product Promise Dependency

각 `0~2`.

```text
0~2  → L0
3~5  → L1
6~8  → L2
9~10 → L3
```

Score는 Routing Aid이며 Mechanism 설명이 필수다.

## PROJECT_GENRE_ROUTING_PROFILE

```text
PROJECT_GENRE_ROUTING_PROFILE

Primary:
- Genre:
  Level:
  Score:
  Why Loaded:
  Player Verb:
  State:
  Core Loop:
  Product Promise:

Secondary:
- ...

Supporting:
- ...

Not Loaded:
- ...

Hybrid Interaction:
- ...

Evidence Boundary:
- ...

HYBRID_SCOPE_WARNING:
YES / NO
```

## Loading Behavior

### L3

- Provisional → `ACTIVE CHECK`
- High / Very High Candidate → `WATCH`
- Medium Candidate → known Risk Signal 있을 때만

### L2

- applicable Provisional → `ACTIVE CHECK`
- Candidate → known Risk Signal 있을 때만

### L1

2~4개 선택 질문.

### L0

로드 금지.

## Candidate Runtime Rule

Candidate는 Finding을 생성할 수 있다.

Finding에:

```text
Knowledge Status:
CANDIDATE
```

를 표시한다.

Candidate라고 Severity가 자동 LOW가 아니다.

---

# 13. Hybrid Resolver

## PASS 5 — Universal Parent → Genre Specialization

Universal Parent와 Genre Child가 같은 Root Mechanism을 가리키면:

```text
Universal Parent
↓
Genre Specialization
```

으로 묶고, Parent는 Root Issue를 소유하며 Child는 Genre-specific residual / reviewer action을 추가한다.

별도 Severity를 중복 생성하지 않는다.

## PASS 6 — Hybrid Resolver

둘 이상의 Primary / Secondary Genre가 있으면:

- Shared Verb
- Shared State
- Shared Consequence

를 먼저 찾는다.

## Hybrid Interaction Types

```text
TYPE-A Reinforcing
TYPE-B Sequential
TYPE-C Conditional
TYPE-D Competing
TYPE-E Cosmetic
```

## HYBRID_CONFLICT

```text
HYBRID_CONFLICT

Genres:

Interaction Type:

Shared Verb:
Shared State:
Shared Consequence:

Conflict:

Hidden Variable:

Product Promise at Risk:

Evidence:

Severity:

Reviewer Question:

Validation Needed:
YES / NO
```

## Hybrid Double-Penalty Rule

예:

```text
UC003
+
GC-MGMT-004
+
GC-SIM-002
```

가 같은 Persistent State Root를 설명한다면:

`ONE RF`.

Management child:
- allocation reprioritization

Simulation child:
- causal propagation

을 diagnostic residual로 붙인다.

---

# 14. Scale Routing Runtime

## PASS 7 — Scale Routing

Team Scale은 Content Scope나 Budget과 동일하지 않다.

```text
Team Scale
≠
Content Scope
≠
Budget
```

## PROJECT_SCALE_ROUTING_PROFILE

```text
PROJECT_SCALE_ROUTING_PROFILE

Core Team:
- Headcount:
- Sustained FTE:
- Core Ownership Domains:
  - Design:
  - Programming:
  - Art:
  - Content:
  - Production:

Scale:
- SOLO
- MICRO
- SMALL
- MID+

Embedded Contributors:
- ...

External Support:
- Art:
- Animation:
- UI:
- Audio:
- QA:
- Localization:
- Porting:
- Other:

AI-assisted Work:
- Code:
- Art:
- Writing:
- QA:
- Documentation:
- Other:

Critical Single-owner Domains:
- ...

Parallel Production Lanes:
- Current:
- Sustainable:
- Blocked by Dependencies:

Specialist Dependencies:
- ...

Integration / Review Ownership:
- ...

Evidence Boundary:
- Supported Scale:
- Unsupported Inference:
```

## Scale Loading

### SOLO

`SC-SOLO-001~004` applicability check.

### MICRO

`SC-MICRO-001` diagnostic.

Solo Core 자동 적용 금지.

### SMALL / MID+

`EVIDENCE_BOUNDARY_SCALE`.

Generic Production Cost Axis / Handoff는 사용할 수 있으나 Solo/Micro Rule을 extrapolate하지 않는다.

## Production Cost Axis

필요한 것만 검사한다.

1. Unique Asset
2. Animation
3. Hand-authored Content
4. Logic Dependency
5. State Combination / QA
6. Balance
7. UI / UX
8. Localization
9. Tooling
10. AI / Agent
11. Technical / Performance
12. Audio / VFX

## Cost Shape

```text
LINEAR
SUBLINEAR / REUSABLE
MULTIPLICATIVE
THRESHOLD
SPECIALIST-GATED
ITERATION-HEAVY
UNKNOWN
```

---

## Outsourcing Guardrail

```text
Externalizable
≠
Cost Removed
```

외주 / 서비스 지원이 있으면 다음 Internal Ownership을 별도로 본다.

- specification
- communication
- revision
- integration
- acceptance QA
- regression ownership

External Production Unit이 분리되어도 Core Team의 integration burden이 남을 수 있다.

## AI-assisted Production Guardrail

```text
AI-assisted Work
≠
Independent Human Owner
≠
Core Team Headcount Increase
```

AI는 `PRODUCTIVITY_MODIFIER`로만 기록한다.

근거 없이:

```text
AI = 0.5 developer
AI = productivity ×2
```

같은 수치를 만들지 않는다.


# 15. Scale Handoff Runtime

## PASS 8 — Relevant Scale Handoff

51개 전체 자동 Load 금지.

Routing 조건:

```text
Active Genre
+
Actual Project Mechanism
+
Observed / plausible Production Driver
```

가 모두 연결될 때만 Handoff를 Reviewer Set에 넣는다.

## Handoff Runtime Role

```text
Core:
NO

Production Risk Routing:
YES

Severity Source by itself:
NO
```

Handoff는:
- hidden cost driver
- cost shape
- internal ownership
- externalization boundary
- QA multiplication
을 구체화한다.

## GSC Runtime

```text
Active Independent GSC:
0
```

따라서 정상 Runtime:

```text
Optional GSC Registry Check
→ NONE
```

Retired:
- `GSC-DECK-SOLO-001`
- `GSC-MGMT-SOLO-001`
- `GSC-DEDUCT-SOLO-001`

는 Historical Trace만 허용.

## Routing Specialization

### Management × Solo
`Responsibility Level as Scope Cut Boundary`

### Action × Solo
`Iteration Throughput / Feel Polish Budgeting`

둘 다:
- Core 아님
- Severity Source 아님
- Reviewer Action Hint.

---

# 16. Market / Selection Routing

## PASS 9 — Market / Selection when applicable

Market / Selection은 Goal이 있을 때만 Load한다.

## Market

주요 Parent:

- `MC-001 — Funnel Separation`
- `MC-002 — Sales ≠ ROI`
- `MC-003 — Downside Compatibility`
- `MC-004 — Satisfaction ≠ Audience`

## MARKET_FINDING

```text
MARKET_FINDING

Claim:
Market Core:

Known Evidence:
Unknown Evidence:

Risk:

Severity:

Evidence Needed:

Design Fix Needed:
- YES
- NO
- UNKNOWN
```

Market Risk와 Design Failure를 합치지 않는다.

## Selection

지원사업 / 전시 / 공모전 / 대회 목표가 있을 때만.

- `SEL-001`
- `SEL-002`
- `SEL-003`

Award Fit와 Market Fit를 분리한다.

---

# 17. Reviewer Set Construction

Dynamic Reviewer Set의 목적:

> Core 문장을 복사하는 것이 아니라 Project Mechanism에 맞는 질문으로 변환하는 것.

## PROJECT_REVIEWER_SET

```text
PROJECT_REVIEWER_SET

Project:

Universal:
- Core:
  Applicability:
  Question:

Primary Genre:
- Core:
  Status:
  Question:

Secondary Genre:
- ...

Hybrid:
- ...

Scale:
- ...

Handoffs:
- ...

Market:
- ...

Selection:
- ...

Conditional Diagnostics:
- ...

Excluded / N/A:
- ...

Merged Questions:
- Parent:
  Children:
  Final Question:

Evidence Boundary Warnings:
- ...
```

## Reviewer Question Budget

```text
Universal:
max 5 + UC006 conditional

Primary Genre:
5~8 each

Secondary Genre:
2~4 each

Scale:
3~8 depending risk

Market / Selection:
only when applicable
```

Dedup 후 Final Question 수를 줄인다.

## Question Quality Rule

좋은 질문:

> 현재 부상이 다음 파견 인력 선택을 실제로 바꾸는가?

나쁜 질문:

> Persistent State가 있는가?

좋은 질문 구조:

```text
Mechanism
+
Project-specific State
+
Decision Consequence
```

---

## Reviewer Runtime Default Questions

1. 이 Project의 핵심 Product Promise는 무엇인가?
2. 플레이어가 반복하는 실제 Verb는 무엇인가?
3. 그 Verb가 어떤 State를 바꾸는가?
4. 그 결과가 다음 Decision을 바꾸는가?
5. Context가 Choice Value를 바꾸는가?
6. 중요한 Uncertainty에 Response Agency가 있는가?
7. 판단 전 필요한 Information이 Actionable한가?
8. 결과 후 Cause를 학습할 수 있는가?
9. Genre Mechanism이 실제 Core Loop에 존재하는가?
10. Scale 대비 숨은 Production Cost는 무엇인가?
11. 같은 문제가 Parent / Genre / Scale에서 중복되고 있지 않은가?
12. 지금 바로 수정할 문제인가?
13. 아니면 Cheap Test가 필요한 Claim인가?
14. Human Test가 필요한가?
15. 현재 정보로 알 수 없는 것은 무엇인가?

Default Question은 그대로 복사하지 않는다.

항상:

```text
Core
↓
Project Mechanism
↓
Project-specific Reviewer Question
```

으로 변환한다.

## Top Issue Budget

기본 사용자-facing 출력:

```text
Critical:
all

High:
max 5

Medium:
max 8

Low:
appendix / only if useful
```

Issue 수 제한은 문제를 숨기기 위한 것이 아니다.

목적:
- 우선순위 없는 장문 Finding dump 방지
- 같은 Root의 중복 지적 방지
- 사용자 Decision load 관리

## Priority Ordering

1. Product-killing structural issue
2. Core Loop / Product Promise
3. Production completion risk
4. Major hybrid conflict
5. High-uncertainty core claim
6. Medium design issue
7. Polish


# 18. Raw Finding Collection

## PASS 10 — Raw Finding Collection

Core 하나마다 RF를 만들지 않는다.

먼저 내부 Raw Finding을 만든다.

```text
RAW_FINDING

Source Core:
Source Layer:

Trigger:

Observed Project Evidence:

Evidence State:
- KNOWN
- INFERRED
- UNKNOWN

Potential Issue:

Potential Root:

Applicability:

Knowledge Status:
- PROVISIONAL
- CANDIDATE
- ROUTING_HINT
- PROJECT_INTERNAL

Knowledge Confidence:

Needs Validation:
YES / NO
```

Raw Finding은 사용자용 최종 출력이 아니다.

---

# 19. Root Cause Merge / Split

## PASS 11 — Root Cause Merge / Split

```text
SYMPTOM
↓
MECHANISM
↓
ROOT ISSUE
```

## ROOT_ISSUE

```text
ROOT_ISSUE

ID:
RI-###

Title:

Category:
- DESIGN
- PRODUCTION
- HYBRID
- MARKET
- SELECTION
- INTERNAL CONSISTENCY

Affected Product Promise:

Observed Evidence:

Unknowns:

Universal Parent:

Genre Specialization:

Scale Core:

Scale Handoff:

Routing Specialization:

Symptoms:

Mechanism:

Impact:

Severity:

Knowledge Confidence:

Project Evidence Strength:

Recommended Action:

Action Class:
- STRUCTURAL FIX FIRST
- VALIDATE FIRST
- NO ACTION YET

Validation Required:
YES / NO
```

## Root Merge Conditions

두 Raw Finding을 Merge하려면 기본적으로 다음 네 조건을 본다.

1. 같은 underlying mechanism.
2. 같은 Product Promise에 영향.
3. 동일 Design / Production Change로 대부분 해결.
4. 같은 Validation Question을 요구.

대부분 충족하면 하나의 Root.

## Root Split Conditions

증상이 비슷해도 다음이면 분리.

1. Root Cause가 다름.
2. Fix가 다름.
3. Validation Type이 다름.
4. Category가 다름.
5. 한쪽은 Design, 다른 쪽은 Production.

## Example — Deck Content

증상:

```text
Card count high
Balance workload high
Tooltip workload high
Regression matrix high
```

가능한 Production Root:

> Interaction Matrix growth exceeds current production / QA capacity.

하지만 별도 Design Root:

> Card choices are context-invariant.

가 있다면 Merge하지 않는다.

---

# 20. Severity Model

## PASS 12 — Severity / Evidence Classification

Issue Severity는 Project Impact다.

## CRITICAL

- Core Product Promise가 구조적으로 성립하지 않음.
- Core Loop 작동 불가.
- 현 Scope에서 completion 가능성이 심각하게 위협됨.
- 해당 Claim 실패 시 Project 존재 이유가 크게 약화.

## HIGH

- 핵심 재미 / 반복 / 운영 구조 크게 약화.
- 제작 후 큰 재설계 가능성.
- 다음 투자 / 개발 단계 전에 수정 또는 검증 필요.

## MEDIUM

- 품질 / 밸런스 / 흐름 / 제작효율 Risk.
- Core 자체는 무효화하지 않음.

## LOW

- local optimization
- polish
- 후순위 개선

## Severity Guardrail

다음은 금지.

```text
Provisional Core
→ HIGH
```

```text
Candidate
→ LOW
```

```text
3개 Core가 지적
→ Severity 3배
```

---

# 21. Evidence / Confidence Model

반드시 세 축을 분리한다.

## A. Knowledge Confidence

Canonical Knowledge 자체의 Evidence Strength.

```text
VERY HIGH
HIGH
MEDIUM-HIGH
MEDIUM
LOW-MEDIUM
LOW
```

## B. Project Evidence Strength

현재 Project에서 해당 문제의 존재를 얼마나 직접 확인했는가.

```text
CONFIRMED
STRONG
PARTIAL
WEAK
UNKNOWN
```

### CONFIRMED

Current approved Project source가 직접 구조를 명시하며 Root 존재가 논리적으로 확정.

### STRONG

여러 Source / System relation이 같은 문제를 지지.

### PARTIAL

문제 가능성이 높지만 일부 중요 Mechanism은 미명시.

### WEAK

Inference 중심.

### UNKNOWN

핵심 정보 없음.

## C. Issue Severity

Project Impact.

`Knowledge Confidence / Project Evidence / Severity`를 상호 변환하지 않는다.

예:

```text
Knowledge:
MEDIUM candidate

Project Evidence:
CONFIRMED

Severity:
HIGH
```

가능.

반대도 가능.

---

# 22. RF Finding Schema

## PASS 13 — Recommended Action

하나의 Root Issue = 하나의 `RF-*`.

```text
RF-###

Title:

Status:
- OPEN
- NEEDS_INFO
- VALIDATION_REQUIRED
- RESOLVED
- ACCEPTED_RISK

Category:

Severity:

Project Evidence Strength:

Knowledge Status:
- PROVISIONAL
- CANDIDATE
- PROJECT_INTERNAL
- MULTI-SOURCE

Knowledge Confidence:

Affected Promise:

Evidence:
- Project Source:
- Canonical Source:

Root Mechanism:

Universal Parent:

Genre Specialization:

Scale / Handoff:

Routing Specialization:

Why It Matters:

Recommended Action:

Recommendation Type:
- REMOVE
- REDUCE
- MERGE
- REFRAME
- SEPARATE
- ADD RESPONSE PATH
- ADD INFORMATION PATH
- CHANGE DEPENDENCY
- CHANGE SCOPE
- CREATE CHEAP TEST MODEL
- SELF TEST
- HUMAN TEST
- UNITY MICRO PROTOTYPE
- AI TESTER LATER
- MARKET TEST
- ACCEPT RISK
- NO ACTION YET

Action Class:
- STRUCTURAL FIX FIRST
- VALIDATE FIRST
- NO ACTION YET

Validation Need:
- NONE
- VALIDATION_REQUIRED

Suggested Evidence Type:
- SIMPLE MODEL
- SELF TEST
- HUMAN TEST
- AI TESTER
- MARKET TEST
- HYBRID
- NONE

Further Validation Design:
- DEFERRED

Unknowns:

Do Not Infer:
- ...
```

---

## Reviewer Action Is Not Final Implementation

예:

```text
Recommendation Type:
ADD RESPONSE PATH
```

의 의미는:

> 현재 Root Mechanism을 해결하려면 Player Response Agency가 필요할 가능성이 높다.

까지다.

Reviewer가:
- 정확한 Recovery 수치
- Cooldown
- Resource cost
- UI implementation
- balance constant

를 확정하지 않는다.

## ACCEPTED_RISK

Product Promise 때문에 의도적으로 Risk를 수용할 수 있다.

```text
ACCEPTED_RISK

Risk:
Reason Accepted:
Product Promise Protected:
Expected Downside:
Monitoring / Future Evidence:
```

Accepted Risk는 `Issue does not exist`를 의미하지 않는다.


# 23. Internal Consistency Finding

Project 자체 문서 충돌은 Reference 없이 찾을 수 있다.

## IC_FINDING

```text
IC-###

Conflicting Sources:

Rule A:

Rule B:

Why Conflict:

Affected System:

Severity:

Project Evidence Strength:

Recommended Resolution:
```

## RF Merge Rule

IC가 특정 Design Root와 동일한 문제라면 RF에 Merge 가능.

예:

```text
Turn order contradiction
↓
same resource can be spent twice
↓
core decision validity broken
```

별도 IC와 RF를 동시에 중복 생성하지 않는다.

---

# 24. Supported Structure

문제만 찾지 않는다.

수정 과정에서 보호해야 할 강한 구조를:

`SUPPORTED_STRUCTURE`.

```text
SS-###

Structure:

Supported By:
- Project Evidence
- Universal / Genre / Scale Knowledge

Why It Works:

Product Promise Protected:

Do Not Accidentally Remove:

Validation Still Needed:
YES / NO

Validation Claim:
- ...
```

## SS Guardrail

`SUPPORTED_STRUCTURE`는 전체 Game PASS가 아니다.

의미:

> 이 부분은 현재 수정 과정에서 보존할 가치가 높은 Design Constraint.

---

# 25. Validation Need Classification

## PASS 14 — Validation Need Classification

## Reviewer Validation Boundary

Reviewer가 출력 가능한 최대 범위:

```text
VALIDATION_REQUIRED

Claim:
...

Suggested Evidence Type:
- SIMPLE MODEL
- SELF TEST
- HUMAN TEST
- AI TESTER
- MARKET TEST
- HYBRID
```

여기서 끝난다.

## Reviewer가 만들지 않는 것

- Test 횟수
- Pass Rate
- Win Rate Threshold
- Persona count
- Sample size
- Seed
- exact Metric criteria
- implementation detail

## Structural Fix vs Validation

### STRUCTURAL FIX FIRST

문서만으로 논리적으로 확인 가능한 문제.

예:
- impossible state
- missing information channel
- contradictory dependency
- broken state transition
- missing required response path
- obvious uncontrolled scope matrix

### VALIDATE FIRST

Human / Experience Claim.

예:
- choice tension
- perceived fairness
- readability
- role identity
- fatigue
- pacing
- emotional consequence
- core-loop subjective appeal

### NO ACTION YET

정보가 부족하거나 비용 대비 우선순위가 낮음.

---

## Cheap Validation Route Hint

Reviewer는 상세 Test Plan 대신 적합한 검증 **형태**만 제안할 수 있다.

| Claim / Problem Type | Suggested Evidence Form |
|---|---|
| Rule / Number / Economy | Paper / Spreadsheet / Simple Simulation |
| Core Choice / Management Loop | Paper Prototype / Simple Web Prototype |
| UI Flow | Figma Prototype |
| Action / Physics / Feel | Unity Micro Prototype |
| Structural Balance after playable prototype | AI Tester later |
| Fun / Readability / Tension | Human Test |
| Market demand / funnel claim | Market Test |

특정 Tool 이름은 optional example이며 Runtime requirement가 아니다.

Further Validation Design:

`DEFERRED`.


# 26. Machine / Human Guardrails

Canonical Guardrails:

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

```text
Response Option Exists
≠
Human can perceive / execute it
```

```text
Progression Unlock Exists
≠
Meaningful Growth
```

```text
State Persists
≠
State changes Future Decisions
```

## Restart / Abandon

Batch Runner restart는 Player Restart가 아니다.

Machine-only에서 다음을 Human behavior로 해석 금지.

- Restart Rate
- Early Abandon Rate
- Continue Rate

## Information

AI direct GameState access:

```text
≠
Player inspected information
```

Inspect / information use는 explicit observation model 또는 Human Telemetry 필요.

## Action

Perfect-reaction AI success:

```text
≠
Human can react
```

## Counterfactual Metric

Formal Definition 없이 Machine Metric으로 확정 금지:

- First Critical Mistake
- Unrecoverable State
- Preventable Failure
- Bad-seed Failure
- Avoidable Death

표시:

`FORMAL DEFINITION REQUIRED`.

---

# 27. Reviewer Verdict

## PASS 15 — Final Review Summary / Verdict

Reviewer 사용자-facing Verdict:

```text
REVIEW_CLEAR
REVIEW_CLEAR_WITH_VALIDATION
REVISION_REQUIRED
STRUCTURAL_RISK
INSUFFICIENT_SPEC
```

## REVIEW_CLEAR

현재 단계에서 주요 Structural Finding 없음.

Human / Market validation이 전혀 필요 없다는 뜻은 아니다.

## REVIEW_CLEAR_WITH_VALIDATION

구조적으로 성립 가능하나 핵심 Experience Claim 검증 필요.

## REVISION_REQUIRED

다음 Prototype / Development 투자 전에 수정 가능한 주요 구조 문제가 존재.

## STRUCTURAL_RISK

Core Product Promise / Scope / Architecture에 높은 Root Risk.

Project Kill 판정이 아니다.

## INSUFFICIENT_SPEC

현재 문서로 핵심 Mechanism 판정 불가.

## Prohibited Verdict

```text
PROCEED
ITERATE
PIVOT
KILL
```

Reviewer Runtime에서 사용하지 않는다.

---

## REVIEW_SUMMARY

```text
REVIEW_SUMMARY

Project:
Version:

Primary Genre:
Secondary Genre:

Scale:

Core Product Promise:

Reviewer Set:
- Universal:
- Genre:
- Scale:
- Market:
- Selection:

Root Issues:
Critical:
High:
Medium:
Low:

Needs Info:
- ...

Validation Required:
- Claim:
  Suggested Evidence Type:

Accepted Risks:
- ...

Supported Structures:
- ...

Evidence Boundary Warnings:
- ...

Reviewer Verdict:
```

## Summary Rule

Review Summary는:
- Issue count 합계
- score average
- success probability

로 Verdict를 계산하지 않는다.

Critical / High Root, Product Promise risk, Unknown blocking core judgment를 우선 본다.


# 28. Finding Lifecycle

## Standard

```text
OPEN
→ RESOLVED
```

## Accepted Risk

```text
OPEN
→ ACCEPTED_RISK
```

## Validation

```text
OPEN
→ VALIDATION_REQUIRED
```

Validation evidence 후 후속 Review에서:
- RESOLVED
- OPEN
- ACCEPTED_RISK
등으로 변경 가능.

## Re-review

같은 Root라면 새 RF를 만들지 않는다.

```text
RF:
Previous Status:
Current Status:
Changed Evidence:
Changed Rule:
Project Version:
Review Version:
```

## Regression

해결된 문제가 재발하면:

`REGRESSION` 태그.

---

# 29. Runtime Data Structures

Core Runtime 최소 Object:

1. `PROJECT_REVIEW_INPUT`
2. `PROJECT_MECHANISM_PROFILE`
3. `PROJECT_CLAIM_REGISTRY`
4. `UNIVERSAL_APPLICABILITY`
5. `PROJECT_GENRE_ROUTING_PROFILE`
6. `PROJECT_SCALE_ROUTING_PROFILE`
7. `PROJECT_REVIEWER_SET`
8. `HYBRID_CONFLICT`
9. `RAW_FINDING`
10. `ROOT_ISSUE`
11. `RF_FINDING`
12. `IC_FINDING`
13. `SUPPORTED_STRUCTURE`
14. `MARKET_FINDING`
15. `REVIEW_SUMMARY`

명시적으로 제외:

`VALIDATION_PLAN_OBJECT`.

---

# 30. Runtime Dependency Graph

## Canonical PASS Sequence

```text
PASS 0
Input Integrity

PASS 1
Project Mechanism Extraction

PASS 2
Product Promise / Claim Registry

PASS 3
Universal Applicability

PASS 4
Genre Routing

PASS 5
Universal Parent → Genre Specialization

PASS 6
Hybrid Resolver

PASS 7
Scale Routing

PASS 8
Relevant Scale Handoff

PASS 9
Market / Selection when applicable

PASS 10
Raw Finding Collection

PASS 11
Root Cause Merge / Split

PASS 12
Severity / Evidence Classification

PASS 13
Recommended Action

PASS 14
Validation Need Classification

PASS 15
Final Review Summary / Verdict
```


```text
PROJECT_REVIEW_INPUT
↓
PASS 0 Input Integrity
↓
PROJECT_MECHANISM_PROFILE
↓
PROJECT_CLAIM_REGISTRY
↓
UNIVERSAL APPLICABILITY
+
GENRE ROUTING
+
SCALE ROUTING
↓
PROJECT_REVIEWER_SET
↓
RAW_FINDING
↓
ROOT MERGE / SPLIT
↓
RF_FINDING
↓
STRUCTURAL FIX
or
VALIDATION NEED TAG
↓
SUPPORTED_STRUCTURE
+
REVIEW_SUMMARY
```

## Canonical Loading Order

```text
Project Mechanism
↓
Product Promise
↓
Universal Applicability
↓
Genre Routing
↓
Universal Parent
↓
Genre Specialization
↓
Hybrid Resolver
↓
Scale Routing
↓
Relevant Handoff
↓
Optional GSC
↓
Market / Selection when applicable
```

---

# 31. Runtime Modes

## QUICK REVIEW

사용:
- early concept
- early pitch
- incomplete brief

출력:
- Mechanism Profile summary
- Product Promise
- Top 3~5 Risks
- major Unknown
- Validation Need

## STANDARD REVIEW

기본.

출력:
- full routing
- Root Finding
- Severity / Evidence
- Supported Structure
- Validation Need
- Review Verdict

## DEEP REVIEW

사용:
- milestone
- large project
- multiple system docs
- pre-production gate

추가:
- full trace
- Hybrid map
- Handoff cost shape
- Evidence Boundary
- finding lifecycle
- more complete medium-risk appendix

## Mode Guardrail

Mode는:

`Output Depth`

만 바꾼다.

Severity / Core / Evidence 기준은 동일.

---

## Development Stage Sensitivity

### CONCEPT
우선:
- Product Promise
- Mechanism
- Scope
- major contradiction

세부 Balance를 확정적으로 평가하지 않는다.

### PAPER PROTOTYPE
우선:
- Decision structure
- loop
- resource / state relation

### CONCEPT TEST MODEL
우선:
- Core claim
- minimal executable mechanism

### DIGITAL PROTOTYPE
우선:
- formal rule
- structural balance
- state transition
- instrumentation readiness

### VERTICAL SLICE
우선:
- Human readability
- UX
- feel
- content-production reality

### PRODUCTION
우선:
- regression
- throughput
- content / balance consistency
- production ownership

### PRE-LAUNCH
우선:
- onboarding
- balance
- product-facing quality
- market-facing claim consistency

Stage sensitivity는 Severity 기준을 바꾸지 않는다.

같은 Issue라도 현재 단계에서 reviewable한 Evidence 종류와 Recommended Action을 조정한다.


# 32. Versioning / Determinism

## Review Snapshot

```text
REVIEW_RUNTIME_VERSION:
REVIEWER_RUNTIME_v0.1

Studio Core:
v0.4

Genre Master:
v0.3

Scale Baseline:
v0.2

Loaded Genre Baselines:
- ...

Project Version:

Review Date:

Mode:
- QUICK
- STANDARD
- DEEP
```

## Determinism Requirement

동일:

- Project Version
- Canonical Core Version
- Runtime Version
- Mode

이면 가능한 한 동일한:
- Genre routing
- loaded rule
- Applicability
- Root Issue
- Trace

를 재현해야 한다.

문장 표현은 달라도 구조 판정은 안정적이어야 한다.

## Formal Engine Candidates

향후 deterministic engine으로 분리 가능:

- genre routing score
- core loading
- status filtering
- version trace
- schema validation
- finding lifecycle
- dedup reference graph

LLM 영역:
- mechanism meaning
- promise interpretation
- root synthesis
- reviewer question generation
- relevance
- recommended action

---

# 33. Anti-pattern Registry

## AP-RUNTIME-001 — Load Every Core
모든 Universal / Genre / Scale Rule을 한 번에 Load.

## AP-RUNTIME-002 — Store Tag Routing
장르 태그만 보고 Rule Load.

## AP-RUNTIME-003 — Candidate = Weak Finding
Candidate status를 Severity에 투영.

## AP-RUNTIME-004 — Confidence = Severity
Evidence Confidence를 Project Impact로 사용.

## AP-RUNTIME-005 — One Core = One Issue
Core마다 RF 생성.

## AP-RUNTIME-006 — Parent + Child Double Penalty
같은 Root에 중복 Severity.

## AP-RUNTIME-007 — Genre Count = Game Depth
Hybrid genre 개수를 깊이로 취급.

## AP-RUNTIME-008 — Feature Exists = Claim Proven
기능 존재로 Experience Claim 검증 처리.

## AP-RUNTIME-009 — Missing Information = Failure
UNKNOWN을 FAIL.

## AP-RUNTIME-010 — AI Result Imagined from GDD
테스트 없이 simulation 결과 생성.

## AP-RUNTIME-011 — Machine State = Player Knowledge
AI access를 Human information으로 해석.

## AP-RUNTIME-012 — Market Risk = Bad Design
Audience size를 Design Quality로 합침.

## AP-RUNTIME-013 — Outsourcing = Cost Removed
외주 가능을 internal cost zero로 처리.

## AP-RUNTIME-014 — AI Tool = Extra Team Member
AI-assisted production으로 Scale 재분류.

## AP-RUNTIME-015 — Reviewer Invents Numeric Threshold
Reference 근거 없는 카드 / 적 / 클래스 수 limit 생성.

## AP-RUNTIME-016 — Reviewer Outputs KILL
실제 evidence 없이 project termination decision.

## AP-RUNTIME-017 — All Medium Issues Listed Equally
priority 없는 장문 issue dump.

## AP-RUNTIME-018 — Historical GSC Loaded
Retired GSC를 active check로 사용.

## AP-RUNTIME-019 — Small/Mid Scale Extrapolated
Solo/Micro evidence를 larger scale에 자동 적용.

## AP-RUNTIME-020 — Generic Advice without Project Mechanism Trace
“UI를 개선하라”, “콘텐츠를 줄여라”만 출력.

## AP-RUNTIME-021 — Validation Planner Automatically Invoked
모든 Review 뒤 상세 Validation Plan을 자동 생성.

---

# 34. Acceptance Test Scenarios

Acceptance Test는 Runtime 구조를 검증하기 위한 **Dry-run Scenario**다.

실제 Test Result를 생성하지 않는다.

## Scenario A — Solo Deckbuilding Roguelite

Expected Runtime Conditions:
- Deck L3
- Roguelike L3
- SOLO
- UC002 / UC004 likely applicable
- Deck interaction / run variation Parent overlap
- Handoff: DECK / ROGUE relevant only
- Card count / QA duplicate Finding = 0

Must demonstrate:
1. Card choice depth와 Production QA를 분리.
2. UC002 + Deck + Rogue variation을 한 Root로 과도 merge하지 않음.
3. QA matrix는 Production Root로 Merge.
4. Retired `GSC-DECK-SOLO-001` 미로드.
5. 필요 시 `VALIDATION_REQUIRED` for perceived build identity.

---

## Scenario B — Narrative Management Simulation

Expected:
- Management L3
- Narrative L3
- Simulation L2
- UC003 / UC005
- SOLO 가능 시 Responsibility Routing Hint
- Entity × State × Event Handoff

Must demonstrate:
1. persistent state Root의 UC003 / MGMT / SIM triple penalty 제거.
2. narrative causal attribution은 UC005와 Root가 다를 때만 분리.
3. world-detail scope를 responsibility level 기준으로 검토.
4. narrative reactivity와 production authored-content cost 분리.

---

## Scenario C — Action RPG

Expected:
- Action L3
- RPG L3
- UC006 conditional
- Action / RPG Evidence Boundary warning
- Player Skill vs Character Skill potential hybrid conflict

Must demonstrate:
1. UC006 Candidate status trace.
2. Vertical Power를 자동 Failure 처리하지 않음.
3. machine response option ≠ human reactability.
4. animation / hitbox / content cost는 Production Root로 분리.
5. Human Test tag for feel / readability when needed.

---

## Scenario D — Deduction Narrative

Expected:
- Deduction L3
- Narrative L2/L3
- UC005 applicability
- Deduction inference exception

Must demonstrate:
1. Information availability를 player-owned inference로 대체하지 않음.
2. `GC-DEDUCT-001/003/004` 독립 검사.
3. authored reveal과 player inference conflict를 Hybrid Finding으로 분리 가능.
4. logic QA는 production handoff.
5. “few screens = small scope” 가정 금지.

---

## Scenario E — One-shot Authored Narrative

Expected:
- Narrative L3
- UC002 `CONDITIONAL / N/A`
- low replay를 결함 처리하지 않음.

Must demonstrate:
1. Product Promise가 replay가 아니면 UC002 violation 없음.
2. narrative meaning / consequence는 별도 relevant Parent로 검사.
3. content consumption 구조를 replay failure로 오판하지 않음.

---

## Scenario F — Micro Simulation

Expected:
- Simulation L3
- MICRO
- `SC-MICRO-001` diagnostic
- Solo Core 자동 적용 금지
- SIM Handoff: entity-state / AI / tooling relevant
- Scale Evidence Boundary warning

Must demonstrate:
1. 2~5명 = Solo×N 계산 금지.
2. parallel lanes와 coordination cost 동시 기록.
3. tooling / AI specialist dependency를 production root로 분석.
4. Solo-specific core violation을 자동 생성하지 않음.

---

## Acceptance Test Expected Output

각 Scenario Dry-run은 최소 다음을 산출해야 한다.

```text
1. Mechanism Profile
2. Product Promise
3. Claim Registry summary
4. Genre Routing Profile
5. Scale Routing Profile
6. Reviewer Set
7. 2~5 Root Findings
8. Duplicate Finding = 0
9. Validation Need Tag when necessary
10. Supported Structure
11. Evidence Boundary
12. Reviewer Verdict
13. Runtime Version Trace
```

Acceptance Test는 실제 플레이 결과를 생성하지 않는다.

검사 목적은:
- Routing stability
- dedup correctness
- evidence boundary
- question specificity
- severity / confidence separation

이다.


# 35. Dry-run Examples

아래 예시는 **Runtime 구조 예시**이며 실제 프로젝트 평가 결과가 아니다.

## Example 1 — Parent + Child Merge

Hypothetical Project Mechanism:

```text
Enemy attack before hit:
small visual flash

Player decision:
dodge / block

Project Claim:
fast but readable combat
```

Raw Findings:

```text
UC005:
Threat information may not be actionable.

GC-ACTION-002:
Cue may not leave a human response window.
```

Merge:

```text
ROOT:
Threat information cannot reliably drive the intended response.

Universal Parent:
UC005

Genre Specialization:
GC-ACTION-002

Severity:
ONE
```

Experience part:

```text
VALIDATION_REQUIRED

Claim:
Human can recognize and react to the cue.

Suggested Evidence Type:
HUMAN TEST
```

Reviewer는 reaction threshold를 임의 생성하지 않는다.

---

## Example 2 — UC003 / UC005 Split

Hypothetical Narrative State:

```text
Player betrays NPC.
Flag persists.
Later NPC refuses help.
```

Case A:

Later refusal이 이후 Resource / Route / Choice를 전혀 바꾸지 않음.

```text
Root:
Persistent consequence has no decision consequence.

Parent:
UC003
```

Case B:

Refusal은 중요한 결과를 만들지만 Player에게 betray → refusal 연결이 표시되지 않음.

```text
Root:
Outcome cause is not learnable.

Parent:
UC005 Outcome-time
```

A와 B는 Root가 달라 분리 가능.

---

## Example 3 — Design vs Production Split

Hypothetical Deck:

```text
180 cards
shared effect grammar
many cross-card triggers
```

Potential Design Root:

```text
Same effect families create context-invariant reward decisions.
```

Potential Production Root:

```text
Cross-trigger interaction matrix exceeds sustainable QA capacity.
```

같은 카드 수에서 출발하지만 Fix / Validation / Category가 달라 분리한다.

---

## Example 4 — UNKNOWN → NEEDS_INFO

Project:

```text
Persistent injury system exists.
```

Unknown:

```text
Does injury affect assignment?
Does it expire?
Can player treat it?
```

Runtime:

```text
Status:
NEEDS_INFO

Known:
Injury state exists.

Unknown:
Future decision effect / recovery path.

Blocked Judgment:
UC003 consequence coupling.
```

다음처럼 쓰지 않는다.

```text
Injury system is meaningless.
```

---

## Example 5 — UC006 Candidate

Hypothetical Product Promise:

```text
Power Fantasy:
YES

Build Expression:
LOW

Progression:
large stat growth
```

Runtime Question:

> Progression의 Promise가 Vertical Power라면 power growth 자체를 Decision Expansion 부족으로 감점하지 않는다. 다만 late progression이 기존 Core Choice를 완전히 제거하는가?

Knowledge Trace:

```text
UC006
Status:
CANDIDATE
```

Human Claim:

```text
Power Fantasy가 충분히 느껴지는가?
→ VALIDATION_REQUIRED / HUMAN TEST
```

---

# 36. Self-Review

| Check | Result |
|---|---|
| 신규 Core 생성 없음? | PASS |
| Canonical Status 변경 없음? | PASS |
| Mechanism-first? | PASS |
| Product Promise 선행? | PASS |
| Universal Applicability Gate? | PASS |
| UC006 Conditional? | PASS |
| Genre L0~L3 loading? | PASS |
| Candidate trace? | PASS |
| Scale / Content / Budget 분리? | PASS |
| Handoff를 Core로 사용하지 않음? | PASS |
| Retired GSC 미로드? | PASS |
| Parent / Child / Handoff duplicate Severity 방지? | PASS |
| Knowledge Confidence / Project Evidence / Severity 분리? | PASS |
| Machine / Human Boundary? | PASS |
| Test Result 생성 금지? | PASS |
| Validation Planner 비필수? | PASS |
| KILL verdict 없음? | PASS |
| UNKNOWN ≠ FAIL? | PASS |
| Supported Structure 포함? | PASS |
| Runtime Version trace? | PASS |

---

# 37. Final Position

## A. Reviewer Runtime의 책임 범위는?

Project Mechanism / Product Promise를 구조화하고, 현재 Project에 적용 가능한 Canonical Knowledge만 Load하여:

- Root Risk
- Supported Structure
- Unknown
- Structural Fix
- Validation Need

로 압축하는 것까지다.

---

## B. Project 입력을 처음 어떻게 구조화하는가?

먼저 `PASS 0 Input Integrity`를 수행하고:

`PROJECT_MECHANISM_PROFILE`

로:
- Player Verb
- State
- Loop
- Decision
- Resource
- Failure / Recovery
- Progression
- Information
- Production-heavy area

를 구조화한다.

Genre 선택은 그 이후다.

---

## C. Product Promise는 언제 추출하는가?

Mechanism Profile 직후, Universal Applicability와 Genre Routing 전에 추출한다.

이유:

> Rule Applicability와 Failure 의미가 Product Promise에 의존하기 때문.

---

## D. Universal / Genre / Scale Rule은 어떤 순서로 로드하는가?

```text
Project Mechanism
↓
Product Promise
↓
Universal Applicability
↓
Genre Routing
↓
Universal Parent
↓
Genre Specialization
↓
Hybrid Resolver
↓
Scale Routing
↓
Relevant Scale Handoff
↓
Optional GSC
```

---

## E. Candidate는 어떻게 처리하는가?

Candidate도 Finding 생성 가능.

단:

```text
Knowledge Status:
CANDIDATE
```

를 표시한다.

Candidate status는 Severity를 자동 낮추지 않는다.

---

## F. Hybrid Genre 중복은 어떻게 제거하는가?

먼저 Shared:
- Verb
- State
- Consequence

를 찾고 Type A~E로 Interaction을 분류한다.

같은 Root Mechanism이면 Universal Parent 아래 Genre residual만 보존하고 Severity는 한 번만 부여한다.

---

## G. Parent / Genre / Scale / Handoff Finding은 어떻게 하나의 Root로 묶는가?

Raw Finding을 먼저 수집한 뒤:

```text
Same Mechanism
+
Same Promise Impact
+
Same Fix
+
Same Validation Question
```

이면 하나의 `ROOT_ISSUE / RF`.

---

## H. Knowledge Confidence와 Issue Severity는 어떻게 분리하는가?

Knowledge Confidence:

> Canonical Rule 자체의 Evidence Strength.

Severity:

> 현재 Project에서 해당 문제가 미치는 영향.

상호 변환하지 않는다.

---

## I. Project Evidence Strength가 왜 별도 필요한가?

Rule이 강한 Evidence를 가져도 현재 프로젝트에서 그 문제가 실제 존재하는지 확인되지 않을 수 있기 때문이다.

반대로 Candidate Rule이라도 Project 문서에서 Root가 직접 확인되면 Project Evidence는 CONFIRMED일 수 있다.

---

## J. UNKNOWN은 어떻게 처리하는가?

FAIL 처리하지 않는다.

핵심 판단을 막으면:

`NEEDS_INFO`.

함께 기록:
- Known
- Unknown
- Unknown이 막는 판단

---

## K. 바로 수정해야 하는 문제와 Test가 필요한 Claim을 어떻게 나누는가?

### STRUCTURAL FIX FIRST
문서만으로 논리적 결함 확인 가능.

### VALIDATE FIRST
Human / Experience Claim.

### NO ACTION YET
정보 부족 / 후순위.

---

## L. Reviewer가 Validation Test Plan까지 만드는가?

**아니다.**

---

## M. Reviewer가 할 수 있는 Validation 관련 출력은 어디까지인가?

```text
VALIDATION_REQUIRED
+
Claim
+
Suggested Evidence Type
```

까지.

Detailed Validation Design:

`DEFERRED`.

---

## N. Machine / AI Tester와 Human Evidence 경계는?

Machine:
- state
- transition
- formal cause
- structural availability
- simulation distribution

에 강하다.

Human:
- readability
- fairness
- attribution
- meaningful choice
- power fantasy
- feel
- tension
- fatigue
- identity

를 소유한다.

Machine proxy로 Human claim을 증명하지 않는다.

---

## O. Reviewer가 최종 PROCEED / ITERATE / PIVOT / KILL을 결정하는가?

**아니다.**

Reviewer는 Evidence-based Review 상태만 제공한다.

---

## P. Reviewer Runtime의 사용자-facing Verdict는 무엇인가?

```text
REVIEW_CLEAR
REVIEW_CLEAR_WITH_VALIDATION
REVISION_REQUIRED
STRUCTURAL_RISK
INSUFFICIENT_SPEC
```

---

## Q. 현재 Canonical Knowledge를 이용해 실제 프로젝트 Dry-run 준비가 되었는가?

**YES.**

Acceptance Scenario 6개와:
- Input schema
- Routing
- Root merge/split
- Severity/Evidence
- Verdict
- Validation boundary

가 정의되었다.

---

## R. 다음 단계는 무엇인가?

```text
Reviewer Runtime Specification
✅
↓
Reviewer Runtime Dry-run #1
↓
Reviewer Runtime Dry-run #2
↓
Runtime Correction / Consolidation
↓
Reviewer Runtime v1.0
↓
Studio OS Canonical Document Manifest
↓
Studio OS Core Package v1.0
```

Validation Planner는 현재 필수 Next Step이 아니다.

---

# 38. Source Trace

## Direct Runtime Prompt
`Studio OS — Reviewer Runtime Specification Prompt v0.2`

## Canonical Universal / Studio
- `Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`

## Canonical Genre Router
- `GENRE_CORE_MASTER_INDEX_v0.3.md`

## Canonical Scale Router
- `SCALE_CORE_BASELINE_v0.2.md`

## Canonical Universal Sync
- `UNIVERSAL_CANONICAL_SYNC_v0.1.md`

## Historical Decision Trace
- `UNIVERSAL_CORE_CONSOLIDATION_v0.1_APPROVED.md`
- `GENRE_SCALE_CORE_INTEGRATION_v0.1_APPROVED.md`
- `GSC_CANONICAL_CONSOLIDATION_v0.1.md`

## Frozen Runtime Facts

```text
Universal Provisional:
5

Universal Candidate:
1

Universal Default:
UC001~005

Universal Conditional:
UC006

Genre Baselines:
9

Scale Handoffs:
51

Active Independent GSC:
0

Retired Historical GSC:
3

Routing Specialization:
2

Scale Evidence:
SOLO strong
MICRO moderate qualitative / weak comparative
SMALL weak
MID+ outside primary scope
```

이 Runtime은 Canonical Knowledge를 적용하는 실행 규격이며 새로운 Core Status를 변경하지 않는다.
