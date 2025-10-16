# absens-css (앱센스-CSS)
**가독성과 부드러운 디자인**에 중점을 둔 **클래스리스(Classless) CSS 프레임워크**입니다.   
스타일링을 위한 클래스를 전혀 사용하지 않고, 오직 깨끗하고 아름다운 기본 HTML 태그에만 스타일이 적용되어 현대적인 레이아웃 구조와 미묘한 곡선 디자인을 제공합니다.

<br/>

## 💡 디자인 3원칙
absens-css는 깔끔하고, 접근성이 높으며, 유지보수가 용이한 사용자 인터페이스를 제공하기 위해 세 가지 핵심 원칙을 기반으로 구축되었습니다.

### 1. 클래스나 ID를 사용하지 않는 순수 스타일링 🏷️
**핵심 철학.** 스타일은 오직 **시맨틱 HTML 태그**(`section`, `p`, `button`, `hr` 등)에만 적용됩니다. 이를 통해 HTML 코드가 깨끗하게 유지되고, 코드의 의미(시맨틱스)에 집중하며, 유지보수 복잡성이 획기적으로 줄어듭니다.

### 2. 가독성과 범용성 최우선 📖
**사용자 경험에 집중.** 타이포그래피, 간격, 레이아웃을 최적화하여 높은 **가독성**과 낮은 인지 부하를 보장합니다. 디자인은 의도적으로 **범용적이고 유연**하게 설계되어, 과도한 커스터마이징 없이도 광범위한 웹 프로젝트에 적합합니다.

### 3. 곡선을 활용한 부드러운 디자인 강조 〰️
**온화한 미학.** 레이아웃 컴포넌트와 폼 요소는 부드러운 **테두리 곡률(border-radius)** 값과 은은한 그림자를 사용하여 디자인되었습니다. 이는 애플리케이션 전반에 걸쳐 현대적이고 친근하며 방해되지 않는 **'소프트 UI'** 미학을 제공합니다.

<br/>

## 🚧 프로젝트 상태 (Project Status)
absens-css는 현재 **개발 초기 단계 (v0.1.0 진행 중)**에 있습니다.
현재 파일 구조와 디자인 원칙에 따라 핵심 CSS 모듈을 작성하고 있으며, **아직 정식으로 사용할 수 있는 통합된 파일(`absens-css.css`)은 제공되지 않습니다.**

**정식 배포 및 사용 방법은 로드맵 v1.0.0 달성 후 "시작하기" 섹션을 통해 안내될 예정입니다.**

<br/>

## 🗺️ 로드맵 (Roadmap)
absens-css는 현재 **개발 초기 단계 (v0.1.0)**에 있으며, `src/modules` 내의 모든 파일을 완성하는 것을 1차 목표로 합니다.

| 버전 | 목표 | 상태 |
| :--- | :--- | :--- |
| **v0.1.0** | 모든 핵심 CSS 모듈 파일 완성 및 통합 (`absens-css.css` 완성) | ⚙️ **진행 중** |
| **v0.2.0** | 반응형 디자인 및 접근성(A11y) 표준 최적화  | 💡 예정 |
| **v1.0.0** | 공식 릴리즈 및 CDN 배포 시작 | 💡 예정 |

### v0.1.0 남은 작업 목록 (To-Do List)
- [x] `demo.html` 파일에 주요 시맨틱 HTML 구조 작성
- [x] `_variables.css` (공통 변수)
- [x] `_reset.css` (기본 스타일 초기화)
- [x] `_base.css` (전역 기본 스타일)
- [x] `_layout.css` (구조 태그)
- [x] `_typography.css` (텍스트 및 링크 태그)
- [x] `_list.css` (목록 태그)
- [x] `_controls.css` (폼 요소)
- [x] `_media.css` (미디어 태그)
- [x] `_buttons.css` (버튼 태그. button, input)
- [x] `_textfields.css` (텍스트필드 관련 태그. input, textarea)

<br/>

## 📂 디렉토리 구조
absens-css는 모듈 방식으로 구성되어 있으며, 각 파일은 특정 용도의 HTML 태그 스타일링을 담당합니다.
```
absens-css/   
├── src/   
│   ├── modules/                     # 🧩 스타일링 모듈   
│   │   ├── _variables.css           # 🎨 공통 변수 (색상, 곡선 크기 등)   
│   │   ├── _reset.css               # 🔄 브라우저 기본 스타일 초기화   
│   │   ├── _base.css                # 📝 전역 기본 스타일 (body 태그에 대한 폰트, 배경 등 설정)   
│   │   ├── _layout.css              # 🏗️ 구조 태그 (header, main, section, form, hr 등)
│   │   ├── _list.css                # 📑 목록 태그 (ul, ol, dl)
│   │   ├── controls/                # 🖊️ 폼 요소 (input, button, textarea, select)
│   │       ├── _controls.css        # 📦 controls 모듈을 @import하는 통합 controls 파일
│   │       ├── _buttons.css         # 🔘 버튼류 스타일 (button, input[type="submit", etc.])
│   │       └── _textfields.css      # 🗄️ 텍스트 입력 및 선택 필드 스타일 (input, textarea, select)
│   │   ├── typography/              # 📖 텍스트 및 링크 태그 (h1-h6, p, a, blockquote)
│   │       ├── _typography.css      # 📦 typography 모듈을 @import하는 통합 typography 파일
│   │       ├── _anchors.css         # 🖊️ 링크 태그 (a)
│   │       └── _headers.css         # 🗄️ 제목 태그 (h1-h6)
│   │   └── _media.css               # 🖼️ 미디어 태그 (img, figure, video)
│   └── absens-css.css               # 📦 모든 모듈을 @import하는 통합 파일      
├── examples/                        # 💡 데모 및 사용 예시 파일 폴더
│   └── demo.html                    # 💻 개발 및 테스트용 데모 페이지
└── README.md                        # 📘 현재 문서
```