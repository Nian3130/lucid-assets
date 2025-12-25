# templates 규칙 (lucid-assets)

이 폴더는 **재사용 가능한 HTML 템플릿**을 보관합니다.  
(캐릭터 카드, 사건 허브, 지도/레이어 UI 등)

Pages 경로:  
https://nian3130.github.io/lucid-assets/templates/

---

## 1) 템플릿 목적 / 운영 원칙

- 케이브덕(모바일/접기 강제)을 기준으로 설계합니다.
- 기본은 **인라인 스타일 중심**으로 유지합니다.
- 템플릿은 “복사 → 값만 교체 → 배포”를 목표로 합니다.
- **원본 텍스트(로어)는 .md**로 보관하고, HTML은 필요 시 가공본으로 생성합니다.

---

## 2) 파일/URL 규칙

### 파일명 규칙
- 소문자 + 언더스코어
- 역할이 드러나는 이름 사용

예시)
- character_card.html
- incident_hub.html
- map_layer_panel.html
- ui_snippets.html

### Pages 미리보기 URL
https://nian3130.github.io/lucid-assets/templates/character_card.html

> 템플릿은 Pages에서 바로 열어 모바일/PC 레이아웃을 빠르게 확인합니다.

---

## 3) “값 교체 포인트” 표준(권장)

템플릿은 아래 항목만 바꾸면 동작하도록 구성합니다.

### (A) 이미지 URL
이미지는 **characters/<name>/assets**에서 불러옵니다.

기본 규칙)
https://nian3130.github.io/lucid-assets/characters/<character>/assets/<file>

예시)
- https://nian3130.github.io/lucid-assets/characters/raven/assets/raven_01.png

> ⚠️ 예전 `/assets/...` 경로는 현재 구조에서는 사용하지 않습니다.

### (B) 텍스트 블록
- 제목(캐릭터명/사건명)
- 한줄 코멘트/키워드 2~4개
- 소개/설명(스크롤 박스 또는 접기)

### (C) 링크(선택)
- 관계 페이지/사건 페이지/다른 카드로 이동 링크

---

## 4) 인라인 스타일 규칙(케이브덕 대응)

- 기본은 `<div style="...">` 형태로 유지합니다.
- 외부 CSS/JS 의존성을 최소화합니다.
- 애니메이션/복잡 효과는 “Pages 미리보기용”으로만 사용하고,
  케이브덕에서는 깨져도 내용이 읽히도록 구성합니다.

권장)
- 모바일 기준 글자 크기: 13~15px
- 줄간격: 1.6~1.9
- 블록 여백: 12~18px 단위
- 긴 내용은 `overflow-y:auto` 박스 또는 접기(accordion) 사용

> 그러나 뉴비라서 잘 못함. ChatGpt한테 검수 받고 있음.

---

## 5) 템플릿 사용 흐름(권장)

1) templates에서 기준 템플릿 선택
2) 파일을 복사하여 대상 위치로 저장
   - 사건 페이지: `incidents/<incident>.html`
   - 캐릭터 카드: 케이브덕 업로드용 HTML 또는 incidents에 포함
3) 이미지/텍스트 “값 교체 포인트”만 수정
4) Pages에서 미리보기로 확인
5) 케이브덕에 최종 반영

추가 원칙)
- **캐릭터/사건 원본 로어는 .md로만 관리**합니다.
- HTML은 “배포/표시용 가공본”으로 보고, 원문 수정은 .md에서 합니다.

---

## 6) 추천 템플릿 목록(운영 기준)

- character_card.html
  - 캐릭터 소개/이미지/프로필/공개 능력 요약

- incident_hub.html
  - 사건 페이지 골격(명령어, 현재 위치/지도, 사건 개요, 캐릭터 섹션)

- map_layer_panel.html
  - 지도 + 레이어(흔적계/심층계/공명지대/기원계) 표시 UI 블록

- ui_snippets.html (선택)
  - 자주 쓰는 박스/배지/경고문/버튼 스타일 조각 모음

---

## 7) 체크리스트(커밋 전)

- [ ] 이미지 URL이 Pages에서 직접 열리는가?
- [ ] 모바일 폭에서 레이아웃이 깨지지 않는가?
- [ ] 핵심 정보(명령어/위치/요약)가 상단에서 바로 보이는가?
- [ ] 텍스트가 너무 길면 스크롤 박스/접기를 적용했는가?
- [ ] 파일명/경로가 소문자/언더스코어 규칙을 지켰는가?
- [ ] (권장) 원본 로어는 .md에 남기고, HTML은 가공본으로 유지했는가?

---

# 캐릭터 원본 .md 템플릿 (KO / EN / CAVEDUCK)

- 별도의 파일에서 확인요망.