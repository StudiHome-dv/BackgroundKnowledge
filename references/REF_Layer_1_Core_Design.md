# Studio Game Design Reviewer — 1차 — Core Design Reference
> 프로젝트 소스 업로드용 통합 Reference 문서
> 각 Case Study의 원문 구조를 유지하며 `REF-XX` 경계로 분리했다.
---


---

# REF-01 — Papers Please

<!-- SOURCE_FILE: 01_Papers_Please.md -->

# Game Design Case Study v1.0 — Papers, Please

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** Lucas Pope / 3909 LLC
- **Release:** 2013
- **Genre:** Puzzle / Simulation / Narrative bureaucracy
- **Development Scale:** Solo-led indie
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
서류 판정이라는 반복 업무를 시간 압박·생계·정치·도덕적 예외와 겹쳐, 단순한 검사 행위 자체를 서사적 긴장으로 바꾼 게임.

### Why This Game Matters
UI 중심 판정 게임, 제한 정보 기반 선택, 작은 제작 범위에서 높은 의사결정 밀도를 만드는 방법을 검토하기 좋은 대표 사례다.

### Primary Design Lessons
- 단순한 핵심 업무도 규칙 변화와 맥락 누적으로 깊어질 수 있다.
- 같은 승인/거절 입력에 경제·도덕·정치 결과를 겹쳐 시스템과 서사를 통합한다.
- 콘텐츠 다양성을 거대한 맵보다 규칙 조합과 상황 변형으로 만들 수 있다.
- 실패 원인은 빠르게 알려주되 장기 결과는 지연해 긴장을 유지할 수 있다.

### Primary Warning
문서 검사라는 외형만 가져오면 반복 노동만 남는다. 핵심은 규칙 변화·시간·생계·인간적 예외가 같은 판정에 충돌한다는 점이다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 국경 심사관으로서 규칙을 적용해야 하지만, 가족의 생존과 입국자의 사정 사이에서 매일 판단한다. '정확한 관료'와 '인간적 개인'의 충돌이 Player Fantasy다.

### Target Player
정보 비교와 규칙 숙련을 좋아하고, 불편한 도덕적 선택과 반복 업무의 긴장을 받아들일 수 있는 플레이어.

### Design Pillars
- Rule Mastery
- Time Pressure
- Moral Tension
- Economy-linked Consequence

### USP
업무용 UI 자체가 게임플레이이며, 동일한 판정 행위가 퍼즐·경제·서사를 동시에 진행한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 문서 확인
- 규칙 대조
- 승인/거절
- 시간 배분
- 가계비 관리
- 예외 판단

### Core Loop
`입국자 등장 → 문서/진술 확인 → 규칙 대조 → 승인/거절 → 오류/보상/서사 결과 → 일일 생계 정산 → 새 규칙`

### Short-Term Loop
한 명의 입국자를 제한 시간 안에 검토하고 판정한다.

### Session Loop
하루 동안 가능한 많은 입국자를 정확히 처리하고 종료 후 가족 생계비를 배분한다.

### Long-Term / Meta Loop
날짜가 진행될수록 규칙과 정치 상황이 복잡해지고, 가족 상태와 조직 선택이 엔딩으로 이어진다.

### Loop Strength
기본 입력은 끝까지 유지되지만 매일 새 규칙과 예외가 추가되어 같은 업무의 의미가 변한다. 단, 핵심 검사 행위를 싫어하는 플레이어에게는 변주가 충분하지 않을 수 있다.

## 4. Decision Design
### Primary Decisions
- 정확성을 위해 시간을 더 쓸지 처리량을 우선할지
- 규칙상 거절 대상에게 예외를 허용할지
- 벌금 위험과 인간적 선택 중 무엇을 택할지

### Decision Depth / Meaningful Choice
선택지는 단순하지만 한 판정이 돈·시간·가족·서사에 동시에 영향을 준다. 가치가 하나의 수치로 환원되지 않기 때문에 Meaningful Choice가 형성된다.

### Dominant Strategy Risk
완벽한 규칙 준수만으로는 생계나 특정 서사 목표가 항상 최적이 아니다. 반대로 무작정 선의만 택하면 경제적으로 무너질 수 있다.

### Information & Uncertainty
현재 규칙은 공개되지만 문서 위조와 개인 사정, 장기 정치 결과는 일부 숨겨진다. 플레이어는 무엇을 검사해야 하는지 학습하고, 예외의 위험을 추론한다.

## 5. Risk / Reward Structure
### Primary Risks
- 오판 벌금
- 처리량 부족
- 가족 질병/굶주림
- 정치 세력과의 갈등

### Primary Rewards
- 정확한 처리 수입
- 가족 생존
- 서사 진행
- 규칙 숙련에서 오는 효율 증가

### Risk Visibility / Failure / Recovery
오류는 비교적 빠르게 통지되어 학습 가능하다. 그러나 인간적 선택의 장기 결과는 지연돼 즉시 기대값 계산을 어렵게 만든다. 경제 압박은 '좋은 선택'에도 실제 비용을 부여한다.

## 6. Progression Design
능력치 성장보다 플레이어 자신의 규칙 숙련이 핵심이다. 시스템 복잡도가 증가하면서 동일한 작업을 더 빠르고 정확하게 수행하는 것이 체감 성장이다.

## 7. Economy & Resource Design
처리 건수 기반 임금이 식비·난방·약값 등의 Sink와 연결된다. 경제는 별도 경영 미니게임이 아니라 도덕 선택의 비용 구조로 기능한다.

## 8. Difficulty & Failure Design
새 규칙, 문서 종류, 위조 패턴과 시간 압박이 누적된다. 난이도는 적 HP 증가가 아니라 정보 처리와 기억 부하의 증가다.

## 9. Onboarding & Learning Curve
초기에는 여권 확인 같은 단순 규칙으로 시작하고 새 문서와 규칙을 단계적으로 추가한다. Progressive Disclosure가 핵심이다.

## 10. Content & Variety
입국자 대사, 문서 조합, 규칙 변화, 사건 플래그를 재조합한다. 대규모 그래픽 제작보다 데이터·텍스트 변주로 밀도를 높인다.

## 11. Replayability
멀티엔딩과 다른 선택 경로가 재플레이를 만들지만 기본 업무가 동일해 장기 반복성은 로그라이트보다 낮다.

## 12. UX & Information Design
책상 배치와 문서 이동 자체가 핵심 조작이다. 정보 위치, 도장, 대조 도구가 곧 난이도이자 플레이 감각이다.

## 13. Player Motivation & Psychology
규칙 숙련, 가족 생존, 새로운 사건에 대한 호기심, 인간적 딜레마와 효율 개선이 동시에 작동한다.

## 14. Scope & Production Efficiency
한정 화면·제한 캐릭터 표현·데이터 조합으로 높은 경험 밀도를 만든다. 1인 개발 Scope 레퍼런스로 매우 강하다.

## 15. What Worked
- 업무와 서사를 동일 입력에 결합해 별도 서사 시스템 없이 선택의 의미를 증폭한다.
- 점진적 규칙 추가가 온보딩과 중후반 난이도 상승을 동시에 해결한다.

## 16. What Did Not Work / Limitations
- 핵심 업무 자체가 반복적이라 플레이어 취향에 따라 피로가 빠르게 누적될 수 있다.
- 규칙이 많아지면 초보자가 정확히 무엇을 놓쳤는지 추적하기 어려워질 수 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 작은 제작 범위로 어떻게 지속적인 긴장을 만들 것인가?  
**Solution:** 핵심 작업은 유지하되 규칙·시간·경제·서사 조건을 계속 충돌시킨다.  
**Trade-off:** 반복 업무 피로와 높은 인지 부하.

## 18. What This Game Teaches
- 단순 입력을 버리지 말고 맥락과 규칙을 확장해 깊이를 만든다.
- 경제 압박은 도덕적 선택에 실질적 비용을 부여할 수 있다.
- UI 조작 자체를 Core Gameplay로 만들 수 있다.

## 19. What NOT to Copy
- 문서 검사라는 소재 자체
- 처리량 압박만 단독으로 추가하는 것
- 불친절함을 하드코어 디자인으로 오해하는 것

## 20. Solo Indie Developer Lessons
### Worth Learning
작은 화면, 적은 애니메이션, 데이터 기반 사건을 사용해 시스템과 콘텐츠를 동시에 생산하는 방식.

### Expensive to Reproduce
고품질 대량 텍스트와 규칙 간 충돌 QA. 콘텐츠가 적어 보여도 판정 조합 테스트는 필요하다.

### Possible Simplification
프로토타입에서는 5~10일, 소수 문서, 하나의 경제 압박만으로 '판정이 반복하고 싶은가'를 검증할 수 있다.

## 21. Reference Comparison Tags
- **Design Tags:** Bureaucracy, Hidden Information, Time Pressure, Moral Choice, UI-as-Gameplay, Solo Scope
- **Best Review Use:** UI 중심 운영 게임 / 정보 판정 / 온보딩 / Solo Scope

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 단순한 핵심 업무도 규칙 변화와 맥락 누적으로 깊어질 수 있다.
- **Biggest Warning:** 문서 검사라는 외형만 가져오면 반복 노동만 남는다. 핵심은 규칙 변화·시간·생계·인간적 예외가 같은 판정에 충돌한다는 점이다.
- **Best Reference For:** UI 중심 운영 게임 / 정보 판정 / 온보딩 / Solo Scope
- **Core Design Principle:** 단순 입력을 버리지 말고 맥락과 규칙을 확장해 깊이를 만든다.

## 23. Final Assessment
### Design Strengths
- 시스템과 서사의 결합
- 낮은 제작비 대비 높은 판단 밀도
- 명확한 Progressive Disclosure

### Design Weaknesses
- 반복 업무 피로
- 중후반 인지 부하
- 장르 취향 의존성

### Most Transferable Lesson
단순 입력을 버리지 말고 맥락과 규칙을 확장해 깊이를 만든다.

### Most Dangerous Misinterpretation
문서 검사라는 외형만 가져오면 반복 노동만 남는다. 핵심은 규칙 변화·시간·생계·인간적 예외가 같은 판정에 충돌한다는 점이다.

## 24. Sources & Evidence
- [Official site](https://papersplea.se/) — Official
- [Road to the IGF](https://www.gamedeveloper.com/design/road-to-the-igf-lucas-pope-s-i-papers-please-i-) — Developer interview
- [Steam](https://store.steampowered.com/app/239030/Papers_Please/) — Official storefront

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-02 — FTL Faster Than Light

<!-- SOURCE_FILE: 02_FTL_Faster_Than_Light.md -->

# Game Design Case Study v1.0 — FTL: Faster Than Light

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** Subset Games
- **Release:** 2012
- **Genre:** Strategy / Roguelike / Real-time with pause
- **Development Scale:** Two-person core team with external contributors
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
우주선 함장 판타지를 전력·승무원·무기·연료·경로 관리와 영구 실패 구조로 압축한 시스템 중심 로그라이크.

### Why This Game Matters
소수 시스템의 상호작용으로 많은 상황을 만들고, RNG와 자원 압박을 준비·적응 판단으로 바꾸는 방법을 학습하기 좋다.

### Primary Design Lessons
- 기능 목록보다 플레이어가 느껴야 할 핵심 판타지를 먼저 고정할 수 있다.
- 서로 연결된 단순 시스템은 많은 독립 콘텐츠보다 큰 상황 다양성을 만든다.
- RNG는 준비·회피·복구 선택이 있을 때 의미가 있다.
- Pause 가능한 실시간 구조로 긴장과 전략 판단을 동시에 유지한다.

### Primary Warning
영구 실패와 무작위 이벤트만 복사하면 불공정성만 커진다. 준비·경로·복구 선택이 함께 있어야 한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 전투기 조종사가 아니라 우주선 '함장'이다. 선내 시스템과 승무원을 지휘하며 계속 발생하는 위기를 관리하는 것이 핵심 판타지다.

### Target Player
시스템 상호작용, 즉흥 문제 해결, 자원 관리와 반복 실패를 통한 학습을 좋아하는 플레이어.

### Design Pillars
- Captain Fantasy
- Systemic Interaction
- Scarcity
- Run Adaptation

### USP
우주선 내부를 하나의 상태 머신처럼 보여주고, 전투·수리·산소·화재·승무원 판단을 같은 공간에서 처리한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 경로 선택
- 전력 배분
- 승무원 배치
- 무기 타게팅
- 수리
- 구매/업그레이드
- 이벤트 선택

### Core Loop
`노드 선택 → 이벤트/전투 → 자원 소모·보상 → 수리/업그레이드 → 다음 경로 → 섹터 이동`

### Short-Term Loop
전투 중 전력·승무원·무기 타이밍을 정지 기능과 함께 조절한다.

### Session Loop
여러 노드를 탐색하며 연료·선체·승무원을 보존해 다음 섹터로 진행한다.

### Long-Term / Meta Loop
한 런은 최종 함대까지의 여정이며 실패 시 재시작한다. 다른 함선/배치 해금이 장기 목표다.

### Loop Strength
같은 전투 규칙이 적 함선, 선내 화재, 승무원 상태, 자원 부족과 결합돼 매번 다른 위기를 만든다.

## 4. Decision Design
### Primary Decisions
- 안전 경로와 고보상 위험 경로 중 선택
- 지금 수리할지 다음 상점까지 자원을 아낄지
- 어느 시스템과 승무원에 전력을 우선할지

### Decision Depth / Meaningful Choice
각 자원은 다른 자원과 연결되어 현재 최적 선택이 미래에 약점이 될 수 있다. 따라서 선택은 단일 기대값보다 준비 범위를 고려한다.

### Dominant Strategy Risk
특정 무기 조합이 강할 수 있지만 적 방어·시스템·자원 상태가 바뀌어 완전한 단일 해법이 되기 어렵다.

### Information & Uncertainty
현재 우주선 상태와 적 시스템은 많이 공개되지만 이후 노드와 이벤트 결과는 불확실하다. 장기 경로는 위험 분산 판단을 요구한다.

## 5. Risk / Reward Structure
### Primary Risks
- 선체 손상
- 승무원 사망
- 연료 고갈
- 불리한 이벤트
- 업그레이드 편향

### Primary Rewards
- 스크랩
- 새 무기/시스템
- 승무원
- 함선 강화
- 해금

### Risk Visibility / Failure / Recovery
RNG가 강하지만 플레이어는 자원 비축, 경로 선택, 시스템 다양화로 확률적 위험에 대비할 수 있다. 실패 비용이 크기 때문에 런 길이와 학습 피드백이 중요하다.

## 6. Progression Design
런 안에서 함선과 시스템이 수직 성장하며, 함선 해금은 수평적 장기 목표다. 핵심 재미는 한 런에서 주어진 재료로 적응형 빌드를 만드는 것이다.

## 7. Economy & Resource Design
스크랩이 수리·업그레이드·장비의 공통 통화라 기회비용이 명확하다. 연료·미사일·드론 같은 별도 자원은 다른 종류의 부족을 만든다.

## 8. Difficulty & Failure Design
섹터가 진행될수록 적 조합과 대응 요구가 증가한다. 최종 보스는 한 가지 강점보다 전체 준비 수준을 시험한다.

## 9. Onboarding & Learning Curve
시스템 수는 많지만 우주선 단면도와 룸 단위 표현이 상태를 공간적으로 이해시키는 역할을 한다.

## 10. Content & Variety
텍스트 이벤트, 적 함선, 시스템 조합, 경로 생성이 재조합되어 높은 런 다양성을 만든다.

## 11. Replayability
절차 생성, 다른 함선, 빌드, 실패 학습으로 매우 높다.

## 12. UX & Information Design
우주선 단면도 하나가 승무원·산소·시스템·피해를 동시에 보여준다. 복잡한 상태를 공간 정보로 압축한다.

## 13. Player Motivation & Psychology
함장 판타지, 위기 극복, 즉흥 최적화, 새로운 함선과 조합 발견.

## 14. Scope & Production Efficiency
3D 우주 전투 대신 아이콘·룸·텍스트 이벤트로 핵심 판타지를 구현한다. 그래픽보다 시스템 조합에 비용을 집중한다.

## 15. What Worked
- 산소·문·화재·승무원·시스템이 상호작용해 적은 콘텐츠로 많은 위기를 만든다.
- 실시간 전투를 Pause 가능하게 해 손 속도보다 판단을 핵심으로 유지한다.

## 16. What Did Not Work / Limitations
- 강한 RNG 때문에 좋은 판단에도 실패했다고 느낄 수 있다.
- 초반에는 자원과 시스템 우선순위가 많아 진입 장벽이 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 우주선 함장 느낌을 큰 3D 제작비 없이 어떻게 만들 것인가?  
**Solution:** 우주선을 기능별 룸과 자원 네트워크로 추상화한다.  
**Trade-off:** 시각적 액션보다 시스템 해석 비중이 커진다.

## 18. What This Game Teaches
- 플레이어 판타지를 상위 목표로 두고 기능을 그 감정에 맞춰 선택한다.
- 연결된 소수 시스템은 독립 콘텐츠보다 큰 변주를 만든다.
- RNG는 준비와 대응 수단이 있을 때 리스크가 된다.

## 19. What NOT to Copy
- Permadeath 자체
- 랜덤 이벤트 비율
- 자원 종류를 이유 없이 늘리는 것

## 20. Solo Indie Developer Lessons
### Worth Learning
공간·전투를 추상화하고 시스템 상호작용에 집중하는 방식은 작은 팀에 매우 유효하다.

### Expensive to Reproduce
다수 시스템 조합 QA와 밸런스. 단순 UI여도 상태 조합 폭은 크다.

### Possible Simplification
프로토타입은 1개 함선, 4개 시스템, 5개 이벤트만으로도 위기 관리 재미를 검증할 수 있다.

## 21. Reference Comparison Tags
- **Design Tags:** Roguelike, Resource Management, Systemic Interaction, Crew, Risk/Reward
- **Best Review Use:** 시스템 상호작용 / RNG / 자원 압박 / 런 기반 경영

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 기능 목록보다 플레이어가 느껴야 할 핵심 판타지를 먼저 고정할 수 있다.
- **Biggest Warning:** 영구 실패와 무작위 이벤트만 복사하면 불공정성만 커진다. 준비·경로·복구 선택이 함께 있어야 한다.
- **Best Reference For:** 시스템 상호작용 / RNG / 자원 압박 / 런 기반 경영
- **Core Design Principle:** 플레이어 판타지를 상위 목표로 두고 기능을 그 감정에 맞춰 선택한다.

## 23. Final Assessment
### Design Strengths
- 높은 시스템적 변주
- 명확한 함장 판타지
- 높은 콘텐츠 재사용 효율

### Design Weaknesses
- RNG 좌절
- 높은 초기 정보량
- 장기 런 실패 비용

### Most Transferable Lesson
플레이어 판타지를 상위 목표로 두고 기능을 그 감정에 맞춰 선택한다.

### Most Dangerous Misinterpretation
영구 실패와 무작위 이벤트만 복사하면 불공정성만 커진다. 준비·경로·복구 선택이 함께 있어야 한다.

## 24. Sources & Evidence
- [GDC Designing Without a Pitch](https://gdcvault.com/play/1018034/Designing-Without-a-Pitch-FTL) — Developer postmortem
- [FTL Postmortem](https://gdcvault.com/play/1017064/FTL-Faster-Than-Light) — Developer postmortem

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-03 — Into the Breach

<!-- SOURCE_FILE: 03_Into_the_Breach.md -->

# Game Design Case Study v1.0 — Into the Breach

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** Subset Games
- **Release:** 2018
- **Genre:** Turn-based tactics / Roguelike
- **Development Scale:** Small indie team
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
적의 다음 행동을 먼저 공개하고, 피해를 예측하는 대신 위치와 공격 상태를 조작해 재난을 막는 퍼즐형 전술 게임.

### Why This Game Matters
완전 정보형 전략, 작은 맵의 Decision Density, 처치보다 상태 조작을 중심으로 전투 깊이를 만드는 방법의 대표 사례다.

### Primary Design Lessons
- 정보를 공개해도 전략 깊이는 줄지 않고 다른 종류의 계산 가능성을 만든다.
- 작은 맵과 적은 유닛은 선택 결과를 더 선명하게 한다.
- 적 처치보다 목표 보호를 중심에 두면 같은 전투 시스템의 판단 기준이 달라진다.
- 위치 조작은 하나의 공격을 여러 시스템과 연결해 콘텐츠 효율을 높인다.

### Primary Warning
적 의도 공개를 그대로 가져오면 모든 전투가 퍼즐화될 수 있다. 즉흥성이나 혼돈이 핵심인 게임과는 목적이 다르다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 '가장 많이 죽이는 지휘관'보다 예고된 재난을 최소 피해로 해결하는 위기 관리자다.

### Target Player
완전 정보 기반 계산, 짧은 퍼즐형 전술, 작은 상태 공간에서 최적 해법을 찾는 플레이어.

### Design Pillars
- Perfect Information
- Position Manipulation
- Small Board
- Consequential Choices

### USP
적 행동을 미리 보여준 뒤 플레이어가 적을 밀고 막고 충돌시켜 미래 결과 자체를 편집한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 이동
- 공격
- 밀기/당기기
- 공격 취소 유도
- 건물 보호
- 희생 선택

### Core Loop
`적 의도 공개 → 위협 분석 → 유닛 행동 계획 → 위치/공격 조작 → 결과 해결 → 새 위협`

### Short-Term Loop
한 턴에 예고된 공격을 최소 피해로 해소하는 행동 조합을 찾는다.

### Session Loop
섬의 여러 미션을 선택해 Grid와 분대를 보존하며 보스까지 진행한다.

### Long-Term / Meta Loop
파일럿·분대 해금과 다른 조합으로 새 런을 시작한다.

### Loop Strength
매 턴 상태가 작고 명확해 선택 결과를 계산할 수 있으면서, 위치 상호작용 때문에 해법 공간은 넓다.

## 4. Decision Design
### Primary Decisions
- 어떤 피해를 완전히 막고 어떤 피해를 허용할지
- 처치와 건물 보호 중 무엇을 우선할지
- 고보상 미션의 위험을 감수할지

### Decision Depth / Meaningful Choice
모든 적 의도가 공개되어 선택의 깊이가 확률 예측이 아니라 상태 변환 순서와 기회비용에서 발생한다.

### Dominant Strategy Risk
분대별 강한 패턴이 존재하지만 목표·맵·적 배치가 달라 동일 콤보만으로 모든 턴을 해결하기 어렵다.

### Information & Uncertainty
적 공격 위치와 순서가 대부분 공개된다. 숨은 정보 대신 플레이어가 현재 상태를 완전히 읽고 계산하는 능력이 핵심이다.

## 5. Risk / Reward Structure
### Primary Risks
- Grid 피해
- 파일럿 사망
- 보너스 목표 실패
- 위치 고착

### Primary Rewards
- Grid 보존
- Reputation
- 코어
- 파일럿 경험
- 분대 해금

### Risk Visibility / Failure / Recovery
실패 원인이 거의 항상 눈앞의 상태에서 추적 가능해 공정성이 높다. 대신 완벽히 보이는 정보 때문에 실수가 더 크게 느껴질 수 있다.

## 6. Progression Design
Mech 코어 업그레이드는 수직 성장, 다른 분대와 파일럿은 수평적 전술 규칙 변화를 제공한다.

## 7. Economy & Resource Design
미션 보상과 Grid 방어가 제한 자원으로 연결된다. 어떤 섬/미션을 선택하는가 자체가 위험/보상 판단이다.

## 8. Difficulty & Failure Design
수치 증가보다 적 종류·환경·보너스 목표의 조합이 문제 공간을 복잡하게 만든다.

## 9. Onboarding & Learning Curve
적 공격 타일과 방향을 직접 표시해 결과를 예측할 수 있게 한다. 정보 가독성이 곧 튜토리얼이다.

## 10. Content & Variety
작은 타일맵, 적 조합, 환경, 목표를 재조합해 높은 변주를 만든다.

## 11. Replayability
분대마다 상태 조작 규칙이 크게 달라 같은 적도 다른 퍼즐이 된다.

## 12. UX & Information Design
공격 경로, 의도, 타일 강조가 모든 의사결정을 지원한다. 표시 오류가 곧 게임성 손실이 된다.

## 13. Player Motivation & Psychology
완벽한 해결책 찾기, 위기 최소화, 새로운 분대 숙련, 높은 난이도 정복.

## 14. Scope & Production Efficiency
작은 맵과 3유닛 구조로 제작량을 통제하면서 시스템 조합에 깊이를 집중했다.

## 15. What Worked
- Enemy Intent 공개가 실패를 운보다 계획 오류로 읽히게 만든다.
- 밀기/막기/충돌 중심 공격은 적 하나를 여러 문제에 재사용하게 한다.

## 16. What Did Not Work / Limitations
- 전투가 퍼즐화되어 전술 RPG 특유의 즉흥 서사나 혼돈은 약하다.
- 좋은 플레이가 이어질수록 작은 실수가 심리적으로 크게 느껴질 수 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 작은 전장으로 높은 전술 깊이를 어떻게 만들 것인가?  
**Solution:** 정보는 숨기지 않고 상호작용 가능한 위치 관계를 촘촘하게 만든다.  
**Trade-off:** 전투 경험이 계산 퍼즐에 가까워진다.

## 18. What This Game Teaches
- 정보 공개는 전략 깊이를 없애지 않고 다른 종류의 깊이를 만든다.
- 작은 문제 공간은 결과 가독성과 Decision Density를 높인다.
- 피해 수치보다 상태 변경이 콘텐츠 상호작용을 늘릴 수 있다.

## 19. What NOT to Copy
- 3유닛 구조 자체
- 완전 의도 공개를 모든 장르에 적용
- 최적해 탐색을 액션 게임에 강제

## 20. Solo Indie Developer Lessons
### Worth Learning
적은 유닛·작은 맵·명확한 상태 표현은 전술 프로토타입의 제작 Scope를 크게 줄일 수 있다.

### Expensive to Reproduce
전술 상호작용의 예외 처리와 QA. 콘텐츠가 작아도 상태 조합 테스트는 까다롭다.

### Possible Simplification
1개 분대, 3개 적 타입, 3개 맵 목표만으로도 Perfect Information 전술 가설을 검증할 수 있다.

## 21. Reference Comparison Tags
- **Design Tags:** Perfect Information, Turn-Based Tactics, Decision Density, Grid, Systemic Interaction
- **Best Review Use:** 공개 정보 / 전술 퍼즐 / 작은 맵 / UX 가독성

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 정보를 공개해도 전략 깊이는 줄지 않고 다른 종류의 계산 가능성을 만든다.
- **Biggest Warning:** 적 의도 공개를 그대로 가져오면 모든 전투가 퍼즐화될 수 있다. 즉흥성이나 혼돈이 핵심인 게임과는 목적이 다르다.
- **Best Reference For:** 공개 정보 / 전술 퍼즐 / 작은 맵 / UX 가독성
- **Core Design Principle:** 정보 공개는 전략 깊이를 없애지 않고 다른 종류의 깊이를 만든다.

## 23. Final Assessment
### Design Strengths
- 매우 높은 결과 가독성
- 작은 상태 공간의 깊이
- 높은 Scope 효율

### Design Weaknesses
- 퍼즐화된 감각
- 실수 스트레스
- 장르 취향 제한

### Most Transferable Lesson
정보 공개는 전략 깊이를 없애지 않고 다른 종류의 깊이를 만든다.

### Most Dangerous Misinterpretation
적 의도 공개를 그대로 가져오면 모든 전투가 퍼즐화될 수 있다. 즉흥성이나 혼돈이 핵심인 게임과는 목적이 다르다.

## 24. Sources & Evidence
- [GDC Design Postmortem](https://www.gdcvault.com/play/1025772/-Into-the-Breach-Design) — Developer postmortem

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-04 — Slay the Spire

<!-- SOURCE_FILE: 04_Slay_the_Spire.md -->

# Game Design Case Study v1.0 — Slay the Spire

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** Mega Crit Games
- **Release:** 2019
- **Genre:** Roguelike deckbuilder
- **Development Scale:** Small indie team
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
전투마다 카드를 드래프트하고 경로·유물·체력을 관리하며, 현재 강함보다 앞으로의 시너지와 위험을 판단하게 만드는 런 기반 덱빌딩 게임.

### Why This Game Matters
Meaningful Choice, 빌드 다양성, 데이터 기반 밸런스, Early Access 반복 검증을 연구하는 기준점이다.

### Primary Design Lessons
- 선택의 가치는 현재 덱과 상황에 따라 달라져야 한다.
- 조건부로 과감하게 강한 시너지를 허용하면 발견의 재미가 생긴다.
- 선택률과 승률을 함께 봐야 인지 가치와 실제 가치를 구분할 수 있다.
- 많은 아이디어를 만든 뒤 강한 설계만 남기는 편집 과정이 중요하다.

### Primary Warning
카드 수와 RNG를 늘린다고 깊이가 생기지 않는다. 적·경로·제거·유물 등 카드 선택 가치를 변화시키는 환경이 같이 필요하다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 완성된 덱을 가져오는 것이 아니라 런 중 주어진 재료로 덱을 '발견하고 구성'한다.

### Target Player
빌드 발견, 장기 기대값 판단, 반복 실패를 통한 숙련, 카드 시너지를 좋아하는 플레이어.

### Design Pillars
- Draft Adaptation
- Synergy
- Risky Routing
- Readable Enemy Intent

### USP
덱빌딩을 런 도중의 즉흥 드래프트와 결합해 매 카드 선택이 미래 전투 확률을 바꾼다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 카드 선택
- 카드 플레이
- 경로 선택
- 상점 구매
- 카드 제거/강화
- 유물 조합

### Core Loop
`전투 → 카드/보상 선택 → 경로 결정 → 이벤트/상점/엘리트 → 덱 수정 → 더 어려운 전투`

### Short-Term Loop
에너지와 손패 안에서 적 의도에 맞는 카드 순서를 결정한다.

### Session Loop
Act 경로를 선택하면서 덱과 유물을 구축해 보스에 도달한다.

### Long-Term / Meta Loop
Ascension, 캐릭터 해금과 숙련이 장기 목표다. 핵심 재미는 매 런의 다른 빌드다.

### Loop Strength
전투·카드 드래프트·경로가 서로 영향을 줘 '좋은 카드'의 가치가 고정되지 않는다.

## 4. Decision Design
### Primary Decisions
- 지금 강한 카드와 장기 시너지 카드 중 선택
- Elite 보상을 위해 위험을 감수할지
- 카드를 추가할지 오히려 건너뛸지

### Decision Depth / Meaningful Choice
같은 카드라도 덱 구성·유물·적·경로에 따라 가치가 바뀐다. 선택을 '추가/비추가'까지 포함시켜 기회비용을 만든다.

### Dominant Strategy Risk
일부 강한 아키타입은 있지만 매 런 카드 제공과 유물, 적이 달라 고정된 완성 덱을 그대로 재현하기 어렵다.

### Information & Uncertainty
적 의도는 공개돼 단기 전투는 계산 가능하지만 이후 카드/유물/경로 조합은 불확실하다. 단기 정보와 장기 불확실성이 공존한다.

## 5. Risk / Reward Structure
### Primary Risks
- HP 손실
- 덱 오염
- Elite/보스 실패
- 회복 기회 부족

### Primary Rewards
- 카드
- 유물
- 골드
- 포션
- 강화

### Risk Visibility / Failure / Recovery
HP는 런 전체를 연결하는 위험 예산이다. Elite 같은 선택적 고위험 노드가 플레이어 스스로 난이도를 조절하게 한다.

## 6. Progression Design
카드·유물 조합을 통한 런 내 성장과 Ascension/해금의 장기 숙련이 결합된다. 수평적 빌드 변화가 중요하다.

## 7. Economy & Resource Design
HP, Gold, Energy, 카드 슬롯 가치, 경로 기회가 서로 다른 자원으로 기능한다. '카드를 안 얻는 선택'이 중요한 Sink 억제 장치다.

## 8. Difficulty & Failure Design
적 패턴이 특정 덱 약점을 시험하고 Act가 올라갈수록 범용 대응력을 요구한다. Ascension은 규칙 변형으로 숙련자를 재시험한다.

## 9. Onboarding & Learning Curve
기본 카드는 단순하고 적 의도를 보여준다. 복잡성은 카드 조합과 적 패턴을 통해 점진적으로 드러난다.

## 10. Content & Variety
카드·유물·적·이벤트·맵 노드가 조합된다. 데이터 콘텐츠 하나가 많은 다른 요소와 상호작용한다.

## 11. Replayability
매우 높다. 캐릭터, 드래프트, 경로, 유물, Ascension이 매 런 다른 최적화를 요구한다.

## 12. UX & Information Design
적 의도와 카드 수치를 명확히 보여 단기 결과는 계산 가능하게 한다.

## 13. Player Motivation & Psychology
강력한 빌드 발견, 시스템 숙련, 어려운 Ascension 정복, 실패 원인 분석.

## 14. Scope & Production Efficiency
아트 제작비보다 카드/유물/적 조합과 밸런스 QA 비용이 크다. 데이터 중심 콘텐츠가 높은 재사용성을 만든다.

## 15. What Worked
- 상황 의존 카드 가치가 드래프트를 자동 선택이 아닌 지속 판단으로 만든다.
- 선택률·승률·피드백·직접 플레이를 함께 사용하는 밸런스 방식이 조건부 시너지를 해석한다.

## 16. What Did Not Work / Limitations
- 콘텐츠가 늘수록 카드·유물·적 상호작용 테스트 비용이 급증한다.
- 초보자는 겉보기 좋은 카드가 장기적으로 왜 나쁜지 이해하기 어렵다.

## 17. Design Problem → Solution Analysis
**Problem:** 수백 번 반복해도 카드 선택이 의미 있으려면?  
**Solution:** 카드 가치가 덱·적·경로·유물에 따라 변하도록 한다.  
**Trade-off:** 밸런스와 테스트 조합이 폭증한다.

## 18. What This Game Teaches
- 선택률과 승률을 함께 봐야 설계 가치를 이해할 수 있다.
- 조건부 강함을 허용하면 시스템 발견의 재미가 생긴다.
- 콘텐츠 수보다 선택 가치를 변화시키는 환경이 중요하다.

## 19. What NOT to Copy
- 대량 카드 수
- Ascension 단계 수
- RNG 드래프트만 가져오는 것

## 20. Solo Indie Developer Lessons
### Worth Learning
작은 팀도 데이터 중심 전투 콘텐츠로 큰 깊이를 만들 수 있지만, 자동 테스트와 플레이 로그 체계가 중요하다.

### Expensive to Reproduce
조합 폭증에 따른 밸런싱과 QA. 카드가 싸게 보여도 상호작용 비용은 높다.

### Possible Simplification
프로토타입은 1캐릭터, 30~40카드, 3~5적 패턴으로 드래프트 가치가 실제로 변하는지만 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Deckbuilding, Roguelike, Metrics, Balance, Meaningful Choice, Synergy
- **Best Review Use:** 밸런스 / AI Tester / Meaningful Choice / 빌드 다양성

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 선택의 가치는 현재 덱과 상황에 따라 달라져야 한다.
- **Biggest Warning:** 카드 수와 RNG를 늘린다고 깊이가 생기지 않는다. 적·경로·제거·유물 등 카드 선택 가치를 변화시키는 환경이 같이 필요하다.
- **Best Reference For:** 밸런스 / AI Tester / Meaningful Choice / 빌드 다양성
- **Core Design Principle:** 선택률과 승률을 함께 봐야 설계 가치를 이해할 수 있다.

## 23. Final Assessment
### Design Strengths
- 높은 선택 가치 변동성
- 데이터 기반 밸런스
- 매우 높은 재플레이

### Design Weaknesses
- 높은 QA 비용
- 초보자 함정
- 조합 복잡도

### Most Transferable Lesson
선택률과 승률을 함께 봐야 설계 가치를 이해할 수 있다.

### Most Dangerous Misinterpretation
카드 수와 RNG를 늘린다고 깊이가 생기지 않는다. 적·경로·제거·유물 등 카드 선택 가치를 변화시키는 환경이 같이 필요하다.

## 24. Sources & Evidence
- [GDC Metrics Driven Design](https://www.gdcvault.com/play/1025731/-Slay-the-Spire-Metrics) — Developer GDC
- [Road to the IGF](https://www.gamedeveloper.com/game-platforms/road-to-the-igf-mega-crit-games-i-slay-the-spire-i-) — Developer interview
- [Mega Crit AMA](https://www.reddit.com/r/IAmA/comments/aj6sq1/were_mega_crit_games_creators_of_slay_the_spire/) — Verified developer AMA

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-05 — Balatro

<!-- SOURCE_FILE: 05_Balatro.md -->

# Game Design Case Study v1.0 — Balatro

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** LocalThunk (core creation) with publishing/port/support collaborators
- **Release:** 2024
- **Genre:** Poker-inspired roguelike deckbuilder
- **Development Scale:** Solo-led core design/development
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
익숙한 포커 족보를 점수 엔진으로 쓰고 Joker·덱 조작·배수 규칙을 겹쳐, 매우 단순한 기본 규칙에서 폭발적 빌드 조합을 만드는 게임.

### Why This Game Matters
익숙한 규칙을 온보딩 비용 절감에 활용하고, 소수의 숫자·슬롯·Modifier로 높은 반복성과 시너지 탐색을 만든 솔로 개발 레퍼런스다.

### Primary Design Lessons
- 익숙한 규칙을 기반으로 새 시스템을 얹으면 온보딩 비용을 줄일 수 있다.
- 단순 점수식도 Modifier가 계산 규칙 자체를 바꾸면 깊어진다.
- 강한 시너지 발견의 재미는 완벽한 균형보다 중요할 수 있다.
- 데모와 반복 피드백은 핵심 재미를 빠르게 검증하는 수단이다.

### Primary Warning
Balatro를 '포커 + 랜덤 아이템'으로만 이해하면 실패한다. 핵심은 제한 슬롯 안에서 Modifier들이 서로 결합해 점수 엔진을 만드는 과정이다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 포커를 잘 치는 사람이 아니라, 매 런 규칙을 비틀어 비정상적으로 큰 점수를 만들어내는 엔진 설계자다.

### Target Player
시너지 발견, 숫자 성장, 덱 최적화, 짧은 런 반복을 좋아하는 플레이어.

### Design Pillars
- Familiar Rule Base
- Engine Building
- Slot Pressure
- Explosive Feedback

### USP
널리 알려진 포커 족보를 공통 언어로 사용하면서 Joker가 그 계산 규칙을 계속 변형한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 패 선택
- 족보 구성
- Joker 구매
- 카드/덱 조작
- 상점 리롤
- 경제 관리

### Core Loop
`Blind → 패 구성/점수 획득 → 보상 → 상점에서 Joker/팩/바우처 구매 → 덱 조정 → 더 높은 목표 점수`

### Short-Term Loop
제한된 Hand/Discard 안에서 현재 빌드가 가장 높은 점수를 내는 패를 만든다.

### Session Loop
Ante를 올라가며 점수 엔진을 구축하고 Boss Blind의 규칙 변형을 통과한다.

### Long-Term / Meta Loop
덱, Joker, Challenge, 난이도 해금이 장기 목표다.

### Loop Strength
핵심 입력은 카드 선택으로 매우 단순하지만 Joker 슬롯과 경제가 매 런 다른 계산 규칙을 만든다.

## 4. Decision Design
### Primary Decisions
- 즉시 점수와 장기 경제 중 선택
- 현재 족보 집중과 범용성 중 선택
- 제한 Joker 슬롯을 어떤 엔진으로 구성할지

### Decision Depth / Meaningful Choice
같은 Joker도 다른 Joker·덱·경제 상태에 따라 가치가 크게 달라진다. 슬롯 제한이 강한 Opportunity Cost를 만든다.

### Dominant Strategy Risk
일부 강한 조합은 존재하지만 런마다 제공되는 Joker와 Boss 규칙이 달라 완전한 고정 빌드 재현은 어렵다.

### Information & Uncertainty
현재 점수 계산은 비교적 명확하지만 향후 상점과 Boss는 불확실하다. 플레이어는 현재 엔진을 강화할지 미래 유연성을 남길지 선택한다.

## 5. Risk / Reward Structure
### Primary Risks
- 목표 점수 미달
- 경제 과소비
- Boss 규칙에 빌드가 막힘
- 과도한 특정 족보 의존

### Primary Rewards
- Joker
- 돈
- 덱 변형
- 점수 배수
- 해금

### Risk Visibility / Failure / Recovery
점수 목표라는 단순 실패 조건 덕분에 원인이 비교적 명확하다. 다만 원하는 Joker가 나오지 않는 RNG는 통제감 손실을 만들 수 있다.

## 6. Progression Design
칩·배수·Joker·카드 변형이 합성되어 수치가 크게 성장한다. 메타 해금은 새로운 시작 조건과 Challenge를 연다.

## 7. Economy & Resource Design
돈이 Joker·팩·리롤·바우처에 쓰인다. 저축/이자 가치가 즉시 점수 강화와 경쟁해 장기 기회비용을 만든다.

## 8. Difficulty & Failure Design
목표 점수 상승과 Boss Blind의 규칙 방해가 결합된다. 단순 수치 인플레이션만 쓰지 않고 빌드 약점을 찌른다.

## 9. Onboarding & Learning Curve
포커 족보라는 사전 지식을 활용하지만, 경험이 없어도 족보표와 즉각 점수 피드백으로 학습 가능하다.

## 10. Content & Variety
Joker와 카드 Modifier는 시각 제작비 대비 조합 가능성이 매우 크다. 소수 슬롯이 콘텐츠 간 경쟁을 만든다.

## 11. Replayability
Joker·덱·Boss·상점 RNG, 난이도, Challenge로 매우 높다.

## 12. UX & Information Design
점수 증가를 과장된 애니메이션·사운드로 보여 계산 행위를 감정적 보상으로 바꾼다.

## 13. Player Motivation & Psychology
숫자 폭발, 시너지 발견, 희귀 조합, 기록 갱신, 새로운 덱 숙련.

## 14. Scope & Production Efficiency
핵심은 카드와 데이터 기반이라 Scope 효율이 높지만, 조합 밸런스와 콘텐츠 큐레이션 비용은 상당하다.

## 15. What Worked
- 익숙한 포커 족보가 새 Joker 시스템을 위한 온보딩 예산을 확보한다.
- Joker 슬롯 제한이 얻기보다 버리기/교체 판단을 지속적으로 만든다.

## 16. What Did Not Work / Limitations
- 서사·공간 탐색·캐릭터 몰입은 거의 없고 숫자 엔진 구축에 집중한다.
- RNG 때문에 특정 런에서 원하는 빌드를 전혀 만들지 못할 수 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 아주 단순한 규칙으로 수백 번 반복할 조합 깊이를 만드는 법.  
**Solution:** 기본 점수식은 유지하고 Modifier가 규칙·배수·카드 상태를 계속 변형하게 한다.  
**Trade-off:** 조합 밸런스 폭증.

## 18. What This Game Teaches
- 익숙한 규칙은 새로운 시스템을 위한 인지 여유를 만든다.
- 슬롯 제한은 콘텐츠 추가 없이 강한 기회비용을 만든다.
- 수치 피드백도 연출을 통해 강한 감정 보상이 될 수 있다.

## 19. What NOT to Copy
- 포커 테마 자체
- 과도한 배수 인플레이션
- Joker 수량 경쟁

## 20. Solo Indie Developer Lessons
### Worth Learning
규칙·카드·Modifier 중심 콘텐츠로 아트 공수를 억제하고 성공 후 확장하는 방식.

### Expensive to Reproduce
수백 Modifier 상호작용과 밸런스 QA, 플랫폼 포팅과 장기 운영.

### Possible Simplification
프로토타입에서는 Joker 20개 안팎과 1개 덱으로 '엔진 구축이 반복하고 싶은가'만 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Solo Dev, Deckbuilding, Engine Building, Score Attack, Synergy, Scope Efficiency
- **Best Review Use:** 솔로 Scope / 시너지 / 온보딩 / 점수 피드백

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 익숙한 규칙을 기반으로 새 시스템을 얹으면 온보딩 비용을 줄일 수 있다.
- **Biggest Warning:** Balatro를 '포커 + 랜덤 아이템'으로만 이해하면 실패한다. 핵심은 제한 슬롯 안에서 Modifier들이 서로 결합해 점수 엔진을 만드는 과정이다.
- **Best Reference For:** 솔로 Scope / 시너지 / 온보딩 / 점수 피드백
- **Core Design Principle:** 익숙한 규칙은 새로운 시스템을 위한 인지 여유를 만든다.

## 23. Final Assessment
### Design Strengths
- 매우 높은 시스템 대비 콘텐츠 효율
- 강한 즉각 보상
- 익숙한 규칙의 재해석

### Design Weaknesses
- RNG 의존 인식
- 조합 QA 폭증
- 숫자 중심 취향 의존

### Most Transferable Lesson
익숙한 규칙은 새로운 시스템을 위한 인지 여유를 만든다.

### Most Dangerous Misinterpretation
Balatro를 '포커 + 랜덤 아이템'으로만 이해하면 실패한다. 핵심은 제한 슬롯 안에서 Modifier들이 서로 결합해 점수 엔진을 만드는 과정이다.

## 24. Sources & Evidence
- [LocalThunk Balatro Timeline](https://localthunk.com/blog/balatro-timeline-3aarh) — Developer primary
- [Verified AMA](https://www.reddit.com/r/Games/comments/1bdtmlg/ama_i_am_localthunk_developer_and_artist_for/) — Developer AMA
- [TouchArcade interview](https://toucharcade.com/2024/03/18/balatro-interview-mobile-port-localthunk-dlc-plans-updates-new-jokers-demo-feedback/) — Developer interview

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-06 — Darkest Dungeon

<!-- SOURCE_FILE: 06_Darkest_Dungeon.md -->

# Game Design Case Study v1.0 — Darkest Dungeon

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** Red Hook Studios
- **Release:** 2016
- **Genre:** Turn-based RPG / Roguelike management
- **Development Scale:** Small indie studio
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
전투 결과를 HP에서 끝내지 않고 스트레스·질병·기벽·사망·회복비용으로 장기 로스터 운영에 연결해 '영웅을 관리하는 고통'을 핵심 경험으로 만든 게임.

### Why This Game Matters
로스터 관리, 부상/회복, 영구 손실, 장기 캠페인 경제와 단기 전술의 연결을 연구하기 좋은 사례다.

### Primary Design Lessons
- 전투 결과를 장기 상태로 남기면 한 번의 전투가 캠페인 판단으로 확장된다.
- 캐릭터를 완전 소모품과 영구 주인공 사이에 두면 애착과 리스크가 함께 생긴다.
- 부정 상태도 단순 페널티가 아니라 운영 콘텐츠가 될 수 있다.
- 철수·치료·교체 같은 중간 선택이 영구 손실을 공정하게 만든다.

### Primary Warning
스트레스·부상·영구 사망을 많이 넣는다고 깊이가 생기지 않는다. 회복·대체 인력·철수·경제가 함께 있어야 한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 완벽한 영웅 파티를 키우는 것이 아니라 망가지는 사람들을 계속 교체·치료·투입하는 원정 관리자다.

### Target Player
고난도 자원 관리, 로스터 애착, 손실 관리와 장기 캠페인을 좋아하는 플레이어.

### Design Pillars
- Attrition
- Roster Management
- Stress
- Long-term Consequence

### USP
전투에서 받은 심리적·신체적 피해가 마을 운영과 다음 원정에 남아 전술과 경영을 결합한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 파티 편성
- 스킬 선택
- 진형 조정
- 탐험
- 자원 사용
- 치료/휴식
- 로스터 교체

### Core Loop
`영웅 모집/치료 → 파티 편성 → 던전 탐험/전투 → 전리품/스트레스/부상 → 마을 복귀 → 회복/업그레이드`

### Short-Term Loop
턴마다 위치·적 우선순위·스킬·스트레스 위험을 판단한다.

### Session Loop
한 번의 원정을 완주하거나 철수해 자원과 영웅 상태를 보존한다.

### Long-Term / Meta Loop
마을 시설과 로스터 성장으로 더 어려운 던전과 최종 목표에 도전한다.

### Loop Strength
전투의 작은 손실이 다음 원정까지 이어져 매 전투의 판단이 장기 비용을 가진다.

## 4. Decision Design
### Primary Decisions
- 부상당한 고레벨 영웅을 계속 쓸지 교체할지
- 더 진행할지 철수할지
- 치료 비용을 누구에게 쓸지

### Decision Depth / Meaningful Choice
현재 전투 승리와 장기 로스터 보존이 충돌한다. 동일한 스킬 선택도 캠페인 상태에 따라 가치가 달라진다.

### Dominant Strategy Risk
강한 파티 조합은 존재하지만 스트레스·상태·지역·적이 바뀌어 전원 고정 로스터 유지가 쉽지 않다.

### Information & Uncertainty
전투 정보는 대체로 공개되지만 명중·크리티컬 등 확률과 장기 상태 누적이 불확실성을 만든다.

## 5. Risk / Reward Structure
### Primary Risks
- 영웅 사망
- 스트레스 붕괴
- 질병/기벽
- 원정 실패
- 투자 손실

### Primary Rewards
- 골드/가보
- 영웅 경험
- 장비
- 마을 발전
- 보스 진행

### Risk Visibility / Failure / Recovery
영구 손실은 강하지만 철수·치료·신규 모집이 존재해 완전한 단절을 완화한다. 이 중간 회복 옵션이 핵심이다.

## 6. Progression Design
영웅 레벨과 마을 업그레이드의 수직 성장, 클래스 조합의 수평 성장이 결합된다.

## 7. Economy & Resource Design
골드와 가보가 다른 Sink를 가지며, 치료비가 원정 수익을 다시 소비시켜 성공 Snowball을 늦춘다.

## 8. Difficulty & Failure Design
던전 길이·적 조합·상태 누적·보스 기믹이 결합된다. 난이도는 한 전투보다 캠페인 누적 피로에서 나온다.

## 9. Onboarding & Learning Curve
시스템이 많아 진입 장벽은 높은 편이며 툴팁과 실패를 통해 학습한다. 대중적 온보딩의 모범보다는 하드코어 트레이드오프 사례다.

## 10. Content & Variety
클래스·적·기벽·질병·던전 속성 조합으로 변주를 만들지만 수작업 아트·적·던전 제작비도 높다.

## 11. Replayability
파티 조합과 랜덤 상태로 중상 수준이나 장기 캠페인 반복 피로가 존재한다.

## 12. UX & Information Design
HP·스트레스·진형·상태를 동시에 추적해야 해 인지 부하가 의도적으로 높다.

## 13. Player Motivation & Psychology
손실 회피, 로스터 성장, 위기 극복, 캐릭터 애착과 강한 분위기.

## 14. Scope & Production Efficiency
시스템 재사용성은 높지만 캐릭터/적/애니메이션/음성/던전 콘텐츠는 솔로 개발자가 그대로 재현하기 어렵다.

## 15. What Worked
- 전투와 장기 운영 상태를 연결해 전술 결정에 캠페인 비용을 부여한다.
- 철수 선택이 성공/실패 이분법 사이의 리스크 관리 공간을 만든다.

## 16. What Did Not Work / Limitations
- 중후반 반복 원정이 Grind로 느껴질 수 있다.
- 복합 페널티가 겹치면 플레이어 통제감이 급격히 줄 수 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 전투가 끝날 때 모든 상태가 초기화되면 장기 운영의 의미가 약하다.  
**Solution:** 스트레스·기벽·부상·사망을 다음 원정까지 남긴다.  
**Trade-off:** 누적 피로와 회복 Grind.

## 18. What This Game Teaches
- 단기 결과를 장기 상태로 연결하면 운영 판단이 깊어진다.
- 영구 손실에는 철수·치료·교체 같은 중간 회복 선택이 필요하다.
- 부정 상태도 관리 콘텐츠가 될 수 있다.

## 19. What NOT to Copy
- 높은 페널티 수치
- 영구 사망 자체
- 복잡한 상태 이상 수량

## 20. Solo Indie Developer Lessons
### Worth Learning
로스터 상태를 데이터화해 전투와 경영을 연결하는 원리는 재사용 가치가 높다.

### Expensive to Reproduce
대량 캐릭터/적 아트와 애니메이션, 장기 캠페인 밸런스, 상태 조합 QA.

### Possible Simplification
프로토타입은 4명 로스터, 2단계 부상, 스트레스 1종만으로 장기 상태가 선택을 바꾸는지 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Roster Management, Stress, Permadeath, Recovery, Campaign Economy
- **Best Review Use:** 부상/은퇴 / 로스터 / 장기 상태 / 캠페인 경제

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 전투 결과를 장기 상태로 남기면 한 번의 전투가 캠페인 판단으로 확장된다.
- **Biggest Warning:** 스트레스·부상·영구 사망을 많이 넣는다고 깊이가 생기지 않는다. 회복·대체 인력·철수·경제가 함께 있어야 한다.
- **Best Reference For:** 부상/은퇴 / 로스터 / 장기 상태 / 캠페인 경제
- **Core Design Principle:** 단기 결과를 장기 상태로 연결하면 운영 판단이 깊어진다.

## 23. Final Assessment
### Design Strengths
- 강한 전투-경영 연결
- 손실에 대한 감정적 의미
- 주제와 시스템의 높은 일치

### Design Weaknesses
- Grind
- 페널티 피로
- 높은 콘텐츠 제작비

### Most Transferable Lesson
단기 결과를 장기 상태로 연결하면 운영 판단이 깊어진다.

### Most Dangerous Misinterpretation
스트레스·부상·영구 사망을 많이 넣는다고 깊이가 생기지 않는다. 회복·대체 인력·철수·경제가 함께 있어야 한다.

## 24. Sources & Evidence
- [GDC Design Postmortem](https://www.gdcvault.com/play/1023435/Darkest-Dungeon-A-Design) — Developer postmortem
- [Kickstarter Post-Mortem](https://www.gamedeveloper.com/business/a-darkest-dungeon-kickstarter-post-mortem-part-2-) — Developer postmortem

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-07 — Against the Storm

<!-- SOURCE_FILE: 07_Against_the_Storm.md -->

# Game Design Case Study v1.0 — Against the Storm

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** Eremite Games
- **Release:** 2023
- **Genre:** Roguelite city builder
- **Development Scale:** Small team
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
도시 건설 장르의 장기 정착을 짧은 런으로 분할하고, 매번 다른 자원·주민·건물 선택으로 적응을 요구하는 로그라이트 경영 게임.

### Why This Game Matters
경영게임의 후반 정체를 세션 구조로 해결하고, 완성 빌드 재현을 막아 반복 플레이를 유지하는 방식을 검토하기 좋다.

### Primary Design Lessons
- 경영 게임의 가장 재미있는 초기 구축 구간을 반복 런으로 만들 수 있다.
- 모든 도구를 주지 않으면 계획보다 적응이 중심이 된다.
- 짧은 정착과 장기 메타를 분리하면 세션 부담과 장기 목표를 동시에 관리할 수 있다.
- 콘텐츠 변주를 새 맵 제작보다 규칙·건물·종족 조합으로 만들 수 있다.

### Primary Warning
로그라이트 메타만 붙인다고 경영 게임의 후반 정체가 해결되지는 않는다. 초기 구축 자체가 반복해도 재미있어야 한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 영구 도시를 완성하는 시장이 아니라, 매번 다른 조건에서 짧은 정착지를 성공시키는 적응형 관리자다.

### Target Player
도시 건설의 초기 최적화, 생산 체인, 로그라이트 반복과 높은 시스템 복잡성을 좋아하는 플레이어.

### Design Pillars
- Adaptive Building
- Short Settlements
- Scarcity
- Meta Progression

### USP
도시 건설의 '새 판 시작' 재미를 메인 세션으로 만들고 장기 세계 진행은 별도 메타로 옮긴다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 건설
- 주민 배치
- 생산 체인 설정
- 자원 선택
- 청사진 선택
- 위험 이벤트 대응

### Core Loop
`지역 선택 → 정착 시작 → 생산/주민 배치 → 목표 수행 → 폭풍 대응 → Reputation 달성 → 정착 종료 → 메타맵`

### Short-Term Loop
현재 자원 병목과 주민 요구를 해결한다.

### Session Loop
하나의 정착지를 압박 안에서 성공시키고 종료한다.

### Long-Term / Meta Loop
Smoldering City 업그레이드와 월드맵 주기, 난이도 상승이 장기 진행을 만든다.

### Loop Strength
모든 건물을 사용할 수 없고 바이옴·종족·자원이 달라 완성된 공략을 그대로 복제하기 어렵다.

## 4. Decision Design
### Primary Decisions
- 현재 부족을 해결할 건물 선택
- 장기 생산 체인과 즉시 목표 중 우선
- 위험 Glade를 언제 열지

### Decision Depth / Meaningful Choice
청사진과 자원이 제한돼 매 런 '없는 것'을 전제로 설계해야 한다. 이 불완전성이 경영 선택을 지속시킨다.

### Dominant Strategy Risk
특정 생산 체인이 강해도 필요한 자원·청사진·종족이 항상 나오지 않아 적응이 필요하다.

### Information & Uncertainty
현재 생산 상태는 공개되지만 이후 청사진·이벤트·지도 자원은 불확실하다.

## 5. Risk / Reward Structure
### Primary Risks
- Queen's Impatience
- Resolve 하락
- 자원 병목
- 위험 이벤트
- 폭풍

### Primary Rewards
- Reputation
- Blueprint
- Cornerstone
- 자원
- 메타 업그레이드

### Risk Visibility / Failure / Recovery
플레이어가 위험 Glade와 Order를 선택해 스스로 위험 수준을 조절한다. 시간 압박과 주민 상태가 실패 조건을 만든다.

## 6. Progression Design
정착 내부 임시 성장과 도시 메타 업그레이드가 분리돼 런 종료 후에도 장기 성취가 남는다.

## 7. Economy & Resource Design
다수 원자재·중간재·식량이 생산 체인으로 연결된다. 모든 체인을 확보할 수 없어 대체재 판단이 중요하다.

## 8. Difficulty & Failure Design
난이도 Modifier, 바이옴, 종족, 청사진 RNG와 폭풍 압박이 조합된다.

## 9. Onboarding & Learning Curve
시스템은 복잡하지만 난이도 단계와 메타 해금으로 일부 기능을 점진적으로 연다.

## 10. Content & Variety
바이옴·종족·건물·Cornerstone·Order·이벤트의 재조합이 핵심이다.

## 11. Replayability
경영 장르 중 매우 강하며, 같은 최적 도시를 반복 구축하기 어렵다.

## 12. UX & Information Design
자원과 생산 체인이 많아 정보량은 높다. 경고·필터·패널이 관리 부담을 완화한다.

## 13. Player Motivation & Psychology
새 정착 최적화, 위기 적응, 메타 성장, 고난도 숙련.

## 14. Scope & Production Efficiency
데이터 재조합 효율은 높지만 생산 체인과 변수 수가 많아 밸런스/QA 비용이 높다.

## 15. What Worked
- 짧은 정착 런이 전통 도시건설의 후반 정체를 회피한다.
- 불완전한 빌드 재료가 완성 공략 복제를 막고 적응을 요구한다.

## 16. What Did Not Work / Limitations
- 높은 시스템 부하로 초보자 진입 장벽이 높다.
- 메타 해금 때문에 초기 계정은 선택 도구가 답답하게 제한될 수 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 도시 건설은 후반에 최적화가 끝나면 정체된다.  
**Solution:** 가장 재미있는 구축 구간에서 세션을 종료하고 다음 조건의 새 정착으로 이동한다.  
**Trade-off:** 영구 도시 애착은 약해진다.

## 18. What This Game Teaches
- 장르의 가장 재미있는 시간 구간만 런으로 추출할 수 있다.
- 모든 도구를 주지 않으면 최적 빌드 재현보다 적응이 중요해진다.
- 단기 세션과 장기 메타를 분리해 목표를 중첩할 수 있다.

## 19. What NOT to Copy
- 로그라이트 메타 자체
- 자원 종류 증가
- 무작위 건물 선택만 추가하는 것

## 20. Solo Indie Developer Lessons
### Worth Learning
짧은 런 구조 아이디어는 유용하지만 실제 생산 체인 규모는 1인 개발에 그대로 적용하기 어렵다.

### Expensive to Reproduce
자원/건물/종족 조합 QA와 장기 밸런스, 방대한 UI.

### Possible Simplification
프로토타입은 자원 5종, 건물 8종, 20~30분 세션으로 '새 판 초기 구축이 반복 가능한가'를 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** City Builder, Roguelite, Adaptive Strategy, Production Chain, Session Design
- **Best Review Use:** 경영 세션 구조 / 반복성 / 적응형 빌드 / 메타

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 경영 게임의 가장 재미있는 초기 구축 구간을 반복 런으로 만들 수 있다.
- **Biggest Warning:** 로그라이트 메타만 붙인다고 경영 게임의 후반 정체가 해결되지는 않는다. 초기 구축 자체가 반복해도 재미있어야 한다.
- **Best Reference For:** 경영 세션 구조 / 반복성 / 적응형 빌드 / 메타
- **Core Design Principle:** 장르의 가장 재미있는 시간 구간만 런으로 추출할 수 있다.

## 23. Final Assessment
### Design Strengths
- 장르 후반 정체 해결
- 강한 재플레이
- 시스템적 콘텐츠 재사용

### Design Weaknesses
- 높은 인지 부하
- 밸런스 변수 폭증
- 영구 도시 애착 약화

### Most Transferable Lesson
장르의 가장 재미있는 시간 구간만 런으로 추출할 수 있다.

### Most Dangerous Misinterpretation
로그라이트 메타만 붙인다고 경영 게임의 후반 정체가 해결되지는 않는다. 초기 구축 자체가 반복해도 재미있어야 한다.

## 24. Sources & Evidence
- [GameDeveloper interview](https://www.gamedeveloper.com/business/how-against-the-storm-managed-to-mix-city-building-and-roguelite-play) — Developer interview
- [Eremite developer post](https://www.reddit.com/r/Games/comments/yha2es/against_the_storm_eremite_games_roguelite/) — Developer post

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-08 — Frostpunk

<!-- SOURCE_FILE: 08_Frostpunk.md -->

# Game Design Case Study v1.0 — Frostpunk

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** 11 bit studios
- **Release:** 2018
- **Genre:** Survival city builder / Management
- **Development Scale:** Mid-size indie studio
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
도시 생존 자원 관리와 법·윤리 선택을 연결해, 효율적인 경영 판단이 사회적·도덕적 비용으로 되돌아오게 만드는 압박형 경영 게임.

### Why This Game Matters
경영 시스템과 서사를 동일한 선택에 결합하고, 자원 압박을 감정적·도덕적 판단으로 전환하는 방법을 연구하기 좋다.

### Primary Design Lessons
- 경영 수치와 도덕 선택을 별도 미니게임으로 분리하지 않을 수 있다.
- 법과 정책은 단순 보너스보다 장기적 사회 방향 선택이 될 수 있다.
- 다가오는 재난을 명확히 예고하면 현재와 미래 자원 배분 갈등이 생긴다.
- 같은 기본 경영 시스템도 시나리오 압박을 바꿔 다른 이야기를 만들 수 있다.

### Primary Warning
잔혹한 선택지를 많이 넣는다고 Frostpunk식 서사가 되지 않는다. 자원 구조가 그 선택을 실제로 필요하게 해야 한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 도시를 효율적으로 키우는 시장이 아니라, 생존을 위해 어디까지 인간성을 양보할지를 결정하는 지도자다.

### Target Player
강한 압박형 경영, 생존 계획, 도덕적 딜레마와 시나리오 중심 진행을 선호하는 플레이어.

### Design Pillars
- Survival Pressure
- Moral Economy
- Heat
- Societal Consequence

### USP
가혹한 법 선택이 실제 생산·질서 문제를 해결하기 때문에 선악과 효율이 같은 시스템 안에서 충돌한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 건설
- 인력 배치
- 열 관리
- 법 제정
- 자원 배분
- 탐험
- 위기 대응

### Core Loop
`자원 생산 → 난방/식량/의료 유지 → 도시 확장 → 사회 수치 관리 → 법/정책 선택 → 더 큰 환경 위기`

### Short-Term Loop
시간대별 생산과 열·의료·식량 병목을 해결한다.

### Session Loop
시나리오의 연속된 위기를 넘겨 도시를 생존시킨다.

### Long-Term / Meta Loop
주로 시나리오 단위 완결이며 다른 시나리오와 난이도가 재플레이 목표다.

### Loop Strength
환경 위기와 시민 상태가 계속 새 병목을 만들어, 단순 도시 확장보다 생존 우선순위가 반복적으로 바뀐다.

## 4. Decision Design
### Primary Decisions
- 효율을 위해 가혹한 정책을 강제할지
- 현재 생존과 미래 대비 중 어디에 자원을 쓸지
- 탐험과 도시 노동력을 어떻게 나눌지

### Decision Depth / Meaningful Choice
도덕 선택이 실제 생산성과 질서에 영향을 주기 때문에 추상적인 선악이 아니라 전략적 비용을 가진다.

### Dominant Strategy Risk
반복 숙련 후 효율적 법/빌드가 알려지면 도덕 딜레마가 최적화 문제로 변할 위험이 있다.

### Information & Uncertainty
다가오는 추위와 현재 자원은 비교적 명확하지만 사건과 사회 반응의 일부는 불확실하다.

## 5. Risk / Reward Structure
### Primary Risks
- 자원 고갈
- 질병/사망
- 불만 폭증
- 희망 붕괴
- 추위

### Primary Rewards
- 도시 생존
- 새 기술
- 자원지
- 사회 안정
- 서사 성취

### Risk Visibility / Failure / Recovery
예고된 장기 재난이 준비 기회를 주고, 단기 사건이 계획을 흔든다. 실패가 단순 운보다 준비 부족으로 읽히도록 한다.

## 6. Progression Design
기술 트리와 인프라가 수직 성장하고, 법은 게임 규칙과 사회 방향을 바꾸는 구조적 성장이다.

## 7. Economy & Resource Design
석탄·목재·철·식량·인력·열이 상호의존한다. 한 자원 최적화가 다른 사회 비용을 유발한다.

## 8. Difficulty & Failure Design
기온 하락과 인구/질병/사건이 시간축을 따라 상승해 장기 계획을 시험한다.

## 9. Onboarding & Learning Curve
시스템 수는 많지만 '추위에서 살아남기'라는 명확한 목표가 무엇을 먼저 배워야 하는지 알려준다.

## 10. Content & Variety
기본 도시 시스템을 시나리오 목표·지도 조건·사회 사건으로 변주한다.

## 11. Replayability
중간. 다른 법과 시나리오/난이도는 있으나 완전 절차 생성형은 아니다.

## 12. UX & Information Design
열 지도와 자원 흐름이 핵심 상태를 시각화한다. 사회 수치와 생산 수치를 함께 추적한다.

## 13. Player Motivation & Psychology
생존, 도시 성장, 도덕적 자기검증, 다가오는 대재난을 넘기는 긴장.

## 14. Scope & Production Efficiency
아트·연출·시나리오 제작비가 높아 솔로 재현은 어렵지만, 동일 경영 시스템을 여러 시나리오에서 재사용하는 방식은 참고 가치가 높다.

## 15. What Worked
- 가혹한 법이 실제 생산/질서 문제를 해결해 도덕과 경제를 같은 선택으로 만든다.
- 예고된 장기 추위가 현재 효율보다 미래 준비를 고려하게 한다.

## 16. What Did Not Work / Limitations
- 숙련 후 법과 빌드가 정답화되면 첫 플레이의 도덕 긴장이 약해질 수 있다.
- 지속 압박 때문에 편안한 경영을 원하는 플레이어에게 피로가 크다.

## 17. Design Problem → Solution Analysis
**Problem:** 경영 게임의 자원 판단에 감정적 의미를 어떻게 부여할 것인가?  
**Solution:** 생존을 위해 필요한 효율 선택이 시민의 삶과 사회 규범을 직접 바꾸게 한다.  
**Trade-off:** 높은 스트레스와 반복 시 정답화.

## 18. What This Game Teaches
- 도덕 선택은 실제 시스템 비용과 연결될 때 강해진다.
- 예고된 장기 위기는 자원 계획의 목적을 만든다.
- 같은 시스템도 시나리오 압박을 바꾸면 다른 경험이 된다.

## 19. What NOT to Copy
- 가혹한 선택의 수
- 희망/불만 게이지
- 재난 타이머 자체

## 20. Solo Indie Developer Lessons
### Worth Learning
도덕 선택을 별도 스토리 분기가 아니라 기존 자원 시스템에 연결하는 원리는 작은 프로젝트에도 적용 가능하다.

### Expensive to Reproduce
고품질 도시 아트, 애니메이션, 시나리오, 복잡한 생산/인구 밸런스.

### Possible Simplification
프로토타입에서는 자원 3종, 사회 수치 1~2개, 장기 위기 1개로 '효율과 윤리가 실제로 충돌하는가'를 확인한다.

## 21. Reference Comparison Tags
- **Design Tags:** City Builder, Survival, Moral Choice, Resource Pressure, Scenario Design
- **Best Review Use:** 도덕 선택 / 경영 압박 / 시나리오 / 장기 위기

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 경영 수치와 도덕 선택을 별도 미니게임으로 분리하지 않을 수 있다.
- **Biggest Warning:** 잔혹한 선택지를 많이 넣는다고 Frostpunk식 서사가 되지 않는다. 자원 구조가 그 선택을 실제로 필요하게 해야 한다.
- **Best Reference For:** 도덕 선택 / 경영 압박 / 시나리오 / 장기 위기
- **Core Design Principle:** 도덕 선택은 실제 시스템 비용과 연결될 때 강해진다.

## 23. Final Assessment
### Design Strengths
- 테마-시스템 일치
- 강한 장기 압박
- 감정적 경영 판단

### Design Weaknesses
- 정답화 위험
- 높은 스트레스
- 높은 제작비

### Most Transferable Lesson
도덕 선택은 실제 시스템 비용과 연결될 때 강해진다.

### Most Dangerous Misinterpretation
잔혹한 선택지를 많이 넣는다고 Frostpunk식 서사가 되지 않는다. 자원 구조가 그 선택을 실제로 필요하게 해야 한다.

## 24. Sources & Evidence
- [Official Frostpunk page](https://11bitstudios.com/game/frostpunk/) — Official
- [GDC Why Make Games](https://gdcvault.com/play/1026288/Why-Make-Games-Lessons-from) — Developer GDC

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-09 — Reigns

<!-- SOURCE_FILE: 09_Reigns.md -->

# Game Design Case Study v1.0 — Reigns

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** Nerial
- **Release:** 2016
- **Genre:** Choice-based strategy / Narrative management
- **Development Scale:** Small indie
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
카드 한 장과 좌우 스와이프라는 극단적으로 단순한 입력으로 왕국의 여러 자원과 장기 사건 플래그를 관리하는 선택형 경영 게임.

### Why This Game Matters
입력 최소화, 이진 선택, 짧은 텍스트 콘텐츠 재사용, 숨은 상태와 장기 결과를 연구하기 좋은 사례다.

### Primary Design Lessons
- 입력 선택지 수가 적어도 결과 축이 여러 개면 판단은 충분히 복잡해질 수 있다.
- 한 카드의 선택이 즉시 수치와 장기 사건 모두에 영향을 주면 작은 콘텐츠의 밀도가 높아진다.
- 빠른 실패와 재시작은 긴 튜토리얼 없이 규칙을 학습시키는 구조가 될 수 있다.
- 모바일의 물리적 제스처를 게임의 정체성과 의사결정 속도에 맞출 수 있다.

### Primary Warning
이진 선택은 제작비를 줄이지만 결과가 예측 불가능하기만 하면 전략성이 아니라 찍기가 된다. 신호와 학습 가능성이 필요하다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 왕으로서 매 순간 두 선택 중 하나를 택하고, 교회·민중·군대·재정의 균형을 유지하며 오래 통치하려 한다.

### Target Player
짧은 세션, 텍스트 선택, 자원 균형과 블랙코미디를 선호하는 플레이어.

### Design Pillars
- Binary Choice
- Resource Balance
- Adaptive Narrative
- Failure-as-Content

### USP
좌우 스와이프 하나로 정치·경제·서사를 모두 처리한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 좌/우 선택
- 자원 균형
- 사건 기억
- 위험 회피

### Core Loop
`카드 제시 → 좌/우 선택 → 자원/플래그 변화 → 다음 카드 → 자원 붕괴 시 사망 → 다음 왕`

### Short-Term Loop
한 선택이 네 자원과 장기 상태에 미칠 영향을 예측한다.

### Session Loop
한 왕의 통치 기간 동안 자원 균형을 유지하고 이벤트를 해금한다.

### Long-Term / Meta Loop
왕이 죽어도 일부 목표와 사건 기억이 다음 통치로 이어져 장기 미스터리를 진행한다.

### Loop Strength
입력은 매우 단순하지만 자원 상태와 플래그가 바뀌면서 같은 선택의 가치가 달라진다.

## 4. Decision Design
### Primary Decisions
- 한 자원을 살리기 위해 다른 자원을 희생할지
- 모호한 결과를 현재 상태에서 감수할지
- 장기 플래그를 위해 위험을 감수할지

### Decision Depth / Meaningful Choice
선택지는 두 개지만 결과 축이 여러 개라 단순 찬반이 아니다. 다만 결과 예측 신호가 약하면 전략성이 떨어진다.

### Dominant Strategy Risk
한 자원만 최대화하면 오히려 사망할 수 있어 균형 자체가 목표다. 단일 최대화 전략을 구조적으로 차단한다.

### Information & Uncertainty
현재 자원은 보이지만 선택의 정확한 수치와 장기 플래그는 일부 숨겨진다.

## 5. Risk / Reward Structure
### Primary Risks
- 자원 극단화로 인한 사망
- 숨은 사건 결과
- 장기 목표 실패

### Primary Rewards
- 통치 연장
- 새 카드/사건
- 장기 목표 진행
- 서사 발견

### Risk Visibility / Failure / Recovery
실패는 매우 빠르고 유머러스하며 다음 왕으로 즉시 이어져 Restart Cost가 낮다. 반복 실패 자체가 콘텐츠 소비다.

## 6. Progression Design
능력치 성장보다 카드 풀, 사건 플래그, 플레이어 지식이 확장된다.

## 7. Economy & Resource Design
네 자원은 각각 높아도 낮아도 위험해 단순 축적이 아니라 균형을 요구한다.

## 8. Difficulty & Failure Design
새 카드와 복합 사건, 결과 모호성이 누적된다. 지식이 늘어날수록 생존력이 높아진다.

## 9. Onboarding & Learning Curve
스와이프 하나로 즉시 시작하며 첫 죽음들이 실질적 튜토리얼 역할을 한다.

## 10. Content & Variety
텍스트 카드, 초상화, 상태 플래그를 재조합해 낮은 그래픽 제작비로 많은 상황을 만든다.

## 11. Replayability
카드 풀·장기 플래그·죽음 변주로 중상 수준이며 짧은 세션이 반복 피로를 완화한다.

## 12. UX & Information Design
선택 미리보기와 자원 아이콘만으로 대부분 판단한다. 모바일 퍼스트 설계의 대표 사례다.

## 13. Player Motivation & Psychology
다음 사건 호기심, 통치 기록, 숨은 서사, 예상 밖의 죽음과 유머.

## 14. Scope & Production Efficiency
아트와 텍스트 카드 중심이라 구현 범위는 작지만 카드 수가 늘수록 상태 관리와 작문 비용이 증가한다.

## 15. What Worked
- Binary input과 Multi-axis consequence를 결합해 입력 단순성과 판단 복잡성을 분리한다.
- 죽음 자체를 유머와 새로운 정보로 사용해 실패를 콘텐츠로 만든다.

## 16. What Did Not Work / Limitations
- 결과가 너무 모호하면 학습보다 랜덤 찍기로 느껴질 수 있다.
- 장시간 플레이 시 카드 반복과 패턴 암기가 드러난다.

## 17. Design Problem → Solution Analysis
**Problem:** 모바일에서 극단적으로 단순한 입력으로 경영 선택을 어떻게 만들 것인가?  
**Solution:** 입력은 2개로 제한하고 결과 축을 여러 자원과 장기 플래그로 확장한다.  
**Trade-off:** 결과 신호가 약하면 전략성이 떨어진다.

## 18. What This Game Teaches
- 입력 단순화와 결과 복잡성은 동시에 가능하다.
- 실패를 짧고 재미있는 콘텐츠로 만들면 재시작 비용이 낮아진다.
- 카드 데이터는 상태 플래그와 결합할 때 깊어진다.

## 19. What NOT to Copy
- 스와이프 UI 자체
- 네 개 게이지
- 랜덤 텍스트 카드만 늘리는 것

## 20. Solo Indie Developer Lessons
### Worth Learning
단순 UI와 카드 데이터 구조는 1인 개발에 특히 적합하며, 프로토타입도 매우 작게 만들 수 있다.

### Expensive to Reproduce
대량 텍스트 작성과 사건 플래그 조합 QA.

### Possible Simplification
프로토타입은 자원 3개, 카드 30장 정도로 선택 결과가 실제로 학습 가능한지 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Binary Choice, Narrative Cards, Mobile UX, Resource Balance, Failure-as-Content
- **Best Review Use:** 모바일 UI / 이진 선택 / 카드 이벤트 / 자원 균형

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 입력 선택지 수가 적어도 결과 축이 여러 개면 판단은 충분히 복잡해질 수 있다.
- **Biggest Warning:** 이진 선택은 제작비를 줄이지만 결과가 예측 불가능하기만 하면 전략성이 아니라 찍기가 된다. 신호와 학습 가능성이 필요하다.
- **Best Reference For:** 모바일 UI / 이진 선택 / 카드 이벤트 / 자원 균형
- **Core Design Principle:** 입력 단순화와 결과 복잡성은 동시에 가능하다.

## 23. Final Assessment
### Design Strengths
- 극단적으로 낮은 입력 복잡도
- 높은 콘텐츠 대비 시스템 효율
- 실패의 낮은 재시작 비용

### Design Weaknesses
- 결과 불투명성
- 카드 반복
- 장기 전략 깊이 한계

### Most Transferable Lesson
입력 단순화와 결과 복잡성은 동시에 가능하다.

### Most Dangerous Misinterpretation
이진 선택은 제작비를 줄이지만 결과가 예측 불가능하기만 하면 전략성이 아니라 찍기가 된다. 신호와 학습 가능성이 필요하다.

## 24. Sources & Evidence
- [Game Design Deep Dive](https://www.gamedeveloper.com/design/game-design-deep-dive-creating-an-adaptive-narrative-in-i-reigns-i-) — Developer-authored analysis
- [Developer interview](https://www.appunwrapper.com/2016/08/17/interview-with-reigns-developer-francois-alliot/) — Developer interview

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-10 — 80 Days

<!-- SOURCE_FILE: 10_80_Days.md -->

# Game Design Case Study v1.0 — 80 Days

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** inkle
- **Release:** 2014
- **Genre:** Interactive fiction / Resource management / Travel strategy
- **Development Scale:** Small indie team with substantial authored narrative
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
세계 여행 경로 선택과 돈·시간·건강·수하물 관리를 대규모 분기 텍스트와 결합해, 매번 다른 여행 이야기를 생성하는 시스템 내러티브 게임.

### Why This Game Matters
텍스트 게임에서 시스템과 이야기를 분리하지 않는 방법, 경로 선택과 자원이 곧 서사 선택이 되는 구조를 연구하기 좋다.

### Primary Design Lessons
- 분기 텍스트는 단순 트리가 아니라 위치·시간·자원·이전 사건에 반응하는 시스템이 될 수 있다.
- 경로 선택 자체가 이야기 선택이 되면 게임플레이와 서사가 분리되지 않는다.
- 자원 압박은 플레이어마다 다른 우선순위와 다른 이야기를 만든다.
- 한 회차에 모든 콘텐츠를 볼 수 없게 하면 세계가 더 크게 느껴진다.

### Primary Warning
80 Days의 강점은 글의 양만이 아니다. 상태 반응형 내러티브 구조 없이 분기 수만 늘리면 제작비가 폭증한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 80일 안에 세계를 도는 여정 관리자로서 시간·돈·건강·정보 사이에서 경로를 선택하며 자신만의 여행담을 만든다.

### Target Player
텍스트 내러티브, 탐험, 자원 관리와 반복 경로 발견을 좋아하는 플레이어.

### Design Pillars
- Route-as-Story
- Adaptive Narrative
- Scarcity
- World Discovery

### USP
지도 경로 선택이 곧 어떤 이야기와 자원 문제를 만날지 결정한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 경로 선택
- 여행 예약
- 대화 선택
- 물품 구매/판매
- 돈 관리
- 시간 관리

### Core Loop
`도시 도착 → 정보/이벤트 탐색 → 다음 경로 선택 → 비용/시간 지불 → 여행 사건 → 새 도시/경로`

### Short-Term Loop
한 도시나 여정에서 텍스트 선택과 자원 판단을 한다.

### Session Loop
여러 도시를 잇는 경로를 계획하며 제한 시간 내 세계 일주를 진행한다.

### Long-Term / Meta Loop
한 회차 완결 후 다른 경로·도시·사건을 발견하기 위해 재플레이한다.

### Loop Strength
경로, 자원, 사건이 서로 영향을 주어 동일한 텍스트 선택도 여행 상태에 따라 의미가 달라진다.

## 4. Decision Design
### Primary Decisions
- 빠르지만 비싼 경로와 느리지만 싼 경로 중 선택
- 새 이야기를 위해 우회할지 목표 시간을 우선할지
- 물품을 버프/판매/서사 목적으로 유지할지

### Decision Depth / Meaningful Choice
경로가 서사와 자원 모두를 바꾸기 때문에 '재미있는 이야기를 볼 것인가'와 '효율적으로 이동할 것인가'가 같은 선택에서 충돌한다.

### Dominant Strategy Risk
빠른 경로가 항상 정답이 아니며 비용·건강·정보와 새로운 연결 노선이 장기 가치에 영향을 준다.

### Information & Uncertainty
현재 도시와 알려진 경로는 보이지만 미발견 노선과 사건 결과는 숨겨져 탐험 욕구를 만든다.

## 5. Risk / Reward Structure
### Primary Risks
- 시간 초과
- 돈 부족
- 건강 악화
- 경로 정보 부족

### Primary Rewards
- 새 도시/노선
- 서사 발견
- 수익
- 시간 단축
- 특수 사건

### Risk Visibility / Failure / Recovery
실패는 자원 압박과 경로 계획 실패에서 나오며, 완전한 전투 패배보다 여행 전체의 누적 선택 결과에 가깝다.

## 6. Progression Design
캐릭터 수치 성장보다 세계 지식, 경로 네트워크, 플레이어의 최적화 지식이 성장한다.

## 7. Economy & Resource Design
돈·시간·건강·수하물 공간이 서로 다른 제약으로 작동해 하나의 통화로 모든 문제를 해결할 수 없다.

## 8. Difficulty & Failure Design
경로 정보 부족, 자원 압박, 예상치 못한 사건이 계획을 흔든다.

## 9. Onboarding & Learning Curve
'80일 안에 세계 일주'라는 명확한 목표가 방향성을 제공하고, 도시 단위로 시스템을 자연스럽게 학습한다.

## 10. Content & Variety
대량의 authored narrative가 필요하지만 위치·상태·경로 시스템이 텍스트를 재맥락화한다.

## 11. Replayability
매우 높다. 한 플레이에서 접근할 수 없는 도시·경로·사건이 많다.

## 12. UX & Information Design
지도와 텍스트, 시간·돈·건강을 한 화면 체계로 연결해 복잡한 세계를 노드 네트워크로 압축한다.

## 13. Player Motivation & Psychology
탐험, 새로운 이야기 발견, 더 좋은 경로, 자신의 여행담 생성.

## 14. Scope & Production Efficiency
글과 상태 관리 비용은 높아 솔로 개발자가 그대로 재현하기 어렵다. 대신 '경로가 곧 콘텐츠 선택'이라는 원리는 강한 참고점이다.

## 15. What Worked
- 지도 이동과 서사 선택을 하나의 행동으로 묶어 시스템과 내러티브를 통합한다.
- 상태 반응형 텍스트가 콘텐츠를 단순 1회 소비가 아니라 다른 맥락에서 재사용하게 한다.

## 16. What Did Not Work / Limitations
- 대량 고품질 텍스트와 상태 추적은 큰 제작 부담이다.
- 원하는 경로나 사건을 찾지 못하는 정보 부족이 좌절을 만들 수 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 텍스트 게임의 선택이 단순 분기 감상으로 느껴지지 않게 하려면?  
**Solution:** 이동·시간·돈·건강 판단이 어떤 이야기를 보게 될지 직접 결정하도록 한다.  
**Trade-off:** 상태 반응형 작문과 QA 비용이 매우 크다.

## 18. What This Game Teaches
- 이동/자원 선택을 곧 서사 선택으로 만들면 게임과 이야기가 통합된다.
- 모든 콘텐츠를 한 회차에 보여주지 않으면 세계가 더 크게 느껴진다.
- 텍스트 분기는 상태 반응성과 결합해야 재사용 가치가 커진다.

## 19. What NOT to Copy
- 도시 수 경쟁
- 분기 텍스트 양 경쟁
- 여행 소재만 모방

## 20. Solo Indie Developer Lessons
### Worth Learning
노드 지도와 자원 구조는 작게 구현 가능하지만 authored narrative 규모는 크게 축소해야 한다.

### Expensive to Reproduce
대량 텍스트, 번역, 상태 플래그와 분기 QA.

### Possible Simplification
프로토타입은 도시 8~10개와 사건 30~40개로 경로가 실제로 이야기를 바꾸는지 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Interactive Fiction, Travel, Branching Narrative, Resource Management, Route Planning
- **Best Review Use:** 텍스트 게임 / 시스템 내러티브 / 여행 / 경로 선택

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 분기 텍스트는 단순 트리가 아니라 위치·시간·자원·이전 사건에 반응하는 시스템이 될 수 있다.
- **Biggest Warning:** 80 Days의 강점은 글의 양만이 아니다. 상태 반응형 내러티브 구조 없이 분기 수만 늘리면 제작비가 폭증한다.
- **Best Reference For:** 텍스트 게임 / 시스템 내러티브 / 여행 / 경로 선택
- **Core Design Principle:** 이동/자원 선택을 곧 서사 선택으로 만들면 게임과 이야기가 통합된다.

## 23. Final Assessment
### Design Strengths
- 강한 시스템-서사 통합
- 매우 높은 세계 탐험감
- 높은 재플레이

### Design Weaknesses
- 작문/번역 비용
- 상태 QA 복잡도
- 정보 누락 좌절

### Most Transferable Lesson
이동/자원 선택을 곧 서사 선택으로 만들면 게임과 이야기가 통합된다.

### Most Dangerous Misinterpretation
80 Days의 강점은 글의 양만이 아니다. 상태 반응형 내러티브 구조 없이 분기 수만 늘리면 제작비가 폭증한다.

## 24. Sources & Evidence
- [GDC Post-mortem](https://gdcvault.com/play/1021666/80-DAYS-Post-mortem-Letting) — Developer postmortem
- [GameDeveloper Postmortem](https://www.gamedeveloper.com/business/postmortem-inkle-s-i-80-days-i-) — Developer postmortem
- [GDC Narrative talk](https://gdcvault.com/play/1022101/Leading-Players-Astray-80-Days) — Narrative designer talk

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-11 — A Short Hike

<!-- SOURCE_FILE: 11_A_Short_Hike.md -->

# Game Design Case Study v1.0 — A Short Hike

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** Adam Robinson-Yu
- **Release:** 2019
- **Genre:** Exploration / Adventure / Small open world
- **Development Scale:** Solo-led indie
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
작은 섬과 하나의 명확한 목표를 중심으로 이동 성장·자유 탐험·짧은 NPC 이벤트를 배치해 '작지만 완결된 오픈월드'를 만든 게임.

### Why This Game Matters
1인 개발 Scope, 작은 맵을 크게 느끼게 하는 방법, 제한된 제작 기간에서 기능을 선택하고 버리는 법의 핵심 레퍼런스다.

### Primary Design Lessons
- 오픈월드의 가치는 면적보다 탐색 밀도와 이동 재미에서 나올 수 있다.
- 짧은 개발 기간은 기능 제거 기준을 명확하게 해 프로젝트 정체성을 강화할 수 있다.
- 하나의 큰 목표와 많은 작은 자발적 목표를 결합하면 자유와 방향성을 동시에 준다.
- 저비용 아트와 거리/카메라 설계가 작은 공간을 더 풍부하게 느끼게 한다.

### Primary Warning
작은 맵과 저해상도 그래픽만 따라 한다고 Scope가 좋아지는 것은 아니다. 모든 요소가 '편안한 탐험과 이동'이라는 같은 경험을 지지한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 정상에 올라 통화 연결을 해야 하지만, 섬 곳곳의 사람과 장소를 자유롭게 발견하며 잠시 쉬어가는 여행자가 된다.

### Target Player
낮은 스트레스, 자유 탐험, 짧은 완결 경험과 이동 자체의 즐거움을 선호하는 플레이어.

### Design Pillars
- Tiny Open World
- Joyful Movement
- Optional Discovery
- Scope Discipline

### USP
오픈월드 감각을 거대한 맵이 아니라 촘촘한 랜드마크와 등반/활공으로 구현한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 걷기
- 등반
- 활공
- 수집
- 대화
- 낚시
- 탐색

### Core Loop
`관심 지점 발견 → 이동/탐험 → NPC/아이템/Feather 획득 → 이동 범위 확장 → 더 높은/먼 지역 탐색`

### Short-Term Loop
다음 관심 지점까지 이동하고 작은 상호작용을 수행한다.

### Session Loop
섬을 자유롭게 돌아다니며 정상에 오르기 위한 준비와 사이드 활동을 한다.

### Long-Term / Meta Loop
짧은 완결형 게임으로 강한 메타 구조는 없다.

### Loop Strength
이동 자체가 즐겁고 Feather가 새로운 공간 접근성을 만들어 같은 지형도 성장 후 다르게 보인다.

## 4. Decision Design
### Primary Decisions
- 정상 목표를 바로 추구할지 주변을 탐험할지
- 어떤 경로로 올라갈지
- NPC 활동에 시간을 쓸지

### Decision Depth / Meaningful Choice
전략적 기회비용은 낮지만 공간 선택과 호기심 중심 Agency가 강하다. '어디로 갈지'가 핵심 선택이다.

### Dominant Strategy Risk
효율적인 정상 경로는 존재할 수 있으나 게임이 시간 경쟁을 강제하지 않아 최적화가 자유 탐험을 압도하지 않는다.

### Information & Uncertainty
정상이라는 큰 목표는 명확하지만 세부 관심 지점은 시야와 랜드마크를 통해 자연스럽게 발견한다.

## 5. Risk / Reward Structure
### Primary Risks
- 낮음
- 길 찾기 실패
- 이동 자원 부족

### Primary Rewards
- 이동 능력
- 새 장소
- 짧은 이야기
- 수집품
- 경치와 발견

### Risk Visibility / Failure / Recovery
실패 처벌보다 탐험 자유가 중심이다. 낙하나 잘못된 길도 큰 비용 없이 다시 시도할 수 있다.

## 6. Progression Design
Golden Feather와 이동 숙련이 공간 접근성을 넓히는 체감 성장이다.

## 7. Economy & Resource Design
가벼운 수집/구매 요소가 있으나 핵심 압박 경제는 아니다.

## 8. Difficulty & Failure Design
정상으로 갈수록 등반 자원과 이동 이해를 더 요구하지만 높은 처벌은 없다.

## 9. Onboarding & Learning Curve
메인 목표를 제시한 뒤 즉시 자유 이동을 허용한다. 조작과 공간 자체가 튜토리얼 역할을 한다.

## 10. Content & Variety
작은 섬에 NPC·수집·경관·이동 루프를 높은 밀도로 배치한다.

## 11. Replayability
낮음~중간. 다른 경로와 놓친 활동은 있지만 런 반복보다 기억에 남는 1회 완결을 우선한다.

## 12. UX & Information Design
HUD를 최소화하고 랜드마크·지형·높이 차가 길 안내를 한다.

## 13. Player Motivation & Psychology
호기심, 이동의 즐거움, 정상 목표, 작은 인간적 만남, 휴식감.

## 14. Scope & Production Efficiency
개발자 GDC 자료에서 초기 출시가 약 4개월 제한 안에서 만들어졌다고 설명된다. Scope 관리 연구에 특히 중요하다.

## 15. What Worked
- 작은 공간과 즐거운 이동을 결합해 면적보다 체감 탐험량을 늘린다.
- 정상이라는 명확한 목표가 자유 탐험 중에도 방향성을 유지한다.

## 16. What Did Not Work / Limitations
- 장기 전략이나 반복 빌드 깊이는 낮다.
- 충분히 탐험한 뒤에는 새 발견이 빠르게 소진된다.

## 17. Design Problem → Solution Analysis
**Problem:** 솔로 개발자가 오픈월드 감각을 만들 수 있는가?  
**Solution:** 면적을 줄이고 이동 재미·랜드마크 밀도·수직성을 높인다.  
**Trade-off:** 장기 콘텐츠와 재플레이는 제한된다.

## 18. What This Game Teaches
- Scope는 콘텐츠 수보다 목표 경험에 기여하는 기능만 남기는 것으로 통제한다.
- 작은 맵은 이동 재미와 랜드마크 밀도로 크게 느껴질 수 있다.
- 짧은 게임은 재플레이보다 완결성과 밀도를 우선할 수 있다.

## 19. What NOT to Copy
- 작은 맵 자체
- 저해상도 그래픽만 모방
- 사이드 활동을 이유 없이 추가

## 20. Solo Indie Developer Lessons
### Worth Learning
프로토타입의 목표 감정을 먼저 정하고 나머지 기능을 과감히 버리는 제작 태도가 가장 중요하다.

### Expensive to Reproduce
오픈월드 규모를 키우거나 고유 NPC/퀘스트를 늘리는 순간 Scope 장점이 빠르게 사라진다.

### Possible Simplification
작은 맵 하나와 이동 능력 2개, NPC 5명만으로 탐험 밀도와 이동 재미를 먼저 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Solo Dev, Scope, Open World, Exploration, Movement, Low-Stress
- **Best Review Use:** 1인 개발 Scope / 작은 오픈월드 / 프로토타입 범위

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 오픈월드의 가치는 면적보다 탐색 밀도와 이동 재미에서 나올 수 있다.
- **Biggest Warning:** 작은 맵과 저해상도 그래픽만 따라 한다고 Scope가 좋아지는 것은 아니다. 모든 요소가 '편안한 탐험과 이동'이라는 같은 경험을 지지한다.
- **Best Reference For:** 1인 개발 Scope / 작은 오픈월드 / 프로토타입 범위
- **Core Design Principle:** Scope는 콘텐츠 수보다 목표 경험에 기여하는 기능만 남기는 것으로 통제한다.

## 23. Final Assessment
### Design Strengths
- 매우 높은 Scope Discipline
- 작은 공간의 높은 밀도
- 명확한 목표와 자유의 공존

### Design Weaknesses
- 낮은 재플레이
- 낮은 전략 깊이
- 콘텐츠 소진

### Most Transferable Lesson
Scope는 콘텐츠 수보다 목표 경험에 기여하는 기능만 남기는 것으로 통제한다.

### Most Dangerous Misinterpretation
작은 맵과 저해상도 그래픽만 따라 한다고 Scope가 좋아지는 것은 아니다. 모든 요소가 '편안한 탐험과 이동'이라는 같은 경험을 지지한다.

## 24. Sources & Evidence
- [GDC Crafting A Tiny Open World](https://gdcvault.com/play/1026613/Independent-Games-Summit-Crafting-A) — Developer postmortem
- [GameDeveloper summary](https://www.gamedeveloper.com/design/finding-smart-shortcuts-in-a-short-hike-postmortem-unlocking-the-vault-4) — Postmortem summary

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY



---

# REF-12 — Vampire Survivors

<!-- SOURCE_FILE: 12_Vampire_Survivors.md -->

# Game Design Case Study v1.0 — Vampire Survivors

> **Studio Game Design Reviewer — Primary Reference Library**  
> 목적: 표면 Feature가 아니라 설계 문제·해결 원리·트레이드오프·제작 효율을 분석한다.

## 0. Document Information
- **Developer:** poncle / Luca Galante (original creator)
- **Release:** 2022
- **Genre:** Action roguelike / Bullet heaven
- **Development Scale:** Solo-origin project expanded into studio development
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
자동 공격과 단순 이동만 남기고 몬스터 밀도·레벨업 선택·무기 진화·수치 폭발을 빠르게 반복해 극단적으로 높은 보상 빈도를 만드는 액션 로그라이트.

### Why This Game Matters
입력 단순화, 즉각적 피드백, 저비용 콘텐츠 확장, 작게 시작해 성공 후 확장하는 전략의 대표 사례다.

### Primary Design Lessons
- 플레이어 입력을 줄여도 위치·빌드·성장 판단을 유지하면 깊이를 보존할 수 있다.
- 짧은 간격의 경험치와 레벨업 선택은 매우 강한 보상 리듬을 만든다.
- 적과 투사체 수 증가만으로도 고비용 애니메이션 없이 성장 스펙터클을 만들 수 있다.
- 작은 핵심 루프를 검증한 뒤 콘텐츠를 확장하는 방식은 1인 개발에 특히 유효하다.

### Primary Warning
자동 공격과 몬스터 수만 복사하면 금방 지루해진다. 이동·빌드 선택·성장 리듬이 계속 판단과 보상을 제공하기 때문에 작동한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 복잡한 액션 콤보를 수행하는 전사가 아니라, 점점 강해지는 자동 무기 시스템을 구축하며 화면을 지배하는 생존자다.

### Target Player
짧은 세션, 강한 성장 피드백, 간단한 조작과 빌드 실험을 좋아하는 플레이어.

### Design Pillars
- Minimal Input
- High Reward Frequency
- Build Evolution
- Enemy Density

### USP
공격 입력을 제거해 이동과 빌드 선택에만 집중시키면서 화면 전체가 성장 피드백이 되게 한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 이동
- 레벨업 선택
- 무기/패시브 조합
- 위치 선정
- 보상 수집

### Core Loop
`적 회피/처치 → 경험치 획득 → 레벨업 선택 → 화력 증가 → 더 많은 적 처치 → 상자/진화 → 더 높은 밀도`

### Short-Term Loop
적 무리 사이에서 안전한 위치와 경험치 수집 경로를 선택한다.

### Session Loop
제한 시간 동안 빌드를 완성하며 지속적으로 증가하는 적 밀도를 버틴다.

### Long-Term / Meta Loop
캐릭터·무기·스테이지·영구 업그레이드·비밀 해금이 장기 목표다.

### Loop Strength
수 초마다 경험치·레벨업·적 처치가 반복돼 보상 공백이 매우 짧다. 동시에 제한 슬롯이 빌드 판단을 유지한다.

## 4. Decision Design
### Primary Decisions
- 현재 생존용 무기와 미래 진화 조합 중 선택
- 위험한 경험치 수집과 안전 위치 중 선택
- 제한 슬롯에 어떤 빌드를 완성할지

### Decision Depth / Meaningful Choice
조작은 단순하지만 성장 선택이 미래 생존력과 진화 조건을 결정한다. 입력 난이도를 빌드 판단으로 옮긴 구조다.

### Dominant Strategy Risk
강한 무기 조합은 존재하지만 캐릭터·스테이지·해금 목표가 다른 빌드를 시도하게 한다.

### Information & Uncertainty
현재 무기와 레벨업 선택은 명확하지만 진화 조건과 비밀 해금은 일부 발견형 정보다.

## 5. Risk / Reward Structure
### Primary Risks
- 초반 화력 부족
- 포위
- 잘못된 빌드
- 보스/이벤트 실패

### Primary Rewards
- 빈번한 레벨업
- 상자
- 무기 진화
- 금화
- 해금

### Risk Visibility / Failure / Recovery
실패 원인은 대부분 화력 성장 속도와 위치 판단에서 나온다. 짧은 세션과 빠른 성장 덕분에 재시작 부담이 낮다.

## 6. Progression Design
런 안에서 매우 빠른 수직 성장, 런 밖에서 영구 해금과 옵션 확장이 결합된다.

## 7. Economy & Resource Design
레벨업 선택 슬롯과 무기/패시브 슬롯이 기회비용이며, 골드는 메타 업그레이드에 쓰인다.

## 8. Difficulty & Failure Design
시간에 따라 적 밀도와 체력이 올라가며 플레이어 성장 속도가 이를 추월해야 한다.

## 9. Onboarding & Learning Curve
이동만 배우면 즉시 플레이 가능하다. 자동 공격 덕분에 전투 튜토리얼이 거의 필요 없다.

## 10. Content & Variety
무기·진화·캐릭터 Modifier·적·스테이지 규칙을 재조합한다. 콘텐츠 단위 제작비가 낮다.

## 11. Replayability
짧은 런, 해금, 빌드, 캐릭터, 비밀 요소로 매우 강하다.

## 12. UX & Information Design
실시간 액션 중에는 이동만 하고, 레벨업 시 게임을 멈춰 소수 선택지를 보여 인지 부하를 분리한다.

## 13. Player Motivation & Psychology
끊임없는 성장, 화면을 뒤덮는 화력, 해금, 조합 발견, 짧은 목표 달성.

## 14. Scope & Production Efficiency
초기에는 낮은 그래픽·조작 범위로 핵심 루프를 검증하고 성공 후 확장했다. 작게 시작하는 전략의 강한 사례다.

## 15. What Worked
- 자동 공격이 조작 복잡성을 제거하고 이동·성장 판단에 집중시킨다.
- 고빈도 경험치→레벨업→강화 루프가 항상 가까운 다음 보상을 만든다.

## 16. What Did Not Work / Limitations
- 정밀 조작과 액션 콤보를 원하는 플레이어에게 단조로울 수 있다.
- 업데이트가 계속되면 무기·캐릭터 콘텐츠 인플레이션이 생긴다.

## 17. Design Problem → Solution Analysis
**Problem:** 매우 적은 입력으로 강한 액션 만족을 만드는 법.  
**Solution:** 공격을 자동화하고 판단은 위치·성장 선택에 남기며, 성장 결과를 화면 밀도로 즉시 보여준다.  
**Trade-off:** 수동 전투 깊이가 줄어든다.

## 18. What This Game Teaches
- 입력 수를 줄여도 판단 수를 유지하면 깊이를 보존할 수 있다.
- 짧은 보상 간격은 Core Loop 지속력을 강하게 만든다.
- 저비용 데이터 콘텐츠는 성공 검증 후 점진 확장하기 좋다.

## 19. What NOT to Copy
- 자동 공격만 도입
- 적 숫자 증가
- 낮은 가격 전략만 모방

## 20. Solo Indie Developer Lessons
### Worth Learning
작은 입력 집합과 반복 보상 루프를 먼저 검증하고, 성공 후 캐릭터·무기·맵을 확대하는 순서.

### Expensive to Reproduce
성공 후 플랫폼·DLC·대량 콘텐츠 운영. 초기 프로토타입보다 라이브 확장 비용이 크다.

### Possible Simplification
프로토타입은 무기 6개, 진화 2개, 스테이지 1개로 15분 동안 성장 루프가 유지되는지 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Solo Origin, Action Roguelike, Auto Attack, Reward Loop, Meta Progression
- **Best Review Use:** 초기 프로토타입 / 보상 루프 / 입력 단순화 / 저비용 확장

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 플레이어 입력을 줄여도 위치·빌드·성장 판단을 유지하면 깊이를 보존할 수 있다.
- **Biggest Warning:** 자동 공격과 몬스터 수만 복사하면 금방 지루해진다. 이동·빌드 선택·성장 리듬이 계속 판단과 보상을 제공하기 때문에 작동한다.
- **Best Reference For:** 초기 프로토타입 / 보상 루프 / 입력 단순화 / 저비용 확장
- **Core Design Principle:** 입력 수를 줄여도 판단 수를 유지하면 깊이를 보존할 수 있다.

## 23. Final Assessment
### Design Strengths
- 극도로 낮은 조작 진입장벽
- 매우 강한 보상 리듬
- 성공 후 확장 가능한 Scope

### Design Weaknesses
- 수동 액션 깊이 제한
- 콘텐츠 인플레이션
- 강한 장르 취향

### Most Transferable Lesson
입력 수를 줄여도 판단 수를 유지하면 깊이를 보존할 수 있다.

### Most Dangerous Misinterpretation
자동 공격과 몬스터 수만 복사하면 금방 지루해진다. 이동·빌드 선택·성장 리듬이 계속 판단과 보상을 제공하기 때문에 작동한다.

## 24. Sources & Evidence
- [Noclip Making of Vampire Survivors](https://www.youtube.com/watch?v=XQVdR8mJrds) — Developer documentary/interview
- [GameDeveloper development analysis](https://www.gamedeveloper.com/design/vampire-survivors-development-sounds-like-an-open-source-fueled-fever-dream) — Developer interview summary
- [Guardian profile](https://www.theguardian.com/games/2023/aug/04/baftas-video-game-vampire-survivors-luca-galante) — Developer profile/interview

> 개발자 Postmortem / GDC / 개발자 인터뷰 / 공식 자료를 우선한다. 분석적 추론은 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop, 주요 시스템, 공식/개발자 자료에서 직접 확인되는 설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리와 Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 개별 Feature의 정확한 내부 제작 의도와 제작 공수.
- **Unknown:** 비공개 예산, 전체 내부 프로토타입 폐기량, 콘텐츠별 실제 제작 시간.

# END OF CASE STUDY

