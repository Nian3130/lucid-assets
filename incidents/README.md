# incidents 규칙 (lucid-assets)

이 폴더는 **사건/이벤트(Incident) 페이지**를 보관합니다.  
각 파일은 GitHub Pages에서 바로 열 수 있는 단일 HTML 문서이며,
케이브덕(모바일/접기 환경)을 고려해 **상단 핵심 정보 → 상세 정보** 순서로 구성합니다.

Pages 경로:
https://nian3130.github.io/lucid-assets/incidents/

---

## 1) 파일/URL 규칙

### 파일명 규칙
- 소문자 + 언더스코어 중심
- 의미가 분명한 사건 코드 사용
- 날짜는 필요할 때만(정렬 목적)

예시)
- heat_anomaly.html
- stair_intrusion.html
- event_2025_12_21.html

### URL 예시
https://nian3130.github.io/lucid-assets/incidents/heat_anomaly.html

---

## 2) 페이지 구성 표준 (권장 레이아웃)

케이브덕의 “접기/모바일”을 기준으로 **핵심을 위로** 배치합니다.

### [1] Command Panel (최상단 고정)
- 로어북에 명시한 명령어 요약
- (예) `!진입`, `!탈출`, `!이벤트`, `!종료` 등
- 사용자가 바로 복사/확인 가능하도록 짧게

### [2] Map / Layer Panel
- 지도 이미지 + 현재 레이어 표시(겹치기/하이라이트)
- “현재 사건 발생 위치”를 시각적으로 보여주는 영역

### [3] Current Location + Incident Summary
- 위치명(간결/구체)
- 발생한 사건(1~3줄 요약)
- 위험도/주의문구(선택)

### [4] Creator Comment / World Notes (가변)
- 크리에이터 코멘트(짧게)
- 세계관/규칙/설명(필요한 만큼, 접기 고려)

### [5] Character Visual
- 캐릭터 이미지(대표 1장)
- 필요 시 여러 장은 접기/슬라이드/썸네일 방식 권장

### [6] Character Profile (공개 인적사항)
- 이름/나이/성별/소속/외형 요약
- 공개 가능한 범위만

### [7] Public Abilities / Known Info
- 능력/제약/관측 정보(공개분)
- “확정된 정보”와 “추정”을 구분하면 좋음

---

## 3) 콘텐츠 운영 원칙

- 사건 페이지는 “요약 → 상세” 구조를 유지합니다.
- 모바일에서 스크롤이 길어지면:
  - 접기(Accordion) 또는 스크롤 박스 사용을 우선 고려
- 민감한 스포일러/비공개 설정은 사건 페이지에 직접 노출하지 않습니다.
  - 필요 시 별도 private 문서로 분리

---

## 4) 캐릭터 카드 연결 방식 (권장)

사건 페이지 내 캐릭터 블록은 재사용을 위해 “카드 템플릿”을 이용합니다.

권장)
- `templates/character_card.html`를 기준으로 복사해 incident에 삽입
- 이미지 URL은 `assets/<character>/...`에서 불러옴

이미지 URL 예시)
https://nian3130.github.io/lucid-assets/assets/raven/raven_01.png

---

## 5) 스타일 규칙 (케이브덕/인라인 기준)

- 기본은 인라인 스타일로 유지(환경 의존성 최소화)
- 공통 스타일이 필요하면:
  - (A) Pages 미리보기용으로 CSS 파일 분리 후
  - (B) 케이브덕용 배포 시 인라인로 합치는 방식 권장

---

## 6) 체크리스트 (발행 전)

- [ ] 페이지 최상단에 Command Panel이 있는가?
- [ ] [위치]와 [사건 요약]이 접기 없이 바로 보이는가?
- [ ] 지도/레이어가 현재 위치를 명확히 보여주는가?
- [ ] 캐릭터 이미지 URL이 Pages에서 정상 로드되는가?
- [ ] 모바일에서 가독성(폰트/여백/줄바꿈)이 괜찮은가?
