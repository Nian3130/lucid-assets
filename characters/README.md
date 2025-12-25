# assets 규칙 (lucid-assets)

이 폴더는 **이미지/리소스 호스팅 전용**입니다.  
GitHub Pages를 통해 외부에서 URL로 직접 불러오는 것을 전제로 합니다.

---

## 1) 기본 URL 규칙

- Pages 루트:
  https://nian3130.github.io/lucid-assets/

- assets 기본 경로:
  https://nian3130.github.io/lucid-assets/assets/

예시)
- https://nian3130.github.io/lucid-assets/assets/raven_01.png
- https://nian3130.github.io/lucid-assets/assets/raven/raven_02.png

> 경로/파일명은 대소문자를 구분합니다.

---

## 2) 폴더 구조 원칙

- 캐릭터별 에셋은 `assets/<character>/` 아래에 저장합니다.
- 공용 UI/지도 등은 별도 하위 폴더로 분리합니다(필요 시 추가).

권장 구조 예시)
- assets/raven/
- assets/serina/
- assets/jaeyul/
- assets/maps/        (지도/레이어 오버레이)
- assets/ui/          (아이콘/프레임/배지 등 공용)

---

## 3) 파일명 규칙 (강력 권장)

### 허용 문자
- 영문 소문자(a-z), 숫자(0-9), 언더스코어(_), 하이픈(-), 점(.)
- 공백 금지, 괄호() 가급적 금지(운영 중 URL 관리가 헷갈릴 수 있음)

### 규칙
- 소문자 + 언더스코어 중심으로 통일
- 정렬/버전 관리를 위해 번호는 2자리 이상 권장: `01`, `02`, `03` ...

예시)
- raven_portrait_01.png
- raven_expr_03.png
- map_base_01.png
- overlay_resonance_01.png

---

## 4) 업로드/교체 운영 규칙

### (A) 새 파일 추가
- 동일한 규칙으로 파일명 작성 → 업로드 → 커밋

### (B) 이미지 교체(같은 URL 유지)
- 같은 경로/같은 파일명으로 새 파일 업로드(덮어쓰기)  
  → HTML 수정 없이 최신 이미지로 교체 가능

주의)
- 브라우저 캐시 때문에 교체 직후 이전 이미지가 보일 수 있음  
  → 강력 새로고침(Ctrl+F5) 또는 파일명 버전업 권장

### (C) 파일명 변경(비추천)
- URL이 깨지므로, 필요한 경우 HTML/템플릿에서도 함께 수정

---

## 5) 타입/해상도 권장

- 포맷: PNG(투명 필요), JPG(용량 절감), WEBP(가능하면)
- 캐릭터 카드용: 세로 이미지 기준 900~1600px 권장
- 지도/오버레이: 동일한 캔버스 크기 유지(겹치기 용이)

---

## 6) 폴더 유지용 파일

빈 폴더는 Git에서 유지되지 않으므로, 필요 시 `.keep` 파일로 폴더를 고정합니다.
예)
- assets/raven/.keep
- assets/maps/.keep
