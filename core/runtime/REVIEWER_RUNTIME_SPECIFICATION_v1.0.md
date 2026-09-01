# REVIEWER_RUNTIME_SPECIFICATION_v1.0

**Studio OS — Design Reviewer Runtime Specification**  
**Status:** `APPROVED_AS_REVIEWER_RUNTIME_V1_BASELINE`  
**Runtime Version:** `REVIEWER_RUNTIME_v1.0`  
**Purpose:** `Evidence-based Project Review / Dynamic Rule Loading / Root-risk Deduplication / Validation-Need Classification`  
**Studio Core:** `Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`  
**Genre Master:** `GENRE_CORE_MASTER_INDEX_v0.3.md`  
**Scale Baseline:** `SCALE_CORE_BASELINE_v0.2.md`  
**Active Independent GSC:** `0`  
**Validated With:**  
- `Project MCC v0.5`
- `Magic Word Deckbuilding v0.9`

**Blocking Runtime Defect at v1 lock:** `0`  
**Major Runtime Defect at v1 lock:** `0`  
**Next:** `Studio OS Canonical Document Manifest`

---

# 1. Executive Summary

`REVIEWER_RUNTIME_SPECIFICATION_v1.0`은 Studio OS의 Canonical Knowledge를 실제 게임 기획에 적용하는 **standalone Reviewer execution baseline**이다.

v1.0은 다음 Runtime sources의 검증된 규칙을 하나로 통합한다.

```text
Reviewer Runtime v0.1
+
Minor Correction #01
+
Dry-run #1 — Project MCC
+
Dry-run #2 — Magic Word
+
Cross-Dry-run Assessment
↓
REVIEWER_RUNTIME_v1.0
```

이 문서를 사용하는 Reviewer는 v0.1, Correction Note, Defect Log를 별도로 읽지 않아도 정상 실행할 수 있어야 한다.

이번 Consolidation에서 **Game Design Knowledge 자체는 변경하지 않았다.**

```text
New Universal Core:
0

New Genre Core:
0

New Scale Core:
0

Core Promotion / Demotion:
0

Confidence Change:
0

Genre Routing Score Change:
0

New GSC:
0
```

v1.0에서 통합된 Runtime execution correction은 정확히 네 가지다.

1. **RD-001 — Review Target Scope**
   - Full Project / Current Milestone / Prototype Slice / Specific System을 명시한다.
   - Full Product feature가 현재 Review violation source로 자동 사용되지 않게 한다.

2. **RD-002 — Reviewer Verdict Precedence**
   - 기존 5개 Verdict를 유지한다.
   - 점수가 아니라 qualitative precedence로 선택한다.

3. **RD-003 — Enum Conformance**
   - Canonical enum field에는 정의된 값 하나만 저장한다.
   - 설명은 Note / Qualifier field로 분리한다.

4. **RD-004 — Unresolved Scale Representation**
   - 팀 정보가 없을 때 Scale을 추정하지 않는다.
   - `UNKNOWN`을 Team Scale category로 추가하지 않는다.
   - `Scale Resolution State`와 `Scale Evidence State`를 별도로 기록한다.

Canonical PASS Architecture는 변경하지 않는다.

```text
PASS 0  Input Integrity
PASS 1  Project Mechanism Extraction
PASS 2  Product Promise / Claim Registry
PASS 3  Universal Applicability
PASS 4  Genre Routing
PASS 5  Universal Parent → Genre Specialization
PASS 6  Hybrid Resolver
PASS 7  Scale Routing
PASS 8  Relevant Scale Handoff
PASS 9  Market / Selection when applicable
PASS 10 Raw Finding Collection
PASS 11 Root Cause Merge / Split
PASS 12 Severity / Evidence Classification
PASS 13 Recommended Action
PASS 14 Validation Need Classification
PASS 15 Final Review Summary / Verdict
```

Runtime 핵심 원칙:

```text
Mechanism-first
+
Product Promise-first
+
Applicability before Violation
+
Many Rules → Few Root Issues
+
ONE ROOT ISSUE = ONE RF
```

반드시 분리한다.

```text
Knowledge Confidence
≠
Project Evidence Strength
≠
Issue Severity
```

그리고:

```text
UNKNOWN
≠
FAIL
```

Reviewer는 Validation Planner가 아니다.

허용되는 최대 출력:

```text
VALIDATION_REQUIRED

Claim:
...

Suggested Evidence Type:
...
```

금지:
- Test count
- Persona specification
- Sample size
- Seed
- Threshold
- detailed metric criteria
- AI Tester implementation

v1.0은 서로 다른 두 실제 Project에서 검증되었다.

### Regression Fixture 01 — MCC

```text
Strategy L3
Management L3
Simulation L2

Review Target:
PROTOTYPE SLICE

Scale:
SOLO

UC006:
Inactive in reviewed slice

Duplicate RF:
0
```

### Regression Fixture 02 — Magic Word

```text
Deckbuilding L3
Roguelike L2
Strategy L2
RPG L1

Review Target:
FULL PROJECT

Scale Resolution:
UNRESOLVED

UC006:
CANDIDATE / CONDITIONAL

Duplicate RF:
0
```

이는 Runtime generalization evidence다.

**Game Core Promotion Evidence가 아니다.**

---

# 2. Runtime Purpose

Reviewer Runtime의 목적은:

> **현재 Project에 필요한 Evidence-Based Knowledge만 동적으로 호출하고, 기획서에서 관찰 가능한 신호를 Root Cause 수준으로 압축하여 수정 / 보존 / 추가 정보 / Validation 필요 상태를 분리하는 것**

이다.

Reviewer는 다음을 수행한다.

1. Project Source 정합성 확인.
2. Review Target / Active Scope 고정.
3. Project Mechanism 구조화.
4. Product Promise / Claim 추출.
5. Universal Applicability 판정.
6. Genre / Hybrid Routing.
7. Scale / Handoff Routing.
8. Project-specific Reviewer Question 생성.
9. Raw Finding 수집.
10. Root Issue Merge / Split.
11. Knowledge / Project Evidence / Severity 분리.
12. Structural Fix vs Validate First 분리.
13. `SUPPORTED_STRUCTURE` 보존.
14. Evidence Boundary / Unknown 명시.
15. qualitative Verdict 생성.

핵심 출력은:

```text
많은 Core Violation
```

이 아니라:

```text
적은 수의 중요한 Root Issue
+
보호해야 할 Supported Structure
+
검증해야 할 Claim
+
현재 판단을 막는 Unknown
```

이다.

---

# 3. Canonical Dependencies

## Level 1 — Universal / Studio Core

`Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`

Runtime state:

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

## Level 2 — Genre Router / Parent Map

`GENRE_CORE_MASTER_INDEX_v0.3.md`

사용:
- Mechanism-first Genre Routing
- L0~L3
- Parent → Specialization
- Candidate loading weight
- Hybrid interaction
- Dedup
- Scale Handoff registry
- Evidence Boundary

## Level 3 — Scale Router

`SCALE_CORE_BASELINE_v0.2.md`

사용:
- Scale taxonomy
- Scale evidence boundary
- 12 Production Cost Axes
- Cost Shape
- Externalization / ownership
- Scale Handoff
- Routing Specialization

## Level 4 — Approved Genre Baselines

Genre Router 결과 필요한 Source만 상세 Load한다.

모든 Genre baseline을 Active Rule Set으로 미리 로드하지 않는다.

## Level 5 — Runtime Validation History

Historical trace:

- `REVIEWER_RUNTIME_SPECIFICATION_v0.1_APPROVED.md`
- `REVIEWER_RUNTIME_CORRECTION_NOTE_01_v0.1.md`
- `REVIEWER_RUNTIME_DRYRUN_01_PROJECT_MCC_v0.1.md`
- `REVIEWER_RUNTIME_DEFECT_LOG_01_v0.1.md`
- `REVIEWER_RUNTIME_DRYRUN_02_MAGIC_WORD_v0.1.md`
- `REVIEWER_RUNTIME_DEFECT_LOG_02_v0.1.md`
- `REVIEWER_RUNTIME_CROSS_DRYRUN_ASSESSMENT_v0.1.md`

이들은 v1.0의 실행 규칙보다 우선하지 않는다.

---

# 4. Runtime Boundary

## Reviewer Responsibilities

- Source reconciliation
- Review scope fixing
- Mechanism interpretation
- Product Promise extraction
- Universal Applicability
- Genre / Scale Routing
- Parent / Child dedup
- Root cause synthesis
- Project-specific questions
- Design / Production / Market category separation
- Severity / Evidence separation
- Supported Structure preservation
- Validation Need tagging
- Reviewer Verdict

## Reviewer Non-responsibilities

### A. 기획서에 없는 기능 생성

```text
Unknown
→ Unknown
```

### B. Test Result Fabrication

금지:
- AI 결과 상상
- Human 반응 상상
- Win rate 생성
- diversity result 생성
- simulated play 결과 생성

### C. Numerical Success Prediction

금지:

```text
Success probability = 75%
```

### D. Final Investment / Kill Decision

금지:

```text
PROCEED
ITERATE
PIVOT
KILL
```

### E. Validation Plan Construction

별도 Layer:
- Test count
- Personas
- Thresholds
- Seeds
- Sample size
- exact test matrix
- AI Tester implementation

### F. Canonical Knowledge Re-promotion

Project Dry-run 결과로:
- Core Promotion
- Confidence 상승
- Genre status 변경

을 하지 않는다.

---

# 5. Input Contract

```text
PROJECT_REVIEW_INPUT

Project Name:
Project Version:

Review Target:
- FULL PROJECT
- CURRENT MILESTONE
- PROTOTYPE SLICE
- SPECIFIC SYSTEM

Active Review Scope:
- ...

Deferred Systems:
- ...

Prototype-only Simplifications:
- ...

Out-of-Scope Systems:
- ...

Current Development Stage:
- CONCEPT
- PAPER PROTOTYPE
- CONCEPT TEST MODEL
- DIGITAL PROTOTYPE
- VERTICAL SLICE
- PRODUCTION
- PRE-LAUNCH

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

Attached Documents:
- ...

Locked Decisions:
- ...

Deprecated / Superseded Documents:
- ...
```

모든 Field가 채워져 있을 필요는 없다.

Missing field를 Reviewer가 임의 생성하지 않는다.

---

# 6. Review Target / Scope

## Review Target Enum

```text
FULL PROJECT
CURRENT MILESTONE
PROTOTYPE SLICE
SPECIFIC SYSTEM
```

Review Target에는 enum 값 하나만 저장한다.

설명:

```text
Review Target Note:
...
```

에 기록한다.

## Active Review Scope

현재 Runtime에서 실제:
- Rule loading
- Finding generation
- Severity
- Verdict

대상이 되는 범위.

## Deferred Systems

Full Product에는 존재하지만 현재 Review Target에서는 구현 / 검증을 미루는 시스템.

## Prototype-only Simplifications

Prototype에서 가설을 싸게 검증하기 위해 의도적으로 단순화한 Rule.

이를 Final Product defect로 자동 처리하지 않는다.

## Out-of-Scope Systems

현재 Review 대상이 아닌 시스템.

## Canonical Scope Rule

```text
Feature Exists In Full Product
≠
Active Review Mechanism
```

---

# 7. Active / Deferred Mechanism

`PROJECT_MECHANISM_PROFILE`에 필요 시:

```text
Active Mechanisms:
- ...

Deferred Mechanisms:
- ...

Context-only Mechanisms:
- ...
```

를 기록한다.

### Active Mechanism

현재 Review Target의 실제 판단 대상.

### Deferred Mechanism

향후 존재하지만 현재 Active Violation Source는 아님.

### Context-only Mechanism

현재 system의 의미를 이해하는 데 필요하지만 자체 violation source가 아닌 것.

## Deferred Dependency Exception

Deferred system이 현재 Architecture / Production Scope를 이미 직접 제약하면 Finding에 사용할 수 있다.

반드시:

```text
Deferred-system Dependency Used:
YES

Reason:
...
```

를 기록한다.

---

# 8. Missing Information Policy

모든 Project 정보는:

```text
KNOWN
INFERRED
UNKNOWN
```

중 하나다.

## KNOWN

Current Source가 직접 명시.

## INFERRED

문서 구조에서 높은 가능성으로 추론되지만 직접 명시되지 않음.

반드시:

```text
Evidence State:
INFERRED
```

표기.

## UNKNOWN

필요한 정보가 없음.

Canonical Rule:

```text
UNKNOWN
≠
FAIL
```

Unknown 때문에 핵심 판단이 막히면:

`NEEDS_INFO`.

함께 기록:
- Known
- Unknown
- Blocked Judgment

---

# 9. PASS 0 — Input Integrity

먼저 확인한다.

1. Current Project Version
2. Current Approved Source
3. Locked Decisions
4. Deprecated / superseded rules
5. conflicting rules
6. prototype rule vs final rule
7. test value vs canonical project rule
8. active scope vs deferred scope

## Source Priority

```text
1. Current Approved Project Document
2. Current Locked Decision
3. Earlier Project Document
4. Reviewer Inference
```

## INPUT_INTEGRITY_REPORT

```text
INPUT_INTEGRITY_REPORT

Current Source:
Project Version:

Review Target:

Locked Decisions:
- ...

Deprecated Rules:
- ...

Conflicts:
- ...

Unknown Version Relationships:
- ...

Input Integrity Status:
- CLEAR
- NEEDS_INFO
```

`INPUT_INTEGRITY_REPORT`의 Status는 local report status이며 RF Status enum과 혼합하지 않는다.

## Internal Consistency Candidate

Reference Core 없이도 명백한 Project document contradiction은 Finding 가능.

---

# 10. PASS 1 — Project Mechanism Extraction

Genre를 먼저 고르지 않는다.

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
- ...

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

Active Mechanisms:
- ...

Deferred Mechanisms:
- ...

Context-only Mechanisms:
- ...
```

## Mechanism-first Rule

잘못된 Runtime:

```text
"Deckbuilder"
→ Deck Rule 전체 Load
```

정상 Runtime:

```text
Deck composition
+
hand availability
+
build commitment
+
reward adaptation
↓
Deck contribution score
```

---

# 11. PASS 2 — Product Promise / Claim Registry

Product Promise는 Mechanism Profile 직후, Universal / Genre Routing 전에 추출한다.

## Claim Types

```text
DESIGN
EXPERIENCE
PRODUCTION
MARKET
SELECTION
```

예:

```text
DESIGN:
매 Run 다른 전략이 필요하다.

EXPERIENCE:
선택이 긴장감 있다.

PRODUCTION:
데이터 중심이라 제작비가 낮다.

MARKET:
스트리머 친화적이다.

SELECTION:
한 문장으로 설명 가능하다.
```

## Feature ≠ Claim Proven

```text
Random events exist
≠
Each run requires adaptation
```

```text
Many cards exist
≠
Build diversity exists
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

Evidence State:
- KNOWN
- INFERRED
- UNKNOWN

Evidence Qualifier:

Current Support:

Status:
- STRUCTURALLY SUPPORTED
- PARTIALLY SUPPORTED
- UNSUPPORTED
- UNKNOWN
- VALIDATION_REQUIRED

Scope State:

Validation Needed:
- YES
- NO

Validation Timing:

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

# 12. PASS 3 — Universal Applicability

Default candidate pool:

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

Applicability Note:

Relevant Mechanism:
Relevant Product Promise:
Project Evidence:
```

## UC001 — Consequence Density

질문:

> 시스템 / 입력은 실제 다른 Decision과 Consequence를 만드는가?

## UC002 — Contextual Value

Replay / repeated decision / systemic variation이 Promise일 때 강하게 적용.

One-shot authored product에는:

`CONDITIONAL / N/A`.

## UC003 — Consequence → Next Decision

Persistent state / delayed consequence가 존재할 때 적용.

```text
State exists
≠
State changes future decisions
```

## UC004 — Uncertainty Response Agency

Meaningful uncertainty가 있을 때 적용.

Deterministic threat cue는 UC005가 우선.

## UC005 — Actionable / Learnable Information

Decision-time information + outcome-time learning.

Deduction inference ownership은 UC005로 대체하지 않는다.

## UC006 — Progression Promise Candidate

항상:

```text
Knowledge Status:
CANDIDATE
```

Progression이 실제 Product Promise일 때만:

```text
Applicability:
CONDITIONAL

Runtime:
CONDITIONAL DIAGNOSTIC
```

Progression 존재와 Progression Promise는 동일하지 않다.

Vertical Power 자체를 결함으로 취급하지 않는다.

Regression expectation:

```text
MCC Prototype Slice:
UC006 inactive

Magic Word Full Project:
UC006 conditional
```

---

# 13. PASS 4 — Genre Routing

9개 Genre는 Mechanism Contribution으로 Routing한다.

Axes:

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

Score는 Routing Aid다.

Mechanism explanation이 반드시 필요하다.

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

## Loading Weight

### L3

- Provisional → `ACTIVE CHECK`
- High / Very High Candidate → `WATCH`
- Medium Candidate → Project Risk Signal 있을 때만

### L2

- applicable Provisional → `ACTIVE CHECK`
- Candidate → Project Risk Signal 있을 때만

### L1

- 2~4 supporting questions
- automatic issue generation 금지

### L0

- Load 금지

## Candidate Rule

Candidate도 RF 생성 가능.

그러나:

```text
Knowledge Status:
CANDIDATE
```

를 Trace한다.

Candidate status는 Severity를 자동 낮추지 않는다.

---

# 14. PASS 5 — Universal Parent → Genre Specialization

Universal Parent와 Genre Child가 같은 Root Mechanism을 설명하면:

```text
Universal Parent
↓
Genre Specialization
```

으로 묶는다.

Parent:
- Root issue ownership

Child:
- genre-specific trigger
- state
- diagnostic
- reviewer action

을 추가한다.

## Canonical Merge Test

```text
Same Mechanism
+
Same Product Promise Impact
+
Same Fix
+
Same Validation Question
↓
ONE ROOT
```

모두 기계적으로 일치해야 하는 것은 아니지만, 대부분이 같다면 하나의 Root가 적절하다.

## Do Not Merge Automatically

같은 Parent 아래 있다는 이유만으로 Merge하지 않는다.

예:

```text
UC005:
Threat Readability

≠

UC005:
Failure Attribution
```

Fix / Validation Question이 다르면 분리 가능.

---

# 15. PASS 6 — Hybrid Resolver

둘 이상의 L2/L3 Genre가 있으면:

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

## Triple-Penalty Guard

예:

```text
UC003
+
GC-MGMT-004
+
GC-SIM-002
```

가 같은 Persistent-State Root를 설명하면:

`ONE RF`.

Genre child는 residual만 추가한다.

---

# 16. PASS 7 — Scale Routing

Team Scale은:

```text
Content Scope
Budget
Project Ambition
```

과 동일하지 않다.

## PROJECT_SCALE_ROUTING_PROFILE

```text
PROJECT_SCALE_ROUTING_PROFILE

Scale Resolution State:
- RESOLVED
- UNRESOLVED

Scale Evidence State:
- KNOWN
- INFERRED
- UNKNOWN

Scale:
- SOLO
- MICRO
- SMALL
- MID+

Scale Evidence Note:

Core Team:
- Headcount:
- Sustained FTE:
- Core Ownership Domains:
  - Design:
  - Programming:
  - Art:
  - Content:
  - Production:

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
- ...

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
- ...
```

## RESOLVED Rule

충분한 evidence가 있으면:

```text
Scale Resolution State:
RESOLVED

Scale Evidence State:
KNOWN
or
INFERRED

Scale:
SOLO / MICRO / SMALL / MID+
```

`INFERRED`인 경우 근거 필수.

## UNRESOLVED Rule

정보 부족:

```text
Scale Resolution State:
UNRESOLVED

Scale Evidence State:
UNKNOWN
```

`Scale` field는 비워둔다.

금지:

```text
Scale:
UNKNOWN
```

UNKNOWN은 team category가 아니다.

금지:

```text
Scale:
SOLO
```

근거 없이 추정.

## Unresolved Scale Runtime Behavior

`UNRESOLVED`면:

1. Scale Core 자동 Load 금지.
2. SOLO / MICRO / SMALL / MID+ 가정 금지.
3. Scale-specific Routing Specialization 자동 Load 금지.
4. Scale-relative feasibility Verdict 금지.
5. 필요 시 `NEEDS_INFO` 기록.

## Scale Loading — Resolved Only

### SOLO
`SC-SOLO-*` applicability.

### MICRO
`SC-MICRO-001` diagnostic.

Solo rule 자동 상속 금지.

### SMALL / MID+
Evidence Boundary 출력.

Solo / Micro rule extrapolation 금지.

## 12 Production Cost Axes

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

`Cost Shape UNKNOWN`은 Scale category UNKNOWN과 다른 개념이다.

## Outsourcing Guardrail

```text
Externalizable
≠
Cost Removed
```

내부에 남을 수 있음:
- specification
- communication
- revision
- integration
- acceptance QA
- regression ownership

## AI-assisted Production Guardrail

```text
AI-assisted Work
≠
Independent Human Owner
≠
Core Team Headcount Increase
```

AI는 `PRODUCTIVITY_MODIFIER`.

근거 없이 숫자 FTE로 환산하지 않는다.

---

# 17. PASS 8 — Relevant Scale Handoff

51개 전체 자동 Load 금지.

Routing 조건:

```text
Active Genre
+
Actual Project Mechanism
+
Relevant Production Driver
```

## Handoff Runtime Role

```text
Core:
NO

Production Risk Routing:
YES

Automatic Severity Source:
NO
```

## Handoff With Unresolved Scale

Scale이 미확정이어도:

```text
Genre
+
Project Mechanism
```

에서 명확한 Production Driver가 있으면 Handoff를 사용할 수 있다.

Trace:

```text
Scale Resolution State:
UNRESOLVED

Handoff Loaded:
YES

Activation Basis:
GENRE + PROJECT MECHANISM
```

Guard:

```text
Handoff
≠
Scale Classification
```

Handoff만으로 Solo/Micro Severity를 만들지 않는다.

---

# 18. GSC Runtime

Current canonical state:

```text
Active Independent GSC:
0

Retired Historical GSC:
3

Routing Specialization:
2
```

## Retired GSC

Historical trace only.

Active Finding Source 금지.

## Routing Specialization

- Management × Solo — Responsibility Level as Scope Cut Boundary
- Action × Solo — Iteration Throughput / Feel Polish Budgeting

둘 다:
- Core 아님
- automatic Severity Source 아님
- Reviewer Action Hint.

Scale Resolution이 `UNRESOLVED`이면 scale-specific Routing Specialization도 자동 Load하지 않는다.

---

# 19. PASS 9 — Market / Selection when applicable

Market / Selection Goal이 실제 Project Source에 있을 때만 Load한다.

## Market

Relevant canonical parents:
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

Market Risk와 Design Failure를 자동 Merge하지 않는다.

## Selection

지원사업 / 공모전 / 전시 / 대회 Goal이 명시될 때만.

- `SEL-001`
- `SEL-002`
- `SEL-003`

Award Fit ≠ Market Fit.

없으면:

`N/A`.

---

# 20. Reviewer Set Construction

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

기본 internal candidate budget:

```text
Universal:
max 5 + UC006 conditional

Primary Genre:
5~8 each

Secondary Genre:
2~4 each

Supporting Genre:
2~4 selected questions

Scale:
3~8 depending risk

Market / Selection:
only when applicable
```

이는 합격 threshold가 아니다.

## Project-specific Question Rule

좋은 질문:

> 현재 부상이 다음 파견 인력 선택을 실제로 바꾸는가?

나쁜 질문:

> Persistent State가 있는가?

변환:

```text
Core
↓
Project Mechanism
↓
Project-specific Reviewer Question
```

## Default Reviewer Questions

1. 핵심 Product Promise는 무엇인가?
2. 실제 반복 Verb는 무엇인가?
3. Verb가 어떤 State를 바꾸는가?
4. 그 결과가 다음 Decision을 바꾸는가?
5. Context가 Choice Value를 바꾸는가?
6. 중요한 Uncertainty에 Response Agency가 있는가?
7. 판단 전 Information이 Actionable한가?
8. 결과 후 Cause를 학습할 수 있는가?
9. Genre Mechanism이 실제 Core Loop에 있는가?
10. 숨은 Production Cost는 무엇인가?
11. Parent / Genre / Scale에서 같은 Root를 반복하고 있지 않은가?
12. 지금 수정할 문제인가?
13. 아니면 Cheap Test가 필요한 Claim인가?
14. Human Evidence가 필요한가?
15. 현재 정보로 알 수 없는 것은 무엇인가?

그대로 복사하지 않는다.

---

# 21. PASS 10 — Raw Finding Collection

Core마다 RF를 만들지 않는다.

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

Evidence Qualifier:

Potential Issue:

Potential Root:

Applicability:
- YES
- CONDITIONAL
- N/A

Applicability Note:

Knowledge Status:
- PROVISIONAL
- CANDIDATE
- ROUTING_HINT
- PROJECT_INTERNAL

Knowledge Confidence:

Needs Validation:
YES / NO
```

RAW_FINDING에는 `MULTI-SOURCE`를 사용하지 않는다.

사용자-facing final output이 아니다.

---

# 22. PASS 11 — Root Cause Merge / Split

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

Mitigation State:

Validation Required:
YES / NO
```

## Merge Conditions

1. same underlying mechanism
2. same Promise impact
3. same fix
4. same validation question

대부분 같으면 one root.

## Split Conditions

다음 중 하나라도 materially 다르면 split 검토.

- different root cause
- different fix
- different validation question
- different category
- Design vs Production

## Regression Examples

MCC:

```text
Predictable Autonomy
≠
ETA Information Utility
```

Magic Word:

```text
Sentence Decision Depth
≠
Grammar Availability
```

또한:

```text
Card Choice Design Risk
≠
Card Regression Production Risk
```

---

# 23. PASS 12 — Severity / Evidence Classification

반드시 세 축을 분리한다.

```text
Knowledge Confidence
≠
Project Evidence Strength
≠
Issue Severity
```

## Knowledge Confidence

Canonical Knowledge 자체의 Evidence Strength.

```text
VERY HIGH
HIGH
MEDIUM-HIGH
MEDIUM
LOW-MEDIUM
LOW
```

## Project Evidence Strength

```text
CONFIRMED
STRONG
PARTIAL
WEAK
UNKNOWN
```

### CONFIRMED
Current approved Source가 Root를 직접 명시하거나 논리적으로 확정.

### STRONG
여러 source/system relation이 같은 Root를 지지.

### PARTIAL
문제 가능성은 높지만 중요 mechanism 일부 미확정.

### WEAK
Inference 중심.

### UNKNOWN
핵심 정보 없음.

## Issue Severity

### CRITICAL
Core Loop / Product Promise / completion을 근본적으로 위협.

### HIGH
다음 단계 전에 수정 또는 검증해야 하는 주요 Risk.

### MEDIUM
품질 / 밸런스 / 흐름 / 제작효율 Risk.

### LOW
local optimization / polish / 후순위.

## Guardrails

금지:

```text
Provisional → HIGH
Candidate → LOW
3 rules triggered → Severity ×3
```

Candidate라도 HIGH Project Issue 가능.

High-confidence Core라도 LOW local issue 가능.

---

# 24. PASS 13 — Recommended Action / RF Schema

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

Confidence Note:

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

Mitigation State:
- NONE
- PLANNED
- CURRENTLY_MITIGATED
- PARTIALLY_MITIGATED
- UNKNOWN

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
DEFERRED

Unknowns:

Status Note:

Do Not Infer:
- ...
```

## Recommended Action Principle

새 시스템 추가가 기본 해법이 아니다.

우선:
- REMOVE
- REDUCE
- MERGE
- REFRAME
- CHANGE DEPENDENCY
- CHANGE SCOPE

를 검토한다.

`ADD RESPONSE PATH / ADD INFORMATION PATH`는 Root에 필요한 기능 역할을 말할 뿐 정확한 implementation을 확정하지 않는다.

## ACCEPTED_RISK

`ACCEPTED_RISK`는 issue 없음이 아니다.

확인:
- Risk awareness
- mitigation
- Product necessity
- next-stage blocking

`ACCEPTED_RISK`가 있다고 자동 `STRUCTURAL_RISK` Verdict를 만들지 않는다.

---

# 25. Internal Consistency Finding

Project document 자체 충돌은 Reference 없이 찾을 수 있다.

```text
IC_FINDING

ID:
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

IC와 Design RF가 같은 Root면 중복 생성하지 않는다.

---

# 26. Supported Structure

Reviewer는 Risk만 찾지 않는다.

수정 시 보호해야 할 구조를:

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

SS는 전체 Game PASS가 아니다.

의미:

> 현재 수정 과정에서 보존 가치가 높은 Constraint.

---

# 27. PASS 14 — Validation Need Classification

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

여기서 종료.

## Reviewer가 만들지 않는 것

- Test count
- Pass rate
- Win rate threshold
- Persona count
- Sample size
- Seed
- exact Metric criteria
- AI Tester implementation

## Action Class

### STRUCTURAL FIX FIRST
문서만으로 논리적 결함 확인.

예:
- impossible state
- contradiction
- missing required information path
- broken transition
- confirmed scope matrix

### VALIDATE FIRST
Human / Experience Claim.

예:
- choice tension
- fairness
- readability
- identity
- fatigue
- pacing
- feel

### NO ACTION YET
정보 부족 또는 후순위.

## Cheap Validation Route Hint

| Claim / Problem Type | Suggested Evidence Form |
|---|---|
| Rule / Number / Economy | Paper / Spreadsheet / Simple Simulation |
| Core Choice / Management Loop | Paper Prototype / Simple Web Prototype |
| UI Flow | Figma Prototype |
| Action / Physics / Feel | Unity Micro Prototype |
| Structural balance after playable prototype | AI Tester later |
| Fun / Readability / Tension | Human Test |
| Market demand / funnel | Market Test |

이는 상세 Test Plan이 아니다.

---

# 28. Machine / Human Guardrails

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
Human Can Execute
```

```text
Progression Unlock Exists
≠
Meaningful Growth
```

```text
State Persists
≠
State Changes Future Decisions
```

## Restart / Abandon

Batch runner restart ≠ player restart.

## Information

AI direct state access ≠ player inspected information.

## Action

Perfect-reaction AI success ≠ human reactability.

## Counterfactual Metrics

Formal definition 없이 다음을 machine fact로 만들지 않는다.

- First Critical Mistake
- Unrecoverable State
- Preventable Failure
- Bad-seed Failure
- Avoidable Death

표시:

`FORMAL DEFINITION REQUIRED`.

---

# 29. PASS 15 — Final Review Summary / Verdict

Reviewer Verdict는 기존 5개만 사용한다.

```text
REVIEW_CLEAR
REVIEW_CLEAR_WITH_VALIDATION
REVISION_REQUIRED
STRUCTURAL_RISK
INSUFFICIENT_SPEC
```

## Qualitative Verdict Precedence

### Step A — Blocking Unknown

Core Mechanism 자체를 판단할 수 없는 Blocking Unknown:

`INSUFFICIENT_SPEC`

일부 수치가 없다는 이유만으로 사용하지 않는다.

### Step B — Structural Risk

다음이면:

- `CONFIRMED / STRONG CRITICAL Structural Root`

또는:

- 여러 unresolved `HIGH Structural Root`가 Core Promise / Completion / Architecture를 직접 위협

`STRUCTURAL_RISK`

### Step C — Revision Required

다음 단계 전에 수정해야 하는:

```text
Severity:
HIGH

Action Class:
STRUCTURAL FIX FIRST
```

Root가 있으나 Architecture 전체 붕괴는 아니면:

`REVISION_REQUIRED`

### Step D — Review Clear With Validation

Blocking Structural Root가 없고 핵심 불확실성이 주로:

`VALIDATE FIRST`

이면:

`REVIEW_CLEAR_WITH_VALIDATION`

### Step E — Review Clear

Material Structural Root가 없고 즉시 해결할 Core Validation blocker도 없으면:

`REVIEW_CLEAR`

## Score 금지

금지:

```text
Critical = 5
High = 3
Risk Total → Verdict
```

Verdict는 qualitative precedence다.

## REVIEW_SUMMARY

```text
REVIEW_SUMMARY

Project:
Version:

Review Target:
Active Review Scope:
Deferred Systems:

Primary Genre:
Secondary Genre:

Scale Resolution State:
Scale Evidence State:
Scale:

Core Product Promise:

Reviewer Set:
- Universal:
- Genre:
- Scale:
- Handoff:
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

Enum Conformance:
- PASS / FAIL

Reviewer Verdict:
```

## Output Priority

사용자-facing 기본:

```text
Critical:
all

High:
max 5

Medium:
max 8

Low:
appendix / optional
```

내부 Finding 삭제 규칙이 아니다.

---

# 30. Finding Lifecycle

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

후속 Evidence Review에서:
- RESOLVED
- OPEN
- ACCEPTED_RISK

로 변경 가능.

## Re-review

같은 Root면 새 RF를 만들지 않는다.

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

`REGRESSION`

tag를 별도 기록한다.

Regression tag는 RF Status enum을 대체하지 않는다.

---

# 31. Runtime Modes

## QUICK

사용:
- early concept
- early pitch
- incomplete brief

출력:
- Mechanism summary
- Product Promise
- Top 3~5 risks
- major Unknown
- Validation Need

## STANDARD

기본.

- routing
- Root Finding
- Severity / Evidence
- Supported Structure
- Validation Need
- Verdict

## DEEP

- full trace
- Hybrid map
- Handoff cost shape
- Evidence Boundary
- lifecycle
- fuller medium-risk appendix

## Mode Guardrail

Mode는:

`Output Depth`

만 변경한다.

Core / Evidence / Severity Rule은 동일.

## Development Stage Sensitivity

### CONCEPT
Promise / Mechanism / Scope / contradiction 우선.

### PAPER PROTOTYPE
Decision / loop / resource-state relation.

### CONCEPT TEST MODEL
Core claim / minimum executable mechanism.

### DIGITAL PROTOTYPE
formal rule / structural balance / instrumentation readiness.

### VERTICAL SLICE
Human readability / UX / feel / content-production reality.

### PRODUCTION
regression / throughput / content consistency / ownership.

### PRE-LAUNCH
onboarding / balance / product-facing quality / market-facing claim consistency.

Stage는 Severity 기준을 바꾸지 않는다.

---

# 32. Enum Registry & Conformance

Canonical Enum Field에는 정의된 값 하나만 저장한다.

설명은 Qualifier / Note에 둔다.

## Optional Qualifier Fields

```text
Evidence Qualifier:
Scope State:
Mitigation State:
Confidence Note:
Applicability Note:
Status Note:
Validation Timing:
Review Scope Note:
Scale Evidence Note:
```

## Object-specific Knowledge Status

### RAW_FINDING

```text
PROVISIONAL
CANDIDATE
ROUTING_HINT
PROJECT_INTERNAL
```

### RF_FINDING

```text
PROVISIONAL
CANDIDATE
PROJECT_INTERNAL
MULTI-SOURCE
```

객체별 enum을 혼합하지 않는다.

## Core Canonical Enum Registry

### Evidence State

```text
KNOWN
INFERRED
UNKNOWN
```

### Claim Status

```text
STRUCTURALLY SUPPORTED
PARTIALLY SUPPORTED
UNSUPPORTED
UNKNOWN
VALIDATION_REQUIRED
```

### Validation Needed

```text
YES
NO
```

### Applicability

```text
YES
CONDITIONAL
N/A
```

### Knowledge Confidence

```text
VERY HIGH
HIGH
MEDIUM-HIGH
MEDIUM
LOW-MEDIUM
LOW
```

### Project Evidence Strength

```text
CONFIRMED
STRONG
PARTIAL
WEAK
UNKNOWN
```

### Issue Severity

```text
CRITICAL
HIGH
MEDIUM
LOW
```

### RF Status

```text
OPEN
NEEDS_INFO
VALIDATION_REQUIRED
RESOLVED
ACCEPTED_RISK
```

### Action Class

```text
STRUCTURAL FIX FIRST
VALIDATE FIRST
NO ACTION YET
```

### Validation Need

```text
NONE
VALIDATION_REQUIRED
```

### Suggested Evidence Type

```text
SIMPLE MODEL
SELF TEST
HUMAN TEST
AI TESTER
MARKET TEST
HYBRID
NONE
```

### Reviewer Verdict

```text
REVIEW_CLEAR
REVIEW_CLEAR_WITH_VALIDATION
REVISION_REQUIRED
STRUCTURAL_RISK
INSUFFICIENT_SPEC
```

### Scale Resolution State

```text
RESOLVED
UNRESOLVED
```

### Scale Evidence State

```text
KNOWN
INFERRED
UNKNOWN
```

### Scale

```text
SOLO
MICRO
SMALL
MID+
```

## Validation Needed Rule

`Validation Needed`에는:

```text
YES
NO
```

만 사용.

금지:
- LATER
- MAYBE
- OPTIONAL
- DEFERRED

시점:

```text
Validation Timing:
LATER
```

로 분리.

## ENUM_CONFORMANCE_CHECK

모든 Runtime Object 생성 후 사용자-facing 출력 직전에 실행.

검사:

- Evidence State
- Claim Status
- Validation Needed
- Applicability
- Knowledge Status
- Knowledge Confidence
- Project Evidence Strength
- Issue Severity
- RF Status
- Action Class
- Validation Need
- Suggested Evidence Type
- Reviewer Verdict
- Scale Resolution State
- Scale Evidence State
- Scale

Undefined value 발견 시:

1. Canonical enum 값 하나로 정규화
2. 추가 의미를 Note / Qualifier로 이동
3. Summary와 object 불일치 재검사

Result:

```text
Enum Conformance:
PASS / FAIL
```

---

# 33. Determinism / Version Trace

## Review Snapshot

```text
REVIEW_RUNTIME_VERSION:
REVIEWER_RUNTIME_v1.0

Studio Core:
v0.4

Genre Master:
v0.3

Scale Baseline:
v0.2

Loaded Genre Baselines:
- ...

Project Version:

Review Target:

Active Review Scope:
- ...

Mode:
- QUICK
- STANDARD
- DEEP

Review Date:
```

## Determinism Input

동일:

- Project Version
- Canonical Version
- Runtime Version
- Mode
- Review Target
- Active Review Scope

이면 가능한 한 동일한:
- Genre routing
- Applicability
- loaded Core
- Root finding
- trace

를 재현해야 한다.

문장 표현은 달라도 구조 판정은 안정적이어야 한다.

## Formal Engine Candidates

향후 deterministic engine으로 분리 가능:

- genre routing score
- core loading
- status filtering
- version trace
- enum validation
- schema validation
- finding lifecycle
- dedup reference graph

LLM 영역:

- mechanism meaning
- promise interpretation
- root synthesis
- question generation
- relevance
- recommended action

---

# 34. Runtime Data Structures

v1.0 최소 Object:

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

`VALIDATION_PLAN_OBJECT`

---

# 35. Evidence Boundary Registry

두 Dry-run에서 충분히 직접 시험되지 않은 Runtime Branch:

- MICRO scale
- SMALL scale
- MID+ scale
- Deduction Primary
- Narrative Primary
- Action Primary
- explicit Market Routing
- explicit Selection Routing
- post-validation Finding Lifecycle
- Regression Finding lifecycle

이것은 Runtime Failure가 아니다.

## Under-tested Branch Behavior

호출될 경우:

1. 기존 Canonical Rule 사용 가능.
2. Evidence Boundary를 출력.
3. Dry-run coverage가 적다는 이유만으로 자동 Failure 처리하지 않는다.
4. 필요한 경우 후속 Runtime fixture를 추가할 수 있다.
5. Canonical Knowledge Confidence를 Runtime coverage 때문에 임의 하향하지 않는다.

---

# 36. Regression Fixtures

Fixtures는 Runtime regression 확인용이다.

Game Design Knowledge Promotion Evidence가 아니다.

## FIXTURE-01 — Project MCC

Expected:

```text
Project:
MCC v0.5

Review Target:
PROTOTYPE SLICE

Primary:
Strategy L3
Management L3

Secondary:
Simulation L2

Supporting:
Narrative L1

Scale Resolution State:
RESOLVED

Scale Evidence State:
KNOWN

Scale:
SOLO

UC006:
Inactive in reviewed slice

Duplicate RF:
0

Validation Planner Leakage:
0

Scope Regression:
0
```

Checks:
- Full Product feature가 Prototype violation으로 자동 Load되지 않는가?
- UC006가 full-project progression 존재만으로 active 되지 않는가?
- Management / Strategy / Simulation duplicate Severity가 제거되는가?
- Solo Handoff가 Design RF로 섞이지 않는가?

## FIXTURE-02 — Magic Word Deckbuilding

Expected:

```text
Project:
Magic Word v0.9

Review Target:
FULL PROJECT

Primary:
Deckbuilding L3

Secondary:
Roguelike L2
Strategy L2

Supporting:
RPG L1

Scale Resolution State:
UNRESOLVED

Scale Evidence State:
UNKNOWN

Scale:
[blank]

UC006:
Knowledge Status = CANDIDATE
Applicability = CONDITIONAL

Duplicate RF:
0

Validation Planner Leakage:
0

Enum Regression:
0
```

Checks:
- Card UI만으로 Deck L3가 되지 않는가?
- Roguelike label만으로 L3가 되지 않는가?
- RPG가 progression 존재만으로 과대 Load되지 않는가?
- Unknown Scale을 SOLO로 추정하지 않는가?
- Handoff는 Genre + Mechanism으로 조건부 Load 가능한가?
- UC006 Candidate status가 보존되는가?

---

# 37. Anti-pattern Registry

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

## AP-RUNTIME-022 — Guess Unresolved Scale

Project Source에 Team Scale Evidence가 없는데:

```text
Scale:
SOLO
```

등을 임의 지정.

## AP-RUNTIME-023 — UNKNOWN as Team Scale

잘못된 예:

```text
Scale:
UNKNOWN
```

Missing Evidence와 Team Category를 혼합한다.

정상:

```text
Scale Resolution State:
UNRESOLVED

Scale Evidence State:
UNKNOWN

Scale:
[blank]
```

---

# 38. Self-Review

## Runtime Architecture

- PASS 0~15 unchanged? → `PASS`

## Scope

- Review Target / Active / Deferred integrated? → `PASS`
- Deferred dependency exception included? → `PASS`

## Verdict

- Five verdicts unchanged? → `PASS`
- Qualitative precedence standalone? → `PASS`
- Score verdict prohibited? → `PASS`

## Enum

- Correction Note 없이 이해 가능? → `PASS`
- Object-specific Knowledge Status included? → `PASS`
- Validation Needed YES/NO only? → `PASS`

## Scale

- RD-004 resolved? → `PASS`
- UNKNOWN added as Scale category? → `NO`
- unresolved Scale blocks Scale Core? → `YES`
- Genre/Mechanism Handoff still possible? → `YES`

## Universal

- UC001~005 Applicability Gate? → `PASS`
- UC006 Candidate / Conditional? → `PASS`

## Genre

- L0~L3 unchanged? → `PASS`
- Candidate loading unchanged? → `PASS`

## GSC

- Active Independent = 0? → `PASS`
- retired GSC not active? → `PASS`

## Handoff

- Core promotion? → `NO`
- automatic Severity source? → `NO`

## Root

- One Root = One RF? → `PASS`
- split rules preserve Design / Production distinction? → `PASS`

## Evidence

```text
Knowledge Confidence
≠
Project Evidence Strength
≠
Issue Severity
```

→ `PASS`

## Validation

- detailed Planner blocked? → `PASS`
- Suggested Evidence Type only? → `PASS`

## Regression Fixtures

- MCC included? → `PASS`
- Magic Word included? → `PASS`

## Evidence Boundary

- under-tested branches stated? → `PASS`

## Canonical Knowledge

- Core Status changed? → `NO`
- Confidence changed? → `NO`
- Genre routing score changed? → `NO`

---

# 39. Final Position

## A. Reviewer Runtime v1.0의 핵심 목적은?

현재 Project의 Mechanism / Product Promise에 필요한 Canonical Knowledge만 Load하고:

```text
Project Signal
↓
Raw Finding
↓
Root Cause
↓
ONE RF
```

로 압축하여:
- Structural Risk
- Supported Structure
- Needs Info
- Validation Need

를 분리하는 것이다.

---

## B. v0.1 대비 어떤 Runtime Execution Rule이 통합됐는가?

### 1. Review Target Scope

```text
Review Target
Active Review Scope
Deferred Systems
Prototype-only Simplifications
Out-of-Scope Systems
```

을 Input / Snapshot / Determinism에 통합.

### 2. Verdict Precedence

```text
INSUFFICIENT_SPEC
→ STRUCTURAL_RISK
→ REVISION_REQUIRED
→ REVIEW_CLEAR_WITH_VALIDATION
→ REVIEW_CLEAR
```

qualitative precedence를 PASS 15에 통합.

### 3. Enum Conformance

Canonical field = defined enum one value.

설명은 Qualifier / Note로 분리.

사용자-facing 출력 전:

`ENUM_CONFORMANCE_CHECK`.

### 4. Unresolved Scale

```text
Scale Resolution State:
RESOLVED / UNRESOLVED

Scale Evidence State:
KNOWN / INFERRED / UNKNOWN
```

을 추가.

Unresolved이면 Scale field는 비워둔다.

---

## C. Canonical Knowledge 변경이 있었는가?

`NO`

---

## D. PASS Architecture 변경이 있었는가?

`NO`

PASS 0~15 유지.

---

## E. RD-001~004 상태는?

```text
RD-001:
INTEGRATED / CLOSED

RD-002:
INTEGRATED / CLOSED

RD-003:
INTEGRATED / CLOSED

RD-004:
INTEGRATED / CLOSED
```

---

## F. Scale 정보가 없는 Project를 어떻게 처리하는가?

```text
Scale Resolution State:
UNRESOLVED

Scale Evidence State:
UNKNOWN

Scale:
[blank]
```

- Scale Core 미로드
- Scale-specific specialization 미로드
- Team-relative feasibility Verdict 금지
- 필요한 Team info는 `NEEDS_INFO`

---

## G. Scale unresolved인데 Genre Production Handoff는 사용할 수 있는가?

`YES — CONDITIONAL`

조건:

```text
Genre
+
Actual Project Mechanism
+
Production Driver
```

가 명확해야 한다.

Trace:

```text
Activation Basis:
GENRE + PROJECT MECHANISM
```

단 Handoff로 Scale classification / Solo Severity를 만들지 않는다.

---

## H. UC006 상태는?

```text
Knowledge Status:
CANDIDATE

Runtime:
CONDITIONAL DIAGNOSTIC
```

Progression이 실제 Product Promise일 때만 Applicability `CONDITIONAL`.

Vertical Power 자체는 결함이 아니다.

---

## I. Validation Planner는 Core Runtime의 다음 필수 단계인가?

`NO`

Reviewer는:

```text
VALIDATION_REQUIRED
+
Claim
+
Suggested Evidence Type
```

에서 멈춘다.

---

## J. Runtime이 실제 두 Project에서 검증됐는가?

`YES`

Validated:
- Project MCC v0.5
- Magic Word Deckbuilding v0.9

그러나 모든 Genre / Scale branch가 검증됐다고 주장하지 않는다.

---

## K. 남은 Evidence Boundary는?

- MICRO
- SMALL
- MID+
- Deduction Primary
- Narrative Primary
- Action Primary
- explicit Market
- explicit Selection
- post-validation lifecycle
- regression lifecycle

---

## L. v1.0이 Studio OS Canonical Package에 들어갈 준비가 되었는가?

`YES`

Basis:

```text
Blocking Runtime Defect:
0

Major Runtime Defect:
0

RD-001~004:
INTEGRATED / CLOSED

Cross-project Generalization:
CONFIRMED WITH BOUNDED COVERAGE
```

---

## M. 다음 단계는?

```text
Reviewer Runtime v1.0
✅
↓
Studio OS Canonical Document Manifest
↓
Studio OS Core Package v1.0
```

Validation Planner는 현재 필수 Roadmap 단계가 아니다.

---

# 40. Source Trace

## Runtime Baseline

- `REVIEWER_RUNTIME_SPECIFICATION_v0.1_APPROVED.md`

## Runtime Correction

- `REVIEWER_RUNTIME_CORRECTION_NOTE_01_v0.1.md`

## Dry-run #1

- `REVIEWER_RUNTIME_DRYRUN_01_PROJECT_MCC_v0.1.md`
- `REVIEWER_RUNTIME_DEFECT_LOG_01_v0.1.md`

## Dry-run #2

- `REVIEWER_RUNTIME_DRYRUN_02_MAGIC_WORD_v0.1.md`
- `REVIEWER_RUNTIME_DEFECT_LOG_02_v0.1.md`

## Cross Assessment

- `REVIEWER_RUNTIME_CROSS_DRYRUN_ASSESSMENT_v0.1.md`

## Canonical Knowledge

- `Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`
- `GENRE_CORE_MASTER_INDEX_v0.3.md`
- `SCALE_CORE_BASELINE_v0.2.md`

## v1.0 Consolidation Rule

Dry-run은:

`Runtime Validation Evidence`

이다.

다음으로 사용하지 않는다.

```text
Game Design Core Promotion Evidence
Genre Promotion Evidence
Scale Promotion Evidence
Confidence Upgrade Evidence
```

이 문서는 Runtime execution baseline이며 Canonical Game Design Knowledge의 Status를 변경하지 않는다.
