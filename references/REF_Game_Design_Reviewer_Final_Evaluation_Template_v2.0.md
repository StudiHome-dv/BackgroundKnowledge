# Studio Game Design Reviewer --- Final Evaluation Template v2.0

> **문서 목적**\
> 프로토타입 제작 직전의 게임 기획을 대상으로, **게임 설계 품질 → 특수
> 설계 문제 → 1인/소규모 제작 가능성 → 상업성 → 프로토타입 진입 여부**를
> 순서대로 판정하는 최종 Greenlight Review 템플릿이다.
>
> **기본 판매 목표 모델**\
> Steam PC 기준 **10K를 최소 검토선, 30K를 현실적 성공, 50K를 주요 목표
> 상단, 100K를 Stretch/Breakout**으로 취급한다. 100K+는 기본 사업계획의
> 전제가 아니다.

------------------------------------------------------------------------

## 0. Review Metadata

-   **Project:**
-   **Document Version:**
-   **Review Date:**
-   **Development Stage:** Concept / Pre-Prototype / Prototype Revision
    / Pre-Production
-   **Target Platform:**
-   **Expected Team Size:**
-   **Expected Development Period:**
-   **Expected Price Range:**
-   **Reviewer Confidence:** High / Medium / Low
-   **Missing Critical Information:**

------------------------------------------------------------------------

# 1. Executive Verdict

## 1.1 Final Decision

**FINAL VERDICT:** `GO / GO WITH CUTS / REVALIDATE / NO-GO`

**Prototype Entry:** `APPROVED / CONDITIONAL / HOLD / REJECTED`

### One-Sentence Verdict

> \[이 게임이 왜 진행할 가치가 있거나 없는지를 한 문장으로 작성\]

## \### Primary Strength

## \### Critical Risk

## \### Required Action Before Next Stage

------------------------------------------------------------------------

# 2. Concept Snapshot

-   **Core Fantasy:**
-   **Genre / Subgenre:**
-   **Target Player:**
-   **USP:**
-   **One-Sentence Store Hook:**
-   **Core Loop:**
-   **Expected Session Length:**
-   **Expected Total Playtime:**
-   **Expected Content Scale:**
-   **Expected Price:**
-   **Comparable Games:**

### Hook Test

다음 세 질문에 각각 `YES / PARTIAL / NO`로 답한다.

1.  게임을 처음 보는 사람이 **한 문장으로 핵심 판타지를 이해할 수
    있는가?**
2.  5\~10초 GIF/Trailer 장면만으로 **플레이의 차별점이 보이는가?**
3.  기존 장르 수요와 연결되면서도 **왜 이 게임을 사야 하는지가
    구분되는가?**

**Hook Verdict:** Strong / Adequate / Weak / Unclear

------------------------------------------------------------------------

# 3. Design Quality --- 25 Points

> **Reference Priority:** 1차 Core Design Reference 2\~3개를 우선
> 호출한다.

  항목                                     점수 핵심 판단
  ----------------------------------- --------- -----------
  Core Loop                                  /5 
  Meaningful Choice & Agency                 /4 
  Risk / Reward                              /3 
  Progression                                /3 
  Replayability / Content Longevity          /3 
  System Cohesion                            /4 
  Feedback & Readability                     /3 
  **Total**                             **/25** 

## 3.1 Core Loop Analysis

-   반복 행동:
-   반복이 재미를 유지하는 이유:
-   반복 피로 발생 예상 지점:
-   플레이어가 숙련되면서 바뀌는 판단:
-   Core Loop를 제거하면 게임 정체성이 무너지는 요소:

## 3.2 Meaningful Choice

-   주요 선택:
-   선택의 Opportunity Cost:
-   지배 전략 위험:
-   선택 결과의 가독성:
-   실패 후 복구 가능성:

## 3.3 Reference Comparison

각 Reference마다 반드시 다음 형식을 사용한다.

**\[Reference Game\]** - 현재 기획의 문제: - Reference가 해결했던
문제: - 조건의 공통점: - 조건의 차이: - 적용 가능한 원리: - 적용 시
Trade-off: - **판정:** Applicable / Partially Applicable / Not
Applicable

------------------------------------------------------------------------

# 4. Specialized Design Review --- 15 Points

> **Reference Priority:** 2차 Specialized Reference에서 실제 문제와
> 관련된 1\~3개만 호출한다.\
> 관련 없는 항목은 억지로 평가하지 않는다.

### Applicable Systems

-   [ ] RNG
-   [ ] AI / NPC
-   [ ] Auto Battle / Indirect Control
-   [ ] Management / Economy
-   [ ] Information / Monitoring
-   [ ] Stealth
-   [ ] Deduction
-   [ ] Narrative
-   [ ] Character State
-   [ ] Card / Common UI Grammar
-   [ ] Time Pressure
-   [ ] Spatial / Network Design
-   [ ] Other:

  특수 시스템   문제 정의   설계 건전성   주요 위험        점수
  ------------- ----------- ------------- ----------- ---------
                                                      
                                                      
  **Total**                                             **/15**

### Specialized Design Verdict

-   가장 잘 해결된 부분:
-   아직 검증되지 않은 부분:
-   Prototype에서 반드시 검증할 시스템:

------------------------------------------------------------------------

# 5. Solo / Micro Production Feasibility --- 20 Points

> **Reference Priority:** 3차 Solo/Micro Indie Reference 2\~3개를
> 호출한다.
>
> 핵심 질문: **"비슷한 소규모 개발 사례와 비교했을 때 현재 Scope가
> 합리적인가?"**

  항목                          점수 위험
  ------------------------ --------- -------------
  Programming Scope               /3 Low / M / H
  Content Production              /3 Low / M / H
  Art / Animation                 /3 Low / M / H
  UI / UX                         /2 Low / M / H
  QA / State Complexity           /3 Low / M / H
  System Dependency               /2 Low / M / H
  Outsourcing Dependency          /2 Low / M / H
  Schedule Robustness             /2 Low / M / H
  **Total**                  **/20** 

## 5.1 Production Profile

-   예상 핵심 개발 인원:
-   예상 개발기간:
-   프로토타입 기간:
-   전용 화면 수:
-   캐릭터/적/아이템/사건 등 주요 콘텐츠 수:
-   고유 애니메이션 수:
-   반복 제작 가능한 데이터 콘텐츠:
-   외주 필요 영역:
-   가장 비싼 제작 영역:
-   가장 위험한 QA 영역:

## 5.2 Scope Creep Check

다음 질문에 `YES / NO`로 답한다.

-   Core Loop 검증 전에 메타 시스템이 과도하게 많은가?
-   전용 UI가 공통 UI보다 많은가?
-   콘텐츠 수 증가가 재미 증가의 주된 수단인가?
-   캐릭터/지역/사건을 절반으로 줄여도 게임 정체성이 유지되는가?
-   Prototype 성공 후에만 추가해도 되는 Feature가 본 Scope에 포함되어
    있는가?
-   외주 실패 시 프로젝트 진행이 중단되는 영역이 있는가?

### Scope Verdict

`SAFE / MANAGEABLE / HIGH RISK / UNSUSTAINABLE`

## 5.3 Required Cuts

  현재 요소     현재 Scope   권장 Scope 이유   Core 훼손 여부
  ----------- ------------ ------------ ------ ----------------
                                               
                                               

------------------------------------------------------------------------

# 6. Market & Commercial Fit --- 20 Points

> **Reference Priority:** 4차 Commercial Reference에서 가까운 성공 사례
> 1\~2개 + 실패/저성과 Control 1개를 함께 호출한다.

  항목                                  점수 판단
  -------------------------------- --------- ------
  Store Hook Legibility                   /4 
  Genre Demand / Audience                 /3 
  Competitive Differentiation             /3 
  Visual Marketability                    /2 
  Price-to-Content Fit                    /2 
  Creator / Streaming Potential           /2 
  Wishlist Acquisition Potential          /2 
  Long-tail / Update Potential            /2 
  **Total**                          **/20** 

## 6.1 Commercial Funnel

### Awareness

-   Steam Festival 적합성:
-   Demo 활용 가능성:
-   Creator/Streamer 노출 가능성:
-   커뮤니티 생성 가능성:
-   Capsule에서 전달되는 핵심 이미지:

### Conversion

-   Wishlist → Purchase를 방해할 요소:
-   가격 저항:
-   Trailer에서 보여줄 핵심 장면:
-   Screenshot만으로 이해 가능한가:

### Satisfaction

-   Refund Risk:
-   기대와 실제 플레이의 불일치 위험:
-   리뷰에서 반복적으로 지적될 가능성이 높은 문제:

### Long Tail

-   업데이트 친화성:
-   할인 친화성:
-   Localization 가치:
-   DLC/확장 필요 여부:
-   출시 이후 콘텐츠 유지 비용:

------------------------------------------------------------------------

# 7. Target Sales Analysis

> **금지:** "이 게임은 30,000장 팔릴 것이다"처럼 판매량을 예언하지
> 않는다.
>
> **판단 대상:** "해당 판매 구간을 목표로 현재 제작비·기간을 투입하는
> 것이 합리적인가?"

  판매 구간         판정             근거
  ----------------- ---------------- ------
  **10K Floor**     Low / M / High   
  **30K Target**    Low / M / High   
  **50K Target**    Low / M / High   
  **100K Upside**   Low / M / High   

### Commercial Efficiency

-   예상 제작 투입:
-   예상 외주/마케팅 부담:
-   10K 수준에서도 감당 가능한가:
-   30K에서 충분한 성공인가:
-   50K를 위해 Scope를 늘릴 필요가 있는가:
-   100K를 기본 전제로 하고 있는 Feature가 있는가:
-   목표 미달 시 Opportunity Cost:
-   **Scope-to-Sales Efficiency:** Low / Medium / High / Exceptional

### Marketing Dependency

`LOW / MEDIUM / HIGH`

설명:

------------------------------------------------------------------------

# 8. Originality & Market Position --- 10 Points

  항목                               점수
  ----------------------------- ---------
  Concept Originality                  /2
  Mechanical Identity                  /2
  Visual Identity                      /2
  Familiarity / Accessibility          /2
  Explainability                       /2
  **Total**                       **/10**

### Positioning Matrix

-   익숙한 요소:
-   새로운 요소:
-   가장 가까운 경쟁작:
-   경쟁작과의 핵심 차이:
-   설명 비용이 높은 요소:
-   플레이 전에는 이해하기 어려운 강점:

### Originality Verdict

`GENERIC / FAMILIAR WITH HOOK / DISTINCTIVE / HIGHLY ORIGINAL BUT HARD TO SELL`

------------------------------------------------------------------------

# 9. Player Experience --- 10 Points

  구간               예상 경험   위험
  ------------------ ----------- ------
  First 10 Minutes               
  First Hour                     
  Mid-game                       
  Late-game                      

### UX / Experience Check

-   Cognitive Load:
-   Repetition Risk:
-   Downtime:
-   Failure Frustration:
-   Feedback Clarity:
-   Reward Frequency:
-   Learning Curve:
-   Player Mastery Curve:

**Player Experience Score:** /10

------------------------------------------------------------------------

# 10. Red Team Review

> **가정:** 이 프로젝트는 출시 후 기대에 미치지 못했다.\
> 이제 가장 가능성이 높은 실패 원인을 역으로 찾는다.

  --------------------------------------------------------------------------
            Rank 실패 원인   발생 가능성 피해 규모   Prototype   지금 제거
                                                     검증 가능?  가능?
  -------------- ----------- ----------- ----------- ----------- -----------
               1             H/M/L       H/M/L       Y/N         Y/N

               2             H/M/L       H/M/L       Y/N         Y/N

               3             H/M/L       H/M/L       Y/N         Y/N

               4             H/M/L       H/M/L       Y/N         Y/N

               5             H/M/L       H/M/L       Y/N         Y/N
  --------------------------------------------------------------------------

## Pre-Mortem Summary

-   가장 위험한 실패 경로:
-   가장 저렴하게 지금 제거할 수 있는 위험:
-   Prototype에서도 확인하기 어려운 위험:
-   출시 직전까지 남을 Commercial Risk:

------------------------------------------------------------------------

# 11. Prototype Validation Plan

> Prototype은 완성판의 축소판이 아니라 **가장 위험한 가설을 가장 싸게
> 검증하는 도구**다.

## 11.1 Must-Prove Hypotheses

    우선순위 가설   검증 방법   성공 기준   실패 시 조치
  ---------- ------ ----------- ----------- --------------
          P0                                
          P0                                
          P1                                

## 11.2 Prototype Scope

-   포함:
-   제외:
-   임시 Asset 허용 범위:
-   테스트용 데이터 수:
-   필요한 플레이 시간:
-   예상 제작 기간:
-   최대 허용 기간:
-   Stop Condition:

## 11.3 Prototype Exit Decision

`PROCEED / ITERATE / PIVOT / KILL`

------------------------------------------------------------------------

# 12. Reference Audit

최종 보고서에서 실제 사용한 Reference만 기록한다.

  Layer             Reference   사용 이유   적용성
  ----------------- ----------- ----------- --------
  1차 Core                                  
  1차 Core                                  
  2차 Specialized                           
  3차 Production                            
  3차 Production                            
  4차 Commercial                            
  4차 Control                               

### Reference Count Rule

-   권장 총량: **6\~10개**
-   1차: 2\~3
-   2차: 0\~3
-   3차: 2\~3
-   4차: 2\~3
-   관련성이 낮으면 숫자를 채우기 위해 호출하지 않는다.

------------------------------------------------------------------------

# 13. Final Decision Summary

## Scorecard

  평가축                          점수
  ------------------------- ----------
  Design Quality                   /25
  Specialized Design               /15
  Solo/Micro Feasibility           /20
  Market & Commercial Fit          /20
  Originality                      /10
  Player Experience                /10
  **TOTAL**                   **/100**

> **주의:** 총점은 보조 지표다. P0 위험이나 Scope 불가능성이 있으면 높은
> 총점에도 `NO-GO`가 가능하다.

## Sales Compatibility

-   **10K Floor:**
-   **30K Target:**
-   **50K Target:**
-   **100K Upside:**

## Final Summary

-   **Primary Strength:**
-   **Critical Risk:**
-   **Required Cuts:**
-   **Prototype Must Prove:**
-   **Recommended Prototype Duration:**
-   **Marketing Dependency:**
-   **Scope-to-Sales Efficiency:**

# FINAL VERDICT

**`GO / GO WITH CUTS / REVALIDATE / NO-GO`**

### Decision Rationale

### Conditions for GO

1.  
2.  
3.  

### Immediate Next Action

------------------------------------------------------------------------

# 14. Reviewer Guardrails

1.  재미있어 보인다는 이유로 GO를 주지 않는다.
2.  Reference의 Feature 수·콘텐츠 수를 직접 목표치로 복사하지 않는다.
3.  대형 성공작의 결과를 일반적인 기대값으로 사용하지 않는다.
4.  100K+ 판매는 기본 사업계획이 아니라 Upside다.
5.  판매량 추정치를 사실처럼 표현하지 않는다.
6.  1인 개발자의 노동을 무료 비용으로 취급하지 않는다.
7.  개발기간에는 Opportunity Cost를 포함해 판단한다.
8.  그래픽/콘텐츠를 AI로 만들 수 있다는 이유만으로 Scope Risk를 낮추지
    않는다.
9.  Prototype에서 검증할 수 없는 위험은 별도로 남긴다.
10. 높은 점수보다 **프로젝트를 죽일 수 있는 단일 P0 위험**을 우선한다.
11. 기획자의 의도를 존중하되, 실현 가능성과 시장성이 충돌하면 이를
    명확히 지적한다.
12. 최종 목적은 기획을 더 크게 만드는 것이 아니라 **완성·출시 가능한
    가장 강한 형태를 찾는 것**이다.

# END
