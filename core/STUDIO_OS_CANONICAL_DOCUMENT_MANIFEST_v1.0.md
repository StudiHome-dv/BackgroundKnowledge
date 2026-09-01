# STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0

**Studio OS — Canonical Document Manifest**  
**Status:** `APPROVED_AS_STUDIO_OS_CANONICAL_MANIFEST_V1`  
**Manifest Version:** `v1.0`  
**Source of Truth:** `GITHUB`  
**Recommended Repository:** `Studio-OS`  
**Canonical Branch:** `main`  
**Canonical Reviewer Runtime:** `REVIEWER_RUNTIME_SPECIFICATION_v1.0.md`  
**Studio Core:** `Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`  
**Genre Master:** `GENRE_CORE_MASTER_INDEX_v0.3.md`  
**Scale Baseline:** `SCALE_CORE_BASELINE_v0.2.md`  
**Active Independent GSC:** `0`  
**Next:** `Studio OS Core Package v1.0`

---

# 1. Executive Summary

이 Manifest는 Studio OS Repository에서 다음 질문에 답하는 **단일 Canonical Source Map**이다.

1. 현재 실행 기준 문서는 무엇인가?
2. 어떤 문서를 항상 사용해야 하는가?
3. 어떤 Genre 문서는 Routing 결과에 따라 조건부로 읽는가?
4. Reference는 언제 조회하는가?
5. Runtime Test는 어디에 보관하는가?
6. Historical / Consolidation 문서는 어디에 두는가?
7. Deprecated 문서는 어떻게 격리하는가?
8. 새 Version 승인 시 어떤 파일이 이전 Canonical을 대체하는가?
9. 개별 게임 GDD와 Studio OS Knowledge를 어떻게 분리하는가?
10. ChatGPT / Claude / Cursor가 어떤 파일을 Source of Truth로 따라야 하는가?

Studio OS의 Canonical Source of Truth는:

```text
GitHub Repository
+
main branch
+
Current Approved Manifest
```

다.

다음은 Source of Truth가 아니다.

```text
ChatGPT Conversation Memory
Claude Conversation Memory
Cursor Chat
개인 메모
임시 Prompt
Dry-run Result
Local Uncommitted File
Unmerged Branch
```

Canonical 원칙:

```text
AI Conversation Memory
≠
Canonical Project Knowledge
```

```text
Current Manifest
→ Current Canonical Version
```

Runtime v1.0 기준 Canonical Active 문서는:

```text
DOC-MANIFEST
DOC-CORE-UNIVERSAL
DOC-GENRE-MASTER
DOC-SCALE-BASELINE
DOC-RUNTIME-REVIEWER
```

총 5개다.

Genre-specific Canonical 문서는 9개이며 모두:

`CANONICAL_CONDITIONAL`

이다.

Reference Library는:
`REFERENCE / LOOKUP_ONLY`

Runtime Dry-run은:
`RUNTIME_TEST`

과거 Version / Consolidation / Correction은:
`HISTORICAL / NEVER`

이다.

개별 게임 GDD는:
`PROJECT_EXTERNAL`

이며 Studio OS Core Repository에 Canonical Knowledge로 복제하지 않는다.

---

# 2. Manifest Purpose

Manifest가 소유하는 것은 **Rule 내용 자체**가 아니라:

- Canonical file identity
- current version pointer
- repository path
- classification
- load policy
- supersession
- dependencies
- source-of-truth precedence

이다.

Canonical Rule 내용은 각 Layer 문서가 소유한다.

예:

```text
Universal Rule
→ Studio Core

Genre Rule
→ Individual Genre Baseline

Genre Routing
→ Genre Master

Scale Rule
→ Scale Baseline

Runtime Execution
→ Reviewer Runtime
```

Manifest는 이 관계를 명시적으로 연결한다.

---

# 3. Source-of-Truth Rule

## Canonical Git State

Studio OS의 현재 Canonical 상태는:

> **GitHub `main` branch에 존재하는 최신 승인 Manifest가 가리키는 승인 문서**

로 정의한다.

권장 운영:

```text
Working Branch / PR
↓
Review
↓
Approval
↓
Canonical File Update
↓
Manifest Update
↓
Merge to main
↓
Canonical State
```

PR / local draft / AI workspace는 Canonical이 아니다.

## Optional Release Tag

Core Package release 시:

```text
studio-os-v1.0
studio-os-v1.1
...
```

처럼 Git tag를 둘 수 있다.

Tag는 snapshot convenience이며 Canonical pointer의 1차 owner는 Manifest다.

---

# 4. Canonical Classification

모든 Repository 문서는 다음 중 하나로 분류한다.

## A. CANONICAL_ACTIVE

현재 Studio OS 실행에 사용하는 최신 승인 문서.

## B. CANONICAL_CONDITIONAL

Routing / Layer activation 결과에 따라 사용하는 최신 승인 문서.

## C. REFERENCE

Core / Pattern / Boundary의 근거가 되는 사례·시장·제작·방법론 자료.

## D. RUNTIME_TEST

Reviewer Runtime Regression / Dry-run 검증 자료.

## E. HISTORICAL

과거 Version / Consolidation / Decision Trace / inactive draft.

## F. DEPRECATED

현재 Rule로 사용하면 안 되며 유지 자체가 특별한 이유를 필요로 하는 문서.

## G. PROJECT_EXTERNAL

개별 게임 Repository가 소유해야 하는 GDD / review / implementation 자료.

---

# 5. Recommended GitHub Repository Architecture

```text
Studio-OS/
│
├─ README.md
│
├─ manifest/
│  └─ STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md
│
├─ core/
│  ├─ universal/
│  │  └─ Studio_OS_Evidence_Based_Core_Extraction_v0.4.md
│  │
│  ├─ genre/
│  │  ├─ GENRE_CORE_MASTER_INDEX_v0.3.md
│  │  └─ baselines/
│  │     ├─ Deckbuilding/
│  │     ├─ Management/
│  │     ├─ Roguelike/
│  │     ├─ Deduction/
│  │     ├─ Narrative/
│  │     ├─ Strategy/
│  │     ├─ Simulation/
│  │     ├─ RPG/
│  │     └─ Action/
│  │
│  ├─ scale/
│  │  └─ SCALE_CORE_BASELINE_v0.2.md
│  │
│  └─ runtime/
│     └─ REVIEWER_RUNTIME_SPECIFICATION_v1.0.md
│
├─ references/
│  ├─ REF_Reference_Master_Index.md
│  ├─ games/
│  ├─ market/
│  ├─ production/
│  ├─ research/
│  └─ methodology/
│
├─ tests/
│  └─ reviewer_runtime/
│     ├─ fixtures/
│     │  ├─ MCC/
│     │  └─ MagicWord/
│     └─ assessments/
│
└─ history/
   ├─ runtime/
   ├─ consolidation/
   ├─ drafts/
   └─ deprecated/
```

추가 폴더는 현재 필요 최소 수준으로 제한한다.

`history/drafts/`는 기존 `DRAFT_FOR_REVIEW` validation / tester 문서를 Active Runtime과 분리하기 위해 사용한다.

---

# 6. Stable Logical Document ID Rule

파일명과 별도로 Stable Logical ID를 사용한다.

예:

```text
DOC-RUNTIME-REVIEWER

v1.0
→
v1.1
→
v2.0
```

Logical ID는 유지된다.

Filename은 변경될 수 있다.

목적:

- naming inconsistency 흡수
- version replacement 추적
- AI / script reference 안정화
- Manifest diff 단순화

---

# 7. Canonical Active Registry

모든 아래 Entry의:

`Source of Truth = GITHUB`

이다.

| ID | File | Path | Classification | Layer | Version | Status | Runtime Load | Context Mode | Load Condition | Supersedes | Dependencies | Used By |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `DOC-MANIFEST` | `STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md` | `manifest/STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md` | CANONICAL_ACTIVE | Repository / Source Map | v1.0 | APPROVED_AS_STUDIO_OS_CANONICAL_MANIFEST_V1 | ALWAYS | FULL / DIRECT | Every Studio OS operation | `00_Studio_OS_Index_v0.2_APPROVED.md`의 Canonical source-resolution 역할 | None | All tools / maintainers |
| `DOC-CORE-UNIVERSAL` | `Studio_OS_Evidence_Based_Core_Extraction_v0.4.md` | `core/universal/Studio_OS_Evidence_Based_Core_Extraction_v0.4.md` | CANONICAL_ACTIVE | Universal / Studio Core | v0.4 | Canonical Universal Sync — Reviewer Runtime Ready | ALWAYS | SECTION_LOOKUP | Every Project Review; active sections after applicability | v0.3 | Reference Evidence / Universal consolidation history | Reviewer Runtime, Genre Master |
| `DOC-GENRE-MASTER` | `GENRE_CORE_MASTER_INDEX_v0.3.md` | `core/genre/GENRE_CORE_MASTER_INDEX_v0.3.md` | CANONICAL_ACTIVE | Genre Router | v0.3 | INTEGRATION_BASELINE / Canonical Universal Parent Map Synced | ALWAYS | SECTION_LOOKUP | Every Project Review routing | v0.2 | Universal v0.4, 9 Genre Baselines, Scale v0.2 | Reviewer Runtime |
| `DOC-SCALE-BASELINE` | `SCALE_CORE_BASELINE_v0.2.md` | `core/scale/SCALE_CORE_BASELINE_v0.2.md` | CANONICAL_ACTIVE | Scale / Production Routing | v0.2 | APPROVED_AS_SCALE_ROUTING_BASELINE | ALWAYS | SECTION_LOOKUP | PASS 7/8; detailed scale/handoff trace | v0.1 Approved | Production references, Genre Master | Reviewer Runtime |
| `DOC-RUNTIME-REVIEWER` | `REVIEWER_RUNTIME_SPECIFICATION_v1.0.md` | `core/runtime/REVIEWER_RUNTIME_SPECIFICATION_v1.0.md` | CANONICAL_ACTIVE | Runtime | v1.0 | APPROVED_AS_REVIEWER_RUNTIME_V1_BASELINE | ALWAYS | FULL | Every Project Review | Runtime v0.1 + Correction #01 | Universal v0.4, Genre Master v0.3, Scale v0.2 | Reviewer / Regression fixtures |

## Active Canonical Count

```text
CANONICAL_ACTIVE:
5
```

---

# 8. Canonical Conditional Genre Registry

현재 9개 Genre Baseline은 모두:

`CANONICAL_CONDITIONAL`

이다.

| ID | File | Path | Classification | Layer | Version | Status | Runtime Load | Context Mode | Load Condition | Supersedes | Dependencies | Used By |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `DOC-GENRE-DECK` | `DECKBUILDING_CORE_CANDIDATES_v0.1.md` | `core/genre/baselines/Deckbuilding/DECKBUILDING_CORE_CANDIDATES_v0.1.md` | CANONICAL_CONDITIONAL | Genre / Deckbuilding | v0.1 | APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE | CONDITIONAL | SECTION_LOOKUP | Deckbuilding L1/L2/L3 per Runtime loading rule | None | Universal / reference evidence | Genre Master / Reviewer |
| `DOC-GENRE-MGMT` | `MANAGEMENT_CORE_CANDIDATES_v0.1.md` | `core/genre/baselines/Management/MANAGEMENT_CORE_CANDIDATES_v0.1.md` | CANONICAL_CONDITIONAL | Genre / Management | v0.1 | APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE | CONDITIONAL | SECTION_LOOKUP | Management L1/L2/L3 | None | Universal / reference evidence | Genre Master / Reviewer |
| `DOC-GENRE-ROGUE` | `ROGUELIKE_CORE_CANDIDATES_v0.1.md` | `core/genre/baselines/Roguelike/ROGUELIKE_CORE_CANDIDATES_v0.1.md` | CANONICAL_CONDITIONAL | Genre / Roguelike | v0.1 | APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE | CONDITIONAL | SECTION_LOOKUP | Roguelike L1/L2/L3 | None | Universal / reference evidence | Genre Master / Reviewer |
| `DOC-GENRE-DEDUCT` | `DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1.md` | `core/genre/baselines/Deduction/DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1.md` | CANONICAL_CONDITIONAL | Genre / Deduction-Information | v0.1 | APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE | CONDITIONAL | SECTION_LOOKUP | Deduction L1/L2/L3 | None | Universal / reference evidence | Genre Master / Reviewer |
| `DOC-GENRE-NARR` | `NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1.md` | `core/genre/baselines/Narrative/NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1.md` | CANONICAL_CONDITIONAL | Genre / Narrative-Systemic | v0.1 | APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE | CONDITIONAL | SECTION_LOOKUP | Narrative L1/L2/L3 | None | Universal / reference evidence | Genre Master / Reviewer |
| `DOC-GENRE-STRAT` | `STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md` | `core/genre/baselines/Strategy/STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md` | CANONICAL_CONDITIONAL | Genre / Strategy | v0.1 | APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE | CONDITIONAL | SECTION_LOOKUP | Strategy L1/L2/L3 | `STRATEGY_CORE_CANDIDATES_v0.1.md` draft | Universal / reference evidence | Genre Master / Reviewer |
| `DOC-GENRE-SIM` | `SIMULATION_CORE_CANDIDATES_v0.1_APPROVED.md` | `core/genre/baselines/Simulation/SIMULATION_CORE_CANDIDATES_v0.1_APPROVED.md` | CANONICAL_CONDITIONAL | Genre / Simulation | v0.1 | APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE | CONDITIONAL | SECTION_LOOKUP | Simulation L1/L2/L3 | `SIMULATION_CORE_CANDIDATES_v0.1.md` draft | Universal / reference evidence | Genre Master / Reviewer |
| `DOC-GENRE-RPG` | `RPG_CORE_CANDIDATES_v0.1_APPROVED.md` | `core/genre/baselines/RPG/RPG_CORE_CANDIDATES_v0.1_APPROVED.md` | CANONICAL_CONDITIONAL | Genre / RPG | v0.1 | APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE | CONDITIONAL | SECTION_LOOKUP | RPG L1/L2/L3 | `RPG_CORE_CANDIDATES_v0.1.md` draft | Universal / reference evidence | Genre Master / Reviewer |
| `DOC-GENRE-ACTION` | `ACTION_CORE_CANDIDATES_v0.1_APPROVED.md` | `core/genre/baselines/Action/ACTION_CORE_CANDIDATES_v0.1_APPROVED.md` | CANONICAL_CONDITIONAL | Genre / Action | v0.1 | APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE | CONDITIONAL | SECTION_LOOKUP | Action L1/L2/L3 | `ACTION_CORE_CANDIDATES_v0.1.md` draft | Universal / reference evidence | Genre Master / Reviewer |

## Genre Load Guard

```text
Genre Routing L0
→ baseline Load 금지
```

```text
Genre Routing L1/L2/L3
→ Runtime Loading Weight에 따라 필요한 section만 조회
```

모든 Genre baseline을 매 Review마다 기본 Context에 넣지 않는다.

---

# 9. Runtime Load Policy

Manifest가 사용하는 Load Class:

```text
ALWAYS
CONDITIONAL
LOOKUP_ONLY
NEVER
```

## ALWAYS

Review 실행에 항상 Canonical dependency로 존재해야 함.

현재:
- Manifest
- Reviewer Runtime
- Universal Core
- Genre Master
- Scale Baseline

## CONDITIONAL

Routing / Layer 결과가 활성화될 때만 조회.

현재:
- 9 Genre Baselines

## LOOKUP_ONLY

필요한 evidence trace / maintenance / regression 작업에서만 조회.

현재:
- Reference Library
- Runtime Tests

## NEVER

정상 Runtime의 Source로 사용 금지.

현재:
- Historical
- Deprecated

---

# 10. Context Access Policy

`Runtime Load`와 `Full Context Injection`은 동일하지 않다.

Context 효율을 위해 다음을 권장한다.

## FULL / DIRECT

항상 전체 구조를 직접 사용할 가치가 높은 문서:

1. `DOC-MANIFEST`
2. `DOC-RUNTIME-REVIEWER`

## SECTION_LOOKUP

Canonical dependency지만 매번 전체 문서를 프롬프트에 넣을 필요는 없는 문서:

3. `DOC-CORE-UNIVERSAL`
4. `DOC-GENRE-MASTER`
5. `DOC-SCALE-BASELINE`

정상 실행:

```text
Runtime
↓
Applicability / Routing
↓
Relevant section lookup
```

## CONDITIONAL SECTION_LOOKUP

9개 Genre Baseline.

Routing 결과 해당 Genre가 L1/L2/L3일 때만 읽는다.

## LOOKUP_ONLY

Reference / Test / History.

---

# 11. Reviewer Runtime Minimum Canonical Set

Studio OS Reviewer를 실행하기 위한 **Logical Minimum Set**:

```text
1. DOC-MANIFEST
2. DOC-RUNTIME-REVIEWER
3. DOC-CORE-UNIVERSAL
4. DOC-GENRE-MASTER
5. DOC-SCALE-BASELINE
+
6. Routed Genre Baselines only
```

Context injection 관점에서는:

```text
Full:
Manifest + Runtime

Lookup:
Universal + Genre Master + Scale

Conditional Lookup:
Routed Genre Baselines
```

가 기본 권장이다.

Tool 환경이 retrieval을 지원하지 않고 모든 Source를 한 번에 제공해야 한다면 Logical Minimum Set 전체를 제공한다.

---

# 12. Knowledge Maintenance Extended Set

Core / Evidence 업데이트 작업에는 Reviewer Runtime Minimum Set보다 넓은 자료를 사용한다.

```text
Canonical Core
+
Relevant Genre Baseline
+
REF_Reference_Master_Index
+
Relevant References
+
Historical Decision Trace when needed
```

History는 maintenance evidence trace용일 뿐 current rule owner가 아니다.

---

# 13. Reference Library Policy

Reference Library는 매 Review마다 전부 읽지 않는다.

정상 흐름:

```text
Canonical Core
↓
Project Finding
↓
Need deeper evidence trace?
YES
↓
Reference Master Index
↓
Relevant Reference lookup
```

Reference 사용 목적:

- Core 근거 추적
- Boundary 확인
- 새로운 Evidence 추가
- Rule 재검토
- future Promotion Review

## Canonical Guardrail

```text
Reference Game Observation
≠
Canonical Rule
```

항상:

```text
Reference
↓
Evidence
↓
Pattern
↓
Canonical Review
↓
Canonical Core
```

를 거친다.

---

# 14. Current Reference Registry

모두:

```text
Classification:
REFERENCE

Runtime Load:
LOOKUP_ONLY

Source of Truth:
GITHUB
```

| ID | File | Recommended Path | Reference Role |
|---|---|---|---|
| `DOC-REF-MASTER` | `REF_Reference_Master_Index.md` | `references/REF_Reference_Master_Index.md` | Reference routing / index |
| `DOC-REF-LAYER1` | `REF_Layer_1_Core_Design.md` | `references/research/REF_Layer_1_Core_Design.md` | Core design evidence |
| `DOC-REF-LAYER2` | `REF_Layer_2_Specialized.md` | `references/research/REF_Layer_2_Specialized.md` | Specialized design evidence |
| `DOC-REF-LAYER3` | `REF_Layer_3_Solo_Micro_Production.md` | `references/production/REF_Layer_3_Solo_Micro_Production.md` | Solo/Micro production evidence |
| `DOC-REF-LAYER4` | `REF_Layer_4_Commercial.md` | `references/market/REF_Layer_4_Commercial.md` | Commercial / market evidence |
| `DOC-REF-LAYER5` | `REF_Layer_5_Korean_Selection.md` | `references/market/REF_Layer_5_Korean_Selection.md` | Korean selection / award evidence |
| `DOC-REF-KR-2024` | `REF_2024_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md` | `references/market/REF_2024_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md` | Market / award benchmark |
| `DOC-REF-KR-2025` | `REF_2025_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md` | `references/market/REF_2025_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md` | Market / award benchmark |
| `DOC-REF-KR-2026` | `REF_2026_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md` | `references/market/REF_2026_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md` | Market / award benchmark |
| `DOC-REF-CASE-TEMPLATE` | `REF_Game_Design_Case_Study_Template_v1.0.md` | `references/methodology/REF_Game_Design_Case_Study_Template_v1.0.md` | Case study methodology/template |
| `DOC-REF-REVIEW-TEMPLATE` | `REF_Game_Design_Reviewer_Final_Evaluation_Template_v2.0.md` | `references/methodology/REF_Game_Design_Reviewer_Final_Evaluation_Template_v2.0.md` | Historical/reusable review methodology reference |
| `DOC-REF-REVIEW-INSTRUCTIONS` | `REF_Game_Design_Reviewer_Project_Instructions_v2.0.md` | `references/methodology/REF_Game_Design_Reviewer_Project_Instructions_v2.0.md` | Reviewer methodology reference |

Reference registry의 개별 game case study가 향후 늘어나면:

```text
references/games/
```

에 저장하고 `REF_Reference_Master_Index.md`에서 routing한다.

---

# 15. Runtime Test Policy

Dry-run / regression 자료는:

`RUNTIME_TEST`

다.

목적:

- Runtime Routing Regression
- Dedup Regression
- Scope Regression
- Enum Regression
- UC006 Regression
- Scale Resolution Regression

## Current Runtime Test Registry

| ID | File | Path | Classification | Runtime Load | Purpose |
|---|---|---|---|---|---|
| `TEST-RUNTIME-MCC-01` | `REVIEWER_RUNTIME_DRYRUN_01_PROJECT_MCC_v0.1.md` | `tests/reviewer_runtime/fixtures/MCC/REVIEWER_RUNTIME_DRYRUN_01_PROJECT_MCC_v0.1.md` | RUNTIME_TEST | LOOKUP_ONLY | Prototype-slice / Strategy-Management-Simulation regression |
| `TEST-RUNTIME-MAGIC-02` | `REVIEWER_RUNTIME_DRYRUN_02_MAGIC_WORD_v0.1.md` | `tests/reviewer_runtime/fixtures/MagicWord/REVIEWER_RUNTIME_DRYRUN_02_MAGIC_WORD_v0.1.md` | RUNTIME_TEST | LOOKUP_ONLY | Deck/Rogue/Strategy/UC006/Unresolved-scale regression |
| `TEST-RUNTIME-CROSS-01` | `REVIEWER_RUNTIME_CROSS_DRYRUN_ASSESSMENT_v0.1.md` | `tests/reviewer_runtime/assessments/REVIEWER_RUNTIME_CROSS_DRYRUN_ASSESSMENT_v0.1.md` | RUNTIME_TEST | LOOKUP_ONLY | Cross-project generalization assessment |

## Test Guardrail

```text
Dry-run Result
≠
Game Design Canonical Evidence
```

금지:

```text
Runtime fixture
→ Universal Core Promotion
```

Dry-run은 Runtime behavior를 검증한다.

---

# 16. Runtime Fixture vs Project GDD

Studio OS Runtime Test에는 저장 가능:

- tested Project name
- tested Project version
- expected routing
- expected Runtime behavior
- selected trace / summarized fixture

기본적으로 Project GDD 전체를 Studio OS Repository에 계속 복제하지 않는다.

권장 fixture trace:

```text
Project Repository:
Magic-Word-Deckbuilding

Project Version:
v0.9

Commit:
<git-sha>

Fixture:
REVIEWER_RUNTIME_DRYRUN_02_MAGIC_WORD_v0.1.md
```

Project GDD가 private / separate repo이면 version/commit pointer만 저장할 수 있다.

---

# 17. Historical Policy

Historical document는:

```text
Current Runtime Rule:
NO

Runtime Load:
NEVER
```

다.

Canonical conflict precedence:

```text
Current Canonical
>
Historical
```

History는:
- audit
- rationale
- supersession trace
- future maintenance

에만 사용한다.

---

# 18. Historical Runtime Registry

권장 위치:

`history/runtime/`

| File | Classification | Runtime Load | Reason |
|---|---|---|---|
| `REVIEWER_RUNTIME_SPECIFICATION_v0.1.md` | HISTORICAL | NEVER | Pre-approval runtime draft |
| `REVIEWER_RUNTIME_SPECIFICATION_v0.1_APPROVED.md` | HISTORICAL | NEVER | Superseded by v1.0 |
| `REVIEWER_RUNTIME_CORRECTION_NOTE_01_v0.1.md` | HISTORICAL | NEVER | Integrated into v1.0 |
| `REVIEWER_RUNTIME_DEFECT_LOG_01_v0.1.md` | HISTORICAL | NEVER | Dry-run defect trace |
| `REVIEWER_RUNTIME_DEFECT_LOG_02_v0.1.md` | HISTORICAL | NEVER | Dry-run defect trace |

Runtime v1.0은 standalone이다.

따라서 정상 Review에서 v0.1 / Correction Note를 다시 읽거나 재적용하면 안 된다.

---

# 19. Core Consolidation / Version History Registry

권장 위치:

`history/consolidation/`

| File | Classification | Runtime Load | Current Owner / Superseded By |
|---|---|---|---|
| `Studio_OS_Evidence_Based_Core_Extraction_v0.2.md` | HISTORICAL | NEVER | Universal v0.4 |
| `Studio_OS_Evidence_Based_Core_Extraction_v0.3.md` | HISTORICAL | NEVER | Universal v0.4 |
| `GENRE_CORE_MASTER_INDEX_v0.1.md` | HISTORICAL | NEVER | Genre Master v0.3 |
| `GENRE_CORE_MASTER_INDEX_v0.1_APPROVED.md` | HISTORICAL | NEVER | Genre Master v0.3 |
| `GENRE_CORE_MASTER_INDEX_v0.2.md` | HISTORICAL | NEVER | Genre Master v0.3 |
| `SCALE_CORE_BASELINE_v0.1.md` | HISTORICAL | NEVER | Scale v0.2 |
| `SCALE_CORE_BASELINE_v0.1_APPROVED.md` | HISTORICAL | NEVER | Scale v0.2 |
| `GENRE_SCALE_CORE_INTEGRATION_v0.1.md` | HISTORICAL | NEVER | Integration decision trace |
| `GENRE_SCALE_CORE_INTEGRATION_v0.1_APPROVED.md` | HISTORICAL | NEVER | Genre Master / Scale current mapping |
| `GSC_CANONICAL_CONSOLIDATION_v0.1.md` | HISTORICAL | NEVER | Current Active GSC state embedded in canonical docs |
| `UNIVERSAL_CORE_CONSOLIDATION_v0.1.md` | HISTORICAL | NEVER | Approved consolidation / Universal v0.4 |
| `UNIVERSAL_CORE_CONSOLIDATION_v0.1_APPROVED.md` | HISTORICAL | NEVER | Universal v0.4 |
| `UNIVERSAL_CANONICAL_SYNC_v0.1.md` | HISTORICAL | NEVER | Universal v0.4 / Genre Master v0.3 |

## Genre Draft History

다음 non-approved duplicate는 current approved-suffixed baseline과 구분해 Historical로 이동한다.

```text
STRATEGY_CORE_CANDIDATES_v0.1.md
SIMULATION_CORE_CANDIDATES_v0.1.md
RPG_CORE_CANDIDATES_v0.1.md
ACTION_CORE_CANDIDATES_v0.1.md
```

권장:

`history/consolidation/genre_drafts/`

Current runtime source는 각각 `_APPROVED.md` version이다.

---

# 20. Inactive Draft Registry

현재 `DRAFT_FOR_REVIEW` 상태이며 Reviewer Runtime v1.0의 실행 dependency가 아닌 문서는:

`HISTORICAL / INACTIVE_DRAFT`

로 격리한다.

권장 위치:

`history/drafts/`

## Legacy Operation Index

`00_Studio_OS_Index_v0.2_APPROVED.md`

Classification:
`HISTORICAL`

Reason:
- ChatGPT Project-based 운영 인덱스
- Canonical document/source-resolution 역할은 Manifest v1.0이 대체
- 필요 시 과거 workflow trace로 조회

Runtime Load:
`NEVER`

## Reviewer / Validation Draft Schemas

- `REVIEW_Reviewer_Finding_Schema_v0.1.md`
- `REVIEW_Validation_Handoff_Schema_v0.1.md`

## Validation Drafts

- `VALID_Hypothesis_Schema_v0.1.md`
- `VALID_Assumption_Schema_v0.1.md`
- `VALID_Metric_Schema_v0.1.md`
- `VALID_Criteria_Schema_v0.1.md`
- `VALID_TestPlan_Schema_v0.1.md`
- `VALID_Evidence_Schema_v0.1.md`
- `VALID_Validation_Package_Template_v0.1.md`

## AI Tester Drafts

- `Universal_AI_Tester_Architecture_v0.1.md`
- `TESTER_Universal_AI_Tester_Implementation_Spec_v0.1.md`

Classification:
`HISTORICAL`

Status Note:
`INACTIVE_DRAFT — not part of Reviewer Runtime v1.0 canonical package`

이 분류는 문서 내용이 영구 폐기되었다는 뜻이 아니다.

향후 별도 module로 승인될 경우 새 Canonical Logical ID / Manifest version을 통해 활성화해야 한다.

---

# 21. Deprecated Document Policy

두 방식 중 기본 권장:

## Recommended — Option A

> **Git history만 남기고 Working Tree에서 제거**

명시적으로 폐기된 전체 문서는 Repository 기본 context에서 제거하는 것이 가장 안전하다.

이유:
- AI accidental load 방지
- search noise 감소
- stale rule 오사용 방지

## Exception — Option B

audit / migration / compliance 이유로 꼭 보관해야 하면:

`history/deprecated/`

에 둔다.

반드시:
- Classification = DEPRECATED
- Runtime Load = NEVER
- Superseded By / Reason 기록

## v1.0 Current State

현재 Manifest migration에서 **명시적으로 DEPRECATED로 유지해야 할 필수 문서는 없음**.

과거 Version / draft는 `HISTORICAL`로 충분히 추적 가능하다.

---

# 22. Project GDD Separation

개별 Game Project GDD는 Studio OS Canonical Knowledge가 아니다.

예:

```text
Project MCC GDD
Magic Word GDD
Villain Inc. GDD
```

Classification:
`PROJECT_EXTERNAL`

각 Project Repository가 소유한다.

예:

```text
MCC/
└─ Docs/

Magic-Word-Deckbuilding/
└─ Docs/

Villain-Inc/
└─ Docs/
```

Project Review Result도 기본적으로 Project Repository에 저장한다.

Studio OS Repository에 복사하는 경우:

> Runtime Regression Fixture로 재사용 가치가 명확할 때만.

---

# 23. Project External Guardrail

```text
Project GDD
≠
Studio OS Canonical Knowledge
```

```text
Project Review Finding
≠
Game Design Core Promotion Evidence
```

Studio internal project result는:
- Runtime regression
- workflow improvement
- project-specific decision

에는 사용할 수 있지만 Core promotion evidence로 자동 사용하지 않는다.

---

# 24. Canonical Document Entry Schema

Manifest의 Canonical document는 다음 Schema를 따른다.

```text
DOCUMENT_ENTRY

ID:

File:

Path:

Classification:
- CANONICAL_ACTIVE
- CANONICAL_CONDITIONAL
- REFERENCE
- RUNTIME_TEST
- HISTORICAL
- DEPRECATED
- PROJECT_EXTERNAL

Layer:

Version:

Status:

Runtime Load:
- ALWAYS
- CONDITIONAL
- LOOKUP_ONLY
- NEVER

Context Mode:
- FULL
- SECTION_LOOKUP
- CONDITIONAL_SECTION_LOOKUP
- LOOKUP_ONLY
- NEVER

Load Condition:

Supersedes:

Superseded By:

Dependencies:

Used By:

Source of Truth:
GITHUB

Notes:
```

`Context Mode`는 Runtime Load와 실제 context injection 비용을 분리하기 위해 v1.0 Manifest에서 사용하는 repository-level metadata다.

Game Design Rule이 아니다.

---

# 25. Version Replacement Rule

새 Version 승인 시:

```text
New Version
APPROVED
↓
Manifest Update
↓
Old Version
HISTORICAL
↓
Merge to main
```

한다.

동일 Logical ID에서:

```text
Current Canonical Active Version:
1
```

만 허용한다.

예:

```text
DOC-RUNTIME-REVIEWER

Current:
REVIEWER_RUNTIME_SPECIFICATION_v1.0.md

Historical:
REVIEWER_RUNTIME_SPECIFICATION_v0.1_APPROVED.md
REVIEWER_RUNTIME_CORRECTION_NOTE_01_v0.1.md
```

---

# 26. Supersession Rule

Supersession에는 두 종류가 있다.

## Full Supersession

새 문서가 이전 문서의 Runtime role을 완전히 대체.

예:

```text
DOC-RUNTIME-REVIEWER

v1.0
supersedes
v0.1 Approved
+
Correction Note #01
```

## Role Supersession

문서 전체가 아니라 특정 역할만 대체.

예:

```text
DOC-MANIFEST

supersedes
00_Studio_OS_Index_v0.2_APPROVED.md

for:
Canonical source resolution / repository document registry
```

과거 Index의 역사적 workflow 설명까지 모두 삭제했다는 의미는 아니다.

---

# 27. Single Canonical Version Rule

같은 Logical ID에 여러 version이 Repository에 있어도:

```text
CANONICAL_ACTIVE / CONDITIONAL:
1
```

만 존재해야 한다.

예:

```text
GENRE_CORE_MASTER_INDEX_v0.2
→ HISTORICAL

GENRE_CORE_MASTER_INDEX_v0.3
→ CANONICAL_ACTIVE
```

AI는 filename similarity가 아니라 Manifest Classification을 따른다.

---

# 28. Filename / Naming Rule

권장 신규 filename:

```text
UPPER_SNAKE_CASE_VERSION.md
```

단 기존 Canonical filename을 일괄 rename하지 않는다.

기존 naming inconsistency는 Stable Logical ID가 흡수한다.

Rename은:
- 명확한 실익
- broken links 영향 평가
- Manifest / dependency update

가 있을 때만 수행한다.

---

# 29. README Contract

`README.md`는 상세 Rule 문서가 아니다.

최소 포함:

- Studio OS 목적
- 현재 Core Package version
- Repository structure
- Canonical Manifest path
- Reviewer Runtime path
- basic use flow

권장 흐름:

```text
Project GDD
↓
Studio OS Manifest
↓
Reviewer Runtime
↓
Universal / Genre Router / Scale
↓
Conditional Genre Baseline
↓
Evidence-based Review
```

실제 Canonical document list는 README가 아니라 Manifest가 소유한다.

---

# 30. AI Tool Source-of-Truth Rule

ChatGPT / Claude / Cursor / Coding Agent에 권장하는 기본 지시:

> Use the current files listed as `CANONICAL_ACTIVE` and routed `CANONICAL_CONDITIONAL` in `STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md` as the source of truth. Historical, deprecated, runtime-test, project-external, and conversation-memory content must not override current canonical documents.

Canonical precedence:

```text
Manifest-listed Current Canonical
>
Project-specific Current Source
>
Historical
>
AI Conversation Memory
```

단 Project Review에서는 게임 자체의 사실관계에 대해:

```text
Current Project GDD
>
Reviewer Inference
```

를 유지한다.

따라서 두 Source 역할은 다르다.

- Studio OS Rule truth → Studio OS Manifest
- Game Project fact truth → Current Project Repository/GDD

---

# 31. Core Update Workflow

새 Evidence가 들어오면:

```text
New Reference
↓
Reference Library
↓
Evidence Extraction
↓
Candidate Pattern
↓
Core Review
↓
Promotion / Merge / Reject
↓
Canonical Core Update
↓
Manifest Update
↓
Merge to main
```

Manifest update 없이 Canonical pointer를 교체하지 않는다.

---

# 32. Runtime Update Workflow

Reviewer Runtime 변경:

```text
Runtime Defect
↓
Correction / Proposal
↓
Regression Fixture
↓
Runtime Consolidation
↓
New Runtime Version
↓
Manifest Update
↓
Merge to main
```

Runtime Test는 Runtime Update evidence다.

Game Design Core Promotion evidence가 아니다.

---

# 33. Project Review Workflow

```text
Project Repository
↓
Current Approved GDD
↓
Studio OS Canonical Manifest
↓
Reviewer Runtime
↓
Universal / Genre / Scale Routing
↓
Conditional Canonical Load
↓
Project Review Result
↓
Project Repository
```

Studio OS Repository에 Review Result를 기본 저장하지 않는다.

---

# 34. Canonical Minimum Set

## A. Reviewer Runtime Minimum Set

Logical dependency:

```text
DOC-MANIFEST
DOC-RUNTIME-REVIEWER
DOC-CORE-UNIVERSAL
DOC-GENRE-MASTER
DOC-SCALE-BASELINE
+
Routed Genre Baselines
```

## B. Context-efficient Default

```text
FULL:
Manifest
Reviewer Runtime

SECTION LOOKUP:
Universal
Genre Master
Scale

CONDITIONAL LOOKUP:
Routed Genre Baselines

LOOKUP ONLY:
Reference / Runtime Test

NEVER:
Historical / Deprecated
```

## C. Knowledge Maintenance Extended Set

```text
Canonical Minimum Set
+
REF Master Index
+
Relevant References
+
Relevant Historical Decision Trace
```

---

# 35. Current Canonical Source Map

```text
STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0
│
├─ DOC-RUNTIME-REVIEWER
│  └─ REVIEWER_RUNTIME_SPECIFICATION_v1.0
│
├─ DOC-CORE-UNIVERSAL
│  └─ Studio_OS_Evidence_Based_Core_Extraction_v0.4
│
├─ DOC-GENRE-MASTER
│  ├─ GENRE_CORE_MASTER_INDEX_v0.3
│  └─ Routed Genre Baselines
│
└─ DOC-SCALE-BASELINE
   └─ SCALE_CORE_BASELINE_v0.2
```

Evidence trace:

```text
Canonical Rule
↓
Reference Master Index
↓
Relevant Reference
```

Regression trace:

```text
Reviewer Runtime
↓
Runtime Fixture
↓
Cross Assessment
```

---

# 36. Migration Map — Current Working Files

현재 working set을 GitHub 구조로 옮길 때의 권장 분류다.

## CANONICAL_ACTIVE

```text
STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md
→ manifest/

Studio_OS_Evidence_Based_Core_Extraction_v0.4.md
→ core/universal/

GENRE_CORE_MASTER_INDEX_v0.3.md
→ core/genre/

SCALE_CORE_BASELINE_v0.2.md
→ core/scale/

REVIEWER_RUNTIME_SPECIFICATION_v1.0.md
→ core/runtime/
```

## CANONICAL_CONDITIONAL

```text
DECKBUILDING_CORE_CANDIDATES_v0.1.md
→ core/genre/baselines/Deckbuilding/

MANAGEMENT_CORE_CANDIDATES_v0.1.md
→ core/genre/baselines/Management/

ROGUELIKE_CORE_CANDIDATES_v0.1.md
→ core/genre/baselines/Roguelike/

DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1.md
→ core/genre/baselines/Deduction/

NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1.md
→ core/genre/baselines/Narrative/

STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md
→ core/genre/baselines/Strategy/

SIMULATION_CORE_CANDIDATES_v0.1_APPROVED.md
→ core/genre/baselines/Simulation/

RPG_CORE_CANDIDATES_v0.1_APPROVED.md
→ core/genre/baselines/RPG/

ACTION_CORE_CANDIDATES_v0.1_APPROVED.md
→ core/genre/baselines/Action/
```

## REFERENCE

```text
REF_Reference_Master_Index.md
→ references/

REF_Layer_1_Core_Design.md
REF_Layer_2_Specialized.md
→ references/research/

REF_Layer_3_Solo_Micro_Production.md
→ references/production/

REF_Layer_4_Commercial.md
REF_Layer_5_Korean_Selection.md
REF_2024_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md
REF_2025_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md
REF_2026_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md
→ references/market/

REF_Game_Design_Case_Study_Template_v1.0.md
REF_Game_Design_Reviewer_Final_Evaluation_Template_v2.0.md
REF_Game_Design_Reviewer_Project_Instructions_v2.0.md
→ references/methodology/
```

## RUNTIME_TEST

```text
REVIEWER_RUNTIME_DRYRUN_01_PROJECT_MCC_v0.1.md
→ tests/reviewer_runtime/fixtures/MCC/

REVIEWER_RUNTIME_DRYRUN_02_MAGIC_WORD_v0.1.md
→ tests/reviewer_runtime/fixtures/MagicWord/

REVIEWER_RUNTIME_CROSS_DRYRUN_ASSESSMENT_v0.1.md
→ tests/reviewer_runtime/assessments/
```

## HISTORICAL — runtime

```text
REVIEWER_RUNTIME_SPECIFICATION_v0.1.md
REVIEWER_RUNTIME_SPECIFICATION_v0.1_APPROVED.md
REVIEWER_RUNTIME_CORRECTION_NOTE_01_v0.1.md
REVIEWER_RUNTIME_DEFECT_LOG_01_v0.1.md
REVIEWER_RUNTIME_DEFECT_LOG_02_v0.1.md
→ history/runtime/
```

## HISTORICAL — consolidation / previous versions

```text
Studio_OS_Evidence_Based_Core_Extraction_v0.2.md
Studio_OS_Evidence_Based_Core_Extraction_v0.3.md

GENRE_CORE_MASTER_INDEX_v0.1.md
GENRE_CORE_MASTER_INDEX_v0.1_APPROVED.md
GENRE_CORE_MASTER_INDEX_v0.2.md

SCALE_CORE_BASELINE_v0.1.md
SCALE_CORE_BASELINE_v0.1_APPROVED.md

GENRE_SCALE_CORE_INTEGRATION_v0.1.md
GENRE_SCALE_CORE_INTEGRATION_v0.1_APPROVED.md
GSC_CANONICAL_CONSOLIDATION_v0.1.md

UNIVERSAL_CORE_CONSOLIDATION_v0.1.md
UNIVERSAL_CORE_CONSOLIDATION_v0.1_APPROVED.md
UNIVERSAL_CANONICAL_SYNC_v0.1.md

STRATEGY_CORE_CANDIDATES_v0.1.md
SIMULATION_CORE_CANDIDATES_v0.1.md
RPG_CORE_CANDIDATES_v0.1.md
ACTION_CORE_CANDIDATES_v0.1.md
→ history/consolidation/
```

## HISTORICAL — inactive drafts

```text
00_Studio_OS_Index_v0.2_APPROVED.md

REVIEW_Reviewer_Finding_Schema_v0.1.md
REVIEW_Validation_Handoff_Schema_v0.1.md

VALID_Hypothesis_Schema_v0.1.md
VALID_Assumption_Schema_v0.1.md
VALID_Metric_Schema_v0.1.md
VALID_Criteria_Schema_v0.1.md
VALID_TestPlan_Schema_v0.1.md
VALID_Evidence_Schema_v0.1.md
VALID_Validation_Package_Template_v0.1.md

Universal_AI_Tester_Architecture_v0.1.md
TESTER_Universal_AI_Tester_Implementation_Spec_v0.1.md
→ history/drafts/
```

---

# 37. Manifest Versioning

Logical ID:

`DOC-MANIFEST`

Current:

`STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md`

새 Canonical pointer가 바뀌면 Manifest를 업데이트한다.

예:

```text
Runtime v1.0
→ Runtime v1.1
```

이면:

```text
Manifest v1.0
→ Manifest v1.1
```

같이 Minor version update 가능.

Studio OS Core 하나의 version이 올라갈 때마다 Manifest Major version을 올릴 필요는 없다.

Manifest Major는 Repository architecture / classification / source-of-truth model이 materially 바뀔 때 사용한다.

---

# 38. Manifest Validation

## A. Canonical Active duplicate version?

`NO`

Logical ID별 current version 1개.

## B. Runtime v1.0 canonical?

`YES`

`DOC-RUNTIME-REVIEWER`.

## C. Runtime v0.1 historical?

`YES`

## D. Correction Note historical?

`YES`

v1.0에 통합됨.

## E. Dry-run이 Canonical Core인가?

`NO`

`RUNTIME_TEST`.

## F. Genre Baseline conditional?

`YES`

9개 모두.

## G. Reference Library full default load?

`NO`

`LOOKUP_ONLY`.

## H. Project GDD가 Core Repository에 섞였는가?

`NO`

`PROJECT_EXTERNAL`.

## I. Deprecated / stale document Runtime source 가능성?

`NO`

Historical / Deprecated = `NEVER`.

## J. Canonical document Logical ID / Path 존재?

`YES`

---

# 39. AI Operating Instruction

Studio OS를 AI Tool에서 사용할 때 권장 instruction:

> Use `STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md` to resolve the current Studio OS source of truth. Use `REVIEWER_RUNTIME_SPECIFICATION_v1.0.md` as the execution baseline. Load Universal, Genre Master, Scale, and routed Genre Baselines according to the Manifest and Runtime. Historical, deprecated, runtime-test, draft, project-external, and conversation-memory content must not override current canonical documents.

## Conflict Rule

Studio OS rule conflict:

```text
Manifest Current Canonical
>
Historical
>
Conversation Memory
```

Project fact conflict:

```text
Current Approved Project GDD
>
Older Project GDD
>
Reviewer Inference
```

---

# 40. README Recommended Minimum

README는 다음 정도로 제한한다.

```text
# Studio OS

Purpose:
Evidence-based independent game design review system.

Current Package:
Studio OS Core Package v1.0

Canonical Manifest:
manifest/STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md

Reviewer Runtime:
core/runtime/REVIEWER_RUNTIME_SPECIFICATION_v1.0.md

Basic Flow:
Project GDD
→ Manifest
→ Reviewer Runtime
→ Dynamic Canonical Load
→ Review
```

README에 Canonical Registry 전체를 복제하지 않는다.

---

# 41. Final Position

## A. Studio OS Canonical Active 문서는 무엇인가?

```text
1. STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md
2. REVIEWER_RUNTIME_SPECIFICATION_v1.0.md
3. Studio_OS_Evidence_Based_Core_Extraction_v0.4.md
4. GENRE_CORE_MASTER_INDEX_v0.3.md
5. SCALE_CORE_BASELINE_v0.2.md
```

---

## B. Conditional Canonical 문서는 무엇인가?

9개 Genre Baseline:

```text
DECKBUILDING_CORE_CANDIDATES_v0.1.md
MANAGEMENT_CORE_CANDIDATES_v0.1.md
ROGUELIKE_CORE_CANDIDATES_v0.1.md
DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1.md
NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1.md
STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md
SIMULATION_CORE_CANDIDATES_v0.1_APPROVED.md
RPG_CORE_CANDIDATES_v0.1_APPROVED.md
ACTION_CORE_CANDIDATES_v0.1_APPROVED.md
```

---

## C. Reference 문서는 어디에 있는가?

```text
references/
```

Reference routing owner:

`REF_Reference_Master_Index.md`

---

## D. Runtime Test는 어디에 있는가?

```text
tests/reviewer_runtime/
```

- fixtures/MCC
- fixtures/MagicWord
- assessments

---

## E. Historical 문서는 어디에 있는가?

```text
history/
├─ runtime/
├─ consolidation/
└─ drafts/
```

명시적 deprecated audit copy가 필요한 경우에만:

`history/deprecated/`.

---

## F. Project GDD는 어디에 저장하는가?

각 Game Project Repository.

예:

```text
MCC/Docs/
Magic-Word-Deckbuilding/Docs/
Villain-Inc/Docs/
```

Studio OS Core Repository의 Canonical Knowledge로 저장하지 않는다.

---

## G. Reviewer 실행 시 최소 Load Set은?

Logical Set:

```text
Manifest
Reviewer Runtime v1.0
Universal v0.4
Genre Master v0.3
Scale v0.2
+
Routed Genre Baselines
```

Context-efficient access:

```text
Full:
Manifest + Runtime

Lookup:
Universal + Genre Master + Scale

Conditional:
Routed Genre Baselines
```

---

## H. Genre Baseline은 언제 읽는가?

`PROJECT_GENRE_ROUTING_PROFILE` 이후.

```text
L0
→ Read 금지

L1/L2/L3
→ Runtime Loading Weight에 따라 조회
```

---

## I. Reference Library는 언제 읽는가?

기본 Review에서는 자동 full-load하지 않는다.

다음일 때 lookup:

- deeper evidence trace
- Boundary 확인
- 새로운 Evidence extraction
- Core maintenance / reconsideration

---

## J. Dry-run 결과는 Canonical Knowledge인가?

`NO`

`RUNTIME_TEST`.

---

## K. Runtime v0.1 / Correction Note는 현재 실행 시 필요한가?

`NO`

둘 다:

`HISTORICAL / NEVER`.

---

## L. 현재 Canonical Reviewer Runtime은?

`REVIEWER_RUNTIME_SPECIFICATION_v1.0.md`

---

## M. GitHub가 Source of Truth인가?

`YES`

정확히는:

> GitHub `main`의 Current Approved Manifest가 가리키는 document set.

---

## N. AI Conversation Memory가 Canonical인가?

`NO`

---

## O. 다음 단계는?

```text
Studio OS Canonical Document Manifest v1.0
✅
↓
Studio OS Core Package v1.0
```

---

# 42. Final Repository Snapshot

```text
Studio-OS/
│
├─ README.md
│
├─ manifest/
│  └─ STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md
│
├─ core/
│  ├─ universal/
│  │  └─ Studio_OS_Evidence_Based_Core_Extraction_v0.4.md
│  ├─ genre/
│  │  ├─ GENRE_CORE_MASTER_INDEX_v0.3.md
│  │  └─ baselines/
│  │     ├─ Deckbuilding/
│  │     ├─ Management/
│  │     ├─ Roguelike/
│  │     ├─ Deduction/
│  │     ├─ Narrative/
│  │     ├─ Strategy/
│  │     ├─ Simulation/
│  │     ├─ RPG/
│  │     └─ Action/
│  ├─ scale/
│  │  └─ SCALE_CORE_BASELINE_v0.2.md
│  └─ runtime/
│     └─ REVIEWER_RUNTIME_SPECIFICATION_v1.0.md
│
├─ references/
│  ├─ REF_Reference_Master_Index.md
│  ├─ games/
│  ├─ market/
│  ├─ production/
│  ├─ research/
│  └─ methodology/
│
├─ tests/
│  └─ reviewer_runtime/
│     ├─ fixtures/
│     │  ├─ MCC/
│     │  └─ MagicWord/
│     └─ assessments/
│
└─ history/
   ├─ runtime/
   ├─ consolidation/
   ├─ drafts/
   └─ deprecated/
```

이 Repository에서:

```text
무엇이 현재 기준인가?
→ Manifest

무엇을 읽어야 하는가?
→ Load Policy

무엇은 조건부인가?
→ Genre Routing + Conditional Registry

무엇은 읽으면 안 되는가?
→ Historical / Deprecated = NEVER

왜 과거 파일이 남아 있는가?
→ audit / decision trace

Project GDD는 어디에 있는가?
→ Project Repository
```

를 Manifest 하나로 판단할 수 있다.
