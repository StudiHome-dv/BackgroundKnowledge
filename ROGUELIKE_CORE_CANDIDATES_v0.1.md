# ROGUELIKE_CORE_CANDIDATES_v0.1

**Studio OS — Roguelike / Roguelite Genre Core Deep Extraction**  
**Document:** `ROGUELIKE_CORE_CANDIDATES_v0.1`  
**Status:** `APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE`  
**Purpose:** 신규 Roguelike / Roguelite / Roguelike Hybrid 기획 평가용 Genre-specific Reviewer Knowledge Base  
**Baseline:** `STUDIO_CORE_CANDIDATES_v0.2`  
**Extraction Prompt:** `Studio OS — Roguelike / Roguelite Genre Core Deep Extraction Prompt v0.1`  
**Provisional Genre Cores:** `GC-ROGUE-001`, `GC-ROGUE-003 ~ GC-ROGUE-005`  
**Candidates:** `GC-ROGUE-002`, `GC-ROGUE-006 ~ GC-ROGUE-013`  
**Pending:** `Additional Evidence / Prototype Validation / Internal Evidence`  
**Evidence Rule:** Primary Roguelike/Roguelite Evidence를 Provisional Core 승격의 중심 근거로 사용하며, Hybrid/Adjacent Evidence는 강화·반례·Boundary 설정에 사용한다.

---

# 1. Executive Summary

이번 Deep Extraction의 핵심 결론은 다음과 같다.

1. **Roguelike/Roguelite의 핵심은 Randomness나 Permadeath 자체가 아니라 `Reset 이후 다른 조건을 읽고 다시 Adapt하고 싶은가`다.**
   - Procedural Generation이 있어도 같은 전략을 반복하면 Run Variety가 아니다.
   - Reset이 있어도 다음 Unlock을 얻기 위해 억지로 반복한다면 Core Replayability의 증거가 아니다.

2. 기존 `GC-ROGUE-001 — Meta Progression Cannot Rescue a Weak Reset Loop`는 **STRENGTHEN / PROVISIONAL CORE 유지**가 맞다.
   - Against the Storm은 “초기 구축 자체가 반복해도 재미있어야 한다”는 강한 직접 Evidence를 제공한다.
   - Vampire Survivors, FTL, Slay the Spire도 Run 내부의 판단/성장/적응이 장기 해금과 별도로 작동한다.

3. 기존 `GC-ROGUE-002 — Player-created Risk`는 **REFRAME / KEEP AS CANDIDATE**가 적절하다.
   - Loop Hero뿐 아니라 Slay the Spire의 Elite 경로, Against the Storm의 Dangerous Glade, FTL의 위험 경로가 유사 Mechanism을 지지한다.
   - 다만 “Player-created Risk가 Passive Difficulty보다 더 강하다”는 비교 명제까지 외부 Evidence가 입증하지는 않는다.
   - 따라서 `Player-selectable Risk Must Create a Legible Trade-off`로 정밀화하되 Candidate를 유지한다.

4. 신규 Provisional Roguelike Core로 가장 강한 것은 다음 세 축이다.
   - `GC-ROGUE-003 — Meaningful Run Variation Must Force Adaptation`
   - `GC-ROGUE-004 — Run Choices Must Create Path Dependence`
   - `GC-ROGUE-005 — Escalation Must Preserve Decisions`

5. `Failure Learning`, `Restart Friction`, `Early-run Autopilot`, `Late-run Autopilot`, `Meta Type`, `Unlock Dilution`, `Run Length`, `Difficulty Scaling`은 매우 중요한 축이지만 현재 Reference에서 직접 Telemetry 또는 독립 Primary Evidence가 부족해 Candidate로 유지한다.

6. Roguelike의 반복 Anti-Pattern은:
   - Meta Progression as Bribe
   - Randomness without Adaptation
   - Content Count = Replayability
   - Fixed Opening Autopilot
   - Early RNG Locks the Run
   - No Commitment / Identityless Run
   - Unrecoverable Bad Seed
   - Failure without Learning
   - Long Run / Low Decision Density
   - Late-run Autopilot
   - Meta Power Hides Balance Problems
   - Unlock Dilution
   - Fake Variation
   - Difficulty as Numeric Inflation
   - Restart Friction

7. AI Tester와 특히 궁합이 좋은 장르다.
   - Seed별 결과
   - Strategy Concentration
   - Build / Route Divergence
   - Risk Selection
   - Recovery Usage
   - Meta Dependency
   - Early / Late Autopilot
   를 대량 Run으로 측정할 수 있다.

8. 그러나 AI Tester가 직접 판단하지 않는 것은:
   - 다시 하고 싶은가
   - 실패가 공정한가
   - Run이 신선한가
   - Build가 만족스러운가
   - Meta가 동기부여되는가
   - 실패가 허무한가
   이다.

9. Roguelike Reviewer의 가장 중요한 질문은 다음과 같다.

> **“Run이 Reset되었을 때 플레이어가 같은 공략을 다시 실행하는가, 아니면 새 조건을 읽고 이전 선택·실패에서 얻은 가설을 수정해 다른 Run을 만들어야 하는가?”**

10. 현재 Evidence Gap 중 가장 큰 것은:
   - Reset → Restart 실제 행동 Telemetry
   - No-meta Replay Behavior
   - Failure Attribution / Learning
   - Seed별 Outcome Variance
   - Bad Seed / Unrecoverable State
   - Early-run Autopilot
   - Late-run Decision Collapse
   - Meta Dependency
   - Unlock Dilution
   - Underperforming Roguelike Control Cases

---

# 2. Roguelike / Roguelite Genre Definition

Studio OS에서는 역사적 장르 정의 논쟁보다 **Run 반복 구조의 설계 기능**을 평가한다.

## 2.1 Inclusion Test

Primary Roguelike/Roguelite Evidence로 분류하기 전에 다음을 확인한다.

### A. Run Boundary
명확한 Run / Session의 시작과 종료가 존재하는가?

### B. Reset
Run 종료 후 일부 또는 대부분의 Run State가 초기화되는가?

### C. Run Variation
새 Run에서 이전 해답을 그대로 복사하기 어렵게 만드는 변화가 존재하는가?

가능한 변화:
- Map
- Encounter
- Reward
- Enemy
- Resource
- Build Option
- Starting Condition
- Character
- Rule Modifier

### D. Adaptation
변화가 단순 장식이 아니라 계획 수정이나 선택 변화로 이어지는가?

### E. Commitment
Run 중 선택이 이후 Choice Space나 전략 가치에 영향을 주는가?

### F. Failure / Completion Learning
Run 종료 후:

> “다음 Run에서는 무엇을 다르게 할 것인가?”

를 설명할 수 있는가?

### G. Restart Motivation
Reset이 단순 벌점이 아니라:
- 다른 조건
- 다른 Build
- 다른 Route
- 새로운 전략 가설
- 개선된 실행

을 다시 시험할 기회가 되는가?

---

## 2.2 Studio OS Roguelike Core Loop

```text
Run Start
    ↓
Variable Context
    ↓
Observe / Choose
    ↓
Commit Resources / Build / Route
    ↓
Encounter Consequence
    ↓
Adapt
    ↓
Escalating Risk / Opportunity
    ↓
Run Success / Failure / Exit
    ↓
Learn / Unlock / Reset
    ↓
Restart
```

다음 구조만으로 강한 Roguelike Evidence로 인정하지 않는다.

```text
Random Stage
↓
Power 증가
↓
죽음
↓
Permanent Stat +5%
↓
다시 반복
```

---

# 3. Source Classification

# 3.1 Tier A — Primary Roguelike / Roguelite Evidence

## REF-02 — FTL: Faster Than Light

**Subtype:** Systemic Strategy Roguelike  
**Evidence Strength:** VERY HIGH — Adaptation / Route / Failure / RNG Response

강한 Evidence 영역:
- Run Adaptation
- Route Choice
- Resource Scarcity
- Persistent Run Damage
- RNG Response Agency
- Failure
- System Interaction
- Long-run Failure Cost
- Unlock as horizontal long-term goal

핵심 관찰:
같은 전투 규칙이 적 함선, 화재, 승무원, 자원 부족과 결합해 매번 다른 위기를 만들고, RNG는 준비·경로·복구 선택이 있을 때 의미를 가진다.

Run 안에서는 함선과 시스템이 수직 성장하고, 함선 해금은 수평 장기 목표다. 핵심 재미는 주어진 재료로 적응형 빌드를 만드는 것이다.

---

## REF-04 — Slay the Spire

**Subtype:** Combat Deckbuilding Roguelike  
**Evidence Strength:** VERY HIGH — Run Choice / Route / Risk / Metrics

강한 Evidence 영역:
- Run Build Formation
- Route Choice
- Optional Elite Risk
- Run Variety
- Encounter Pressure
- Ascension
- Decision Metrics

Deckbuilding Core의:
- Contextual Card Value
- Pool Quality
- Build Identity

는 복제하지 않는다.

Roguelike Evidence로 사용하는 부분:
- 매 Run 같은 완성 덱을 복제하기 어렵다.
- 경로 / Elite / 보상 / 유물 변화가 Run 전략을 바꾼다.
- HP가 Run 전체의 위험 예산으로 작동한다.
- Ascension이 규칙 변화로 숙련자를 재시험한다.

---

## REF-07 — Against the Storm

**Subtype:** Roguelite Management  
**Evidence Strength:** VERY HIGH — Reset / Adaptation / Core Before Meta

강한 Evidence 영역:
- Short Settlement
- Session Reset
- Variable Inputs
- Adaptive Planning
- Meta Progression
- Run-specific Scarcity
- Systemic Content Reuse

핵심 관찰:
경영의 초기 구축 구간을 반복 Run으로 추출하고, 매번 모든 도구를 주지 않아 완성 공략 복제를 어렵게 한다.

가장 중요한 Warning:

> 로그라이트 Meta만 붙인다고 후반 정체가 해결되지는 않으며, 초기 구축 자체가 반복해도 재미있어야 한다.

---

## REF-20 — Dicey Dungeons

**Subtype:** Compact Rule-Variant Roguelike / Deckbuilding Hybrid  
**Evidence Strength:** HIGH — Visible RNG / Adaptation / Rule Variation

강한 Evidence 영역:
- Visible RNG
- RNG Manipulation
- Character Rule Variants
- Compact Combat
- Episode Rule Variation
- Given Input → Adaptive Response

핵심 관찰:
매 턴 주어진 입력은 달라지지만 현재 도구로 그 입력을 어떻게 처리할지가 반복 판단이 된다.

---

## REF-12 — Vampire Survivors

**Subtype:** Survivors-like Action Roguelite  
**Evidence Strength:** HIGH — Reward Loop / Build / Run Escalation / Meta

강한 Evidence 영역:
- Short Session
- Build Evolution
- High Reward Frequency
- Time-based Escalation
- Vertical Run Power
- Permanent Unlock
- Low Restart Burden

핵심 관찰:
자동 공격과 단순 이동만으로 작동하는 것이 아니라, 위치·빌드·성장 판단이 지속적으로 남기 때문에 반복 Run이 작동한다.

실패 원인은 주로:
- 화력 성장 속도
- 위치 판단

에 연결되며, 짧은 Session과 빠른 성장으로 Restart 부담이 낮다.

---

# 3.2 Tier B — Roguelike Hybrid / Secondary Evidence

## REF-18 — Loop Hero

**Use**
- Player-created Risk
- Continue / Retreat
- Run Escalation
- Auto / Indirect Control
- Self-authored Difficulty
- Reward and Risk in the same action

중요한 Evidence지만 Library상 Secondary이고 구조가 독특하므로 전체 Roguelike Core를 단독 지지하지 않는다.

---

## REF-27 — Tiny Rogues

**Classification Decision:** `TIER B / PRODUCTION-HEAVY SUPPORT`

초기 Prompt에서는 Tier A 후보였으나 현재 Studio Reference는:
- Solo production
- Scope fight
- item/enemy content volume

중심이다.

따라서:
- Compact Run
- Build
- Meta
에 대한 직접 Design Evidence가 충분하지 않아 Primary 승격하지 않는다.

---

## REF-34 — Peglin

**Classification:** `TIER B / PRODUCTION-HEAVY SUPPORT`

Use:
- Run Build
- Hybrid Mechanic
- Prototype → Expansion
- Data / Meta expansion

현재 Reference는 Production Case 중심이므로 세부 Run Design Core의 Evidence Weight를 낮춘다.

---

## REF-36 — Brotato

**Classification:** `TIER B / PRODUCTION-HEAVY SUPPORT`

Use:
- Short Run Build
- Reward Selection
- Character Rule Variation
- Wave Escalation
- Unlock

현재 Production Evidence 비중이 높다.

---

## REF-06 — Darkest Dungeon

**Use**
- Failure
- Long-term Loss
- Recovery
- Risk Management

Campaign / Roster 구조가 강하므로 pure Run Roguelike Evidence로 과대 적용하지 않는다.

---

# 3.3 Tier C — Adjacent / Control Evidence

필요한 Mechanism에만 사용:
- Into the Breach
- Balatro
- Luck be a Landlord
- Dome Keeper
- SNKRX
- Patch Quest
- Thronefall

Tier C만으로 Provisional Roguelike Core를 승격하지 않는다.

---

# 3.4 Source Limitation

현재 Reference Pool은 성공작과 강한 사례가 중심이다.

특히 부족한 Control:
- Meta grind가 Core 약점을 가린 실패 사례
- Seed variance가 플레이어 이탈을 만든 사례
- Early-run repetition이 심한 사례
- Unlock pool dilution 사례
- Long-run failure fatigue 사례

따라서 일부 Anti-Pattern은:
- 성공작의 Warning
- 구조적 Mechanism
- Adjacent Evidence

에서 추출된 Candidate Risk다.

---

# 4. Existing Core Audit

# GC-ROGUE-001 — Meta Progression Cannot Rescue a Weak Reset Loop

**Decision:** `STRENGTHEN`  
**Status:** `PROVISIONAL CORE`  
**Origin:** `EXISTING GC REFINEMENT`

## Refined Pattern

강한 Roguelike/Roguelite 사례에서는 Meta가 Run을 반복시키는 유일한 이유가 아니라:
- Run 자체의 적응
- 새 Build
- 새 Route
- 실행 개선
- 조건 재해석

위에 장기 목표를 추가한다.

## Rule

> **Meta Progression을 고정하거나 제거한 상태에서도 Reset 후 다시 시험하고 싶은 Core Run 이유가 존재해야 한다. Meta는 Core Restart Motivation을 보완할 수 있지만 대체할 수 없다.**

## Mechanism

나쁜 구조:

```text
Run 자체는 동일하고 지루함
→ 실패
→ +5% 영구 성장
→ 숫자로 다음 구간 통과
→ 더 큰 +%를 위해 반복
```

이 경우 Reset은 새로운 문제를 제공하지 않고 Grind Gate가 된다.

좋은 구조:

```text
Run Failure
→ 다른 조건 / 전략 가설
→ 다시 Run
+
장기 Unlock / Meta
```

Meta는 새로운 Run을 보강하지만 Core Loop를 대신하지 않는다.

## Primary Evidence

### Against the Storm
가장 직접적이다.

- 경영의 초기 구축 자체를 반복 Run으로 만든다.
- 모든 도구를 주지 않아 적응을 요구한다.
- 짧은 정착과 장기 Meta를 분리한다.
- “Meta만 붙인다고 후반 정체가 해결되지 않는다. 초기 구축 자체가 반복해도 재미있어야 한다”는 Warning이 명시된다.

### Vampire Survivors
- Run 내부에서 위치·빌드·성장 선택이 지속된다.
- Run 밖 영구 해금과 옵션 확장이 존재하지만, 자동 공격과 Meta만으로는 작동하지 않는다고 Warning한다.

### FTL
- 한 Run에서 주어진 시스템·승무원·경로에 적응하는 것이 핵심이다.
- 함선 해금은 수평적 장기 목표다.

## Counter Evidence

Vertical Meta Power 자체가 핵심 Motivation인 Roguelite도 존재한다.

따라서:
- Permanent Stat = bad
- Horizontal Unlock = always better

로 일반화하지 않는다.

## Applies To

- Roguelite Management
- Action Roguelite
- Strategy Roguelike
- Survivors-like
- Hybrid Roguelite

## Boundary

짧은 Arcade Run에서 Meta 성장 자체가 명확한 Product Fantasy라면 Core 반복과 Meta의 비중이 달라질 수 있다.

## Observed Metric

현재 Reference에는 `No-meta Restart Rate` 같은 공통 Telemetry가 없다.

## Candidate Metric — Machine

- Win Rate by Meta Level
- Run Length by Meta Level
- Permanent Power Contribution
- Unlock Usage Rate
- Strategy Diversity by Meta Level

## Candidate Metric — Human / Hybrid

- Restart Motivation
- Meta Motivation
- No-meta Replay Intent
- “다음 Run 이유” 분류
- Meta Dependency Experience

## Validation Type

Hybrid.

## AI Tester Applicability

HIGH for structural Meta dependency.  
Human required for motivation.

## Confidence

**VERY HIGH**

## Reviewer Action

Meta System이 있다면 먼저:

> **“영구 성장/해금을 전부 고정해도 이 Run을 다시 시작할 이유가 무엇인가?”**

를 묻는다.

답이 “다음 업그레이드를 얻기 위해서”뿐이면 `META_AS_BRIBE_RISK`.

---

# GC-ROGUE-002 — Player-selectable Risk Must Create a Legible Trade-off

**Decision:** `REFRAME / KEEP`  
**Status:** `CANDIDATE`  
**Origin:** `REFINEMENT OF EXISTING GC-ROGUE-002`

## Previous Claim

`Player-created Risk is Stronger than Passive Difficulty when the Game Promises Risk Management`

## Reframing Reason

현재 Evidence는:
- 플레이어가 Risk를 스스로 선택하면 Agency가 커질 수 있음
- Risk와 Reward를 같은 선택에 묶으면 Trade-off가 선명해짐

을 지지한다.

하지만:

> Player-created Risk가 Passive Difficulty보다 일반적으로 더 강하다.

는 비교 인과를 입증하지 않는다.

## Refined Rule Candidate

> **Risk Management를 Product Promise로 하는 Run에서는 플레이어가 위험의 크기·시점·경로 중 일부를 선택할 수 있을 때 Risk/Reward Agency가 강화될 수 있다. 단, 위험과 기대 보상을 읽을 수 있어야 한다.**

## Primary Evidence

### Slay the Spire
- Elite Node는 더 큰 보상을 위해 HP 위험을 선택하게 한다.
- HP는 Run 전체 위험 예산이다.

### Against the Storm
- Dangerous Glade와 Order 선택이 플레이어에게 위험 수준 조절 권한을 준다.

### FTL
- 안전 경로와 고보상 위험 경로, 수리/비축 선택이 존재한다.

## Secondary Evidence

### Loop Hero
가장 강한 직접 사례.
위험 타일을 더 배치하는 행위가 보상 생성과 실패 확률을 동시에 높인다.

## Counter Evidence

- Forced Escalation 자체가 긴장감을 만드는 Action Roguelite
- time pressure가 핵심인 Survivors-like

에서는 위험을 매번 선택하게 만들 필요가 없다.

## Candidate Metric — Machine

- Optional Risk Take Rate
- Elite / Dangerous Route Selection
- Risk Escalation Rate
- Retreat Rate
- Cash-out Rate
- Greed Failure Rate
- Risk → Reward Efficiency

## Candidate Metric — Human

- Risk Legibility
- Perceived Agency
- “왜 위험을 감수했는가?” Explanation

## Confidence

**MEDIUM-HIGH**

## Reviewer Action

Optional Risk가 있다면:

> **위험을 고르는 이유와 안전하게 거절하는 이유가 둘 다 존재하는가?**

를 본다.

---

# 5. Provisional Roguelike Cores

# GC-ROGUE-003 — Meaningful Run Variation Must Force Adaptation

**Status:** `PROVISIONAL CORE`  
**Origin:** `GENRE SPECIALIZATION OF UC-DESIGN-002`

## Pattern

강한 Roguelike/Roguelite 사례에서 Run Variation은 단순히 콘텐츠 순서를 랜덤하게 바꾸는 것이 아니라:
- 현재 Route
- Build
- Resource
- Tool
- Risk
- Position

가치를 변화시킨다.

## Roguelike Context

- Strategy Roguelike
- Deckbuilding Roguelike
- Roguelite Management
- Rule-variant Roguelike
- Action Roguelite

## Rule

> **Run Variety는 Seed / Map / Reward가 달라졌는지가 아니라, 그 변화 때문에 플레이어의 전략·경로·자원·Build 선택이 실제로 달라지는지로 평가한다.**

## Mechanism

Fake Variation:

```text
적 위치 랜덤
→ 하지만 항상 같은 전략
→ 결과적으로 같은 Run
```

Meaningful Variation:

```text
현재 자원 / 적 / 보상 / 도구 변화
→ 기존 최적 전략 약화
→ Plan / Build / Route 수정
→ 다른 Run Identity
```

## Primary Evidence

### FTL
노드, 이벤트, 적, 자원 상태가 달라져:
- 경로
- 수리
- 시스템 투자
- 위험 분산

판단이 달라진다.

### Slay the Spire
카드, 유물, 경로, 적이 달라 같은 완성 덱을 매번 복제하기 어렵다.

### Against the Storm
모든 건물과 자원을 항상 사용할 수 없고:
- 바이옴
- 종족
- 청사진
- 자원

이 달라서 적응형 정착을 요구한다.

### Dicey Dungeons
캐릭터와 Episode 규칙이 같은 Core Input을 다른 방식으로 해석하게 한다.

### Vampire Survivors
단순성은 높지만:
- 캐릭터
- 빌드
- 스테이지
- 해금 목표

가 다른 성장 선택을 유도한다.

## Counter Evidence

Arcade Score Attack처럼 실행 숙련을 반복하는 것이 주된 Product Promise라면 전략 Variation이 낮아도 성립할 수 있다.

## Boundary

“매 Run 모든 것이 달라야 한다”는 Rule이 아니다.

핵심은:

> **달라진 요소가 Decision Value를 바꾸는가?**

다.

## Observed Metric

Slay the Spire Reference에는 Choice Rate / Win Rate 분석이 존재하지만, Run-level Strategy Change 공통 Telemetry는 없다.

## Candidate Metric — Machine

- Encounter Distribution
- Reward Distribution
- Route Diversity
- State Diversity
- Strategy Change Rate
- Route Change Rate
- Context-triggered Action Shift
- Same Persona / Different Seed Divergence
- Run State Similarity
- Universal Strategy Rate

## Candidate Metric — Human / Hybrid

- Run Freshness
- “이전 Run과 다른 문제를 풀었다” 인식
- Variation Recognition

## Validation Type

Hybrid.

## AI Tester Applicability

VERY HIGH.

## Confidence

**VERY HIGH**

## Reviewer Action

Procedural / Random 시스템이 있다면:

> **“Seed가 달라졌을 때 최적 행동도 달라지는가?”**

를 묻는다.

아니라면 `FAKE_VARIATION_RISK`.

---

# GC-ROGUE-004 — Run Choices Must Create Path Dependence

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

강한 Run-based 사례에서는 현재 선택이 그 순간의 Power만 바꾸지 않고 이후:
- 선택 가치
- Route
- Build
- Resource Reserve
- 대응 가능성

을 바꾼다.

## Rule

> **Run 중 의미 있는 선택은 미래 Choice Space나 미래 선택 가치에 흔적을 남겨 Run Identity를 만들어야 한다. 모든 결정을 즉시 되돌리거나 매 순간 최적 옵션으로 갈아탈 수 있다면 Run의 Commitment가 약해진다.**

## Mechanism

Path Dependence가 없으면:

```text
현재 최고 효율 선택
→ 다음 선택은 이전과 독립
→ Run History가 전략에 거의 영향 없음
```

Path Dependence가 있으면:

```text
현재 투자
→ 미래 Resource / Build / Route 가치 변화
→ 선택의 기회비용 증가
→ 이번 Run 고유 전략 형성
```

## Primary Evidence

### FTL
- 시스템 Upgrade
- Crew
- Weapon
- Scrap 소비
- Route

가 이후 위험 대응 범위를 바꾼다.

### Slay the Spire
Deckbuilding Core 자체는 복제하지 않되, Roguelike 관점에서는:
- 카드/유물/HP/경로

선택이 이후 Encounter와 Reward 가치에 누적된다.

### Against the Storm
- Blueprint
- Production Chain
- Population
- Resource Availability

가 이후 정착의 가능성을 제한하고 재구성한다.

### Vampire Survivors
제한된 무기/패시브 Slot과 진화 조건이 Run 중 Build 방향을 만든다.

## Counter Evidence

Rule-variant puzzle roguelike처럼 Run Identity가 Build보다:
- execution
- level solution
- character rule

에 있는 경우 Commitment 방식이 약할 수 있다.

## Boundary

Path Dependence가 너무 강하면:
- Early RNG Lock
- No Pivot
- doomed run

위험이 발생한다.

따라서 이 Core는 “강하게 고정하라”가 아니라:

> **이전 선택이 의미를 남겨야 한다.**

는 Rule이다.

## Candidate Metric — Machine

- Early Choice → Later Choice Dependency
- Strategy Cluster Persistence
- Build / Route Commitment Rate
- Run State Divergence after Key Choice
- Reversal / Pivot Rate
- Universal Choice Rate after Commitment

## Candidate Metric — Human

- Strategy Identity
- “이번 Run을 한 문장으로 설명” 가능성
- Commitment vs Lock-in perception

## Validation Type

Hybrid.

## AI Tester Applicability

HIGH.

## Confidence

**HIGH**

## Reviewer Action

Run 중 Upgrade / Reward가 있다면:

> **“이 선택 때문에 이후 무엇이 더 좋아지고 무엇이 더 어려워지는가?”**

를 묻는다.

모든 Reward가 독립적인 +Power라면 `IDENTITYLESS_RUN_RISK`.

---

# GC-ROGUE-005 — Escalation Must Preserve Decisions

**Status:** `PROVISIONAL CORE`  
**Origin:** `NEW GENRE CORE`

## Pattern

Run이 진행될수록 성공 사례들은 압박을 키우지만, 단순히 숫자만 높이는 방식은 Subtype마다 비중이 다르다.

공통적으로 중요한 것은:

> 압박이 증가해도 플레이어가 계속 판단하거나 실행을 조정해야 한다.

는 점이다.

## Rule

> **Run Escalation은 Run 후반까지 의미 있는 Adaptation / Risk / Execution 결정을 유지해야 한다. 단순 HP·Damage 증가만으로 난이도를 설명하지 않으며, 숫자 증가가 Core Fantasy인 Subtype에서는 그 숫자 압박이 계속 선택을 요구하는지 확인한다.**

## Mechanism

나쁜 형태:

```text
Build 완성
→ 같은 행동 반복
→ 적 HP만 증가
→ 결과는 이미 확정
```

좋은 형태 후보:

```text
Run 진행
→ 새로운 적 조합 / Rule / Resource pressure
→ 현재 Build의 약점 노출
→ 새로운 선택 / 실행 조정
```

또는 Survivors-like에서는:

```text
적 밀도 증가
→ 위치 / 성장 속도 / Slot 선택 압박 지속
```

처럼 Numeric Density 자체가 판단 조건을 변화시킬 수 있다.

## Primary Evidence

### FTL
섹터가 진행될수록 적 조합과 대응 요구가 증가하며 최종 보스는 한 가지 강점보다 전체 준비를 시험한다.

### Slay the Spire
Act가 진행될수록 적 패턴이 특정 덱 약점을 시험하고, Ascension은 규칙 변형으로 숙련자를 재시험한다.

### Against the Storm
폭풍, Impatience, Resource Constraint와 난이도 Modifier가 조합되어 정착 후반에도 Adaptation을 요구한다.

### Vampire Survivors
시간에 따라 적 밀도와 체력이 증가하고 플레이어 성장 속도가 이를 추월해야 한다. Numeric Escalation이 강하지만 위치·빌드·성장 판단이 남는 것이 핵심이다.

### Dicey Dungeons
Character / Episode Rule 변화가 같은 Core System을 다른 방식으로 재시험한다.

## Counter Evidence

Power Fantasy에서 후반 Autopilot 자체가 짧은 보상 구간으로 의도될 수 있다.

문제는:
- 언제 시작되는가
- 얼마나 지속되는가
- 이후 Run Outcome이 사실상 확정되는가

다.

## Candidate Metric — Machine

- Decision Entropy by Run Phase
- Strategy Change Rate by Phase
- Last Structural Decision
- Autopilot Duration
- Late-run Strategy Concentration
- Encounter-specific Action Shift
- Failure Stage Distribution

## Candidate Metric — Human / Hybrid

- Late-run Decision Quality
- Run Pacing
- “후반에도 새로운 판단이 있었는가?”
- Perceived Escalation Quality

## Validation Type

Hybrid.

## AI Tester Applicability

HIGH structurally.

## Confidence

**HIGH**

## Reviewer Action

난이도 곡선을 볼 때:

> **“적 숫자가 올라가는 것 외에 후반에 어떤 새로운 판단을 요구하는가?”**

를 묻는다.

단, Survivors-like처럼 숫자 압박 자체가 위치/빌드 판단을 바꾸는 경우를 예외로 인정한다.

---

# 6. Roguelike Core Candidates

# GC-ROGUE-006 — Failure Should Generate a Next-Run Hypothesis

**Status:** `CANDIDATE`  
**Origin:** `NEW GENRE CORE`

## Rule Candidate

> **Run Failure는 최소한 플레이어에게 다음 Run에서 시험할 새로운 행동·Route·Build·Resource 가설을 남겨야 한다. 실패 원인을 전혀 좁힐 수 없다면 Reset이 학습보다 복권 재시도에 가까워질 수 있다.**

## Supporting Evidence

### FTL
Target Player를 “반복 실패를 통한 학습을 좋아하는 플레이어”로 명시하고, 준비·회피·복구 선택이 RNG 대응의 핵심이다.

### Slay the Spire
적 패턴, 경로, 카드 선택은 Run 반복을 통해 학습되며 Ascension은 숙련을 재시험한다.

### Against the Storm
같은 완성 정착을 복제하기보다 매 Run 다른 조건에서 초기 구축 판단을 재시도한다.

### Dicey Dungeons
Character / Episode 규칙은 같은 Core를 다른 방식으로 학습하게 한다.

## Promotion Blocker

현재 Reference에는:
- Failure Attribution telemetry
- “next-run change” player response

가 직접 측정되어 있지 않다.

## Candidate Metric — Machine

- Structural Failure Cause Distribution
- First Critical Mistake
- Failure after Recovery Opportunity
- Repeated Same-cause Failure Rate

## Candidate Metric — Human

- Failure Attribution
- Failure Learning
- “다음 Run에 무엇을 바꿀 것인가?”
- Cause Explanation Accuracy

## Hybrid

- Structural Cause ↔ Perceived Cause Agreement

## Confidence

**MEDIUM-HIGH**

---

# GC-ROGUE-007 — Run Length Must Justify Failure Cost

**Status:** `CANDIDATE`

## Rule Candidate

> **Run이 길어질수록 실패로 잃는 시간과 상태가 커지므로, 중간 Decision Density와 학습 가치가 그 비용을 정당화해야 한다.**

## Evidence

### FTL
Reference가 `장기 Run 실패 비용`을 명시적 Weakness로 기록하며, 실패 비용이 크기 때문에 Run 길이와 학습 피드백이 중요하다고 분석한다.

### Against the Storm
기존 City Builder의 긴 정착을 짧은 Run으로 분할해 초기 구축의 반복 가치를 높인다.

### Vampire Survivors
짧은 Session과 빠른 성장으로 Restart 부담을 낮춘다.

## Promotion Blocker

“어느 길이가 적정한가”에 대한 공통 Telemetry가 없다.

## Candidate Metric — Machine

- Run Length
- Failure Stage
- Time Lost per Failure
- Meaningful Decision Count / Run
- Decision Density by Phase

## Candidate Metric — Human / Hybrid

- Failure Cost
- Session Fatigue
- “다시 시작하기 부담스럽다” 평가

## Confidence

**MEDIUM-HIGH**

---

# GC-ROGUE-008 — Restart Friction Should Not Hide the Next Decision

**Status:** `CANDIDATE`

## Rule Candidate

> **Run 실패 이후 다음 의미 있는 선택까지의 메뉴·로딩·Meta 관리·반복 Tutorial이 길어질수록 Reset Loop의 재시작 동기가 약해질 수 있다.**

## Evidence

Vampire Survivors의 짧은 Session / 낮은 Restart burden이 간접 지지.

Against the Storm의 Session 구조도 장기 도시 완성 대신 반복 가능한 정착을 의도한다.

## Promotion Blocker

실제 `Death → Next Meaningful Decision` Telemetry가 현재 Reference에 없다.

## Candidate Metric

### Machine
- Death → Run Start Time
- Run Start → First Meaningful Choice
- Menu / Meta Screen Time
- Tutorial Repetition Time

### Human
- Restart Friction
- “실패 후 재도전이 번거로운가?”

## Confidence

**MEDIUM**

---

# GC-ROGUE-009 — Early Run Must Not Collapse into Fixed Autopilot

**Status:** `CANDIDATE`

## Rule Candidate

> **반복 Run의 초반 구간이 이전 Run에서 이미 해결한 동일 절차로 고정되면 Reset의 반복 비용이 커진다. 초반에도 적어도 일부 Contextual Choice 또는 빠른 Variation이 필요할 수 있다.**

## Supporting Evidence

Against the Storm은 장르의 “재미있는 초기 구축”을 반복 Run으로 만들었지만 동시에 모든 도구를 주지 않아 매 초기 구축을 다르게 만든다.

Slay the Spire도 경로·카드 제공이 초반부터 달라진다.

## Promotion Blocker

Early Action Sequence Telemetry 부족.

## Candidate Metric — Machine

- Early Action Sequence Concentration
- First Choice Diversity
- First Strategy Divergence Turn
- Early Run State Similarity

## Human / Hybrid

- Early-run Repetition
- “이미 해결한 초반을 다시 한다” 인식

## Confidence

**MEDIUM**

---

# GC-ROGUE-010 — Meta Progression Type Must Match Product Promise

**Status:** `CANDIDATE`

## Pattern Candidate

Meta에는 최소 세 종류가 있다.

### Vertical Meta
Permanent Stat / Power 증가.

### Horizontal Meta
Character / Item / Rule / Starting Option 해금.

### Knowledge Meta
플레이어가 적·Route·Build·Risk를 학습.

## Rule Candidate

> **Meta Progression을 단일 축으로 평가하지 않고, 어떤 종류의 장기 성장이 Target Player와 Difficulty Promise에 맞는지 구분한다.**

## Evidence

- FTL — 함선 해금은 수평적 장기 목표.
- Slay the Spire — Character/Ascension과 숙련.
- Against the Storm — Settlement 내부 임시 성장과 장기 Meta 분리.
- Vampire Survivors — 빠른 Run 성장 + 영구 해금 / 업그레이드.

## Counter Evidence

Vertical Meta는:
- 접근성
- Power Fantasy
- 장기 성취

에 매우 유효할 수 있다.

반대로 높은 Skill / Knowledge mastery를 약속하는 게임에서 과도한 Permanent Power는 Difficulty Interpretation을 흐릴 수 있다.

## Candidate Metrics

- Permanent Power Contribution
- Horizontal Unlock Usage
- Knowledge-dependent Success Improvement
- Win Rate by Meta Level
- New Strategy Count by Unlock Level

## Human

- Meta Motivation
- “강해져서 성공했나 / 배워서 성공했나” 인식

## Confidence

**MEDIUM**

---

# GC-ROGUE-011 — Unlock Expansion Can Create Pool Dilution

**Status:** `CANDIDATE`

## Rule Candidate

> **장기 해금이 Variety를 늘릴 수 있지만 Reward / Item / Encounter Pool을 확장해 특정 전략의 출현률이나 Choice Quality를 낮출 수도 있으므로, Unlock은 사용량뿐 아니라 Pool Dilution을 함께 검토한다.**

## Evidence

Slay the Spire / Vampire Survivors / Dicey Dungeons는 Unlock 확장을 가진다.

그러나 현재 Reference는 Unlock 증가가 Pool Quality에 미친 직접 Telemetry를 제공하지 않는다.

Deckbuilding `Pool Growth Needs Quality Control`과 중복되지 않도록 Roguelike에서는 **런 밖 해금이 미래 Run의 Random Pool을 바꾸는 문제**에만 적용한다.

## Candidate Metric — Machine

- Unlock Usage Rate
- Reward Pool Size by Meta Level
- Desired-option Availability
- Dead / Low-use Unlock Rate
- Strategy Diversity by Unlock Level
- Strategy Concentration by Unlock Level

## Candidate Metric — Human

- Unlock Value Perception
- “해금이 선택지를 늘렸나 잡음을 늘렸나?”

## Confidence

**MEDIUM**

---

# GC-ROGUE-012 — Difficulty Should Re-test Mastery, not Only Shrink Error Margin

**Status:** `CANDIDATE`

## Rule Candidate

> **높은 난이도가 핵심 상품이라면 단순 HP/Damage 증가 외에도 기존 지식·Build·Route·Execution을 다른 방식으로 시험하는지 검토한다. 단, 숫자 압박 자체가 Core Fantasy인 Subtype은 예외다.**

## Evidence

### Slay the Spire
Ascension은 규칙 변형으로 숙련자를 재시험한다.

### Dicey Dungeons
Character / Episode Rule Variation으로 같은 Core를 다르게 시험한다.

### FTL
섹터가 진행될수록 적 조합과 대응 요구가 증가한다.

## Counter Evidence

Vampire Survivors:
시간에 따른 밀도 / 체력 증가가 핵심 Power Race를 만든다.

## Candidate Metric — Machine

- Difficulty Level → Strategy Distribution
- Difficulty Level → Action Change
- Numeric-only Scaling Ratio
- New Constraint Count
- Universal Strategy Survival across Difficulty

## Human

- “더 잘 판단해야 했다” vs “숫자만 불리했다”
- Difficulty Fairness

## Confidence

**MEDIUM-HIGH**

---

# GC-ROGUE-013 — Late-run Autopilot Must Be Bounded

**Status:** `CANDIDATE`

## Rule Candidate

> **Run Build / Engine이 완성된 뒤 동일 행동으로 결과가 사실상 확정되는 구간이 존재한다면 그 구간 길이와 보상 역할을 검토한다. 짧은 Power Fantasy 구간은 가능하지만 Run의 큰 비중을 차지하면 Decision Collapse 위험이 있다.**

## Evidence

Vampire Survivors / Balatro adjacent에서 Power Explosion은 보상으로 유효할 수 있다.

FTL / Slay the Spire / Against the Storm은 후반에도 적 / 압박 / Resource가 Run을 시험한다.

## Candidate Metric

- Last Meaningful Decision
- Autopilot Duration
- Decision Entropy by Run Phase
- Outcome Certainty after Power Spike

## Human

- Late-run Decision Quality
- “이미 이긴/진 Run을 실행만 했다” 인식

## Confidence

**MEDIUM**

---

# 7. Roguelike Anti-Patterns

# AP-ROGUE-001 — Meta Progression as Bribe

## Trigger
Run 자체보다 Permanent Reward가 유일한 재시작 이유.

## Mechanism
반복 Core의 동일함을 장기 숫자 증가로 덮는다.

## Consequence
- Grind
- Core weakness masking
- Meta dependency

## Evidence
Against the Storm의 직접 Warning:
Meta만 붙여서는 반복 정체를 해결할 수 없다.

## Detection Metric
- Win Rate by Meta Level
- No-meta Replay Intent
- Restart Motivation Classification
- Permanent Power Contribution

## Mitigation
Meta를 제거한 Micro Run Test.

---

# AP-ROGUE-002 — Randomness without Adaptation

## Trigger
Seed / Reward / Enemy는 달라지지만 Player Response는 동일.

## Consequence
Randomness는 Replayability가 아니라 결과 변동만 만든다.

## Evidence
FTL / Dicey Dungeons:
RNG는 준비·조작·복구·배분 선택이 있을 때 전략 자원이 된다.

## Detection Metric
- Same Persona / Different Seed Strategy Similarity
- Strategy Change Rate
- RNG Response Usage

## Mitigation
Random element가 어떤 Plan Change를 요구하는지 정의한다.

---

# AP-ROGUE-003 — Content Count = Replayability

## Trigger
방·적·아이템 수 증가를 Run Variety로 간주.

## Consequence
콘텐츠는 많지만 같은 전략 반복.

## Evidence
Against the Storm은 새 맵 수보다 규칙·건물·종족 조합으로 변주.
Slay the Spire는 카드 수와 RNG만 늘린다고 깊이가 생기지 않는다고 Warning.

## Detection Metric
- Content Count vs Strategy Diversity
- Context-triggered Strategy Shift
- Universal Strategy Rate

## Mitigation
새 콘텐츠가 기존 Choice Value를 바꾸는지 확인.

---

# AP-ROGUE-004 — Fixed Opening Autopilot

## Trigger
매 Run 동일한 초반 절차.

## Consequence
Reset이 “새 문제”가 아니라 반복 Setup 비용이 됨.

## Detection Metric
- Early Action Sequence Concentration
- Time to First Divergence
- Early State Similarity

## Mitigation
초반부터:
- starting state
- route
- tool
- reward
중 적어도 일부를 Decision-relevant하게 변화.

---

# AP-ROGUE-005 — Early RNG Locks the Run

## Trigger
초반 Reward / Event 하나가 미래 전략을 지나치게 고정.

## Consequence
- doomed run
- later choices lose meaning
- seed attribution

## Detection Metric
- Early Choice / RNG → Outcome Correlation
- Pivot Rate
- Bad-seed Failure Concentration

## Mitigation
- recovery window
- alternate path
- flexible reward
- pivot option

---

# AP-ROGUE-006 — No Commitment / Identityless Run

## Trigger
이전 선택이 미래 Choice Value에 거의 영향을 주지 않음.

## Consequence
매 선택이 현재 Power 비교로 환원.

## Detection Metric
- Strategy Cluster Persistence
- Run State Divergence
- Universal Choice Rate

## Mitigation
Path dependence를 추가하되 hard lock은 피한다.

---

# AP-ROGUE-007 — Unrecoverable Bad Seed

## Trigger
불리한 Seed에서 합리적 대응 수단 없이 결과가 사실상 결정.

## Consequence
실패가 Adaptation보다 Lottery로 인식.

## Detection Metric
- Seed Outcome Variance
- Bad-seed Failure Concentration
- Same Seed / Different Persona Divergence
- Recovery Option Usage

## Mitigation
- route
- reroll
- reserve
- retreat
- alternate build
- recovery

---

# AP-ROGUE-008 — Failure without Learning

## Trigger
패배 원인을 좁히기 어렵거나 같은 실패가 반복되어도 새 가설이 생기지 않음.

## Consequence
Restart motivation이 Meta / luck에 의존.

## Detection Metric
- Repeated Same-cause Failure
- Structural Failure Cause
- Human Failure Attribution
- Next-run Change Statement

## Mitigation
Cause readability + recoverable decision points.

---

# AP-ROGUE-009 — Long Run / Low Decision Density

## Trigger
Run은 길지만 중간 구간 판단이 적음.

## Consequence
실패 비용이 학습 가치보다 커짐.

## Detection Metric
- Meaningful Decisions / Run
- Decision Density by Phase
- Time Lost per Failure
- Autopilot Duration

## Mitigation
Run 단축 또는 반복 실행 압축.

---

# AP-ROGUE-010 — Late-run Autopilot

## Trigger
Build 완성 후 결과가 사실상 확정.

## Consequence
Run 후반이 보상이라기보다 실행 대기시간이 될 수 있음.

## Detection Metric
- Last Meaningful Decision
- Decision Entropy late-run
- Outcome Certainty

## Mitigation
새 Encounter pressure / bounded victory lap / run 종료 가속.

---

# AP-ROGUE-011 — Meta Power Hides Balance Problems

## Trigger
Permanent Stat이 낮은 Run success를 반복적으로 보정.

## Consequence
- Player Skill과 Stat Gate 구분 어려움
- 약한 초기 Balance가 가려짐

## Detection Metric
- Win Rate by Meta Level
- Same Strategy success by Meta level
- Permanent Power Contribution

## Mitigation
고정 Meta 상태의 Core balance test.

---

# AP-ROGUE-012 — Unlock Dilution

## Trigger
해금이 늘수록 Reward / Item Pool에 저가치 선택 증가.

## Consequence
Variety 증가와 함께 Desired Build consistency 감소.

## Detection Metric
- Unlock Usage
- Low-use Unlock Rate
- Reward Pool Size
- Strategy Diversity vs Pool Size

## Mitigation
Pool segmentation / filtering / unlock quality control.

---

# AP-ROGUE-013 — Fake Variation

## Trigger
맵/색/적 위치는 달라지지만 의사결정 구조 동일.

## Consequence
Seed count는 많지만 Run Freshness 낮음.

## Detection Metric
- Run State Similarity
- Strategy Similarity across seeds
- Route / Action divergence

## Mitigation
Context가 Value Ranking을 바꾸도록 설계.

---

# AP-ROGUE-014 — Difficulty as Numeric Inflation

## Trigger
높은 Difficulty가 HP / Damage / Speed 증가로만 구성.

## Consequence
새 판단보다 Error Margin만 감소.

## Detection Metric
- New Constraint Count by difficulty
- Strategy Distribution Shift
- Numeric Scaling Ratio

## Mitigation
Subtype에 맞는:
- rule modifier
- enemy behavior
- resource pressure
- route pressure
를 검토.

---

# AP-ROGUE-015 — Restart Friction

## Trigger
실패 후:
- menu
- loading
- meta allocation
- tutorial
- fixed opening

이 길게 이어짐.

## Consequence
Reset Loop의 실제 반복비 증가.

## Detection Metric
- Death → First New Decision Time
- Meta Screen Time
- Fixed Opening Duration

## Mitigation
빠른 Restart / persistent settings / tutorial skip / early divergence.

---

# 8. Conflicting Findings

# CF-ROGUE-001 — Vertical Meta vs Horizontal Meta

## Evidence A — Vertical
Vampire Survivors:
영구 성장과 Unlock이 접근성과 Power Fantasy를 지원한다.

## Evidence B — Horizontal / Knowledge
FTL:
함선 해금은 수평적 목표이며 Run 적응 자체가 중요하다.

Slay the Spire:
Ascension / Character와 플레이어 숙련이 큰 비중을 가진다.

## Hidden Variables
- Target Audience
- Difficulty Promise
- Power Fantasy
- Accessibility
- Run Length

## Resolution
Vertical Meta를 자동 감점하지 않는다.

다음만 묻는다.

> **Meta Power가 Core learning을 보완하는가, 대체하는가?**

---

# CF-ROGUE-002 — High Variance vs Controlled Variance

## Evidence A
FTL은 이벤트 / Route / 자원 변동성이 높다.

## Evidence B
Dicey Dungeons는 현재 RNG를 명확히 보여주고 조작 수단을 제공한다.

## Hidden Variables
- Information
- Response Agency
- Recovery
- Run Length

## Resolution
Variance 수준 자체가 아니라:
- 대응 가능성
- 실패 비용
- 학습 가능성

을 함께 본다.

---

# CF-ROGUE-003 — Short Run vs Long Run

## Evidence A
Vampire Survivors / Dicey Dungeons:
짧고 빠른 반복.

## Evidence B
FTL:
상대적으로 긴 Systemic Run과 큰 실패 비용.

## Hidden Variables
- Decision Density
- Narrative / systemic accumulation
- Restart friction
- failure learning
- attachment to current run

## Resolution
Run length Universal Threshold를 만들지 않는다.

---

# CF-ROGUE-004 — Build Commitment vs Pivot

## Strong Commitment
Run Identity를 만든다.

## Flexible Pivot
Bad Seed / 초기 실수에서 회복 가능.

## Hidden Variables
- Run Length
- Information Timing
- Reward Frequency
- Build Specificity

## Resolution

> **Run History가 의미를 남기되 초반 한 선택이 결과를 확정하지 않는 범위**

를 프로젝트별로 검증한다.

---

# CF-ROGUE-005 — Permadeath vs Partial Persistence

Reset 범위는 Product Promise에 따라 달라진다.

- FTL — Run failure reset + horizontal unlock
- Against the Storm — Settlement reset + world/meta persistence
- Vampire Survivors — Run reset + broad unlock/power persistence

## Resolution
“더 많이 Reset할수록 Roguelike답다”를 Reviewer Rule로 사용하지 않는다.

---

# CF-ROGUE-006 — Knowledge Progression vs Stat Progression

## Knowledge-heavy
FTL / Slay the Spire / Dicey Dungeons.

## Stat / Unlock-heavy
Vampire Survivors.

## Hidden Variables
- Action skill
- Target audience
- accessibility
- desired mastery curve

## Resolution
Player Skill / Knowledge / Stat contribution을 분리 측정한다.

---

# CF-ROGUE-007 — Unknown Information vs Readable Risk

## FTL
장기 Node / Event outcome은 불확실.

## Slay the Spire
단기 적 의도는 공개, 장기 Reward는 불확실.

## Dicey Dungeons
현재 RNG input은 공개.

## Resolution
모든 위험을 공개할 필요는 없다.

단:
- 위험의 존재
- 대응 Channel
- 실패 후 학습

이 의도한 Fantasy와 맞아야 한다.

---

# CF-ROGUE-008 — Self-authored Risk vs Forced Escalation

## Self-authored
Loop Hero / Slay the Spire Elite / Against the Storm Dangerous Glade.

## Forced
Vampire Survivors의 시간 기반 밀도 증가.

## Hidden Variable
Product Promise.

- Risk management
- Survival pressure
- Power race
- route planning

## Resolution
Player-created Risk를 전체 장르 필수로 만들지 않는다.

---

# 9. AI Tester Metric Map

Metric은 Criteria가 아니다.  
Threshold는 각 프로젝트 Validation Planner가 잠근다.

## 9.1 Run Metrics

| Metric | Type | Purpose |
|---|---|---|
| Run Completion Rate | Machine | 전체 성공 분포 |
| Run Length | Machine | 세션 구조 |
| Failure Stage Distribution | Machine | 실패 위치 |
| Restart Rate | Machine / instrumented | 실제 재시도 빈도 |
| Early Abandon Rate | Machine / instrumented | 중도 포기 |
| Late-run Failure Rate | Machine | 후반 실패 집중 |

---

## 9.2 Variation Metrics

| Metric | Type |
|---|---|
| Encounter Distribution | Machine |
| Reward Distribution | Machine |
| Route Diversity | Machine |
| Seed Outcome Variance | Machine |
| State Diversity | Machine |
| Run State Similarity | Machine |
| Same Persona / Different Seed Strategy Divergence | Machine |

---

## 9.3 Adaptation Metrics

| Metric | Type |
|---|---|
| Strategy Change Rate | Machine |
| Route Change Rate | Machine |
| Build Pivot Rate | Machine |
| Resource Reallocation Rate | Machine |
| Context-triggered Action Shift | Machine |
| Retreat / Skip Usage | Machine |

---

## 9.4 Strategy Metrics

| Metric | Type |
|---|---|
| Strategy Concentration | Machine |
| Strategy Success Distribution | Machine |
| Build Diversity | Machine |
| Build Convergence | Machine |
| Character Strategy Diversity | Machine |
| Universal Strategy Rate | Machine |

---

## 9.5 Risk Metrics

| Metric | Type |
|---|---|
| Optional Risk Take Rate | Machine |
| Elite / Dangerous Route Selection | Machine |
| Risk → Reward Efficiency | Machine |
| Retreat Rate | Machine |
| Cash-out Rate | Machine |
| Greed Failure Rate | Machine |
| Risk Escalation Rate | Machine |

---

## 9.6 RNG Metrics

| Metric | Type |
|---|---|
| Outcome Variance by Seed | Machine |
| Same Persona / Different Seed Divergence | Machine |
| Different Persona / Same Seed Divergence | Machine |
| Bad-seed Failure Concentration | Machine / model-dependent |
| Recovery Option Usage | Machine |
| RNG Response Usage | Machine |

---

## 9.7 Failure Metrics

| Metric | Type |
|---|---|
| Structural Failure Cause Distribution | Machine / model-dependent |
| Unrecoverable State Entry | Machine / model-dependent |
| First Critical Mistake | Machine / model-dependent |
| Failure after Recovery Opportunity | Machine / model-dependent |
| Run Lost-before-Player-Knows Rate | Machine / model-dependent |
| Perceived Failure Attribution | Human |
| Structural ↔ Perceived Cause Agreement | Hybrid |

### Model-dependent Failure Metric Rule

다음 Metric은 일반적인 Machine Metric으로 자동 사용하지 않는다.

- First Critical Mistake
- Unrecoverable State Entry
- Bad-seed Failure Concentration
- Preventable Failure
- Failure after Recovery Opportunity
- Run Lost-before-Player-Knows Rate

이 항목들은 **프로젝트별 Formal Definition 또는 Counterfactual Model이 존재할 때만 Machine Metric으로 사용한다.**

예를 들어:

```text
Turn 12에서 Elite 선택
→ Turn 20 사망
```

이라는 사실만으로 Turn 12 선택을 `First Critical Mistake`로 판정하지 않는다.

최소한:

- 다른 선택을 했을 경우의 Counterfactual Outcome
- 프로젝트별 명시적 Error Definition
- Unrecoverable State의 Formal Condition

중 하나가 필요하다.

---

## 9.8 Meta Metrics

| Metric | Type |
|---|---|
| Win Rate by Meta Level | Machine |
| Run Duration by Meta Level | Machine |
| Strategy Diversity by Unlock Level | Machine |
| Permanent Power Contribution | Machine / model-dependent |
| Unlock Usage Rate | Machine |
| Unlock Dilution | Machine / model-dependent |

---

## 9.9 Pacing Metrics

| Metric | Type |
|---|---|
| First Meaningful Choice | Machine if formally defined / Hybrid |
| Build Formation Timing | Hybrid |
| First Major Risk Timing | Machine if state-defined / Hybrid |
| First Recovery Decision | Machine |
| Last Structural Decision | Machine if formally defined / Hybrid |
| Autopilot Duration | Machine if policy-defined / Hybrid |
| Run Pacing | Hybrid |
| Early-run Repetition | Hybrid |
| Late-run Decision Quality | Hybrid |

---

# 10. Persona Validation Map

AI Tester Persona는 게임 규칙을 변경하지 않고 **선택 정책**만 바꾼다.

## P-ROGUE-001 — Efficiency Persona

선택 경향:
- 기대값 최대화
- 보수적 resource efficiency
- high value route 우선

검토:
- Dominant Strategy
- Universal Choice
- Balance exploit

---

## P-ROGUE-002 — Risk-seeking Persona

선택 경향:
- Elite
- Optional Risk
- Greed
- Continue over Retreat

검토:
- Risk → Reward Efficiency
- Greed Failure
- Player-selectable risk balance

---

## P-ROGUE-003 — Conservative Persona

선택 경향:
- 회복
- 안전 Route
- Reserve
- Retreat

검토:
- survival viability
- excessive punishment
- reward opportunity cost

---

## P-ROGUE-004 — Explorer Persona

선택 경향:
- 미사용 Route
- 미사용 Build
- 새 Reward
- 낮은 familiarity option

검토:
- content / strategy coverage
- dead unlock
- hidden dominant route

---

## P-ROGUE-005 — General Persona

극단 최적화 없이 혼합 행동.

검토:
- baseline behavior
- Persona divergence comparison

---

## Persona Comparison Metrics

- Persona별 Win Rate
- Persona별 Route Distribution
- Persona별 Risk Take
- Persona별 Build / Strategy Cluster
- Persona별 Failure Cause
- Persona Divergence
- Same Seed / Different Persona Outcome Divergence

### Interpretation Limit

Persona 간 결과 차이가 크다고 해서 Human Variety가 자동으로 좋다는 뜻은 아니다.

---

# 11. Human Validation Map

## H-ROGUE-001 — Restart Motivation

> Run이 끝난 직후 다시 시작하고 싶은 이유는 무엇인가?

분류:
- Core Play
- 새로운 전략
- 다른 Seed
- Execution 개선
- Unlock 획득
- Meta Grind

---

## H-ROGUE-002 — Failure Attribution

> 왜 실패했다고 생각하는가?

분류 후보:
- Decision
- Execution
- Build
- Resource
- Route
- RNG
- Unknown

---

## H-ROGUE-003 — Failure Learning

> 다음 Run에서 무엇을 다르게 할 것인가?

---

## H-ROGUE-004 — RNG Fairness

> 결과를 Randomness 때문이라고 느끼는가, 자신의 대응 선택 때문이라고 느끼는가?

---

## H-ROGUE-005 — Run Freshness

> 이전 Run과 다른 문제를 풀었다고 느끼는가?

---

## H-ROGUE-006 — Early-run Repetition

> 이미 알고 있는 초반 절차를 다시 수행하는 느낌이 강한가?

---

## H-ROGUE-007 — Run Strategy Identity

> 이번 Run의 전략을 한 문장으로 설명할 수 있는가?

---

## H-ROGUE-008 — Commitment / Pivot

> 전략을 만들었다고 느끼는가, 초반 RNG에 묶였다고 느끼는가?

---

## H-ROGUE-009 — Meta Motivation

> 다음 Run을 시작하는 이유가 플레이 자체인가, 다음 해금인가?

---

## H-ROGUE-010 — Failure Cost

> 현재 Run 길이에 비해 실패가 과도하게 허무하게 느껴지는가?

---

## H-ROGUE-011 — Late-run Decision

> 후반에도 새로운 판단이 있었는가?

---

## H-ROGUE-012 — Difficulty Growth

> 높은 난이도에서 더 잘 판단해야 했는가, 단순히 숫자가 불리해졌는가?

---

## H-ROGUE-013 — Power / Learning Attribution

> 이번 성공은 내가 더 잘 알아서인가, 영구 능력치가 올라서인가?

---

# 12. Scale Handoff Candidates

이번 문서에서는 Scale Core로 승격하지 않는다.

# SCALE_HANDOFF-ROGUE-001 — Run Content Matrix QA Explosion

## Finding

Roguelike의 QA 비용은 개별 콘텐츠 수보다:

```text
Character
× Enemy
× Reward
× Map
× Event
× Difficulty
× Modifier
× Build
```

조합에서 폭증할 수 있다.

## Supporting Evidence

- Slay the Spire — 높은 조합 QA 비용
- Against the Storm — 자원·종족·건물·난이도 조합
- FTL — 시스템·적·이벤트·자원 상태 상호작용

## Handoff

Genre × Scale 분석에서 팀 규모별 QA Capacity와 함께 검토.

---

# SCALE_HANDOFF-ROGUE-002 — Procedural Generation Is Not Free Content

## Finding

Procedural Generation은 수작업 콘텐츠 비용을 줄일 수 있지만 다음 비용을 만든다.

- Generator Code
- Invalid State Prevention
- Balance
- Repetition Detection
- Edge-case QA
- Seed Debugging

## Evidence Status

현재 Reference가 Procedural production cost를 직접 충분히 정량화하지 않으므로 Handoff Candidate 유지.

---

# SCALE_HANDOFF-ROGUE-003 — Unlock / Meta Content Cost

## Finding

Character / Item / Rule / Stage Unlock이 늘수록:

- Data
- UI
- Balance
- Regression QA
- Tutorial / Tooltip

비용이 증가한다.

## Supporting Evidence

- Vampire Survivors
- Tiny Rogues production case
- Brotato production case
- Peglin production case

---

# SCALE_HANDOFF-ROGUE-004 — Systemic Recombination as Content Multiplier

## Finding

FTL / Against the Storm처럼 소수 시스템과 조건을 재조합하면 개별 고유 콘텐츠보다 높은 Run Variation을 만들 수 있다.

## Boundary

Systemic Reuse가 높아도:
- balance
- readability
- QA

비용이 사라지는 것은 아니다.

---

# 13. Universal Reclassification Candidates

이 단계에서는 Universal로 직접 승격하지 않는다.

# UC-RECLASS-ROGUE-001 — Failure Should Generate New Information

## Candidate Rule

> 반복 시도를 전제로 하는 시스템에서는 실패가 다음 시도의 행동 가설을 좁히는 정보를 남겨야 한다.

Roguelike에서 강하지만:
- Puzzle
- Strategy
- Action
- Learning game

에도 확장 가능성이 있다.

**Status:** `UNIVERSAL RECLASSIFICATION CANDIDATE`

---

# UC-RECLASS-ROGUE-002 — Variation Must Change Decisions

이미 `UC-DESIGN-002 Contextual Value Shift`와 강하게 겹친다.

## Decision

새 Universal Core로 만들지 않고:

`GC-ROGUE-003 = UC-DESIGN-002의 Run specialization`

으로 유지한다.

---

# UC-RECLASS-ROGUE-003 — Restart Friction

## Candidate Rule

> 반복 시도가 핵심인 시스템에서는 실패 후 다음 의미 있는 시도까지의 비의사결정 시간이 경험 비용이 된다.

Roguelike 밖:
- puzzle retry
- boss retry
- experiment iteration

에도 적용 가능.

현재 Evidence 부족.

---

# UC-RECLASS-ROGUE-004 — Difficulty Should Change the Problem, not only the Margin

Strategy / Puzzle / Deckbuilding에도 확장 가능성이 있으나 Vampire Survivors 같은 반례 때문에 Boundary 연구가 필요하다.

---

# 14. Evidence Gaps

# GAP-ROGUE-001 — Reset → Restart Telemetry

부족:
- 실제 재시작률
- 실패 후 이탈률
- 다음 Run 시작까지 시간
- Meta screen 체류시간

---

# GAP-ROGUE-002 — No-meta Replay Behavior

`GC-ROGUE-001`을 더 강하게 검증하려면:
- Meta 고정 상태의 replay
- Unlock 없는 초기 Prototype
- Meta 제거 A/B

자료가 필요하다.

---

# GAP-ROGUE-003 — Seed Outcome Variance

필요:
- 동일 Persona / Seed별 Win Rate
- bad-seed concentration
- recovery opportunity

---

# GAP-ROGUE-004 — Failure Attribution / Learning

필요:
- Structural Cause
- Player-perceived Cause
- Next-run plan
- Cause Agreement

---

# GAP-ROGUE-005 — Early-run Autopilot

필요:
- early action sequence
- first divergence
- player boredom
- abandonment

---

# GAP-ROGUE-006 — Late-run Decision Collapse

필요:
- last meaningful decision
- power spike
- outcome certainty
- human late-run engagement

---

# GAP-ROGUE-007 — Meta Dependency

필요:
- win rate by meta
- player motivation by meta
- permanent power contribution
- meta-free core test

---

# GAP-ROGUE-008 — Unlock Dilution

필요:
- unlock pool size
- low-use unlock
- desired reward availability
- choice quality by meta level

---

# GAP-ROGUE-009 — Run Abandonment

현재 성공/실패만 보는 자료가 많고:
- voluntary abandon
- quit mid-run
- restart before death

데이터가 부족하다.

---

# GAP-ROGUE-010 — Persona Strategy Divergence

AI Tester 설계와 직접 연결될 수 있으나 현재 Reference에서 실제 multi-persona simulation evidence는 없다.

---

# GAP-ROGUE-011 — Underperforming Roguelike Controls

특히 필요:
- Meta grind backlash
- procedural sameness
- bad seed frustration
- overlong run
- unlock bloat
- late-game autopilot

에 대한 Postmortem / telemetry.

---

# GAP-ROGUE-012 — Tiny Rogues Design Evidence

현재 Studio Reference는 Production 사례다.

Tiny Rogues를 Primary Roguelike Design Evidence로 올리려면:
- run build formation
- reward choice
- meta
- run pacing
- encounter variation

에 관한 Design Source가 필요하다.

---

# 15. Additional References Needed

아래는 Research Target이며 현재 Core Evidence가 아니다.

# P0 — Hades

## 강화 대상
- `GC-ROGUE-001 Core Before Meta`
- `GC-ROGUE-006 Failure Learning`
- `GC-ROGUE-008 Restart Friction`
- `GC-ROGUE-010 Meta Type`

## Research Questions
- Narrative Reward와 Core Run Restart Motivation을 어떻게 분리하는가?
- Vertical Meta가 접근성과 Skill Mastery에 어떻게 작동하는가?
- Death → Hub → Next Run의 friction은 어떤 의도로 설계됐는가?

## 필요한 Evidence
- Developer talks
- postmortem
- run/restart telemetry if public
- player behavior analysis

---

# P0 — Spelunky

## 강화 대상
- Failure Learning
- Knowledge Progression
- Low Meta Power
- Systemic Variation

## Research Questions
- 영구 Power가 거의 없이도 Restart가 유지되는 이유는 무엇인가?
- 실패가 플레이어 Knowledge로 어떻게 전환되는가?

---

# P0 — The Binding of Isaac

## 강화 대상
- High Run Variance
- Unlock Dilution
- Item Interaction
- Knowledge Meta
- Bad Seed

## Research Questions
- 큰 Item Pool이 언제 Variety이고 언제 Dilution인가?
- 높은 Seed Variance에도 Replay가 유지되는 대응 구조는 무엇인가?

---

# P0 — Dead Cells

## 강화 대상
- Skill vs Meta
- Route
- Difficulty Scaling
- Run Pacing
- Restart Friction

## Research Questions
- Permanent Upgrade와 execution mastery의 관계는?
- 높은 Difficulty가 새 판단을 요구하는가, error margin을 줄이는가?

---

# P0 — Risk of Rain 2

## 강화 대상
- Escalation
- Time Pressure
- Item Stacking
- Late-run Autopilot
- Risk Timing

## Research Questions
- 시간 증가 난이도가 Route / Loot decision을 어떻게 바꾸는가?
- 후반 Power Explosion에서 Decision은 언제 사라지는가?

---

# P1 — Enter the Gungeon

## 강화 대상
- Weapon RNG
- Skill
- Resource
- Route
- Unlock Pool

## Research Questions
- 낮은 성능 Weapon / Unlock이 Pool Quality에 어떤 영향을 주는가?
- Skill이 RNG를 얼마나 상쇄하는가?

---

# P1 — Monster Train

## 강화 대상
- Run Commitment
- Reward Choice
- Roguelike Deckbuilding
- Encounter Pressure

Deckbuilding Core와 중복되는 부분은 Genre Cross-reference로 처리.

---

# P1 — Noita

## 강화 대상
- Extreme Systemic Variance
- Knowledge Progression
- Failure Attribution
- Build Experimentation
- Unrecoverable state

## Research Questions
- 높은 불확실성과 치명적 실패가 Knowledge progression으로 정당화되는 조건은 무엇인가?

---

# 16. Promotion Table

| ID | Name | Decision | Status | Confidence |
|---|---|---|---|---|
| GC-ROGUE-001 | Meta Progression Cannot Rescue a Weak Reset Loop | STRENGTHEN | **PROVISIONAL CORE** | VERY HIGH |
| GC-ROGUE-002 | Player-selectable Risk / Legible Trade-off | REFRAME | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-ROGUE-003 | Meaningful Run Variation Must Force Adaptation | NEW | **PROVISIONAL CORE** | VERY HIGH |
| GC-ROGUE-004 | Run Choices Must Create Path Dependence | NEW | **PROVISIONAL CORE** | HIGH |
| GC-ROGUE-005 | Escalation Must Preserve Decisions | NEW | **PROVISIONAL CORE** | HIGH |
| GC-ROGUE-006 | Failure Generates Next-run Hypothesis | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-ROGUE-007 | Run Length Must Justify Failure Cost | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-ROGUE-008 | Restart Friction | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-ROGUE-009 | Early-run Autopilot | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-ROGUE-010 | Meta Type Matches Product Promise | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-ROGUE-011 | Unlock Dilution | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-ROGUE-012 | Difficulty Re-tests Mastery | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-ROGUE-013 | Late-run Autopilot Must Be Bounded | NEW | KEEP AS CANDIDATE | MEDIUM |

---

# 17. Roguelike Reviewer Default Set

신규 Roguelike / Roguelite / Hybrid 기획 검토 시 우선 사용할 15개 질문.

## Q1 — Inclusion

> **Run Boundary → Variation → Adaptation → Commitment → Reset → Restart가 실제 하나의 반복 구조로 연결되는가?**

---

## Q2 — Core Before Meta

> **Meta를 고정하거나 제거해도 Run을 다시 시작하고 싶은가?**

관련:
`GC-ROGUE-001`

---

## Q3 — Meaningful Variation

> **Run마다 달라지는 요소가 실제 Strategy / Route / Build / Resource 판단을 바꾸는가?**

관련:
`GC-ROGUE-003`

---

## Q4 — Adaptation

> **플레이어는 미리 정한 공략을 실행하는가, 현재 조건을 읽고 계획을 수정하는가?**

관련:
`GC-ROGUE-003`

---

## Q5 — Run Commitment

> **현재 선택이 미래 Choice Value를 바꾸어 이번 Run의 History와 Identity를 만드는가?**

관련:
`GC-ROGUE-004`

---

## Q6 — Early Lock

> **초반 Reward / RNG 하나가 Run 결과를 지나치게 고정하지 않는가?**

관련:
`AP-ROGUE-005`

---

## Q7 — Failure Learning

> **실패 후 다음 Run에서 무엇을 다르게 할지 설명할 수 있는가?**

관련:
`GC-ROGUE-006`

---

## Q8 — RNG Response

> **Randomness에 준비·회피·복구·변환·Route 선택 등 대응 Channel이 있는가?**

관련:
`UC-DESIGN-004`

---

## Q9 — Optional Risk

> **Risk를 선택할 수 있다면 위험과 보상의 Trade-off가 읽히고, 거절도 합리적인가?**

관련:
`GC-ROGUE-002`

---

## Q10 — Early-run Repetition

> **매 Run 초반이 이미 해결한 Fixed Opening으로 반복되지 않는가?**

관련:
`GC-ROGUE-009`

---

## Q11 — Run Length / Failure Cost

> **Run 길이에 비해 중간 Decision Density와 실패 학습 가치가 충분한가?**

관련:
`GC-ROGUE-007`

---

## Q12 — Late-run Decision

> **Build / Engine 완성 후에도 새로운 판단이 남는가?**

관련:
`GC-ROGUE-005 / 013`

---

## Q13 — Meta / Unlock

> **Meta는 Core를 보완하는가, 약한 Core를 숫자로 통과시키는가? Unlock은 Variety인가 Dilution인가?**

관련:
`GC-ROGUE-001 / 010 / 011`

---

## Q14 — Difficulty

> **높은 난이도는 새로운 판단·행동을 요구하는가, 단순히 허용오차만 줄이는가?**

관련:
`GC-ROGUE-012`

---

## Q15 — Machine vs Human

> **Seed·수렴·Route·Meta dependency는 AI Tester로 측정하고, Restart Motivation·Freshness·Fairness·Replay Intent는 Human Test로 분리했는가?**

---

# 18. Default Metric Bundle

Metric은 Criteria가 아니다.

게임별 Threshold는 Validation Planner가 별도로 확정한다.

## Structural — Machine

- Run Completion Rate
- Run Length
- Failure Stage Distribution
- Late-run Failure Rate
- Encounter Distribution
- Reward Distribution
- Route Diversity
- Seed Outcome Variance
- State Diversity
- Run State Similarity
- Strategy Change Rate
- Route Change Rate
- Resource Reallocation Rate
- Context-triggered Action Shift
- Strategy Concentration
- Strategy Success Distribution
- Build Diversity
- Build Convergence
- Universal Strategy Rate
- Optional Risk Take Rate
- Elite / Dangerous Route Selection
- Retreat Rate
- Cash-out Rate
- Greed Failure Rate
- Risk Escalation Rate
- Recovery Option Usage
- RNG Response Usage
- Win Rate by Meta Level
- Run Duration by Meta Level
- Strategy Diversity by Unlock Level
- Unlock Usage Rate
- Early Action Sequence Concentration

## Observed Player Telemetry / Instrumented

- Restart Rate
- Early Abandon Rate
- Voluntary Run Abandon Rate
- Death → Next Run Start Rate
- Quit-after-Failure Rate

### Interpretation Rule

`Batch Runner가 다음 Seed를 자동 실행한 것`과 `플레이어가 실제로 재시작을 선택한 것`을 동일한 Restart 행동으로 취급하지 않는다.

AI Persona에 다음과 같은 명시적 의사결정 모델이 포함된 경우에만 Machine Simulation Candidate로 사용할 수 있다.

```text
Continue?
Restart?
Abandon?
```

그렇지 않다면 이 항목들은 **Human Prototype Test 또는 실제 Player Telemetry**에서 해석한다.

## Human

- Restart Motivation
- Failure Attribution
- Failure Learning
- RNG Fairness
- Run Freshness
- Strategy Identity
- Meta Motivation
- Perceived Fairness
- Replay Intent
- Session Fatigue
- Commitment vs Lock-in Perception
- Difficulty Perception

## Hybrid / Model-dependent

- Reset → Restart Friction
- Build Formation Timing
- First Major Risk Timing
- Structural Failure Cause ↔ Perceived Cause Agreement
- Bad-seed Failure Concentration
- Unrecoverable State Entry
- First Critical Mistake
- Permanent Power Contribution
- Unlock Dilution
- Run Pacing
- Early-run Repetition
- Last Meaningful Decision
- Autopilot Duration
- Late-run Decision Quality
- Meta Dependency Experience
- Run Variety Quality
- Failure Cost

---

# 19. Self-Review Result

## Check 1 — Random Generation ≠ Roguelike Core
**PASS**

Variation 자체가 아니라 Decision 변화와 Adaptation을 Core로 정의했다.

## Check 2 — Permadeath ≠ Genre Value
**PASS**

Reset 범위는 Conflict로 처리했으며 Permadeath를 필수 Core로 만들지 않았다.

## Check 3 — Meta ≠ Replayability
**PASS**

`GC-ROGUE-001`에서 Core Restart Motivation과 Meta를 분리했다.

## Check 4 — Content Count ≠ Variety
**PASS**

`AP-ROGUE-003`으로 명시했다.

## Check 5 — Variation → Decision
**PASS**

`GC-ROGUE-003`의 핵심 Rule로 설정했다.

## Check 6 — Universal RNG Duplicate
**PASS**

RNG 대응은 `UC-DESIGN-004`를 참조하고 별도 Roguelike Universal Rule로 복제하지 않았다.

## Check 7 — Deckbuilding / Management Duplicate
**PASS**

Run Reset / Variation / Restart와 직접 관련된 특수 조건만 남겼다.

## Check 8 — Subtype Overgeneralization
**PASS WITH GAPS**

Player-created Risk, Run Length, Meta Type, Difficulty 방식은 Candidate / Conflict로 유지했다.

## Check 9 — Vertical Meta always bad
**PASS**

Vampire Survivors를 Counter / Boundary로 보존했다.

## Check 10 — Knowledge / Skill / Stat Progression
**PASS**

Meta Type Candidate와 Conflict에서 분리했다.

## Check 11 — Machine → Replay Intent / Fun
**PASS**

Restart Motivation / Freshness / Fairness는 Human으로 유지했다.

## Check 12 — Run Length + Failure Cost
**PASS**

`GC-ROGUE-007`에서 함께 검토했다.

## Check 13 — Early / Late Autopilot
**PASS**

별도 Candidate / Anti-Pattern으로 분리했다.

## Check 14 — Underperforming Evidence Gap
**PASS**

`GAP-ROGUE-011`에 명시했다.

## Check 15 — Reviewer Usability
**PASS**

15개 Default Question으로 압축했다.

---

# 20. Final Position

현재 Studio OS Roguelike Knowledge Base에서 우선 `Provisional Core`로 사용할 항목은 4개다.

1. `GC-ROGUE-001 — Meta Progression Cannot Rescue a Weak Reset Loop`
2. `GC-ROGUE-003 — Meaningful Run Variation Must Force Adaptation`
3. `GC-ROGUE-004 — Run Choices Must Create Path Dependence`
4. `GC-ROGUE-005 — Escalation Must Preserve Decisions`

Candidate는 다음과 같다.

- `GC-ROGUE-002 — Player-selectable Risk`
- `GC-ROGUE-006 — Failure → Next-run Hypothesis`
- `GC-ROGUE-007 — Run Length / Failure Cost`
- `GC-ROGUE-008 — Restart Friction`
- `GC-ROGUE-009 — Early-run Autopilot`
- `GC-ROGUE-010 — Meta Type`
- `GC-ROGUE-011 — Unlock Dilution`
- `GC-ROGUE-012 — Difficulty Re-tests Mastery`
- `GC-ROGUE-013 — Late-run Autopilot`

이번 Extraction에서 가장 중요한 정리점은:

> **Roguelike의 반복성은 “랜덤 콘텐츠가 많다”가 아니라 `Run마다 Choice Value가 달라지고, 이전 선택이 Run Identity를 만들며, 압박이 증가해도 Adaptation이 계속 남는가`로 평가해야 한다.**

또한 `GC-ROGUE-001`은 매우 강하지만:

> Meta가 없어야 한다

는 Rule이 아니다.

정확히는:

> **Meta가 없어도 Core Run의 반복 이유를 설명할 수 있어야 한다.**

이다.

현재 가장 중요한 Evidence Gap은:

> **Failure Learning / Restart Telemetry / Early-Late Autopilot / Meta Dependency / Unlock Dilution / Underperforming Control**

이다.

따라서 다음 Reference 확장은 성공작 수를 늘리는 것보다:

> **왜 죽고도 다시 시작하는가?  
> 언제 Randomness가 Adaptation이 아니라 Bad Seed가 되는가?  
> 언제 Meta가 Motivation이고 언제 Bribe인가?  
> Run 초반과 후반은 언제 Autopilot으로 변하는가?**

에 실제 Postmortem / Telemetry가 존재하는 사례를 우선 조사하는 편이 효율적이다.

---

# 21. Source Trace

## Primary Roguelike / Roguelite Evidence
- REF-02 — FTL: Faster Than Light
- REF-04 — Slay the Spire
- REF-07 — Against the Storm
- REF-20 — Dicey Dungeons
- REF-12 — Vampire Survivors

## Secondary / Hybrid
- REF-18 — Loop Hero
- REF-27 — Tiny Rogues (`Production-heavy`)
- REF-34 — Peglin (`Production-heavy`)
- REF-36 — Brotato (`Production-heavy`)
- REF-06 — Darkest Dungeon

## Adjacent / Control
- REF-03 — Into the Breach
- REF-05 — Balatro
- REF-26 — Luck be a Landlord
- REF-32 — Patch Quest
- REF-33 — SNKRX
- REF-35 — Dome Keeper
- REF-28 — Thronefall

## Baseline
- STUDIO_CORE_CANDIDATES_v0.2
- Studio OS — Evidence-Based Core Extraction Master Prompt v0.2
- Studio OS — Roguelike / Roguelite Genre Core Deep Extraction Prompt v0.1

---

# 22. Traceability Rule

Core는 원본 Reference를 대체하지 않는다.

신규 프로젝트 Review에서 위험 신호가 발생하면:

```text
Genre Core
↓
Primary Reference
↓
Problem
↓
Solution
↓
Context
↓
Trade-off
↓
Current Project
```

순서로 다시 내려가 확인한다.

`ROGUELIKE_CORE_CANDIDATES_v0.1`은 Studio OS Reviewer가 Run-based 게임의 반복 구조를 빠르고 일관되게 평가하기 위한 압축된 Genre 판단 계층이다.
