# Game Design Case Study v1.0

> **Studio Game Design Reviewer --- Reference Library**\
> 목적: 상용 게임의 표면적인 Feature가 아니라, 설계 문제와 해결 원리를
> 분석하여 신규 게임 기획 검토 시 비교 Reference로 사용한다.

------------------------------------------------------------------------

## 0. Document Information

-   **Game Title:**
-   **Developer:**
-   **Publisher:**
-   **Release Year:**
-   **Genre:**
-   **Platform:**
-   **Development Scale:** Solo / Small Team / Mid-size / Large
-   **Analysis Date:**
-   **Document Version:**
-   **Primary Sources:**
-   **Secondary Sources:**

### Evidence Quality

-   **Developer-confirmed:** 개발자 인터뷰 / GDC / Postmortem 등으로
    확인
-   **Observed:** 실제 게임 구조에서 직접 관찰 가능
-   **Inferred:** 분석자가 구조를 바탕으로 추론
-   **Unknown:** 신뢰할 수 있는 근거 부족

분석 과정에서 사실과 추론을 가능한 한 구분한다.

------------------------------------------------------------------------

## 1. Executive Summary

### 1.1 One-Sentence Design Summary

이 게임이 어떤 플레이 경험을 제공하는지 한 문장으로 설명한다.

### 1.2 Why This Game Matters

이 게임을 Reference Library에 포함해야 하는 이유.

### 1.3 Primary Design Lessons

이 게임에서 얻을 수 있는 핵심 설계 교훈 3\~5개.

-   Lesson 1:
-   Lesson 2:
-   Lesson 3:

### 1.4 Primary Warning

이 게임을 다른 프로젝트에서 참고할 때 가장 주의해야 할 점.

------------------------------------------------------------------------

## 2. Game Overview

### 2.1 Core Concept

게임의 핵심 아이디어.

### 2.2 Player Fantasy

플레이어가 게임 안에서 무엇이 되거나 무엇을 한다고 느끼는가?

### 2.3 Target Player

주요 플레이어층과 요구되는 장르 경험.

### 2.4 Design Pillars

게임을 지탱하는 핵심 설계 원칙. 가능하면 3\~5개로 정리한다.

### 2.5 Unique Selling Proposition

비슷한 게임과 비교했을 때 이 게임을 구분하는 핵심 요소.

------------------------------------------------------------------------

## 3. Core Gameplay Structure

### 3.1 Core Player Verbs

플레이어가 반복적으로 수행하는 핵심 행동.

예: - 선택 - 이동 - 전투 - 배치 - 구매 - 관리 - 협상

### 3.2 Core Loop

다음 형식으로 표현한다.

`Player Action → Game Response → Result → Reward / Loss → New Decision → Repeat`

### 3.3 Short-Term Loop

수 초\~수 분 단위에서 반복되는 행동.

### 3.4 Session Loop

한 플레이 세션에서 반복되는 구조.

### 3.5 Long-Term / Meta Loop

여러 세션 또는 전체 게임에 걸쳐 반복되는 성장 구조.

### 3.6 Loop Strength

다음을 평가한다.

-   반복 동기가 명확한가?
-   결과가 다음 선택에 영향을 주는가?
-   보상이 새로운 판단을 만들어내는가?
-   시간이 지나면서 Loop가 발전하는가?
-   단순 반복 노동으로 변할 위험은 없는가?

------------------------------------------------------------------------

## 4. Decision Design

### 4.1 Primary Decisions

플레이어가 가장 자주 고민하는 선택.

### 4.2 Decision Frequency

선택이 얼마나 자주 발생하는가?

### 4.3 Decision Depth

선택 하나를 판단하기 위해 고려해야 하는 정보의 양.

### 4.4 Meaningful Choice

선택지가 실제로 서로 다른 결과와 전략을 제공하는가?

### 4.5 Dominant Strategy Risk

항상 우월한 선택이나 전략이 존재하는가? 존재한다면 게임이 이를 어떻게
통제하는가?

### 4.6 Opportunity Cost

하나를 선택함으로써 무엇을 포기하게 되는가?

### 4.7 Information Structure

플레이어가 판단할 때: - 무엇을 알고 있는가? - 무엇을 모르는가? - 무엇을
추론해야 하는가?

### 4.8 Uncertainty

불확실성이 어디에서 발생하는가?

-   RNG
-   Hidden Information
-   Player Skill
-   Opponent Behavior
-   Resource Constraint
-   Future Consequence

------------------------------------------------------------------------

## 5. Risk / Reward Structure

### 5.1 Primary Risks

플레이어가 감수하는 주요 위험.

### 5.2 Primary Rewards

플레이어가 얻는 주요 보상.

### 5.3 Risk Visibility

위험을 선택 전에 얼마나 예측할 수 있는가?

### 5.4 Failure Cost

실패하면 무엇을 잃는가?

### 5.5 Recovery

실패 후 회복할 방법이 있는가?

### 5.6 Snowball Structure

성공 또는 실패가 계속 누적되는 구조인가?

### 5.7 Comeback Mechanisms

불리해진 플레이어가 회복할 수 있는 구조가 존재하는가?

------------------------------------------------------------------------

## 6. Progression Design

### 6.1 Short-Term Progression

짧은 시간 동안 플레이어가 느끼는 성장.

### 6.2 Long-Term Progression

전체 플레이에 걸친 성장.

### 6.3 Horizontal vs Vertical Progression

-   **Vertical:** 수치적으로 강해지는 성장
-   **Horizontal:** 새로운 선택이나 전략이 추가되는 성장

어느 쪽을 중심으로 사용하는가?

### 6.4 Unlock Structure

새로운 콘텐츠와 시스템이 어떤 순서로 열린다?

### 6.5 Progression Motivation

플레이어가 다음 단계로 가고 싶어 하는 이유.

### 6.6 Progression Risks

-   Grind
-   Power Creep
-   Meaningless Upgrade
-   Late-game Stagnation

등의 위험이 존재하는가?

------------------------------------------------------------------------

## 7. Economy & Resource Design

### 7.1 Primary Resources

주요 자원 목록.

### 7.2 Sources

각 자원을 얻는 방법.

### 7.3 Sinks

각 자원을 소비하는 방법.

### 7.4 Scarcity

어떤 자원이 의도적으로 부족하도록 설계되었는가?

### 7.5 Resource Interaction

자원들이 서로 어떤 영향을 주는가?

### 7.6 Economic Pressure

플레이어에게 어떤 소비 판단을 요구하는가?

### 7.7 Economic Failure

경제 시스템이 무너질 수 있는 방식.

예: - 자원 무한 축적 - 특정 자원 무의미화 - 필수 Sink 부족 - 초반 빈곤 /
후반 과잉

------------------------------------------------------------------------

## 8. Difficulty & Failure Design

### 8.1 Sources of Difficulty

난이도가 어디에서 발생하는가?

-   Mechanical Skill
-   Strategic Decision
-   Resource Management
-   Information
-   Time Pressure
-   Randomness

### 8.2 Difficulty Curve

초반 → 중반 → 후반 난이도 변화.

### 8.3 Failure Structure

플레이어가 어떻게 실패하는가?

### 8.4 Failure Feedback

왜 실패했는지 플레이어가 이해할 수 있는가?

### 8.5 Learning Through Failure

실패가 다음 플레이를 위한 정보를 제공하는가?

### 8.6 Punishment Level

실패의 처벌 수준과 그 이유.

------------------------------------------------------------------------

## 9. Onboarding & Learning Curve

### 9.1 First 5 Minutes

플레이어에게 무엇을 먼저 경험시키는가?

### 9.2 First 30 Minutes

어떤 순서로 시스템을 학습시키는가?

### 9.3 Tutorial Method

-   Explicit Tutorial
-   Contextual Tutorial
-   Progressive Disclosure
-   Learning by Failure
-   Tooltips
-   NPC Guidance
-   No Tutorial

### 9.4 Complexity Introduction

복잡한 시스템을 한꺼번에 보여주는가, 단계적으로 공개하는가?

### 9.5 Cognitive Load

플레이어가 동시에 기억해야 하는 정보량.

### 9.6 Likely Onboarding Failure Points

초보자가 이탈하거나 혼란을 느낄 가능성이 높은 부분.

------------------------------------------------------------------------

## 10. Content & Variety

### 10.1 Content Types

게임이 사용하는 주요 콘텐츠 유형.

### 10.2 Content Reuse

기존 콘텐츠를 어떻게 재조합하는가?

### 10.3 Systemic Variety

새 콘텐츠를 계속 제작하지 않고도 시스템 상호작용으로 다양성을 만드는가?

### 10.4 Authored Variety

개발자가 직접 제작해야 하는 콘텐츠 양.

### 10.5 Repetition Management

반복 피로를 어떻게 방지하는가?

### 10.6 Content Production Efficiency

개발 비용 대비 플레이 시간과 다양성을 얼마나 확보하는가?

------------------------------------------------------------------------

## 11. Replayability

### 11.1 Replay Motivation

왜 다시 플레이하는가?

### 11.2 Run / Playthrough Variation

플레이마다 무엇이 달라지는가?

### 11.3 Build Variety

서로 다른 전략이나 플레이 스타일이 가능한가?

### 11.4 Randomness vs Authored Content

반복성을 RNG와 제작 콘텐츠 중 무엇으로 확보하는가?

### 11.5 Discovery

여러 번 플레이해야 발견할 수 있는 요소가 존재하는가?

### 11.6 Replayability Limit

반복 플레이가 어느 시점부터 약해지는가?

------------------------------------------------------------------------

## 12. UX & Information Design

### 12.1 Critical Information

플레이어가 항상 알아야 하는 정보.

### 12.2 Information Hierarchy

중요한 정보를 어떤 우선순위로 보여주는가?

### 12.3 Feedback

행동 → 결과의 관계가 명확하게 전달되는가?

### 12.4 Hidden Information

의도적으로 숨기는 정보와 그 이유.

### 12.5 UI Complexity

게임의 시스템 복잡도 대비 UI가 얼마나 복잡한가?

### 12.6 Decision Support

UI가 플레이어의 판단을 어떻게 지원하는가?

------------------------------------------------------------------------

## 13. Player Motivation & Psychology

### 13.1 Primary Motivation

플레이어를 계속 플레이하게 하는 핵심 동기.

예: - Mastery - Discovery - Optimization - Collection - Narrative -
Expression - Competition - Survival

### 13.2 Short-Term Motivation

다음 몇 분을 플레이하게 만드는 요소.

### 13.3 Long-Term Motivation

게임을 계속 진행하게 만드는 요소.

### 13.4 Emotional Curve

게임이 의도하는 주요 감정 변화.

### 13.5 Tension / Release

긴장과 보상의 리듬.

------------------------------------------------------------------------

## 14. Scope & Production Efficiency

### 14.1 Development Scale

알려진 개발 인원, 기간, 개발 조건. 확실하지 않다면 추정하지 않고
Unknown으로 표시한다.

### 14.2 High-Cost Systems

제작 비용이 높았을 것으로 판단되는 부분.

### 14.3 Low-Cost / High-Impact Systems

상대적으로 적은 제작 비용으로 큰 플레이 효과를 만든 부분.

### 14.4 Content Burden

지속적으로 수작업 제작이 필요한 콘텐츠.

### 14.5 Technical Complexity

구현 및 유지보수 난도가 높은 구조.

### 14.6 Scope Efficiency

게임의 제작 범위 대비 실제 플레이 경험의 밀도.

### 14.7 Solo-Dev Applicability

1인 개발자가 참고할 수 있는 부분과 그대로 적용하기 어려운 부분을
구분한다.

------------------------------------------------------------------------

## 15. What Worked

게임에서 특히 성공적으로 작동한 설계를 정리한다.

### Success 01

-   **Design:**
-   **Problem it solves:**
-   **Why it works:**
-   **Dependencies:**
-   **Evidence:**
-   **Generalizable Lesson:**

------------------------------------------------------------------------

## 16. What Did Not Work / Limitations

게임의 단점이나 구조적 한계를 분석한다. 판매 성공 여부와 관계없이
평가한다.

### Limitation 01

-   **Problem:**
-   **Why it occurs:**
-   **Player impact:**
-   **Design dependency:**
-   **Possible reason it was accepted:**
-   **Generalizable Lesson:**

------------------------------------------------------------------------

## 17. Design Problem → Solution Analysis

### Case 01

-   **Design Problem:**
-   **Chosen Solution:**
-   **Why this solution fits this game:**
-   **Trade-offs:**
-   **Alternative solutions:**
-   **Reusable Principle:**

------------------------------------------------------------------------

## 18. What This Game Teaches

### Principle 01

-   **Principle:**
-   **Why it matters:**
-   **Applicable when:**
-   **Not applicable when:**

------------------------------------------------------------------------

## 19. What NOT to Copy

### Warning 01

-   **Feature:**
-   **Why it works in this game:**
-   **Why copying it may fail:**
-   **Required conditions:**
-   **Safer takeaway:**

------------------------------------------------------------------------

## 20. Solo Indie Developer Lessons

### 20.1 Worth Learning

적은 비용으로 높은 효과를 낸 설계.

### 20.2 Expensive to Reproduce

소규모 개발자가 그대로 따라 하기 어려운 설계.

### 20.3 Possible Simplification

비슷한 효과를 더 작은 Scope로 구현할 방법.

### 20.4 Scope Lesson

이 게임에서 얻을 수 있는 제작 범위 관련 교훈.

------------------------------------------------------------------------

## 21. Reference Comparison Tags

## \### Genre Tags

### Design Tags

예: - Resource Management - Risk / Reward - Hidden Information - Deck
Building - Roster Management

### Review Use Cases

예: - Core Loop Reference - Economy Reference - Onboarding Reference -
Scope Reference - Replayability Reference

### Relevant Project Types

어떤 종류의 신규 기획을 검토할 때 이 Case Study의 참고 가치가 높은가?

------------------------------------------------------------------------

## 22. Reviewer Quick Reference

## \### Strongest Lesson

## \### Biggest Warning

## \### Best Reference For

## \### Poor Reference For

## \### Core Design Principle

## \### Scope Lesson

------------------------------------------------------------------------

## 23. Final Assessment

### Design Strengths

1.  
2.  
3.  

### Design Weaknesses

1.  
2.  
3.  

## \### Most Important Innovation

## \### Most Important Trade-off

## \### Most Transferable Lesson

## \### Most Dangerous Misinterpretation

------------------------------------------------------------------------

## 24. Sources & Evidence

각 분석의 근거가 되는 자료를 기록한다.

우선순위:

1.  Developer Postmortem
2.  GDC / Developer Presentation
3.  Developer Interview
4.  Official Documentation
5.  Direct Game Observation
6.  High-quality Critical Analysis
7.  Player Community Evidence

각 Source에 가능하면 다음을 기록한다.

-   **Source:**
-   **Type:**
-   **Author:**
-   **Date:**
-   **Relevant Sections:**
-   **Reliability:**
-   **Notes:**

------------------------------------------------------------------------

## 25. Confidence & Unknowns

## \### High Confidence Findings

## \### Medium Confidence Findings

## \### Low Confidence / Inferred Findings

## \### Unknown Information

추론을 사실처럼 기록하지 않는다.

------------------------------------------------------------------------

# END OF CASE STUDY
