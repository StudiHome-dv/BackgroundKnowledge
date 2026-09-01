# Studio Game Design Reviewer — 2차 — Specialized Design Reference
> 프로젝트 소스 업로드용 통합 Reference 문서
> 각 Case Study의 원문 구조를 유지하며 `REF-XX` 경계로 분리했다.
---


---

# REF-13 — RimWorld

<!-- SOURCE_FILE: 13_RimWorld.md -->

# Game Design Case Study v1.0 — RimWorld

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Ludeon Studios / Tynan Sylvester
- **Release:** 2018
- **Genre:** Colony simulation / Story generator
- **Development Scale:** Solo-origin, tiny-team production
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
식민지 경영의 목표를 '완벽한 기지 최적화'보다 예측 불가능한 사건과 인물 관계가 만드는 이야기 생성으로 재정의한 시뮬레이션.

### Why This Game Matters
직원/캐릭터 상태, 사건 생성, 시스템 내러티브, 기능 Scope 선택을 검토하는 데 매우 강한 사례다.

### Primary Design Lessons
- 게임의 상위 목적을 '승리 시스템'이 아니라 '어떤 이야기를 생성할 것인가'로 정의할 수 있다.
- 모든 현실적 기능을 구현하지 않고 이야기 발생에 기여하는 시스템만 선택하면 Scope를 통제할 수 있다.
- 캐릭터의 개별 특성과 관계가 시스템 사건을 감정적 사건으로 바꾼다.
- 랜덤 사건은 난이도뿐 아니라 서사 리듬을 조절하는 감독 시스템이 될 수 있다.

### Primary Warning
시스템 수와 랜덤 사건을 많이 넣는 것 자체가 Story Generator를 만들지는 않는다. 사건이 캐릭터 상태와 장기 기억에 연결되어야 한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 효율적인 공장을 만드는 관리자이면서, 결함 있는 식민지 주민들이 살아남으며 만들어내는 이야기를 관찰·개입하는 감독자다.

### Design Pillars
- Story Generator
- Character Specificity
- Systemic Consequence
- Selective Simulation

### USP
AI Storyteller가 사건 리듬을 조절하고, 주민의 특성·관계·부상·욕구가 사건을 개인적인 이야기로 만든다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 건설
- 업무 배치
- 자원 관리
- 주민 관리
- 전투 대응
- 사건 수습

### Core Loop
`기지 구축 → 생산/생활 유지 → 사건 발생 → 주민·자원 상태 변화 → 대응/회복 → 더 복잡한 사건`

### Loop Strength
기본 생산 루프 위에 주민별 상태와 사건이 겹쳐 같은 위기도 매번 다른 의미를 가진다.

## 4. Decision Design
### Primary Decisions
- 효율과 주민 행복 중 무엇을 우선할지
- 위험한 주민을 구조/영입할지
- 부상·갈등·자원 부족 중 무엇부터 해결할지

### Meaningful Choice
결정이 생산량뿐 아니라 특정 주민의 생존과 관계, 향후 사건 가능성을 바꾸기 때문에 다축 결과를 가진다.

### Information & Uncertainty
기지 상태는 상세히 공개되지만 다음 Storyteller 사건과 주민 행동의 일부는 불확실하다.

## 5. Risk / Reward Structure
주민 사망·정신 붕괴·자원 부족·습격이 핵심 위험이다. 보상은 기지 성장뿐 아니라 예상치 못한 생존 이야기와 주민 애착에서 발생한다.

## 6. Progression Design
기술·기지·장비의 수직 성장과 주민 관계·기억의 누적이 병행된다.

## 7. Economy & Resource Design
생산 자원과 인력 시간이 상호 연결되며, 과도한 부는 더 큰 위협을 불러올 수 있어 단순 축적이 항상 최선은 아니다.

## 8. Difficulty & Failure Design
Storyteller와 난이도 설정이 사건 빈도와 압박을 조절한다. 난이도는 고정 스테이지보다 캠페인 상태에 반응한다.

## 9. Onboarding & Learning Curve
시스템 수가 많아 진입 장벽은 높다. 대신 공간적 기지와 주민 행동이 원인-결과를 시각적으로 보여준다.

## 10. Content & Variety
아이템·특성·사건·생물·환경이 재조합되어 콘텐츠 하나가 여러 이야기 문맥에 사용된다.

## 11. Replayability
Storyteller, 바이옴, 주민, 사건 조합 때문에 매우 높다.

## 12. UX & Information Design
많은 상태를 공간과 우선순위 시스템으로 관리한다. 복잡성이 핵심 재미인 만큼 정보 필터링이 중요하다.

## 13. Player Motivation & Psychology
기지 성장, 주민 애착, 위기 극복, 예상하지 못한 이야기 관찰.

## 14. Scope & Production Efficiency
개발자는 GDC에서 기능을 관습적으로 넣기보다 핵심 경험에 실제 기여하는지를 기준으로 선택했다고 설명한다. Solo Scope에서 특히 중요한 교훈이다.

## 15. What Worked
- Story Generator라는 상위 프레임이 기능 선택 기준을 명확하게 만들었다.
- 캐릭터 특성이 시스템 사건을 개인적 사건으로 변환한다.

## 16. What Did Not Work / Limitations
- 시스템 규모가 커질수록 UI와 학습 비용이 매우 높아진다.
- 모드와 장기 업데이트를 제외한 초기 제작도 상태 조합 QA가 무겁다.

## 17. Design Problem → Solution Analysis
**Problem:** 경영 시뮬레이션의 반복 상황을 어떻게 기억에 남는 이야기로 만들 것인가?  
**Solution:** 캐릭터 특성·관계·사건 감독을 연결해 동일한 시스템 결과에 개인적 맥락을 부여한다.  
**Trade-off:** 상태 공간과 QA 복잡도가 크게 증가한다.

## 18. What This Game Teaches
- 상위 Player Experience가 Feature 선택 기준이 되어야 한다.
- 시뮬레이션은 현실성보다 의미 있는 사건 발생에 필요한 부분만 구현할 수 있다.
- 캐릭터 상태는 추상 수치를 감정적 사건으로 바꾼다.

## 19. What NOT to Copy
- 방대한 자원 종류
- 무한 절차 생성 자체
- AI Storyteller라는 이름만 모방

## 20. Solo Indie Developer Lessons
### Worth Learning
기능을 '필수 장르 관습'이 아니라 핵심 경험 기여도로 평가하는 제작 철학.

### Expensive to Reproduce
방대한 상태 조합, UI, 장기 밸런스와 모딩 생태계.

### Possible Simplification
주민 4~6명, 욕구 3개, 사건 10개 정도로 캐릭터 상태가 사건 의미를 바꾸는지만 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Story Generator, Colony Sim, Character State, Emergent Narrative, Scope
- **Best Review Use:** 직원/캐릭터 운영 / 사건 생성 / 시스템 내러티브 / Feature Scope

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 게임의 상위 목적을 '승리 시스템'이 아니라 '어떤 이야기를 생성할 것인가'로 정의할 수 있다.
- **Biggest Warning:** 시스템 수와 랜덤 사건을 많이 넣는 것 자체가 Story Generator를 만들지는 않는다. 사건이 캐릭터 상태와 장기 기억에 연결되어야 한다.
- **Best Reference For:** 직원/캐릭터 운영 / 사건 생성 / 시스템 내러티브 / Feature Scope
- **Core Design Principle:** 상위 Player Experience가 Feature 선택 기준이 되어야 한다.

## 23. Final Assessment
### Design Strengths
- 강한 emergent narrative
- 높은 재사용성
- 명확한 상위 설계 철학

### Design Weaknesses
- 높은 시스템 복잡도
- 높은 온보딩 비용
- QA 폭증

### Most Transferable Lesson
상위 Player Experience가 Feature 선택 기준이 되어야 한다.

## 24. Sources & Evidence
- [GDC RimWorld Design Methods](https://www.gdcvault.com/play/1024232/-RimWorld) — Developer GDC

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-14 — Mini Metro

<!-- SOURCE_FILE: 14_Mini_Metro.md -->

# Game Design Case Study v1.0 — Mini Metro

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Dinosaur Polo Club
- **Release:** 2015
- **Genre:** Minimalist strategy / Network management
- **Development Scale:** Tiny team
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
지하철 노선 연결이라는 하나의 추상 시스템만으로 수요 증가·병목·제한 자원을 만들어 짧고 반복 가능한 네트워크 경영 게임을 구성했다.

### Why This Game Matters
Scope 제약을 아이디어 생성 규칙으로 사용한 대표 Postmortem이며, 작은 시스템으로 운영 게임을 만드는 방법을 검토하기 좋다.

### Primary Design Lessons
- 개발자의 약점과 시간 제약을 먼저 정의하면 적합한 게임 아이디어를 더 빨리 찾을 수 있다.
- 수작업 레벨과 대량 아트를 제거하고 절차적 수요 변화에 집중하면 작은 팀도 반복 가능한 경영 게임을 만들 수 있다.
- 프로토타입을 이틀 안에 만들 수 있는가를 Scope 필터로 사용할 수 있다.
- 초기 공개 검증은 개발 리스크 감소와 커뮤니티 형성을 동시에 할 수 있다.

### Primary Warning
미니멀한 그래픽이 곧 작은 Scope를 의미하지 않는다. 밸런스와 UX polish는 예상보다 긴 개발 비용을 만들 수 있다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 도시 전체를 건설하는 시장이 아니라 계속 변하는 승객 수요에 노선을 재배치하는 교통망 운영자다.

### Design Pillars
- Network Optimization
- Minimal Scope
- Dynamic Demand
- Readable Abstraction

### USP
도시를 노선도 수준으로 추상화해 복잡한 교통 문제를 몇 개의 선과 도형으로 표현한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 노선 연결
- 노선 수정
- 차량/터널 배분
- 병목 관찰
- 업그레이드 선택

### Core Loop
`역/승객 생성 → 노선 연결 → 수요 증가 → 병목 발생 → 노선 재구성/업그레이드 → 더 높은 수요`

### Loop Strength
맵은 단순하지만 역 위치와 승객 수요가 계속 바뀌어 네트워크를 완성할 수 없고 지속적인 재설계가 필요하다.

## 4. Decision Design
### Primary Decisions
- 현재 병목을 해결할지 미래 확장을 준비할지
- 제한된 노선/차량/터널을 어디에 배치할지
- 기존 노선을 재구성해 단기 혼란을 감수할지

### Meaningful Choice
한 자원을 어디에 배치하느냐가 전체 네트워크 효율을 바꾸므로 적은 선택지에서도 기회비용이 크다.

### Information & Uncertainty
현재 승객과 노선 상태는 시각적으로 공개되지만 다음 역 생성과 수요 증가는 불확실하다.

## 5. Risk / Reward Structure
한 역의 과밀이 실패로 이어진다. 보상은 점수와 더 효율적인 네트워크, 주기적 업그레이드 선택이다.

## 6. Progression Design
런 내부에서 노선·차량·터널이 증가한다. 장기 성장보다 플레이어의 네트워크 설계 숙련이 중요하다.

## 7. Economy & Resource Design
노선, 객차, 터널이 제한 자원이며 서로 대체되지 않아 배치 우선순위가 중요하다.

## 8. Difficulty & Failure Design
시간이 갈수록 역과 승객이 늘어 네트워크가 자연스럽게 복잡해진다.

## 9. Onboarding & Learning Curve
도형과 선만으로 상태를 표현해 조작과 결과를 빠르게 이해시킨다.

## 10. Content & Variety
도시별 지형 규칙과 절차적 역 생성이 수작업 레벨 제작 부담을 줄인다.

## 11. Replayability
짧은 세션과 절차적 배치, 도시별 제약으로 높다.

## 12. UX & Information Design
실제 교통 노선도의 시각 언어를 사용해 복잡한 네트워크를 직관적으로 표현한다.

## 13. Player Motivation & Psychology
질서 만들기, 병목 해결, 점수 향상, 아름다운 네트워크 구성.

## 14. Scope & Production Efficiency
개발진은 Postmortem에서 '수작업 레벨 없음, 아트-heavy 금지, 오디오 의존 금지' 같은 제약을 먼저 세웠다고 설명한다.

## 15. What Worked
- 제약을 부정적 한계가 아니라 콘셉트 생성 도구로 사용했다.
- 단일 네트워크 시스템이 자연스럽게 난이도와 반복성을 만든다.

## 16. What Did Not Work / Limitations
- 밸런스와 인터페이스 polish가 초기 예상보다 훨씬 큰 비용이었다.
- 장기 서사·캐릭터 동기는 거의 없다.

## 17. Design Problem → Solution Analysis
**Problem:** 시간과 아트 역량이 제한된 작은 팀이 완성 가능한 경영 게임을 어떻게 고를 것인가?  
**Solution:** 제작 제약을 먼저 명문화하고 그 안에서만 콘셉트를 탐색한다.  
**Trade-off:** 표현 범위와 장르적 풍부함이 제한된다.

## 18. What This Game Teaches
- 제작 제약은 콘셉트 선택의 적극적 설계 도구가 될 수 있다.
- 프로토타입 가능 크기는 최종 Scope의 강력한 위험 신호다.
- 추상화는 제작비를 줄이면서 시스템 가독성을 높일 수 있다.

## 19. What NOT to Copy
- 노선도 그래픽 자체
- 무조건 절차 생성
- 미니멀 UI를 polish 비용이 없는 것으로 가정

## 20. Solo Indie Developer Lessons
### Worth Learning
현재 보유 기술·시간·외주 가능 영역을 먼저 적고, 그 조건을 만족하는 게임만 후보로 남기는 방식.

### Expensive to Reproduce
밸런싱, 크로스 플랫폼 UX, 고급 procedural audio와 polish.

### Possible Simplification
한 도시, 5개 역 타입, 3개 제한 자원만으로 병목 해결이 반복 가능한지 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Scope, Network, Minimalism, Procedural Demand, Prototype
- **Best Review Use:** 1인 개발 Scope / 네트워크 운영 / 프로토타입 검증

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 개발자의 약점과 시간 제약을 먼저 정의하면 적합한 게임 아이디어를 더 빨리 찾을 수 있다.
- **Biggest Warning:** 미니멀한 그래픽이 곧 작은 Scope를 의미하지 않는다. 밸런스와 UX polish는 예상보다 긴 개발 비용을 만들 수 있다.
- **Best Reference For:** 1인 개발 Scope / 네트워크 운영 / 프로토타입 검증
- **Core Design Principle:** 제작 제약은 콘셉트 선택의 적극적 설계 도구가 될 수 있다.

## 23. Final Assessment
### Design Strengths
- 극도로 명확한 Core Loop
- 높은 시각 가독성
- 강한 Scope discipline

### Design Weaknesses
- 제한된 서사성
- 후반 반복
- 예상보다 큰 polish 비용

### Most Transferable Lesson
제작 제약은 콘셉트 선택의 적극적 설계 도구가 될 수 있다.

## 24. Sources & Evidence
- [Mini Metro Postmortem](https://www.gamedeveloper.com/audio/postmortem-dinosaur-polo-club-s-i-mini-metro-i-) — Developer postmortem

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-15 — This War of Mine

<!-- SOURCE_FILE: 15_This_War_of_Mine.md -->

# Game Design Case Study v1.0 — This War of Mine

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** 11 bit studios
- **Release:** 2014
- **Genre:** Survival management / Narrative
- **Development Scale:** Indie studio
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
전쟁을 군인의 승리 판타지가 아니라 민간인의 생존·결핍·도덕적 타협으로 재구성해 자원 시스템 자체가 메시지를 전달하게 만든 게임.

### Why This Game Matters
테마와 시스템을 일치시키는 방법, 자원 부족이 도덕 선택을 발생시키는 구조, 캐릭터 상태의 서사화를 검토하는 데 유용하다.

### Primary Design Lessons
- 게임의 메시지는 컷신보다 플레이어가 반복하는 시스템 행동으로 전달할 수 있다.
- 자원 부족이 실제 선택 비용을 만들 때 도덕적 딜레마가 강해진다.
- 캐릭터의 우울·질병·상처 같은 상태가 플레이어의 효율 판단을 인간적 판단으로 바꾼다.
- 테마가 명확하면 기능·아트·사운드가 같은 경험을 향하도록 정렬할 수 있다.

### Primary Warning
우울한 분위기와 잔혹한 선택만 복제하면 감정 조작처럼 보일 수 있다. 선택의 원인이 실제 생존 시스템에서 발생해야 한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 전쟁에서 승리하는 영웅이 아니라 포위된 도시의 민간인 집단을 하루씩 버티게 하는 생존 관리자다.

### Design Pillars
- Civilian Perspective
- Scarcity
- Moral Consequence
- Human Cost

### USP
전쟁 게임의 관점을 전투 승리에서 일상 생존과 인간적 비용으로 뒤집는다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 제작
- 탐색
- 약탈/거래
- 식량 배분
- 치료
- 야간 파견
- 도덕적 선택

### Core Loop
`낮: 은신처 관리/제작 → 밤: 탐색/거래/위험 행동 → 자원 획득 → 캐릭터 상태 변화 → 다음 날 생존`

### Loop Strength
같은 식량·약품도 캐릭터 상태와 도덕적 사건에 따라 가치가 달라진다.

## 4. Decision Design
### Primary Decisions
- 누구에게 부족한 자원을 우선 배분할지
- 타인을 약탈해 생존할지
- 위험한 지역에 누구를 보낼지

### Meaningful Choice
효율적 선택이 캐릭터의 심리와 인간적 결과를 악화시킬 수 있어 전략적 최적화와 가치 판단이 충돌한다.

### Information & Uncertainty
현재 생존 상태는 보이지만 탐색 장소의 위험과 사건 결과는 일부 불확실하다.

## 5. Risk / Reward Structure
굶주림·질병·부상·사망·우울이 누적된다. 보상은 생존과 자원뿐 아니라 인간성을 지켰다는 감정적 성취다.

## 6. Progression Design
은신처 설비와 제작 능력은 성장하지만 전쟁 상황은 지속적으로 이를 압박한다.

## 7. Economy & Resource Design
식량·약품·재료·시간·인력이 모두 부족해 완전한 해결이 어렵다. 부족 자체가 선택을 발생시키는 엔진이다.

## 8. Difficulty & Failure Design
겨울, 습격, 질병과 자원 고갈이 장기적으로 누적된다.

## 9. Onboarding & Learning Curve
생존이라는 직관적 목표가 시스템 우선순위를 알려주지만 실패를 통한 학습 비중도 높다.

## 10. Content & Variety
장소·생존자·사건·상태 조합이 같은 시스템에 다른 도덕적 맥락을 부여한다.

## 11. Replayability
캐릭터 조합과 사건 변주로 중상 수준이며 첫 플레이의 감정적 충격이 가장 강하다.

## 12. UX & Information Design
은신처의 단면 구조가 사람과 생산 시설을 동시에 보여줘 생활 상태를 공간적으로 읽게 한다.

## 13. Player Motivation & Psychology
생존, 캐릭터 보호, 도덕적 자기검증, 전쟁이 끝날 때까지 버티기.

## 14. Scope & Production Efficiency
1차 Library의 Frostpunk보다 개인 단위 상태와 작은 공간에 집중한 참고점이다.

## 15. What Worked
- 테마가 시스템 선택과 직접 결합되어 메시지가 플레이 경험에서 나온다.
- 캐릭터 상태가 자원 배분을 감정적 판단으로 바꾼다.

## 16. What Did Not Work / Limitations
- 지속적인 결핍과 우울한 톤이 플레이 피로를 높인다.
- 반복 플레이에서는 첫 회차의 도덕적 충격이 최적화 지식으로 대체될 수 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 게임이 특정 주제를 말하는 데서 끝나지 않고 플레이어가 체험하게 하려면?  
**Solution:** 주제의 핵심 갈등을 자원·상태·반복 행동의 규칙으로 변환한다.  
**Trade-off:** 의도적으로 불편하고 피로한 플레이가 될 수 있다.

## 18. What This Game Teaches
- 테마는 플레이어가 반복하는 행동에 내장될 때 가장 강하다.
- 결핍은 선택을 만들지만 회복 가능성을 완전히 없애면 통제감도 사라진다.
- 개별 캐릭터 상태는 추상 경제를 인간적 비용으로 번역한다.

## 19. What NOT to Copy
- 암울한 톤
- 도덕적 충격 이벤트 수
- 결핍을 무조건 심하게 만드는 것

## 20. Solo Indie Developer Lessons
### Worth Learning
큰 세계 대신 작은 생활 공간과 소수 캐릭터 상태로 주제를 시스템화하는 방식.

### Expensive to Reproduce
고품질 아트·애니메이션·다수 사건과 캐릭터 반응 콘텐츠.

### Possible Simplification
3명 캐릭터, 자원 4종, 10일 생존 시나리오로 자원 선택과 도덕 판단이 실제 충돌하는지 확인한다.

## 21. Reference Comparison Tags
- **Design Tags:** Survival, Moral Choice, Character State, Theme-System Alignment, Scarcity
- **Best Review Use:** 도덕 선택 / 생존 경영 / 캐릭터 상태 / 테마-시스템 일치

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 게임의 메시지는 컷신보다 플레이어가 반복하는 시스템 행동으로 전달할 수 있다.
- **Biggest Warning:** 우울한 분위기와 잔혹한 선택만 복제하면 감정 조작처럼 보일 수 있다. 선택의 원인이 실제 생존 시스템에서 발생해야 한다.
- **Best Reference For:** 도덕 선택 / 생존 경영 / 캐릭터 상태 / 테마-시스템 일치
- **Core Design Principle:** 테마는 플레이어가 반복하는 행동에 내장될 때 가장 강하다.

## 23. Final Assessment
### Design Strengths
- 매우 강한 테마-시스템 통합
- 감정적 자원 판단
- 명확한 Player Experience

### Design Weaknesses
- 높은 감정 피로
- 반복 시 최적화
- 콘텐츠 제작비

### Most Transferable Lesson
테마는 플레이어가 반복하는 행동에 내장될 때 가장 강하다.

## 24. Sources & Evidence
- [GDC Lessons from This War of Mine and Frostpunk](https://www.gdcvault.com/play/1025741/Why-Make) — Developer GDC

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-16 — Invisible Inc

<!-- SOURCE_FILE: 16_Invisible_Inc.md -->

# Game Design Case Study v1.0 — Invisible, Inc.

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Klei Entertainment
- **Release:** 2015
- **Genre:** Turn-based stealth tactics / Roguelike
- **Development Scale:** Indie studio
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
스텔스의 불확실성과 턴제 전술의 계산 가능성을 결합하고, 경보가 시간에 따라 상승하는 구조로 '완벽한 잠입'보다 제한된 시간 안의 위험 관리에 집중한 게임.

### Why This Game Matters
잠입/정보 설계, 경보 시스템, 턴제 상태 가독성, 실패를 완전 종료가 아닌 탈출 판단으로 만드는 구조에 유용하다.

### Primary Design Lessons
- 스텔스도 턴제로 만들면 정보와 결과를 더 명확하게 보여줄 수 있다.
- 경보 타이머는 플레이어가 무한 대기·완전 탐색하는 지배 전략을 억제한다.
- 발각을 즉시 실패로 만들지 않으면 실수 이후의 복구 플레이가 생긴다.
- 절차 생성은 콘텐츠 수보다 반복되는 의사결정 구조를 유지하는 데 사용해야 한다.

### Primary Warning
경보 게이지만 추가하면 긴장이 생기는 것이 아니다. 시간이 지날수록 실제 게임 상태와 적 대응이 변해야 한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 모든 경비를 제거하는 전투 부대가 아니라 정보를 훔치고 상황이 악화되기 전에 탈출하는 첩보 지휘관이다.

### Design Pillars
- Information
- Escalation
- Stealth Recovery
- Procedural Missions

### USP
턴제 완전 정지 상태에서 경비 시야와 이동을 계산하면서도 Alarm이 계속 임무의 장기 압박을 만든다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 이동
- 관찰
- 해킹
- 기절
- 문 조작
- 아이템 사용
- 탈출

### Core Loop
`시설 진입 → 정보 수집/해킹 → 경보 상승 → 목표 확보 → 위험 증가 → 탈출 → 요원/장비 강화`

### Loop Strength
단기 턴은 계산 가능하지만 장기 경보가 계속 상태를 악화시켜 안전한 정답 탐색을 제한한다.

## 4. Decision Design
### Primary Decisions
- 추가 보상을 위해 더 깊이 들어갈지
- 경비를 우회/기절/해킹 중 어떻게 처리할지
- 실수 후 임무를 계속할지 즉시 탈출할지

### Meaningful Choice
시간·Power·요원 위치·경보가 서로 경쟁해 완벽한 해결보다 손실 최소화 판단이 중요하다.

### Information & Uncertainty
경비 시야와 행동을 관찰해 정보를 얻을 수 있지만 미탐색 공간과 이후 증원은 불확실하다.

## 5. Risk / Reward Structure
경보 상승, 요원 체포, Power 부족이 핵심 위험이며 보상은 Credits·장비·정보·요원 성장이다.

## 6. Progression Design
런 내 요원·장비 강화와 캠페인 진행이 결합된다.

## 7. Economy & Resource Design
Power는 해킹 행동의 제한 자원이고 Credits는 장비/증강에 쓰인다. 턴 자체도 경보라는 시간 자원이다.

## 8. Difficulty & Failure Design
Alarm 단계와 기업별 보안 장치, 미션 구조가 복합적으로 상승한다.

## 9. Onboarding & Learning Curve
턴제와 시야 표시가 스텔스 결과를 읽기 쉽게 하지만 시스템 종류가 늘면서 학습 부담이 커진다.

## 10. Content & Variety
절차 맵, 기업 보안 규칙, 요원, 장비를 재조합한다.

## 11. Replayability
캠페인 절차 생성과 다른 요원 조합으로 높다.

## 12. UX & Information Design
위험 타일과 경비 시야를 명확하게 표시해 '보이지 않아서 실패'하는 문제를 줄인다.

## 13. Player Motivation & Psychology
정보 우위, 완벽한 탈출, 위기 복구, 요원 빌드.

## 14. Scope & Production Efficiency
Solo 규모는 아니지만 복잡한 스텔스를 작은 타일·턴 구조로 추상화하는 방식은 프로토타입 참고 가치가 높다.

## 15. What Worked
- Alarm이 무한 최적화 전략을 억제하고 임무 리듬을 만든다.
- 발각 이후에도 복구·탈출 가능성을 남겨 스텔스 실패의 이분법을 완화한다.

## 16. What Did Not Work / Limitations
- 턴제 계산과 스텔스 긴장의 조합은 높은 인지 부하를 만든다.
- 절차 맵이 수작업 잠입 레벨만큼 강한 공간 서사를 주기 어렵다.

## 17. Design Problem → Solution Analysis
**Problem:** 스텔스에서 플레이어가 무한 대기하며 완벽한 안전을 확보하는 것을 어떻게 막을 것인가?  
**Solution:** 시간 경과가 경보와 적 대응을 실제로 강화하게 한다.  
**Trade-off:** 신중한 플레이어에게 시간 압박 스트레스를 준다.

## 18. What This Game Teaches
- 타이머는 단순 숫자가 아니라 게임 상태를 변화시켜야 한다.
- 실수 이후의 복구 선택은 실패 경험을 더 풍부하게 만든다.
- 정보를 명확히 보여주면 난이도를 숨은 규칙 대신 판단에서 만들 수 있다.

## 19. What NOT to Copy
- Alarm 숫자만 추가
- 절차 맵 자체
- 턴제 스텔스를 모든 잠입 장르에 적용

## 20. Solo Indie Developer Lessons
### Worth Learning
작은 Grid와 명확한 시야 규칙으로 복잡한 잠입을 추상화하는 방식.

### Expensive to Reproduce
절차 레벨 QA, 적 AI와 시야 예외 처리, 캠페인 밸런스.

### Possible Simplification
8x8 수준 Grid, 경비 2종, Alarm 4단계로 압박과 복구 플레이를 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Stealth, Alarm, Turn-Based, Information, Recovery
- **Best Review Use:** 모니터링/잠입 / 정보 가독성 / 시간 압박 / 복구 설계

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 스텔스도 턴제로 만들면 정보와 결과를 더 명확하게 보여줄 수 있다.
- **Biggest Warning:** 경보 게이지만 추가하면 긴장이 생기는 것이 아니다. 시간이 지날수록 실제 게임 상태와 적 대응이 변해야 한다.
- **Best Reference For:** 모니터링/잠입 / 정보 가독성 / 시간 압박 / 복구 설계
- **Core Design Principle:** 타이머는 단순 숫자가 아니라 게임 상태를 변화시켜야 한다.

## 23. Final Assessment
### Design Strengths
- 명확한 정보 기반 스텔스
- 강한 임무 리듬
- 실패 복구 공간

### Design Weaknesses
- 인지 부하
- 절차 맵의 공간성 한계
- AI QA 비용

### Most Transferable Lesson
타이머는 단순 숫자가 아니라 게임 상태를 변화시켜야 한다.

## 24. Sources & Evidence
- [Klei forum linking developer GDC procedural stealth talk](https://forums.kleientertainment.com/forums/topic/53830-invisible-inc-official-release/) — Developer community reference

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-17 — Return of the Obra Dinn

<!-- SOURCE_FILE: 17_Return_of_the_Obra_Dinn.md -->

# Game Design Case Study v1.0 — Return of the Obra Dinn

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Lucas Pope
- **Release:** 2018
- **Genre:** Deduction / Mystery adventure
- **Development Scale:** Solo development
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
정답 선택지를 직접 알려주지 않고 제한된 정지 장면·명단·대화·공간 단서를 조합해 플레이어 스스로 인물과 사망 원인을 추론하게 만든 순수 Deduction 게임.

### Why This Game Matters
정보 설계, 추론 검증, UI를 통한 복잡한 정보 정리, Solo Scope에서 독창적 핵심 문제에 집중하는 방법의 강한 사례다.

### Primary Design Lessons
- 추리 게임의 핵심은 단서 수보다 플레이어가 스스로 결론을 만들어낼 수 있는 정보 구조다.
- 정답 검증을 묶음 단위로 지연하면 무작위 대입을 줄일 수 있다.
- 제한된 시각 스타일도 명확한 목적과 제작 제약을 해결하면 정체성이 된다.
- 하나의 독창적 문제를 깊게 해결하는 것이 많은 Feature보다 강한 USP가 될 수 있다.

### Primary Warning
정보를 숨기는 것과 추리를 만드는 것은 다르다. 필요한 단서가 논리적으로 연결되지 않으면 난해함만 남는다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 사건 현장을 복원해 누가 누구이며 어떤 운명을 맞았는지를 스스로 증명하는 보험 조사관이다.

### Design Pillars
- Logical Deduction
- Evidence Cross-Reference
- Delayed Validation
- Constraint-driven Presentation

### USP
사망 순간의 정지된 3D 장면을 자유롭게 관찰하고 명단·관계·공간 단서를 교차해 정답을 작성한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 관찰
- 장면 이동
- 명단 대조
- 단서 기록
- 신원 추론
- 사인 입력

### Core Loop
`사망 장면 발견 → 공간/대화 관찰 → 명단/다른 장면 교차 참조 → 가설 입력 → 여러 정답 단위 검증`

### Loop Strength
새 장면 하나가 기존 미해결 사건의 의미까지 바꿔 정보가 누적될수록 추론 네트워크가 확장된다.

## 4. Decision Design
### Primary Decisions
- 어떤 미해결 인물부터 추적할지
- 어떤 단서를 신뢰할지
- 가설을 언제 확정할지

### Meaningful Choice
전략적 자원 선택보다 정보 우선순위와 논리적 확신 수준이 핵심 선택이다.

### Information & Uncertainty
필요한 정보는 세계 안에 존재하지만 직접 정답 형태로 주어지지 않는다. 플레이어가 관계를 만들어야 한다.

## 5. Risk / Reward Structure
전통적 실패 비용은 낮다. 핵심 위험은 잘못된 가설과 정보 과부하다. 보상은 정답 검증과 전체 사건 구조가 갑자기 연결되는 통찰이다.

## 6. Progression Design
캐릭터 성장 대신 플레이어의 지식 그래프가 성장한다.

## 7. Economy & Resource Design
전통적 경제 없음. Attention과 정보 정리가 사실상의 제한 자원이다.

## 8. Difficulty & Failure Design
초기에는 명백한 사망 원인부터 시작해 신원·관계·간접 단서 비중이 증가한다.

## 9. Onboarding & Learning Curve
첫 사건들이 장면 관찰→명단→가설 입력의 문법을 가르친다.

## 10. Content & Variety
각 장면은 고유 제작이 필요하지만 동일 인물·공간·대사가 여러 추론에 재사용된다.

## 11. Replayability
정답을 알면 낮다. 대신 첫 플레이의 추론 밀도를 극대화한 1회 완결형 설계다.

## 12. UX & Information Design
책 형태의 명단과 사건 기록이 외부 메모 없이 복잡한 추론을 관리하도록 설계된다.

## 13. Player Motivation & Psychology
미스터리 해소, 통찰의 순간, 완전한 사건 재구성.

## 14. Scope & Production Efficiency
Lucas Pope의 공개 인터뷰는 기술·표현 제약 자체를 흥미로운 설계 문제로 다루는 태도를 보여준다.

## 15. What Worked
- 단서가 여러 사건에 동시에 쓰여 정보 콘텐츠의 밀도가 높다.
- 검증을 지연해 brute-force를 억제하면서 플레이어의 가설 형성은 자유롭게 둔다.

## 16. What Did Not Work / Limitations
- 정답을 알고 나면 재플레이 가치가 크게 떨어진다.
- 정보 설계 오류 하나가 전체 추론 경험을 무너뜨릴 수 있어 제작 난도가 높다.

## 17. Design Problem → Solution Analysis
**Problem:** 추리 게임에서 플레이어가 '선택지 중 정답 맞히기'가 아니라 실제 추론을 하게 하려면?  
**Solution:** 정답 문장을 주지 않고 여러 장면의 간접 정보를 교차하게 하며 검증을 지연한다.  
**Trade-off:** 정보 설계와 QA 난도가 매우 높다.

## 18. What This Game Teaches
- Deduction은 정보 부족이 아니라 정보 관계 설계에서 나온다.
- 정답 검증 방식도 Core Mechanic의 일부다.
- 낮은 재플레이를 허용하고 첫 경험 밀도를 극대화하는 전략도 가능하다.

## 19. What NOT to Copy
- 1-bit 비주얼
- 정답을 무조건 숨기기
- 난해한 단서

## 20. Solo Indie Developer Lessons
### Worth Learning
하나의 독창적 상호작용 문제에 제작 역량을 집중하고 나머지 시스템을 최소화하는 방식.

### Expensive to Reproduce
고밀도 단서 설계, 사건 간 논리 QA, 3D 장면 제작.

### Possible Simplification
인물 8~10명, 사건 5개 정도의 폐쇄 공간으로 단서 교차 구조부터 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Deduction, Information Design, Solo Dev, Mystery, Validation
- **Best Review Use:** 정보 설계 / 추리 / 조사 UI / 1회 완결형 Scope

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 추리 게임의 핵심은 단서 수보다 플레이어가 스스로 결론을 만들어낼 수 있는 정보 구조다.
- **Biggest Warning:** 정보를 숨기는 것과 추리를 만드는 것은 다르다. 필요한 단서가 논리적으로 연결되지 않으면 난해함만 남는다.
- **Best Reference For:** 정보 설계 / 추리 / 조사 UI / 1회 완결형 Scope
- **Core Design Principle:** Deduction은 정보 부족이 아니라 정보 관계 설계에서 나온다.

## 23. Final Assessment
### Design Strengths
- 순수한 추론 Agency
- 매우 높은 정보 밀도
- 독창적 USP

### Design Weaknesses
- 낮은 재플레이
- 높은 설계 QA 난도
- 진입 난도

### Most Transferable Lesson
Deduction은 정보 부족이 아니라 정보 관계 설계에서 나온다.

## 24. Sources & Evidence
- [Lucas Pope interview](https://www.gamedeveloper.com/design/for-lucas-pope-i-return-of-the-obra-dinn-i-was-a-bunch-of-appealing-design-problems) — Developer interview
- [Lucas Pope official development page](https://www.dukope.com/) — Official developer site

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-18 — Loop Hero

<!-- SOURCE_FILE: 18_Loop_Hero.md -->

# Game Design Case Study v1.0 — Loop Hero

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Four Quarters
- **Release:** 2021
- **Genre:** Roguelike / Auto-battler / Deckbuilding
- **Development Scale:** Four-person core team
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
주인공의 이동과 전투를 자동화하고 플레이어에게 길 위의 위험·보상 배치 권한을 줘 '내가 난이도를 설계하고 그 결과를 감당하는' 독특한 루프를 만든 게임.

### Why This Game Matters
자동 전투와 플레이어 Agency의 공존, 위험을 직접 배치하는 Risk/Reward, 작은 팀의 Jam→상용화 경로를 연구하기 좋다.

### Primary Design Lessons
- 직접 조작을 제거해도 플레이어가 환경과 위험을 설계하게 하면 Agency를 유지할 수 있다.
- 보상을 얻으려면 플레이어 스스로 위험을 추가해야 하는 구조는 Risk/Reward를 매우 선명하게 만든다.
- 타일 간 숨은 상호작용은 콘텐츠 하나의 재사용 가치를 높인다.
- 게임잼 프로토타입이 핵심 가설을 빠르게 검증하는 출발점이 될 수 있다.

### Primary Warning
자동 전투만 가져오면 관전 게임이 된다. 플레이어가 '어떤 위험을 언제 얼마나 추가할지' 결정하는 핵심 권한이 필요하다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 영웅을 직접 조종하지 않고, 영웅이 반복해서 걸을 세계와 위험을 배치해 성장 경로를 설계한다.

### Design Pillars
- Indirect Control
- Self-authored Risk
- Tile Synergy
- Loop Escalation

### USP
적을 피하는 대신 더 많은 보상을 위해 플레이어 자신이 적 생성 타일을 길에 놓는다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 타일 배치
- 장비 선택
- 덱 구성
- 철수 판단
- 기지 업그레이드

### Core Loop
`자동 순환/전투 → 카드·장비 획득 → 위험/보상 타일 배치 → 더 강한 적 → 더 좋은 보상 → 철수 또는 보스`

### Loop Strength
강해지려면 위험도 함께 키워야 해 플레이어가 매 Loop마다 스스로 난이도를 재설정한다.

## 4. Decision Design
### Primary Decisions
- 지금 위험 타일을 더 놓을지
- 안전하게 철수할지 다음 Loop를 돌지
- 어떤 타일 시너지를 만들지

### Meaningful Choice
보상 생성과 위험 생성이 같은 행동에 묶여 있어 성장 선택이 동시에 실패 가능성을 높인다.

### Information & Uncertainty
현재 루프와 타일은 보이지만 카드 드롭과 일부 타일 조합 효과는 발견형 정보다.

## 5. Risk / Reward Structure
사망 시 자원 손실, 과도한 적 생성, 잘못된 빌드가 위험이다. 보상은 장비·기지 자원·새 카드와 시너지 발견.

## 6. Progression Design
런 내부 장비 성장과 캠프의 영구 메타 성장이 결합된다.

## 7. Economy & Resource Design
타일이 사실상 위험-보상 통화이며, 기지 자원은 장기 업그레이드에 사용된다.

## 8. Difficulty & Failure Design
플레이어가 놓은 타일과 Loop 횟수에 따라 적이 강화되어 난이도의 일부를 스스로 생성한다.

## 9. Onboarding & Learning Curve
자동 이동 덕분에 기본 행동은 단순하지만 타일 시너지와 장비 비교는 점차 학습한다.

## 10. Content & Variety
타일·카드·클래스·장비 속성이 서로 겹치며 비교적 작은 제작 자산으로 많은 조합을 만든다.

## 11. Replayability
클래스·덱·타일 시너지와 메타 성장으로 높다.

## 12. UX & Information Design
자동 진행과 Pause 가능한 배치 판단을 분리해 실시간 압박과 전략 사고를 함께 제공한다.

## 13. Player Motivation & Psychology
시너지 발견, 위험 한계 시험, 기지 성장, 효율적 Loop 설계.

## 14. Scope & Production Efficiency
개발진 Postmortem에 따르면 Ludum Dare 프로토타입에서 시작해 약 1.5년간 개발되었으며 작은 팀의 실험적 Core Loop 상용화 사례다.

## 15. What Worked
- 위험과 보상 생성이 동일 행동에 묶여 선택의 의미가 즉시 드러난다.
- 자동화가 조작 부담을 줄이는 대신 세계 설계 판단을 강화한다.

## 16. What Did Not Work / Limitations
- 초반 반복 관전 시간이 지루하게 느껴질 수 있다.
- 숨은 타일 시너지가 지나치면 외부 위키 의존을 만들 수 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 자동 전투에서 플레이어가 수동적이라고 느끼지 않게 하려면?  
**Solution:** 전투가 아니라 전투 조건과 위험 밀도를 플레이어가 직접 설계하게 한다.  
**Trade-off:** 순간 전투 Agency는 낮아진다.

## 18. What This Game Teaches
- 자동화할 행동과 플레이어에게 남길 결정을 명확히 분리해야 한다.
- 위험과 보상을 같은 선택에 묶으면 Risk/Reward가 선명해진다.
- 시스템 간 조합은 작은 콘텐츠 풀의 수명을 늘린다.

## 19. What NOT to Copy
- 원형 Loop 맵
- 자동 전투 자체
- 숨은 조합을 과도하게 만드는 것

## 20. Solo Indie Developer Lessons
### Worth Learning
Jam 수준 핵심 루프를 먼저 만들고, 그 루프가 반복 가능한지 확인한 뒤 메타·콘텐츠를 추가하는 방식.

### Expensive to Reproduce
타일 조합 밸런스, 장비 속성 QA, 장기 메타 콘텐츠.

### Possible Simplification
타일 8개, 적 4종, 장비 슬롯 3개만으로 자기 생성 Risk/Reward를 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Indirect Control, Auto Battle, Risk Reward, Tile Synergy, Jam Prototype
- **Best Review Use:** 자동화 / 위험 설계 / 프로토타입 / 시스템 시너지

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 직접 조작을 제거해도 플레이어가 환경과 위험을 설계하게 하면 Agency를 유지할 수 있다.
- **Biggest Warning:** 자동 전투만 가져오면 관전 게임이 된다. 플레이어가 '어떤 위험을 언제 얼마나 추가할지' 결정하는 핵심 권한이 필요하다.
- **Best Reference For:** 자동화 / 위험 설계 / 프로토타입 / 시스템 시너지
- **Core Design Principle:** 자동화할 행동과 플레이어에게 남길 결정을 명확히 분리해야 한다.

## 23. Final Assessment
### Design Strengths
- 독창적 Agency 배분
- 명확한 Risk/Reward
- 높은 시스템 재사용

### Design Weaknesses
- 관전 피로
- 숨은 규칙
- 밸런스 조합 비용

### Most Transferable Lesson
자동화할 행동과 플레이어에게 남길 결정을 명확히 분리해야 한다.

## 24. Sources & Evidence
- [Loop Hero Postmortem](https://www.gamedeveloper.com/design/postmortem-loop-hero) — Developer postmortem
- [Developer interview](https://www.windowscentral.com/loop-hero-interview) — Developer interview

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-19 — Cultist Simulator

<!-- SOURCE_FILE: 19_Cultist_Simulator.md -->

# Game Design Case Study v1.0 — Cultist Simulator

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Weather Factory
- **Release:** 2018
- **Genre:** Narrative card simulation / Experimental strategy
- **Development Scale:** Small indie team
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
행동·인물·감정·지식·시간을 모두 카드와 슬롯으로 추상화해, 설명을 최소화한 채 플레이어가 규칙을 발견하는 실험적 시스템 내러티브.

### Why This Game Matters
카드 기반 운영 UI, 추상 상태 모델링, Discovery onboarding의 장단점, 저예산 실험 게임의 상업적 Scope를 검토하기 좋다.

### Primary Design Lessons
- 서로 다른 개념을 동일한 카드 문법으로 표현하면 UI와 콘텐츠 시스템을 재사용할 수 있다.
- 설명을 줄이고 발견을 보상으로 만들 수 있지만 대상 플레이어를 명확히 선택해야 한다.
- 저예산 게임은 모든 사람에게 친절하기보다 강한 정체성을 선택하는 전략도 가능하다.
- 실험적 규칙도 일관된 문법이 있으면 플레이어가 스스로 학습할 수 있다.

### Primary Warning
불친절함 자체는 깊이가 아니다. 발견 과정이 의미 있는 패턴 학습으로 이어지지 않으면 단순한 UX 실패가 된다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 금지된 지식을 탐구하는 인물로서 시간·직업·추종자·욕망을 카드로 조합해 비밀 조직을 성장시킨다.

### Design Pillars
- Card Grammar
- Discovery
- Systemic Narrative
- Deliberate Obscurity

### USP
사람·장소·감정·행동까지 같은 카드/슬롯 인터페이스로 표현한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 카드 배치
- 타이머 관리
- 조합 실험
- 추종자 관리
- 탐험
- 의식 수행

### Core Loop
`행동 슬롯 선택 → 카드 투입 → 시간 경과 → 결과 카드 획득/상태 변화 → 새 조합 발견 → 더 위험한 행동`

### Loop Strength
새 카드가 기존 슬롯과 다른 방식으로 결합되면서 플레이어의 가능한 행동 문법이 확장된다.

## 4. Decision Design
### Primary Decisions
- 제한된 시간 슬롯을 어디에 쓸지
- 위험한 지식 탐구를 계속할지
- 어떤 추종자/자원을 의식에 사용할지

### Meaningful Choice
시간과 카드가 여러 행동에서 경쟁하고, 결과를 완전히 알 수 없어 실험의 기회비용이 발생한다.

### Information & Uncertainty
핵심 규칙 일부를 의도적으로 설명하지 않아 플레이어가 카드 설명과 결과를 통해 학습한다.

## 5. Risk / Reward Structure
시간 부족, 질병, 수사, 자원 고갈과 패배 상태가 위험이다. 보상은 새 지식·추종자·의식·규칙 발견.

## 6. Progression Design
새 지식과 카드 조합이 행동 가능성을 확장한다. 지식 자체가 성장 자원이다.

## 7. Economy & Resource Design
시간 슬롯과 카드 상태가 핵심 경제다. 많은 카드가 유효기간을 가져 보유 자체가 관리 문제가 된다.

## 8. Difficulty & Failure Design
시스템 이해 부족과 여러 타이머가 동시에 압박하면서 상승한다.

## 9. Onboarding & Learning Curve
의도적으로 최소 설명을 택해 발견을 경험으로 만들지만 진입 이탈 위험이 크다.

## 10. Content & Variety
카드 문법 하나로 대량 텍스트·상태·행동을 표현해 제작 시스템을 통일한다.

## 11. Replayability
다른 욕망/승리 경로와 발견 과정으로 중상 수준.

## 12. UX & Information Design
일관된 카드 문법은 강점이지만 테이블이 복잡해지면 시각적 관리 부담이 급증한다.

## 13. Player Motivation & Psychology
금지된 규칙 발견, 미스터리, 시스템 숙련, 비밀 지식 축적.

## 14. Scope & Production Efficiency
GDC 자료에서 제작 기간 1년 미만, 총 제작비 20만 달러 미만의 의도적 저예산 실험 프로젝트였다고 설명한다.

## 15. What Worked
- 단일 카드 문법이 다양한 개념을 같은 제작 파이프라인으로 처리한다.
- 강한 정체성을 위해 대상 플레이어를 의도적으로 좁힌다.

## 16. What Did Not Work / Limitations
- 높은 이탈률을 감수하는 불친절한 온보딩.
- 카드가 많아지면 테이블 관리가 실제 플레이보다 번거로워질 수 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 작은 팀이 복잡한 세계와 상태를 많은 전용 UI 없이 표현하려면?  
**Solution:** 거의 모든 개념을 카드·슬롯·타이머라는 공통 문법으로 추상화한다.  
**Trade-off:** 가독성과 온보딩 부담.

## 18. What This Game Teaches
- 공통 UI 문법은 콘텐츠 제작과 시스템 확장을 동시에 단순화할 수 있다.
- 의도적 난해함은 명확한 타깃과 발견 보상이 있을 때만 유효하다.
- 작은 프로젝트는 보편성보다 독창성을 선택할 수 있다.

## 19. What NOT to Copy
- 튜토리얼 제거
- 카드 UI 자체
- 난해한 텍스트를 깊이로 착각

## 20. Solo Indie Developer Lessons
### Worth Learning
여러 시스템을 하나의 데이터/인터페이스 문법으로 통일하는 방식은 구현 효율이 높다.

### Expensive to Reproduce
대량 텍스트, 상태 조합 QA, 복잡한 UX polish.

### Possible Simplification
카드 30장, 행동 슬롯 4개로 공통 문법이 여러 종류의 상태를 충분히 표현하는지 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** Card UI, Systemic Narrative, Discovery, Experimental, Low Budget
- **Best Review Use:** 카드형 운영 / 공통 UI 문법 / 발견형 온보딩 / 실험 게임

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 서로 다른 개념을 동일한 카드 문법으로 표현하면 UI와 콘텐츠 시스템을 재사용할 수 있다.
- **Biggest Warning:** 불친절함 자체는 깊이가 아니다. 발견 과정이 의미 있는 패턴 학습으로 이어지지 않으면 단순한 UX 실패가 된다.
- **Best Reference For:** 카드형 운영 / 공통 UI 문법 / 발견형 온보딩 / 실험 게임
- **Core Design Principle:** 공통 UI 문법은 콘텐츠 제작과 시스템 확장을 동시에 단순화할 수 있다.

## 23. Final Assessment
### Design Strengths
- 강한 독창성
- 높은 시스템 재사용
- 낮은 전용 화면 의존

### Design Weaknesses
- 불친절한 온보딩
- 높은 관리 피로
- 좁은 타깃

### Most Transferable Lesson
공통 UI 문법은 콘텐츠 제작과 시스템 확장을 동시에 단순화할 수 있다.

## 24. Sources & Evidence
- [GDC Cultist Simulator](https://www.gdcvault.com/play/1025794/-Cultist-Simulator-Designing-an) — Developer GDC

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-20 — Dicey Dungeons

<!-- SOURCE_FILE: 20_Dicey_Dungeons.md -->

# Game Design Case Study v1.0 — Dicey Dungeons

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Terry Cavanagh with collaborators
- **Release:** 2019
- **Genre:** Dice deckbuilder / Turn-based roguelike
- **Development Scale:** Solo-led small-team production
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
주사위라는 명시적 RNG를 장비 슬롯의 입력값으로 바꾸고 캐릭터마다 같은 규칙을 전혀 다른 방식으로 해석하게 만들어, 불확실성을 읽고 조작하는 전술 게임.

### Why This Game Matters
RNG 통제, 캐릭터별 규칙 변형, 작은 Core System을 여러 플레이스타일로 확장하는 방법에 유용하다.

### Primary Design Lessons
- 랜덤을 숨기기보다 눈앞에 보여주고 플레이어에게 변환·재굴림·분할 수단을 주면 전략 자원이 된다.
- 같은 Core Mechanic도 캐릭터별 제약 규칙을 바꾸면 거의 다른 게임처럼 느껴질 수 있다.
- 두 종류의 RNG가 겹쳐 혼란스러우면 하나를 고정해 전략성을 회복할 수 있다.
- Game Jam 프로토타입은 시스템 가능성을 빠르게 발견하는 좋은 방법이다.

### Primary Warning
RNG의 양이 아니라 RNG를 조작할 수 있는 선택이 중요하다. 확률만 늘리면 통제감이 사라진다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 매 턴 굴린 주사위를 장비에 배치해 제한된 결과를 최대한 효율적으로 변환한다.

### Design Pillars
- Visible Randomness
- RNG Manipulation
- Character Rule Variants
- Compact Combat

### USP
주사위 결과가 행동 가능성을 제한하지만 각 캐릭터가 그 불확실성을 서로 다른 방식으로 다룬다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 주사위 굴림
- 장비 배치
- 주사위 변환
- 장비 선택
- 경로 선택

### Core Loop
`전투 → 주사위 배치/조작 → 적 처치 → 장비/업그레이드 → 다음 전투 → 에피소드 규칙 변화`

### Loop Strength
매 턴 주사위가 다르지만 장비는 비교적 고정되어 '주어진 입력을 현재 도구로 어떻게 처리할지'가 반복 판단이 된다.

## 4. Decision Design
### Primary Decisions
- 높은 주사위를 공격/방어/유틸리티 어디에 쓸지
- RNG 조작 장비를 언제 사용할지
- 어떤 장비 구성을 유지할지

### Meaningful Choice
랜덤 결과가 먼저 공개되고 이후 플레이어가 배치하기 때문에 확률 이전보다 확률 이후의 대응 판단이 중요하다.

### Information & Uncertainty
현재 주사위와 장비 효과는 완전히 보인다. 다음 굴림과 적 행동 일부가 불확실하다.

## 5. Risk / Reward Structure
나쁜 주사위 분포와 HP 손실이 위험이며, 보상은 장비·업그레이드·새 규칙 숙련.

## 6. Progression Design
런 내부 장비 강화와 캐릭터별 Episode 해금이 결합된다.

## 7. Economy & Resource Design
주사위 눈 자체가 매 턴 소비 가능한 행동 자원이다. 슬롯 조건이 자원 가치를 상황별로 바꾼다.

## 8. Difficulty & Failure Design
캐릭터와 Episode마다 규칙 변형을 통해 같은 Core System을 재시험한다.

## 9. Onboarding & Learning Curve
주사위 숫자를 장비 칸에 넣는 직관적 행위로 시작해 조작 규칙을 점진적으로 추가한다.

## 10. Content & Variety
장비와 캐릭터 규칙을 조합해 적은 기본 시스템으로 많은 플레이스타일을 만든다.

## 11. Replayability
6개 캐릭터와 Episode 변형으로 높다.

## 12. UX & Information Design
모든 현재 RNG 결과를 테이블 위에 보여주기 때문에 실패 원인을 읽기 쉽다.

## 13. Player Motivation & Psychology
나쁜 운을 영리하게 해결하는 만족, 캐릭터 숙련, 장비 조합.

## 14. Scope & Production Efficiency
공식 자료에 따르면 7-Day Roguelike 프로토타입에서 시작했고, 이후 동일 메커니즘을 캐릭터별로 확장했다.

## 15. What Worked
- 랜덤 결과를 먼저 공개해 RNG를 계획 가능한 자원으로 바꾼다.
- 캐릭터별 규칙 변형으로 콘텐츠 자산을 재사용하면서 플레이 감각을 크게 바꾼다.

## 16. What Did Not Work / Limitations
- 일부 전투는 선택보다 주사위 결과 영향이 크게 느껴질 수 있다.
- 캐릭터별 규칙이 늘수록 별도 밸런스 비용이 커진다.

## 17. Design Problem → Solution Analysis
**Problem:** RNG를 유지하면서 플레이어가 운에 끌려간다고 느끼지 않게 하려면?  
**Solution:** 랜덤 결과를 행동 전에 공개하고 그것을 변환하는 도구를 제공한다.  
**Trade-off:** 변환 수단이 너무 강하면 RNG 의미가 사라진다.

## 18. What This Game Teaches
- RNG는 결과 공개 시점과 조작 가능성이 설계의 핵심이다.
- 하나의 Core Mechanic을 규칙 변형으로 여러 캐릭터에 재사용할 수 있다.
- 복수 RNG가 전략을 흐리면 일부 변수를 고정하는 편이 낫다.

## 19. What NOT to Copy
- 주사위 테마
- 캐릭터 수
- 랜덤을 단순히 눈에 보이게만 하는 것

## 20. Solo Indie Developer Lessons
### Worth Learning
작은 전투 규칙 하나를 Jam에서 검증한 뒤 캐릭터별 규칙 변형으로 확장하는 순서.

### Expensive to Reproduce
캐릭터별 밸런스, 장비 조합 QA, 아트/음악 협업.

### Possible Simplification
캐릭터 2명, 장비 12개, 주사위 조작 3종으로 통제 가능한 RNG인지 검증한다.

## 21. Reference Comparison Tags
- **Design Tags:** RNG, Dice, Rule Variants, Roguelike, Game Jam
- **Best Review Use:** RNG 설계 / 캐릭터 차별화 / 전투 규칙 / 프로토타입

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 랜덤을 숨기기보다 눈앞에 보여주고 플레이어에게 변환·재굴림·분할 수단을 주면 전략 자원이 된다.
- **Biggest Warning:** RNG의 양이 아니라 RNG를 조작할 수 있는 선택이 중요하다. 확률만 늘리면 통제감이 사라진다.
- **Best Reference For:** RNG 설계 / 캐릭터 차별화 / 전투 규칙 / 프로토타입
- **Core Design Principle:** RNG는 결과 공개 시점과 조작 가능성이 설계의 핵심이다.

## 23. Final Assessment
### Design Strengths
- 높은 RNG 가독성
- 효율적 규칙 재사용
- 명확한 캐릭터 차별화

### Design Weaknesses
- 운 영향 체감
- 캐릭터별 밸런스 비용
- 장기 조합 한계

### Most Transferable Lesson
RNG는 결과 공개 시점과 조작 가능성이 설계의 핵심이다.

## 24. Sources & Evidence
- [Official presskit](https://terrycavanaghgames.com/dice/presskit/xbox/) — Developer official
- [Road to the IGF](https://www.gamedeveloper.com/business/road-to-the-igf-cavanagh-houston-dobbe-s-i-dicey-dungeons-i-) — Developer interview

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-21 — Mark of the Ninja

<!-- SOURCE_FILE: 21_Mark_of_the_Ninja.md -->

# Game Design Case Study v1.0 — Mark of the Ninja

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Klei Entertainment
- **Release:** 2012
- **Genre:** 2D stealth action
- **Development Scale:** Indie studio
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
스텔스에서 플레이어가 왜 발각됐는지 이해하도록 소리·시야·적 반응을 시각화해, 정보 가독성을 난이도와 분리한 사례.

### Why This Game Matters
잠입과 모니터링에서 정보 표현 자체가 공정성과 Player Agency를 만드는 방식을 연구하기 좋다.

### Primary Design Lessons
- 스텔스 난이도는 정보를 숨기는 데서 만들 필요가 없다.
- 소리와 시야를 시각화하면 플레이어가 계획하고 실패 원인을 학습할 수 있다.
- 핵심 판타지에 맞지 않는 장르 관습은 제거할 수 있다.

### Primary Warning
시야선과 소리 원을 그대로 복사하기보다 어떤 정보가 판단에 필수인지 먼저 정의해야 한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어가 실제 닌자처럼 적을 관찰하고 그림자·소리를 이용해 통제하는 판타지.

### Design Pillars
- Readable Stealth
- Ninja Fantasy
- Feedback

### USP
정보를 숨기지 않는 2D 스텔스.

## 3. Core Gameplay Structure
### Core Player Verbs
- 관찰
- 은신
- 소음 유도
- 기절/처치
- 경로 선택

### Core Loop
`관찰 → 경로 계획 → 잠입/교란 → 적 반응 → 재계획 → 목표/탈출`

### Loop Strength
정보 가독성이 높아 실패가 규칙 오해보다 판단 결과로 읽힌다.

## 4. Decision Design
### Primary Decisions
- 비살상/살상 접근
- 위험 경로와 안전 경로
- 교란 도구 사용 시점

### Meaningful Choice
명확한 피드백 덕분에 여러 접근법의 결과를 비교할 수 있다.

### Information & Uncertainty
시야·소음 정보는 공개되고 미탐색 공간만 불확실하다.

## 5. Risk / Reward Structure
발각과 전투가 위험이며 목표 달성·점수·완벽 잠입이 보상이다.

## 6. Progression Design
도구와 능력 해금이 접근법을 확장한다.

## 7. Economy & Resource Design
도구 사용 횟수와 위치/시간이 주요 제한 자원이다.

## 8. Difficulty & Failure Design
적 종류와 공간 조합으로 복잡도가 상승한다.

## 9. Onboarding & Learning Curve
초기부터 시야와 소리를 시각적으로 설명한다.

## 10. Content & Variety
수작업 레벨 비용은 높지만 적/도구 규칙은 재사용된다.

## 11. Replayability
다른 스타일/점수 목표로 중상.

## 12. UX & Information Design
시야·소음·경보를 강하게 시각화한다.

## 13. Player Motivation & Psychology
통제감, 완벽한 잠입, 다양한 해결법.

## 14. Scope & Production Efficiency
2D로 잠입 공간을 단순화했지만 레벨 제작은 여전히 비싸다.

## 15. What Worked
- 가독성 높은 정보가 스텔스의 공정성을 강화한다.
- 닌자 판타지를 기능 선택의 기준으로 삼았다.

## 16. What Did Not Work / Limitations
- 수작업 레벨 비용
- 정밀 액션과 정보 표시의 균형

## 17. Design Problem → Solution Analysis
**Problem:** 스텔스 실패가 '왜 들켰는지 모르겠다'로 느껴지는 문제.  
**Solution:** 소리·시야·적 상태를 명시적으로 시각화한다.  
**Trade-off:** 현실적 불확실성은 줄어든다.

## 18. What This Game Teaches
- 필수 정보 공개는 난이도를 낮추는 것이 아니라 판단 품질을 높인다.
- Player Fantasy는 Feature 우선순위 기준이 될 수 있다.

## 19. What NOT to Copy
- 시야 원 UI 자체
- 모든 숨은 정보를 공개
- 닌자 테마

## 20. Solo Indie Developer Lessons
### Worth Learning
모니터링/잠입 프로토타입에서 핵심 정보 표시 규칙을 먼저 만드는 방식.

### Expensive to Reproduce
수작업 레벨과 애니메이션.

### Possible Simplification
한 방, 경비 2종, 소음 도구 2개로 정보 가독성을 검증.

## 21. Reference Comparison Tags
- **Design Tags:** Stealth, Information, Feedback, 2D
- **Best Review Use:** 잠입 / 모니터링 / 정보 표시

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 스텔스 난이도는 정보를 숨기는 데서 만들 필요가 없다.
- **Biggest Warning:** 시야선과 소리 원을 그대로 복사하기보다 어떤 정보가 판단에 필수인지 먼저 정의해야 한다.
- **Best Reference For:** 잠입 / 모니터링 / 정보 표시
- **Core Design Principle:** 필수 정보 공개는 난이도를 낮추는 것이 아니라 판단 품질을 높인다.

## 23. Final Assessment
### Design Strengths
- 높은 공정성
- 강한 판타지 일치

### Design Weaknesses
- 레벨 제작비
- 액션 구현 비용

### Most Transferable Lesson
필수 정보 공개는 난이도를 낮추는 것이 아니라 판단 품질을 높인다.

## 24. Sources & Evidence
- [Developer Postmortem](https://www.gamedeveloper.com/design/classic-postmortem-klei-entertainment-s-i-mark-of-the-ninja-i-) — Developer postmortem

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-22 — Stacklands

<!-- SOURCE_FILE: 22_Stacklands.md -->

# Game Design Case Study v1.0 — Stacklands

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Sokpop Collective
- **Release:** 2022
- **Genre:** Card-based village builder
- **Development Scale:** Tiny indie team
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
마을·주민·자원·건물을 모두 카드로 표현하고 카드를 겹치는 단순 조작으로 생산 체인과 사건을 만든 초소형 경영 게임.

### Why This Game Matters
공통 UI 문법으로 복잡한 경영 시스템을 축소하는 데 좋은 보조 사례다.

### Primary Design Lessons
- 오브젝트 종류가 달라도 같은 조작 문법으로 통일하면 구현과 학습 비용을 줄일 수 있다.
- 공간 배치 자체를 생산 규칙으로 만들면 별도 메뉴를 줄일 수 있다.
- 작은 콘텐츠도 조합 레시피로 확장할 수 있다.

### Primary Warning
카드화 자체가 Scope 해결책은 아니다. 카드 간 조합 규칙이 읽기 쉬워야 한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 카드 더미를 정리하며 작은 마을의 생산망을 구축한다.

### Design Pillars
- Common Interaction Grammar
- Compact Economy
- Spatial Cards

### USP
드래그·겹치기 하나로 대부분의 경영 행동을 처리.

## 3. Core Gameplay Structure
### Core Player Verbs
- 카드 이동
- 겹치기
- 생산
- 판매
- 전투

### Core Loop
`카드 획득 → 조합/생산 → 자원 증가 → 새 팩/레시피 → 더 복잡한 마을`

### Loop Strength
같은 드래그 입력이 생산·건설·전투에 재사용된다.

## 4. Decision Design
### Primary Decisions
- 어떤 생산 체인을 우선할지
- 공간과 인력을 어디에 배치할지
- 카드를 팔지 보존할지

### Meaningful Choice
단순 입력에 여러 경제 결과가 연결된다.

### Information & Uncertainty
레시피 발견과 다음 팩 결과에 불확실성이 있다.

## 5. Risk / Reward Structure
식량 부족과 적 공격이 위험, 새 카드·레시피가 보상.

## 6. Progression Design
새 팩과 레시피가 생산 가능성을 넓힌다.

## 7. Economy & Resource Design
카드 자체가 자원·시설·인력 역할을 겸한다.

## 8. Difficulty & Failure Design
새 레시피와 적이 복잡도를 높인다.

## 9. Onboarding & Learning Curve
드래그/겹치기에서 시작해 레시피를 발견한다.

## 10. Content & Variety
카드 데이터와 공통 조작으로 제작 효율이 높다.

## 11. Replayability
레시피/런 구조로 중상.

## 12. UX & Information Design
물리적 카드 더미가 상태와 공간을 동시에 표현한다.

## 13. Player Motivation & Psychology
정리, 발견, 생산망 확장.

## 14. Scope & Production Efficiency
공통 카드 시스템 덕분에 전용 UI가 적다.

## 15. What Worked
- 공통 조작 문법으로 여러 시스템을 처리한다.
- 카드 조합이 작은 콘텐츠 풀을 확장한다.

## 16. What Did Not Work / Limitations
- 카드가 많아지면 화면 정리가 피로해진다.
- 복잡한 자동화에는 카드 UI가 한계가 있다.

## 17. Design Problem → Solution Analysis
**Problem:** 작은 팀이 경영게임의 많은 오브젝트와 화면을 어떻게 줄일 것인가?  
**Solution:** 모든 오브젝트를 카드로 통일하고 겹치기를 공통 동사로 사용한다.  
**Trade-off:** 후반 화면 혼잡.

## 18. What This Game Teaches
- 공통 상호작용 문법은 제작비와 온보딩을 동시에 줄인다.
- 공간 UI 자체가 경제 시스템이 될 수 있다.

## 19. What NOT to Copy
- 카드 그래픽 자체
- 레시피 수 경쟁

## 20. Solo Indie Developer Lessons
### Worth Learning
여러 종류의 운영 객체를 하나의 Prefab/Data 구조로 통일하는 발상.

### Expensive to Reproduce
후반 UX와 대량 조합 QA.

### Possible Simplification
카드 20장과 레시피 10개로 공통 문법을 검증.

## 21. Reference Comparison Tags
- **Design Tags:** Card UI, Management, Common Grammar, Scope
- **Best Review Use:** 경영 UI / 데이터 구조 / Scope

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 오브젝트 종류가 달라도 같은 조작 문법으로 통일하면 구현과 학습 비용을 줄일 수 있다.
- **Biggest Warning:** 카드화 자체가 Scope 해결책은 아니다. 카드 간 조합 규칙이 읽기 쉬워야 한다.
- **Best Reference For:** 경영 UI / 데이터 구조 / Scope
- **Core Design Principle:** 공통 상호작용 문법은 제작비와 온보딩을 동시에 줄인다.

## 23. Final Assessment
### Design Strengths
- 높은 구현 효율
- 낮은 조작 복잡도

### Design Weaknesses
- 후반 화면 혼잡
- 자동화 한계

### Most Transferable Lesson
공통 상호작용 문법은 제작비와 온보딩을 동시에 줄인다.

## 24. Sources & Evidence
- [Official Sokpop page](https://sokpop.co/games/stacklands) — Official developer page

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-23 — Citizen Sleeper

<!-- SOURCE_FILE: 23_Citizen_Sleeper.md -->

# Game Design Case Study v1.0 — Citizen Sleeper

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Jump Over the Age / Gareth Damian Martin
- **Release:** 2022
- **Genre:** Narrative RPG / Dice allocation
- **Development Scale:** Solo-led narrative development with collaborators
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
매일 굴린 주사위를 노동·관계·생존 행동에 배분해, 텍스트 RPG의 선택을 시간과 자원 기회비용에 연결한 내러티브 시스템.

### Why This Game Matters
텍스트 이벤트를 단순 대화 선택이 아니라 일정·자원 배분 게임으로 만드는 데 유용하다.

### Primary Design Lessons
- 텍스트 선택에 제한 행동 자원을 붙이면 서사 선택이 전략 선택이 된다.
- 관계 퀘스트를 타이머와 자원에 연결하면 일상 루틴과 장기 목표가 생긴다.
- 주사위는 성공 확률보다 하루의 행동 가능성을 형성하는 자원으로도 쓸 수 있다.

### Primary Warning
타이머를 많이 넣으면 서사 몰입보다 일정표 관리가 앞설 수 있다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 붕괴하는 인공 신체를 유지하며 우주 정거장에서 관계와 생존 기반을 만든다.

### Design Pillars
- Narrative Economy
- Dice Allocation
- Relationship Progress

### USP
주사위 배분으로 일상 생존과 인간관계 서사를 같은 행동 체계에 묶는다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 주사위 배치
- 대화
- 일하기
- 자원 사용
- 관계 진행

### Core Loop
`하루 시작/주사위 → 행동 슬롯 배분 → 자원/관계 변화 → 이벤트/Clock 진행 → 다음 날`

### Loop Strength
매일 제한된 주사위가 모든 목표에서 경쟁해 텍스트 선택에 기회비용을 준다.

## 4. Decision Design
### Primary Decisions
- 생존 자원과 관계 중 어디에 행동을 쓸지
- 좋은 주사위를 안전한 일과 중요한 위험 행동 중 어디에 배치할지

### Meaningful Choice
서사적 관심과 생존 효율이 같은 행동 자원을 두고 경쟁한다.

### Information & Uncertainty
행동 성공 가능성은 주사위와 슬롯을 통해 비교적 명확하다.

## 5. Risk / Reward Structure
상태 악화·돈 부족·시간 제한이 위험, 관계·안정·새 서사가 보상.

## 6. Progression Design
스킬과 관계/스토리 Clock이 장기 진행을 만든다.

## 7. Economy & Resource Design
주사위, 돈, 상태와 시간 Clock이 핵심 자원.

## 8. Difficulty & Failure Design
초기 생존 압박 후 관계와 장기 목표가 확장된다.

## 9. Onboarding & Learning Curve
소수 행동부터 시작해 공간 노드를 열어간다.

## 10. Content & Variety
텍스트·초상·지도 노드 중심이라 3D 제작비는 낮지만 작문량이 크다.

## 11. Replayability
분기와 관계 경로로 중간.

## 12. UX & Information Design
정거장을 노드 지도와 Clock으로 추상화한다.

## 13. Player Motivation & Psychology
관계 형성, 생존 안정, 정체성 선택.

## 14. Scope & Production Efficiency
그래픽 Scope는 통제되지만 고품질 텍스트가 핵심 제작비다.

## 15. What Worked
- 주사위가 서사 행동의 Opportunity Cost를 만든다.
- Clock이 장기 서사를 UI상에서 추적 가능하게 한다.

## 16. What Did Not Work / Limitations
- 후반 자원 압박이 약해지면 시스템 긴장이 감소할 수 있다.
- 대량 작문 비용

## 17. Design Problem → Solution Analysis
**Problem:** 텍스트 RPG의 선택을 단순 분기 감상 이상으로 만들려면?  
**Solution:** 하루 행동 자원을 모든 관계·생존·스토리 선택이 공유하게 한다.  
**Trade-off:** 일정 관리가 서사보다 앞설 위험.

## 18. What This Game Teaches
- 서사 선택에도 실제 Opportunity Cost가 필요할 수 있다.
- 장기 서사 상태를 시각적 Clock으로 표현하면 진행 기대가 명확해진다.

## 19. What NOT to Copy
- 주사위 UI 자체
- 모든 퀘스트에 타이머

## 20. Solo Indie Developer Lessons
### Worth Learning
텍스트 게임에서 행동 포인트와 관계 상태를 공통 시스템으로 묶는 방식.

### Expensive to Reproduce
작문·편집·분기 QA.

### Possible Simplification
노드 6개, 관계 3명, 하루 주사위 3개로 선택 충돌을 검증.

## 21. Reference Comparison Tags
- **Design Tags:** Narrative RPG, Dice Allocation, Clock, Relationship
- **Best Review Use:** 텍스트 게임 / 일정 / 관계 / 행동 자원

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 텍스트 선택에 제한 행동 자원을 붙이면 서사 선택이 전략 선택이 된다.
- **Biggest Warning:** 타이머를 많이 넣으면 서사 몰입보다 일정표 관리가 앞설 수 있다.
- **Best Reference For:** 텍스트 게임 / 일정 / 관계 / 행동 자원
- **Core Design Principle:** 서사 선택에도 실제 Opportunity Cost가 필요할 수 있다.

## 23. Final Assessment
### Design Strengths
- 강한 시스템-서사 연결
- 명확한 장기 진행

### Design Weaknesses
- 작문 비용
- 후반 압박 약화 가능

### Most Transferable Lesson
서사 선택에도 실제 Opportunity Cost가 필요할 수 있다.

## 24. Sources & Evidence
- [Official game site](https://www.fellowtraveller.games/citizen-sleeper) — Official publisher/game page

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY



---

# REF-24 — Dorfromantik

<!-- SOURCE_FILE: 24_Dorfromantik.md -->

# Game Design Case Study v1.0 — Dorfromantik

> **Studio Game Design Reviewer — Secondary Reference Library**  
> 목적: 1차 Reference의 공백을 보완하고, 신규 기획의 문제와 유사한 사례를 `문제 → 해결 원리 → 조건 → 트레이드오프` 단위로 비교한다.

## 0. Document Information
- **Developer:** Toukana Interactive
- **Release:** 2022
- **Genre:** Tile placement / Puzzle / Relaxing strategy
- **Development Scale:** Small indie team
- **Analysis Date:** 2026-08-14
- **Version:** 1.0

## 1. Executive Summary
### One-Sentence Design Summary
육각 타일을 하나씩 배치하는 단순 규칙에 연결 보너스·퀘스트·제한 타일 공급을 얹어 편안함과 장기 최적화를 동시에 만든 퍼즐.

### Why This Game Matters
저스트레스 게임에서도 Meaningful Choice와 장기 목표를 만드는 방법을 검토하기 좋다.

### Primary Design Lessons
- 실패 압박을 낮춰도 제한 자원과 공간 기회비용으로 깊이를 만들 수 있다.
- 한 번 놓은 타일이 미래 선택 공간을 바꾸면 단순 배치가 장기 전략이 된다.
- 미학적 만족과 점수 최적화를 같은 행동에 결합할 수 있다.

### Primary Warning
편안한 분위기와 낮은 난이도를 동일시하면 안 된다. 숨은 장기 기회비용은 충분히 존재한다.

## 2. Game Overview
### Core Concept / Player Fantasy
플레이어는 풍경 타일을 이어 아름다운 세계를 만들면서 타일 공급을 연장하고 점수를 높인다.

### Design Pillars
- Relaxing Strategy
- Spatial Opportunity Cost
- Aesthetic Reward

### USP
같은 타일 배치가 퍼즐 점수와 풍경 창작을 동시에 진행한다.

## 3. Core Gameplay Structure
### Core Player Verbs
- 타일 회전
- 배치
- 연결 계획
- 퀘스트 완성

### Core Loop
`타일 획득 → 배치 → 연결/퀘스트 → 추가 타일 → 더 큰 지도`

### Loop Strength
배치 하나가 현재 점수와 미래 연결 가능성을 동시에 바꾼다.

## 4. Decision Design
### Primary Decisions
- 완벽 연결과 미래 공간 확보 중 선택
- 퀘스트를 위해 배치를 왜곡할지

### Meaningful Choice
낮은 압박 속에서도 되돌릴 수 없는 공간 선택이 기회비용을 만든다.

### Information & Uncertainty
다음 타일 순서가 제한적으로 불확실하다.

## 5. Risk / Reward Structure
타일 소진이 실패, 추가 타일·점수·아름다운 지도가 보상.

## 6. Progression Design
해금과 숙련이 중심이며 강한 수직 성장은 없다.

## 7. Economy & Resource Design
타일 공급 자체가 핵심 자원.

## 8. Difficulty & Failure Design
지도 확장과 퀘스트 요구가 자연스럽게 계획 난도를 높인다.

## 9. Onboarding & Learning Curve
회전/배치만으로 시작해 연결 규칙을 학습한다.

## 10. Content & Variety
모듈 타일 재조합으로 높은 시각 재사용성을 가진다.

## 11. Replayability
절차적 타일 순서와 점수로 높음.

## 12. UX & Information Design
최소 HUD와 강한 공간 피드백.

## 13. Player Motivation & Psychology
정리감, 아름다움, 점수, 장기 집중.

## 14. Scope & Production Efficiency
모듈 타일 제작은 효율적이지만 연결 아트의 기술적 polish가 필요하다.

## 15. What Worked
- 저스트레스와 전략 깊이가 양립한다.
- 미학적 결과가 시스템 보상과 같은 행동에서 발생한다.

## 16. What Did Not Work / Limitations
- 장기 세션에서 목표가 단조로울 수 있다.
- 콘텐츠 확장은 타일 규칙 차별화가 필요하다.

## 17. Design Problem → Solution Analysis
**Problem:** 편안한 게임에서 강한 실패 압박 없이 선택을 의미 있게 만드는 법.  
**Solution:** 되돌리기 어려운 공간 배치와 제한 타일 공급으로 장기 기회비용을 만든다.  
**Trade-off:** 긴장감은 낮다.

## 18. What This Game Teaches
- Meaningful Choice는 높은 처벌 없이도 기회비용으로 만들 수 있다.
- 미학적 보상과 시스템 보상을 통합할 수 있다.

## 19. What NOT to Copy
- 육각 타일 자체
- Cozy 아트만 모방

## 20. Solo Indie Developer Lessons
### Worth Learning
작은 모듈 자산을 재조합해 높은 콘텐츠 효율을 만드는 방식.

### Expensive to Reproduce
연결형 타일 아트와 procedural QA.

### Possible Simplification
타일 12종, 퀘스트 3종으로 공간 기회비용을 검증.

## 21. Reference Comparison Tags
- **Design Tags:** Cozy, Tile Placement, Spatial Strategy, Low Stress
- **Best Review Use:** 저스트레스 경영 / 공간 배치 / 모듈 콘텐츠

## 22. Reviewer Quick Reference
- **Strongest Lesson:** 실패 압박을 낮춰도 제한 자원과 공간 기회비용으로 깊이를 만들 수 있다.
- **Biggest Warning:** 편안한 분위기와 낮은 난이도를 동일시하면 안 된다. 숨은 장기 기회비용은 충분히 존재한다.
- **Best Reference For:** 저스트레스 경영 / 공간 배치 / 모듈 콘텐츠
- **Core Design Principle:** Meaningful Choice는 높은 처벌 없이도 기회비용으로 만들 수 있다.

## 23. Final Assessment
### Design Strengths
- 낮은 진입 장벽
- 높은 모듈 재사용

### Design Weaknesses
- 장기 목표 단조로움
- 공간 규칙 확장 한계

### Most Transferable Lesson
Meaningful Choice는 높은 처벌 없이도 기회비용으로 만들 수 있다.

## 24. Sources & Evidence
- [Official Toukana page](https://www.toukana.com/dorfromantik) — Official developer page

> 개발자 Postmortem / GDC / 공식 개발자 자료를 우선한다. 분석적 추론은 공개 사실과 구분한다.

## 25. Confidence & Unknowns
- **High Confidence:** 공개된 Core Loop와 공식/개발자 자료에서 직접 확인되는 제작·설계 방향.
- **Medium Confidence:** 시스템이 플레이어 심리, 반복성, Scope에 미치는 영향에 대한 분석.
- **Low Confidence / Inferred:** 공개되지 않은 내부 의도, 세부 제작 공수, 폐기된 프로토타입의 정확한 영향.
- **Unknown:** 비공개 예산·세부 KPI·전체 QA 비용.

# END OF CASE STUDY

