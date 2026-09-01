# Studio Game Design Reviewer — 3차 — Solo / Micro Production Reference
> 프로젝트 소스 업로드용 통합 Reference 문서
> 각 Case Study의 원문 구조를 유지하며 `REF-XX` 경계로 분리했다.
---


---

# REF-25 — Buckshot Roulette

<!-- SOURCE_FILE: 25_Buckshot_Roulette.md -->

# Solo / Micro Indie Production Case Study — Buckshot Roulette

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Mike Klubnika
- **Core Development Scale:** 1인
- **Engine / Stack:** Godot
- **Primary Review Axis:** 극소 Scope / Hook / 반복 완성
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
16개의 소형 게임을 먼저 완성한 뒤, 기존 앤솔로지의 shotgun roulette 아이디어를 떼어 독립작으로 만들었다. Tabletop Simulator로 핵심 규칙을 먼저 시험했고 15~20분짜리 경험에 집중했다.

## 2. Production Model
짧은 게임 반복 완성 → 강한 Hook → 작은 상용작으로 연결하는 생산 모델.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`1인` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
짧은 게임이라고 제작비가 자동으로 낮은 것은 아니다. 독특한 3D 미술·사운드·연출 역량이 Hook을 지탱한다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** 극소 Scope / Hook / 반복 완성
- **Most Transferable Lesson:** 짧은 게임 반복 완성 → 강한 Hook → 작은 상용작으로 연결하는 생산 모델.
- **Primary Caution:** 짧은 게임이라고 제작비가 자동으로 낮은 것은 아니다. 독특한 3D 미술·사운드·연출 역량이 Hook을 지탱한다.

## 12. Evidence / Sources
- https://godotengine.org/article/godot-showcase-buckshot-roulette/
- https://mikeklubnika.com/logs/log_4

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-26 — Luck be a Landlord

<!-- SOURCE_FILE: 26_Luck_be_a_Landlord.md -->

# Solo / Micro Indie Production Case Study — Luck be a Landlord

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Dan DiIorio / TrampolineTales
- **Core Development Scale:** 1인 시작
- **Engine / Stack:** Godot 계열(현재 공개 쇼케이스)
- **Primary Review Axis:** 데이터 콘텐츠 / 단일 시스템 확장
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
슬롯머신의 심볼 선택과 시너지라는 단일 규칙에 콘텐츠를 집중하고, 성공적인 Early Access 이후 협업을 확대했다.

## 2. Production Model
공통 규칙 아래 심볼 데이터를 늘려 제작비 대비 빌드 다양성을 확보하는 방식.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`1인 시작` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
데이터 수를 늘리는 것만으로 깊이가 생기지 않는다. 시너지 가독성과 밸런스가 핵심 비용이다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** 데이터 콘텐츠 / 단일 시스템 확장
- **Most Transferable Lesson:** 공통 규칙 아래 심볼 데이터를 늘려 제작비 대비 빌드 다양성을 확보하는 방식.
- **Primary Caution:** 데이터 수를 늘리는 것만으로 깊이가 생기지 않는다. 시너지 가독성과 밸런스가 핵심 비용이다.

## 12. Evidence / Sources
- https://trampolinetales.com/presskit
- https://godotengine.org/showcase/

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-27 — Tiny Rogues

<!-- SOURCE_FILE: 27_Tiny_Rogues.md -->

# Solo / Micro Indie Production Case Study — Tiny Rogues

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** RubyDev
- **Core Development Scale:** 1인
- **Engine / Stack:** 비공개/자료 제한
- **Primary Review Axis:** 단순 아트 / 대량 빌드 / Scope Fight
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
첫 대형 솔로 프로젝트로, 단순한 아트 스타일을 사용해 많은 아이템과 적을 제작하는 방향을 택했다. 개발자 스스로 Scope와 싸우는 것을 핵심 조언으로 제시한다.

## 2. Production Model
그래픽 복잡도를 낮추고 데이터·빌드 다양성에 제작비를 집중하는 모델.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`1인` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
콘텐츠 수가 커지면 솔로 개발에서도 밸런스와 QA가 급격히 증가한다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** 단순 아트 / 대량 빌드 / Scope Fight
- **Most Transferable Lesson:** 그래픽 복잡도를 낮추고 데이터·빌드 다양성에 제작비를 집중하는 모델.
- **Primary Caution:** 콘텐츠 수가 커지면 솔로 개발에서도 밸런스와 QA가 급격히 증가한다.

## 12. Evidence / Sources
- https://store.steampowered.com/app/2088570/Tiny_Rogues/
- https://store.steampowered.com/news/posts/?enddate=1724099599&feed=steam_community_announcements

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-28 — Thronefall

<!-- SOURCE_FILE: 28_Thronefall.md -->

# Solo / Micro Indie Production Case Study — Thronefall

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Grizzly Games — Jonas Tyroller & Paul Schnepf
- **Core Development Scale:** 2인
- **Engine / Stack:** Unity / C#
- **Primary Review Axis:** 빠른 프로토타입 / 미니멀 전략
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
수개월간 1~2일짜리 프로토타입을 반복했고, 최종 아이디어는 매우 빠른 초기 프로토타입에서 나왔다. Early Access까지 약 180일, 당시 4레벨·3~4시간 규모였다.

## 2. Production Model
Play Prototype과 Art Prototype을 분리하고 작은 EA 범위로 빠르게 시장 검증하는 모델.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`2인` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
최종 성공 규모를 그대로 목표로 삼으면 안 된다. 핵심은 성공 결과가 아니라 작은 검증 단위다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** 빠른 프로토타입 / 미니멀 전략
- **Most Transferable Lesson:** Play Prototype과 Art Prototype을 분리하고 작은 EA 범위로 빠르게 시장 검증하는 모델.
- **Primary Caution:** 최종 성공 규모를 그대로 목표로 삼으면 안 된다. 핵심은 성공 결과가 아니라 작은 검증 단위다.

## 12. Evidence / Sources
- https://newsletter.pragmaticengineer.com/p/thronefall
- https://indiegames.wtf/interviews/thronefall/

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-29 — Strange Horticulture

<!-- SOURCE_FILE: 29_Strange_Horticulture.md -->

# Solo / Micro Indie Production Case Study — Strange Horticulture

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Bad Viking — Rob & John Donkin
- **Core Development Scale:** 2인 형제
- **Engine / Stack:** 공개 자료상 전용 엔진 정보 비중 낮음
- **Primary Review Axis:** 제한된 공간 / 역할 분담 / 세계관 압축
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
Rob이 코드, John이 아트를 담당하며 식물 가게와 식물 식별이라는 제한된 인터페이스를 중심으로 큰 세계관을 표현했다.

## 2. Production Model
월드 전체를 제작하지 않고 하나의 장소와 오브젝트를 통해 세계를 암시하는 Scope 절약.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`2인 형제` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
텍스트·식물 아트·퍼즐 설계량은 여전히 크며, 제한된 화면이 콘텐츠 제작비까지 제거하지는 않는다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** 제한된 공간 / 역할 분담 / 세계관 압축
- **Most Transferable Lesson:** 월드 전체를 제작하지 않고 하나의 장소와 오브젝트를 통해 세계를 암시하는 Scope 절약.
- **Primary Caution:** 텍스트·식물 아트·퍼즐 설계량은 여전히 크며, 제한된 화면이 콘텐츠 제작비까지 제거하지는 않는다.

## 12. Evidence / Sources
- https://www.badviking.com/
- https://www.gamedeveloper.com/design/deep-dive-strange-horticulture

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-30 — The Case of the Golden Idol

<!-- SOURCE_FILE: 30_The_Case_of_the_Golden_Idol.md -->

# Solo / Micro Indie Production Case Study — The Case of the Golden Idol

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Color Gray Games — Andrejs & Ernests Kļaviņš
- **Core Development Scale:** 2인 형제
- **Engine / Stack:** Godot (원작)
- **Primary Review Axis:** 추리 콘텐츠 / 역할 분담 / Prototype-first
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
코드와 그래픽 역할을 형제가 나누고, 스튜디오 설립 목적 자체를 상업 가능성을 확인하는 프로토타입 제작에 두었다. 제한된 장면에서 단서 교차에 제작비를 집중했다.

## 2. Production Model
작은 팀이 장면 수보다 정보 밀도와 핵심 추리 상호작용으로 가치를 만드는 모델.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`2인 형제` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
추리 콘텐츠는 자산 수가 적어 보여도 논리 QA와 작문 비용이 매우 높다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** 추리 콘텐츠 / 역할 분담 / Prototype-first
- **Most Transferable Lesson:** 작은 팀이 장면 수보다 정보 밀도와 핵심 추리 상호작용으로 가치를 만드는 모델.
- **Primary Caution:** 추리 콘텐츠는 자산 수가 적어 보여도 논리 QA와 작문 비용이 매우 높다.

## 12. Evidence / Sources
- https://godotengine.org/showcase/
- https://www.escapistmagazine.com/strange-horticulture-case-of-golden-idol-interview-bad-viking-color-gray-games-donkin-klavins/

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-31 — Chants of Sennaar

<!-- SOURCE_FILE: 31_Chants_of_Sennaar.md -->

# Solo / Micro Indie Production Case Study — Chants of Sennaar

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Rundisc — Julien Moya & Thomas Panuel
- **Core Development Scale:** 2인 핵심 + 일부 협업
- **Engine / Stack:** Unity 계열로 알려짐(문서에는 확정 자료만 사용)
- **Primary Review Axis:** 전문화된 역할 / 단일 USP
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
Julien Moya가 아트·디자인, Thomas Panuel이 코드·디자인을 맡아 언어 해독이라는 하나의 강한 USP를 중심으로 제작했다. 이전 작품 출시 경험을 통해 자체 출시 역량을 먼저 검증했다.

## 2. Production Model
2인이 코드/아트를 전문화하면서 디자인은 공동 소유하는 소규모 팀 모델.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`2인 핵심 + 일부 협업` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
고유 아트와 수작업 퍼즐·월드 제작량이 커서 1인이 동일 Scope를 그대로 복제하기 어렵다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** 전문화된 역할 / 단일 USP
- **Most Transferable Lesson:** 2인이 코드/아트를 전문화하면서 디자인은 공동 소유하는 소규모 팀 모델.
- **Primary Caution:** 고유 아트와 수작업 퍼즐·월드 제작량이 커서 1인이 동일 Scope를 그대로 복제하기 어렵다.

## 12. Evidence / Sources
- https://www.rundisc.io/chants-of-sennaar/
- https://en.wikipedia.org/wiki/Chants_of_Sennaar

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-32 — Patch Quest

<!-- SOURCE_FILE: 32_Patch_Quest.md -->

# Solo / Micro Indie Production Case Study — Patch Quest

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Liam Edwards / Lychee Game Labs
- **Core Development Scale:** 1인 핵심
- **Engine / Stack:** Unity 계열(공개 인터뷰 기반 확인 필요)
- **Primary Review Axis:** Solo Scope Warning / 장기 개발
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
약 7년에 걸쳐 솔로 핵심 개발이 진행된 사례로, 여러 시스템을 한 작품에 결합할 때 장기화되는 위험을 보여준다.

## 2. Production Model
성공 사례라기보다 “솔로가 시스템을 계속 추가할 때 시간 비용이 어떻게 커지는가”를 보는 경고 Reference.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`1인 핵심` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
긴 개발 기간 자체가 기회비용이다. 기능 결합의 재미와 제작 효율을 분리해서 평가해야 한다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** Solo Scope Warning / 장기 개발
- **Most Transferable Lesson:** 성공 사례라기보다 “솔로가 시스템을 계속 추가할 때 시간 비용이 어떻게 커지는가”를 보는 경고 Reference.
- **Primary Caution:** 긴 개발 기간 자체가 기회비용이다. 기능 결합의 재미와 제작 효율을 분리해서 평가해야 한다.

## 12. Evidence / Sources
- https://store.steampowered.com/news/posts/?enddate=1677777042&feed=steam_community_announcements
- https://store.steampowered.com/app/1347970/Patch_Quest/

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-33 — SNKRX

<!-- SOURCE_FILE: 33_SNKRX.md -->

# Solo / Micro Indie Production Case Study — SNKRX

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** a327ex
- **Core Development Scale:** 1인
- **Engine / Stack:** LÖVE / Lua
- **Primary Review Axis:** 저비용 아트 / 빌드 시스템 / 재사용
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
추상적 그래픽과 자동 공격, 영웅 클래스 시너지를 결합해 시각 자산보다 빌드 조합에 콘텐츠 비용을 집중했다.

## 2. Production Model
전투 애니메이션과 고유 캐릭터 아트를 최소화하고 시스템 조합을 콘텐츠로 사용하는 모델.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`1인` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
빌드 조합 수가 많아질수록 밸런스·툴팁·가독성 비용이 증가한다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** 저비용 아트 / 빌드 시스템 / 재사용
- **Most Transferable Lesson:** 전투 애니메이션과 고유 캐릭터 아트를 최소화하고 시스템 조합을 콘텐츠로 사용하는 모델.
- **Primary Caution:** 빌드 조합 수가 많아질수록 밸런스·툴팁·가독성 비용이 증가한다.

## 12. Evidence / Sources
- https://store.steampowered.com/app/915310/SNKRX/
- https://store.steampowered.com/developer/a327ex/

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-34 — Peglin

<!-- SOURCE_FILE: 34_Peglin.md -->

# Solo / Micro Indie Production Case Study — Peglin

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Red Nexus Games
- **Core Development Scale:** 4인 초기 상용팀
- **Engine / Stack:** Unity 계열(공개 자료 기반 확인 필요)
- **Primary Review Axis:** Game Jam → 상용화 / 역할 분담
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
48시간 게임잼에서 pachinko 아이디어를 만든 뒤 4인 팀이 개발·아트·음악 역할을 나누어 Early Access까지 확장했다.

## 2. Production Model
Jam에서 한 문장짜리 Core Mechanic을 검증한 뒤 데이터 콘텐츠와 메타를 추가하는 모델.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`4인 초기 상용팀` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
작은 팀이라도 물리 기반 전투와 대량 유물 조합은 밸런스 비용이 크다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** Game Jam → 상용화 / 역할 분담
- **Most Transferable Lesson:** Jam에서 한 문장짜리 Core Mechanic을 검증한 뒤 데이터 콘텐츠와 메타를 추가하는 모델.
- **Primary Caution:** 작은 팀이라도 물리 기반 전투와 대량 유물 조합은 밸런스 비용이 크다.

## 12. Evidence / Sources
- https://www.shacknews.com/article/127914/peglin-developer-talks-making-the-game-with-a-four-person-team
- https://en.wikipedia.org/wiki/Peglin

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-35 — Dome Keeper

<!-- SOURCE_FILE: 35_Dome_Keeper.md -->

# Solo / Micro Indie Production Case Study — Dome Keeper

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Bippinbits
- **Core Development Scale:** 2인 Jam 시작 → 극소규모 협업
- **Engine / Stack:** Godot
- **Primary Review Axis:** Jam Prototype / 이중 루프 / 모듈 콘텐츠
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
Ludum Dare 48의 72시간 프로토타입 Dome Romantik에서 출발했다. René와 Anne이 핵심을 만들고 이후 음악·개발 협업이 더해졌다. 채굴과 방어를 교대로 반복하는 두 루프에 집중한다.

## 2. Production Model
Game Jam에서 검증된 작은 Core Loop를 상용 제품으로 확장하는 모델.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`2인 Jam 시작 → 극소규모 협업` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
상용화 단계에서 콘텐츠·아트·밸런스·업데이트가 늘어나므로 Jam Scope와 Release Scope를 혼동하면 안 된다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** Jam Prototype / 이중 루프 / 모듈 콘텐츠
- **Most Transferable Lesson:** Game Jam에서 검증된 작은 Core Loop를 상용 제품으로 확장하는 모델.
- **Primary Caution:** 상용화 단계에서 콘텐츠·아트·밸런스·업데이트가 늘어나므로 Jam Scope와 Release Scope를 혼동하면 안 된다.

## 12. Evidence / Sources
- https://bippinbits.com/
- https://domekeeper.wiki.gg/wiki/Dome_Keeper

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END



---

# REF-36 — Brotato

<!-- SOURCE_FILE: 36_Brotato.md -->

# Solo / Micro Indie Production Case Study — Brotato

> Studio Game Design Reviewer — 3차 Reference Library

## 0. Production Profile
- **Developer:** Blobfish / Thomas Gervraud
- **Core Development Scale:** 1인 시작
- **Engine / Stack:** Godot
- **Primary Review Axis:** 데이터 중심 / 캐릭터 규칙 변형 / 빠른 반복
- **Library Role:** 제작 가능성·Scope·콘텐츠 효율 평가용

## 1. Why This Case Matters
Blobfish는 2018년부터 작은 게임을 만들어 온 솔로 개발자이며 Brotato 역시 솔로 중심으로 출발했다. 짧은 웨이브, 다수 캐릭터의 규칙 변형, 아이템/무기 데이터로 반복성을 만든다.

## 2. Production Model
동일 전투 자산을 캐릭터 Modifier와 상점·아이템 데이터로 재맥락화하는 높은 콘텐츠 효율.

## 3. Core Scope Strategy
이 작품에서 중요한 것은 최종 성공 규모가 아니라, 소수 인원이 **어떤 요소를 직접 만들고 어떤 요소를 단순화했는가**이다. Reviewer는 신규 기획과 비교할 때 그래픽 수, 전용 화면 수, 고유 콘텐츠 수, 시스템 조합 수, QA 범위를 함께 본다.

## 4. Prototype → Product Lesson
- 핵심 재미를 가능한 작은 단위에서 먼저 검증한다.
- 검증 전 콘텐츠 확장을 피한다.
- 상용화 과정에서 추가된 기능과 최초 핵심 루프를 구분한다.
- 히트 이후 업데이트 규모를 초기 개발 Scope로 오해하지 않는다.

## 5. Content Efficiency
### Reuse Principle
공통 규칙·데이터·모듈 자산·제한된 공간 중 어떤 수단으로 콘텐츠 제작비를 줄였는지를 우선 분석한다.

### What to Measure in a New Project
- 고유 화면 수
- 고유 캐릭터/적/장소 수
- 전용 애니메이션 및 일러스트 수
- 데이터만 추가해 확장 가능한 콘텐츠 비율
- 수작업 레벨/시나리오 비율
- 조합 폭증에 따른 QA 비용

## 6. Role Distribution Lesson
`1인 시작` 규모라는 사실 자체보다 코드·아트·디자인·음악·마케팅 중 무엇을 핵심 개발자가 맡고 무엇을 협업/외주했는지 비교해야 한다.

## 7. Solo Feasibility Analysis
### Strongly Transferable
- 핵심 Loop를 먼저 분리해 검증하는 방식
- 공통 시스템을 통한 자산 재사용
- 프로젝트의 가장 비싼 제작 축을 의식적으로 제한하는 방식

### Main Risk
히트 이후의 대규모 확장 상태를 초기 솔로 Scope로 오해하면 안 된다. 초기 제품과 후속 확장을 분리해서 봐야 한다.

### Solo Feasibility Verdict
**REFERENCE-WORTHY.** 단, 작품 전체를 복제하는 것이 아니라 해당 작품이 사용한 Scope 절약 원리를 현재 프로젝트에 적용할 수 있는지 판단한다.

## 8. Scope Warning Signs for Reviewer
신규 기획이 이 Reference보다 훨씬 많은 전용 화면·수작업 콘텐츠·고유 애니메이션·상태 조합을 요구한다면, 재미 평가와 별도로 `SOLO_SCOPE_RISK`를 올린다.

## 9. What NOT to Copy
- 성공 후 추가된 콘텐츠 규모
- 장르/아트 스타일의 표면적 모방
- 판매량을 제작 방식의 정당성으로 사용하는 것
- '소규모 팀이 만들었으니 나도 동일 Scope가 가능하다'는 단순 추론

## 10. Reviewer Questions
1. 이 게임의 최초 재미 검증 단위는 얼마나 작았는가?
2. 가장 비싼 제작 영역은 무엇이었는가?
3. 콘텐츠를 데이터/조합으로 얼마나 재사용했는가?
4. 현재 검토 기획은 이 사례보다 고유 자산이 얼마나 많은가?
5. 동일 구조를 1인이 만든다면 무엇을 삭제해야 하는가?
6. 프로토타입에서 반드시 검증해야 할 하나의 가설은 무엇인가?

## 11. Production Verdict
- **Reference Axis:** 데이터 중심 / 캐릭터 규칙 변형 / 빠른 반복
- **Most Transferable Lesson:** 동일 전투 자산을 캐릭터 Modifier와 상점·아이템 데이터로 재맥락화하는 높은 콘텐츠 효율.
- **Primary Caution:** 히트 이후의 대규모 확장 상태를 초기 솔로 Scope로 오해하면 안 된다. 초기 제품과 후속 확장을 분리해서 봐야 한다.

## 12. Evidence / Sources
- https://www.blobfish.dev/about/
- https://www.blobfish.dev/

## 13. Evidence Confidence
- 공개 개발자 자료·공식 사이트에서 확인되는 인원/개발 과정은 사실 데이터로 취급한다.
- 엔진·기간·외주 범위가 명확히 공개되지 않은 경우 추정하지 않고 `Unknown`으로 남긴다.
- 판매량은 **3차의 평가 기준으로 사용하지 않는다.** 판매 성과 분석은 4차 Commercial Reference에서 별도 처리한다.

# END

