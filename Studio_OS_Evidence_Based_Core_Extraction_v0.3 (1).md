# Studio OS — Evidence-Based Studio Core Extraction v0.3

> Basis: `Evidence-Based Core Extraction Master Prompt v0.2`  
> Purpose: Studio OS의 신규 게임 기획 평가와 Validation 설계에 재사용 가능한 Evidence-Based Reviewer Knowledge Base  
> Status: `Provisional Extraction — GSC Canonical Sync`  
> Version Change: `v0.2 → v0.3`는 Genre × Scale Core 3개의 Canonical retirement sync만 반영한다.  
> No-change: Universal / Genre / Scale / Market / Selection / Validation Core status는 이번 version에서 변경하지 않는다.  
> Rule: 외부 Reference를 Core 근거로 사용하며, Studio 내부 프로젝트의 기획/리뷰는 Core 승격 근거에서 제외한다.

---

# 1. Executive Summary

이번 추출에서 **Provisional Core로 승격할 근거가 가장 강한 Pattern은 9개**다.

| ID | 핵심 Rule | 분류 | Confidence |
|---|---|---|---|
| UC-DESIGN-001 | **입력 수가 아니라 상충하는 결과가 Decision Depth를 만든다** | Universal | VERY HIGH |
| UC-DESIGN-002 | **반복성은 콘텐츠 양보다 Context가 기존 선택의 가치를 바꾸는가에 달린다** | Universal | HIGH |
| UC-DESIGN-003 | **한 시스템의 결과가 다음 시스템의 의사결정을 바꿀 때 Cohesion이 생긴다** | Universal | HIGH |
| UC-DESIGN-004 | **Uncertainty에는 준비·조작·복구 중 하나 이상의 Agency가 필요하다** | Universal | HIGH |
| UC-DESIGN-005 | **정보량보다 Actionability와 Learnability를 평가한다** | Universal | HIGH |
| SC-SOLO-001 | **Prototype은 완성작 축소판이 아니라 Project-killing Risk의 최소 실행형이어야 한다** | Scale | VERY HIGH |
| SC-SOLO-002 | **작은 화면·픽셀·카드는 작은 Scope의 증거가 아니다** | Scale | Not separately scored¹ |
| MC-001 | **Market은 Awareness→Conversion→Satisfaction→Long-tail Funnel로 분리한다** | Commercial | VERY HIGH |
| SEL-001 | **심사에서는 가장 강한 Core Grammar를 5~15분 내 증명하는 것이 반복적으로 유리하다** | Selection | HIGH |

¹ `SC-SOLO-002`의 Canonical Confidence는 기존 Source에서 별도 점수화되지 않았다. `SCALE_CORE_BASELINE_v0.2`의 **Integration Assessment = VERY HIGH**는 Canonical Confidence와 별개다.

중요한 분류 원칙:

- `Theme inside Player Verb`
- `Progression changes choice space`
- `5~15분 Demo`
- `Data-driven Content`

등은 중요하지만, 적용 범위가 더 좁거나 반례가 존재하므로 Universal Core로 과도하게 승격하지 않는다.

또한 이번 최초 추출에서는 **Validated Studio Core를 생성하지 않는다.** 외부 Evidence만으로는 원칙적으로 `Provisional Core`까지 승격한다.

---

# 2. Universal Design Core Candidates

## UC-DESIGN-001 — Consequence Density over Input Count

**Core Type:** Universal Design Core  
**Promotion:** `PROMOTE TO PROVISIONAL CORE`

### Pattern
서로 다른 장르에서 단순한 입력 구조라도 한 행동이 여러 상충 결과에 영향을 줄 때 의미 있는 판단이 발생한다.

### Context
- 경영
- 전략
- 선택형 게임
- 자동전투 / 간접조작
- UI 중심 게임

### Rule
> **게임의 Decision Depth를 버튼·카드·명령 종류의 수로 판단하지 않는다. 한 선택이 몇 개의 상충하는 현재/미래 결과를 만드는지 평가한다.**

### Mechanism
입력이 많아도 기대값이 한 축으로 환원되면 최적해만 찾게 된다. 반대로 하나의 단순한 선택이 자원, 미래 상태, 위험, 관계를 서로 다른 방향으로 움직이면 Opportunity Cost가 발생한다.

### Supporting Evidence
- `EVD-UC001-A — Reigns`: 이진 선택이 복수 국정 수치와 장기 결과에 연결됨.
- `EVD-UC001-B — Papers, Please`: 반복 입력이 경제·정치·도덕·시간 결과를 동시에 변경.
- `EVD-UC001-C — Loop Hero`: 위험과 보상을 같은 타일 배치 행동이 동시에 생성.

### Counter Evidence
입력 자체의 숙련이 Product Promise인 액션·리듬·정밀 플랫폼에서는 Input Complexity가 가치의 일부일 수 있다.

### Applies To
System / Decision 중심 게임 전반.

### Exceptions / Boundary
Motor Skill 자체가 고객 욕구인 장르.

### Observed Metric
공통적으로 정량 측정된 Universal Metric은 현재 Reference에서 부족하다.

### Candidate Metrics
**Machine-testable**
- Choice Concentration
- Action Usage Distribution
- Decision Candidates When Available
- 결과축별 State Delta

**Human Required**
- Self-reported Decision Tension

### Validation Method
Rule Simulation → AI Tester → Human Prototype Test.

### Confidence
**VERY HIGH**

### Reviewer Action
새 시스템을 검토할 때 다음을 묻는다.

> “이 입력은 기존 입력과 다른 **질문**을 만드는가?”

아니라면 삭제 / 통합을 우선 검토한다.

---

## UC-DESIGN-002 — Contextual Value Shift

**Promotion:** `PROMOTE TO PROVISIONAL CORE`

### Pattern
Replayability가 강한 시스템 게임에서는 동일한 Action / 카드가 항상 같은 가치가 아니라 현재 상황에 따라 가치가 바뀐다.

### Rule
> **반복 플레이를 약속하는 게임은 콘텐츠 수보다 Context 변화가 기존 선택의 우선순위를 실제로 바꾸는지를 평가한다.**

### Mechanism
적, 자원, 현재 Build, 경로, 시간, 이전 결과가 Action Value를 변화시키면 플레이어는 다시 판단해야 한다.

### Supporting Evidence
- Slay the Spire
- Against the Storm
- Papers, Please
- FTL

### Counter Evidence
Return of the Obra Dinn처럼 첫 플레이의 추론 밀도가 핵심인 게임은 Replayability가 낮아도 제품으로 성립한다.

### Boundary
**Replayability가 Product Promise일 때 적용.**

### Candidate Metrics
**Machine**
- Context별 Choice Rate
- Strategy Concentration by Phase
- Build Diversity
- Same Action Value / Usage Variance

**Hybrid**
- Perceived Variety
- Replay Intent

### Confidence
**HIGH**

### Reviewer Action
`적 30종 / 카드 200장 / 이벤트 500개`보다 먼저 다음을 요구한다.

> **“상황이 달라지면 기존 선택 중 무엇이 달라지는가?”**

---

## UC-DESIGN-003 — Consequence-to-Next-Decision Coupling

**Promotion:** `PROMOTE TO PROVISIONAL CORE`

### Pattern
강하게 결합된 시스템은 단순 Resource를 공유하는 것이 아니라 **이전 시스템의 결과가 다음 선택상태를 변경**한다.

### Rule
> **System A의 결과가 System B에서 플레이어가 하는 다음 판단을 바꾸지 않는다면 둘의 결합 필요성을 재검토한다.**

### Mechanism
`Combat 결과 → 부상 → 인력 부족 → 다음 Management 선택 변경`처럼 인과가 이어질 때 하나의 경험으로 인식된다.

### Supporting Evidence
- Darkest Dungeon
- FTL
- 80 Days

### Counter Evidence
State coupling이 너무 많아지면 Snowball, 복구 피로, QA 폭증이 발생할 수 있다.

### Candidate Metrics
- Cross-System Plan Change Rate
- Persistent Consequence Duration
- State Transition Frequency
- Recovery Usage

### Validation Method
Machine + Human Hybrid.

### Confidence
**HIGH**

---

## UC-DESIGN-004 — Uncertainty Requires Response Agency

**Promotion:** `PROMOTE TO PROVISIONAL CORE`

### Pattern
RNG / 불확실성이 핵심인 사례에서 좋은 구조는 Randomness 자체를 제거하지 않고 플레이어가 준비, 변환, 회피, 복구할 수 있도록 한다.

### Rule
> **중요한 결과가 RNG에 의해 결정될수록 플레이어에게 최소 하나 이상의 의미 있는 대응 경로가 필요하다.**

### Supporting Evidence
- Dicey Dungeons
- FTL
- Slay the Spire

### Counter Evidence
Party / Chaos 장르처럼 결과의 예측불가능성 자체가 즐거움인 경우에는 약화된다.

### Candidate Metrics
**Machine**
- Uncontrollable Failure Rate
- Recovery Option Usage
- RNG-triggered Plan Change
- State Recovery Rate

**Human**
- Perceived Fairness

### Confidence
**HIGH**

---

## UC-DESIGN-005 — Actionable Information, not Maximum Information

**Promotion:** `PROMOTE TO PROVISIONAL CORE`

### Pattern
완전정보와 불완전정보 모두 성공 사례가 존재하지만 공통적으로 플레이어는 **의도한 판단을 수행하고 실패 원인을 학습할 수 있을 만큼의 정보**를 받는다.

### Rule
> **정보 구조는 공개량이 아니라 ‘의도한 판단을 할 수 있는가’와 ‘실패 원인을 학습할 수 있는가’를 기준으로 평가한다.**

### Mechanism
정보가 부족하면 Guessing이 되고, 너무 완전하면 특정 장르에서는 Optimization Puzzle이 될 수 있다.

### Supporting Evidence
- Into the Breach
- Reigns
- Mini Metro

### Counter Evidence
Into the Breach식 완전정보를 다른 장르에 기계적으로 이식하면 심리전·예측·즉흥성이 줄어들 수 있다.

### Candidate Metrics
**Machine**
- Information Usage Rate
- State Check → Action Change
- Decision Latency

**Human**
- Failure Cause Explanation Rate
- Rule Understanding
- Perceived Fairness

### Confidence
**HIGH**

---

## UC-DESIGN-006 — Progression Should Alter Decisions

**Promotion:** `KEEP AS CANDIDATE`

### Rule Candidate
> 성장 후 플레이어가 같은 선택을 더 강하게 수행하는 것만이 아니라, **다른 판단을 할 수 있게 되는가**를 별도로 평가한다.

### Supporting Evidence
- Slay the Spire
- Papers, Please
- Against the Storm

### Counter Evidence
Vampire Survivors처럼 Vertical Power Growth 자체가 핵심 보상인 게임도 충분히 성립한다.

### Candidate Metrics
- New Action Unlock Rate
- Progression 전후 Choice Distribution
- New Build Emergence
- Upgrade Concentration

### Confidence
**MEDIUM-HIGH**

현재 Universal Provisional Core까지는 올리지 않는다.

---

# 3. Genre Core Candidates

## Deckbuilding

### GC-DECK-001 — Contextual Card Value

**Promotion:** `PROVISIONAL CORE`

> **카드 Power는 단독 수치가 아니라 현재 덱·적·경로·다음 보상과 함께 평가한다.**

### Supporting Evidence
- Slay the Spire
- Balatro
- Dicey Dungeons

### Observed Metrics
- 카드 선택률
- 카드 승률

### Candidate Metrics
- Pick Rate
- Win Rate conditional on pick
- Dead Pick Rate
- Build별 카드 Usage
- Top-card Concentration

### Validation
AI Tester + Human.

### Confidence
**VERY HIGH**

---

### GC-DECK-002 — Build Identity Requires Both Commitment and Pivot

**Promotion:** `KEEP AS CANDIDATE`

빌드가 존재하려면 특정 조합을 선택할 이유가 있어야 하지만, 초반 선택 하나가 Run 전체를 강제로 결정해서도 안 된다.

### Candidate Metrics
- Early Choice → Final Build Correlation
- Build Pivot Frequency
- Pivot Survival / Success
- Locked-build Rate

### Confidence
**MEDIUM**

추가 Deckbuilder Postmortem Evidence가 필요하다.

---

### GC-DECK-003 — RNG Control is Part of Deckbuilding Agency

**Promotion:** `PROVISIONAL CORE`

`UC-DESIGN-004`의 Deckbuilding 특수 적용.

> Draw RNG가 존재하면 덱 압축, Draw, Discard, Selection, Retain 등 **확률구조를 조작할 Player Verb**의 존재를 검토한다.

---

## Management / Simulation

### GC-MGMT-001 — Management Depth Comes from Priority Conflict

**Promotion:** `PROVISIONAL CORE`

> **관리 대상 수보다 동시에 해결할 수 없는 문제의 충돌이 중요하다.**

### Supporting Evidence
- Papers, Please
- Frostpunk
- Darkest Dungeon
- This War of Mine

### Candidate Metrics
- Concurrent Critical Problems
- Priority Switching Rate
- Resource Starvation
- Action Concentration

### Confidence
**HIGH**

---

### GC-MGMT-002 — Loss Needs Recovery Structure

**Promotion:** `PROVISIONAL CORE`

> 장기 상태 손실을 사용할 때는 복구·대체·철수·우회 중 하나 이상의 선택이 존재해야 한다.

### Candidate Metrics
**Machine**
- Recovery Usage
- Unrecoverable State Rate
- Snowball Rate

**Human**
- Perceived Hopelessness
- Perceived Fairness

---

### GC-MGMT-003 — Automation Should Remove Execution, not Decisions

**Promotion:** `KEEP AS CANDIDATE`

Loop Hero 등에서 자동화가 조작부담을 줄이고 전략판단을 남기는 패턴이 존재한다. 추가 자동전투 / Management Reference가 확보되면 강한 Genre Core 후보가 될 수 있다.

---

## Roguelike / Roguelite

### GC-ROGUE-001 — Meta Progression Cannot Rescue a Weak Reset Loop

**Promotion:** `PROVISIONAL CORE`

> Meta Upgrade를 제거해도 기본 Run을 다시 시작하고 싶은 이유가 있는지 먼저 검증한다.

### Candidate Metrics
**Hybrid**
- No-Meta Replay Intent
- Reset → Restart Rate
- Repeat Loop Completion
- Session Fatigue

---

### GC-ROGUE-002 — Player-created Risk is Stronger than Passive Difficulty when the Game Promises Risk Management

**Promotion:** `KEEP AS CANDIDATE`

Loop Hero처럼 더 많은 보상을 위해 스스로 위험을 생성하는 구조는 강한 Risk / Reward를 만들 수 있다. 다만 독립 사례가 더 필요하다.

---

## Deduction / Information

### GC-DEDUCT-001 — The Game Should Manage Evidence, not Solve the Inference

**Promotion:** `PROVISIONAL CORE`

> **추리 UI는 검색·기억 비용을 줄이되 결론을 대신 만들어서는 안 된다.**

### Human Metrics
- Clue Recall
- Inference Explanation
- Hint Dependency
- External Note Dependency

### Confidence
**HIGH**

---

### GC-DEDUCT-002 — Low Replayability is not automatically a defect

**Promotion:** `PROVISIONAL CORE`

정답 지식이 상품을 소비하는 구조에서는 첫 플레이의 정보 밀도가 더 중요할 수 있다.

---

## Narrative / Systemic Narrative

### GC-NARR-001 — Recontextualization over Branch Count

**Promotion:** `PROVISIONAL CORE`

> 분기 수를 늘리기보다 동일 사건이 Player State 때문에 다른 의미를 갖도록 만드는 편이 시스템 내러티브와 Scope 양쪽에서 효율적일 수 있다.

### Supporting Evidence
- Papers, Please
- 80 Days
- This War of Mine

### Boundary
순수 Visual Novel처럼 Authored Narrative 자체가 상품이면 약화된다.

---

# 4. Scale Core Candidates

현재 Reference Pool은 Solo / Micro에 강하고 Small / Mid-size 비교 데이터는 부족하다.

## Solo

### SC-SOLO-001 — Risk-first Prototype

**Promotion:** `PROVISIONAL CORE — VERY HIGH`

> **Prototype은 Final Game의 작은 버전이 아니라 가장 위험한 Design Claim을 실행할 최소 모델이어야 한다.**

### Supporting Evidence
- Buckshot Roulette
- Thronefall
- Layer 3 공통 Production Rule

### Candidate Metrics
- Time to Testable Core
- Prototype Feature Count
- Core Risk Coverage / Dev-day
- Nonessential Feature Ratio

---

### SC-SOLO-002 — Visible Scope ≠ Production Scope

**Promotion:** `PROVISIONAL CORE`

> **Scope를 Unique Assets + Hand-authored Content + Logic Dependencies + State Combinations + Balance/QA + UI + Localization + Tooling으로 분해한다.**

### Candidate Metrics
- Unique Asset Count
- Authored Content Units
- State Combination Estimate
- Regression Test Matrix
- Localization Words
- UI Screen / State Count

---

### SC-SOLO-003 — Common Grammar is a Content Multiplier

**Promotion:** `PROVISIONAL CORE`

> **신규 콘텐츠가 새 코드·화면·조작보다 기존 Grammar의 Data 추가로 만들어질수록 Solo 제작효율이 높다.**

### Boundary
Balance / QA 비용은 별도로 증가할 수 있다.

---

### SC-SOLO-004 — Never Copy Post-success Scope

**Promotion:** `PROVISIONAL CORE`

> **Reference의 현재 콘텐츠 규모보다 최초 Prototype / 최초 상용 Scope를 비교한다.**

성공 이후 추가된 캐릭터·카드·모드·업데이트를 초기 제작 기준으로 사용하지 않는다.

---

## Micro Team

### SC-MICRO-001 — Reuse still matters, but Parallel Capacity changes the cut line

**Promotion:** `KEEP AS CANDIDATE`

2~5명 팀은 Art / Code / Content 병렬화가 가능하지만 현재 자료는 “몇 명이면 어떤 Scope가 안전한가”를 정량 비교하기 부족하다.

**Confidence:** LOW-MEDIUM.

---

## Small / Mid-sized+

현재 **Core 승격 보류**.

현재 Reference Library 구성으로는 충분한 근거가 없다.

---

# 5. Genre × Scale Historical Registry

## Canonical Layer State

```text
Active Independent GSC:
NONE

GSC Candidate:
NONE

Retired Historical GSC:
3
```

`RETIRED_AS_INDEPENDENT_GSC`는 Rule이 틀렸다는 뜻이 아니다.

의미:

> 별도 Genre × Scale Core로 로드할 필요가 없으며, 동일 Reviewer Decision은 Parent Genre + Parent Scale + Scale Handoff에서 생성한다.

---

## GSC-DECK-SOLO-001 — Interaction QA Budget before Card Count

**Former Status:** `PROVISIONAL CORE`  
**Canonical Status:** `RETIRED_AS_INDEPENDENT_GSC`

### Parent Route

Genre:
- `GC-DECK-004`
- `GC-DECK-005`

Scale:
- `SC-SOLO-002`
- `SC-SOLO-003`

Handoff:
- `SCALE_HANDOFF-DECK-001`
- `SCALE_HANDOFF-DECK-002`

### Preserved Reviewer Meaning

> Raw Card Count보다 Interaction / Regression Matrix를 먼저 본다.

### Runtime Behavior

- Active Core Load 금지
- 별도 Issue / Severity 생성 금지
- Historical Trace / Reviewer wording만 허용

### Retirement Basis

`GENRE_SCALE_CORE_INTEGRATION_v0.1_APPROVED`의 Reduction / Reviewer Difference Test에서 Parent + Handoff로 완전 환원 가능 판정.

---

## GSC-MGMT-SOLO-001 — Simulate the Player’s Job, not the Whole World

**Former Status:** `PROVISIONAL CORE`  
**Canonical Status:** `RETIRED_AS_INDEPENDENT_GSC`

### Parent Route

Genre:
- `GC-MGMT-014`
- relevant Management responsibility / priority rules

Conditional Genre:
- `GC-SIM-001` — Simulation이 실제 routed된 프로젝트에서만

Scale:
- `SC-SOLO-002`
- 필요 시 `SC-SOLO-003`

Handoff:
- `SCALE_HANDOFF-MGMT-001`
- `SCALE_HANDOFF-MGMT-002`
- 필요 시 `SCALE_HANDOFF-MGMT-003`

### Preserved Reviewer Meaning

> `Player Responsibility Level as Scope Cut Boundary`

이 표현은 Core가 아니라 `ROUTING SPECIALIZATION / REVIEWER ACTION HINT`로 보존한다.

### Runtime Behavior

- Active GSC Load 금지
- Management + Solo에서 Parent/Handoff가 활성화될 때 Reviewer Hint로만 사용
- Simulation Parent는 실제 Simulation routing 시에만 추가

### Retirement Basis

Genre / Scale / Handoff Parent만으로 동일 Scope Cut Decision에 도달 가능.

---

## GSC-DEDUCT-SOLO-001 — Few Screens can hide expensive authored logic

**Former Status:** `PROVISIONAL CORE`  
**Canonical Status:** `RETIRED_AS_INDEPENDENT_GSC`

### Parent Route

Genre:
- `GC-DEDUCT-003`
- `GC-DEDUCT-005`
- relevant authored relation findings

Scale:
- `SC-SOLO-002`

Handoff:
- `SCALE_HANDOFF-DEDUCT-001`
- `SCALE_HANDOFF-DEDUCT-002`
- `SCALE_HANDOFF-DEDUCT-003`
- `SCALE_HANDOFF-DEDUCT-005`

### Preserved Reviewer Meaning

> 적은 Screen / Scene 수가 낮은 Production Scope를 의미하지 않는다.

`SC-SOLO-002`의 Deduction Routing Example로 보존한다.

### Runtime Behavior

- Active / Diagnostic Core Load 금지
- Historical Trace / Parent mapping / wording만 허용

### Retirement Basis

`Visible Scope ≠ Production Scope` + Deduction Handoff로 동일 Reviewer Action에 도달 가능.

---

## Reopening Gate

Retired GSC를 다시 활성화하려면 최소 다음이 모두 필요하다.

1. New Direct Evidence
2. Genre Counterfactual 통과
3. Scale Counterfactual 통과
4. Parent Reduction Test 실패
5. Reviewer Difference Test 통과
6. Decision Difference Test 통과
7. Scale-specific Validation Path

`표현이 유용하다`는 이유만으로 재활성화하지 않는다.

---

# 6. Market / Commercial Core Candidates

## MC-001 — Commercial Funnel Separation

**Promotion:** `PROVISIONAL CORE — VERY HIGH`

### Pattern
Hook, Wishlist, Sales, Refund, Review 사이에는 자동적인 연결이 없다.

### Rule
> **Audience → Awareness → Interest/Wishlist → Purchase → Refund/Satisfaction → Long-tail을 독립 Gate로 평가한다.**

### Observed Metrics
- Sales
- Wishlist
- Refund
- Review
- Price
- Development Time

### Candidate Metrics
- Demo → Wishlist Conversion
- Wishlist → Purchase Conversion
- Retained Purchase Conversion
- Refund-adjusted Sales
- Creator Exposure Contribution

### Validation
Market Test / Sales Data.

---

## MC-002 — Sales Milestone ≠ ROI

**Promotion:** `PROVISIONAL CORE`

### Rule
> **판매량은 Team × Development Months × Cash Cost × Marketing/Publisher Support와 함께 해석한다.**

### Candidate Metrics
- Dev-months / 10K retained copies
- Break-even Copies
- Failure Cost
- Opportunity Cost Months

---

## MC-003 — Downside Compatibility before Breakout Upside

**Promotion:** `PROVISIONAL CORE`

> **100K가 가능한가보다 10K 이하에서도 이 프로젝트 투입이 감당 가능한가를 먼저 본다.**

---

## MC-004 — High Satisfaction ≠ Large Audience

**Promotion:** `PROVISIONAL CORE`

> **Review Quality와 Addressable Audience Size를 별도 평가한다.**

---

# 7. Selection / Award / Exhibition Core Candidates

## SEL-001 — Core Grammar must be demonstrable quickly

**Promotion:** `PROVISIONAL CORE`

### Rule
> **심사용 Demo는 Full Game 축소판보다 가장 강한 한 문장을 5~15분 안에 한 번 완결시키는 구조를 우선한다.**

### Candidate Metrics
- Time to Core Interaction
- Time to First Complete Core Loop
- One-sentence Recall Rate
- Demo Completion Rate

---

## SEL-002 — Theme should become an Interaction Hook

**Promotion:** `PROVISIONAL CORE — Selection only`

### Rule
> **심사에서 테마를 설명문으로 제시하지 말고 플레이어가 직접 수행하는 규칙으로 보여준다.**

---

## SEL-003 — Award Fit ≠ Market Fit

**Promotion:** `PROVISIONAL CORE — VERY HIGH`

Award는 다음의 Evidence로 사용할 수 있다.

- Hook
- Demo
- Execution
- Completion Credibility

하지만 **구매수요 Evidence가 아니다.**

---

# 8. Validation Core Candidates

## VAL-001 — Machine Structural Evidence ≠ Human Experience Evidence

**Promotion:** `PROVISIONAL CORE`

### Rule
Machine Evidence와 Human Experience Evidence를 분리한다.

#### Machine
- Choice Concentration
- Win Rate
- Economy Stability
- Dead End
- Strategy Distribution

#### Human
- Fun
- Fairness
- Fatigue
- Readability
- Fantasy Fulfillment

**Confidence:** VERY HIGH.

---

## VAL-002 — Metric, Criteria, Hypothesis를 분리한다

**Promotion:** `PROVISIONAL CORE`

- Hypothesis = Claim
- Metric = Measurement
- Criteria = PASS / FAIL Threshold

를 하나의 객체로 합치지 않는다.

---

## VAL-003 — Evidence accumulates across stages

**Promotion:** `PROVISIONAL CORE`

> `MACHINE_PRE → MACHINE_POST → HUMAN → EXTERNAL`

Evidence를 누적하고 Hypothesis Confidence를 업데이트한다.

Pre-Prototype Simulation PASS는 Game Core 또는 Human Fun의 최종 PASS가 아니다.

---

## VAL-004 — Pre-Prototype should eliminate structural failures before expensive human testing

**Promotion:** `PROVISIONAL CORE`

Machine으로 검증 가능한 구조적 문제를 먼저 제거하고 Human Playtest로 넘어간다.

### Boundary
Human Experience 자체를 Machine으로 사전 확정하지 않는다.

---

# 9. Anti-Patterns

## AP-001 — Feature Count as Depth

### Problem Structure
시스템 / 카드 / 입력 수 증가를 깊이로 간주.

### Observed Consequence
학습·QA 비용은 증가하지만 선택은 기존 질문을 반복할 수 있다.

### Mitigation
새 Feature마다 새 Decision Question을 요구한다.

### Detection Metrics
- Choice Concentration
- Feature Usage
- Redundant Function Mapping

---

## AP-002 — Punishment without Recovery

### Trigger
영구손실·RNG·부상 누적.

### Consequence
- Snowball
- Hopelessness
- Restart Optimality

### Mitigation
- Recovery
- Replacement
- Retreat
- Risk Avoidance

---

## AP-003 — Meta Progression as Core Loop Patch

### Trigger
반복 Core가 약한 상태에서 Unlock / Meta를 먼저 추가.

### Consequence
성장보상은 있지만 플레이 자체의 피로는 유지된다.

### Mitigation
No-Meta Core Test.

---

## AP-004 — Minimal Visuals = Cheap Production

### Consequence
UI / Logic / Balance / Text / QA가 숨은 비용으로 증가.

### Mitigation
Production Cost Axis로 Scope를 재계산한다.

---

## AP-005 — Perfect Information Transferred without Context

### Consequence
심리전 / 즉흥성이 필요한 게임이 Optimization Puzzle화.

### Mitigation
Product Decision Type부터 정의한다.

---

## AP-006 — Common Grammar without Learnability

### Consequence
높은 System Reuse에도 인지부하와 상태관리 피로 증가.

### Mitigation
- Progressive Disclosure
- Readability Test
- State Visibility 개선

---

## AP-007 — Award = Demand

### Consequence
지원 / 수상 후 시장검증 없이 Production 확대.

### Mitigation
`Award → Demo → Wishlist → Purchase` 별도 Gate.

---

## AP-008 — Wishlist = Sales

### Mitigation
Conversion + Refund + Satisfaction까지 함께 평가한다.

---

## AP-009 — Handcrafted Quantity as Variety

### Consequence
텍스트·장면·퀘스트는 늘지만 같은 판단이 반복되고 Localization / QA 비용이 증가.

### Mitigation
State-based Recontextualization 우선 검토.

---

## AP-010 — Final Hit Scope as Starting Scope

### Consequence
검증 전 대량 콘텐츠 투자.

### Mitigation
최초 Prototype / First Commercial Scope 기준으로 Reference를 비교한다.

---

# 10. Conflicting Findings

## CF-001 — Complete Information vs Hidden Information

### Evidence A
Into the Breach — 높은 정보공개가 전략성을 지원.

### Evidence B
심리 / 추론 게임 — 불완전정보가 핵심.

### Hidden Variable
> 플레이어가 해결해야 하는 문제가 **Optimization인가 Prediction인가?**

### Resolution
정보 공개량 자체를 Core로 만들지 않는다.

---

## CF-002 — High Replayability vs One-shot Completion

### Evidence A
Slay the Spire / Against the Storm.

### Evidence B
Return of the Obra Dinn.

### Hidden Variable
Product Promise.

### Resolution
Replayability는 Universal Quality Metric이 아니다.

---

## CF-003 — Data-driven vs Handcrafted Content

### Evidence A
Luck be a Landlord 계열 → Data reuse 효율.

### Evidence B
Golden Idol / Obra Dinn / 80 Days 계열 → 고유 제작 콘텐츠가 핵심 상품가치.

### Resolution
`Handcrafted = bad`가 아니다.

> **제작비 증가가 Customer Value 증가와 연결되는가**

를 평가한다.

---

## CF-004 — Horizontal vs Vertical Progression

System-heavy 전략게임에서는 새 선택지의 가치가 크지만 Vampire Survivors류에서는 Vertical Power Fantasy 자체도 유효하다.

### Resolution
Progression 방식은 Player Motivation에 종속된다.

---

## CF-005 — Strong Hook vs Strong Satisfaction

Hook, Demand, Satisfaction은 서로 다른 Funnel 단계다.

### Resolution
강한 Hook와 높은 Satisfaction을 별도 평가한다.

---

# 11. Candidate / Hypothesis

## CAND-001 — Higher Decision Density increases Fun

**Confidence:** LOW

Strategy에서는 유력하지만 Relaxing / Exploration에는 반례 가능.

**Need:** Human Tests across genres.

---

## CAND-002 — Strong one-sentence Hook improves Wishlist Conversion

**Confidence:** MEDIUM-LOW

Award Evidence는 강하지만 Marketing Variables 통제 부족.

**Validation:** Capsule / Trailer A-B + Store Analytics.

---

## CAND-003 — Data-only Content Ratio predicts Scope Efficiency

**Confidence:** MEDIUM

Logic / QA 비용을 동시에 측정해야 한다.

---

## CAND-004 — Prototype-first reduces commercial failure

**Confidence:** LOW

Survivorship Bias가 큼.

---

## CAND-005 — Strategy Diversity predicts Replayability

**Confidence:** MEDIUM-LOW

Machine Diversity ≠ Human Desire to Replay.

---

## CAND-006 — Job Fantasy materially improves management-game conversion

국내 Award에서는 반복 Evidence가 있으나 실제 Sales Conversion 자료는 부족하다.

**Promotion:** Selection Candidate, not Market Core.

---

# 12. Evidence Gaps

## A. Human Behavior Telemetry

부족한 데이터:

- 실제 선택률
- 전략 변경률
- 온보딩 실패
- Fatigue
- Tutorial Completion

Reference는 Design Interpretation은 풍부하지만 Raw Player Behavior 데이터가 상대적으로 적다.

---

## B. Commercial Funnel Completeness

많은 사례에서:

- 판매량은 있지만 Wishlist 없음
- Wishlist는 있지만 Refund 없음
- 판매량은 있지만 제작비 없음

등으로 Funnel 전체가 연결되지 않는다.

---

## C. Team-scale Comparison

현재 Production Library가 Solo / Micro 중심이라:

- 6~15명
- 16명+

규모에서 Scope / Tooling / Communication Cost가 어떻게 바뀌는지 Core를 만들 근거가 부족하다.

---

## D. Prototype Failures

성공작이 어떤 Prototype을 사용했는지는 존재하지만, **프로토타입 이후 폐기된 프로젝트 모집단**이 부족하다.

---

## E. Long-tail

출시 직후보다 12~24개월 장기 데이터가 부족하다.

---

# 13. Additional Research Priorities

## P0 — Commercial Funnel Dataset

최우선 수집 필드:

`Team / Dev Months / Cash Budget / Price / Launch Wishlist / Demo Conversion / Launch Sales / Refund / Review / 12M Sales`

20~30개 수준의 일관된 사례가 확보되면 Market Core 신뢰도를 크게 올릴 수 있다.

---

## P0 — Prototype → Product Dataset

수집 항목:

- Prototype Duration
- What Hypothesis Was Tested
- Which Features Were Cut
- Time to Commercial Build
- Final Scope Difference

---

## P1 — Human Decision Dataset

필요 데이터:

- Plan Change Rate
- Rule Explanation Rate
- Choice Tension
- Replay Intent
- Fatigue
- Perceived Fairness

---

## P1 — Production Unit Cost

실제:

- 카드 1개
- 적 1개
- 이벤트 1개
- 추리 Scene 1개
- 일러스트 1개
- Animation 1개

당 Dev-hour 자료.

---

## P1 — Award Longitudinal Study

2024~2026 국내 수상작을:

`Award → Demo → Wishlist → Launch → Review / Sales`

로 지속 추적한다.

---

# 14. Promotion Recommendation

## Universal

| ID | 판정 |
|---|---|
| UC-DESIGN-001 Consequence Density > Input Count | **PROMOTE TO PROVISIONAL CORE** |
| UC-DESIGN-002 Contextual Value Shift | **PROMOTE TO PROVISIONAL CORE** |
| UC-DESIGN-003 Consequence-to-Next-Decision | **PROMOTE TO PROVISIONAL CORE** |
| UC-DESIGN-004 Uncertainty Response Agency | **PROMOTE TO PROVISIONAL CORE** |
| UC-DESIGN-005 Actionable Information | **PROMOTE TO PROVISIONAL CORE** |
| UC-DESIGN-006 Progression Alters Decision | **KEEP AS CANDIDATE** |

## Genre

| ID | 판정 |
|---|---|
| GC-DECK-001 Contextual Card Value | **PROVISIONAL CORE** |
| GC-DECK-002 Build Pivotability | **KEEP AS CANDIDATE** |
| GC-DECK-003 RNG Control | **PROVISIONAL CORE** |
| GC-MGMT-001 Priority Conflict | **PROVISIONAL CORE** |
| GC-MGMT-002 Recovery Structure | **PROVISIONAL CORE** |
| GC-MGMT-003 Automation Removes Execution | **KEEP AS CANDIDATE** |
| GC-ROGUE-001 Core before Meta | **PROVISIONAL CORE** |
| GC-DEDUCT-001 UI Supports Inference | **PROVISIONAL CORE** |
| GC-DEDUCT-002 Low Replay can be Valid | **PROVISIONAL CORE** |
| GC-NARR-001 Recontextualization > Branch Count | **PROVISIONAL CORE** |

## Scale / Genre × Scale

| ID | 판정 |
|---|---|
| SC-SOLO-001 Risk-first Prototype | **PROVISIONAL CORE** |
| SC-SOLO-002 Hidden Scope Cost | **PROVISIONAL CORE** |
| SC-SOLO-003 Common Grammar Multiplier | **PROVISIONAL CORE** |
| SC-SOLO-004 Do not copy Post-success Scope | **PROVISIONAL CORE** |
| SC-MICRO-001 Parallel Capacity | **KEEP AS CANDIDATE** |
| GSC-DECK-SOLO-001 Interaction QA Budget | **RETIRED_AS_INDEPENDENT_GSC** |
| GSC-MGMT-SOLO-001 Simulate Player Job | **RETIRED_AS_INDEPENDENT_GSC** |
| GSC-DEDUCT-SOLO-001 Hidden Logic Cost | **RETIRED_AS_INDEPENDENT_GSC** |

## Market / Selection / Validation

| ID | 판정 |
|---|---|
| MC-001 Funnel Separation | **PROVISIONAL CORE** |
| MC-002 Sales ≠ ROI | **PROVISIONAL CORE** |
| MC-003 Downside before Upside | **PROVISIONAL CORE** |
| MC-004 Satisfaction ≠ Audience | **PROVISIONAL CORE** |
| SEL-001 Fast Core Demonstration | **PROVISIONAL CORE** |
| SEL-002 Theme→Interaction | **PROVISIONAL CORE** |
| SEL-003 Award ≠ Market | **PROVISIONAL CORE** |
| VAL-001 Machine ≠ Human Experience | **PROVISIONAL CORE** |
| VAL-002 Hypothesis/Metric/Criteria Separation | **PROVISIONAL CORE** |
| VAL-003 Evidence Accumulation | **PROVISIONAL CORE** |
| VAL-004 Structural Pre-validation First | **PROVISIONAL CORE** |

---

# 15. Studio OS Reviewer 기본 Core Set

전체 Core를 모든 게임에 일괄 적용하지 않는다.

## 항상 확인할 Reviewer 기본 Core

1. `UC-DESIGN-001`
   - **각 시스템은 실제 다른 Decision을 만드는가?**

2. `UC-DESIGN-002`
   - **반복 시 Context가 Choice Value를 바꾸는가?**

3. `UC-DESIGN-003`
   - **시스템 결과가 다음 판단에 연결되는가?**

4. `UC-DESIGN-004`
   - **불확실성에 대응 Agency가 있는가?**

5. `UC-DESIGN-005`
   - **필요한 정보를 읽고 실패에서 학습할 수 있는가?**

6. `SC-SOLO-001`
   - **가장 위험한 가설을 가장 작은 Prototype으로 검증 가능한가?**

7. `SC-SOLO-002`
   - **보이지 않는 Production Cost는 무엇인가?**

8. `MC-001 / MC-003`
   - **시장 Funnel과 Downside Cost가 분리되어 있는가?**

## Contextual Core 호출 방식

- 장르에 따라 → `GC-*`
- 제작규모에 따라 → `SC-*`, `GSC-*`
- 지원 / 전시 목적 → `SEL-*`
- Validation 단계 → `VAL-*`

즉 Studio OS Reviewer Knowledge Base는:

> **모든 Core를 모든 게임에 적용하는 Checklist가 아니라, 현재 게임의 Context에 맞는 Rule을 선택적으로 호출하는 구조**

로 운용한다.

---

# 16. Final Position

이 Knowledge Base의 목적은 성공작의 공통 특징을 저장하는 것이 아니다.

향후 신규 게임 기획을 입력받았을 때 Studio OS가:

1. 어떤 Core를 적용해야 하는지 선택하고,
2. 어떤 위험을 우선 질문해야 하는지 판단하고,
3. 어떤 문제는 장르 특성인지 구분하고,
4. 어떤 문제는 제작 규모 위험인지 구분하고,
5. 어떤 부분은 시장 검증이 필요한지 구분하고,
6. 어떤 부분은 Prototype으로 검증해야 하는지 결정하고,
7. 어떤 부분은 AI Tester로 측정 가능한지 판단하고,
8. 어떤 부분은 Human Test가 필요한지 구분할 수 있게 하는 것

이 최종 목적이다.

원칙:

> **Reference → Evidence → Pattern → Core의 추적 관계를 유지한다.**

Core는 원본 Evidence를 대체하지 않는다.

Core는 원본 Evidence를 더 빠르고 일관되게 활용하기 위한 **압축된 Reviewer 판단 계층**이다.
