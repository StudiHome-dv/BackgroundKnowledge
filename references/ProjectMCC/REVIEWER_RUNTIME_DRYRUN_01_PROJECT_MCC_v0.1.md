# REVIEWER_RUNTIME_DRYRUN_01_PROJECT_MCC_v0.1

**Studio OS — Reviewer Runtime Dry-run #1**  
**Project:** `Project MCC / 빌런 대응 관제센터`  
**Project Version:** `v0.5`  
**Dry-run ID:** `DRYRUN-01`  
**Mode:** `DEEP REVIEW`  
**Reviewer Runtime:** `REVIEWER_RUNTIME_v0.1`  
**Studio Core:** `v0.4`  
**Genre Master:** `v0.3`  
**Scale Baseline:** `v0.2`  
**Review Date:** `2026-09-01`  
**Project Review Verdict:** `REVIEW_CLEAR_WITH_VALIDATION`

---

# 1. Dry-run Snapshot

```text
DRY_RUN_ID:
DRYRUN-01

Project:
Project MCC / 빌런 대응 관제센터

Project Version:
v0.5

Reviewer Runtime:
REVIEWER_RUNTIME_v0.1

Studio Core:
v0.4

Genre Master:
v0.3

Scale Baseline:
v0.2

Loaded Genre Baselines:
- Strategy v0.1 APPROVED
- Management v0.1
- Simulation v0.1 APPROVED

Mode:
DEEP REVIEW

Review Date:
2026-09-01
```

이번 Dry-run은 `Villain Inc.`가 아니라 사용자 제공 최신 통합 문서인 `Project MCC 통합 기획 정리 v0.5`를 Project Source로 사용한다.

현재 Review Target은 문서 전체 제품 비전이 아니라:

```text
Current Development Stage:
Core Prototype 기술 설계 준비

Active Review Slice:
Core Prototype
```

를 중심으로 한다.

Project Source 자체가 Core Prototype에서 다음을 제외한다고 명시한다.

- 경제
- 도시개발
- 정보분석팀
- 정식 히어로 전투

따라서 이 시스템들은 Full Product Context에는 기록하되 현재 Prototype Root Finding의 Active Violation Source로 과도하게 로드하지 않는다.

---

# 2. Input Integrity

## INPUT_INTEGRITY_REPORT

### Active Sources

1. `Project_MCC_통합_기획정리_v0.5.md`
   - 현재 최신 통합 기획 정리본
   - 전체 방향 정리 완료
   - Core Prototype 기술 설계 준비

### Runtime Canonical Sources

- `REVIEWER_RUNTIME_SPECIFICATION_v0.1_APPROVED.md`
- `Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`
- `GENRE_CORE_MASTER_INDEX_v0.3.md`
- `SCALE_CORE_BASELINE_v0.2.md`

### Loaded Genre Sources

- `STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md`
- `MANAGEMENT_CORE_CANDIDATES_v0.1.md`
- `SIMULATION_CORE_CANDIDATES_v0.1_APPROVED.md`

### Deprecated Sources

Current input bundle에서 MCC의 이전 버전 문서는 제공되지 않았다.

따라서 v0.5와 충돌하는 과거 Rule을 Active Source로 사용하지 않는다.

### Conflicts

`NONE FOUND`

현재 v0.5 내부에서 Core Prototype Scope와 Full Product Scope는 명시적으로 구분되어 있다.

### Unknown Version Relationships

별도 `Locked Decision Manifest`는 제공되지 않았다.

그러나 사용자 지시와 문서 자체가 v0.5를 최신 통합 기획으로 지정하므로 이번 Dry-run에서는 v0.5를 Active Project Source로 사용한다.

### Input Integrity Status

`CLEAR`

### Boundary Note

이번 Dry-run에서 가장 중요한 Source 해석 규칙:

```text
Full Product Feature
≠
Current Prototype Active Scope
```

이다.

---

# 3. Project Mechanism Profile

## PROJECT_MECHANISM_PROFILE

### Project

`Project MCC / 빌런 대응 관제센터`

### Core Player Fantasy

도시에 발생한 빌런/괴수 사건에서 관제센터 운영자로서:

- 시민 이동을 직접 지시하고
- 빌런/괴수의 목적과 이동을 관찰·예측하며
- 시설과 환경 개입으로 간접 유도하고
- 히어로 도착 전 피해를 최소화하는

실시간 재난 관제 전략.

### Primary Player Verbs

- 관찰한다
- 시민 집단을 선택한다
- 시민 목적지를 재지정한다
- 포대를 ON/OFF한다
- 방벽을 OPEN/CLOSE한다
- 유도기를 ON/OFF한다
- 예상 경로를 비교한다
- ETA를 비교한다
- 충돌 위험을 판단한다
- 변화 후 계획을 다시 연결한다

### Secondary Player Verbs — Full Product

- 대응 인프라 위치 선택
- 복구 우선순위 선택
- 장기 투자
- 히어로 선택
- 정보 수준 관리

현재 Core Prototype에서는 일부 제외.

### Core Loop

```text
괴수 예상경로 확인
→ 시민 대피계획 수립
→ 포대 / 방벽 / 유도기로 개입
→ 괴수 경로 변경
→ 시민 경로와 신규 충돌
→ 시민 경로 재설정
→ 다시 관찰 / 대응
```

### Loop Unit

`Incident / Crisis Replanning Cycle`

### Loop Reset

Prototype:
- Mission clear / failed

Full Product:
- 사건 종료
- 결과 보고
- 다음 달

### Decision Types

- Position
- Timing
- Information
- Risk
- Resource
- Routing / path
- Priority
- Intervention

### Persistent States — Prototype

- 시민 위치 / 목적지 / 경로
- 괴수 위치 / Primary Objective / Temporary Target
- 포대 상태
- 방벽 상태
- 유도기 상태
- 발전소 / 관제센터 생존 상태

### Persistent States — Full Product

- 시설 상태
- 도시 중요도
- 세입 / 복구비
- 반복 빌런 정보
- 캠페인 진행도

현재 Prototype에서는 대부분 Deferred.

### Temporary States

- 괴수 Temporary Target
- 포대 영향
- 유도기 효과
- 충돌 위험
- 변경된 예상경로
- Hero ETA

### Main Resources

Prototype:
- 시간
- 공간 / 경로
- intervention opportunity

Full Product:
- 예산
- 시설
- 정보
- 대응 여력

### Failure Structure

Prototype:
- 괴수가 Hero 도착 전 발전소 도달
- 관제센터 파괴

Full Product:
- 사건 실패가 캠페인 상태에 누적
- 관제센터 완전 파괴는 즉시 Game Over

### Recovery Structure

Prototype:
- 시민 경로 재지정
- 시설 상태 변경
- 괴수 경로 재유도

Full Product:
- 후속 히어로 호출
- 다음 달 복구
- 영구 인프라 재구성

### Progression Structure

현재 Prototype:
`N/A / DEFERRED`

Full Product:
- 도시 중요도
- 대응 인프라
- 정보분석팀
- 장기 시설
- 캠페인 위협 상승

### Information Structure

Prototype:
- 괴수 계산 경로 전체 공개
- 실제 이동 좌표와 Overlay 동일 Source
- ETA
- 예상 충돌
- 경로 변화 원인 피드백

Full Product:
- 사전정보 / 현장정보
- 정보팀 수준에 따른 가시성
- 원인 분석 지연
- 반복 빌런 정보 자산화

### Content Unit

- 도시 맵
- 시민 집단
- 괴수 Profile
- 대응시설
- Incident Scenario

### System Dependencies

```text
Facility State
↓
Kaiju Cost / Temporary Target
↓
Kaiju Route Recalculation
↓
Route Overlay
↓
ETA
↓
Civilian Collision Prediction
↓
Player Replanning
```

이 dependency chain은 Prototype의 핵심 기술·게임플레이 결합부다.

### Production-heavy Areas

- 시민 Road Graph
- 괴수 Weighted Navigation
- dynamic path recalculation
- route visualization
- ETA / collision prediction
- autonomous AI
- state observability
- QA of route + facility interactions

### Product Promises

1. `Indirect Control`
2. `Predictable Autonomy`
3. `Continuous Replanning`
4. `Future Collision / ETA-based Decision`
5. `Different Intervention Roles`
6. `Real-time Crisis Judgment`
7. `Lightweight Operations, not Full City Builder`
8. `Solo-feasible Risk-first Prototype`

---

# 4. Product Promise

## Core Promise A — Indirect Control

> 시민에게는 경로를 명령하고, 빌런에게는 환경을 제시한다.

이 문장은 MCC의 Control Fantasy를 가장 정확하게 정의한다.

## Core Promise B — Continuous Replanning

> 완벽한 계획을 세우는 게임이 아니라, 계속 무너지는 계획을 더 큰 피해가 나기 전에 다시 연결한다.

Prototype의 존재 이유와 직접 연결된다.

## Core Promise C — Predictable Autonomy

괴수는 플레이어가 직접 이동명령을 내리지 않지만:

- Primary Objective
- Temporary Target
- Threat / stimulus
- terrain
- trait

에 의해 납득 가능한 경로를 만든다.

## Core Promise D — Information as Decision Tool

MCC의 정보 핵심은:

> 현재 위치보다 몇 분 뒤 발생할 충돌.

따라서 ETA / route / collision prediction이 실제 의사결정 자원이어야 한다.

## Supporting Promise — Lightweight Operations

도시 운영 / 경제는 독립 City Builder가 아니라 관제 조건을 바꾸는 보조 전략층.

현재 Prototype에서는 의도적으로 제외.

---

# 5. Claim Registry

| Claim | Type | Evidence State | Current Support | Status | Validation Needed | Suggested Evidence Type |
|---|---|---|---|---|---|---|
| 시민은 직접 지시하고 괴수는 환경으로 간접 유도할 때 Agency가 성립한다 | DESIGN / EXPERIENCE | KNOWN + unproven experience | Control architecture가 명확히 명시 | PARTIALLY SUPPORTED | YES | HYBRID |
| 괴수의 자율적 경로 변경이 예측 가능하지만 직접조종처럼 느껴지지 않는다 | DESIGN / EXPERIENCE | KNOWN claim | Primary/Temporary Target + cost model 명시 | VALIDATION_REQUIRED | YES | HYBRID |
| 경로 변화가 시민 계획을 반복적으로 무너뜨려 재계획을 요구한다 | DESIGN / EXPERIENCE | KNOWN claim | Core Loop에 명시 | VALIDATION_REQUIRED | YES | HUMAN TEST |
| ETA와 예상 충돌이 실제 판단 근거가 된다 | DESIGN / EXPERIENCE | KNOWN claim | ETA / collision system 명시 | VALIDATION_REQUIRED | YES | HUMAN TEST |
| 포대 / 방벽 / 유도기가 다른 전략적 역할을 가진다 | DESIGN / EXPERIENCE | KNOWN structure | suppression / path cost / temp target 분리 | PARTIALLY SUPPORTED | YES | HUMAN TEST |
| Full path 공개 Prototype으로 Core interaction을 먼저 검증한 뒤 정보 제한을 추가한다 | PRODUCTION / DESIGN | KNOWN | Prototype scope에 명시 | STRUCTURALLY SUPPORTED | NO | NONE |
| 경로 계산 데이터와 실제 이동 / Overlay를 같은 Source로 사용해 정합성을 유지한다 | PRODUCTION | KNOWN | 명시적 기술 원칙 | STRUCTURALLY SUPPORTED | NO | SELF TEST |
| 1인 개발에서 범용 pathfinding은 asset을 사용하고 MCC logic만 자체 소유한다 | PRODUCTION | KNOWN | 기술 구현 원칙 명시 | STRUCTURALLY SUPPORTED | NO | SELF TEST |
| 도시 경제가 관제 핵심을 침범하지 않는다 | DESIGN | KNOWN intention | 70~80% 관제, Prototype 제외 | PARTIALLY SUPPORTED / DEFERRED | LATER | HUMAN TEST |
| Real-time with Pause가 정답 입력형 정적 퍼즐이 아니라 긴장과 판단을 만든다 | EXPERIENCE | KNOWN claim | Pause / 1x / 2x 명시 | VALIDATION_REQUIRED | YES | HUMAN TEST |

---

# 6. Universal Applicability

## UC-DESIGN-001 — Consequence Density over Input Count

**Applicability:** `YES`

Relevant Mechanism:
- 시민 reroute
- 포대 toggle
- 방벽 toggle
- 유도기 toggle

Reviewer Question:

> 네 개입이 단순히 같은 경로 조작을 다른 버튼으로 반복하는가, 아니면 서로 다른 비용·상태·후속 판단을 만드는가?

---

## UC-DESIGN-002 — Contextual Value Shift

**Applicability:** `YES`

Relevant Promise:
- same map / different response
- kaiju profile difference
- route/context-dependent facility value

Reviewer Question:

> 같은 포대·방벽·유도기가 괴수 타입, 현재 경로, 시민 흐름에 따라 실제로 다른 가치가 되는가?

---

## UC-DESIGN-003 — Consequence-to-Next-Decision Coupling

**Applicability:** `YES`

Relevant Mechanism:

```text
Facility Change
→ Kaiju Route Change
→ Collision Change
→ Civilian Replanning
```

Reviewer Question:

> 이전 개입의 결과가 실제 다음 시민/시설 판단을 바꾸는가?

---

## UC-DESIGN-004 — Uncertainty Requires Response Agency

**Applicability:** `YES`

Relevant Promise:
- autonomous kaiju
- indirect control

Reviewer Question:

> 플레이어가 괴수를 직접 명령하지 않아도 준비·유도·회피·재계획으로 충분히 대응할 수 있는가?

---

## UC-DESIGN-005 — Actionable Information

**Applicability:** `YES`

Relevant Mechanism:
- route overlay
- ETA
- collision warning
- cause feedback

Reviewer Question:

> 경로 / ETA / 원인 정보가 단순 표시가 아니라 실제 명령 변경으로 이어지는가?

---

## UC-DESIGN-006 — Progression Should Match Its Intended Promise

**Applicability:** `CONDITIONAL — NOT ACTIVE IN CURRENT PROTOTYPE SLICE`

Full Product에는 progression이 존재한다.

그러나 현재 Core Prototype은:
- 경제
- 도시개발
- 정보팀
- 장기 progression

을 명시적으로 제외한다.

따라서 이번 Dry-run의 Active Finding Source로 사용하지 않는다.

---

# 7. Genre Routing Profile

## Routing Scores

| Genre | Core Loop | Player Verb | State | Decision | Product Promise | Total | Level | Runtime |
|---|---:|---:|---:|---:|---:|---:|---|---|
| Strategy | 2 | 2 | 2 | 2 | 2 | **10** | **L3** | PRIMARY |
| Management | 2 | 2 | 2 | 2 | 1 | **9** | **L3** | PRIMARY / OPERATIONS |
| Simulation | 2 | 1 | 2 | 2 | 1 | **8** | **L2** | SECONDARY |
| Narrative / Systemic Narrative | 0 | 0 | 1 | 1 | 1 | **3** | L1 | SUPPORTING ONLY |
| Deduction / Information | 0 | 0 | 1 | 1 | 0 | **2** | L0 | NOT LOADED |
| Action | 0 | 1 | 0 | 1 | 0 | **2** | L0 | NOT LOADED |
| Roguelike | 0 | 0 | 0 | 1 | 0 | **1** | L0 | NOT LOADED |
| RPG | 0 | 0 | 0 | 0 | 0 | **0** | L0 | NOT LOADED |
| Deckbuilding | 0 | 0 | 0 | 0 | 0 | **0** | L0 | NOT LOADED |

## PROJECT_GENRE_ROUTING_PROFILE

### Primary — Strategy

**Level:** `L3`  
**Score:** `10`

Why Loaded:
- 경로 예측
- 위치
- ETA
- future option
- intervention
- replanning
- objective pressure

가 Core Loop 전체를 지배한다.

### Primary — Management / Operations

**Level:** `L3`  
**Score:** `9`

Why Loaded:
- 여러 시민 집단
- 시설 상태
- 시간 압박
- priority conflict
- monitoring
- rerouting
- responsibility scope

가 incident play의 실제 Verb다.

`경량 도시 운영`이라는 테마 때문이 아니라 **관제 운영 자체가 Management Mechanism**이므로 L3.

### Secondary — Simulation

**Level:** `L2`  
**Score:** `8`

Why Loaded:
- autonomous kaiju
- weighted navigation
- system state propagation
- facility influence
- route recomputation

가 player decision의 원인이 된다.

다만 플레이어의 fantasy는 Simulation 관찰 자체보다 Strategy / Operations에 있으므로 L2.

### Supporting — Narrative

**Level:** `L1`

현재 Full Product에는:
- 반복 등장 빌런
- 정보 자산
- 사건 보고
- 월간 진행

이 있지만 Core Prototype의 Player Verb나 Product Promise를 지배하지 않는다.

따라서 Narrative Core 상세 Load는 하지 않는다.

### Not Loaded

- Deduction
- Action
- Roguelike
- RPG
- Deckbuilding

Real-time, 정보, 빌런 테마라는 표면적 인접성만으로 Load하지 않는다.

## HYBRID_SCOPE_WARNING

`NO`

Primary L3 2개 + L2 1개는 Hybrid이지만, 세 Genre가 하나의 incident-state / route / intervention chain을 공유한다.

---

# 8. Hybrid Resolver

## Strategy × Management

**Interaction Type:** `TYPE-A — Reinforcing`

Shared Verb:
- reroute
- toggle
- prioritize
- monitor

Shared State:
- civilian routes
- facility states
- ETA
- danger zones

Shared Consequence:
- future options / safety / time pressure

Conflict:
`NONE STRUCTURALLY CONFIRMED`

Risk:
Strategy choice가 Management workload로만 변하면 decision density가 떨어질 수 있음.

---

## Strategy × Simulation

**Interaction Type:** `TYPE-A — Reinforcing`

Shared State:
- kaiju path
- facility influence
- objectives
- route cost

Simulation causal changes are directly consumed by Strategy replanning.

Risk:
autonomy가 너무 불투명하면 Strategy가 guesswork가 됨.

---

## Management × Simulation

**Interaction Type:** `TYPE-C — Conditional`

Simulation detail은:

> Player Responsibility를 바꾸는 정보 / 상태일 때만

Management value가 있다.

그렇지 않으면:
- extra state
- UI burden
- QA
- micromanagement

로 변할 수 있다.

Routing Specialization:

`Responsibility Level as Scope Cut Boundary`

를 Reviewer Action Hint로 사용한다.

별도 Severity Source로 사용하지 않는다.

---

# 9. Scale Routing Profile

## PROJECT_SCALE_ROUTING_PROFILE

### Core Team

`1인 개발`

### Sustained FTE

`UNKNOWN`

### Scale

`SOLO`

### External Support

Project Source에 human contractor / external team 정보 없음.

`UNKNOWN / NOT ASSUMED`

### AI-assisted Work

`YES`

단:

```text
AI Assistance
≠
Additional FTE
```

### Critical Single-owner Domains

- game design
- programming
- system integration
- project architecture
- gameplay QA
- UI integration
- prototype production

### Parallel Production Lanes

실질적으로 제한적.

External asset / AI는 productivity modifier 또는 dependency reduction으로 사용.

### Specialist Dependencies

- pathfinding package integration
- route visualization
- Unity implementation

외부 package가 있어도 MCC-specific:
- threat rules
- route costs
- target switching
- collision prediction
- debugging
- acceptance QA

ownership은 내부에 남는다.

### Evidence Boundary

Solo evidence는 강한 적용 범위.

---

## Scale Core Applicability

### SC-SOLO-001 — Risk-first Prototype

**Applicability:** `YES`

Project는 명시적으로:
- 2D debug map
- Kaiju A first
- economy/info/heroes deferred
- free/official assets first

로 위험한 Core interaction만 먼저 검증한다.

현재 강한 Supported Structure.

### SC-SOLO-002 — Visible Scope ≠ Production Scope

**Applicability:** `YES`

Prototype 화면은 단순하지만 실제 hidden complexity는:

```text
2 navigation structures
+
dynamic route change
+
overlay sync
+
ETA
+
collision prediction
+
facility state
+
autonomous AI
```

로 높다.

### SC-SOLO-003 — Common Grammar is a Content Multiplier

**Applicability:** `YES`

- Primary Objective
- Temporary Target
- Attraction
- Avoidance
- Reaction
- MovementProfile

공통 AI grammar와 shared path data를 사용한다.

단 QA cost는 사라지지 않는다.

### SC-SOLO-004 — Never Copy Post-success Scope

**Applicability:** `N/A / NO ACTIVE TRIGGER`

현재 Project는 상용 Reference의 post-success scope를 복제하는 방향이 아니라 오히려 Prototype scope를 축소하고 있다.

---

# 10. Loaded Scale Handoffs

이번 Dry-run에서 실제로 Load한 Handoff만 기록한다.

## `SCALE_HANDOFF-STRAT-003 — Map / Pathfinding Scope`

**Loaded:** YES

Reason:
MCC Core Prototype이:
- civilian road graph
- kaiju weighted navigation
- dynamic route
에 직접 의존.

---

## `SCALE_HANDOFF-SIM-002 — Cross-system Interaction Matrix`

**Loaded:** YES

Reason:

```text
Facility
×
Kaiju Profile
×
Route
×
Civilian Route
×
ETA / Collision
```

조합이 Core QA surface.

---

## `SCALE_HANDOFF-SIM-003 — Agent AI Cost`

**Loaded:** YES

Reason:
Kaiju autonomy / target / replan은 Prototype의 핵심 기술 위험.

---

## `SCALE_HANDOFF-SIM-005 — Observability Tooling`

**Loaded:** YES

Reason:
경로 Overlay / ETA / cause feedback / debug가 Core Player Information이자 개발 디버깅 기반.

---

## `SCALE_HANDOFF-MGMT-002 — Management UI State Cost`

**Loaded:** YES — bounded

Reason:
현재 Prototype도:
- 시민 3집단
- kaiju
- 시설
- ETA
- collision marker

를 동시에 보여준다.

다만 current scope가 작아 Full-scale UI explosion은 아직 발생하지 않는다.

---

## Not Loaded

- Multiplayer Balance
- Procedural Content
- Companion
- Narrative localization
- large authored content

현재 Prototype Mechanism과 직접 연결되지 않음.

---

# 11. Project Reviewer Set

## Question Count Audit

```text
Universal Questions:
5

Primary Strategy Questions:
6

Primary Management Questions:
6

Secondary Simulation Questions:
5

Scale Questions:
3

Handoff Questions:
5

Hybrid Questions:
3

Market / Selection Questions:
0

Before Dedup:
33

After Dedup:
13

Reduction:
20
```

이 숫자는 합격 Threshold가 아니라 Question Explosion audit다.

## Final Deduped Reviewer Questions

### Q-01 — Intervention Consequence Density

Sources:
- UC001

> 시민 reroute / 포대 / 방벽 / 유도기가 서로 다른 consequence를 만드는가, 아니면 같은 route control을 다른 버튼으로 반복하는가?

### Q-02 — Contextual Intervention Value

Sources:
- UC002
- GC-STRAT-003
- GC-SIM-005

> 같은 시설이 괴수 특성·현재 route·시민 흐름에 따라 실제로 다른 가치를 갖는가?

### Q-03 — Replanning Coupling

Sources:
- UC003
- GC-STRAT-001
- GC-STRAT-002
- GC-MGMT-004
- GC-SIM-002

> 한 번의 개입 결과가 다음 판단을 실제로 바꾸는가, 아니면 재계획 없이도 기존 계획이 유지되는가?

### Q-04 — Predictable Autonomy

Sources:
- UC004
- GC-SIM-006
- GC-STRAT-007

> 괴수는 직접 명령할 수 없지만 충분히 대응 가능한가? 너무 통제 가능하거나 너무 불투명하지 않은가?

### Q-05 — Information → Action / Learning

Sources:
- UC005
- GC-STRAT-004
- GC-MGMT-007
- GC-SIM-004

> 예상경로 / ETA / 충돌 / 원인 정보가 실제 명령 변경과 다음 판단 학습으로 이어지는가?

### Q-06 — Spatial Value

Sources:
- GC-STRAT-005

> Hardpoint / 방벽 / 도로 위치가 future option value를 실질적으로 바꾸는가?

### Q-07 — Priority Conflict vs Workload

Sources:
- GC-MGMT-001
- GC-MGMT-014
- Management × Solo Routing Hint

> 여러 시민집단과 시설을 관리하는 것이 우선순위 선택을 만드는가, 단순 클릭 workload를 늘리는가?

### Q-08 — Time Pressure

Sources:
- GC-MGMT-005

> HERO ETA가 단순 countdown인가, 현재 행동과 미래 위험 사이의 tradeoff를 만드는가?

### Q-09 — Selective Simulation

Sources:
- GC-SIM-001
- GC-MGMT-014

> 현재 simulation detail 중 Player Responsibility와 의사결정에 필요 없는 state가 있는가?

### Q-10 — Risk-first Prototype

Sources:
- SC-SOLO-001

> Prototype이 core-risk 검증보다 완성품 scope를 앞서 구현하고 있지 않은가?

### Q-11 — Hidden Production Integration

Sources:
- SC-SOLO-002
- STRAT-003
- SIM-002
- SIM-003
- SIM-005
- MGMT-002

> route calculation → movement → overlay → ETA → collision chain의 integration cost가 현재 Solo scope를 위협하는가?

### Q-12 — Common Grammar

Sources:
- SC-SOLO-003

> Kaiju data grammar / shared route source가 unique implementation을 줄이면서 QA를 통제 가능한 형태로 유지하는가?

### Q-13 — Management × Simulation Responsibility Boundary

Sources:
- Hybrid Resolver
- GC-MGMT-014
- GC-SIM-001

> simulation detail이 관제센터 책임 수준 아래로 내려가 micromanagement를 만들고 있지 않은가?

---

# 12. Raw Finding Summary

Relevant Raw Findings generated:

`15`

대표 Raw Finding:

1. autonomous route cause may be structurally legible but human predictability unproven.
2. full calculated route exposure may make kaiju feel too deterministic.
3. temporary target / cost changes may still feel like indirect direct-control.
4. route changes are specified to trigger replanning but recurrence is unproven.
5. civilian rerouting has no specified friction / capacity / command cost.
6. pause allows command during analysis; tension effect unknown.
7. ETA / collision warnings exist but actual use is unproven.
8. turret / wall / lure are structurally distinct but experiential differentiation unproven.
9. hardpoint positioning gives spatial commitment.
10. citizen groups prevent individual-NPC micromanagement.
11. simulation state is deliberately restricted in prototype.
12. two navigation representations + shared overlay create integration risk.
13. autonomous AI + dynamic path recalculation creates debugging / QA risk.
14. same route data for movement + display is a strong consistency mechanism.
15. data-driven kaiju grammar reduces unique AI code risk but does not remove QA.

N/A / Deferred systems are not converted into Raw Findings.

---

# 13. Root Merge / Split

## Merge Cluster A — Predictable Autonomy

Merged:
- UC004 response agency
- SIM autonomous observation/intervention
- UC005 cause legibility subset
- Strategy recovery/flexibility subset

Root:
`Kaiju autonomy must stay inside a predictable-but-not-commandable band.`

---

## Merge Cluster B — Replanning

Merged:
- UC003 consequence coupling
- Strategy future-option / reevaluation
- Management reprioritization
- Simulation causal propagation

Root:
`Route changes must repeatedly create new decisions rather than cosmetic path changes.`

---

## Merge Cluster C — Information Utility

Merged:
- UC005
- Strategy prediction
- Management diagnosis
- Simulation causal diagnosis

Root:
`ETA / collision / path information must change action and support causal learning.`

Not merged with RF-001 because:

- RF-001 asks whether AI behavior is in a usable autonomy band.
- RF-003 asks whether information presented about that behavior is decision-bearing.

Fix and validation question differ.

---

## Merge Cluster D — Production Integration

Merged:
- SC-SOLO-002
- Map / Pathfinding Handoff
- Cross-system interaction
- Agent AI
- Observability
- UI state cost

Root:
`The core prototype concentrates multiple technical dependencies in one route-consistency chain.`

Not merged with Design RFs because:
- Category differs
- Fix differs
- validation form differs

---

## Split — Intervention Differentiation

Facility role differentiation is not merged into autonomy.

Reason:
- autonomy asks whether the kaiju response is legible/usable.
- tool differentiation asks whether three player options create distinct choice value.

Different Root.

---

## Duplicate Root Audit

`Duplicate Final RF: 0`

## Over-Merge Audit

`Over-merged RF: 0`

---

# 14. Critical / High Findings

## RF-MCC-001 — Predictable Autonomy Band

**Status:** `VALIDATION_REQUIRED`  
**Category:** `DESIGN`  
**Severity:** `HIGH`  
**Project Evidence Strength:** `PARTIAL`  
**Knowledge Status:** `MULTI-SOURCE`  
**Knowledge Confidence:** `HIGH`

### Affected Promise

- Indirect Control
- Predictable Autonomy
- Real-time Crisis Judgment

### Evidence

Project Source structurally defines:
- fixed Primary Objective
- Temporary Target
- weighted path cost
- facility influence
- route-change feedback

따라서 autonomy architecture는 존재한다.

하지만 문서만으로는:

> 플레이어가 이 behavior를 “납득 가능한 자율성”으로 느끼는지

확인할 수 없다.

### Root Mechanism

```text
Too Predictable
→ facility toggle behaves like disguised direct movement command

Too Opaque
→ player cannot plan or learn

Required Band
→ behavior changes, but cause and response remain learnable
```

### Universal Parent

- UC-DESIGN-004
- UC-DESIGN-005 partial

### Genre Specialization

- GC-SIM-006
- GC-SIM-004
- GC-STRAT-004

### Why It Matters

이 Root가 실패하면 MCC의 가장 독특한 Control Principle:

> 시민에게는 명령 / 괴수에게는 환경

이 무너진다.

### Recommended Action

`NO NEW SYSTEM FIRST`

현재:
- Primary Objective
- Temporary Target
- route cost
- visible route-change cause

구조를 유지한 상태에서 autonomy band 자체를 검증한다.

불투명함을 해결하기 위해 랜덤 규칙이나 추가 정보시스템을 먼저 늘리지 않는다.

### Action Class

`VALIDATE FIRST`

### Validation Need

```text
VALIDATION_REQUIRED

Claim:
Player can predict and respond to kaiju autonomy without feeling that the kaiju is directly controllable.

Suggested Evidence Type:
HYBRID

Further Validation Design:
DEFERRED
```

### Do Not Infer

- deterministic path model이 곧 재미있다
- cause label이 있다고 player가 실제 cause를 이해한다
- route changes가 많으면 autonomy가 좋다

---

## RF-MCC-002 — Replanning Loop Necessity

**Status:** `VALIDATION_REQUIRED`  
**Category:** `DESIGN`  
**Severity:** `HIGH`  
**Project Evidence Strength:** `PARTIAL`  
**Knowledge Confidence:** `VERY HIGH / HIGH parent cluster`

### Affected Promise

`Continuous Replanning`

### Evidence

Project Source는 Core Loop를 명확하게:

```text
Kaiju route change
→ new collision
→ civilian route reset
```

으로 설계한다.

그러나 현재 Prototype Rule에는:

- civilian reroute cost
- road capacity
- command cooldown
- split cost

가 명시되지 않았다.

이것은 자동 결함이 아니다.

하지만 reroute가:
- 즉시
- 무료
- pause 중 가능

한 상태에서도 실제 tradeoff가 생기는지는 아직 증명되지 않았다.

### Root Mechanism

> 경로 변화가 발생한다는 사실과, 경로 변화가 새로운 의사결정을 만든다는 것은 다르다.

### Universal Parent

`UC-DESIGN-003`

### Genre Specialization

- GC-STRAT-001
- GC-STRAT-002
- GC-MGMT-004
- GC-SIM-002

### Why It Matters

Replanning이 단순한 “새 선을 다시 그리기”가 되면 MCC의 Core Fantasy가 약해진다.

### Recommended Action

현재 구조에 friction 시스템을 선제 추가하지 않는다.

먼저:
- multiple civilian groups
- ETA overlap
- dynamic kaiju route
- limited facility positions

만으로 충분한 priority conflict가 발생하는지 확인한다.

### Action Class

`VALIDATE FIRST`

### Validation Need

```text
VALIDATION_REQUIRED

Claim:
Kaiju route changes naturally force meaningful civilian / facility replanning rather than trivial re-routing.

Suggested Evidence Type:
HUMAN TEST

Further Validation Design:
DEFERRED
```

### Unknown

개입 / reroute의 정확한 opportunity cost는 현재 `UNKNOWN`.

---

## RF-MCC-003 — ETA / Collision Prediction Must Be Decision-Bearing

**Status:** `VALIDATION_REQUIRED`  
**Category:** `DESIGN`  
**Severity:** `HIGH`  
**Project Evidence Strength:** `PARTIAL`  
**Knowledge Confidence:** `HIGH`

### Affected Promise

`Future Collision / ETA-based Decision`

### Evidence

MCC는 명시적으로:

> 현재 위치보다 몇 분 뒤 발생할 충돌이 핵심 정보

라고 정의한다.

Prototype은:
- route ETA
- intersection timing
- collision marker

를 구현한다.

그러나 UI 존재는 사용 가치의 증거가 아니다.

### Root Mechanism

```text
Information shown
≠
Information changes decision
```

### Universal Parent

`UC-DESIGN-005`

### Genre Specialization

- GC-STRAT-004
- GC-MGMT-007
- GC-SIM-004

### Why It Matters

ETA를 보지 않아도:
- 시민 reroute
- facility toggle
- mission success

이 가능하면 MCC의 정보 관제 차별성이 크게 약해진다.

### Recommended Action

현재 Prototype에서 ETA / collision information을 유지한다.

추가 정보 layer를 늘리기 전에:

> 실제 command change를 유발하는가?

를 먼저 확인한다.

### Action Class

`VALIDATE FIRST`

### Validation Need

```text
VALIDATION_REQUIRED

Claim:
ETA and predicted collision information materially change player commands.

Suggested Evidence Type:
HUMAN TEST

Further Validation Design:
DEFERRED
```

---

## RF-MCC-004 — Core Route-Consistency Chain Is a Concentrated Solo Production Risk

**Status:** `ACCEPTED_RISK`  
**Category:** `PRODUCTION`  
**Severity:** `HIGH`  
**Project Evidence Strength:** `CONFIRMED`  
**Knowledge Confidence:** `HIGH`

### Affected Promise

모든 Core Prototype Promise.

### Observed Production Chain

```text
Civilian Graph
+
Kaiju Weighted Navigation
+
Facility Influence
+
Path Recalculation
+
Movement
+
Route Overlay
+
ETA
+
Collision Prediction
+
Pause / Time Scale
```

### Scale Parent

`SC-SOLO-002`

### Relevant Handoffs

- `SCALE_HANDOFF-STRAT-003`
- `SCALE_HANDOFF-SIM-002`
- `SCALE_HANDOFF-SIM-003`
- `SCALE_HANDOFF-SIM-005`
- `SCALE_HANDOFF-MGMT-002`

### Root Mechanism

Simple 2D presentation does not mean simple integration.

Core risk is not art scope.

It is:
- state consistency
- path consistency
- event ordering
- recalculation timing
- debug visibility

### Current Mitigation — Supported

Project Source already does several strong cuts.

- 2D debug map
- one Kaiju first
- full-path prototype
- same route coordinates for movement + overlay
- external pathfinding package
- no economy / info team / hero combat
- P01~P10 staged implementation

### Recommended Action

`CHANGE SCOPE — PRESERVE CURRENT CUTS`

Prototype PASS 전:
- campaign systems
- info limitation
- detailed building traversal
- multiple movement profiles
- broad content

를 integration chain에 섞지 않는다.

### Action Class

`STRUCTURAL FIX FIRST / CURRENTLY MITIGATED`

### Risk Acceptance

이 Production Risk는 Product Promise 자체에 필수라 제거할 수 없다.

따라서:

`ACCEPTED_RISK`

로 기록하되 current mitigation을 보호한다.

### Do Not Infer

- A* asset 사용 = AI / QA cost 제거
- 2D map = low technical scope
- shared route source = regression risk zero

---

# 15. Medium Findings

## RF-MCC-005 — Intervention Roles Could Collapse into Equivalent Route Manipulation

**Status:** `VALIDATION_REQUIRED`  
**Category:** `DESIGN`  
**Severity:** `MEDIUM`  
**Project Evidence Strength:** `PARTIAL`  
**Knowledge Confidence:** `HIGH / MEDIUM-HIGH`

### Affected Promise

- Decision Depth
- Contextual Value
- Infrastructure Strategy

### Current Structural Separation

#### Turret
- suppression / stimulus
- possible target attraction

#### Barrier
- path cost / block

#### Lure
- Temporary Target

구조상 역할은 구분되어 있다.

### Remaining Risk

실제 플레이에서는 세 수단이 모두:

> “괴수 path를 원하는 방향으로 꺾는 버튼”

처럼 수렴할 수 있다.

### Universal Parent

- UC-DESIGN-001
- UC-DESIGN-002

### Genre Relation

- GC-STRAT-003
- GC-STRAT-005
- GC-SIM-005

### Recommended Action

새 facility를 추가하지 않는다.

현재 세 수단만으로:
- 언제 가치가 바뀌는지
- 어떤 상황에서 대체 불가능한지

확인한다.

### Action Class

`VALIDATE FIRST`

### Validation Need

```text
VALIDATION_REQUIRED

Claim:
Turret, barrier, and lure create distinct intervention decisions rather than equivalent route manipulation.

Suggested Evidence Type:
HUMAN TEST

Further Validation Design:
DEFERRED
```

---

# 16. Needs Info

## NI-MCC-001 — Command / Intervention Friction

### Known

- pause 중 command 가능
- citizen reroute 가능
- facility state change 가능

### Unknown

- civilian reroute cost
- command cooldown
- facility toggle cooldown / commitment
- repeated toggle restriction

### Blocked Judgment

`RF-MCC-002 Replanning Decision Density`

### Runtime Treatment

`UNKNOWN ≠ FAIL`

현재 Prototype에서 friction이 없어도 core가 작동할 수 있으므로 선제 기능 추가 근거로 사용하지 않는다.

---

## NI-MCC-002 — Sustained Solo Production Capacity

### Known

- 1인 개발
- AI 활용
- external assets 활용 방침

### Unknown

- Sustained FTE
- contractor support
- schedule
- QA support

### Blocked Judgment

정확한 Production Timeline / throughput.

Runtime은 일정 추정을 만들지 않는다.

---

## NI-MCC-003 — Collision Formal Definition

### Known

- 시민/괴수 path가 위험범위와 시간에서 겹치면 warning.

### Unknown

- exact danger radius
- temporal overlap formal definition
- edge / node crossing semantics

### Blocked Judgment

Collision prediction implementation precision.

### Runtime Treatment

`FORMAL DEFINITION REQUIRED`

Prototype technical specification 단계에서 정의 필요.

---

# 17. Validation Required

Reviewer는 Test Plan을 만들지 않는다.

## V-MCC-001

```text
Claim:
Kaiju autonomy is predictable but not directly controllable.

Suggested Evidence Type:
HYBRID
```

## V-MCC-002

```text
Claim:
Route changes force meaningful replanning rather than trivial re-routing.

Suggested Evidence Type:
HUMAN TEST
```

## V-MCC-003

```text
Claim:
ETA / collision information changes player commands.

Suggested Evidence Type:
HUMAN TEST
```

## V-MCC-004

```text
Claim:
Turret / barrier / lure create distinct intervention roles.

Suggested Evidence Type:
HUMAN TEST
```

## V-MCC-005

```text
Claim:
Real-time with Pause creates judgment pressure rather than a static answer-entry puzzle.

Suggested Evidence Type:
HUMAN TEST
```

Detailed Validation Design:

`DEFERRED`

---

# 18. Supported Structures

## SS-MCC-001 — Asymmetric Control Doctrine

### Structure

> 시민에게는 경로를 명령하고, 빌런에게는 환경을 제시한다.

### Supported By

- UC004 response agency
- Simulation autonomy specialization
- Strategy indirect response structure

### Why It Works

Player responsibility boundary가 선명하다.

괴수 직접제어와 완전 비개입 사이의 고유한 interaction identity를 만든다.

### Product Promise Protected

- indirect control
- predictable autonomy

### Do Not Accidentally Remove

괴수에게 direct movement command를 추가해 solve하지 않는다.

### Validation Still Needed

`YES`

---

## SS-MCC-002 — Risk-first Prototype Cut

### Structure

Prototype excludes:
- economy
- city development
- information team
- full hero combat

and uses:
- 2D debug map
- Kaiju A first
- limited citizen groups
- fixed core facilities

### Supported By

`SC-SOLO-001`

### Why It Works

가장 위험한 core claim을 product breadth보다 먼저 검증한다.

### Do Not Accidentally Remove

Visual polish / campaign systems를 Prototype PASS 전 필수 범위로 올리지 않는다.

---

## SS-MCC-003 — One Route Data Source

### Structure

```text
Path calculation data
=
Movement reference
=
Route overlay input
```

### Why It Works

Player-facing prediction과 actual simulation 사이 mismatch를 줄인다.

### Product Promise Protected

- readable planning
- ETA trust
- predictable autonomy

### Do Not Accidentally Remove

visual route를 gameplay route와 별도 handcrafted logic로 분리하지 않는다.

---

## SS-MCC-004 — Common Kaiju Grammar

### Structure

- Primary Objective
- Temporary Target
- Attraction
- Avoidance
- Reaction
- Ability
- MovementProfile

### Supported By

- SC-SOLO-003
- GC-SIM-005

### Why It Works

Kaiju A/B 차이를 unique AI code보다 data/rule interaction으로 만들 수 있다.

### Do Not Accidentally Remove

각 괴수마다 독립 AI architecture로 분기하지 않는다.

---

## SS-MCC-005 — Citizen Group Abstraction

### Structure

시민은 individual NPC가 아니라 지역별 집단.

### Supported By

- GC-MGMT-014
- GC-SIM-001
- Management × Solo Routing Specialization

### Why It Works

Player Job Fantasy를:
- evacuation command
- route priority
- group safety

수준에 유지한다.

### Product Promise Protected

관제센터 fantasy.

### Do Not Accidentally Remove

개별 시민 micromanagement를 기본 control unit로 승격하지 않는다.

---

## SS-MCC-006 — City Management Scope Boundary

### Structure

도시경제는 관제조건을 바꾸는 전략층으로 제한.

### Why It Works

Full Product expansion이 Core Loop를 City Builder로 대체하는 위험을 명시적으로 막고 있다.

### Validation Still Needed

`LATER — Full Campaign Stage`

---

# 19. Evidence Boundary

1. **No playable prototype evidence**
   - 이번 Dry-run은 design document review다.

2. **No Human Experience evidence**
   - 재미
   - tension
   - readability
   - perceived autonomy
   - intervention identity
   는 검증되지 않았다.

3. **No AI Tester result**
   - route diversity
   - policy stability
   - collision rate
   - win rate
   를 생성하지 않았다.

4. **No Market / Selection Goal**
   - 현재 source에 명시적 sales / award target이 없으므로 PASS 9는 `N/A`.

5. **Narrative / Deduction / Action not loaded**
   - Theme adjacency만으로 Genre Core를 Load하지 않았다.

6. **Full Product progression is deferred**
   - UC006은 current Prototype Active Check가 아니다.

7. **Solo evidence applies**
   - Scale는 명확히 SOLO.
   - AI 사용을 추가 FTE로 취급하지 않았다.

---

# 20. Reviewer Verdict

## Project Verdict

`REVIEW_CLEAR_WITH_VALIDATION`

### Reason

현재 v0.5에서:

- Core Loop contradiction 없음
- direct control / indirect control responsibility가 명확함
- Prototype scope가 위험한 claim에 집중됨
- technical architecture가 route consistency를 의식함
- Full Product support layers가 Prototype에서 제외됨

따라서 Prototype 이전에 반드시 재설계해야 하는 확정적 Structural Failure는 발견되지 않았다.

그러나 MCC의 존재 이유와 직접 연결된 다음 Claim은 아직 Experience Evidence가 없다.

1. Predictable Autonomy
2. Replanning Loop Necessity
3. ETA / Collision Decision Utility
4. Intervention Role Differentiation
5. Real-time Pause tension

즉:

```text
Structure:
Reviewable / coherent

Core Experience:
Validation required
```

이다.

`REVIEW_CLEAR_WITH_VALIDATION`은 Prototype 제작 투자 승인이나 상업적 성공 판정이 아니다.

---

# 21. Source Trace

## Project Source

`Project_MCC_통합_기획정리_v0.5.md`

## Reviewer Runtime

`REVIEWER_RUNTIME_SPECIFICATION_v0.1_APPROVED.md`

## Universal / Studio

`Studio_OS_Evidence_Based_Core_Extraction_v0.4.md`

## Genre Router

`GENRE_CORE_MASTER_INDEX_v0.3.md`

## Scale Router

`SCALE_CORE_BASELINE_v0.2.md`

## Loaded Genre Baselines

- `STRATEGY_CORE_CANDIDATES_v0.1_APPROVED.md`
- `MANAGEMENT_CORE_CANDIDATES_v0.1.md`
- `SIMULATION_CORE_CANDIDATES_v0.1_APPROVED.md`

## Runtime Audit Snapshot

```text
Universal Applicable:
5

UC006:
CONDITIONAL / NOT ACTIVE IN CURRENT PROTOTYPE

Genre:
Strategy L3
Management L3
Simulation L2
Narrative L1
Others L0

Scale:
SOLO

Reviewer Questions:
33 → 13

Raw Findings:
15

Root Issues:
5

Final RF:
5

Duplicate RF:
0

Over-merged RF:
0

Validation Planner:
NOT INVOKED
```
