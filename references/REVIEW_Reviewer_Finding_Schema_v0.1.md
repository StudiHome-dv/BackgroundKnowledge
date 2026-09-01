# Studio OS — Reviewer Finding Schema v0.1

**Document ID:** `REVIEW_Reviewer_Finding_Schema`  
**Version:** `v0.1`  
**Status:** `DRAFT_FOR_REVIEW`  
**Parent:** `00_Studio_OS_Index v0.1 — APPROVED_BASELINE`

---

# 0. Purpose

`Reviewer Finding(RF)`은 **Game Design Reviewer가 발견한 중요한 판단·위험·불확실성을 Validation Planner로 전달하기 위한 표준 Handoff 단위**다.

RF의 목적은 테스트 방법을 완성하는 것이 아니다.

- Game Design Reviewer: **무엇이 문제이거나 검증이 필요한가?**
- Reviewer Finding: **그 판단을 추적 가능한 형태로 기록한다.**
- Validation Planner: **그 Finding을 어떤 Hypothesis와 Test Plan으로 검증할 것인가?**

따라서 RF에는 Metric, Pass/Fail Threshold, Run Count, Persona 구성 같은 상세 Test Plan을 넣지 않는다.

---

# 1. Core Rule

하나의 RF에는 가능한 한 **하나의 핵심 Finding만** 기록한다.

나쁜 예:

> 경제가 불안정하고 전략 다양성이 낮으며 후반이 지루할 수 있다.

권장:

- `RF-001` — 자원 경제가 특정 구간에서 붕괴할 위험
- `RF-002` — 단일 전략이 지배 전략이 될 위험
- `RF-003` — 후반 반복 피로가 발생할 위험

---

# 2. Required Fields

## 2.1 `reviewer_finding_id`

고유 식별자.

권장 형식:

```text
RF-{PROJECT}-{###}
```

예:

```text
RF-VI-001
RF-MSC-003
```

---

## 2.2 `title`

Finding을 한 줄로 식별할 수 있는 짧은 이름.

예:

```text
Potential Dominant Strategy in Contract Selection
```

---

## 2.3 `statement`

Reviewer가 실제로 내린 핵심 판단.

조건:

- 모호한 감상 대신 구체적인 설계 위험 또는 불확실성을 기술한다.
- 아직 검증되지 않은 내용은 사실처럼 단정하지 않는다.
- 가능하면 한 개의 주장만 포함한다.

예:

```text
현재 보상 구조에서는 특정 의뢰 유형이 위험 대비 기대값에서 지속적으로 우세하여,
다른 의뢰 유형의 선택 가치를 약화시킬 가능성이 있다.
```

---

## 2.4 `finding_kind`

Finding의 성격.

허용 값:

```text
RISK
UNCERTAINTY
CONTRADICTION
SCOPE_RISK
STRENGTH_TO_VALIDATE
CONSTRAINT
```

설명:

- `RISK` — 현재 설계가 실패 원인이 될 수 있음
- `UNCERTAINTY` — 중요하지만 기획만으로 판단 불가능
- `CONTRADICTION` — 기획 규칙 또는 목표 간 충돌
- `SCOPE_RISK` — 제작 범위/비용/QA 위험
- `STRENGTH_TO_VALIDATE` — 핵심 강점으로 예상되지만 실제 검증 필요
- `CONSTRAINT` — 이후 Validation/Production에서 반드시 지켜야 할 제한

---

## 2.5 `priority`

Finding이 프로젝트에 미치는 중요도.

```text
P0
P1
P2
```

정의:

- `P0` — 실패 시 Core Concept, Prototype Entry 또는 프로젝트 지속 여부를 재검토해야 함
- `P1` — 중요하지만 구조 수정으로 해결 가능한 핵심 위험
- `P2` — Balance / Polish / 최적화 수준의 개선 항목

P0는 Reviewer 총점보다 우선할 수 있다.

---

## 2.6 `review_domains`

Finding이 발생한 Reviewer 평가 영역.

복수 선택 가능.

권장 값:

```text
DESIGN_QUALITY
SPECIALIZED_DESIGN
PRODUCTION_FEASIBILITY
SCOPE
MARKET_COMMERCIAL
ORIGINALITY_POSITIONING
PLAYER_EXPERIENCE
RED_TEAM
OTHER
```

---

## 2.7 `why_it_matters`

이 Finding이 실제 게임 또는 프로젝트 결과에 왜 중요한지 기록한다.

예:

```text
지배 전략이 존재하면 Meaningful Choice와 Replayability가 동시에 약화되고,
다수 콘텐츠를 제작해도 실제 사용 폭이 좁아질 수 있다.
```

---

## 2.8 `source`

Finding의 추적 가능성을 위한 출처 정보.

최소 포함:

```yaml
source:
  reviewer_report:
  design_document:
  reviewer_sections: []
```

예:

```yaml
source:
  reviewer_report: GAME_VI_Final_Review_v0.4
  design_document: Villain_Inc_GDD_v0.8
  reviewer_sections:
    - Design Quality / Meaningful Choice
    - Red Team Review
```

---

## 2.9 `validation_required`

Validation Planner로 넘겨 실제 검증 계획을 만들어야 하는지 여부.

```text
YES
NO
```

일반적으로:

- P0 / P1 + 검증 가능한 불확실성 → `YES`
- 문서만 수정하면 해결되는 명백한 모순 → 상황에 따라 `NO`
- 단순 제작 제약 기록 → `NO` 가능

---

# 3. Optional Handoff Fields

## 3.1 `validation_hint`

Reviewer가 예상하는 검증 방식에 대한 **힌트**다.
Validation Planner의 최종 결정이 아니다.

복수 선택 가능:

```text
MACHINE_PRE
MACHINE_POST
HUMAN
EXTERNAL
UNKNOWN
```

예:

```yaml
validation_hint:
  - MACHINE_PRE
  - MACHINE_POST
```

---

## 3.2 `related_reference`

Finding 판단에 실제 사용한 Reference만 기록한다.

예:

```yaml
related_reference:
  - REF-14 Mini Metro
  - REF-16 Invisible Inc.
```

Reference Library 전체를 다시 나열하지 않는다.

---

## 3.3 `design_constraint`

Validation 또는 수정 과정에서 훼손하면 안 되는 핵심 기획 의도.

예:

```text
위험한 선택 자체를 제거하지 말 것. 위험과 보상의 Trade-off를 유지한 상태에서 조정할 것.
```

이 필드는 Validation Planner가 단순히 문제를 제거하는 과정에서 Core Identity를 훼손하는 것을 방지한다.

---

## 3.4 `notes`

기타 필요한 보충 정보.

필수 정보가 아닌 내용만 기록한다.

---

# 4. Lifecycle Fields

## 4.1 `status`

RF의 현재 상태.

```text
OPEN
HANDED_OFF
RESOLVED
SUPERSEDED
CLOSED_NO_VALIDATION
```

정의:

- `OPEN` — Reviewer가 생성했으며 아직 Planner 처리 전
- `HANDED_OFF` — Validation Planner가 하나 이상의 Hypothesis로 변환함
- `RESOLVED` — 기획 수정 또는 Evidence로 문제가 해결됨
- `SUPERSEDED` — 새 RF 또는 최신 기획으로 대체됨
- `CLOSED_NO_VALIDATION` — 별도 테스트 없이 문서/Scope 수정으로 종료됨

---

## 4.2 `linked_hypotheses`

Validation Planner가 생성한 Hypothesis ID.

Reviewer 생성 시에는 비어 있을 수 있다.

예:

```yaml
linked_hypotheses:
  - HYP-VI-001
  - HYP-VI-002
```

하나의 RF에서 여러 Hypothesis가 파생될 수 있다.

---

# 5. Canonical RF Template

```yaml
reviewer_finding_id: RF-{PROJECT}-{###}

title:
statement:

finding_kind: RISK | UNCERTAINTY | CONTRADICTION | SCOPE_RISK | STRENGTH_TO_VALIDATE | CONSTRAINT
priority: P0 | P1 | P2

review_domains:
  -

why_it_matters:

source:
  reviewer_report:
  design_document:
  reviewer_sections:
    -

validation_required: YES | NO

validation_hint:
  - MACHINE_PRE | MACHINE_POST | HUMAN | EXTERNAL | UNKNOWN

related_reference:
  -

design_constraint:

status: OPEN
linked_hypotheses: []

notes:
```

---

# 6. Minimal RF Template

Game Design Reviewer가 매번 긴 RF를 작성하지 않아도 되도록 최소형을 허용한다.

```yaml
reviewer_finding_id:
title:
statement:
finding_kind:
priority:
review_domains:
why_it_matters:
source:
validation_required:
status: OPEN
```

`validation_hint`, `related_reference`, `design_constraint`, `notes`는 필요할 때만 추가한다.

---

# 7. Example

```yaml
reviewer_finding_id: RF-VI-001

title: Contract Selection Dominant Strategy Risk

statement: >
  현재 보상 구조에서는 특정 의뢰 유형이 위험 대비 기대값에서 지속적으로 우세하여,
  다른 의뢰 유형의 선택 가치를 약화시킬 가능성이 있다.

finding_kind: RISK
priority: P0

review_domains:
  - DESIGN_QUALITY
  - RED_TEAM

why_it_matters: >
  하나의 의뢰 유형이 반복적으로 최적해가 되면 Meaningful Choice가 약화되고,
  의뢰 콘텐츠의 실질적인 사용 다양성도 감소할 수 있다.

source:
  reviewer_report: GAME_VI_Final_Review_v0.4
  design_document: Villain_Inc_GDD_v0.8
  reviewer_sections:
    - Design Quality / Meaningful Choice
    - Red Team Review

validation_required: YES

validation_hint:
  - MACHINE_PRE
  - MACHINE_POST

related_reference:
  - REF-16 Invisible Inc.

design_constraint: >
  고위험 의뢰의 존재와 Risk/Reward 선택 자체는 유지해야 한다.

status: OPEN
linked_hypotheses: []

notes:
```

---

# 8. Reviewer / Planner Boundary

Reviewer Finding에는 아래 항목을 넣지 않는다.

```text
Specific Metric Formula
Pass Threshold
Warning Threshold
Fail Threshold
AI Persona Count
Simulation Run Count
Seed Count
Sensitivity Range
Stop Condition
Detailed Test Procedure
```

위 항목은 모두 Validation Planner의 책임이다.

Reviewer는 다음까지만 말한다.

> 무엇이 위험한가?  
> 왜 중요한가?  
> 검증이 필요한가?  
> 어떤 종류의 검증이 적절해 보이는가?

Validation Planner가 그 다음을 설계한다.

---

# 9. RF Generation Rule for Game Design Reviewer

Game Design Reviewer는 Final Review 종료 시 모든 지적사항을 RF로 변환하지 않는다.

RF 생성 대상:

1. Prototype Entry에 영향을 주는 P0 / P1 위험
2. Prototype Must-Prove 항목
3. 기획만으로 결론내릴 수 없는 중요한 불확실성
4. 핵심 강점이지만 실제 플레이에서 반드시 증명되어야 하는 주장
5. Scope / Production을 무너뜨릴 수 있는 구조적 위험
6. 추후 Evidence로 추적해야 하는 중요한 설계 판단

RF로 만들지 않아도 되는 것:

1. 단순 문구 수정
2. 오탈자
3. 즉시 고칠 수 있는 명백한 문서 불일치
4. 중요도가 낮은 P2 Polish 아이디어
5. 단순 Feature 제안

---

# 10. Definition of Done — Reviewer Finding Schema v0.1

다음 조건을 만족하면 승인한다.

- Reviewer와 Validation Planner 사이의 책임 경계가 명확하다.
- 하나의 RF가 하나의 핵심 Finding을 표현한다.
- P0 / P1 / P2 우선순위가 정의되어 있다.
- Source Traceability가 존재한다.
- Validation 필요 여부를 표현할 수 있다.
- Validation 방식은 Hint로만 전달한다.
- 하나의 RF에서 여러 Hypothesis로 연결 가능하다.
- RF Lifecycle을 추적할 수 있다.
- 상세 Test Plan 정보가 RF에 침범하지 않는다.

승인 후 Status:

```text
APPROVED_BASELINE
```

---

# 11. Next Step

Reviewer Finding Schema 승인 후 다음 문서를 설계한다.

```text
REVIEW_Validation_Handoff_Schema_v0.1
```

그 다음:

```text
VALID_Hypothesis_Schema_v0.1
```

---

# END
