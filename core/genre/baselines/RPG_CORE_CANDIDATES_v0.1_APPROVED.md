# RPG_CORE_CANDIDATES_v0.1

**Studio OS — RPG Genre Core Deep Extraction**  
**Document:** `RPG_CORE_CANDIDATES_v0.1`  
**Status:** `APPROVED_AS_GENRE_CORE_CANDIDATE_BASELINE`  
**Purpose:** 신규 Narrative RPG / Party RPG / Tactical RPG / Character-build RPG / Action RPG Hybrid / Roguelike RPG Hybrid / Management RPG Hybrid / Systemic RPG / Stat / Skill-check RPG 기획 평가용 Genre-specific Reviewer Knowledge Base  
**Baseline:** `STUDIO_CORE_CANDIDATES_v0.2`  
**Extraction Prompt:** `Studio OS — RPG Genre Core Deep Extraction Prompt v0.1`  
**Deduplication Baselines:** `NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1`, `STRATEGY_CORE_CANDIDATES_v0.1`, `MANAGEMENT_CORE_CANDIDATES_v0.1`, `ROGUELIKE_CORE_CANDIDATES_v0.1`, `SIMULATION_CORE_CANDIDATES_v0.1`  
**Provisional Genre Cores:** `NONE`  
**Candidates:** `GC-RPG-001 ~ GC-RPG-008`  
**Universal Strengthening:** `GC-RPG-001 Evidence → UC-DESIGN-006 — Progression Should Match Its Intended Promise`  
**Evidence Boundary:** `Darkest Dungeon / Citizen Sleeper 중심. Traditional CRPG / JRPG / Open-world RPG / Action RPG / Equipment-driven ARPG / Companion-heavy RPG는 Additional Evidence 전까지 제한 적용.`  
**Pending:** `Additional Evidence / Prototype Validation / Internal Evidence`  
**Evidence Rule:** 현재 Direct RPG Evidence가 Darkest Dungeon과 Citizen Sleeper에 크게 편중되어 있으므로 Traditional CRPG / JRPG / Open-world RPG / Action RPG / Class-heavy RPG / Equipment-driven ARPG / Companion-heavy RPG 전체로 자동 일반화하지 않는다.

---

# 1. Executive Summary

이번 Deep Extraction의 핵심 결론은 다음과 같다.

1. **현재 Evidence만으로 독립적인 RPG Provisional Genre Core를 새로 승격하지 않는 것이 가장 안전하다.**
   - Darkest Dungeon은 강한 RPG 사례이지만 가장 직접적인 Evidence는 Roster / Attrition / Long-term Consequence Management에 있다.
   - Citizen Sleeper는 Narrative RPG이지만 현재 Studio Reference의 가장 강한 분석 축은 Dice Allocation / Narrative Economy / Opportunity Cost에 있다.
   - Dicey Dungeons는 Character Rule Identity를 보조하지만 Roguelike / RNG 설계가 중심이다.
   - 따라서 두 사례의 겹치는 부분을 그대로 RPG Universal로 승격하면 Management / Narrative / UC-DESIGN-006을 재포장할 위험이 크다.

2. **가장 강한 발견은 신규 RPG Core라기보다 `UC-DESIGN-006 — Progression Should Match Its Intended Promise`의 강화 필요성이다.**
   - RPG 관점에서는 성장 후:
     - 새 Capability
     - 새 Role
     - 새 Solution
     - 새 Limitation
     - 다른 Encounter response
     가 생기는지를 별도로 검토해야 한다.
   - 그러나 Vertical Power Growth 자체가 Fantasy인 RPG도 충분히 성립하므로:
     > 모든 성장 단계가 새 행동을 제공해야 한다
     는 Rule로 올리지 않는다.

3. 현재 가장 유력한 RPG Candidate는 다음 6개다.
   - `GC-RPG-001 — Character Investment Should Change Available Solutions`
   - `GC-RPG-002 — Mechanical Role Claims Need Behavioral Consequences`
   - `GC-RPG-003 — Character Formation Should Preserve Differentiation`
   - `GC-RPG-004 — Build Variety Needs Supporting Content`
   - `GC-RPG-005 — Persistent Character Consequences Should Change Future Play`
   - `GC-RPG-006 — Equipment Should Create Choice, not Only Replacement`

4. 다음은 중요하지만 현재 Direct Evidence가 특히 부족해 낮은 Confidence Candidate로 유지한다.
   - `GC-RPG-007 — Commitment / Respec Must Match Character Ownership`
   - `GC-RPG-008 — Player Skill / Character Skill Balance Must Match Subtype`

5. RPG를 Feature 목록으로 정의하지 않는다.
   - Level
   - EXP
   - Stat
   - Skill Tree
   - Equipment
   - Quest
   는 RPG Depth의 증거가 아니다.

6. Studio OS에서 RPG의 가장 유용한 작업 정의는 다음이다.

> **Player가 Character 또는 Party의 능력·성향·관계·역할을 지속적으로 형성하고, 그 형성이 이후 가능한 행동과 문제 해결 방식에 영향을 주는 구조.**

7. RPG Identity는 세 층으로 나눠야 한다.
   - Mechanical Role
   - Expressive Role
   - Fictional Role
   세 축 모두가 반드시 강할 필요는 없지만, Product Promise가 주장하는 축은 실제 시스템이나 콘텐츠에서 표현되어야 한다.

8. Darkest Dungeon이 강하게 지지하는 것은:
   - Character State Persistence
   - Short-term Result → Long-term Character Consequence
   - Party Composition
   - Attachment / Replaceability tension
   이다.
   그러나 Stress / Injury / Permadeath 자체를 RPG Core로 일반화하면 안 된다.

9. Citizen Sleeper가 강하게 지지하는 것은:
   - Skill / Character Condition
   - Persistent relationship / progression
   - Narrative role
   - Character state와 available action의 결합 가능성
   이다.
   그러나 현재 Reference는 Build / Skill Tree / Stat solution space를 직접 충분히 분석하지 않는다.

10. Dicey Dungeons가 보조하는 것은:
    - Character Rule Variant가 실제 플레이 감각을 바꿀 수 있다는 점.
    이는 `Class Name without Mechanical Identity` Anti-pattern의 반대 사례로 유용하다.

11. RPG AI Tester는 다음에 강하다.
    - Build Distribution
    - Stat Distribution
    - Skill Usage
    - Equipment Usage
    - Progression Timing
    - Build Convergence
    - Content Coverage
    - Class-specific solution usage

12. 그러나 Machine은 다음을 직접 판정하지 않는다.
    - “내 캐릭터 같다”
    - “성장한 느낌이다”
    - “이 Class Fantasy가 좋다”
    - “이 Build를 내가 만들었다”
    - “Companion에게 애착이 간다”
    - “Roleplay가 된다”

13. 현재 가장 중요한 Evidence Gap은:
    - CRPG Quest Solution by Build
    - JRPG fixed-role progression
    - Action RPG Player Skill vs Character Skill
    - Skill Tree actual behavior
    - Respec behavior
    - Dump Stat / Universal Stat telemetry
    - Equipment replacement
    - Companion attachment
    - Build regret
    - Character identity perception
    - Underperforming RPG control cases

14. 따라서 현재 RPG Knowledge Base의 핵심 목적은:
    - 억지 Provisional Core를 만드는 것이 아니라
    - 신규 RPG Review에서 검증해야 할 Candidate와 Evidence Gap을 명확히 분리하는 것
    이다.

---

# 2. RPG Genre Definition

Studio OS에서 RPG를:

> Level과 Stat이 있는 게임

으로 정의하지 않는다.

기본 작업 정의:

> **Player가 Character 또는 Party의 지속적인 상태를 형성하고, 그 형성이 이후 가능한 행동·역할·문제 해결 방식에 영향을 주는 구조.**

기본 구조:

```text
Character / Party State
↓
Invest / Choose / Equip / Relate
↓
Act in World
↓
Outcome
↓
Persistent Character Change
↓
Capability / Limitation / Relationship Changes
↓
Future Problem-solving Changes
```

---

# 2.1 RPG Inclusion Test

## A. Persistent Character State

다음 중 일부가 지속되는가?

- Skill
- Trait
- Equipment
- Relationship
- Reputation
- Condition
- Knowledge
- Class
- Ability

---

## B. Player-directed Formation

Player가 해당 State의 일부를 실제로 형성하는가?

---

## C. Expression

형성된 Character가 실제 Gameplay / Narrative에서 다른 방식으로 행동할 수 있는가?

---

## D. Consequence

Character State가 최소 하나 이상의 해결 방식에 영향을 주는가?

- Combat
- Dialogue
- Quest
- Exploration
- Resource
- Relationship
- Risk

---

## E. Persistence

투자나 결과가 이후 Character Identity에 남는가?

---

## F. Progression

시간이 지나 Character가 변하는가?

단순 숫자가 아니라:

> **문제 해결 방식이 어떻게 달라지는가?**

를 본다.

---

## G. Role Recognition

Player가:

> **“내 Character는 어떤 Character인가?”**

를 Ability / 행동 / 선택 중 적어도 하나로 설명할 수 있는가?

---

# 3. Evidence Scope / Limitation

## 상대적으로 강한 Direct RPG Evidence

- `REF-06 Darkest Dungeon`
- `REF-23 Citizen Sleeper`

## Strong Hybrid Support

- `REF-20 Dicey Dungeons`
- `REF-02 FTL`
- `REF-15 This War of Mine`

## 약한 영역

- Traditional CRPG
- JRPG
- Open-world RPG
- Party Relationship RPG
- Action RPG
- Class-heavy RPG
- Quest-heavy RPG
- Dialogue / Skill-check RPG
- Equipment-driven ARPG
- Companion-driven RPG

## Boundary

현재 Core Candidate는:

> **Character Formation / Differentiation / Capability Expression**

같은 저수준 Mechanism에만 적용한다.

다음으로 자동 확대하지 않는다.

- 모든 RPG는 Build Craft가 핵심이다.
- 모든 RPG는 Roleplay Choice가 있어야 한다.
- 모든 RPG는 Party가 있어야 한다.
- 모든 RPG는 Skill Check가 있어야 한다.
- 모든 RPG는 Horizontal Progression이 Vertical Progression보다 우월하다.

---

# 4. Mechanical / Expressive / Fictional Role

RPG Identity를 최소 세 층으로 분리한다.

# 4.1 Mechanical Role

Character가 시스템적으로 무엇을 잘하는가?

예:
- Tank
- Healer
- Scout
- Hacker
- Diplomat
- Burst Damage

검토:

> 이 Role이 실제 Action / Outcome / Encounter에서 다른 행동을 만들고 있는가?

---

# 4.2 Expressive Role

Player가 Character를 어떤 성향으로 표현하는가?

예:
- merciful
- selfish
- lawful
- reckless
- loyal

검토:

> Character Identity와 선택이 실제로 일치하거나 충돌할 수 있는가?

Narrative Core와 중복되는 Roleplay Quality 자체는 여기서 복제하지 않는다.

---

# 4.3 Fictional Role

세계 안에서 Character가 누구인가?

예:
- detective
- mercenary
- sleeper
- knight
- mage
- ruler

검토:

> Fiction에서 주장하는 전문성 / 정체성이 Gameplay Capability 또는 World Response에서 표현되는가?

---

# 4.4 Role Alignment Rule

좋은 RPG가 반드시 세 Role을 모두 강하게 제공해야 하는 것은 아니다.

하지만 Product Promise가:

> “당신은 Master Thief다.”

라고 말한다면 실제 시스템에서:
- lockpick
- stealth
- infiltration
중 아무 차이가 없는 것은 `FICTION_MECHANICS_MISMATCH_RISK`다.

---

# 5. Source Classification

# 5.1 Tier A — Primary RPG Evidence

## REF-06 — Darkest Dungeon

**Subtype:** `Party / Roster RPG + Management Hybrid`  
**Evidence Strength:** VERY HIGH — Persistent Character State / Party / Long-term Consequence

### Strong Evidence Areas

- Hero Level
- Class Composition
- Skill Selection
- Stress
- Injury / Disease / Quirk
- Persistent Character State
- Character Loss
- Attachment / Replaceability
- Short-term Encounter → Long-term Character Consequence

### Core Observation

전투 결과가 HP에서 초기화되지 않고:
- Stress
- Quirk
- Disease
- Death
- Recovery Need
로 남아 이후:
- Party Composition
- Hero Selection
- Risk
를 바꾼다.

### RPG-specific Use

Management의:
- 치료 우선순위
- 로스터 경제
- Recovery Structure
를 복제하지 않는다.

RPG에서는:

> **Character가 Encounter 밖에서도 지속되는 상태를 갖고, 그 상태가 이후 Character 사용 방식과 Party 선택을 바꾸는가?**

에 한정해서 사용한다.

### Boundary

Darkest Dungeon을 근거로:
- Permanent Death
- Stress
- Injury
를 RPG 필수로 만들지 않는다.

---

# 5.2 Tier B — Strong RPG / Hybrid Evidence

## REF-23 — Citizen Sleeper

**Subtype:** `Narrative RPG / Dice Allocation`

### Strong Evidence Areas

- Character Condition
- Skill
- Persistent Relationship
- Narrative Role
- Character State
- Progression
- Identity Choice

### Source Limitation

현재 Studio Reference의 가장 강한 Lesson은:
- Narrative Economy
- Opportunity Cost
- Clock
이다.

RPG 관점에서는:
- Skill
- Condition
- Relationship
이 Persistent Character State를 만든다는 점만 보조적으로 사용한다.

Build / Stat / Class / Equipment Core를 강하게 지지하는 Primary로 사용하지 않는다.

---

## REF-20 — Dicey Dungeons

**Subtype:** `Character-rule Roguelike RPG Hybrid`

### Strong Supporting Use

- Character Rule Identity
- Ability Difference
- Different Playstyle from same Core Mechanic

### Important Observation

같은 Core Mechanic도 Character별 제약 규칙을 바꾸면:
> 거의 다른 게임처럼 느껴질 수 있다.

이는:
- Class Name
- Character Name
이 아니라
- 실제 Rule / Action Value
가 Mechanical Identity를 만든다는 보조 Evidence다.

### Boundary

Progression / RPG build보다 RNG / Roguelike evidence가 훨씬 강하다.

---

## REF-02 — FTL

### Use

- Crew Species Difference
- Crew Skill
- Role Assignment
- Persistent Crew State

### Boundary

RPG Primary Evidence로 사용하지 않는다.

Character Formation보다:
- Strategy
- Systemic Management
가 중심이다.

---

## REF-15 — This War of Mine

### Use

- Individual Character State
- Injury / Sickness / Mood
- Human Cost

### Boundary

Management / Narrative evidence가 우선.

RPG에서는:
> Character state가 단순 숫자가 아니라 이후 행동 조건과 보호 가치에 영향을 줄 수 있다
는 보조 Evidence로만 사용한다.

---

# 5.3 Tier C — Adjacent / Control

- 80 Days
- Against the Storm
- Reigns
- Vampire Survivors
- Tiny Rogues
- Loop Hero
- Into the Breach

특정 Mechanism 비교에만 사용한다.

Tier C만으로 RPG Provisional을 승격하지 않는다.

---

# 6. Universal / Existing Genre Core Audit

# 6.1 UC-DESIGN-006 — Progression Should Match Its Intended Promise

**Current:** `CANDIDATE`

Rule:

> 성장 후 같은 행동을 더 강하게 수행하는 것만이 아니라 다른 판단을 할 수 있게 되는가를 별도로 평가한다.

## RPG Audit

이 Rule은 RPG에서 매우 중요하지만 그대로 `GC-RPG`로 복제하면 중복이다.

### RPG Specialization

RPG에서는:

> **Progression이 Character Formation / Role / Available Solution에 어떤 차이를 만드는가?**

를 본다.

### Evidence

Darkest Dungeon:
- Level / class / state / party usage가 장기 Character 활용 방식과 연결.

Citizen Sleeper:
- Skill / relationship / condition이 장기 Character State를 구성.

Dicey Dungeons:
- Character rule difference가 실제 playstyle change를 만든다는 보조 Evidence.

### Decision

`GC-RPG-001`은 별도 RPG Provisional로 승격하지 않고:

> `UC-DESIGN-006 RPG specialization`

상태의 Candidate로 유지한다.

또한 본 Extraction은 `UC-DESIGN-006`의 Promotion Evidence를 **강화**한다.

---

# 6.2 Narrative Deduplication

복제하지 않는다.

- Roleplay Choice
- Relationship consequence
- System / Narrative Coupling
- Delayed Consequence

RPG에서는:

> 해당 Narrative Choice가 Character Identity / Build / Role을 표현하는가?

만 본다.

---

# 6.3 Management Deduplication

Darkest Dungeon의:
- Recovery
- Replacement
- Roster Priority
는 Management Core에 남긴다.

RPG에서는:
- persistent Character state
- identity
- capability change
만 사용한다.

---

# 6.4 Strategy Deduplication

Build / Party가:
- Strategy Diversity
를 만든다는 사실만으로 RPG Core를 만들지 않는다.

RPG에서는:

> Character Formation의 차이가 actual role / capability 차이를 만드는가?

를 본다.

---

# 6.5 Roguelike Deduplication

Run Build / Reset / Meta / Pivot을 복제하지 않는다.

---

# 7. Provisional RPG Cores

## Result

**현재 신규 Provisional RPG Core 승격 없음.**

### Reason

현재 Promotion 기준은:
1. 최소 2개 독립 RPG Design Evidence
2. 동일 Mechanism
3. 다른 Genre / Universal과 중복 제거
4. Subtype Boundary
5. Reviewer utility
6. Validation path

이다.

현재 가장 강한 RPG Mechanism 후보들은:

- Progression → Capability
- Persistent Character State → Future Play
- Mechanical Role → Behavioral Difference

이지만 각각:
- `UC-DESIGN-006`
- `UC-DESIGN-003 / Management`
- Character-specific evidence shortage

와 중복 또는 Evidence Gap이 존재한다.

따라서 이번 단계에서 억지 승격보다 Candidate Baseline을 만드는 편이 정확하다.

---

# 8. RPG Core Candidates

# GC-RPG-001 — Character Investment Should Change Available Solutions

**Status:** `CANDIDATE`  
**Origin:** `UC-DESIGN-006 RPG SPECIALIZATION`

## Pattern

RPG Progression은:
- Level
- Stat
- Skill
- Equipment
투자를 통해 Character를 형성한다.

중요한 것은 수치가 오르는 사실이 아니라:
> **어떤 문제에 어떤 방식으로 대응할 수 있게 되는가**
다.

## Rule Candidate

> **Character Investment를 RPG의 핵심 가치로 제시한다면 최소 일부 Progression은 이후 Available Capability / Solution / Role Value를 변화시켜야 한다. Vertical Power Growth만으로도 성립할 수 있지만, Character-build를 약속하면서 모든 투자가 같은 행동의 숫자만 키우는 구조는 별도 검토한다.**

## Primary Evidence

### Darkest Dungeon
- Level
- Class
- Skill
- Persistent State
가 Hero의 party use와 Encounter 선택에 영향을 준다.

## Secondary Evidence

### Citizen Sleeper
- Skill과 Character Condition이 Persistent Character State의 일부를 만든다.

### Dicey Dungeons
- Character rule variation이 실제 action logic을 바꾼다.

## Counter Evidence

### Vertical Power Fantasy RPG
단순히:
- 더 강한 Damage
- 더 큰 HP
를 얻는 성장 자체가 핵심 동기일 수 있다.

## Applies To

강하게:
- Character-build RPG
- Class RPG
- Tactical RPG
- CRPG

조건부:
- Action RPG
- Narrative RPG

## Boundary

모든 Level마다 새 Action을 줄 필요는 없다.

핵심은 전체 progression arc에서:
> capability / role / solution 변화가 존재하는가
다.

## Candidate Metric — Simulation

- Skill Unlock Timing
- New Action Unlock Rate
- Progression Stage → Action Distribution
- Build Distribution
- Build Convergence

## Structural / model-dependent

- Capability Coverage
- Solution Space Change
- Meaningful Progression

## Human

- Progression Meaning
- “성장 후 새롭게 할 수 있게 된 것”
- Character Growth Perception

## Validation Type

Simulation + Structural / model-dependent + Human.

## AI Tester Applicability

HIGH structurally.

## Confidence

**HIGH as UC specialization / MEDIUM for independent RPG Core**

## Reviewer Action

Level / Skill Tree가 있다면:

> **“이 투자를 한 뒤 이전과 다른 어떤 해결 방식이 생기는가?”**

를 묻는다.

---

# GC-RPG-002 — Mechanical Role Claims Need Behavioral Consequences

**Status:** `CANDIDATE`  
**Origin:** `NEW GENRE CORE`

## Pattern

Class / Character 이름이 달라도:
- action
- target
- resource
- risk
사용 방식이 동일하면 Mechanical Role 차이는 약하다.

## Rule Candidate

> **Character / Class / Trait이 특정 Mechanical Role을 주장한다면 실제 Action Distribution, Capability, Positioning, Targeting 또는 Problem-solving 방식에서 차이가 나타나야 한다. 이름과 Damage Type만 다른 것은 Role Differentiation의 충분한 증거가 아니다.**

## Primary Evidence

### Darkest Dungeon
Class와 Party Composition이:
- Skill
- Position
- Target
- formation
차이를 만든다.

## Secondary Evidence

### Dicey Dungeons
같은 Dice Core를 Character별 rule constraint로 바꿔 플레이 감각을 크게 변화시킨다.

### FTL
Crew species / skill / assignment difference는 역할 차이가 실제 system use에 영향을 줄 수 있다는 보조 사례.

## Counter Evidence

### Narrative RPG
Mechanical class differentiation이 약하고 Expressive / Fictional Role이 중심일 수 있다.

## Applies To

강하게:
- Class RPG
- Party RPG
- Tactical RPG
- Character-rule RPG

약하게:
- Narrative RPG
- Open roleless RPG

## Candidate Metric — Simulation

- Class Action Distribution
- Class-specific Skill Usage
- Role-specific Position Distribution
- Role-specific Target Distribution
- Role Overlap

`Role Overlap`은 Formal Definition 필요.

## Human

- Mechanical Identity
- Class Fantasy
- “다른 Class와 실제 플레이가 달랐는가?”

## Confidence

**MEDIUM-HIGH**

## Reviewer Action

Class가 8개라면:

> **“8개 Class가 실제로 어떤 서로 다른 Player Verb / Risk / Position / Resource pattern을 만드는가?”**

를 요구한다.

---

# GC-RPG-003 — Character Formation Should Preserve Differentiation

**Status:** `CANDIDATE`

## Rule Candidate

> **Character Formation을 장기 RPG 가치로 제시한다면 진행 후 모든 Character / Build가 같은 핵심 Stat / Skill / Equipment로 수렴해 초기 선택 차이가 사라지는지 검토한다.**

## Evidence

### Darkest Dungeon
Class 차이와 persistent hero state가 roster identity를 유지.

### Dicey Dungeons
Character rule identity가 강한 counterexample to convergence.

## Promotion Blocker

Traditional CRPG / JRPG / ARPG progression ceiling evidence 부족.

## Candidate Metric

- Final Build Similarity
- Build Convergence
- Shared Skill Rate
- Universal Stat Concentration
- Universal Equipment Rate
- Class Action Similarity

## Human

- Character Differentiation
- Build Ownership
- Endgame Identity

## Confidence

**MEDIUM**

---

# GC-RPG-004 — Build Variety Needs Supporting Content

**Status:** `CANDIDATE`

## Rule Candidate

> **여러 Build / Stat / Skill을 제공한다면 실제 Encounter / Quest / Exploration에서 서로 다른 강점이 사용될 Context가 존재해야 한다. Build 수와 실제 활용되는 Solution Space를 분리한다.**

## Evidence

Darkest Dungeon:
- enemy
- region
- formation
- stress state
가 party / class value를 바꾸는 보조 Evidence.

Citizen Sleeper:
- skill / relationship / action slot의 Contextual value가 존재하는 Narrative RPG support.

## Promotion Blocker

Quest Solution by Build 직접 Evidence 부족.

## Candidate Metric

- Build → Encounter Usage
- Skill → Opportunity Exposure
- Stat Check Exposure
- Class-specific Solution Usage
- Dead Investment Rate
- Build-specific Success Distribution

대부분 일부 Formal Definition 필요.

## Human

- Build-supporting Content
- “내 Build가 빛난 순간”
- Dead Investment perception

## Confidence

**MEDIUM-HIGH**

---

# GC-RPG-005 — Persistent Character Consequences Should Change Future Play

**Status:** `CANDIDATE`  
**Origin:** `UC-DESIGN-003 / MANAGEMENT SPECIALIZATION RISK`

## Rule Candidate

> **부상 / Trait / Curse / Reputation / Relationship 같은 Persistent Character State를 RPG Feature로 사용한다면 단순 장식 또는 penalty stack이 아니라 이후 Character 선택·Ability·Risk·Availability 중 일부를 실제로 바꾸는지 검토한다.**

## Primary Evidence

### Darkest Dungeon
가장 강한 Evidence.
Combat 결과가:
- Stress
- Quirk
- Disease
- Death
로 남아 다음 Expedition / Hero usage를 바꾼다.

## Secondary Evidence

### Citizen Sleeper
Condition / relationship / progression이 persistent Character State를 구성.

### This War of Mine
Injury / sickness / mood가 이후 action / protection decision에 영향을 준다.

## Duplicate Risk

- UC-DESIGN-003
- GC-MGMT-002
- Narrative persistent consequence

와 중복.

## Confidence

**HIGH as cross-genre specialization / LOW-MEDIUM need for separate RPG Core**

## Reviewer Action

Persistent Trait가 있다면:

> **“이 Trait가 다음 30분 플레이에서 무엇을 실제로 바꾸는가?”**

를 묻는다.

---

# GC-RPG-006 — Equipment Should Create Choice, not Only Replacement

**Status:** `CANDIDATE`

## Rule Candidate

> **Equipment를 RPG Progression의 주요 축으로 제시한다면 새 장비가 항상 기존 장비의 상위 숫자라 자동 교체되는지, 아니면 Role / Skill / Resistance / Trade-off / Interaction 차이를 만들어 선택을 요구하는지 검토한다.**

## Evidence

현재 Direct RPG Equipment Evidence 부족.

Darkest Dungeon은 장비 / trinket이 존재하지만 Studio Reference의 직접 분석은 Equipment Choice보다 Attrition에 집중한다.

FTL의 weapon / system 선택은 Equipment-like trade-off의 Adjacent Evidence이나 RPG Core로 사용하지 않는다.

## Status Reason

중요하지만 Evidence Gap이 큼.

## Candidate Metric

- Equip Rate
- Immediate Replacement Rate
- Equipment Lifetime
- Universal Best Item Rate
- Build-compatible Equipment Usage
- Unequip / Swap Frequency

## Human

- Equipment Choice Quality
- “새 장비가 고민인가 자동 교체인가?”

## Confidence

**MEDIUM-LOW**

---

# GC-RPG-007 — Commitment / Respec Must Match Character Ownership

**Status:** `CANDIDATE`

## Rule Candidate

> **Character-build RPG에서 투자 선택이 너무 쉽게 완전 무효화되면 Character History가 약해질 수 있고, 반대로 초기 정보 부족 상태의 투자가 장시간 수정 불가하면 실험 비용이 과도해질 수 있다. Commitment와 Respec 비용을 Product Promise에 맞춰 검증한다.**

## Evidence

현재 Direct Respec Evidence 거의 없음.

Deckbuilding / Roguelike pivot과 유사하지만 RPG의:
- long campaign
- character ownership
관점이 다름.

## Candidate Metric

- Respec Rate
- Build Reset Timing
- Build Regret
- Early Choice → Final Build Correlation
- Abandoned Character Rate

## Human

- Build Ownership
- Progression Regret
- Respec Perception

## Confidence

**LOW-MEDIUM**

---

# GC-RPG-008 — Player Skill / Character Skill Balance Must Match Subtype

**Status:** `CANDIDATE`

## Rule Candidate

> **Action / Skill-check / Turn-based RPG에서는 Player execution과 Character stat / ability가 결과에 기여하는 비율이 Product Promise와 맞는지 검토한다. 어느 한쪽이 항상 우월하다고 일반화하지 않는다.**

## Evidence

현재 Direct Action RPG Evidence 없음.

Citizen Sleeper:
Character / dice / slot 중심.

Darkest Dungeon:
Character stats + player tactical decision 중심.

## Promotion Blocker

Action RPG / ARPG / skill-heavy evidence 부족.

## Candidate Metric

- Character Stat → Outcome Contribution
- Player Execution → Outcome Contribution
- Same Build / Different Player Outcome Variance
- Same Player / Different Build Outcome Variance

모두 model-dependent.

## Human

- Character Skill / Player Skill Balance
- Build impact perception

## Confidence

**LOW**

---

# 9. RPG Anti-Patterns

# AP-RPG-001 — More Stats = More Roleplaying

## Trigger
Stat 종류가 많다는 이유로 RPG depth를 주장.

## Consequence
- UI complexity
- balance cost
- dump stat
- no meaningful identity

## Detection
- Stat Usage by Context
- Universal Stat Concentration
- Dump Stat Candidate
- Human stat meaning

## Mitigation
각 Stat에:
> 어떤 해결 방식 / role / content를 바꾸는가?
를 정의.

---

# AP-RPG-002 — Level Number without Character Change

## Trigger
Level은 오르지만:
- new capability
- role shift
- meaningful power milestone
이 거의 없음.

## Boundary
Vertical power fantasy는 예외.

## Detection
- Dead Level Count
- New Action Unlock Rate
- Progression Stage → Action Shift

## Mitigation
모든 level이 아니라 progression milestone 중심으로 의미 설계.

---

# AP-RPG-003 — Skill Tree with Fake Forks

## Trigger
Node는 많지만:
- prerequisite
- value
- synergy
때문에 사실상 하나의 경로.

## Detection
- Skill Selection Concentration
- Build Convergence
- Fork Survival Rate
- Never-picked Skill

## Mitigation
Node 수보다 distinct build outcome 검증.

---

# AP-RPG-004 — Universal Best Stat

## Trigger
모든 Build가 같은 Stat을 우선.

## Detection
- Stat Allocation Concentration
- Win / success by stat
- cross-class same stat priority

## Mitigation
Context / role별 value shift.

---

# AP-RPG-005 — Dump Stat without Trade-off

## Trigger
대부분 Context에서 투자 가치가 없음.

## Detection
- near-zero allocation
- low check exposure
- low outcome contribution

## Mitigation
Stat 삭제 / 통합 / dedicated use context 검토.

---

# AP-RPG-006 — Class Name without Mechanical Identity

## Trigger
Warrior / Mage / Rogue지만 행동 패턴이 거의 동일.

## Evidence
Dicey Dungeons의 character rule variation이 반대 사례.

## Detection
- Class Action Similarity
- Skill overlap
- position / target overlap

## Mitigation
Class마다 distinct problem-solving pattern 정의.

---

# AP-RPG-007 — Fiction / Mechanics Mismatch

## Trigger
Fictional expert인데 actual system advantage 없음.

## Detection
- Fictional role claim → capability mapping
- human mismatch report

## Mitigation
fiction claim을 낮추거나 actual capability 부여.

---

# AP-RPG-008 — Build without Supporting Content

## Trigger
Build 선택은 많지만 활용할 encounter / quest가 없음.

## Detection
- Skill Opportunity Exposure
- Build → Encounter Usage
- Dead Investment Rate

## Mitigation
새 Build보다 existing content coverage 우선.

---

# AP-RPG-009 — Equipment as Linear Number Replacement

## Trigger
새 장비가 항상:
`+10 → +12`

## Consequence
Equipment UI는 있으나 decision 없음.

## Detection
- Immediate Replacement Rate
- Item Lifetime
- Swap decision rate

## Mitigation
trade-off / role / effect difference.

---

# AP-RPG-010 — Loot Volume as Progression

## Trigger
Loot 수 자체를 RPG variety로 사용.

## Consequence
inventory burden / low-value drops.

## Detection
- Unused Loot Rate
- meaningful equip rate
- immediate discard rate

## Mitigation
drop count보다 equip decision quality.

---

# AP-RPG-011 — Progression Convergence

## Trigger
후반에 모든 Character가 같은 핵심 Skill / Stat 획득.

## Detection
- Final Build Similarity
- Class Action Similarity
- Universal unlock rate

## Mitigation
Product Promise에 따라 exclusivity / cap / role-specific progression.

---

# AP-RPG-012 — Early Build Trap

## Trigger
초반 정보 부족 상태의 선택이 장기 Character를 망침.

## Boundary
Hardcore buildcraft에서 실험 / knowledge가 핵심일 수 있음.

## Detection
- Early Choice → Failure
- Respec demand
- build regret
- abandoned character

## Mitigation
preview / limited respec / low-cost early experiment.

---

# AP-RPG-013 — Respec Erases Identity

## Trigger
무비용 / 무제한 완전 변경으로 long-term formation 의미 약화.

## Boundary
Experimentation-heavy RPG에서는 장점.

## Detection
- Respec Frequency
- rapid build cycling
- human ownership perception

## Mitigation
Product Promise에 맞는 friction.

---

# AP-RPG-014 — Roleplay Choice with Universal Reward Winner

## Trigger
Expressive option이 존재하지만 한 선택이:
- reward
- power
- relationship
모두 우월.

## Deduplication

Narrative `Roleplay vs Dominant Utility`가 Primary.

RPG에서는:
> Character Identity expression이 mechanical reward 때문에 사라지는가?
만 본다.

---

# AP-RPG-015 — Character Skill Irrelevant to Player Skill

## Trigger
Action RPG에서 build investment가 체감되지 않거나,
반대로 Player execution이 거의 의미가 없음.

## Boundary
Product Promise에 따라 둘 다 가능.

## Detection
- same player different build
- same build different player
outcome variance.

---

# 10. Conflicting Findings

# CF-RPG-001 — Vertical vs Horizontal Progression

## Vertical
- power fantasy
- clarity
- reward cadence

## Horizontal
- capability
- role change
- solution expansion

## Resolution

Vertical = shallow로 평가하지 않는다.

`UC-DESIGN-006`은:
> **Decision change를 별도 축으로 측정하라**
는 Rule이지
> vertical growth를 제거하라
가 아니다.

---

# CF-RPG-002 — Fixed Class vs Free Build

## Fixed
- identity
- readability
- authored balance

## Free
- expression
- experimentation
- hybrid role

## Resolution
Product Promise에 종속.

---

# CF-RPG-003 — Commitment vs Respec

## Commitment
- history
- ownership
- differentiated character

## Respec
- experimentation
- recovery from bad information
- long game accessibility

## Resolution
Universal 정답 없음.

---

# CF-RPG-004 — Player Skill vs Character Skill

Action RPG / Turn-based / Narrative RPG를 같은 기준으로 평가하지 않는다.

---

# CF-RPG-005 — Unique Character vs Replaceable Roster

Darkest Dungeon:
attachment + replaceability tension.

Single protagonist:
replacement 개념이 부적절.

---

# CF-RPG-006 — Mechanical Optimization vs Roleplay Expression

일부 RPG는 build optimization 자체가 주요 fantasy.

Roleplay freedom이 반드시 핵심은 아니다.

---

# CF-RPG-007 — Party Synergy vs Individual Identity

Character가:
- unique person
인지
- party function component
인지
Product Promise에 따라 다름.

---

# CF-RPG-008 — Power Fantasy vs Persistent Consequence

Injury / loss가 성장 감각을 상쇄할 수 있다.

Darkest Dungeon에서는 의도적.

다른 RPG에는 자동 적용 금지.

---

# 11. Structural / Simulation Validation Map

# 11.1 Progression Metrics

| Metric | Type |
|---|---|
| Level Distribution | Simulation / Telemetry |
| XP Curve | Structural |
| Time / Encounters per Level | Simulation / Telemetry |
| Skill Unlock Timing | Simulation / Telemetry |
| New Action Unlock Rate | Structural / Simulation |
| Dead Level Count | Structural / model-dependent |
| Progression Choice Frequency | Telemetry |

---

# 11.2 Build Metrics

| Metric | Type |
|---|---|
| Build Distribution | Simulation / Telemetry |
| Build Concentration | Simulation |
| Build Success Distribution | Simulation |
| Build Convergence | Simulation / model-dependent |
| Respec Rate | Player Telemetry / Simulation if explicit |
| Build Pivot Rate | Player Telemetry / Simulation |
| Final Build Similarity | Simulation / model-dependent |

---

# 11.3 Stat Metrics

| Metric | Type |
|---|---|
| Stat Allocation Distribution | Simulation / Telemetry |
| Universal Stat Concentration | Simulation / model-dependent |
| Dump Stat Rate | Simulation / model-dependent |
| Stat Usage by Context | Simulation / Telemetry |
| Stat → Outcome Contribution | Structural / model-dependent |

---

# 11.4 Skill Metrics

| Metric | Type |
|---|---|
| Skill Usage Rate | Simulation / Telemetry |
| Skill Concentration | Simulation |
| Never-used Skill Rate | Simulation / Telemetry |
| Context-specific Skill Usage | Simulation |
| Universal Best Skill Candidate | Simulation / model-dependent |
| Skill Synergy Usage | Simulation / model-dependent |

---

# 11.5 Equipment Metrics

| Metric | Type |
|---|---|
| Equip Rate | Player Telemetry / Simulation |
| Immediate Replacement Rate | Player Telemetry / Simulation |
| Equipment Lifetime | Player Telemetry / Simulation |
| Universal Best Item Rate | Simulation / model-dependent |
| Build-compatible Equipment Usage | Simulation / model-dependent |
| Unused Loot Rate | Player Telemetry / Simulation |

---

# 11.6 Role Metrics

| Metric | Type |
|---|---|
| Class Action Distribution | Simulation / Telemetry |
| Class-specific Solution Usage | Simulation / Telemetry |
| Role Overlap | Structural / model-dependent |
| Party Role Coverage | Structural / model-dependent |
| Role-specific Success / Failure | Simulation |

---

# 11.7 Content Coverage Metrics

| Metric | Type |
|---|---|
| Build → Encounter Usage | Simulation / model-dependent |
| Skill → Opportunity Exposure | Structural / Simulation |
| Stat Check Exposure | Structural / Simulation |
| Class-specific Content Exposure | Structural / Simulation |
| Dead Investment Rate | Structural / model-dependent |

---

# 11.8 Persistent Character State Metrics

| Metric | Type |
|---|---|
| Trait Duration | Simulation |
| Injury / Condition Duration | Simulation |
| Condition Impact | Structural / model-dependent |
| Relationship State | Simulation / Telemetry |
| Recovery | Simulation / Telemetry |
| Character Loss | Simulation / Telemetry |

Interpretation:
- Management recovery quality
- Narrative consequence meaning
은 해당 Genre/Human layer로 분리한다.

---

# 12. RPG Tester Profile Map

Persona는 Rule을 바꾸지 않고 investment / action policy만 바꾼다.

# P-RPG-001 — Vertical Power Optimizer

우선:
- direct stat
- damage
- immediate numeric upgrade

검출:
- universal power path
- linear progression dominance

---

# P-RPG-002 — Specialist

한:
- role
- stat
- skill family
에 집중.

검출:
- specialization viability
- content support
- lock-in

---

# P-RPG-003 — Generalist

폭넓은 분산 투자.

검출:
- jack-of-all-trades dominance
- specialization reward

---

# P-RPG-004 — Roleplayer Policy

사전 정의 Tag:
- lawful
- aggressive
- support
- stealth
등에 맞는 행동을 우선.

**LLM 자유 감성 판단 금지.**

검출:
- role expression support
- reward conflict

---

# P-RPG-005 — Explorer

저사용:
- skill
- equipment
- stat
- solution
선호.

검출:
- dead content
- hidden viable option
- low-use asset

---

# P-RPG-006 — Respec / Pivot Tester

여러 progression stage에서 build 변경.

검출:
- hard lock
- zero-cost exploit
- content adaptability

---

# 13. Human Validation Map

# H-RPG-001 — Character Identity

> **내 Character가 어떤 존재인지 한 문장으로 설명할 수 있는가?**

---

# H-RPG-002 — Mechanical Identity

> **다른 Character / Build와 실제 플레이 방식이 다르다고 느끼는가?**

---

# H-RPG-003 — Progression Meaning

> **성장 후 무엇을 새롭게 할 수 있게 되었는가?**

---

# H-RPG-004 — Power Growth

> **강해졌다고 느끼는가?**

Vertical progression의 별도 축.

---

# H-RPG-005 — Build Ownership

> **이 Build가 자신이 형성한 Character라고 느끼는가?**

---

# H-RPG-006 — Role Expression

> **Character 성향 / 역할을 선택으로 표현할 수 있었는가?**

---

# H-RPG-007 — Fiction / Mechanics Alignment

> **설정상 잘한다고 말하는 것과 실제 Gameplay 능력이 일치하는가?**

---

# H-RPG-008 — Progression Regret

> **과거 투자를 후회하는가? 왜 그런가?**

---

# H-RPG-009 — Respec Perception

> **Build 변경이 너무 어렵거나 너무 가볍다고 느끼는가?**

---

# H-RPG-010 — Equipment Choice

> **새 Equipment가 자동 교체인가, 고민할 Choice인가?**

---

# H-RPG-011 — Character Attachment

Party / Roster RPG에서만.

---

# H-RPG-012 — Party Identity

> **각 Party Member가 서로 다른 역할 / 인물로 기억되는가?**

---

# H-RPG-013 — Build-supporting Content

> **자신의 Build가 실제로 빛난 순간이 있었는가?**

---

# H-RPG-014 — Player Skill / Character Skill Balance

Subtype-dependent.

---

# 14. AI Tester Interpretation Limits

Machine이 강한 것:

```text
Build distribution
Build convergence
Stat allocation
Skill use
Equipment use
Class solution
Content coverage
Persistent state
Progression timing
```

Machine이 직접 결론내리지 않는 것:

```text
내 캐릭터 같다.
성장한 느낌이다.
Roleplaying이 된다.
Class Fantasy가 좋다.
Build를 내가 만들었다.
Companion에게 애착이 간다.
```

그리고:

```text
Build Diversity ↑
≠
Character Identity Quality ↑
```

```text
Skill Usage ↑
≠
Progression Meaning ↑
```

---

# 15. Player Telemetry vs Simulation

구분:

```text
AI Build State
→ 구조적 가능성

Player Telemetry
→ 실제 선택 / 사용

Human
→ 이해 / ownership / fantasy
```

AI Tester가:
- 모든 Skill
- 모든 Build
- 모든 hidden formula
를 알고 있다고 해서

> Player가 Build를 이해했다

고 기록하지 않는다.

---

# 16. Scale Handoff Candidates

# SCALE_HANDOFF-RPG-001 — Class × Skill × Equipment Matrix

```text
Class
× Skill
× Equipment
× Enemy
× Encounter
```

QA 폭증.

---

# SCALE_HANDOFF-RPG-002 — Quest × Build Coverage

여러 Build를 Quest에서 지원할수록:
- condition
- branch
- alternate solution
- dialogue
비용 증가.

---

# SCALE_HANDOFF-RPG-003 — Companion Cost

Companion 증가:

- Art
- Animation
- Dialogue
- Combat AI
- Relationship
- Quest
- State
- Voice

비용 증가.

---

# SCALE_HANDOFF-RPG-004 — Equipment Content Cost

Loot 증가:

- icon/model
- data
- balance
- drop
- UI
- QA

증가.

---

# SCALE_HANDOFF-RPG-005 — Progression QA Matrix

- prerequisite
- respec
- equipment
- skill synergy
- stat cap
조합 QA.

---

# SCALE_HANDOFF-RPG-006 — Narrative Reactivity Multiplier

Class / Stat / Background를 Dialogue / Quest에서 반응시키면 Narrative Scope 증가.

---

# SCALE_HANDOFF-RPG-007 — Build-supporting Content Cost

Mechanical build variety를 실제로 살리려면:
- enemy
- environment
- quest
- exploration obstacle
가 필요할 수 있다.

즉:
> Build System Scope와 Content Scope는 별개가 아니다.

---

# 17. Universal Reclassification Candidates

# UC-RECLASS-RPG-001 — Progression Should Change Capability or Decision Context

## Decision

새 Universal Core를 만들지 않는다.

현재 `UC-DESIGN-006`을 강화하는 Evidence로 보낸다.

### RPG Contribution

Progression 변화는:
- new action
- new role
- solution access
- limitation removal
등으로 측정할 수 있다.

---

# UC-RECLASS-RPG-002 — Identity Claims Need Behavioral Consequences

Potential Universal:
- Simulation Agent
- Strategy Unit
- Character RPG

에 확장 가능.

현재 RPG / Character evidence가 부족해 승격 보류.

---

# UC-RECLASS-RPG-003 — Choice Diversity Requires Content that Rewards Different Strengths

Deckbuilding / Strategy / RPG 전반에 확장 가능.

하지만 이미:
- Contextual Value
- Objective-conditioned Value
와 중복 가능성이 높다.

승격 보류.

---

# 18. Evidence Gaps

# GAP-RPG-001 — Direct CRPG Design Evidence

필요:
- build
- skill check
- quest solution
- party
- respec
- narrative expression.

---

# GAP-RPG-002 — JRPG Role / Progression

필요:
- fixed character identity
- party switching
- power curve
- progression choice
- role differentiation.

---

# GAP-RPG-003 — Action RPG Player Skill vs Character Skill

필요:
- same player / different build
- same build / different player
- stat contribution.

---

# GAP-RPG-004 — Skill Tree Behavior

필요:
- node pick rate
- path convergence
- respec
- dead node
- branch timing.

---

# GAP-RPG-005 — Build Regret / Respec

필요:
- regret timing
- respec use
- character abandonment
- onboarding knowledge.

---

# GAP-RPG-006 — Stat Usage / Dump Stat

필요:
- allocation
- context use
- check exposure
- outcome contribution.

---

# GAP-RPG-007 — Quest Solution by Build

핵심 Gap.

여러 Build가 실제:
- combat
- dialogue
- exploration
- stealth
에서 다른 Solution을 갖는지 자료 부족.

---

# GAP-RPG-008 — Companion Attachment

필요:
- companion usage
- party removal
- relationship
- narrative attachment
- combat role.

---

# GAP-RPG-009 — Equipment Replacement

필요:
- item lifetime
- swap
- discard
- universal best item
- meaningful equip rate.

---

# GAP-RPG-010 — Character Identity Perception

필요:
- self-description
- build ownership
- class identity
- fiction/mechanics alignment.

---

# GAP-RPG-011 — Progression Ceiling

필요:
- endgame convergence
- all-skill acquisition
- class distinction late game.

---

# GAP-RPG-012 — Underperforming RPG Controls

특히:
- fake skill tree
- universal stat
- build trap
- loot bloat
- class sameness
- quest build irrelevance
실패 사례.

---

# 19. Additional References Needed

현재 RPG는 **P0 research가 다른 장르보다 중요하다.**

# P0 — Disco Elysium

## 강화 후보

- `GC-RPG-001`
- `GC-RPG-002`
- Fiction / Mechanics Alignment
- Skill Check
- Roleplay

## Counter Evidence

Mechanical combat 없이도 RPG Identity가 성립하는 조건.

## Needed Evidence

- developer design talk
- skill system analysis
- failed-check design
- player skill distribution if public

---

# P0 — Baldur's Gate 3

## 강화 후보

- `GC-RPG-001`
- `GC-RPG-004`
- Party / Class
- Quest Solution by Build

## Critical Research Question

> **Build 차이가 실제 Quest / Encounter Solution Space를 바꾸는가?**

## Needed Evidence

- developer talks
- class / solution telemetry
- quest design breakdown

---

# P0 — Divinity: Original Sin 2

## 강화 후보

- Build freedom
- Party composition
- Environment interaction
- Respec
- Skill combination

## Counter Question

Free build가 identity를 강화하는가, convergence를 만드는가?

---

# P0 — Mass Effect 2

## 강화 후보

- Companion identity
- Party role
- loyalty
- narrative consequence

## Needed Evidence

- companion selection
- loyalty design
- party role design
- attachment data if public

---

# P0 — Final Fantasy X / Representative JRPG Study

## 강화 후보

- Fixed role
- Party switching
- Vertical growth
- Sphere Grid
- Character differentiation

## Purpose

Western CRPG bias 방지.

---

# P1 — Diablo II / IV

강화:
- Equipment
- Loot
- Skill Tree
- Build commitment
- Power fantasy
- Respec

---

# P1 — Path of Exile

강화:
- extreme build space
- complexity
- identity
- respec cost
- convergence.

---

# P1 — Dragon Age: Origins

강화:
- party
- class
- companion
- roleplay
- build.

---

# P1 — Fallout: New Vegas

강화:
- stat / skill check
- quest solution
- faction
- character build.

---

# P1 — Elden Ring

강화:
- player skill vs character build
- stat investment
- weapon identity
- respec
- encounter support.

---

# 20. Promotion Table

| ID | Name | Decision | Status | Confidence |
|---|---|---|---|---|
| GC-RPG-001 | Character Investment Changes Available Solutions | NEW / UC SPECIALIZATION | KEEP AS CANDIDATE | HIGH as specialization / MEDIUM independent |
| GC-RPG-002 | Mechanical Role Claims Need Behavioral Consequences | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-RPG-003 | Character Formation Preserves Differentiation | NEW | KEEP AS CANDIDATE | MEDIUM |
| GC-RPG-004 | Build Variety Needs Supporting Content | NEW | KEEP AS CANDIDATE | MEDIUM-HIGH |
| GC-RPG-005 | Persistent Character Consequences Change Future Play | UC / OTHER GENRE SPECIALIZATION | KEEP AS CANDIDATE | HIGH cross-genre / LOW-MEDIUM independent |
| GC-RPG-006 | Equipment Creates Choice, not Only Replacement | NEW | KEEP AS CANDIDATE | MEDIUM-LOW |
| GC-RPG-007 | Commitment / Respec Matches Character Ownership | NEW | KEEP AS CANDIDATE | LOW-MEDIUM |
| GC-RPG-008 | Player Skill / Character Skill Balance Matches Subtype | NEW | KEEP AS CANDIDATE | LOW |

## Provisional Genre Core

**NONE at current Evidence level.**

---

# 21. RPG Reviewer Default Set

신규 RPG 기획을 검토할 때 우선 적용할 15개 질문.

## Q1 — RPG Formation

> **Player가 실제로 어떤 Character / Party State를 형성하는가?**

---

## Q2 — Persistent Identity

> **그 선택이 Encounter 하나를 넘어 Character에 남는가?**

---

## Q3 — Progression Meaning

> **성장 후 무엇을 새롭게 할 수 있게 되는가?**

관련:
`UC-DESIGN-006 / GC-RPG-001`

---

## Q4 — Vertical Growth

> **숫자 성장 자체가 Product Promise에서 어떤 보상을 제공하는가?**

Vertical을 자동 감점하지 않는다.

---

## Q5 — Mechanical Role

> **Class / Build가 실제 Action / Position / Target / Solution 차이를 만드는가?**

관련:
`GC-RPG-002`

---

## Q6 — Fiction / Mechanics

> **게임이 주장하는 Character Identity가 실제 Capability에 표현되는가?**

---

## Q7 — Stat Value

> **각 핵심 Stat에 실제 사용 Context가 존재하는가?**

---

## Q8 — Dominance

> **Universal Best Stat / Skill / Build가 Context와 무관하게 수렴하지 않는가?**

---

## Q9 — Skill Tree

> **Fork가 실제 서로 다른 Character Formation으로 이어지는가?**

---

## Q10 — Equipment

> **새 Equipment가 자동 숫자 교체인가, Role / Trade-off Choice인가?**

관련:
`GC-RPG-006`

---

## Q11 — Supporting Content

> **선택 가능한 Build를 실제 Encounter / Quest / Exploration이 시험하는가?**

관련:
`GC-RPG-004`

---

## Q12 — Commitment / Respec

> **Build 선택을 수정하는 비용이 Campaign 길이와 Experimentation Promise에 맞는가?**

관련:
`GC-RPG-007`

---

## Q13 — Player vs Character Skill

> **Player execution과 Character investment의 기여 비율이 Subtype에 맞는가?**

관련:
`GC-RPG-008`

---

## Q14 — Machine vs Human

> **Build / Usage / Coverage는 Simulation으로, Identity / Ownership / Fantasy는 Human으로 분리했는가?**

---

## Q15 — Evidence Boundary

> **현재 Darkest Dungeon / Citizen Sleeper 중심 Evidence를 CRPG / JRPG / ARPG 전체에 과도하게 일반화하고 있지 않은가?**

---

# 22. Default Metric Bundle

Metric은 Criteria가 아니다.

Threshold는 프로젝트별 Validation Planner가 정한다.

## Structural / Machine

- Level Count
- Skill Count
- Stat Count
- Equipment Count
- Skill Prerequisite Graph
- Class Capability Coverage
- Encounter Requirement Coverage
- Stat Check Definition Count
- Class-specific Capability Count

---

## Structural / model-dependent

- Build Identity
- Role Overlap
- Dead Investment
- Universal Best Stat
- Universal Best Skill
- Character Differentiation
- Fiction / Mechanics Alignment
- Build-supporting Content Coverage
- Stat → Outcome Contribution
- Skill → Outcome Contribution
- Dead Level Count
- Final Build Similarity
- Universal Best Item

Project-specific Formal Definition 없이 일반 Machine Metric으로 자동 사용하지 않는다.

---

## Simulation

- Build Distribution
- Build Concentration
- Build Success Distribution
- Stat Allocation Distribution
- Skill Usage
- Equipment Usage
- Class-specific Action Distribution
- Progression Timing
- Character State Distribution
- Party Composition Distribution
- Skill Unlock Timing
- Context-specific Skill Usage
- Role-specific Success / Failure

## Simulation / model-dependent

- Build Convergence

### Interpretation Rule

`Build Convergence`는 프로젝트별 Build Similarity 정의 없이 일반 Simulation Metric으로 자동 사용하지 않는다.

예를 들어 다음은 서로 다른 수렴 정의가 될 수 있다.

```text
Skill 구성 유사도
Action Distribution 유사도
Role / Function 유사도
Equipment / Stat 구성 유사도
```

따라서 어떤 축을 기준으로 “서로 다른 Build가 같은 결과로 수렴했다”고 판정하는지 Formal Definition을 먼저 고정한다.

---

## Instrumented Player Telemetry

- Level-up Choice
- Skill Selection
- Stat Allocation
- Equipment Equip / Unequip
- Respec
- Build Reset
- Dialogue / Skill-check Selection
- Party Change
- Character Inspection
- Progression Screen Usage
- Decision Time
- Equipment Lifetime
- Immediate Replacement
- Build Abandonment if observable

---

## Instrumented / Simulation

명시적인 Game Action인 경우:

- Skill Use
- Item Equip
- Party Assignment
- Respec
- Dialogue Solution
- Stat Check
- Rest / Recovery

### Interpretation Rule

AI internal Build evaluation을 Player Understanding으로 취급하지 않는다.

예:

```text
AI knows optimal stat
≠
Player understood stat value
```

---

## Human

- Character Identity
- Mechanical Identity
- Progression Meaning
- Power Growth Satisfaction
- Build Ownership
- Role Expression
- Fiction / Mechanics Alignment
- Progression Regret
- Respec Perception
- Equipment Choice Quality
- Character Attachment
- Party Identity
- Build Fantasy
- Character Skill / Player Skill Balance

---

## Hybrid

- Meaningful Build Diversity
- Progression Quality
- Character Differentiation Quality
- Roleplay Quality
- Build-supporting Content Quality
- Equipment Decision Quality
- Stat Value Diversity
- Party Synergy Quality
- Progression Pacing
- Build Commitment Quality
- Class Identity Quality
- Character Consequence Quality

---

# 23. Self-Review Result

## Check 1 — Level / EXP = RPG Core
**PASS**

Level 자체를 Core로 만들지 않았다.

## Check 2 — Stat Count = RPG Depth
**PASS**

Anti-pattern으로 분리.

## Check 3 — Vertical Progression automatically bad
**PASS**

Power Fantasy Boundary 유지.

## Check 4 — UC-DESIGN-006 duplicate
**PASS**

`GC-RPG-001`을 Candidate specialization으로만 유지.

## Check 5 — Darkest Dungeon Management duplicate
**PASS**

Recovery / Roster priority를 RPG Core로 복제하지 않았다.

## Check 6 — Citizen Sleeper Narrative duplicate
**PASS**

Opportunity Cost / Narrative Coupling을 RPG Core로 복제하지 않았다.

## Check 7 — Class name = mechanical identity
**PASS**

`GC-RPG-002 / AP-RPG-006`에서 behavioral evidence 요구.

## Check 8 — Skill Tree Node Count = Build Depth
**PASS**

Build distribution / convergence / supporting content를 검토.

## Check 9 — Equipment Count = Progression Depth
**PASS**

Equip decision quality와 replacement를 분리.

## Check 10 — Player Skill vs Character Skill
**PASS WITH EVIDENCE GAP**

Candidate로만 유지.

## Check 11 — Build Variety + Supporting Content
**PASS**

`GC-RPG-004`.

## Check 12 — Machine Build Distribution = Character Identity
**PASS**

Human layer 분리.

## Check 13 — Western CRPG 기준 generalization
**PASS**

JRPG / ARPG Evidence Gap 명시.

## Check 14 — Genre vs Scope
**PASS**

Class × Skill × Equipment / Quest / Companion은 Scale Handoff.

## Check 15 — Weak Direct Evidence boundary
**PASS**

신규 Provisional을 0개로 유지.

---

# 24. Final Position

현재 Studio OS RPG Knowledge Base에서는:

## Provisional Genre Core

**없음.**

이는 RPG에 Core가 없다는 의미가 아니다.

현재 Studio Reference의 Direct RPG Evidence가:
- Darkest Dungeon의 Roster / Persistent Consequence
- Citizen Sleeper의 Narrative Economy
에 편중되어 있고,

가장 강한 RPG 원칙 후보가 이미:
- `UC-DESIGN-006`
- Narrative
- Management
- Strategy
와 상당 부분 겹치기 때문에 **승격을 보류**한 것이다.

현재 Candidate:

1. `GC-RPG-001 — Character Investment Should Change Available Solutions`
2. `GC-RPG-002 — Mechanical Role Claims Need Behavioral Consequences`
3. `GC-RPG-003 — Character Formation Should Preserve Differentiation`
4. `GC-RPG-004 — Build Variety Needs Supporting Content`
5. `GC-RPG-005 — Persistent Character Consequences Should Change Future Play`
6. `GC-RPG-006 — Equipment Should Create Choice, not Only Replacement`
7. `GC-RPG-007 — Commitment / Respec Must Match Character Ownership`
8. `GC-RPG-008 — Player Skill / Character Skill Balance Must Match Subtype`

이번 Extraction에서 가장 중요한 결과는 신규 Genre Core 숫자가 아니라:

> **`UC-DESIGN-006 — Progression Should Match Its Intended Promise`이 RPG 검토에서 매우 강한 상위 Rule이라는 점이 재확인되었다.**

다만 정확한 표현은:

> **RPG의 성장은 반드시 Horizontal이어야 한다**

가 아니다.

더 정확한 질문은:

> **이 RPG가 Character Formation을 약속한다면 성장 전후 Character의 Capability / Role / Solution / Identity 중 무엇이 실제로 달라지는가?**

다.

또한 RPG Review에서 다음을 강하게 구분해야 한다.

```text
Build Exists
≠
Build Matters
```

```text
Class Name Differs
≠
Playstyle Differs
```

```text
Equipment Count High
≠
Equipment Decisions Deep
```

```text
Character State Persists
≠
Character Identity Exists
```

현재 가장 중요한 다음 단계는 P0 RPG Reference 확보다.

우선순위:

1. Disco Elysium
2. Baldur's Gate 3
3. Divinity: Original Sin 2
4. Mass Effect 2
5. Representative JRPG Study

이 Evidence가 들어온 뒤에야:
- Character Identity
- Build / Solution Space
- Fiction / Mechanics Alignment
- Party / Companion
- Player Skill vs Character Skill
축 중 일부를 Provisional Core로 승격하는 것이 타당하다.

---

# 25. Source Trace

## Primary RPG Evidence
- REF-06 — Darkest Dungeon

## Strong RPG / Hybrid
- REF-23 — Citizen Sleeper
- REF-20 — Dicey Dungeons
- REF-02 — FTL
- REF-15 — This War of Mine

## Adjacent / Control
- REF-10 — 80 Days
- REF-07 — Against the Storm
- REF-09 — Reigns
- REF-12 — Vampire Survivors
- REF-27 — Tiny Rogues
- REF-18 — Loop Hero
- REF-03 — Into the Breach

## Baseline / Deduplication
- STUDIO_CORE_CANDIDATES_v0.2
- NARRATIVE_SYSTEMIC_CORE_CANDIDATES_v0.1
- STRATEGY_CORE_CANDIDATES_v0.1
- MANAGEMENT_CORE_CANDIDATES_v0.1
- ROGUELIKE_CORE_CANDIDATES_v0.1
- SIMULATION_CORE_CANDIDATES_v0.1
- Studio OS — RPG Genre Core Deep Extraction Prompt v0.1

---

# 26. Traceability Rule

Core는 원본 Reference를 대체하지 않는다.

RPG 위험 신호가 발견되면:

```text
RPG Candidate / Universal Core
↓
Primary / Strong Reference
↓
Character State
↓
Investment / Progression
↓
Available Capability
↓
Encounter / Quest Expression
↓
Persistent Identity
↓
Boundary / Trade-off
↓
Current Project
```

순서로 다시 내려가 검토한다.

`RPG_CORE_CANDIDATES_v0.1`은 현재 Evidence가 부족한 상태에서 RPG를 Feature 목록으로 일반화하지 않고, **Character Formation / Capability / Differentiation / Supporting Content**를 중심으로 다음 Evidence 수집과 신규 RPG Review를 구조화하기 위한 Candidate Baseline이다.
