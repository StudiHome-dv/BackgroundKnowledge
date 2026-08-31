# DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1

**Studio OS — Deduction / Information Genre Core Deep Extraction**  
**Document:** `DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1`  
**Status:** `APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE`  
**Purpose:** 신규 Deduction / Investigation / Information Puzzle / Identification / Language Decoding / Mystery Adventure / Information-processing Hybrid 기획 평가용 Genre-specific Reviewer Knowledge Base  
**Baseline:** `STUDIO_CORE_CANDIDATES_v0.2`  
**Extraction Prompt:** `Studio OS — Deduction / Information Genre Core Deep Extraction Prompt v0.1`  
**Provisional Genre Cores:** `GC-DEDUCT-001`, `GC-DEDUCT-003`, `GC-DEDUCT-004`  
**Candidates:** `GC-DEDUCT-005 ~ GC-DEDUCT-008`, `GC-DEDUCT-010 ~ GC-DEDUCT-012`  
**Merge Candidate:** `GC-DEDUCT-009 → GC-DEDUCT-001 Sub-rule`  
**Reclassified:** `GC-DEDUCT-002 → Product / Content Consumption Core Candidate`  
**Pending:** `Additional Evidence / Prototype Validation / Internal Evidence`  
**Evidence Rule:** Pure Deduction Design Evidence를 최우선으로 사용하며, Production-heavy / Information-processing / Investigation Hybrid Reference는 보조·반례·Boundary 설정에만 사용한다.

---

# 1. Executive Summary

이번 Deep Extraction의 핵심 결론은 다음과 같다.

1. **Deduction의 핵심은 Hidden Information이 아니라 `Evidence Relation → Hypothesis Space Reduction → Player-owned Conclusion`이다.**
   - 단서가 많아도 한 단서를 클릭하면 정답이 나오면 Deduction Depth가 약하다.
   - 정보가 적어도 공간·시간·관계·언어 단서를 조합해야 하나의 결론이 남는다면 강한 Deduction 구조가 될 수 있다.

2. `Information Processing`과 `Deduction`은 분리해야 한다.
   - `Information Processing`: 이미 주어진 Rule을 데이터에 적용해 Correct Processing을 수행.
   - `Deduction`: 복수 Evidence 관계를 플레이어가 구성하여 Hidden Conclusion을 생성.
   - Papers, Please는 강한 Information Processing 사례지만 Pure Deduction의 단독 Primary Evidence로 사용하지 않는다.

3. 기존 `GC-DEDUCT-001 — The Game Should Manage Evidence, not Solve the Inference`는 **STRENGTHEN / PROVISIONAL CORE 유지**가 맞다.
   - 다만 두 개의 별도 Core로 분리하지 않고 하나의 Trade-off Core로 유지한다.
   - `Memory/Search Externalization`과 `Inference Ownership`은 서로 독립 기능이 아니라 **UI가 어디까지 도와야 하는가**라는 동일 설계 문제의 양쪽 경계이기 때문이다.

4. 기존 `GC-DEDUCT-002 — Low Replayability is not automatically a defect`는 **RECLASSIFY**가 적절하다.
   - 중요한 판단이지만 Deduction Mechanism 자체보다 `Solution Knowledge Consumption / First-play Value / Product Value Model` 문제에 가깝다.
   - 따라서 Genre Design Core에서는 제외하고 `Product / Content Consumption Core Candidate`로 이동한다.

5. 신규 Provisional Deduction Core로 가장 강한 것은 두 개다.
   - `GC-DEDUCT-003 — Evidence Relations Must Make the Conclusion Logically Reachable`
   - `GC-DEDUCT-004 — Validation Design Must Preserve Reasoning`

6. 즉 현재 우선 Provisional Genre Core는 총 3개다.
   - `GC-DEDUCT-001`
   - `GC-DEDUCT-003`
   - `GC-DEDUCT-004`

7. 다음 항목은 매우 중요하지만 현재 Reference Pool의 Direct Design Evidence가 부족해 Candidate로 유지한다.
   - Evidence Accessibility
   - Single-point Bottleneck / Redundancy
   - Hypothesis Space Calibration
   - Stuck-state Recovery
   - Memory / Search Burden
   - Knowledge Recontextualization
   - Deduction Pacing
   - Multiple Reasoning Paths

8. 현재 Source Weight는 보수적으로 잡는다.
   - `REF-17 Return of the Obra Dinn` → **Tier A / Primary Design**
   - `REF-30 The Case of the Golden Idol` → **Tier B / Production-heavy Deduction Support**
   - `REF-31 Chants of Sennaar` → **Tier B / Production-heavy Language Deduction Support**
   - `REF-29 Strange Horticulture` → **Tier B / Production-heavy Identification Support**
   - `REF-01 Papers, Please` → **Tier B / Information Processing Hybrid**
   - `REF-48 The Operator` → **Tier B / Commercial-heavy Investigation Support**

9. Deduction의 반복 Anti-Pattern은:
   - Hidden Information ≠ Deduction
   - Single Clue Gives the Answer
   - Missing Critical Evidence
   - Memory Test Disguised as Deduction
   - Search Burden Disguised as Depth
   - UI Solves the Inference
   - Brute-force Beats Reasoning
   - Instant Validation Leak
   - No Validation / No Learning
   - Hint Gives Conclusion
   - Single-point Clue Bottleneck
   - False Complexity
   - Arbitrary Solution
   - External Knowledge Dependency
   - Revelation without Player Inference

10. Formal / Machine Validation은 이 장르에서 매우 강하지만, **Human Reasoning Difficulty를 대체하지 않는다.**
    - Machine: Evidence Graph, Reachability, Solution Count, Dependency, Brute-force vulnerability.
    - Human: Inference Ownership, Evidence Sufficiency Experience, Aha, Fairness, Cognitive Load, Search/Memory Burden.

11. Deduction Reviewer의 가장 중요한 질문은 다음과 같다.

> **“플레이어가 정답을 발견하는가, 아니면 게임이 정리해 준 정보를 확인하는가?”**

조금 더 구조적으로는:

> **“결론에 필요한 Evidence가 충분히 존재하고, 그 Evidence 사이의 관계를 플레이어가 직접 구성하며, Validation이 Guess보다 Reasoning을 유리하게 만드는가?”**

12. 현재 가장 큰 Evidence Gap은:
   - Human Inference Explanation
   - Stuck Reason
   - Hint Dependency
   - Brute-force 실제 행동
   - Observation vs Reasoning Time
   - Critical Clue Miss
   - Alternate Reasoning Paths
   - Validation Leakage
   - External Note Dependency
   - Underperforming Deduction Control Cases

---

# 2. Deduction / Information Genre Definition

Studio OS에서는 “추리 소재”와 “추리 Mechanism”을 분리한다.

## 2.1 Information Processing

이미 주어진 규칙을 사용해 정보를 확인·분류·처리한다.

```text
Known Rule
+
Observed Data
↓
Correct Processing
```

예:
- 문서 규칙 확인
- 조건 일치 여부 판정
- 주어진 카테고리 분류
- 명시적 절차 준수

이 구조도 깊고 재미있을 수 있지만 Pure Deduction과 같은 평가기준을 적용하지 않는다.

---

## 2.2 Deduction

여러 Evidence 사이의 관계를 플레이어가 구성해 Hidden Conclusion을 만든다.

```text
Evidence A
+
Evidence B
+
Context C
↓
Relation Construction
↓
Hypothesis
↓
Cross-check
↓
Conclusion
```

핵심은 정보량이 아니라:

> **플레이어가 어떤 관계를 직접 구성해야 하는가**

다.

---

## 2.3 Deduction Inclusion Test

### A. Hidden Conclusion
플레이어가 직접 밝혀야 하는 미확정 정보가 존재하는가?

가능한 형태:
- Identity
- Cause
- Sequence
- Relationship
- Location
- Meaning
- Ownership
- Rule
- Motive

### B. Evidence Availability
정답에 필요한 Evidence가 게임 안에 존재하는가?

### C. Evidence Relation
둘 이상의 Evidence 또는 Context를 연결해야 하는가?

### D. Player-owned Inference
게임이 Evidence를 자동 결합해 Conclusion을 완성하지 않는가?

### E. Hypothesis Space
둘 이상의 가능한 설명이 존재하며 Evidence가 이를 줄이는가?

### F. Validation
Hypothesis를 확인하거나 반박할 방법이 있는가?

### G. Learnable Stuck State
막혔을 때 무엇을 다시 관찰·비교·재해석할지 찾을 수 있는가?

---

## 2.4 Studio OS Deduction Core Loop

```text
Observe
   ↓
Collect / Notice Evidence
   ↓
Organize Information
   ↓
Find Relationships
   ↓
Generate Hypothesis
   ↓
Test / Cross-check
   ↓
Revise
   ↓
Commit Conclusion
   ↓
Validate
   ↓
New Information / Next Mystery
```

다음 구조만으로는 강한 Deduction으로 인정하지 않는다.

```text
Text
↓
4-choice Question
↓
Wrong
↓
Try next
↓
Correct
```

또는:

```text
Hidden Object Found
↓
Notebook Auto-register
↓
UI Auto-connect
↓
Conclusion Display
```

---

# 3. Source Classification

# 3.1 Tier A — Primary Deduction Design Evidence

## REF-17 — Return of the Obra Dinn

**Subtype:** `Pure Logical Deduction / Identity Reconstruction`  
**Evidence Strength:** VERY HIGH

### Strong Evidence Areas

- Evidence Cross-reference
- Identity Deduction
- Spatial Clue
- Dialogue Clue
- Relationship Clue
- Delayed Validation
- Notebook
- Player-owned Inference
- Brute-force Resistance
- One-shot / first-play information density
- Logic QA

### Key Source-derived Observations

- 정답 선택지를 직접 알려주지 않고 정지 장면·명단·대화·공간 단서를 교차해 인물과 사망 원인을 추론하게 한다.
- Deduction의 핵심은 단서 수가 아니라 플레이어가 스스로 결론을 만들 수 있는 정보 구조다.
- 정답 검증을 묶음 단위로 지연하면 무작위 대입을 줄일 수 있다.
- 정보를 숨기는 것과 추리를 만드는 것은 다르며, 필요한 단서가 논리적으로 연결되지 않으면 난해함만 남는다.
- 낮은 재플레이를 허용하고 첫 경험 밀도를 극대화하는 전략도 가능하다.
- 고밀도 단서 설계와 사건 간 논리 QA는 높은 제작비를 만든다.

---

# 3.2 Tier B — Deduction / Identification Support

## REF-30 — The Case of the Golden Idol

**Subtype:** `Scene-based Logical Reconstruction`  
**Classification:** `TIER B / PRODUCTION-HEAVY DEDUCTION SUPPORT`

### Use

- 제한된 장면
- 정보 밀도
- 단서 교차
- 추리 콘텐츠에 제작비 집중
- Logic authoring / QA cost

### Classification Reason

현재 Studio Reference가:
- Production model
- Prototype-first
- 작은 팀
- 제한 장면 / 단서 교차

중심이다.

따라서:
- Validation timing
- Brute-force behavior
- Hypothesis telemetry
- Notebook UX

등 세부 Design Mechanism을 Primary Evidence로 과대 사용하지 않는다.

---

## REF-31 — Chants of Sennaar

**Subtype:** `Language Decoding / Semantic Deduction`  
**Classification:** `TIER B / PRODUCTION-HEAVY DEDUCTION SUPPORT`

### Use

- 언어 해독이라는 단일 USP
- Progressive Knowledge
- Symbol / meaning inference 가능성
- Knowledge progression / recontextualization 연구 Target

### Classification Reason

현재 Reference는:
- 2인 역할 분담
- USP 집중
- Scope
- Production efficiency

가 중심이다.

Language Deduction Design Core의 직접 Evidence로는 제한적이다.

---

## REF-29 — Strange Horticulture

**Subtype:** `Reference-based Identification`  
**Classification:** `TIER B / PRODUCTION-HEAVY IDENTIFICATION SUPPORT`

### Use

- 식물 식별
- Reference Book
- 제한된 인터페이스
- 큰 세계를 작은 작업공간에 압축
- Search / identification / reference burden 연구 Target

### Classification Reason

현재 Reference는 Production / Scope 중심이다.

---

# 3.3 Tier B — Information / Investigation Hybrid

## REF-01 — Papers, Please

**Subtype:** `Rule Verification / Information Processing`

### Use

- Rule-based comparison
- Information prioritization
- UI search burden
- Error feedback
- Progressive rule complexity
- Information Processing과 Deduction의 Boundary

### Critical Boundary

Papers, Please의 중심 문제는:

```text
Known Rule
+
Document
↓
Correct Judgment
```

의 성격이 강하다.

따라서:
- Evidence relation
- Hidden conclusion
- free hypothesis

를 요구하는 Pure Deduction과 동일하게 취급하지 않는다.

---

## REF-48 — The Operator

**Subtype:** `Investigation / In-world Computer Interface`

### Use

- Investigation Fantasy
- Information Retrieval
- Case Structure
- UI-as-investigation

### Limitation

현재 Studio Reference는 Commercial Layer 중심이므로 Deduction Design Evidence Weight를 낮춘다.

---

# 3.4 Tier C — Adjacent / Control

필요한 Mechanism 비교에만 사용한다.

- Into the Breach
  - Complete information / clarity comparison
- Invisible, Inc.
  - Information → Action
- Cultist Simulator
  - Discovery / cognitive load
- Citizen Sleeper
  - Information / relationship / state
- Reigns
  - Hidden consequence / learnability
- 80 Days
  - Information recontextualization / narrative state

Tier C만으로 Provisional Deduction Core를 승격하지 않는다.

---

# 3.5 Source Limitation

이번 장르는 이전 Deckbuilding / Management보다 Primary Design Evidence가 좁다.

현재 강한 Direct Design Reference는 사실상:

`Return of the Obra Dinn`

에 집중되어 있다.

따라서:

> 중요한 주제라는 이유만으로 Core를 늘리지 않는다.

Promotion 기준의:

> “하나의 매우 강한 직접 사례 + 복수 보조 사례”

를 사용하되, 보조 사례가 Production 중심이면 Confidence를 낮춘다.

---

# 4. Existing Core Audit

# GC-DEDUCT-001 — UI Should Externalize Memory / Search, Not Inference

**Decision:** `STRENGTHEN`  
**Status:** `PROVISIONAL CORE`  
**Origin:** `EXISTING GC REFINEMENT`

## Previous Rule

> 추리 UI는 검색·기억 비용을 줄일 수 있지만 Evidence 관계를 만들고 Conclusion을 도출하는 추론까지 대신해서는 안 된다.

## Audit Decision

`KEEP AS ONE CORE`.

다음 두 문장을 분리 Core로 만들지 않는다.

```text
A. UI should reduce recall/search cost.
B. Core inference relationship should remain player-owned.
```

이유:

두 문장은 사실상 같은 설계 경계의 양쪽이다.

> **UI가 어디까지 도와야 하는가?**

라는 하나의 문제다.

## Refined Pattern

강한 Deduction UI는:
- 이름
- 장면
- 기록
- 이미 본 정보
- 대상 목록

을 외부화할 수 있다.

그러나:

- 어떤 정보가 서로 관련되는지
- 어떤 가설이 더 타당한지
- 최종 Conclusion이 무엇인지

까지 자동 결정하면 Inference Ownership이 사라진다.

## Rule

> **Deduction UI는 Recall / Search / Organization Cost를 줄일 수 있지만, Core Evidence Relation과 Conclusion Formation은 플레이어에게 남겨야 한다.**

## Mechanism

과도한 기억 부담:

```text
30분 전 이름을 기억 못함
→ 추론 실패
```

는 Deduction Skill과 Memory Skill을 불필요하게 섞는다.

반대로 과도한 자동화:

```text
Evidence A 발견
+
Evidence B 발견
↓
UI 자동 연결
↓
Conclusion C
```

는 플레이어의 핵심 Reasoning Verb를 제거한다.

좋은 UI의 역할:

```text
기억 보조
검색 보조
정리
재방문
비교
```

플레이어의 역할:

```text
Relation Construction
Hypothesis
Cross-check
Conclusion
```

## Primary Evidence

### Return of the Obra Dinn

Reference가:
- Notebook
- 명단
- 정지 장면
- 공간
- 대화

를 복잡한 정보 정리 도구로 사용하면서도 플레이어가 직접 Identity와 Fate를 연결하는 구조를 강한 Lesson으로 정리한다.

가장 직접적인 문장:

> 추리 게임의 핵심은 단서 수보다 플레이어가 스스로 결론을 만들어낼 수 있는 정보 구조다.

## Secondary Evidence

### Strange Horticulture
Reference Book / 제한 인터페이스가 큰 세계의 정보를 한 작업 공간에서 다루는 구조를 지지한다.

단, 현재 Source는 Production 중심이라 보조 Evidence로만 사용.

### Papers, Please
Rulebook과 문서 UI는 Memory / Search를 지원하지만, 이 사례는 Information Processing이므로 Deduction Ownership의 직접 증거는 아니다.

## Counter Evidence

### Memory-heavy Mystery
특정 인물·언어·세부 정보 기억 자체가 Fantasy일 수 있다.

### Free-form note game
의도적으로 Built-in notebook을 제한해 플레이어가 외부 노트를 쓰는 행위를 Fantasy로 만들 수도 있다.

따라서 Built-in Notebook을 Universal Feature로 강제하지 않는다.

## Applies To

- Pure Logical Deduction
- Identity Deduction
- Scene Reconstruction
- Language Decoding
- Investigation Adventure

## Boundary

Information Processing에서는 UI가 더 적극적으로 Rule Violation을 표시해도 Core를 훼손하지 않을 수 있다.

## Observed Metric

현재 Reference에 직접 Human telemetry는 부족하다.

## Candidate Metric — Instrumented

- Notebook Open Rate
- Evidence Revisit Rate
- Search Time
- Character / Evidence Lookup Frequency
- External Note Usage

## Candidate Metric — Human

- Inference Ownership
- Memory Burden
- Search Burden
- Notebook Utility
- “UI가 답을 알려줬다” 인식

## Validation Type

Human + Instrumented Player Telemetry.

## AI Tester Applicability

LOW for UX experience.  
Formal UI state coverage에는 사용 가능.

## Confidence

**VERY HIGH**

## Reviewer Action

Notebook / Evidence Board / Timeline이 있다면:

> **“이 UI가 줄이는 것은 기억 비용인가, 추론 비용인가?”**

를 묻는다.

추론 비용까지 제거한다면 `UI_SOLVES_INFERENCE_RISK`.

---

# GC-DEDUCT-002 — Solution Knowledge Consumption Changes the Value Model

**Decision:** `RECLASSIFY`  
**Status:** `RECLASSIFY — PRODUCT / CONTENT CONSUMPTION CORE CANDIDATE`  
**Origin:** `EXISTING GC REASSESSMENT`

## Previous Name

`Low Replayability is not automatically a defect`

## Why Reclassify

이 문장은 맞지만:

> 신규 Deduction Mechanism이 잘 설계되었는가?

를 직접 판단하는 Rule이라기보다:

> 정답을 알면 콘텐츠 가치가 얼마나 소비되는가?

라는 Product / Content Consumption 문제다.

즉:
- replay expectation
- price / length value
- first-play density
- spoiler sensitivity
- authored content cost

와 더 가깝다.

## Reframed Rule Candidate

> **Solution Knowledge가 핵심 콘텐츠를 소비하는 구조에서는 Replay Count를 자동 품질지표로 사용하지 않고, First-play Deduction Density / Solution Integrity / Time-to-Value를 함께 평가한다.**

## Primary Evidence

Return of the Obra Dinn Reference는:
- 낮은 Replayability를 Weakness로 인정
- 동시에 첫 경험 밀도를 극대화하는 전략도 가능하다고 정리

한다.

## Counter Evidence

- Generated Deduction
- Systemic Mystery
- Random Case
- Multiple-solution Investigation

은 Replayability가 제품 가치의 핵심일 수 있다.

## Reviewer Use

Deduction Genre Reviewer에서 완전히 버리지 않는다.

단:

`Genre Mechanism Core`

가 아니라:

`Product / Content Consumption Context`

로 호출한다.

## Confidence

**HIGH — Reclassification**

---

# 5. Provisional Deduction Cores

# GC-DEDUCT-003 — Evidence Relations Must Make the Conclusion Logically Reachable

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

Deduction의 핵심 실패는 정보가 적은 것이 아니라:

- 필요한 Evidence가 없거나
- 서로 연결되지 않거나
- Conclusion이 Evidence에서 도출되지 않는

경우 발생한다.

반대로 강한 사례는 한 Scene / Dialogue / Position / Identity 정보가 여러 관계에 기여하며, 플레이어가 이를 교차해 Hypothesis Space를 줄인다.

## Deduction Context

- Pure Logical Deduction
- Identity Deduction
- Scene Reconstruction
- Language Decoding
- Reference-based Identification

## Rule

> **Hidden Conclusion에 필요한 Evidence는 게임 안에 존재해야 하며, 플레이어가 Evidence 관계를 구성하면 Hypothesis Space가 논리적으로 축소되어 Conclusion에 도달할 수 있어야 한다. 정보 부족이나 임의의 Story Revelation을 난이도로 사용하지 않는다.**

## Mechanism

좋은 Deduction:

```text
Evidence A
→ Candidate 8 → 4

Evidence B
→ 4 → 2

Context C
→ 2 → 1

Conclusion
```

나쁜 Deduction:

```text
Evidence A
Evidence B
Evidence C
↓
논리적 연결 없음
↓
작가가 마지막에 정답 공개
```

또는:

```text
Critical Evidence D 없음
↓
정답을 추측해야 함
```

## Primary Evidence

### Return of the Obra Dinn

Reference의 가장 강한 Lesson:

> **Deduction은 정보 부족이 아니라 정보 관계 설계에서 나온다.**

정지 장면·명단·대화·공간 단서를 교차해:
- Identity
- Fate

를 플레이어가 직접 증명한다.

Primary Warning 역시:

> 필요한 단서가 논리적으로 연결되지 않으면 난해함만 남는다.

라고 정리한다.

## Secondary Evidence

### The Case of the Golden Idol
현재 Production Reference지만:
- 제한된 장면
- 정보 밀도
- 단서 교차

에 제작비를 집중한 사례로 Mechanism 방향을 보조한다.

### Strange Horticulture
식물 식별이라는 Reference-based Identification 구조는:
- Description
- Object
- Reference

관계가 결론을 만드는 Subtype 후보를 지지한다.

### Chants of Sennaar
언어 해독이라는 USP는:
- unknown symbol
- contextual meaning

관계를 통한 Knowledge Deduction의 다른 Subtype을 보조한다.

## Counter Evidence

### Investigation Narrative with deliberate ambiguity
정답이 하나가 아니거나 Player Interpretation을 허용하는 제품에서는 Unique Logical Conclusion을 강제하면 안 된다.

### Discovery Adventure
핵심이 추론보다 세계 탐색과 Story discovery라면 Evidence Graph 엄밀성의 비중이 낮다.

## Applies To

강하게:
- Formal Deduction
- Identity
- Scene Reconstruction

조건부:
- Language Decoding
- Identification

약하게:
- Narrative Investigation with ambiguity

## Boundary

`Conclusion Reachability`와 `Human Discoverability`는 다르다.

Formal model에서 정답이 가능해도:
- 시각 단서가 너무 작거나
- 위치가 지나치게 숨겨지거나
- 기억 부담이 높으면

Human에게는 불공정할 수 있다.

## Observed Metric

Source에서 공통 정량 Telemetry 없음.

## Candidate Metric — Formal / Machine

- Evidence Node Count
- Evidence Relation Count
- Conclusion Reachability
- Solution Count
- Contradiction Count
- Unsatisfied Constraint Count
- Minimum Evidence Set Size
- Evidence → Conclusion Path Count
- Mandatory Evidence Bottleneck
- Orphan Evidence Rate
- Unused Evidence Rate

## Candidate Metric — Human

- Evidence Sufficiency Experience
- Inference Explanation Accuracy
- Solution Fairness
- “정답을 안 뒤 필요한 단서가 있었다고 느끼는가?”

## Validation Type

Formal / Machine + Human.

## AI Tester Applicability

VERY HIGH for formal structure.  
LOW for human clarity.

## Confidence

**VERY HIGH**

## Reviewer Action

Mystery를 검토할 때:

> **“정답을 알고 있는 작가가 아니라, 정답을 모르는 플레이어가 어떤 Evidence chain으로 여기까지 도달하는가?”**

를 요구한다.

그 Chain을 문서화할 수 없다면 `ARBITRARY_SOLUTION_RISK`.

---

# GC-DEDUCT-004 — Validation Design Must Preserve Reasoning

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

Deduction에서는 정답 입력 UI 자체보다:

> **언제, 어떤 단위로, 얼마만큼 정오답을 알려주는가**

가 Player Strategy를 바꾼다.

즉 Validation은 Feedback UI가 아니라 Core Mechanic의 일부다.

## Rule

> **Validation은 플레이어가 Hypothesis를 시험하고 수정할 수 있게 해야 하지만, Guess / Exhaustive Search가 Evidence-based Reasoning보다 효율적인 전략이 되도록 정답 정보를 과도하게 누출해서는 안 된다.**

## Mechanism

### Immediate Per-field Validation

```text
Candidate A 입력
→ Wrong
Candidate B
→ Wrong
Candidate C
→ Correct
```

이면 정오답 Feedback 자체가 Evidence가 된다.

Candidate가 적고 Retry Cost가 낮다면:

> Reasoning < Brute-force

가 될 수 있다.

### Delayed / Grouped Validation

여러 Conclusion을 묶어 확인하면:
- Guess information gain 감소
- Cross-evidence reasoning 증가

가능성이 있다.

하지만 너무 늦으면:
- Wrong hypothesis 장기 유지
- Stuck
- frustration

이 증가할 수 있다.

## Primary Evidence

### Return of the Obra Dinn

Reference가 직접:

> **정답 검증을 묶음 단위로 지연하면 무작위 대입을 줄일 수 있다.**

고 정리한다.

또:

> **정답 검증 방식도 Core Mechanic의 일부다.**

라는 Lesson을 명시한다.

## Secondary / Counter Evidence

### Papers, Please

Information Processing에서는:
- 오류 피드백
- Rule checking

이 더 빠르게 제공되어도 Gameplay가 무너지지 않는다.

즉 Immediate Feedback이 항상 나쁜 것이 아니다.

Hidden Variable은:

> 정오답 Feedback이 Core Hypothesis Space를 얼마나 줄이는가?

다.

## Counter Evidence

### Short tutorial deduction
초기 학습 구간에서는 Immediate Validation이 Rule Learning을 위해 유효할 수 있다.

### High candidate / high input cost
Free-form answer나 매우 큰 Candidate Space에서는 즉시 Feedback이 있어도 Brute-force가 비경제적일 수 있다.

## Applies To

강하게:
- Identity Deduction
- Formal Logical Deduction
- Multiple-choice / candidate assignment deduction

조건부:
- Language Decoding
- Identification

## Boundary

Validation Delay 자체를 Core로 만들지 않는다.

핵심은:

> **Reasoning Expected Value > Guess Expected Value**

가 되도록 Validation 구조를 설계하는 것이다.

## Observed Metric

Return of the Obra Dinn의 grouped/delayed confirmation 구조는 Qualitative Evidence.

## Candidate Metric — Formal / Machine

- Guess Space Size
- Random Guess Success Rate
- Attempts to Solve without Evidence
- Immediate-validation Information Gain
- Validation Leakage
- Candidate Elimination per Wrong Attempt
- Brute-force Expected Attempts

## Candidate Metric — Instrumented

- Wrong-answer Attempts
- Guess Sequence Length
- Validation-triggered rapid retry
- Time between evidence check and answer

## Candidate Metric — Human

- Brute-force Temptation
- Validation Fairness
- “생각하는 것보다 넣어보는 게 빠르다” 인식
- Wrong-answer Learning

## Validation Type

Formal / Machine + Instrumented + Human.

## AI Tester Applicability

VERY HIGH for brute-force structure.

## Confidence

**HIGH**

## Reviewer Action

정답 확인 시스템이 있다면:

> **“플레이어가 단서 없이 입력만 반복했을 때 얼마나 빨리 정답에 도달하는가?”**

를 계산한다.

---

# 6. Deduction Core Candidates

# GC-DEDUCT-005 — Evidence Accessibility Is Separate from Evidence Sufficiency

**Status:** `CANDIDATE`  
**Origin:** `NEW GENRE CORE`

## Rule Candidate

> **필수 Evidence가 논리적으로 존재하더라도 합리적으로 발견할 수 없다면 Human Deduction은 실패한다. Formal Sufficiency와 Human Accessibility를 분리 검증한다.**

## Mechanism

```text
Evidence exists in data
≠
Player can reasonably notice it
```

특히:
- 작은 시각 단서
- 특정 시점
- 재방문 불가
- UI scale
- 색상 의존
- one-time dialogue

는 Single-point Fail을 만들 수 있다.

## Supporting Evidence

Return of the Obra Dinn은 정지 장면을 자유롭게 관찰하고 공간 단서를 사용한다.

하지만 현재 Reference에는 실제 Clue Miss Telemetry가 없다.

Strange Horticulture는 Reference-based identification 가능성을 보조하지만 Production Source 중심.

## Candidate Metric

### Formal
- Critical Evidence Count
- Time-windowed Evidence Count
- Revisitability Flag

### Instrumented
- Critical Clue Miss Rate
- Evidence Discovery Rate
- Revisit Rate

### Human
- Evidence Readability
- “단서를 못 봤다” 비율

## Confidence

**MEDIUM-HIGH**

---

# GC-DEDUCT-006 — Robust Deduction Should Avoid Unrecoverable Single-point Bottlenecks

**Status:** `CANDIDATE`

## Rule Candidate

> **한 개의 작은 단서 누락이 전체 추론을 영구 차단하는 구조라면 Redundancy, Alternate Path, Revisit, Hint 중 하나 이상의 Recovery를 검토한다.**

## Mechanism

Critical Evidence 하나가:
- 놓치기 쉽고
- 재방문 불가하며
- 대체 관계도 없다면

Puzzle difficulty가 아니라 Discovery lottery가 될 수 있다.

## Evidence

Obra Dinn의 복수 정보 교차 구조가 간접 지지하지만:
- 실제 Minimum Evidence Set
- Alternate reasoning path

자료는 부족하다.

Golden Idol의 고밀도 장면 역시 보조적.

## Candidate Metric

- Mandatory Evidence Bottleneck
- Evidence → Conclusion Path Count
- Critical Evidence Count
- Missed-clue Dead-end Rate
- Recovery Path Count

## Confidence

**MEDIUM**

---

# GC-DEDUCT-007 — Hypothesis Space Must Be Narrowed by Evidence, not Trial Exhaustion

**Status:** `CANDIDATE`

## Rule Candidate

> **가능한 정답 수는 Evidence가 의미 있게 줄여야 하며, Candidate Space가 너무 작아 Guess가 빠르거나 너무 커 Exhaustive Search가 최적이 되지 않도록 검토한다.**

## Mechanism

Too Small:

```text
3 candidates
+
instant wrong feedback
→ brute force
```

Too Large:

```text
100 candidates
+
weak evidence
→ reasoning보다 spreadsheet exhaustion
```

## Evidence

Obra Dinn의:
- 명단
- 관계
- 묶음 validation
- cross-reference

가 Hypothesis Space 관리 Mechanism을 지지.

그러나 다른 Primary Design 사례 부족.

## Candidate Metric

- Hypothesis Count by Stage
- Evidence-induced Candidate Reduction
- Guess Space Size
- Random Guess Success
- Exhaustive Search Cost

## Confidence

**MEDIUM-HIGH**

---

# GC-DEDUCT-008 — Stuck Recovery Should Redirect Reasoning, Not Replace It

**Status:** `CANDIDATE`

## Rule Candidate

> **막힘 완화 장치는 정답을 전달하기보다 관찰 범위·Evidence·Relation을 다시 보게 해야 한다.**

## Hint Level

1. Navigation Hint
2. Evidence Hint
3. Relation Hint
4. Conclusion Hint

Level이 올라갈수록 Inference Ownership 감소 가능성이 커진다.

## Evidence

현재 Primary Source에서 Hint telemetry 부족.

Obra Dinn의 UI / delayed validation 구조가 추론 자율성을 지지하지만 Hint Core 승격에는 부족하다.

## Candidate Metric

### Instrumented
- Hint Use
- Hint Level
- Time-to-Hint
- Hint → Conclusion Time

### Human
- Hint Satisfaction
- Ownership after Hint
- Stuck Recovery Quality

## Confidence

**MEDIUM**

---

# GC-DEDUCT-009 — Memory / Search Burden Should Not Dominate Inference

**Status:** `CANDIDATE`  
**Origin:** `SPECIALIZATION / SUPPORTING RULE OF GC-DEDUCT-001`

## Rule Candidate

> **핵심 Fantasy가 추론이라면 이미 획득한 정보를 기억하거나 다시 찾는 비용이 Relation Reasoning보다 커지는지 별도 점검한다.**

## Why Candidate not Core

이 문제는 `GC-DEDUCT-001`의 하위 위험과 중복된다.

별도 Core로 승격하기보다:
- Human metric
- Anti-pattern
- Reviewer sub-question

으로 유지할 가능성이 높다.

## Candidate Metric

- Search Time
- Evidence Revisit Rate
- Notebook Open Rate
- External Note Usage
- Observation vs Reasoning Ratio

## Confidence

**MEDIUM-HIGH**

## Merge Candidate

추가 Evidence가 없으면 `GC-DEDUCT-001 Sub-rule`로 병합 가능.

---

# GC-DEDUCT-010 — Knowledge Progression Should Recontextualize Evidence

**Status:** `CANDIDATE`

## Rule Candidate

> **Language / Identification / Knowledge-gated Deduction에서 새로운 지식은 단순 Gate Key가 아니라 이전 Evidence의 의미를 바꾸거나 새로운 Relation을 읽게 해야 한다.**

## Supporting Evidence

### Chants of Sennaar
현재 Studio Reference는 Production 중심이지만:
- 언어 해독
- 강한 단일 USP

가 Knowledge progression 연구 대상임을 지지한다.

### Obra Dinn
새 Identity / Event 이해가 다른 장면의 관계를 재해석할 수 있는 구조가 간접 지지.

## Promotion Blocker

Chants의 상세 Design Case 부족.

## Candidate Metric

- Prior Evidence Revisit after Knowledge Gain
- Recontextualization-triggered Conclusion
- Knowledge Unlock → Hypothesis Change

## Human

- “새 지식 때문에 예전 단서가 다르게 보였다” 인식
- Aha

## Confidence

**MEDIUM**

---

# GC-DEDUCT-011 — Deduction Pacing Needs Progressive Commitment

**Status:** `CANDIDATE`

## Rule Candidate

> **장시간 아무것도 확정할 수 없는 상태와, 매 단서마다 정답이 자동 확정되는 상태 사이에서 작은 Hypothesis / Confirmation이 더 큰 Conclusion으로 누적되는 리듬을 검토한다.**

## Evidence

Obra Dinn의 grouped validation이 pacing에 영향을 주지만 직접 Player telemetry 부족.

Golden Idol / Chants는 Production 중심.

## Candidate Metric

- First Solvable State
- Time to First Confirmed Conclusion
- Conclusion Frequency
- Longest Unconfirmed Reasoning Span
- Major Revelation Timing

## Human

- Puzzle Pacing
- Stuck Severity
- Aha cadence

## Confidence

**MEDIUM-LOW**

---

# GC-DEDUCT-012 — Multiple Reasoning Paths Can Improve Robustness

**Status:** `CANDIDATE`

## Rule Candidate

> **같은 Conclusion에 독립적인 Evidence 경로가 존재하면 Missed Clue Robustness와 Player-specific Reasoning을 지원할 수 있지만, 과도한 Redundancy는 정답을 너무 명백하게 만들 수 있다.**

## Evidence

Obra Dinn의:
- spatial
- dialogue
- relationship

교차가 이를 시사.

그러나 실제 Path Count / Player path data가 없음.

## Candidate Metric

- Evidence → Conclusion Path Count
- Independent Path Count
- Minimum Evidence Set Count
- Redundant Evidence Count

## Confidence

**MEDIUM**

---

# 7. Deduction Anti-Patterns

# AP-DEDUCT-001 — Hidden Information ≠ Deduction

## Trigger
정보를 숨겼지만 Evidence relation이 없음.

## Mechanism
플레이어는 추론이 아니라:
- 탐색
- 기다림
- Guess

으로 진행.

## Consequence
Mystery theme는 있으나 Deduction Agency 부족.

## Evidence
Obra Dinn Primary Warning:
정보를 숨기는 것과 추리를 만드는 것은 다르다.

## Detection
- Evidence Relation Count
- Conclusion Reachability
- Observation-only Conclusion Rate

## Mitigation
Hidden fact마다 Evidence relation chain을 작성한다.

---

# AP-DEDUCT-002 — Single Clue Gives the Answer

## Trigger
한 단서가 곧 정답.

## Consequence
Discovery는 있으나 Relation Reasoning이 없음.

## Boundary
Identification Subtype에서는 충분히 세밀한 관찰 자체가 Fantasy일 수 있다.

## Detection
- Minimum Evidence Set Size = 1
- Observation-only Conclusion Rate

## Mitigation
Relation requirement를 추가하되 억지 복잡화는 금지.

---

# AP-DEDUCT-003 — Missing Critical Evidence

## Trigger
정답에 필요한 필수 Evidence가 없거나 획득 불가.

## Consequence
Logical difficulty가 아니라 arbitrary guessing.

## Detection
- Conclusion Reachability FAIL
- Unsatisfied Constraint
- Critical Evidence Missing

## Mitigation
Formal evidence graph / reachability test.

---

# AP-DEDUCT-004 — Memory Test Disguised as Deduction

## Trigger
이미 본 이름·숫자·위치를 기억 못하면 진행 불가.

## Consequence
Reasoning보다 recall skill이 결과 지배.

## Detection
- Human stuck reason
- Notebook dependency
- Memory burden
- External note use

## Mitigation
필요 정보 Externalization.

---

# AP-DEDUCT-005 — Search Burden Disguised as Depth

## Trigger
이미 발견한 정보를 어디서 봤는지 찾는 시간이 과도.

## Consequence
Administrative retrieval이 deduction time을 대체.

## Detection
- Search Time
- Evidence Revisit Rate
- Observation vs Reasoning Ratio

## Mitigation
Index / replay / filter / bookmark.

---

# AP-DEDUCT-006 — UI Solves the Inference

## Trigger
Evidence Board가 관계를 자동 연결하거나 Conclusion을 표시.

## Consequence
Player-owned inference 제거.

## Evidence
Obra Dinn의 가장 강한 반대 구조.

## Detection
- Auto-generated relation count
- Player explanation vs UI conclusion dependency
- Inference Ownership

## Mitigation
Organization과 conclusion logic 분리.

---

# AP-DEDUCT-007 — Brute-force Beats Reasoning

## Trigger
Candidate가 적고 Wrong Feedback이 즉시·무료.

## Consequence
최적 전략이 trial-and-error.

## Detection
- Random Guess Success
- Expected Guess Attempts
- Validation Leakage
- rapid wrong-answer sequence

## Mitigation
- grouped validation
- delayed validation
- meaningful commit cost
- larger but legible evidence space

---

# AP-DEDUCT-008 — Instant Validation Leak

## Trigger
부분 입력마다 정오답 공개.

## Consequence
Feedback가 Evidence를 대체.

## Boundary
Tutorial / Information Processing에서는 유효할 수 있음.

## Detection
- Information Gain per Wrong Attempt
- candidate reduction from feedback only

## Mitigation
Validation granularity 조절.

---

# AP-DEDUCT-009 — No Validation / No Learning

## Trigger
Hypothesis가 맞는지 확인할 수 없음.

## Consequence
Stuck / ambiguity / arbitrary progression.

## Detection
- Unvalidated Conclusion Count
- Stuck duration

## Mitigation
적절한 validation channel 제공.

---

# AP-DEDUCT-010 — Hint Gives Conclusion

## Trigger
Hint가 관계나 탐색 방향이 아니라 답 자체를 제시.

## Consequence
Stuck은 해소되지만 Inference Ownership 소멸.

## Detection
- Hint level
- Hint → immediate conclusion
- ownership after hint

## Mitigation
Navigation → Evidence → Relation 순의 단계형 Hint.

---

# AP-DEDUCT-011 — Single-point Clue Bottleneck

## Trigger
한 단서를 놓치면 전체 Progress 중단.

## Consequence
Deduction failure보다 perception miss가 지배.

## Detection
- Mandatory Evidence Bottleneck
- Missed clue dead-end
- single path conclusion

## Mitigation
Revisit / alternate path / redundancy / hint.

---

# AP-DEDUCT-012 — False Complexity

## Trigger
인물·문서·단서 수는 많지만 Relation Type은 동일 반복.

## Consequence
인지부하 증가, 추론 다양성은 낮음.

## Detection
- Evidence Count vs Relation Type Count
- repeated inference pattern concentration

## Mitigation
콘텐츠 수보다 새로운 Relation Question 우선.

---

# AP-DEDUCT-013 — Arbitrary Solution

## Trigger
정답은 있지만 Evidence에서 논리적으로 도출되지 않음.

## Consequence
Player trust 붕괴.

## Detection
- Conclusion Reachability
- Player inference explanation failure after reveal

## Mitigation
Formal evidence graph와 blind review.

---

# AP-DEDUCT-014 — External Knowledge Dependency

## Trigger
게임 내부 Evidence보다 현실 전문지식이 필수.

## Consequence
Target knowledge에 따라 불공정 난이도.

## Boundary
Trivia / historical research fantasy라면 의도 가능.

## Detection
- External knowledge required flag
- test cohort knowledge dependency

## Mitigation
필수 지식은 게임 안에서 제공하거나 명시적 Target Audience 조건으로 둔다.

---

# AP-DEDUCT-015 — Revelation without Player Inference

## Trigger
플레이어가 추론하기 전에 Story가 정답 공개.

## Consequence
Mystery narrative는 존재하지만 Deduction payoff 없음.

## Detection
- Conclusion revealed before solvable state
- Player-predicted conclusion rate
- inference ownership

## Mitigation
Revelation 전에 충분한 solvable window 제공.

---

# 8. Conflicting Findings

# CF-DEDUCT-001 — Immediate vs Delayed Validation

## Immediate

장점:
- 빠른 Feedback
- Learning
- Stuck 감소

위험:
- Brute-force
- Hypothesis leakage

## Delayed

장점:
- 추론 보존
- Guess 억제

위험:
- Wrong hypothesis 장기 유지
- Frustration

## Hidden Variables
- Candidate Count
- Retry Cost
- Puzzle Length
- Hint Structure
- Input Format

## Resolution

“Delayed is better”가 아니라:

> **Reasoning EV가 Guess EV보다 높으면서 Learning loop가 유지되는 Timing**

을 찾는다.

---

# CF-DEDUCT-002 — Redundant Clues vs Elegant Minimal Clues

## Redundancy
- robust
- multiple paths
- missed clue recovery

## Minimal
- elegant
- lower noise
- stronger inference precision

## Hidden Variables
- clue accessibility
- puzzle length
- revisit
- target difficulty

## Resolution
Universal clue-count threshold를 만들지 않는다.

---

# CF-DEDUCT-003 — Notebook Assistance vs Pure Memory

## Assistance
- recall burden 감소
- evidence comparison 쉬움

## Pure Memory
- immersion
- investigator fantasy
- mastery

## Hidden Variable
Player Fantasy.

## Resolution
Memory가 Core Skill인지 Administrative Cost인지 먼저 정의한다.

---

# CF-DEDUCT-004 — Explicit Hypothesis Options vs Free-form Inference

## Explicit Options
- UX 쉬움
- accessible
- formal validation 쉬움
- brute-force risk

## Free-form
- agency
- candidate generation
- input burden
- parser/UI 문제

## Resolution
Candidate generation 자체가 Core Fantasy인지에 따라 선택.

---

# CF-DEDUCT-005 — Unique Solution vs Ambiguous Interpretation

## Formal Deduction
Unique solution이 중요.

## Narrative Mystery
Intentional ambiguity가 가치일 수 있음.

## Resolution
Solution Count를 모든 mystery에 동일 Criteria로 쓰지 않는다.

---

# CF-DEDUCT-006 — Low Replay vs Replayable Deduction

## Fixed Solution
Obra Dinn 계열.

## Generated / Systemic
Procedural investigation 가능.

## Resolution
Replayability는 Genre Quality가 아니라 Product Structure에 종속.

---

# CF-DEDUCT-007 — Dense Evidence vs Progressive Reveal

## Dense
- 자유로운 cross-reference
- 높은 agency
- cognitive load 증가

## Progressive
- pacing 통제
- onboarding 쉬움
- hypothesis space 인위적 제한

## Resolution
Puzzle Scope / cognitive load / revision cost에 맞춰 결정.

---

# CF-DEDUCT-008 — Player-created Notes vs Built-in Organization

## External Notes
- 자유도
- investigator fantasy

## Built-in
- accessibility
- console/mobile usability
- lower memory/search burden

## Resolution
Product Promise와 Platform에 따라 결정.

---

# 9. Formal / Machine Validation Map

Deduction 장르에서는 “AI가 인간처럼 풀었다”보다 **Formal Structure 검증**이 더 신뢰할 수 있다.

---

## 9.1 Evidence Graph Metrics

| Metric | Type | Purpose |
|---|---|---|
| Evidence Node Count | Formal | 정보량 |
| Evidence Relation Count | Formal | 관계 구조 |
| Conclusion Dependency | Formal | 결론 의존성 |
| Critical Evidence Count | Formal | 필수 단서 수 |
| Redundant Evidence Count | Formal | 대체 경로 |
| Orphan Evidence Rate | Formal | 결론에 기여하지 않는 단서 |
| Unused Evidence Rate | Formal / model-dependent | 해결에 불필요한 Evidence |

---

## 9.2 Reachability Metrics

| Metric | Type |
|---|---|
| Conclusion Reachability | Formal |
| Evidence → Conclusion Path Count | Formal |
| Mandatory Evidence Bottleneck | Formal |
| Minimum Evidence Set Size | Formal |
| Maximum Dependency Depth | Formal |
| Alternate Reasoning Path Count | Formal / model-dependent |

---

## 9.3 Solution Metrics

Formal model이 가능한 경우만 사용한다.

| Metric | Type |
|---|---|
| Solution Count | Formal |
| Unique Solution Check | Formal |
| Contradiction Count | Formal |
| Ambiguous State Count | Formal |
| Unsatisfied Constraint Count | Formal |
| Premature Solvability | Formal / model-dependent |

### Rule

Narrative ambiguity가 의도된 게임에 `Unique Solution`을 자동 적용하지 않는다.

---

## 9.4 Brute-force Metrics

| Metric | Type |
|---|---|
| Guess Space Size | Formal |
| Attempts to Solve without Evidence | Formal / simulated |
| Immediate-validation Information Gain | Formal |
| Random Guess Success Rate | Formal |
| Validation Leakage | Formal / model-dependent |
| Candidate Elimination from Wrong Feedback | Formal |

---

## 9.5 Progression Metrics

| Metric | Type |
|---|---|
| First Solvable State | Formal / model-dependent |
| Evidence Availability Timing | Formal |
| Conclusion Unlock Timing | Formal |
| Stuck State Reachability | Formal / model-dependent |
| Critical Clue Miss Recovery | Formal / scenario-based |
| Recontextualization Dependency | Formal / model-dependent |

---

## 9.6 Instrumented UI / Information Metrics

| Metric | Type |
|---|---|
| Evidence Revisit Rate | Player Telemetry |
| Notebook Open Rate | Player Telemetry |
| Search Time | Player Telemetry |
| Character / Evidence Lookup Frequency | Player Telemetry |
| Hint Usage | Player Telemetry |
| External Note Usage | Instrumented / Human report |
| Critical Clue Miss Rate | Instrumented / model-dependent |
| Wrong-answer Attempts | Player Telemetry |
| Time to Conclusion | Player Telemetry |

---

# 9.7 Formal Metric Interpretation Rule

다음은 Project-specific Formal Model이 있어야 한다.

- First Solvable State
- Stuck State Reachability
- Validation Leakage
- Premature Solvability
- Critical Clue Miss Recovery
- Unused Evidence Rate
- Alternate Reasoning Path Count

Formal Definition 없이 이름만 붙여 Machine Metric처럼 사용하지 않는다.

---

# 10. Deduction Tester Profile Map

Human Persona를 모방하기보다 **검증 전략 Profile**로 사용한다.

## P-DEDUCT-001 — Exhaustive Searcher

행동:
- 가능한 Candidate를 체계적으로 대입
- Evidence reasoning 최소화

목적:
- Brute-force vulnerability
- Validation leakage
- guess EV

검출.

---

## P-DEDUCT-002 — Minimal Evidence Solver

행동:
- 가능한 가장 적은 Evidence만 사용
- 조기 Conclusion 시도

목적:
- Premature solvability
- single-clue answer
- unnecessary evidence

검출.

---

## P-DEDUCT-003 — Full Evidence Verifier

행동:
- 획득 가능한 모든 Evidence 수집 후 결론

목적:
- Conclusion reachability
- contradiction
- orphan clue
- missing evidence

검출.

---

## P-DEDUCT-004 — Missed-clue Scenario

행동:
- 특정 Evidence 일부 누락

목적:
- single-point bottleneck
- alternate path
- recovery
- redundancy

검출.

---

## P-DEDUCT-005 — Wrong Hypothesis Tester

행동:
- 논리적으로 가능한 오답 가설을 유지
- 새로운 Evidence에 따라 수정 여부 확인

목적:
- contradiction structure
- wrong-answer recovery
- validation timing

검출.

---

# 10.1 Tester Interpretation Limit

다음 결론은 금지한다.

```text
LLM solved puzzle
→ human difficulty appropriate
```

또는:

```text
Exhaustive Agent failed
→ puzzle is good
```

Tester Profile의 역할은:

> **구조적 취약점 검출**

이다.

---

# 11. Human Validation Map

## H-DEDUCT-001 — Inference Ownership

> 정답을 게임이 알려준 것이 아니라 자신이 알아냈다고 느끼는가?

---

## H-DEDUCT-002 — Evidence Sufficiency

> 정답을 안 뒤 “필요한 단서가 충분히 있었다”고 느끼는가?

---

## H-DEDUCT-003 — Inference Explanation

> 왜 이 결론이 맞는지 자신의 말로 설명할 수 있는가?

매우 중요한 Human Metric.

---

## H-DEDUCT-004 — Stuck Reason

막힌 이유를 분류한다.

- Evidence not noticed
- Information forgotten
- Search failure
- Relation not understood
- Wrong hypothesis
- Rule misunderstanding
- Missing evidence
- Unknown

---

## H-DEDUCT-005 — Observation vs Reasoning

플레이 시간 중:
- 단서 탐색
- 정보 검색
- 관계 사고
- 입력 / validation

비중을 구분한다.

---

## H-DEDUCT-006 — Search Burden

> 추리보다 이미 본 정보를 다시 찾는 데 더 많은 시간을 쓰는가?

---

## H-DEDUCT-007 — Memory Burden

> 정답을 못 찾은 이유가 추론이 아니라 기억 실패인가?

---

## H-DEDUCT-008 — Notebook Utility

> Notebook이 사고를 돕는가, 사고를 대신하는가?

---

## H-DEDUCT-009 — Validation Fairness

> 정답 검증 방식이 자신의 추론을 시험한다고 느끼는가?

---

## H-DEDUCT-010 — Brute-force Temptation

> 생각하는 것보다 후보를 하나씩 넣는 편이 빠르다고 느끼는가?

---

## H-DEDUCT-011 — Hint Dependency

기록:
- Hint Use
- Hint Level
- Hint Timing
- Hint after wrong hypothesis

---

## H-DEDUCT-012 — Stuck Recovery

> 막힌 뒤 무엇을 다시 확인해야 할지 알 수 있었는가?

---

## H-DEDUCT-013 — Aha / Revelation

> 정답 순간 이전 Evidence가 다시 연결되는 경험이 있었는가?

**Human-only.**

---

## H-DEDUCT-014 — Cognitive Load

- 이름
- 관계
- 기호
- 문서 위치
- Rule

기억 부담이 추론을 방해하는지 확인한다.

---

## H-DEDUCT-015 — First-play Value

Fixed-solution 구조에서는:

> 다시 플레이하고 싶은가?

만 묻지 않는다.

함께 묻는다.

> 첫 플레이에 사용한 시간 대비 추론 경험과 만족도가 충분했는가?

---

# 12. Scale Handoff Candidates

이번 문서에서는 Genre × Scale Core를 확정하지 않는다.

# SCALE_HANDOFF-DEDUCT-001 — Logic QA Cost

## Finding

Deduction의 숨은 Production Cost는 Scene 수보다:

```text
Evidence
× Hypothesis
× Sequence
× Validation
× Hint
```

관계 조합에서 폭증할 수 있다.

## Supporting Evidence

Return of the Obra Dinn:
- 고밀도 단서 설계
- 사건 간 논리 QA
가 높은 비용이라고 Reference가 명시.

Golden Idol:
- 제한 장면에 정보 밀도와 추리 상호작용을 집중하는 Production model.

## Handoff

`GSC-DEDUCT-SOLO-001 Hidden Logic Cost`를 강하게 지지.

---

# SCALE_HANDOFF-DEDUCT-002 — Authored Relation Cost

사건 수보다:
- clue relation
- dialogue implication
- contradiction
- alternate reasoning path
- solution consistency

작성 비용이 중요하다.

---

# SCALE_HANDOFF-DEDUCT-003 — Localization Can Become Logic QA

언어·텍스트·wordplay가 Evidence Relation에 포함되면 Localization은 단순 번역이 아니라:

- ambiguity
- clue strength
- candidate reduction
- unintended answer

검증이 필요하다.

Chants of Sennaar 같은 Language Deduction은 특히 후속 연구 가치가 높다.

---

# SCALE_HANDOFF-DEDUCT-004 — Visual Evidence Accessibility QA

시각 단서가 핵심이면:
- resolution
- color vision
- screen size
- UI scaling
- input device

에 따라 Evidence Accessibility가 바뀔 수 있다.

---

# SCALE_HANDOFF-DEDUCT-005 — Limited Screens Do Not Mean Low Content Cost

Strange Horticulture / Golden Idol Production Reference는:
- 제한된 화면
- 작은 팀

이어도:
- 고유 텍스트
- 퍼즐 논리
- 오브젝트 / 장면 정보

제작비가 남는다는 Scale 경고를 지지한다.

---

# 12.1 Existing Genre × Scale Candidate Audit

`GSC-DEDUCT-SOLO-001 — Hidden Logic Cost`

**Decision:** `STRENGTHEN AS HANDOFF EVIDENCE`

이번 Genre Extraction은:
- Obra Dinn
- Golden Idol

에서 Hidden Logic / authored relation QA 비용을 지지한다.

하지만 이번 단계에서 Genre × Scale Core 최종 승격은 하지 않는다.

---

# 13. Universal Reclassification Candidates

# UC-RECLASS-DEDUCT-001 — UI Should Externalize Memory, not Decisions

`GC-DEDUCT-001`은 Deduction에서 매우 강하지만:
- Strategy
- Management
- Planning

에도 확장 가능하다.

다만 현재 가장 직접 Evidence가 Deduction에 편중되어 있으므로 Universal 승격하지 않는다.

---

# UC-RECLASS-DEDUCT-002 — Validation Timing Shapes Player Strategy

Wrong / success feedback timing이:
- Puzzle
- Strategy
- Experimentation

의 행동 전략을 바꿀 수 있다.

현재는 Deduction Evidence 중심.

**Status:** `UNIVERSAL RECLASSIFICATION CANDIDATE`

---

# UC-RECLASS-DEDUCT-003 — Wrong Answer Should Reduce Uncertainty without Solving the Problem

Puzzle / learning system 전체로 확장 가능성 있음.

현재 Stuck / Hint evidence가 부족해 Universal 승격 금지.

---

# UC-RECLASS-DEDUCT-004 — Formal Solvability ≠ Human Solvability

Deduction뿐 아니라:
- Puzzle
- Tutorial
- Strategy challenge

에도 적용 가능.

Studio Validation Methodology Candidate로 보낼 가치가 높다.

---

# 14. Evidence Gaps

# GAP-DEDUCT-001 — Human Inference Explanation

필요:
- 플레이어가 왜 결론이 맞는지 설명한 Transcript
- 정답 우연 / 추론 구분

---

# GAP-DEDUCT-002 — Stuck Reason

필요:
- 못 봄
- 못 기억함
- 못 찾음
- 관계 이해 실패
- 논리 오류

분류 데이터.

---

# GAP-DEDUCT-003 — Hint Dependency

필요:
- Hint usage
- level
- timing
- satisfaction
- ownership impact

---

# GAP-DEDUCT-004 — External Note Dependency

필요:
- external note 사용률
- built-in notebook 사용
- platform effect

---

# GAP-DEDUCT-005 — Critical Clue Miss

필요:
- clue discovery
- missed clue
- missed clue → stuck correlation
- revisit success

---

# GAP-DEDUCT-006 — Brute-force Behavior

Formal vulnerability뿐 아니라 실제 Player가:
- brute force를 시도하는가
- 언제 시도하는가
- reasoning 대신 선택하는가

데이터 부족.

---

# GAP-DEDUCT-007 — Wrong-answer Iteration

필요:
- wrong attempts
- immediate retries
- evidence revisit after wrong
- hypothesis revision

---

# GAP-DEDUCT-008 — Observation vs Reasoning Time

Deduction에서 매우 중요한 Human telemetry.

필요:
- search
- observation
- recall
- reasoning
- input

시간 분리.

---

# GAP-DEDUCT-009 — Solution Uniqueness QA

현재 Studio Reference에 개발자가 실제로 어떤:
- solver
- logic checker
- QA tool

을 사용했는지 부족.

---

# GAP-DEDUCT-010 — Alternate Reasoning Paths

필요:
- player path
- minimum evidence set
- missed clue robustness

---

# GAP-DEDUCT-011 — Validation Leakage

Formal model로 설계 가능하지만 실제 플레이어가 Feedback를 어떻게 exploit하는지 자료 부족.

---

# GAP-DEDUCT-012 — Cognitive Load

특히:
- names
- symbols
- relation graph
- documents

기억 부담과 reasoning performance 관계 부족.

---

# GAP-DEDUCT-013 — Replay / First-play Value

`GC-DEDUCT-002` 재분류를 더 정밀하게 하려면:
- completion time
- replay
- satisfaction
- price / value

자료 필요.

---

# GAP-DEDUCT-014 — Underperforming Deduction Controls

특히 필요:
- arbitrary solution
- excessive hint
- clue bottleneck
- search burden
- brute-force
- inaccessible visual clue

로 문제가 된 Postmortem / player data.

---

# 15. Additional References Needed

아래는 **Research Target**이며 현재 Core Evidence가 아니다.

# P0 — The Roottrees are Dead

## 강화 대상
- `GC-DEDUCT-001 UI / inference ownership`
- `GC-DEDUCT-003 Evidence relation`
- `GC-DEDUCT-006 Bottleneck`
- `GC-DEDUCT-007 Hypothesis space`

## Research Questions
- Obra Dinn형 identity deduction을 어떤 notebook 구조로 확장했는가?
- 관계 graph를 플레이어가 직접 만드는 정도는?
- validation / brute-force 방지는?

## 필요한 Evidence
- Developer postmortem
- puzzle design interview
- player stuck / hint data if public

---

# P0 — Her Story

## 강화 대상
- Search burden
- Player-created hypothesis
- Evidence accessibility
- non-linear information retrieval

## Research Questions
- 검색어 선택이 추론인가 retrieval puzzle인가?
- missable information과 player agency의 경계는?

---

# P0 — Outer Wilds

## 강화 대상
- Knowledge Progression
- Evidence Recontextualization
- Failure / revisit
- no-stat progression

## Boundary
Exploration Core와 분리.

## Research Questions
- 새 Knowledge가 이전 장소 / 정보 의미를 어떻게 바꾸는가?
- Knowledge gate가 실제 inference인가 단순 key인가?

---

# P0 — Unheard

## 강화 대상
- Auditory Evidence
- Identity / Relationship
- Information Replay
- Search / memory burden

---

# P1 — Paradise Killer

## 강화 대상
- Evidence collection
- accusation timing
- incomplete certainty
- player commitment
- unique vs ambiguous solution

---

# P1 — The Painscreek Killings

## 강화 대상
- Open investigation
- external note burden
- clue discovery
- stuck-state recovery

---

# P1 — Shadows of Doubt

## 강화 대상
- Systemic / procedural investigation
- generated evidence
- solution integrity
- procedural QA

## Research Questions
Procedural mystery에서:
- evidence sufficiency
- contradiction
- invalid case

를 어떻게 보장하는가?

---

# P1 — Telling Lies

## 강화 대상
- retrieval burden
- narrative investigation
- information organization
- search dependency

---

# P1 — Design-focused Golden Idol Research

현재 REF-30은 Production 중심이다.

별도 Design Study가 필요하다.

Research:
- word token system
- scene information density
- answer grammar
- validation timing
- alternate reasoning

---

# P1 — Design-focused Chants of Sennaar Research

현재 REF-31은 Production 중심이다.

Research:
- symbol hypothesis
- notebook validation
- language ambiguity
- recontextualization
- false hypothesis recovery

---

# 16. Promotion Table

| ID | Name | Decision | Status | Confidence |
|---|---|---|---|---|
| GC-DEDUCT-001 | UI Externalizes Memory/Search, Not Inference | STRENGTHEN | **PROVISIONAL CORE** | VERY HIGH |
| GC-DEDUCT-002 | Solution Knowledge Consumption / Low Replay | RECLASSIFY | PRODUCT / CONTENT CONSUMPTION CANDIDATE | HIGH |
| GC-DEDUCT-003 | Evidence Relations Make Conclusion Reachable | NEW | **PROVISIONAL CORE** | VERY HIGH |
| GC-DEDUCT-004 | Validation Design Preserves Reasoning | NEW | **PROVISIONAL CORE** | HIGH |
| GC-DEDUCT-005 | Evidence Accessibility vs Sufficiency | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-DEDUCT-006 | Avoid Single-point Bottlenecks | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-DEDUCT-007 | Hypothesis Space Reduced by Evidence | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-DEDUCT-008 | Stuck Recovery Preserves Inference | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-DEDUCT-009 | Memory/Search Burden | NEW | MERGE CANDIDATE → GC-DEDUCT-001 Sub-rule | MEDIUM-HIGH |
| GC-DEDUCT-010 | Knowledge Recontextualizes Evidence | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-DEDUCT-011 | Deduction Pacing | NEW | KEEP AS CANDIDATE | MEDIUM-LOW |
| GC-DEDUCT-012 | Multiple Reasoning Paths | NEW | KEEP AS CANDIDATE | MEDIUM |

---

# 17. Deduction Reviewer Default Set

신규 Deduction / Information 기획을 검토할 때 우선 적용할 15개 질문.

## Q1 — Inclusion

> **플레이어가 직접 밝혀야 하는 Hidden Conclusion이 있고, Evidence 관계를 통해 이를 추론하는가?**

---

## Q2 — Information Processing Boundary

> **이미 알려진 Rule을 적용하는가, 알려지지 않은 Conclusion을 Evidence 관계로 만드는가?**

Pure Deduction이 아니라면 Deduction Core를 과도 적용하지 않는다.

---

## Q3 — Evidence Sufficiency

> **정답에 필요한 Evidence가 게임 안에 존재하는가?**

관련:
`GC-DEDUCT-003`

---

## Q4 — Evidence Relation

> **단서를 발견하는 것 외에 둘 이상의 정보 관계를 구성해야 하는가?**

관련:
`GC-DEDUCT-003`

---

## Q5 — Logical Reachability

> **정답을 아는 작가가 아니라 정답을 모르는 플레이어 관점에서 Conclusion Chain을 설명할 수 있는가?**

관련:
`GC-DEDUCT-003`

---

## Q6 — Evidence Accessibility

> **필수 Evidence는 합리적으로 발견하고 재확인할 수 있는가?**

관련:
`GC-DEDUCT-005`

---

## Q7 — Inference Ownership

> **UI가 기억 / 검색 / 정리를 돕되 Relation과 Conclusion은 플레이어에게 남기는가?**

관련:
`GC-DEDUCT-001`

---

## Q8 — Single-point Failure

> **한 단서 누락이 전체 Progress를 영구 차단하지 않는가?**

관련:
`GC-DEDUCT-006`

---

## Q9 — Hypothesis Space

> **Evidence가 가능한 정답 후보를 실제로 줄이는가, Guess / exhaustive search가 더 효율적인가?**

관련:
`GC-DEDUCT-007`

---

## Q10 — Validation

> **Validation Timing과 Granularity가 Reasoning을 보존하는가?**

관련:
`GC-DEDUCT-004`

---

## Q11 — Wrong Hypothesis

> **틀린 가설을 새로운 Evidence로 반박하고 수정할 수 있는가?**

관련:
`GC-DEDUCT-008`

---

## Q12 — Search / Memory Burden

> **막힌 이유가 추론이 아니라 이미 본 정보를 기억하거나 다시 찾는 비용은 아닌가?**

관련:
`GC-DEDUCT-001 / 009`

---

## Q13 — Hint / Stuck Recovery

> **Hint가 답을 주는가, 다시 사고할 위치와 관계를 제시하는가?**

관련:
`GC-DEDUCT-008`

---

## Q14 — Formal vs Human

> **Solution Integrity는 Formal Tester로, Aha / Fairness / Readability / Ownership은 Human Test로 분리했는가?**

---

## Q15 — Product Value

> **Solution Knowledge로 Replayability가 낮아진다면 First-play Deduction Density와 Value Model이 이를 정당화하는가?**

관련:
`GC-DEDUCT-002 RECLASSIFIED`

---

# 18. Default Metric Bundle

Metric은 Criteria가 아니다.

Threshold는 프로젝트별 Validation Planner가 잠근다.

## Formal / Machine

- Evidence Node Count
- Evidence Relation Count
- Critical Evidence Count
- Redundant Evidence Count
- Orphan Evidence Rate
- Conclusion Reachability
- Evidence → Conclusion Path Count
- Mandatory Evidence Bottleneck
- Minimum Evidence Set Size
- Dependency Depth
- Solution Count
- Contradiction Count
- Ambiguous State Count
- Unsatisfied Constraint Count
- Guess Space Size
- Random Guess Success Rate
- Immediate-validation Information Gain

### Formal / model-dependent

- Validation Leakage
- First Solvable State
- Stuck State Reachability
- Unused Evidence Rate
- Alternate Reasoning Path Count
- Premature Solvability
- Critical Clue Miss Recovery
- Attempts to Solve without Evidence

Formal Definition 없이 자동 Metric으로 사용하지 않는다.

---

## Instrumented Player Telemetry

- Evidence Revisit Rate
- Notebook Open Rate
- Search Time
- Character / Evidence Lookup Frequency
- Hint Usage
- Hint Timing
- Wrong-answer Attempts
- Time to Conclusion
- Rapid Guess Sequence Rate
- Evidence Check → Conclusion Time

### Instrumented / Human report

- External Note Usage

### Instrumented / model-dependent

- Critical Clue Miss Rate

---

## Human

- Inference Ownership
- Evidence Sufficiency Experience
- Inference Explanation Accuracy
- Perceived Fairness
- Stuck Reason
- Search Burden
- Memory Burden
- Hint Satisfaction
- Aha / Revelation Quality
- First-play Value
- Cognitive Load
- Notebook Utility
- Validation Fairness

---

## Hybrid

- Deduction Difficulty
- Stuck Severity
- Validation Quality
- Brute-force Temptation
- Puzzle Pacing
- Solution Fairness
- Evidence Readability
- Observation vs Reasoning Ratio
- Wrong-hypothesis Recovery Quality
- Evidence Accessibility
- Knowledge Recontextualization Quality

---

# 19. Self-Review Result

## Check 1 — Hidden Information ≠ Deduction
**PASS**

Hiddenness가 아니라 Evidence relation과 player-owned conclusion을 기준으로 삼았다.

## Check 2 — More Clues ≠ More Depth
**PASS**

Evidence Count보다 Relation / Reachability / Hypothesis reduction을 우선했다.

## Check 3 — Observation vs Inference
**PASS**

별도 Human/Hybrid axis로 유지했다.

## Check 4 — Memory Test vs Deduction
**PASS**

`GC-DEDUCT-001 / 009`, Anti-pattern으로 분리했다.

## Check 5 — Search Burden
**PASS**

Search Time을 Deduction Depth로 간주하지 않았다.

## Check 6 — UI Solves Inference
**PASS**

`GC-DEDUCT-001`의 핵심 경계로 정의했다.

## Check 7 — Brute-force
**PASS**

`GC-DEDUCT-004`, Formal metric, Anti-pattern으로 직접 검증한다.

## Check 8 — Immediate Validation always bad
**PASS**

Papers, Please / Tutorial 등 Counter / Boundary를 보존했다.

## Check 9 — Obra Dinn overgeneralization
**PASS WITH GAPS**

Obra Dinn 의존도가 높음을 명시하고 Provisional 수를 3개로 제한했다.

## Check 10 — Production Evidence ≠ Design Evidence
**PASS**

Golden Idol / Chants / Strange Horticulture는 Tier B 유지.

## Check 11 — Formal Solvability ≠ Human Difficulty
**PASS**

명시적으로 분리했다.

## Check 12 — LLM Solves = Human Solvability
**PASS**

Deduction Tester Profile을 구조 검증 도구로만 사용한다.

## Check 13 — Deduction vs Narrative
**PASS**

Story Revelation 자체는 Deduction Core가 아니라고 Anti-pattern으로 분리했다.

## Check 14 — Low Replayability
**PASS**

자동 승인/감점하지 않고 `GC-DEDUCT-002`를 Product / Content Consumption으로 Reclassify했다.

## Check 15 — Reviewer Usability
**PASS**

15개 Default Question으로 압축했다.

---

# 20. Final Position

현재 Studio OS Deduction / Information Knowledge Base에서 우선 `Provisional Genre Core`로 사용할 항목은 **3개**다.

1. `GC-DEDUCT-001 — UI Should Externalize Memory / Search, Not Inference`
2. `GC-DEDUCT-003 — Evidence Relations Must Make the Conclusion Logically Reachable`
3. `GC-DEDUCT-004 — Validation Design Must Preserve Reasoning`

기존:

`GC-DEDUCT-002 — Low Replayability is not automatically a defect`

는 Genre Core에서 제외하고 다음으로 재분류한다.

> **Product / Content Consumption Core Candidate — Solution Knowledge Consumption Changes the Value Model**

Candidate는 다음과 같다.

- `GC-DEDUCT-005 — Evidence Accessibility`
- `GC-DEDUCT-006 — Single-point Bottleneck`
- `GC-DEDUCT-007 — Hypothesis Space`
- `GC-DEDUCT-008 — Stuck Recovery`
- `GC-DEDUCT-009 — Memory / Search Burden`
- `GC-DEDUCT-010 — Knowledge Recontextualization`
- `GC-DEDUCT-011 — Deduction Pacing`
- `GC-DEDUCT-012 — Multiple Reasoning Paths`

이 중 `GC-DEDUCT-009`는 현재 별도 Core보다 `GC-DEDUCT-001`의 Sub-rule로 병합될 가능성이 높다.

이번 Extraction의 가장 중요한 문장은:

> **Deduction Depth는 “얼마나 많이 숨겼는가”가 아니라 “플레이어가 Evidence 사이의 어떤 관계를 직접 구성해야 하나의 Conclusion이 남는가”로 평가한다.**

또한:

> **Formal Solver가 정답을 찾을 수 있다는 사실은 Logic Integrity Evidence이지 Human Difficulty / Fairness Evidence가 아니다.**

현재 가장 큰 Evidence Gap은:

> **Human Inference Explanation / Stuck Reason / Brute-force Behavior / Validation Leakage / Alternate Reasoning Path / Search-Memory Burden / Underperforming Control**

이다.

따라서 다음 Reference 확장은 유명 Mystery title 수를 늘리는 것보다:

> **플레이어가 실제로 어떤 단서에서 막히는가?  
> Guess는 언제 Reasoning보다 유리해지는가?  
> Notebook은 언제 사고를 돕고 언제 대신하는가?  
> Knowledge를 얻었을 때 이전 Evidence가 실제로 재해석되는가?**

에 개발자 분석 또는 Playtest Data가 있는 사례를 우선 조사하는 편이 효율적이다.

---

# 21. Source Trace

## Primary Deduction Design Evidence
- REF-17 — Return of the Obra Dinn

## Deduction / Identification Support
- REF-30 — The Case of the Golden Idol (`Production-heavy`)
- REF-31 — Chants of Sennaar (`Production-heavy`)
- REF-29 — Strange Horticulture (`Production-heavy`)

## Information / Investigation Hybrid
- REF-01 — Papers, Please
- REF-48 — The Operator (`Commercial-heavy`)

## Adjacent / Control
- REF-03 — Into the Breach
- REF-16 — Invisible, Inc.
- REF-19 — Cultist Simulator
- REF-23 — Citizen Sleeper
- REF-09 — Reigns
- REF-10 — 80 Days

## Baseline
- STUDIO_CORE_CANDIDATES_v0.2
- Studio OS — Evidence-Based Core Extraction Master Prompt v0.2
- Studio OS — Deduction / Information Genre Core Deep Extraction Prompt v0.1

---

# 22. Traceability Rule

Core는 원본 Reference를 대체하지 않는다.

신규 프로젝트 Review에서 Deduction 위험 신호가 발생하면:

```text
Genre Core
↓
Primary Reference
↓
Evidence Structure
↓
Inference Mechanism
↓
Validation
↓
Boundary / Trade-off
↓
Current Project
```

순서로 다시 내려가 확인한다.

`DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1`은 Studio OS Reviewer가 추리 소재의 표면적 유사성이 아니라 **Evidence Structure와 Player-owned Inference**를 빠르고 일관되게 평가하기 위한 압축된 Genre 판단 계층이다.
