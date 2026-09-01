# Studio OS

Studio OS는 출시 게임·시장·개발 사례에서 추출한 **Evidence-Based Knowledge**를 이용해 신규 게임 기획의 구조적 위험, 제작 위험, 검증 필요 Claim을 조기에 발견하는 개인용 Game Design Review System이다.

Studio OS는:
- 성공하는 게임을 예측하는 시스템이 아니며
- 재미를 자동 판정하는 AI가 아니고
- 판매량 예측기가 아니다.

## Current Package

`Studio OS Core Package v1.0`

Canonical source map:

`manifest/STUDIO_OS_CANONICAL_DOCUMENT_MANIFEST_v1.0.md`

Reviewer execution baseline:

`core/runtime/REVIEWER_RUNTIME_SPECIFICATION_v1.0.md`

## Basic Review Flow

```text
Current Project GDD
↓
Studio OS Canonical Manifest
↓
Reviewer Runtime
↓
Universal Applicability
↓
Genre Routing
↓
Scale Routing
↓
Conditional Genre Load
↓
Root Findings
↓
Structural Fix / Validation Required
```

## Repository Structure

```text
Studio-OS/
├─ README.md
├─ STUDIO_OS_CORE_PACKAGE_v1.0.md
├─ AI_OPERATING_INSTRUCTIONS.md
├─ manifest/
├─ core/
│  ├─ universal/
│  ├─ genre/
│  ├─ scale/
│  └─ runtime/
├─ references/
├─ tests/reviewer_runtime/
└─ history/
```

## Source of Truth

Studio OS Rule의 Source of Truth는:

```text
GitHub main
+
Current Approved Canonical Manifest
```

이다.

```text
Conversation Memory
≠
Canonical Knowledge
```

개별 게임 사실관계는 각 Project Repository의 **Current Approved GDD**가 우선한다.

## Runtime Loading

기본 논리 Set:

```text
Manifest
Reviewer Runtime
Universal
Genre Master
Scale
+
Routed Genre Baselines
```

Context-efficient 권장 방식:

```text
FULL:
Manifest + Reviewer Runtime

SECTION LOOKUP:
Universal + Genre Master + Scale

CONDITIONAL:
Routed Genre Baselines

LOOKUP ONLY:
Reference / Runtime Test

NEVER:
Historical / Deprecated
```

## Knowledge Update

```text
New Reference
↓
Evidence Extraction
↓
Candidate Pattern
↓
Core Review
↓
Canonical Update
↓
Manifest Update
↓
Merge to main
```

Runtime 수정은 별도 Regression Fixture를 거쳐 새 Runtime Version으로 통합한다.

자세한 현재 파일 목록·Version·Load Policy·Supersession은 README가 아니라 **Canonical Manifest**가 소유한다.
