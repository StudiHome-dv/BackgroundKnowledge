# STUDIO_OS_CORE_PACKAGE_v1.0

**Status:** `APPROVED_AS_STUDIO_OS_CORE_PACKAGE_V1`  
**Package Version:** `v1.0`  
**Deployment Readiness:** `PACKAGE_READY_WITH_MIGRATION_FIX`  
**Canonical Manifest:** `STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md`  
**Reviewer Runtime:** `REVIEWER_RUNTIME_SPECIFICATION_v1.0.md`  
**Source of Truth:** `GitHub main`  
**Package Type:** `Evidence-based Design Reviewer Core`  
**Recommended Tag After Migration Fix:** `studio-os-v1.0`

---

# 1. Release Summary

Studio OS Core Package v1.0은 새로운 Game Design Knowledge를 추가하는 문서가 아니다.

다음 승인 자산을 GitHub Repository에서 운용하기 위한 Release Baseline이다.

```text
Canonical Manifest
+
Canonical Core
+
Reviewer Runtime
+
Conditional Genre Baselines
+
Repository README
+
AI Operating Instructions
+
Reference Index
+
Runtime Regression Fixtures
+
Historical Separation
+
Migration Checklist
```

이번 Assembly에서 변경하지 않은 것:

```text
Universal Core Status
Genre Core Status
Scale Core Status
Confidence
Genre Routing Score
PASS 0~15
GSC State
Validation Boundary
```

현재 필수 Canonical 파일과 9개 Genre Baseline은 실제 working set에서 모두 존재함을 확인했다.

```text
Required Canonical / Conditional Files Missing:
0
```

다만 Git tag 전 **4건의 stale metadata sync**가 필요하다.

따라서:

`PACKAGE_READY_WITH_MIGRATION_FIX`

로 판정한다.

---

# 2. Package Entry Point

Studio OS 실제 사용 시작점:

```text
Current Project GDD
↓
Canonical Manifest
↓
Reviewer Runtime
```

Repository entry:

1. `README.md`
2. `manifest/STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md`
3. `core/runtime/REVIEWER_RUNTIME_SPECIFICATION_v1.0.md`

Runtime이 이후:
- Universal
- Genre Master
- Scale
- Routed Genre Baseline

을 동적으로 조회한다.

---

# 3. Canonical Active Set

## DOC-MANIFEST

```text
File:
STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md

Path:
manifest/STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md

Version:
v1.0

Classification:
CANONICAL_ACTIVE

Runtime Load:
ALWAYS

Verified:
YES
```

## DOC-RUNTIME-REVIEWER

```text
File:
REVIEWER_RUNTIME_SPECIFICATION_v1.0.md

Path:
core/runtime/REVIEWER_RUNTIME_SPECIFICATION_v1.0.md

Version:
v1.0

Status:
APPROVED_AS_REVIEWER_RUNTIME_V1_BASELINE

Classification:
CANONICAL_ACTIVE

Runtime Load:
ALWAYS

Verified:
YES
```

## DOC-CORE-UNIVERSAL

```text
File:
Studio_OS_Evidence_Based_Core_Extraction_v0.4.md

Path:
core/universal/Studio_OS_Evidence_Based_Core_Extraction_v0.4.md

Version:
v0.4

Classification:
CANONICAL_ACTIVE

Runtime Load:
ALWAYS / SECTION_LOOKUP

Verified:
YES
```

## DOC-GENRE-MASTER

```text
File:
GENRE_CORE_MASTER_INDEX_v0.3.md

Path:
core/genre/GENRE_CORE_MASTER_INDEX_v0.3.md

Version:
v0.3

Classification:
CANONICAL_ACTIVE

Runtime Load:
ALWAYS / SECTION_LOOKUP

Verified:
YES

Migration Note:
Lifecycle metadata의 `Next / Pending` 문구가 Runtime v1.0 이전 상태를 가리킴.
Rule / Routing content 변경 없이 metadata sync 필요.
```

## DOC-SCALE-BASELINE

```text
File:
SCALE_CORE_BASELINE_v0.2.md

Path:
core/scale/SCALE_CORE_BASELINE_v0.2.md

Version:
v0.2

Status:
APPROVED_AS_SCALE_ROUTING_BASELINE

Classification:
CANONICAL_ACTIVE

Runtime Load:
ALWAYS / SECTION_LOOKUP

Verified:
YES

Migration Note:
Header에 Studio Core v0.3 / Genre Master v0.2 / Universal Consolidation Next가 남아 있음.
Scale Core Rule은 변경하지 않고 current pointer metadata만 sync 필요.
```

## Active Count

```text
CANONICAL_ACTIVE:
5
```

---

# 4. Conditional Genre Set

설치되어 있지만 항상 로드하지 않는다.

```text
Installed
≠
Always Loaded
```

| Logical ID | File | Version | Classification | Runtime Load | Actual File Verified |
|---|---|---:|---|---|---|
| DOC-GENRE-DECK | `DECKBUILDING_CORE_CANDIDATES_v0.1.md` | v0.1 | CANONICAL_CONDITIONAL | CONDITIONAL | YES |
| DOC-GENRE-MGMT | `MANAGEMENT_CORE_CANDIDATES_v0.1.md` | v0.1 | CANONICAL_CONDITIONAL | CONDITIONAL | YES |
| DOC-GENRE-ROGUE | `ROGUELIKE_CORE_CANDIDATES_v0.1.md` | v0.1 | CANONICAL_CONDITIONAL | CONDITIONAL | YES |
| DOC-GENRE-DEDUCT | `DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1.md` | v0.1 | CANONICAL_CONDITIONAL | CONDITIONAL | YES |
| DOC-GENRE-NARR | `NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1.md` | v0.1 | CANONICAL_CONDITIONAL | CONDITIONAL | YES |
| DOC-GENRE-STRAT | `STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md` | v0.1 | CANONICAL_CONDITIONAL | CONDITIONAL | YES |
| DOC-GENRE-SIM | `SIMULATION_CORE_CANDIDATES_v0.1_APPROVED.md` | v0.1 | CANONICAL_CONDITIONAL | CONDITIONAL | YES |
| DOC-GENRE-RPG | `RPG_CORE_CANDIDATES_v0.1_APPROVED.md` | v0.1 | CANONICAL_CONDITIONAL | CONDITIONAL | YES |
| DOC-GENRE-ACTION | `ACTION_CORE_CANDIDATES_v0.1_APPROVED.md` | v0.1 | CANONICAL_CONDITIONAL | CONDITIONAL | YES |

## Conditional Count

`9`

## Pre-tag Metadata Sync Notes

### RPG Baseline

현재 승인 파일 내부에 이전 UC006 title:

`Progression Should Alter Decisions`

가 historical canonical wording처럼 남아 있다.

현재 Canonical title:

`Progression Should Match Its Intended Promise`

으로 **cross-reference metadata만** sync해야 한다.

RPG Candidate status는 변경하지 않는다.

### Action Baseline

현재 승인 파일에:

`Universal Reclassification Candidate: GC-ACTION-003 → Failure Attribution`

이 남아 있다.

현재 Canonical mapping은 Genre Master v0.3 기준:

```text
GC-ACTION-003
→ UC005 Outcome-time Specialization
+ Cross-Genre Failure Attribution Pattern
```

이다.

Action Core status는 변경하지 않고 mapping metadata만 sync해야 한다.

---

# 5. Runtime Load Policy

## Logical Minimum

```text
Manifest
Reviewer Runtime v1.0
Universal v0.4
Genre Master v0.3
Scale v0.2
+
Routed Genre Baselines
```

## Context-efficient Access

```text
FULL:
Manifest
Reviewer Runtime

SECTION_LOOKUP:
Universal
Genre Master
Scale

CONDITIONAL_SECTION_LOOKUP:
Routed Genre Baselines

LOOKUP_ONLY:
References
Runtime Tests

NEVER:
Historical
Deprecated
```

9개 Genre Baseline을 매 Review마다 전부 넣지 않는다.

---

# 6. Reference Layer

Reference는 Canonical Rule이 아니다.

```text
Reference Observation
≠
Runtime Rule
```

기본 path:

```text
references/
├─ REF_Reference_Master_Index.md
├─ games/
├─ market/
├─ production/
├─ research/
└─ methodology/
```

Current Reference Master Index:

`REF_Reference_Master_Index.md`

Runtime Load:

`LOOKUP_ONLY`

사용:
- deeper evidence trace
- Core boundary 확인
- new Evidence extraction
- future Core maintenance

기본 Project Review에서 Reference Library 전체를 읽지 않는다.

---

# 7. Runtime Test Layer

Regression Fixture:

```text
MCC
→ tests/reviewer_runtime/fixtures/MCC/

Magic Word
→ tests/reviewer_runtime/fixtures/MagicWord/
```

Cross Assessment:

```text
tests/reviewer_runtime/assessments/
```

Current files:

- `REVIEWER_RUNTIME_DRYRUN_01_PROJECT_MCC_v0.1.md`
- `REVIEWER_RUNTIME_DRYRUN_02_MAGIC_WORD_v0.1.md`
- `REVIEWER_RUNTIME_CROSS_DRYRUN_ASSESSMENT_v0.1.md`

모두 actual file existence 확인됨.

```text
Runtime Test
≠
Game Design Canonical Evidence
```

---

# 8. Historical Layer

정상 Runtime Load:

`NEVER`

기본 구조:

```text
history/
├─ runtime/
├─ consolidation/
├─ drafts/
└─ deprecated/
```

예:

```text
Runtime v0.1
Correction Note
Defect Logs
Previous Universal / Genre / Scale versions
Consolidation decisions
Inactive Validation / AI Tester drafts
```

Runtime v1.0은 standalone이다.

과거 Runtime / Correction Note를 정상 Review에서 재적용하지 않는다.

---

# 9. Project Separation

개별 게임 GDD는:

`PROJECT_EXTERNAL`

이다.

기본:

```text
Studio-OS repo에 전체 GDD 저장:
NO
```

각 Project Repository가 소유한다.

예:

```text
MCC/Docs/
Magic-Word-Deckbuilding/Docs/
Villain-Inc/Docs/
```

Runtime Fixture는:
- Project name
- version
- expected routing
- commit pointer
- selected review result

만 보존할 수 있다.

---

# 10. AI Source-of-Truth Policy

Studio OS Rule:

```text
Current Manifest
↓
Current Canonical Document
↓
Historical Trace
↓
Conversation Memory
```

Project Fact:

```text
Current Approved Project GDD
↓
Locked Current Decision
↓
Older Project Source
↓
Reviewer Inference
```

두 계층을 혼합하지 않는다.

---

# 11. Known Runtime Evidence Boundary

직접 Dry-run coverage:

```text
MCC:
Management
Strategy
Simulation
SOLO
Prototype Slice

Magic Word:
Deckbuilding
Roguelike
Strategy
RPG-supporting
UNRESOLVED SCALE
Full Project
```

직접 충분히 시험하지 않은 Runtime Branch:

- MICRO
- SMALL
- MID+
- Deduction Primary
- Narrative Primary
- Action Primary
- explicit Market Routing
- explicit Selection Routing
- post-validation Finding lifecycle
- regression lifecycle

의미:

```text
Not Dry-run Tested
≠
Broken
```

정확한 의미:

```text
Canonical Rule exists
+
Direct Runtime regression coverage is limited
```

---

# 12. Package Freeze Rule

v1.0 tag 이후 임의 확장을 중단한다.

변경 Trigger:

1. Runtime Defect
2. New Evidence에 의한 Core Review
3. Canonical Rule Conflict
4. 반복되는 Missing Runtime Branch
5. Repository operation problem

금지:

> 좋아 보이니까 기능 하나 더 추가.

---

# 13. Package Exclusions

v1.0에 포함하지 않는다.

```text
Validation Planner
AI Tester Persona Specification
Human Test Planner
Market Test Planner
Automated Repository Agent
Implementation Generator
```

향후 optional module 가능.

Reviewer Runtime은 Validation Need와 Suggested Evidence Type까지만 출력한다.

---

# 14. Package Freeze / Update Rule

## Core Update

```text
Reference
→ Evidence
→ Candidate
→ Review
→ Canonical Core update
→ Manifest update
```

## Runtime Update

```text
Runtime Defect
→ Correction / Proposal
→ Regression Fixture
→ New Runtime Version
→ Manifest update
```

Manifest를 건너뛰고 Canonical pointer를 교체하지 않는다.

---

# 15. Source Integrity Check

## Required Active / Conditional Files

```text
Canonical Active:
5 / 5 actual files verified

Genre Conditional:
9 / 9 actual files verified

Reference Master Index:
verified

Runtime Fixtures:
3 / 3 verified
```

## File Missing

`0`

## Filename Mismatch

`0` for current Manifest required Active / Conditional Set.

## Metadata Consistency Fix Required

`4`

1. Genre Master v0.3 lifecycle metadata
2. Scale v0.2 Canonical pointer / Next metadata
3. RPG baseline old UC006 title cross-reference
4. Action baseline old Failure Attribution mapping cross-reference

이 4건은:

```text
Rule Change:
NO

Core Status Change:
NO

Confidence Change:
NO
```

인 release metadata sync다.

---

# 16. Package Readiness Verdict

`PACKAGE_READY_WITH_MIGRATION_FIX`

## Why Not PACKAGE_READY Yet?

필수 파일은 모두 존재하고 Canonical ownership conflict도 없다.

하지만 release tag 전에 Current Canonical 문서 내부의 stale cross-reference metadata 4건을 sync해야 Repository 자체가 self-consistent해진다.

## Blocking Knowledge Issue

`NONE`

## Blocking Runtime Issue

`NONE`

## Blocking File Missing

`NONE`

## Required Before Tag

`Metadata sync 4건`

---

# 17. Release Recommendation

Metadata sync 완료 후:

```text
GitHub Repository Migration
↓
Package Health Check
↓
git tag studio-os-v1.0
↓
Optional GitHub Release
↓
Actual Project Review Operation
```

권장 Git tag:

`studio-os-v1.0`

---

# 18. Suggested GitHub Release Note

```text
Studio OS Core Package v1.0

- Initial canonical repository package
- Reviewer Runtime v1.0
- Universal Core v0.4
- Genre Master v0.3
- Scale Baseline v0.2
- 9 Conditional Genre Baselines
- MCC / Magic Word Runtime Regression Fixtures
- Canonical Manifest v1.0
- Known runtime evidence boundaries documented
```

---

# 19. Final Position

## A. Entry Point

```text
README
→ Canonical Manifest
→ Reviewer Runtime
```

## B. Canonical Active 5

1. Manifest v1.0
2. Reviewer Runtime v1.0
3. Universal v0.4
4. Genre Master v0.3
5. Scale Baseline v0.2

## C. Conditional Genre Baseline

`9`

## D. Project Review에서 Reference Library를 전부 읽는가?

`NO`

## E. Historical 문서를 Runtime이 읽는가?

`NO`

## F. Project GDD를 Studio OS Repository에 저장하는가?

기본:

`NO`

## G. AI Source of Truth

Studio OS Rule:
`Current Manifest + Current Canonical GitHub files`

Project Fact:
`Current Approved Project GDD`

## H. Runtime Fixture 역할

Reviewer Runtime Regression Evidence.

Game Design Core evidence가 아니다.

## I. Validation Planner 포함?

`NO`

## J. Known Runtime Evidence Boundary

MICRO / SMALL / MID+, Deduction/Narrative/Action Primary, Market/Selection, lifecycle branches 등 direct regression coverage가 제한적.

## K. Actual File / Manifest mismatch 처리

1. Actual latest approved file 확인
2. Logical Canonical identity 확인
3. Manifest filename/path 수정
4. 필요 시 stale metadata sync
5. Rule 내용은 Assembly 단계에서 임의 변경하지 않음

## L. GitHub 배치 준비?

`YES — WITH MIGRATION FIX`

Verdict:

`PACKAGE_READY_WITH_MIGRATION_FIX`

## M. Git Tag

`studio-os-v1.0`

## N. Next

```text
Metadata Migration Fix
↓
GitHub Repository Migration
↓
Core Package v1.0 Tag
↓
Actual Project Review Operation
```
