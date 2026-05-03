# HTECH Indigo Design Guide

## Brand Direction
- HTECH의 기본 색 방향은 `Indigo Blue`를 중심으로 잡는다.
- 인디고는 반도체 장비 브랜드에 필요한 정밀함, 신뢰감, 고급 기술 이미지를 동시에 준다.
- 기존 블루보다 조금 더 깊고 농도 있는 톤으로 조정해 B2B 제안서, 전시 그래픽, 웹 헤더에서 밀도를 높인다.

## Core Palette
- Primary Indigo: `#3347C4`
- Deep Indigo: `#1F2F8A`
- Bright Accent Indigo: `#5870FF`
- Mono Indigo: `#4053CE`
- Reverse Background Indigo: `#1C276F`
- Wordmark Black: `#111111`
- White: `#FFFFFF`

## Typography
- 기본 브랜드 서체는 `Pretendard`를 사용한다.
- 국문/영문 모두 가능한 한 `Pretendard`로 통일해 문서, 웹, 제안서, 전시물 톤을 일관되게 유지한다.
- 대체 서체 순서는 `Apple SD Gothic Neo` → `Noto Sans KR` → `sans-serif`로 둔다.
- 제목, 섹션 헤드라인, UI 라벨, 문서 본문 모두 같은 서체 체계 안에서 굵기만 조절하는 방식을 기본으로 한다.
- 권장 굵기:
  - Display / Key Headline: `Pretendard Bold` 또는 `Pretendard ExtraBold`
  - Section Title: `Pretendard SemiBold` 또는 `Pretendard Bold`
  - Body / Caption: `Pretendard Regular` 또는 `Pretendard Medium`
- 영문만 따로 다른 서체로 분리하지 않는 것을 기본 원칙으로 한다.
- 현재 제공한 로고 파일은 외곽선 처리된 `SVG`이므로 폰트 의존성은 없지만, 로고 주변의 모든 브랜드 문서·웹·슬라이드 텍스트는 `Pretendard` 기준으로 운용한다.

## Logo Variations
- `HTECH_LOGO_primary-indigo.svg`
  - 기본 브랜드 서명.
  - 웹사이트, 회사소개서 표지, 일반 인쇄물 기본값으로 사용.
  - `H.TECH`, `(주)에이치테크`, 태그라인은 검은색으로 통일.
- `HTECH_LOGO_deep-indigo.svg`
  - 조금 더 고급스럽고 기술적인 인상.
  - 반도체 장비 카탈로그, IR 문서, 부스 그래픽에 적합.
  - `H.TECH`는 심볼과 분리해 검은색으로 유지.
- `HTECH_LOGO_mono-indigo.svg`
  - 심볼 단색 운용 버전.
  - 실크 인쇄, 각인, 유니폼, 저비용 출력물에 적합.
  - 텍스트는 검은색으로 유지해 가독성을 확보.
- `HTECH_LOGO_reverse-indigo.svg`
  - 어두운 인디고 배경용 단색 역상 버전.
  - 심볼, `H.TECH`, `(주)에이치테크`, 태그라인 전부 흰색으로 통일.
  - 다크 모드 웹 섹션, 배너, 전시장 벽면 그래픽에 적합.
- `HTECH_LOGO_black-background.svg`
  - 검은 배경용 단색 역상 버전.
  - 전광판, 간판 시안, 어두운 장비 패널 목업에 적합.

## Usage Rules
- 가능하면 `Primary Indigo`를 기본값으로 사용한다.
- 배경이 밝고 고급 톤이 필요할 때만 `Deep Indigo`를 사용한다.
- 색상 제약이 있는 생산물에는 `Mono Indigo`를 우선 사용한다.
- 밝은 배경 variation에서는 `H.TECH`와 텍스트를 검은색으로 고정한다.
- 어두운 배경 위에서는 일반 버전을 반전하지 말고 반드시 `Reverse Indigo` 또는 `Black Background`를 사용한다.
- 브랜드 응용 그래픽, 소개서, 웹페이지 텍스트는 `Pretendard`를 기본 서체로 사용한다.

## Clear Space
- 로고 주변 최소 여백은 심볼 내부 흰 사각형 한 변의 `0.5배` 이상 확보한다.
- 워드마크나 태그라인 아래에 다른 문구를 붙일 때는 태그라인 높이 이상 간격을 둔다.

## Minimum Size
- 가로형 전체 로고 최소 너비: `140px`
- 심볼 단독 최소 너비: `28px`
- 태그라인 포함 버전은 `220px` 이하에서 사용하지 않는 것을 권장한다.

## Background Guidance
- 화이트, 라이트 그레이, 매우 연한 인디고 배경이 가장 안정적이다.
- 채도가 높은 사진 위 직접 사용은 피한다.
- 배경과의 대비가 부족하면 태그라인이 먼저 무너지므로, 밝은 배경에서는 검은 텍스트 고정, 어두운 배경에서는 흰색 단색 역상 고정을 사용한다.

## Do / Don't
- Do: 인디고 계열 안에서 메인톤과 포인트톤의 계층을 유지한다.
- Do: 인쇄물에서는 단색 판형 여부를 먼저 확인하고 `Mono Indigo` 적용을 검토한다.
- Do: 국문과 영문을 같은 `Pretendard` 계열 안에서 정리해 톤을 통일한다.
- Don't: 심볼 메인과 텍스트를 서로 다른 계열 색으로 과도하게 분리하지 않는다.
- Don't: 브랜드 문서에서 영문만 별도 디스플레이 폰트로 분리해 이질감을 만들지 않는다.
- Don't: 역상 사용 시 텍스트만 검은색으로 남기지 않는다.
- Don't: 역상 사용 시 내부 흰 사각형을 그대로 두어 심볼 구조가 무너지게 하지 않는다.
- Don't: 태그라인만 별도 색으로 튀게 만들지 않는다.

## Deliverables
- `HTECH_LOGO_primary-indigo.svg`
- `HTECH_LOGO_deep-indigo.svg`
- `HTECH_LOGO_mono-indigo.svg`
- `HTECH_LOGO_reverse-indigo.svg`
- `HTECH_LOGO_black-background.svg`
- `HTECH_Indigo_Design_Guide.md`
- `HTECH_Indigo_Variations_Preview.html`
