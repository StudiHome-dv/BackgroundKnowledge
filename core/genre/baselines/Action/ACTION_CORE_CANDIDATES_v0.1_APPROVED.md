# ACTION_CORE_CANDIDATES_v0.1

**Studio OS — Action Genre Core Deep Extraction**  
**Document:** `ACTION_CORE_CANDIDATES_v0.1`  
**Status:** `APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE`  
**Purpose:** 신규 Combat Action / Stealth Action / Action Roguelite / Survivors-like / Twin-stick Action / Shooter Hybrid / Melee Action / Dodge-heavy Action / Movement-centric Action / Action RPG Hybrid 기획 평가용 Genre-specific Reviewer Knowledge Base  
**Baseline:** `STUDIO_CORE_CANDIDATES_v0.2`  
**Extraction Prompt:** `Studio OS — Action Genre Core Deep Extraction Prompt v0.1`  
**Deduplication Baselines:** `STRATEGY_CORE_CANDIDATES_v0.1`, `ROGUELIKE_CORE_CANDIDATES_v0.1`, `RPG_CORE_CANDIDATES_v0.1`, `SIMULATION_CORE_CANDIDATES_v0.1`  
**Provisional Genre Cores:** `NONE`  
**Candidates:** `GC-ACTION-001 ~ GC-ACTION-007`  
**Universal Strengthening:** `GC-ACTION-002 Evidence → UC-DESIGN-005 — Actionable Information`; `GC-ACTION-007 Evidence → UC-DESIGN-001 — Consequence Density over Input Count`  
**Canonical Parent Mapping:** `GC-ACTION-003 → UC-DESIGN-005 Outcome-time Specialization + Failure Attribution Cross-Genre Pattern`  
**Evidence Boundary:** `Stealth Action / Survivors-like / Compact Action 중심. Character Action / FPS / Fighting / Souls-like / Precision Platformer / Bullet Hell / Competitive PvP는 Additional Evidence 전까지 제한 적용.`  
**Pending:** `Additional Evidence / Prototype Validation / Internal Evidence`  
**Evidence Rule:** 현재 Direct Evidence는 Stealth Action / Survivors-like / compact action에 편중되어 있으므로 Character Action / FPS / Fighting / Souls-like / Precision Platformer / Bullet Hell / Competitive PvP 전체로 자동 일반화하지 않는다.

---

# 1. Executive Summary

이번 Deep Extraction의 핵심 결론은 다음과 같다.

1. **현재 Evidence만으로 신규 Action Provisional Genre Core를 승격하지 않는 것이 가장 안전하다.**
   - `REF-21 Mark of the Ninja`는 Action Design Evidence가 강하지만 핵심은 Detection / Sound / Visibility Readability이며 `UC-DESIGN-005 — Actionable Information`의 Action specialization 성격이 매우 강하다.
   - `REF-12 Vampire Survivors`는 Minimal Input / Movement / Auto Attack의 강한 사례지만 핵심 Lesson은 `UC-DESIGN-001 — Consequence Density over Input Count`와 Roguelike Build / Reward Loop에 크게 걸친다.
   - 현재 두 Primary 사례가 공통으로 지지하는 Action 고유 Mechanism은 아직 범용 Action Core로 승격하기에 충분히 넓지 않다.

2. Action은 다음과 같은 작업 정의가 가장 유용하다.

> **Player의 Timing / Position / Direction / Execution 입력이 짧은 Feedback Loop 안에서 World State와 위험에 직접 영향을 주고, 그 결과를 읽어 다음 입력을 수정하는 구조.**

3. 따라서 Action Reviewer의 기본 분석 단위는:

```text
Input
→ Character Response
→ World / Enemy Outcome
→ Feedback
→ Player Interpretation
→ Next Adjustment
```

다.

4. 이번 Extraction의 가장 중요한 Deduplication 결과는 다음이다.
   - `Action Depth Does Not Require High Input Count`
     → 독립 GC보다 `UC-DESIGN-001 Action specialization`.
   - `Critical Action States Must Be Readable in Time to Respond`
     → 독립 GC보다 `UC-DESIGN-005 Action specialization`.
   - `Uncertainty Needs Dodge / Guard / Reposition / Interrupt`
     → `UC-DESIGN-004 Action specialization`.
   즉 RPG와 마찬가지로:
     > 장르에서 자주 나타난다 ≠ 장르 전용 Core
     를 보존한다.

5. 현재 가장 유력한 Action Candidate는 다음 7개다.
   - `GC-ACTION-001 — Input Should Produce Predictable Controllable Response`
   - `GC-ACTION-002 — Critical Action States Need Timely Actionable Readability`
   - `GC-ACTION-003 — Execution Failures Need Legible Attribution`
   - `GC-ACTION-004 — Movement Should Change Immediate Threat / Opportunity State`
   - `GC-ACTION-005 — Commitment Needs Matching Risk / Reward`
   - `GC-ACTION-006 — Error Propagation Should Preserve Intended Recovery Structure`
   - `GC-ACTION-007 — Removed Input Must Leave Meaningful Action Agency Elsewhere`

6. 이 중 현재 가장 승격 가능성이 높은 것은 `GC-ACTION-001 / 003`이다.
   - 둘 모두 Action의 짧은 Feedback Loop와 직접 연결된다.
   - 그러나 현재 Reference Pool에는 Hades / Dead Cells / Sekiro / Celeste / DOOM Eternal 같은 Direct Action Design Evidence가 없으므로 Candidate 유지가 맞다.

7. `GC-ACTION-002`는 매우 강한 Reviewer Rule이지만 `UC-DESIGN-005` 중복 위험이 높다.
   - Action에서만 추가되는 특수성은:
     > Information이 보이는 것뿐 아니라 **Response Window 안에 실제 Execution으로 변환 가능해야 한다**
     는 점이다.
   - 따라서 현재 `UC specialization` Candidate로 유지한다.

8. `Mark of the Ninja`는 Action에서 Tier A로 승격한다.
   - 소리 / 시야 / 적 반응을 시각화.
   - Player가 계획하고 실패 원인을 학습하도록 만든다.
   - Stealth 난이도를 정보 은폐와 동일시하지 않는다.

9. `Vampire Survivors`도 Tier A로 사용하되 범위를 제한한다.
   - Auto Attack 이후에도:
     - Movement
     - Position
     - Collection Timing
     - Build
     가 Agency를 남긴다.
   - 그러나 이 사례를 근거로 모든 Action에서 공격 Input을 제거하거나 Minimal Input을 권장하지 않는다.

10. Tiny Rogues / Brotato / Patch Quest / Dome Keeper는 현재 Studio Reference가 Production 중심이므로 Tier B 이하로 유지한다.
    - Action Feature가 존재한다는 사실만으로 Direct Design Evidence Weight를 높이지 않는다.

11. Action에서 “Feel”은 직접 Core로 승격하지 않는다.
    - `Responsiveness`
    - `Hit Feel`
    - `Movement Feel`
    을 감상어로 사용하지 않고 다음으로 분해한다.

```text
Input Recognition
Response Start
Movement / Attack State
Contact
State Change
Audio / Visual / Motion Feedback
Control Recovery
Player Interpretation
```

12. Machine / AI Tester가 강하게 검증할 수 있는 것은:
    - Collision
    - State Transition
    - Action Usage
    - Threat / Detection State
    - Hit / Miss / Damage
    - Recovery
    - Position
    - Pattern Distribution
    - Error Chain
    이다.

13. Machine이 직접 판정하지 않는 것은:
    - 조작감이 좋다.
    - 타격감이 좋다.
    - 공정하게 느껴진다.
    - 반응할 수 있었다.
    - 공격이 무겁다 / 시원하다.
    - 움직임이 만족스럽다.

14. 특히 다음을 운영 규칙으로 고정한다.

```text
AI knew threat state
≠
Player saw threat
```

```text
AI dodged successfully
≠
Human had enough reaction opportunity
```

```text
Collision was correct
≠
Hit felt fair / satisfying
```

15. 현재 가장 큰 Evidence Gap은:
    - Input / Response Design Postmortem
    - Cancel / Buffer / Commitment
    - Melee Combat
    - Souls-like Telegraph
    - FPS Aim / Recoil
    - Fighting Frame / Recovery
    - Precision Movement
    - Hitbox / Hurtbox Readability
    - Human Response Timing
    - Hit Feedback
    - Stunlock / Recovery
    - Crowd Pressure
    - VFX Clarity
    - Underperforming Action Controls

16. 따라서 P0 추가 Reference가 RPG 못지않게 중요하다.
    - Hades
    - Dead Cells
    - Sekiro
    - DOOM Eternal
    - Celeste
    이 5개가 들어온 뒤 `GC-ACTION-001 / 003 / 005 / 006` 승격을 재심사하는 것이 가장 효율적이다.

---

# 2. Action Genre Definition

Studio OS에서 Action을:

> **실시간 입력이 많은 게임**

으로 정의하지 않는다.

기본 작업 정의:

> **Player의 Timing / Position / Direction / Execution 입력이 짧은 Feedback Loop 안에서 World State와 위험에 직접 영향을 주고, 그 결과를 즉시 읽어 다음 입력을 수정하는 구조.**

기본 구조:

```text
Perceive Threat / Opportunity
↓
Input
↓
Character Response
↓
World / Enemy Response
↓
Immediate Feedback
↓
State Changes
↓
Player Re-adjusts
↓
Next Input
```

핵심은:

```text
Input Frequency
≠
Action Depth
```

보다:

```text
Input
→ Response
→ Read
→ Adjust
```

의 반복 품질이다.

---

# 2.1 Action Inclusion Test

## A. Timing-sensitive Execution

Player Input Timing이 Outcome에 영향을 주는가?

---

## B. Direct Control

Player가 다음 중 일부를 직접 제어하는가?

- movement
- aiming
- attack
- defense
- dodge
- positioning
- jump
- parry
- interrupt

---

## C. Immediate State Change

Input 결과가 짧은 시간 안에 다음 State를 바꾸는가?

- position
- damage
- threat
- enemy state
- resource
- vulnerability
- detection

---

## D. Feedback

Player가 Input Outcome을 확인할 수 있는가?

---

## E. Adjustment

Player가 결과를 보고 다음 입력을 바꿀 수 있는가?

---

## F. Execution Error

실패 원인 중 Player Execution이 실제 역할을 하는가?

---

## G. Recovery / Continuation

작은 실수가:
- 즉시 종료
- 단기 disadvantage
- 누적 loss
- recovery opportunity

중 어떤 구조로 연결되는가?

---

# 3. Evidence Scope / Limitation

## 상대적으로 강한 영역

- Stealth Action
- Readable Detection / Threat
- Movement-focused Survivors-like
- Action Roguelite Hybrid
- Small / Compact Action
- Simplified-input Action

## 상대적으로 약한 영역

- Character Action
- Fighting Game
- FPS
- Competitive Shooter
- Souls-like
- Precision Platformer
- Hack-and-Slash
- Bullet Hell
- Rhythm Action
- Physics Combat
- Multiplayer PvP Action

## Boundary

현재 Candidate를:
- all-action timing law
- universal frame rule
- universal cancel rule
- universal hitbox rule

로 사용하지 않는다.

특히:
- Mark of the Ninja의 Stealth readability
- Vampire Survivors의 Minimal Input

을 서로 다른 Product Promise의 Action Game에 그대로 강제하지 않는다.

---

# 4. Input / Response / Outcome / Feedback 구분

Action Review에서 반드시 다음 층을 분리한다.

# 4.1 Input

Player가 실제로 무엇을 입력했는가?

예:
- direction
- attack
- dodge
- parry
- aim

---

# 4.2 Character Response

Game Character가 실제로 무엇을 했는가?

검토:
- action state
- movement start
- attack start
- queue
- buffer
- cancel
- lock

---

# 4.3 Outcome

World / Enemy State가 어떻게 바뀌었는가?

- hit
- miss
- block
- detection
- position
- damage
- stagger
- vulnerability

---

# 4.4 Feedback

Player에게 무엇이 전달되었는가?

- animation
- audio
- VFX
- UI
- enemy reaction
- camera
- hit stop
- state icon

---

# 4.5 Interpretation

Player가:

> **왜 성공 / 실패했는가?**

를 이해했는가?

---

# 4.6 Core Separation Rule

```text
Input occurred
≠
Desired Action executed
```

```text
Action executed
≠
Player understood result
```

```text
Damage happened
≠
Hit felt satisfying
```

```text
Telegraph existed
≠
Player had actionable reaction opportunity
```

---

# 5. Source Classification

# 5.1 Tier A — Primary Action Evidence

## REF-21 — Mark of the Ninja

**Subtype:** `Stealth Action / Readability-driven Action`  
**Evidence Strength:** VERY HIGH for Stealth Readability / Failure Attribution

### Strong Evidence Areas

- Detection Readability
- Sound Visualization
- Enemy Awareness
- Visibility
- Feedback
- Planning → Execution
- Failure Attribution
- Information / Action Coupling

### Key Source-derived Observation

Reference의 가장 강한 Lesson은:

> **스텔스 난이도는 정보를 숨기는 데서 만들 필요가 없다.**

그리고:
- 소리
- 시야
- 적 반응

을 시각화하면 Player가:
- 계획하고
- 실행하고
- 발각 원인을 학습

할 수 있다는 것이다.

### Action-specific Use

Strategy에서는 Information reference였지만 Action에서는:
- real-time movement
- timing
- detection transition
- execution failure
와 연결되므로 Primary로 사용한다.

### Boundary

이 사례는:
- melee commitment
- shooter recoil
- combo cancel
- hit feel
의 Primary Evidence가 아니다.

---

## REF-12 — Vampire Survivors

**Subtype:** `Movement-centric Survivors-like Action`  
**Evidence Strength:** VERY HIGH for Minimal Input / Residual Agency

### Strong Evidence Areas

- Minimal Direct Input
- Auto Attack
- Continuous Movement
- Positioning
- Enemy Density
- Spatial Pressure
- Reward Frequency
- Survival
- Escalation

### Key Source-derived Observation

Reference는:

> **플레이어 입력을 줄여도 위치·빌드·성장 판단을 유지하면 깊이를 보존할 수 있다.**

고 정리한다.

Primary Warning:

> **자동 공격과 몬스터 수만 복사하면 금방 지루해진다. 이동·빌드 선택·성장 리듬이 계속 판단과 보상을 제공하기 때문에 작동한다.**

### Action-specific Use

Roguelike / Build Progression은 별도 Core에 남긴다.

Action에서는:

> **공격 Input을 제거한 뒤에도 Movement / Position이 실제 Threat와 Survival State를 바꾸는가?**

만 사용한다.

### Boundary

Minimal Input은 Action의 우월한 형태가 아니다.

Character Action / Fighting / Shooter에서는:
- high input expression
자체가 Product Promise일 수 있다.

---

# 5.2 Tier B — Action / Hybrid Support

## REF-27 — Tiny Rogues

**Classification:** `TIER B / PRODUCTION-HEAVY ACTION SUPPORT`

Potential use:
- room combat
- dodge
- position
- enemy pattern

현재 Studio Reference는:
- Solo scope
- data/content expansion
중심이므로 Direct Action Core 승격 Evidence로 과대 사용하지 않는다.

---

## REF-36 — Brotato

**Classification:** `TIER B / PRODUCTION-HEAVY SURVIVORS SUPPORT`

Potential use:
- movement
- arena pressure
- density
- auto attack

현재 Reference는:
- solo production
- data modifiers
- reuse
중심.

Action pressure의 Direct Design Evidence는 약하다.

---

## REF-32 — Patch Quest

**Classification:** `TIER B / PRODUCTION-HEAVY ACTION HYBRID`

Potential use:
- twin-stick
- movement
- compact system
- enemy interaction

현재 가장 강한 Reference Axis는:
- Solo Scope Warning
- long development
이다.

---

## REF-35 — Dome Keeper

**Classification:** `TIER B / PRODUCTION-HEAVY HYBRID`

Potential use:
- movement
- combat / mining transition
- threat cycle
- timing

Direct Combat Feel / Telegraph evidence는 부족.

---

## REF-25 — Buckshot Roulette

**Classification:** `TIER C / CONTROL`

Use:
- compact feedback
- tension
- readable state

Pure continuous Action의 Primary Evidence로 사용하지 않는다.

---

# 5.3 Tier C — Adjacent / Control

- Into the Breach
- Invisible, Inc.
- FTL
- Dicey Dungeons
- Loop Hero

특정:
- information
- recovery
- risk
- state readability

비교에만 사용한다.

실시간 Execution이 약하거나 없는 사례를 Action Core 승격의 독립 Evidence로 사용하지 않는다.

---

# 6. Universal / Existing Genre Core Audit

# 6.1 UC-DESIGN-001 — Consequence Density over Input Count

## Action Specialization

다음을 별도 GC로 복제하지 않는다.

> Action Depth does not require many buttons.

Action에서는:

> **Input 하나가 Position / Risk / Contact / Vulnerability / Timing에 어떤 즉시 결과를 만드는가?**

를 본다.

### Evidence

Vampire Survivors가 매우 강하다.

## Decision

`GC-ACTION-007 Removed Input`은 Candidate로 유지하되 Universal Strengthening Evidence로도 보낸다.

---

# 6.2 UC-DESIGN-004 — Uncertainty Requires Response Agency

Action에서는 대응 Verb가:

- movement
- dodge
- guard
- reposition
- interrupt
- retreat

형태로 나타난다.

새 Action Core로 복제하지 않는다.

---

# 6.3 UC-DESIGN-005 — Actionable Information

Action에서 핵심 specialization:

> **Threat / Detection / Contact Information이 Player에게 보일 뿐 아니라 실제 Response Window 안에 Execution으로 변환 가능해야 한다.**

Mark of the Ninja가 강한 Evidence다.

## Decision

`GC-ACTION-002`는 독립 Provisional보다 `UC-DESIGN-005 Action specialization` Candidate가 적절하다.

---

# 6.4 Strategy Deduplication

Position / Target Priority 자체를 복제하지 않는다.

Action에서는:

> 실시간 Timing / Exposure / Escape / Contact와 결합된 Position

만 사용한다.

---

# 6.5 Roguelike Deduplication

- Build
- Reset
- Meta
- Run Variation

을 복제하지 않는다.

Vampire Survivors는 Action layer만 사용한다.

---

# 6.6 RPG Deduplication

Player Skill / Character Skill은 RPG Candidate에 이미 존재.

Action에서는:
> direct execution loop
만 본다.

---

# 7. Provisional Action Cores

## Result

**현재 신규 Provisional Action Core 승격 없음.**

### Reason

현재 가장 강한 발견이 각각:

- `UC-DESIGN-001`
- `UC-DESIGN-005`

의 Action specialization에 해당한다.

Action 고유 Candidate인:
- Input Response
- Execution Attribution
- Commitment / Recovery

는 현재 Direct Reference가 부족하다.

Promotion 기준의:
1. 두 독립 Action Evidence
2. 동일 Mechanism
3. Universal / adjacent deduplication
4. Subtype boundary
5. validation path

를 보수적으로 적용하면 아직 승격하지 않는 편이 정확하다.

이는 Action Core가 없다는 뜻이 아니라:

> **현재 Reference Library로 증명된 Action 전용 Core가 아직 부족하다**

는 뜻이다.

---

# 8. Action Core Candidates

# GC-ACTION-001 — Input Should Produce Predictable Controllable Response

**Status:** `CANDIDATE`  
**Origin:** `NEW GENRE CORE`

## Pattern

Action에서는 Player가 입력을 통해 즉시 Character State를 바꾸려 한다.

그런데:
- context
- animation
- queue
- lock
- input ambiguity

때문에 예상하지 않은 행동이 나오면
Execution Error와 Control Error를 구분하기 어려워진다.

## Rule Candidate

> **Action의 핵심 직접 조작은 동일한 Relevant State에서 Player가 예측 가능한 Character Response를 만들어야 하며, 의도적 Commitment / Buffer / Contextual Action은 Player가 학습 가능한 Rule로 일관되게 작동해야 한다.**

## Mechanism

```text
Input
↓
Predictable Action State
↓
World Outcome
↓
Feedback
↓
Next Input
```

문제 구조:

```text
Input
↓
Unexpected Contextual Response
↓
Failure
↓
Player cannot tell:
execution mistake?
control rule?
animation lock?
```

## Primary Evidence

현재 Mark of the Ninja / Vampire Survivors는:
- readable control goals
- minimal movement loop
를 간접 지지하지만

Buffer / Cancel / Input Response를 직접 분석하는 Source는 부족하다.

## Counter Evidence

- deliberate animation commitment
- context-sensitive action
- fighting command priority
는 복잡할 수 있다.

Predictable = Instant가 아니다.

## Applies To

강하게:
- Melee Action
- Shooter
- Precision Action
- Action Roguelite
- Movement Action

조건부:
- Survivors-like

## Boundary

Responsiveness를:
> animation이 즉시 취소된다
로 정의하지 않는다.

Predictability와 commitment는 공존 가능하다.

## Candidate Metric — Structural / Instrumented

- Input → Action State Mapping
- Contextual Action Collision
- Repeated Input Rate
- Buffer Usage
- Cancel Usage
- Input during Lock State
- Failed Command Candidate

`Failed Command`는 Formal Definition 필요.

## Human

- Control Intent
- Responsiveness
- Movement Confidence

## AI Tester Applicability

MEDIUM-HIGH for state mapping.  
Human required for feel.

## Confidence

**MEDIUM**

## Reviewer Action

핵심 Action마다:

> **“Player가 이 Input을 했을 때 어떤 State에서 어떤 Response가 나오는가?”**

를 명시한다.

---

# GC-ACTION-002 — Critical Action States Need Timely Actionable Readability

**Status:** `CANDIDATE`  
**Origin:** `UC-DESIGN-005 ACTION SPECIALIZATION`

## Pattern

Threat가 보인다는 사실만으로 충분하지 않다.

Action에서는:

```text
Threat cue
↓
Player perceives
↓
interprets
↓
selects response
↓
executes
```

가 실제 danger window 안에 들어가야 한다.

## Rule Candidate

> **Action에서 핵심 Threat / Detection / Vulnerability State는 Product Promise에 필요한 수준으로 읽혀야 하며, 읽은 정보가 실제 Response Window 안에서 Movement / Dodge / Guard / Interrupt 등으로 변환 가능해야 한다.**

## Primary Evidence

### Mark of the Ninja

가장 강한 Evidence.

- sound visualization
- sight
- enemy reaction
- detection state
를 명확하게 보여
Player가 계획하고 실패 원인을 학습하게 한다.

## Secondary Evidence

### Vampire Survivors

적 밀도와 공간 압력은 Movement를 통해 지속적으로 읽고 대응해야 하는 구조.

다만 Source는 Telegraph timing보다 minimal input / reward loop가 강하다.

## Counter Evidence

- Horror
- surprise attack
- high-precision mastery
에서는 일부 정보 불완전성이 의도될 수 있다.

## Duplicate Risk

`UC-DESIGN-005`와 매우 강하게 겹친다.

## Candidate Metric — Structural / Simulation

- Threat State Definition
- Telegraph State
- Threat → Response Opportunity
- Detection State Transition
- Threat → Dodge / Movement Response
- Unavoidable Threat Candidate

마지막 두 항목의 해석은 model-dependent 가능.

## Human

- Threat Recognition
- Reaction Opportunity
- Perceived Fairness
- Damage Source Recognition

## AI Tester Applicability

HIGH structurally.  
LOW for Human response sufficiency.

## Confidence

**VERY HIGH as UC specialization / LOW need for independent GC**

## Reviewer Action

Threat마다:

> **“언제 알 수 있고, 알게 된 뒤 어떤 Action이 아직 가능한가?”**

를 묻는다.

---

# GC-ACTION-003 — Execution Failures Need Legible Attribution

**Status:** `CANDIDATE`  
**Origin:** `NEW GENRE CORE / UC-DESIGN-005 OUTCOME-TIME SPECIALIZATION + FAILURE ATTRIBUTION CROSS-GENRE PATTERN`

## Pattern

Action failure는 짧은 시간에 발생한다.

Player가 실패 원인을:
- telegraph miss
- bad position
- late dodge
- early dodge
- attack commitment
- wrong target
- control mismatch

중 어느 것인지 구분할 수 없다면 학습 Loop가 약해진다.

## Rule Candidate

> **Execution-heavy Action에서 중요한 실패는 Player가 최소한 하나의 actionable 원인으로 되짚을 수 있어야 한다. Failure Attribution이 없는 처벌은 mastery learning을 약화시킬 수 있다.**

## Primary Evidence

### Mark of the Ninja

Reference의 가장 직접적 Lesson 중 하나.

소리 / 시야 / 적 반응을 명확히 해:
- 왜 발각됐는지
- 무엇을 바꿔야 하는지
학습 가능하게 한다.

## Secondary Evidence

Vampire Survivors는:
- position
- density
- movement
이 survival outcome과 연결되는 보조 사례지만 Failure Attribution Source는 상대적으로 약하다.

## Counter Evidence

- chaos fantasy
- party brawler
- spectacle survival
에서 완전한 cause attribution이 Product Promise의 중심이 아닐 수 있다.

## Candidate Metric

### Structural / model-dependent
- Damage Cause Classification
- Detection Cause Classification
- First Critical Mistake
- Error Propagation Source

### Player Telemetry
- Death Cause Selection / Report
- Retry after Failure
- Playback / inspect if present

### Human
- Failure Attribution
- Damage Source Recognition
- “다음 시도에서 무엇을 바꿀 것인가?”

## AI Tester Applicability

HIGH for event trace.  
Human required for explanation quality.

## Confidence

**HIGH for stealth / precision action, MEDIUM for all Action**

## Reviewer Action

실패 이벤트마다:

> **“Game log가 아는 원인과 Player가 이해할 수 있는 원인이 같은가?”**

를 분리한다.

---

# GC-ACTION-004 — Movement Should Change Immediate Threat / Opportunity State

**Status:** `CANDIDATE`

## Pattern

Movement-centric Action에서 이동은:
- 화면을 가로지르는 기능
가 아니라:
- 안전 공간
- attack opportunity
- detection
- range
- escape route
를 바꾸는 핵심 Action이다.

## Rule Candidate

> **Movement를 핵심 Action Verb로 제시한다면 Position 변화가 짧은 Feedback Loop 안에서 Threat / Contact / Attack / Escape Opportunity 중 일부를 실제로 바꾸어야 한다. 움직임의 빈도와 움직임의 가치가 같은 것은 아니다.**

## Primary Evidence

### Vampire Survivors

Auto Attack 이후 직접 남는 핵심 Action은 Movement다.

Movement가:
- enemy contact
- density exposure
- pickup route
- survival
을 바꾼다.

## Secondary Evidence

### Mark of the Ninja

Movement / placement가:
- visibility
- noise
- detection
에 영향을 준다.

## Counter Evidence

Stationary shooter / rhythm action 등 Movement 비중이 낮은 Action도 존재한다.

## Applies To

- Survivors-like
- Stealth Action
- Twin-stick
- Bullet Hell
- Melee / Shooter with spatial play

Subtype-dependent.

## Candidate Metric

### Simulation
- Position Distribution
- Movement Distance
- Time Stationary
- Contact Frequency

### Simulation / model-dependent
- Position → Damage Relationship
- Movement → Survival Relationship
- Safe-space Ratio
- Escape Lane Availability

### Human
- Movement Value
- Movement Confidence

## Confidence

**MEDIUM-HIGH for Movement-centric Action**

---

# GC-ACTION-005 — Commitment Needs Matching Risk / Reward

**Status:** `CANDIDATE`

## Pattern

공격 / dodge / reload / heavy move의 commitment는:
- weight
- tension
- anticipation
를 만들 수 있다.

하지만:
- control loss만 늘고
- benefit / identity / tactical value가 없으면
불필요한 friction이 될 수 있다.

## Rule Candidate

> **Action Commitment를 사용할 경우 Lock / Recovery / Cancel 제한이 Product Fantasy와 Risk / Reward를 실제로 만들어야 한다. Commitment가 단순 입력 지연이나 animation tax로만 작동하는지 검토한다.**

## Evidence

현재 Direct Source가 부족하다.

Mark of the Ninja와 Vampire Survivors는 이 축의 Primary가 아니다.

## Counter Evidence

High-cancel Character Action은:
- expression
- combo
- recovery
가 핵심일 수 있다.

Heavy Action은:
- commitment
- anticipation
이 핵심일 수 있다.

## Candidate Metric

### Structural
- Lock State

### Structural / model-dependent
- Commitment
- Cancel Window
- Recovery Window

### Simulation / Telemetry
- Action during Lock
- Cancel Usage
- Recovery State Duration
- Punishment after Commitment

### Human
- Control Intent
- Commitment Quality
- Responsiveness

## Confidence

**LOW-MEDIUM**

## Promotion Blocker

Hades / Dead Cells / Sekiro / DMC / Fighting evidence 필요.

---

# GC-ACTION-006 — Error Propagation Should Preserve Intended Recovery Structure

**Status:** `CANDIDATE`

## Pattern

작은 실수 후:

```text
Hit
→ short disadvantage
→ recovery
```

일 수도 있고:

```text
Hit
→ stun
→ second hit
→ lock
→ death
```

일 수도 있다.

어느 쪽도 자동으로 나쁘지 않지만 Product Promise와 맞아야 한다.

## Rule Candidate

> **Action에서 첫 Execution Error가 이후 입력 가능성과 실패 확률을 어떻게 변화시키는지 명시하고, 의도한 Punishment / Recovery 구조와 실제 Error Chain이 일치하는지 검증한다.**

## Evidence

Mark of the Ninja는 발각 후 state transition을 학습하는 보조 Evidence.

현재 Direct melee / shooter recovery evidence 부족.

## Candidate Metric

### Simulation / model-dependent
- Error Propagation Depth
- Stunlock Chain
- Recovery Window
- Unavoidable Follow-up Candidate

### Simulation
- Consecutive Hit Chain
- Time between Hits
- Recovery Action Usage
- Time to Safe State

### Human
- Recovery Perception
- Error Fairness

## Confidence

**MEDIUM-LOW**

---

# GC-ACTION-007 — Removed Input Must Leave Meaningful Action Agency Elsewhere

**Status:** `CANDIDATE`  
**Origin:** `UC-DESIGN-001 SPECIALIZATION / UC-RECLASS CANDIDATE`

## Pattern

Action 입력을 줄이는 것은:
- accessibility
- focus
- scope
를 개선할 수 있다.

하지만 제거된 Input이 실제 Agency까지 제거할 수 있다.

## Rule Candidate

> **핵심 직접 Input을 자동화하거나 제거할 경우, Player가 여전히 Timing / Movement / Position / Target / Route 등 다른 Action 축에서 의미 있는 상태 변화를 만들 수 있는지 검토한다.**

## Primary Evidence

### Vampire Survivors

가장 강한 Evidence.

Attack Input을 제거하지만:
- continuous movement
- positioning
- collection
이 survival을 바꾼다.

## Secondary / Adjacent

Loop Hero 같은 indirect control 사례는 Action이 아니므로 Universal reclass 참고만 한다.

## Duplicate Risk

`UC-DESIGN-001`.

따라서 독립 Action Core보다:
`UC-DESIGN-001 Action specialization`
가능성이 높다.

## Candidate Metric

- Direct Input Count
- Movement / Position Action Distribution
- Auto-resolved Action Rate
- Player-triggered State Change Rate
- Residual Action Diversity

`Meaningful Agency`는 Human / Hybrid.

## Human

- Action Agency
- Control Fatigue
- “내가 실제로 무엇을 결정하고 있는가?”

## Confidence

**VERY HIGH as specialization / LOW need for independent GC**

---

# 9. Action Anti-Patterns

# AP-ACTION-001 — More Buttons = More Depth

## Trigger
Input 수 / Combo 수를 Action Depth의 직접 증거로 사용.

## Consequence
- cognitive load
- input fatigue
- unused commands

## Evidence
Vampire Survivors가 강한 반례.

## Detection
- Action Usage Concentration
- Low-use Action Rate
- Context-specific Action Shift
- Human control burden

## Mitigation
버튼마다:
> 어떤 다른 Threat / Timing / State 문제를 해결하는가?
를 정의.

---

# AP-ACTION-002 — Input without Predictable Response

## Trigger
같은 Relevant State의 같은 Input이 학습 불가능한 방식으로 다른 Response를 생성.

## Consequence
Execution skill보다 control ambiguity가 결과 지배.

## Detection
- Input → State mapping
- contextual collision
- repeated corrective input
- human control intent mismatch

## Mitigation
priority / buffer / context rule 명시.

---

# AP-ACTION-003 — Animation before Control

## Trigger
Animation fidelity를 위해 Player input / state control이 설명 없이 무시됨.

## Consequence
Responsiveness perception 저하.

## Boundary
Commitment-heavy action은 예외 가능.

## Detection
- input during lock
- cancel availability
- human response complaint

## Mitigation
Product Promise에 맞는 commitment와 feedback.

---

# AP-ACTION-004 — Telegraph without Response Window

## Trigger
공격 전 Cue는 존재하지만 실제 회피 / 방어 Timing이 사실상 불가능.

## Consequence
“보여줬다”와 “대응 가능했다” 혼동.

## Detection
- threat cue timing
- action start
- available escape
- reaction sensitivity model

## Mitigation
telegraph / range / movement / recovery state 재조정.

---

# AP-ACTION-005 — Invisible Threat State

## Trigger
hit / detection / vulnerability 원인이 보이지 않음.

## Evidence
Mark of the Ninja의 반대 사례.

## Detection
- unexplained damage
- detection cause
- damage source recognition

## Mitigation
필요한 cue / state feedback 추가.

---

# AP-ACTION-006 — Feedback without State Change

## Trigger
Screen shake / sound / VFX는 강하지만 실제 enemy state change가 미미.

## Consequence
Impact presentation이 mechanical value와 분리.

## Detection
- effect trigger vs damage / stagger / displacement
- human hit confirmation vs actual state

## Mitigation
Presentation과 gameplay consequence를 구분해 설계.

---

# AP-ACTION-007 — State Change without Feedback

## Trigger
실제:
- block
- armor
- hit
- vulnerability
가 변했지만 Player가 구분 불가.

## Consequence
learning / targeting / mastery 약화.

## Detection
- state transition without presentation mapping
- human state recognition

## Mitigation
audio / motion / VFX / UI 중 필요한 channel 제공.

---

# AP-ACTION-008 — Hitbox / Animation Mismatch

## Trigger
보이는 범위와 actual collision이 반복적으로 불일치.

## Consequence
fairness / trust 저하.

## Detection
- collision trace
- animation state
- player hit report

## Mitigation
presentation / collision alignment 또는 learnable consistent rule.

---

# AP-ACTION-009 — Stunlock Removes Recovery

## Trigger
작은 실수 후 긴 Control Loss.

## Consequence
첫 error 이후 후속 input의 의미 소멸.

## Boundary
Fighting combo / intentional punish는 예외.

## Detection
- consecutive hit chain
- input-locked duration
- recovery opportunity

## Mitigation
Product Promise에 맞는 escape / invulnerability / knockback / reset.

---

# AP-ACTION-010 — Enemy Count = Difficulty

## Trigger
적 수만 증가.

## Consequence
새 Pattern / Position judgment보다 화면 부담과 성능 부하만 증가.

## Evidence
Vampire Survivors도 Enemy Count만으로 작동하는 것이 아니라 movement / density / reward structure가 함께 존재한다.

## Detection
- density vs movement policy
- escape lane
- threat overlap
- human visual clarity

## Mitigation
count보다 spatial pattern / speed / combination / lane pressure 검토.

---

# AP-ACTION-011 — Damage Sponge as Escalation

## Trigger
Enemy HP만 증가.

## Consequence
같은 execution 반복 시간만 증가.

## Detection
- time-to-kill
- strategy / action shift by difficulty

## Mitigation
필요하면:
- pattern
- range
- mix
- timing
변화.

---

# AP-ACTION-012 — Cooldown Piano

## Trigger
Skill은 많지만 cooldown마다 누르는 것이 최적.

## Consequence
Decision보다 routine execution.

## Detection
- skill use immediately on cooldown
- low context-specific usage
- action concentration

## Mitigation
resource / exposure / timing / target 차이.

---

# AP-ACTION-013 — Movement without Tactical Value

## Trigger
계속 움직이지만 position이 threat / opportunity를 거의 바꾸지 않음.

## Consequence
busy input.

## Detection
- position → outcome relation
- stationary vs moving outcome

## Mitigation
range / lane / detection / escape / pickup relation 강화 또는 movement 축소.

---

# AP-ACTION-014 — Auto Attack without Residual Agency

## Trigger
공격을 자동화했지만:
- movement
- position
- target
- route
판단도 약함.

## Evidence
Vampire Survivors Primary Warning의 핵심.

## Detection
- player-triggered state change
- movement policy impact
- human agency

## Mitigation
제거된 input을 되돌리기 전에 남은 action decision이 충분한지 먼저 검토.

---

# AP-ACTION-015 — VFX Obscures Threat

## Trigger
Player attack effect가 enemy cue / projectile / hit source를 가림.

## Consequence
Power spectacle가 threat readability를 파괴.

## Detection
- threat visibility state
- effect overlap
- human missed cue report

## Mitigation
layering / contrast / effect budget / opacity.

---

# AP-ACTION-016 — Failure without Attribution

## Trigger
죽음 / detection / hit은 발생했지만 원인을 설명하기 어려움.

## Evidence
Mark of the Ninja 반대 사례.

## Detection
- death cause report
- mismatch between actual and perceived cause

## Mitigation
failure trace / cue / replay / damage source feedback.

---

# 10. Conflicting Findings

# CF-ACTION-001 — Responsiveness vs Commitment

## High responsiveness / cancel
- fluidity
- recovery
- expression

## Commitment
- weight
- anticipation
- risk

## Resolution
Instant response가 항상 우월하지 않다.

핵심:
> Player가 commitment rule을 예측하고 그것이 fantasy / risk를 지지하는가?

---

# CF-ACTION-002 — Precision vs Forgiveness

작은 hitbox / tight timing은:
- mastery
를 만들 수 있지만
- accessibility
- readability
를 낮출 수 있다.

Universal threshold 금지.

---

# CF-ACTION-003 — High Input vs Minimal Input

## High Input
Character Action / Fighting:
- expression
- execution depth

## Minimal Input
Vampire Survivors:
- movement / position / build focus

## Resolution
Button count가 아니라 residual / intended agency를 평가.

---

# CF-ACTION-004 — Telegraph Clarity vs Surprise

모든 threat를 완전 공개할 필요는 없다.

Hidden variable:
- mastery
- horror
- reaction
- prediction
Fantasy.

---

# CF-ACTION-005 — Speed vs Readability

빠른 게임이 좋은 Action이라는 규칙 없음.

속도가 올라갈수록:
- perception
- decision
- execution
window가 함께 변한다.

---

# CF-ACTION-006 — Crowd Density vs Individual Enemy Complexity

많은 단순 Enemy와 적은 복잡 Enemy는 다른 pressure model.

Vampire Survivors를 melee duel에 강제하지 않는다.

---

# CF-ACTION-007 — Player Control vs Animation Fidelity

Animation priority가:
- weight
- spectacle
를 만들 수 있지만
- precise direct control
을 줄일 수 있다.

Product Promise에 종속.

---

# CF-ACTION-008 — Recovery vs Punishment

강한 punish는 mastery fantasy를 만들 수 있다.

Recovery window는 learning / continuity를 지원할 수 있다.

둘 중 하나가 Universal 정답이 아니다.

---

# 11. Structural / Simulation Validation Map

# 11.1 Input Metrics

| Metric | Type |
|---|---|
| Input Frequency | Player Telemetry |
| Action Usage | Simulation / Telemetry |
| Action Concentration | Simulation |
| Input → State Transition | Structural / Instrumented |
| Repeated Input Rate | Player Telemetry |
| Cancel Usage | Instrumented / Simulation |
| Buffer Usage | Instrumented / Simulation |

---

# 11.2 Response Metrics

| Metric | Type |
|---|---|
| Action Start State | Structural |
| Action End State | Structural |
| Recovery State | Structural |
| Lock State | Structural |
| Cancel Window | Structural / model-dependent |
| Movement State Transition | Structural / Simulation |

실제 frame / ms는 project instrumentation이 있을 때만 사용한다.

---

# 11.3 Movement Metrics

| Metric | Type |
|---|---|
| Position Distribution | Simulation / Telemetry |
| Movement Distance | Simulation / Telemetry |
| Direction Change | Simulation / Telemetry |
| Dodge Usage | Simulation / Telemetry |
| Dash Usage | Simulation / Telemetry |
| Time Stationary | Simulation |
| Escape Route Usage | Simulation / model-dependent |

---

# 11.4 Threat Metrics

| Metric | Type |
|---|---|
| Threat Count | Simulation |
| Threat Density | Simulation |
| Threat Overlap | Simulation / model-dependent |
| Telegraph State | Structural |
| Threat → Hit Rate | Simulation |
| Threat → Dodge Rate | Simulation |
| Unavoidable Threat Candidate | Simulation / model-dependent |

---

# 11.5 Combat Metrics

| Metric | Type |
|---|---|
| Attack Usage | Simulation / Telemetry |
| Hit Rate | Simulation / Telemetry |
| Miss Rate | Simulation / Telemetry |
| Damage Distribution | Simulation |
| Kill Rate | Simulation |
| Target Distribution | Simulation / Telemetry |
| Overkill | Simulation |
| Interrupt | Simulation |
| Block | Simulation |
| Parry | Simulation |

Subtype-dependent.

---

# 11.6 Damage-taken Metrics

| Metric | Type |
|---|---|
| Hit Source | Simulation |
| Hit Direction | Simulation |
| Damage Cause | Structural / model-dependent |
| Consecutive Hit Chain | Simulation |
| Time between Hits | Simulation |
| Death Cause | Structural / model-dependent |

---

# 11.7 Recovery Metrics

| Metric | Type |
|---|---|
| Recovery Action Usage | Simulation / Telemetry |
| Time to Safe State | Simulation / model-dependent |
| Hits after First Error | Simulation / model-dependent |
| Escape after Damage | Simulation |
| Heal / Guard / Dodge after Hit | Simulation / Telemetry |

---

# 11.8 Spatial Metrics

| Metric | Type |
|---|---|
| Safe-space Ratio | Structural / model-dependent |
| Enemy Distance Distribution | Simulation |
| Threat Direction Distribution | Simulation |
| Position → Damage Relationship | Simulation / model-dependent |
| Movement → Survival Relationship | Simulation / model-dependent |

---

# 11.9 Stealth Metrics

| Metric | Type |
|---|---|
| Detection State Transition | Simulation |
| Detection Cause | Structural / model-dependent |
| Time in Suspicion | Simulation |
| Alert Trigger | Simulation |
| Escape after Detection | Simulation |
| Re-detection | Simulation |
| Noise Action Usage | Simulation / Telemetry |

---

# 11.10 Survivors-like Metrics

| Metric | Type |
|---|---|
| Enemy Density | Simulation |
| Movement Path | Simulation |
| Time Encircled | Simulation / model-dependent |
| Escape Lane Availability | Simulation / model-dependent |
| Contact Frequency | Simulation |
| Damage by Density State | Simulation / model-dependent |
| Movement Policy by Build | Simulation / model-dependent |

---

# 12. Action Tester Profile Map

AI Tester가 Human reflex를 그대로 재현한다고 가정하지 않는다.

# P-ACTION-001 — Aggressive

Policy:
- approach
- attack
- target pressure

Purpose:
- aggression viability
- overcommit punishment

---

# P-ACTION-002 — Defensive

Policy:
- distance
- guard
- dodge
- safe-space preference

Purpose:
- defensive viability
- low-risk dominance

---

# P-ACTION-003 — Mobility

Policy:
- continuous movement
- reposition
- flank / escape

Purpose:
- movement value
- route pressure
- contact avoidance

---

# P-ACTION-004 — Greedy Damage

Policy:
- damage uptime
- minimal retreat
- late dodge

Purpose:
- DPS dominance
- commitment punishment

---

# P-ACTION-005 — Survival

Policy:
- damage minimization
- escape
- heal / safety

Purpose:
- recoverability
- safe strategy dominance

---

# P-ACTION-006 — Explorer

Policy:
저사용:
- action
- route
- movement pattern
- weapon
탐색.

Purpose:
- dead action
- hidden viable strategy
- action coverage

---

# 13. Human Validation Map

# H-ACTION-001 — Control Intent

> **입력한 행동이 의도한 대로 나갔다고 느끼는가?**

---

# H-ACTION-002 — Responsiveness

> **조작과 Character 반응 사이가 답답하게 느껴지는가?**

Human-only component 포함.

---

# H-ACTION-003 — Movement Confidence

> **원하는 위치로 정확히 이동할 수 있다고 느끼는가?**

---

# H-ACTION-004 — Threat Recognition

> **무엇이 위험한지 필요한 시점에 알 수 있었는가?**

---

# H-ACTION-005 — Reaction Opportunity

> **위험을 본 뒤 실제 대응할 기회가 있었다고 느끼는가?**

---

# H-ACTION-006 — Failure Attribution

> **왜 맞거나 죽었는지 설명할 수 있는가?**

---

# H-ACTION-007 — Hit Confirmation

> **공격이 맞았는지 즉시 알 수 있는가?**

---

# H-ACTION-008 — Impact / Hit Feel

> **공격이 실제로 상대에게 영향을 줬다고 느끼는가?**

Human 중심.

---

# H-ACTION-009 — Damage Source Recognition

> **어디에서 피격됐는지 알 수 있었는가?**

---

# H-ACTION-010 — Recovery Perception

> **실수 후 다시 통제권을 회복할 수 있었다고 느끼는가?**

---

# H-ACTION-011 — Movement Value

> **움직임 때문에 위험과 기회가 실제로 바뀌었다고 느끼는가?**

---

# H-ACTION-012 — Visual Clarity

> **Player VFX / Enemy VFX 때문에 중요한 Threat를 놓치지 않았는가?**

---

# H-ACTION-013 — Control Fatigue

> **입력 반복 자체가 피로한가?**

---

# H-ACTION-014 — Action Fantasy

Subtype별:
- ninja
- survivor
- shooter
- swordsman
등의 Fantasy가 direct control에서 전달되는가?

---

# H-ACTION-015 — Perceived Fairness

> **실패가 자신의 판단 / 실행 결과라고 납득되는가?**

---

# 14. AI Tester Interpretation Limits

Machine이 강한 영역:

```text
Collision
Action state
Movement state
Threat state
Detection
Hit / miss
Damage
Recovery
Position
Pattern
Distribution
Error chain
```

Machine이 직접 결론내리지 않는 영역:

- 조작감이 좋다.
- 타격감이 좋다.
- 무게감이 있다.
- 공정하다.
- 반응하기 충분했다.
- 시원하다.
- 움직임이 만족스럽다.
- 피로하지 않다.

---

# 14.1 Reaction Model Rule

AI Tester가 Telegraph 발생 즉시 완벽하게 회피하면:

> Human Difficulty Evidence가 아니다.

Sensitivity Test로 다음을 변수화할 수 있다.

- reaction delay
- perception probability
- input error probability
- decision policy

하지만:

```text
Persona reaction delay
≠
Actual human reaction time
```

로 취급한다.

---

# 14.2 State Knowledge Rule

```text
AI knew threat state
≠
Player saw threat
```

```text
AI executed dodge
≠
Human had enough response window
```

```text
Collision resolved correctly
≠
Hit felt fair
```

Simulation / Player Telemetry / Human을 분리한다.

---

# 15. Scale Handoff Candidates

# SCALE_HANDOFF-ACTION-001 — Animation State Matrix

```text
Action
× Direction
× Weapon
× Character
× State
```

조합이 Animation 제작 / QA를 폭증시킨다.

---

# SCALE_HANDOFF-ACTION-002 — Hitbox / Hurtbox QA

```text
Attack
× Enemy
× Animation
× Position
× State
```

Collision QA 증가.

---

# SCALE_HANDOFF-ACTION-003 — Enemy Pattern Matrix

```text
Enemy
× Attack
× Difficulty
× Arena
× Player Ability
```

패턴 조합 테스트 폭증.

---

# SCALE_HANDOFF-ACTION-004 — VFX / SFX Feedback Cost

Action 추가는 Data 하나가 아니라:
- VFX
- SFX
- animation
- hit reaction
- camera
- UI
를 함께 요구할 수 있다.

---

# SCALE_HANDOFF-ACTION-005 — Weapon / Skill Content Cost

새 Weapon / Skill은:
- animation
- hitbox
- VFX
- SFX
- balance
- enemy interaction
을 늘린다.

---

# SCALE_HANDOFF-ACTION-006 — Control Scheme QA

- keyboard
- controller
- remap
- accessibility
- resolution
- framerate

환경별 조작 검증 필요.

---

# SCALE_HANDOFF-ACTION-007 — Performance Is a Design Constraint

Enemy / projectile / VFX 증가로 FPS가 떨어지면:
- input response
- timing
- readability
가 바뀐다.

Technical / Scale Handoff.

---

# SCALE_HANDOFF-ACTION-008 — Feel Polish Is Iterative Production Cost

- camera
- freeze
- sound
- animation timing
- movement tuning

은 한 번의 구현으로 끝나지 않을 수 있다.

1인 개발에서는 `Feel polish iteration budget`을 별도 계산한다.

---

# 16. Universal Reclassification Candidates

# UC-RECLASS-ACTION-001 — Critical State Changes Need Timely Readable Feedback

## Duplicate Risk

`UC-DESIGN-005 Actionable Information`.

## Decision

새 Universal Core보다 UC-DESIGN-005 강화 후보.

Action은:
> timely / executable response
라는 추가 조건을 제공한다.

---

# UC-RECLASS-ACTION-002 — Failure Should Be Attributable to a Decision or Execution Cause

Deduction / Strategy / Action 등으로 확장 가능.

현재 Mark of the Ninja Evidence가 강하지만 Action 밖 cross-evidence가 부족.

**Canonical Mapping:** `UC-DESIGN-005 Outcome-time Specialization + Failure Attribution Cross-Genre Pattern`  
**New Universal Core:** `NO`  
**GC-ACTION-003 Genre Status:** `CANDIDATE`

---

# UC-RECLASS-ACTION-003 — Presentation Should Match Simulation State

Action:
- animation
- hitbox
- invulnerability
- detection
에서 특히 중요.

Simulation / UI에도 확장 가능.

현재 승격 보류.

---

# UC-RECLASS-ACTION-004 — Removed Input Must Leave Meaningful Agency Elsewhere

Vampire Survivors / indirect control genre까지 확장 가능.

## Duplicate Risk

`UC-DESIGN-001`.

새 Universal보다 UC-DESIGN-001 Boundary 강화 후보.

---

# 17. Evidence Gaps

# GAP-ACTION-001 — Direct Input / Response Design Evidence

필요:
- buffer
- queue
- input priority
- response tuning
- postmortem

---

# GAP-ACTION-002 — Character Action

필요:
- combo
- cancel
- expression
- enemy reaction
- animation priority

---

# GAP-ACTION-003 — Melee Combat

필요:
- range
- commitment
- hit stun
- recovery
- contact.

---

# GAP-ACTION-004 — Souls-like Telegraph / Commitment

필요:
- attack tell
- dodge timing
- recovery
- stamina
- failure attribution.

---

# GAP-ACTION-005 — FPS Aim / Recoil

필요:
- input precision
- recoil
- target acquisition
- damage feedback.

---

# GAP-ACTION-006 — Fighting Frame / Recovery

필요:
- startup
- active
- recovery
- cancel
- punish
- counterplay.

---

# GAP-ACTION-007 — Precision Movement

필요:
- acceleration
- coyote / grace systems
- retry
- movement consistency.

---

# GAP-ACTION-008 — Human Response Timing

필요:
- reaction perception
- telegraph recognition
- input execution
- skill cohort.

---

# GAP-ACTION-009 — Hitbox / Hurtbox Readability

필요:
- actual collision
- perceived boundary
- learnability.

---

# GAP-ACTION-010 — Hit Feedback

필요:
- audio
- visual
- motion
- state change
- human confirmation.

---

# GAP-ACTION-011 — Recovery after Error

필요:
- first hit
- follow-up hit
- escape
- heal
- lockout.

---

# GAP-ACTION-012 — Crowd Pressure

필요:
- density
- escape lane
- spatial compression
- human visual load.

---

# GAP-ACTION-013 — Control Fatigue

필요:
- repeated input
- session length
- physical fatigue.

---

# GAP-ACTION-014 — VFX Clarity

필요:
- own effect overlap
- enemy cue loss
- projectile visibility.

---

# GAP-ACTION-015 — Underperforming Action Control Cases

특히:
- sluggish controls
- invisible hitbox
- stunlock frustration
- unreadable VFX
- damage sponge
- cooldown routine
실패 사례.

---

# 18. Additional References Needed

현재 Action은 P0 Evidence 확보가 중요하다.

# P0 — Hades

## 강화 후보

- `GC-ACTION-001 Input / Response`
- `GC-ACTION-002 Threat Readability`
- `GC-ACTION-003 Failure Attribution`
- `GC-ACTION-006 Recovery`

## Research

- dash
- attack timing
- animation response
- enemy telegraph
- hit feedback
- recovery

## Boundary

Roguelike Boon / Meta는 분리.

## Needed Evidence

- developer design talk
- action tuning postmortem
- technical input / animation evidence
- playtest findings if public

---

# P0 — Dead Cells

## 강화 후보

- `GC-ACTION-001`
- `GC-ACTION-005 Commitment`
- movement
- weapon identity
- cancel / recovery

## Counter Question

Fast responsiveness와 attack commitment를 어떤 방식으로 동시에 유지하는가?

---

# P0 — Sekiro

## 강화 후보

- `GC-ACTION-002`
- `GC-ACTION-003`
- `GC-ACTION-005`
- Reaction Window
- Parry Feedback

## Research

- telegraph
- posture
- parry timing
- recovery
- failure learning

Souls-like 전체로 일반화 금지.

---

# P0 — DOOM Eternal

## 강화 후보

- movement
- target priority
- combat resource
- aggression
- threat readability

## Research

> 고속 FPS에서 정보 가독성과 movement pressure가 어떻게 유지되는가?

---

# P0 — Celeste

## 강화 후보

- `GC-ACTION-001`
- precision movement
- retry
- failure attribution

## Purpose

Combat이 없는 Action Control Reference.

---

# P1 — Hollow Knight

Research:
- movement
- attack reach
- telegraph
- contact damage
- recovery.

---

# P1 — Enter the Gungeon

Research:
- dodge
- bullet pattern
- density
- spatial readability.

---

# P1 — Nuclear Throne

Research:
- fast action
- crowd threat
- weapon impact
- recovery.

---

# P1 — Devil May Cry 5

Research:
- high-input expression
- cancel
- combo
- mastery
- enemy response.

Minimal-input reference의 Counter.

---

# P1 — Street Fighter 6

Research:
- frame commitment
- recovery
- punish
- counterplay
- state readability.

Competitive Fighting Boundary.

---

# 19. Promotion Table

| ID | Name | Decision | Status | Confidence |
|---|---|---|---|---|
| GC-ACTION-001 | Input Produces Predictable Controllable Response | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-ACTION-002 | Critical States Need Timely Actionable Readability | UC SPECIALIZATION | KEEP AS CANDIDATE / POSSIBLE UC SUB-RULE | VERY HIGH as specialization |
| GC-ACTION-003 | Execution Failures Need Legible Attribution | UC005 OUTCOME-TIME SPECIALIZATION + CROSS-GENRE PATTERN | KEEP AS CANDIDATE | HIGH stealth / MEDIUM broad Action |
| GC-ACTION-004 | Movement Changes Threat / Opportunity State | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH movement subtypes |
| GC-ACTION-005 | Commitment Needs Matching Risk / Reward | NEW | KEEP AS CANDIDATE | LOW-MEDIUM |
| GC-ACTION-006 | Error Propagation Preserves Intended Recovery | NEW | KEEP AS CANDIDATE | MEDIUM-LOW |
| GC-ACTION-007 | Removed Input Leaves Meaningful Agency Elsewhere | UC SPECIALIZATION | KEEP AS CANDIDATE / POSSIBLE UC SUB-RULE | VERY HIGH as specialization |

## Provisional Genre Core

**NONE at current Evidence level.**

---

# 20. Action Reviewer Default Set

신규 Action 기획에서 우선 적용할 15개 질문.

## Q1 — Direct Action

> **Player가 직접 제어하는 핵심 Action은 무엇인가?**

---

## Q2 — Input / Response

> **같은 Relevant State에서 같은 Input이 예측 가능한 Character Response를 만드는가?**

관련:
`GC-ACTION-001`

---

## Q3 — Commitment

> **Attack / Dodge / Movement의 Lock / Cancel / Recovery가 Product Fantasy와 맞는가?**

관련:
`GC-ACTION-005`

---

## Q4 — Movement

> **Movement가 실제 Threat / Contact / Escape / Attack Opportunity를 바꾸는가?**

관련:
`GC-ACTION-004`

---

## Q5 — Threat Readability

> **위험 State를 필요한 시점에 읽을 수 있는가?**

관련:
`UC-DESIGN-005 / GC-ACTION-002`

---

## Q6 — Response Opportunity

> **Threat를 읽은 뒤 실제 실행 가능한 대응 Window가 남아 있는가?**

관련:
`GC-ACTION-002`

---

## Q7 — Contact Feedback

> **Hit / Miss / Block / Armor / Detection 결과를 구분할 수 있는가?**

---

## Q8 — Failure Attribution

> **왜 맞거나 발각되거나 죽었는지 actionable 원인으로 설명할 수 있는가?**

관련:
`GC-ACTION-003`

---

## Q9 — Recovery

> **첫 실수 이후 Input Agency가 어떻게 변하는가? Product Promise와 맞는가?**

관련:
`GC-ACTION-006`

---

## Q10 — Difficulty

> **난이도가 HP / Enemy Count만 증가시키는가, 아니면 execution demand의 성격도 바뀌는가?**

---

## Q11 — Input Count

> **버튼 수를 Depth로 착각하고 있지 않은가? 제거된 Input 뒤에도 Agency가 남는가?**

관련:
`UC-DESIGN-001 / GC-ACTION-007`

---

## Q12 — Presentation / State Alignment

> **Animation / VFX가 actual Hitbox / Vulnerability / Detection State와 일치하는가?**

---

## Q13 — AI vs Human

> **AI의 완벽한 state access / reaction을 Human Perception / reaction evidence로 오해하지 않았는가?**

---

## Q14 — Validation Layer

> **Machine은 Collision / State / Pattern을, Human은 Feel / Fairness / Clarity를 평가하도록 분리했는가?**

---

## Q15 — Evidence / Scope Boundary

> **현재 Stealth / Survivors-like Evidence를 Character Action / FPS / Fighting 전체로 일반화하거나, Animation / Enemy / VFX Scope를 과소평가하고 있지 않은가?**

---

# 21. Default Metric Bundle

Metric은 Criteria가 아니다.

Threshold는 프로젝트별 Validation Planner가 정한다.

# 21.1 Structural / Machine

- Action Definition Count
- Movement State Count
- Attack State Count
- Recovery State Count
- Lock State Count
- Hitbox / Hurtbox Definition
- Threat State Definition
- Detection State Definition
- Collision Rule Coverage
- Input → Action Mapping Coverage

---

# 21.2 Structural / model-dependent

- Recovery Window
- Cancel Window
- Commitment
- Threat Cue Availability
- Threat State → Presentation Mapping Coverage
- Threat Cue → Response Window
- Unavoidable Threat
- Safe Space
- Stunlock
- Execution Error
- Damage Cause Classification
- Detection Cause Classification
- First Critical Mistake
- Positional Value
- Failed Command Candidate

Formal Definition 없이 자동 Machine Metric으로 사용하지 않는다.

### Threat Readability Interpretation Rule

Machine은 `Cue가 존재하는가`, `Threat State가 Presentation에 매핑되는가`, `Cue 이후 Response Window가 존재하는가` 같은 구조 조건을 검증할 수 있다.

하지만:

```text
Cue exists
≠
Player recognized the cue
```

이므로 `Threat Readability / Threat Legibility` 자체는 Human / Hybrid Evidence로 처리한다.

---

# 21.3 Simulation

- Action Usage
- Action Concentration
- Position Distribution
- Movement Distance
- Direction Change
- Dodge Usage
- Dash Usage
- Attack Usage
- Hit Rate
- Miss Rate
- Damage Distribution
- Kill Rate
- Target Distribution
- Threat → Hit Rate
- Threat → Dodge Rate
- Consecutive Hit Chain
- Detection State Transition
- Enemy Density
- Contact Frequency
- Recovery Action Usage
- Escape after Detection
- Time in Suspicion

---

# 21.4 Simulation / model-dependent

- Threat Overlap
- Crowd Pressure
- Escape Lane Availability
- Position → Damage Relationship
- Movement → Survival Relationship
- Unavoidable Threat Candidate
- Stunlock Chain
- Error Propagation Depth
- Time to Safe State
- Hits after First Error
- Damage by Density State
- Movement Policy by Build
- Time Encircled

Project-specific Formal Definition 없이 일반 Simulation Metric으로 사용하지 않는다.

---

# 21.5 Instrumented Player Telemetry

- Input Frequency
- Action Usage
- Dodge Timing
- Cancel Usage
- Buffer Usage
- Attack Timing
- Movement Pattern
- Pause
- Retry
- Control Remap
- Repeated Input
- Damage-taken Timing
- Player-selected / reported Death Cause if collected

---

# 21.6 Instrumented / Simulation

다음이 명시적 Game Action인 경우:

- attack
- dodge
- guard
- parry
- dash
- jump
- aim
- reload
- heal
- interrupt

측정:
- usage
- timing
- state before
- state after
- follow-up state

### Interpretation Rule

AI internal state knowledge를 Player Perception으로 취급하지 않는다.

```text
AI knows attack state
≠
Player recognized telegraph
```

AI가 deterministic policy로 dodge에 성공했다고 해서:

```text
Human had enough reaction opportunity
```

라고 결론내리지 않는다.

---

# 21.7 Human

- Control Intent
- Responsiveness
- Movement Confidence
- Threat Recognition
- Reaction Opportunity
- Failure Attribution
- Hit Confirmation
- Impact / Hit Feel
- Damage Source Recognition
- Recovery Perception
- Movement Value
- Visual Clarity
- Control Fatigue
- Action Fantasy
- Perceived Fairness

---

# 21.8 Hybrid

- Action Readability
- Control Quality
- Combat Feedback Quality
- Threat Readability / Threat Legibility
- Difficulty Quality
- Recovery Quality
- Movement Quality
- Commitment Quality
- Enemy Pressure Quality
- Execution Satisfaction
- Action Decision Density
- Presentation / State Alignment Quality

---

# 22. Self-Review Result

## Check 1 — Real-time = Action Core
**PASS**

실시간 자체를 Core로 만들지 않았다.

## Check 2 — Button Count = Depth
**PASS**

`UC-DESIGN-001`, Vampire Survivors를 통해 분리했다.

## Check 3 — Responsiveness as vague adjective
**PASS**

Input / response / lock / cancel / recovery로 분해했다.

## Check 4 — Hit Feel = Screen Shake / Hit Stop
**PASS**

Mechanical state change와 Human Impact Feel을 분리했다.

## Check 5 — Mark of the Ninja overgeneralization
**PASS**

Stealth / readability Evidence로만 사용했다.

## Check 6 — Vampire Survivors overgeneralization
**PASS**

Minimal Input을 Universal best practice로 만들지 않았다.

## Check 7 — Strategy Position duplicate
**PASS**

Action에서는 timing / contact / escape 관점만 사용했다.

## Check 8 — Roguelike Build duplicate
**PASS**

Vampire Survivors의 Build / Meta를 Action Core로 복제하지 않았다.

## Check 9 — Telegraph = Fairness
**PASS**

Response Window와 Human perception을 별도 검증한다.

## Check 10 — AI immediate response = Human response
**PASS**

Reaction Policy를 sensitivity model로만 사용한다.

## Check 11 — Collision correctness = Hit Feel
**PASS**

Structural / Human 분리.

## Check 12 — Enemy Count = Difficulty
**PASS**

Crowd Pressure / escape lane / readability로 분해했다.

## Check 13 — Animation / VFX vs Gameplay State
**PASS**

Presentation / State Alignment을 별도 검토했다.

## Check 14 — Genre vs Production Scope
**PASS**

Animation / VFX / Weapon / Enemy / performance는 Scale Handoff.

## Check 15 — Evidence Boundary
**PASS**

현재 Stealth / Survivors-like 중심임을 명시하고 Provisional을 0개로 유지했다.

---

# 23. Final Position

현재 Studio OS Action Knowledge Base에서는:

## Provisional Genre Core

**없음.**

이는 Action에 Core가 없다는 의미가 아니다.

현재 Direct Action Evidence가:

- `Mark of the Ninja`
  - Stealth information
  - detection readability
  - failure attribution
- `Vampire Survivors`
  - minimal input
  - movement agency
  - density / survival

라는 서로 다른 Subtype에 편중되어 있고,

가장 강한 두 발견이 이미:

- `UC-DESIGN-005 — Actionable Information`
- `UC-DESIGN-001 — Consequence Density over Input Count`

의 Action specialization으로 설명 가능하기 때문이다.

현재 Candidate:

1. `GC-ACTION-001 — Input Should Produce Predictable Controllable Response`
2. `GC-ACTION-002 — Critical Action States Need Timely Actionable Readability`
3. `GC-ACTION-003 — Execution Failures Need Legible Attribution`
4. `GC-ACTION-004 — Movement Should Change Immediate Threat / Opportunity State`
5. `GC-ACTION-005 — Commitment Needs Matching Risk / Reward`
6. `GC-ACTION-006 — Error Propagation Should Preserve Intended Recovery Structure`
7. `GC-ACTION-007 — Removed Input Must Leave Meaningful Action Agency Elsewhere`

이번 Extraction에서 가장 중요한 결과는 다음이다.

> **Action의 품질을 입력량이나 연출량이 아니라 `Input → Response → Outcome → Feedback → Adjustment`의 짧은 폐쇄 루프로 평가한다.**

그리고:

> **Threat를 보여줬다는 사실과 Player가 대응할 수 있었다는 사실을 분리한다.**

또:

> **Collision correctness와 Human Fairness / Hit Feel을 분리한다.**

현재 가장 강한 Universal Strengthening은:

### UC-DESIGN-005

Action에서:

> Information은 timely하고 executable해야 한다.

### UC-DESIGN-001

Action에서:

> Removed Input 뒤에 Movement / Timing / Position 같은 다른 consequence-bearing Agency가 남아야 한다.

현재 가장 중요한 다음 단계는 P0 Direct Action Evidence 확보다.

우선순위:

1. Hades
2. Dead Cells
3. Sekiro
4. DOOM Eternal
5. Celeste

이 Evidence가 추가되면 가장 먼저 재검토할 Candidate는:

1. `GC-ACTION-001`
2. `GC-ACTION-003`
3. `GC-ACTION-005`
4. `GC-ACTION-006`

이다.

특히 Hades / Dead Cells / Sekiro에서:

- Input response
- commitment
- recovery
- telegraph
- failure attribution

이 동일 Mechanism으로 반복 확인될 경우 Action-specific Provisional을 처음 승격할 가능성이 높다.

---

# 24. Source Trace

## Primary Action Evidence
- REF-21 — Mark of the Ninja
- REF-12 — Vampire Survivors

## Action / Hybrid Support
- REF-27 — Tiny Rogues
- REF-36 — Brotato
- REF-32 — Patch Quest
- REF-35 — Dome Keeper

## Adjacent / Control
- REF-25 — Buckshot Roulette
- REF-03 — Into the Breach
- REF-16 — Invisible, Inc.
- REF-02 — FTL
- REF-20 — Dicey Dungeons
- REF-18 — Loop Hero

## Baseline / Deduplication
- STUDIO_CORE_CANDIDATES_v0.2
- STRATEGY_CORE_CANDIDATES_v0.1
- ROGUELIKE_CORE_CANDIDATES_v0.1
- RPG_CORE_CANDIDATES_v0.1
- SIMULATION_CORE_CANDIDATES_v0.1
- Studio OS — Action Genre Core Deep Extraction Prompt v0.1

---

# 25. Traceability Rule

Core는 원본 Reference를 대체하지 않는다.

Action 위험 신호가 발견되면:

```text
Action Candidate / Universal Core
↓
Primary / Strong Reference
↓
Input
↓
Character Response
↓
Threat / Contact State
↓
Feedback
↓
Player Adjustment
↓
Recovery / Failure
↓
Boundary / Trade-off
↓
Current Project
```

순서로 다시 내려가 검토한다.

`ACTION_CORE_CANDIDATES_v0.1`은 현재 Evidence가 제한된 상태에서 Action을 버튼 수·속도·타격 연출로 일반화하지 않고, **Input / Response / Threat Readability / Failure Attribution / Movement / Recovery**를 중심으로 다음 Evidence 수집과 신규 Action Review를 구조화하기 위한 Candidate Baseline이다.
