# STUDIO_OS_REPOSITORY_MIGRATION_CHECKLIST_v1.0

**Package:** `Studio OS Core Package v1.0`  
**Manifest:** `STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md`  
**Current Readiness:** `PACKAGE_READY_WITH_MIGRATION_FIX`  
**Required Knowledge Change:** `NO`  
**Required Runtime Architecture Change:** `NO`

---

# 1. Pre-Migration Source Integrity

현재 working set에서 확인된 상태:

```text
Canonical Active files:
5 / 5 VERIFIED

Conditional Genre Baselines:
9 / 9 VERIFIED

Reference Master Index:
VERIFIED

Runtime Regression Fixtures:
3 / 3 VERIFIED

Required File Missing:
0

Canonical filename mismatch:
0
```

## Pre-tag Metadata Fix Required

```text
4
```

아래 Phase 0을 완료한 뒤 Git tag를 생성한다.

---

# 2. Phase 0 — Canonical Metadata Sync Before Tag

## FIX-01 — Genre Master lifecycle metadata

File:

`GENRE_CORE_MASTER_INDEX_v0.3.md`

현재 stale:

```text
Next:
Reviewer Runtime Specification

Pending:
... Reviewer Runtime ...
```

현재 Canonical 상태:

```text
Reviewer Runtime v1.0:
COMPLETE

Canonical Manifest v1.0:
COMPLETE

Next:
Studio OS Core Package v1.0 / Repository Migration
```

Action:

```text
[ ] Rule / Router content를 변경하지 않고 lifecycle metadata만 sync
[ ] version v0.3 유지 여부 확인 — semantic rule change가 아니므로 same-version metadata fix 권장
[ ] Manifest logical ID 유지
```

---

## FIX-02 — Scale Baseline current pointers

File:

`SCALE_CORE_BASELINE_v0.2.md`

현재 stale header:

```text
Canonical Starting Point:
Studio Core v0.3

Genre Router:
Genre Master v0.2

Next:
Universal Core Consolidation
```

현재 pointer:

```text
Studio Core:
v0.4

Genre Master:
v0.3

Universal Consolidation:
COMPLETE

Reviewer Runtime:
v1.0
```

Action:

```text
[ ] Scale Rule / Status / Confidence는 변경하지 않음
[ ] source pointer / lifecycle metadata만 sync
[ ] v0.2 semantic baseline 유지
```

---

## FIX-03 — RPG UC006 title cross-reference

File:

`RPG_CORE_CANDIDATES_v0.1_APPROVED.md`

현재 일부 metadata / prose cross-reference:

`UC-DESIGN-006 — Progression Should Alter Decisions`

현재 Canonical title:

`UC-DESIGN-006 — Progression Should Match Its Intended Promise`

Action:

```text
[ ] UC006 title cross-reference sync
[ ] RPG Candidate status 변경 금지
[ ] RPG Evidence Boundary 변경 금지
[ ] Universal status 변경 금지
```

---

## FIX-04 — Action Failure Attribution mapping cross-reference

File:

`ACTION_CORE_CANDIDATES_v0.1_APPROVED.md`

현재 header:

```text
Universal Reclassification Candidate:
GC-ACTION-003 → Failure Attribution
```

현재 Canonical mapping:

```text
GC-ACTION-003
→ UC-DESIGN-005 Outcome-time Specialization
+ Failure Attribution Cross-Genre Pattern
```

Action:

```text
[ ] mapping metadata sync
[ ] GC-ACTION-003 Genre Candidate status 유지
[ ] Action Evidence Boundary 유지
[ ] 신규 Universal Core 생성 금지
```

---

# 3. Phase A — Repository Bootstrap

```text
[ ] GitHub repository `Studio-OS` 생성
[ ] `main` branch 확인
[ ] default branch protection 여부 결정
[ ] README.md 추가
[ ] STUDIO_OS_CORE_PACKAGE_v1.0.md 추가
[ ] AI_OPERATING_INSTRUCTIONS.md 추가
[ ] manifest/ 생성
[ ] core/ 생성
[ ] references/ 생성
[ ] tests/ 생성
[ ] history/ 생성
```

---

# 4. Phase B — Canonical Active Migration

## DOC-MANIFEST

```text
[ ] Source file 존재
[ ] Filename = STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md
[ ] Destination = manifest/
[ ] Version = v1.0
[ ] Status = APPROVED_AS_STUDIO_OS_CANONICAL_MANIFEST_V1
```

## DOC-RUNTIME-REVIEWER

```text
[ ] Source file 존재
[ ] Filename = REVIEWER_RUNTIME_SPECIFICATION_v1.0.md
[ ] Destination = core/runtime/
[ ] Version = v1.0
[ ] Status = APPROVED_AS_REVIEWER_RUNTIME_V1_BASELINE
[ ] PASS 0~15 확인
[ ] RD-001~004 integrated 확인
```

## DOC-CORE-UNIVERSAL

```text
[ ] Source file 존재
[ ] Filename = Studio_OS_Evidence_Based_Core_Extraction_v0.4.md
[ ] Destination = core/universal/
[ ] Version = v0.4
[ ] UC001~005 Provisional 유지
[ ] UC006 Candidate 유지
[ ] Active Independent GSC = 0
```

## DOC-GENRE-MASTER

```text
[ ] Source file 존재
[ ] Filename = GENRE_CORE_MASTER_INDEX_v0.3.md
[ ] Destination = core/genre/
[ ] Version = v0.3
[ ] Phase 0 lifecycle metadata fix 완료
[ ] 9 Approved Genre Baselines pointer 확인
```

## DOC-SCALE-BASELINE

```text
[ ] Source file 존재
[ ] Filename = SCALE_CORE_BASELINE_v0.2.md
[ ] Destination = core/scale/
[ ] Version = v0.2
[ ] Status = APPROVED_AS_SCALE_ROUTING_BASELINE
[ ] Phase 0 pointer metadata fix 완료
[ ] 51 Handoff 유지
```

---

# 5. Phase C — Genre Baselines

## Deckbuilding

```text
[ ] DECKBUILDING_CORE_CANDIDATES_v0.1.md 존재
[ ] APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE 확인
[ ] core/genre/baselines/Deckbuilding/ 이동
```

## Management

```text
[ ] MANAGEMENT_CORE_CANDIDATES_v0.1.md 존재
[ ] 승인 상태 확인
[ ] core/genre/baselines/Management/ 이동
```

## Roguelike

```text
[ ] ROGUELIKE_CORE_CANDIDATES_v0.1.md 존재
[ ] 승인 상태 확인
[ ] core/genre/baselines/Roguelike/ 이동
```

## Deduction

```text
[ ] DEDUCTION_INFORMATION_CORE_CANDIDATES_v0.1.md 존재
[ ] 승인 상태 확인
[ ] core/genre/baselines/Deduction/ 이동
```

## Narrative

```text
[ ] NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1.md 존재
[ ] 승인 상태 확인
[ ] core/genre/baselines/Narrative/ 이동
```

## Strategy

```text
[ ] STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md 존재
[ ] 승인 상태 확인
[ ] core/genre/baselines/Strategy/ 이동
[ ] STRATEGY_CORE_CANDIDATES_v0.1.md draft → history/consolidation/
```

## Simulation

```text
[ ] SIMULATION_CORE_CANDIDATES_v0.1_APPROVED.md 존재
[ ] 승인 상태 확인
[ ] core/genre/baselines/Simulation/ 이동
[ ] SIMULATION_CORE_CANDIDATES_v0.1.md draft → history/consolidation/
```

## RPG

```text
[ ] RPG_CORE_CANDIDATES_v0.1_APPROVED.md 존재
[ ] 승인 상태 확인
[ ] Phase 0 UC006 title metadata sync 완료
[ ] core/genre/baselines/RPG/ 이동
[ ] RPG_CORE_CANDIDATES_v0.1.md draft → history/consolidation/
```

## Action

```text
[ ] ACTION_CORE_CANDIDATES_v0.1_APPROVED.md 존재
[ ] 승인 상태 확인
[ ] Phase 0 Failure Attribution mapping sync 완료
[ ] core/genre/baselines/Action/ 이동
[ ] ACTION_CORE_CANDIDATES_v0.1.md draft → history/consolidation/
```

## Genre Registry Check

```text
[ ] Conditional Genre Baseline = 9
[ ] duplicate active Genre version = 0
[ ] L0 Genre default load = 0
```

---

# 6. Phase D — Reference Library

```text
[ ] references/REF_Reference_Master_Index.md 이동
[ ] REF_Layer_1_Core_Design.md → references/research/
[ ] REF_Layer_2_Specialized.md → references/research/
[ ] REF_Layer_3_Solo_Micro_Production.md → references/production/
[ ] REF_Layer_4_Commercial.md → references/market/
[ ] REF_Layer_5_Korean_Selection.md → references/market/
[ ] REF_2024_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md → references/market/
[ ] REF_2025_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md → references/market/
[ ] REF_2026_Korean_Indie_Award_Market_Benchmark_INTEGRATED.md → references/market/
[ ] REF_Game_Design_Case_Study_Template_v1.0.md → references/methodology/
[ ] REF_Game_Design_Reviewer_Final_Evaluation_Template_v2.0.md → references/methodology/
[ ] REF_Game_Design_Reviewer_Project_Instructions_v2.0.md → references/methodology/
```

Guard:

```text
[ ] Reference Runtime Load = LOOKUP_ONLY
[ ] Reference Game Observation을 direct Rule로 사용하지 않음
```

---

# 7. Phase E — Runtime Tests

## MCC

```text
[ ] REVIEWER_RUNTIME_DRYRUN_01_PROJECT_MCC_v0.1.md
    → tests/reviewer_runtime/fixtures/MCC/
```

## Magic Word

```text
[ ] REVIEWER_RUNTIME_DRYRUN_02_MAGIC_WORD_v0.1.md
    → tests/reviewer_runtime/fixtures/MagicWord/
```

## Cross Assessment

```text
[ ] REVIEWER_RUNTIME_CROSS_DRYRUN_ASSESSMENT_v0.1.md
    → tests/reviewer_runtime/assessments/
```

Guard:

```text
[ ] Runtime Test classification 확인
[ ] Core Promotion Evidence로 사용하지 않음
```

Optional fixture pointer:

```text
[ ] Project name 기록
[ ] Project version 기록
[ ] Project repository 기록
[ ] tested commit SHA 기록
```

Project GDD 전체 copy는 기본 금지.

---

# 8. Phase F — Runtime History

다음 파일:

```text
[ ] REVIEWER_RUNTIME_SPECIFICATION_v0.1.md
[ ] REVIEWER_RUNTIME_SPECIFICATION_v0.1_APPROVED.md
[ ] REVIEWER_RUNTIME_CORRECTION_NOTE_01_v0.1.md
[ ] REVIEWER_RUNTIME_DEFECT_LOG_01_v0.1.md
[ ] REVIEWER_RUNTIME_DEFECT_LOG_02_v0.1.md
```

→ `history/runtime/`

검사:

```text
[ ] Runtime Load = NEVER
[ ] v1.0 실행에서 재적용하지 않음
```

---

# 9. Phase G — Consolidation / Previous Version History

```text
[ ] Studio Core v0.2 / v0.3 → history/consolidation/
[ ] Genre Master v0.1 / v0.1 Approved / v0.2 → history/consolidation/
[ ] Scale v0.1 / v0.1 Approved → history/consolidation/
[ ] Genre × Scale Integration v0.1 / Approved → history/consolidation/
[ ] GSC Canonical Consolidation → history/consolidation/
[ ] Universal Consolidation draft / approved → history/consolidation/
[ ] Universal Canonical Sync → history/consolidation/
[ ] non-approved Strategy/Simulation/RPG/Action duplicates → history/consolidation/
```

Guard:

```text
[ ] Historical ≠ Current Rule
[ ] Runtime Load = NEVER
```

---

# 10. Phase H — Inactive Drafts

다음:

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
```

→ `history/drafts/`

확인:

```text
[ ] Classification = HISTORICAL / INACTIVE_DRAFT
[ ] Reviewer Runtime dependency에서 제외
[ ] AI default context에서 제외
```

---

# 11. Phase I — Deprecated

기본 정책:

> 명시적 deprecated 전체 문서는 Working Tree에서 제거하고 Git history로 추적.

audit 사유로 남길 때만:

`history/deprecated/`

검사:

```text
[ ] DEPRECATED Runtime Load = NEVER
[ ] current Manifest에서 active pointer 없음
```

---

# 12. Phase J — Project GDD Separation

Studio OS Core에 전체 이동 금지:

```text
[ ] MCC GDD
[ ] Magic Word GDD
[ ] Villain Inc. GDD
[ ] Other Project GDD
```

각 Project Repository가 소유.

Project Review Result도 기본적으로 각 Project Repository에 저장.

---

# 13. Phase K — Manifest Path Verification

모든 Canonical Registry Entry마다:

```text
[ ] Actual file exists
[ ] Manifest filename matches
[ ] Manifest path matches repository path
[ ] Version matches
[ ] Status matches
[ ] Classification matches
[ ] Runtime Load matches
[ ] Dependencies resolvable
```

Actual / Manifest mismatch 발견 시:

1. latest approved actual file 확인
2. Logical ID 확인
3. Manifest filename/path/version 수정
4. 필요하면 metadata-only sync
5. Assembly 단계에서 Core Rule 자체는 임의 수정하지 않음

---

# 14. Phase L — README / AI Instructions

```text
[ ] README short-form 확인
[ ] README에 Core Rule 상세 복제 없음
[ ] Canonical Manifest path 정확
[ ] Runtime path 정확
[ ] AI_OPERATING_INSTRUCTIONS.md 추가
[ ] Conversation Memory ≠ Canonical 명시
[ ] Project GDD precedence 명시
[ ] Historical / Deprecated override 금지
```

---

# 15. Phase M — Package Health Check

## Canonical

```text
[ ] Manifest current = 1
[ ] Reviewer Runtime current = 1
[ ] Universal current = 1
[ ] Genre Master current = 1
[ ] Scale current = 1
```

## Genre

```text
[ ] Conditional Genre Baseline = 9
[ ] duplicate active genre version = 0
```

## History

```text
[ ] Runtime v0.1 active = 0
[ ] Correction Note active = 0
[ ] stale Genre draft active = 0
```

## Runtime

```text
[ ] PASS 0~15 accessible
[ ] UC006 remains CANDIDATE
[ ] UC006 runtime = CONDITIONAL DIAGNOSTIC
[ ] Active Independent GSC = 0
[ ] Validation Planner not required
[ ] Scale Resolution State supported
[ ] ENUM_CONFORMANCE_CHECK supported
```

## Runtime Test

```text
[ ] MCC fixture exists
[ ] Magic Word fixture exists
[ ] Cross assessment exists
```

---

# 16. Phase N — Final Release Gate

모두 확인:

```text
[ ] Phase 0 metadata fix 4건 완료
[ ] required file missing = 0
[ ] Canonical filename mismatch = 0
[ ] Canonical active duplicate = 0
[ ] Conditional genre = 9
[ ] Historical default load = 0
[ ] Project GDD copied into core = 0
[ ] Runtime Test misclassified as Core = 0
```

그 후:

```text
Package Readiness:
PACKAGE_READY
```

로 전환 가능.

---

# 17. Phase O — Git Tag / Release

```text
[ ] merge to main
[ ] main 상태 재검증
[ ] git tag studio-os-v1.0
[ ] tag push
[ ] optional GitHub Release 생성
```

권장 Release title:

`Studio OS Core Package v1.0`

---

# 18. Current Final Position

현재 working set 기준:

```text
Essential files:
PRESENT

Canonical ownership:
CLEAR

Runtime v1.0:
APPROVED

Manifest v1.0:
APPROVED

Missing canonical:
0

Migration metadata fix:
4
```

따라서 현재:

`PACKAGE_READY_WITH_MIGRATION_FIX`

이다.

Phase 0 완료 후:

`PACKAGE_READY`

로 승격할 수 있다.
