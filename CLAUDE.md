# CLAUDE.md

이 파일은 Claude Code가 이 저장소에서 작업할 때 참고하는 안내서입니다.

## 프로젝트 개요

Slidev 기반의 멀티 프레젠테이션 프로젝트입니다. 각 프레젠테이션은 `presentations/` 하위 폴더에 저장되며, GitHub Actions를 통해 GitHub Pages로 자동 배포됩니다.

## 프로젝트 구조

```
/slidev/
├── presentations/           # 모든 프레젠테이션
│   ├── comfyui/            # 예시 프레젠테이션
│   │   ├── slides.md       # 슬라이드 내용
│   │   └── public/images/  # 이 프레젠테이션의 이미지
│   └── template/           # 새 프레젠테이션 템플릿
├── shared/                  # 공유 리소스
│   ├── components/         # Vue 컴포넌트
│   └── styles/             # CSS 스타일
├── scripts/                 # 유틸리티 스크립트
│   └── create-presentation.js
├── docs/                    # 문서
└── .github/workflows/       # GitHub Actions
```

## 주요 명령어

```bash
# 개발 서버 실행 (기본: comfyui)
pnpm dev

# 특정 프레젠테이션 개발 서버 실행
pnpm slidev presentations/<이름>/slides.md --open

# 새 프레젠테이션 생성
pnpm new <프레젠테이션-이름>

# 프로덕션 빌드
pnpm build

# PDF 내보내기
pnpm export
```

## 새 프레젠테이션 만들기

1. `pnpm new my-presentation` 실행
2. `presentations/my-presentation/slides.md` 편집
3. `.github/workflows/deploy.yml` 매트릭스에 프레젠테이션 이름 추가:
   ```yaml
   matrix:
     presentation: [comfyui, my-presentation]
   ```
4. `main` 브랜치에 push하면 자동 배포

## 필수 설정 사항

### routerMode: 'hash' (필수)
모든 프레젠테이션의 frontmatter에 `routerMode: 'hash'`를 반드시 포함해야 합니다 (GitHub Pages용):
```yaml
---
routerMode: 'hash'
---
```
이 설정이 없으면 직접 URL 접근 시 404 에러가 발생합니다.

### 이미지 경로
- 이미지는 `presentations/<이름>/public/images/`에 저장
- 절대 경로로 참조: `/images/파일명.png`
- GitHub Actions가 하위 디렉토리 배포를 위한 경로를 자동 변환

### Frontmatter 템플릿
```yaml
---
theme: light-icons
routerMode: 'hash'
title: 프레젠테이션 제목
transition: slide-left
mdc: true
aspectRatio: '16/9'
canvasWidth: 980
layout: intro
---
```

## GitHub Pages 배포

- `main` 브랜치에 push하면 자동 배포
- 각 프레젠테이션 URL: `https://AI-GameDev.github.io/slides/<프레젠테이션>/`
- 루트 인덱스 페이지에서 모든 프레젠테이션 목록 확인 가능
- 매트릭스 빌드: 각 프레젠테이션이 독립적으로 빌드

## 슬라이드 문법

### 슬라이드 구분자
`---`로 슬라이드를 구분합니다:
```markdown
---
layout: intro
---
# 슬라이드 제목

---

# 다음 슬라이드
```

### 주요 레이아웃
- `default` - 기본 레이아웃
- `intro` - 타이틀/인트로 슬라이드
- `center` - 중앙 정렬
- `image-right` / `image-left` - 이미지와 텍스트
- `two-cols` - 2단 레이아웃

### 클릭 애니메이션
```markdown
<v-clicks>

- 항목 1
- 항목 2
- 항목 3

</v-clicks>
```

### 코드 블록 하이라이팅
````markdown
```python {2-3}
def hello():
    print("Hello")  # 하이라이트
    return True     # 하이라이트
```
````

### 이미지 레이아웃
frontmatter에서 배경 이미지 사용:
```yaml
---
layout: dynamic-image
image: /images/my-image.png
---
```

### Mermaid 다이어그램
````markdown
```mermaid
flowchart LR
    A[시작] --> B[처리]
    B --> C[끝]
```
````

## 참고 링크

- [Slidev 공식 문서](https://sli.dev/)
- [Addon 갤러리](https://sli.dev/resources/addon-gallery) — 커뮤니티 addon 목록
- [테마 갤러리](https://sli.dev/resources/theme-gallery) — 사용 가능한 테마 목록
- [NPM에서 addon 검색](https://www.npmjs.com/search?q=slidev-addon) — `slidev-addon-*` 키워드로 검색
- Addon 사용법: frontmatter에 `addons: [addon-name]` 추가

## 문제 해결

### 로컬 vs 프로덕션 환경

| 항목 | 로컬 | 프로덕션 |
|------|------|----------|
| URL 형식 | `localhost:3030/1` | `...github.io/slides/name/#/1` |
| 이미지 경로 | `/images/...` | 자동 변환 |
| 라우터 모드 | history | hash (필수) |

### 이미지가 표시되지 않을 때
1. 경로가 `/images/파일명.png` (절대 경로)인지 확인
2. `presentations/<이름>/public/images/`에 파일이 존재하는지 확인
3. 브라우저 강력 새로고침 (Cmd+Shift+R / Ctrl+Shift+R)

### 빌드 실패 시
1. GitHub Actions 로그 확인
2. `slides.md`의 YAML frontmatter가 유효한지 확인
3. 참조된 모든 이미지가 존재하는지 확인

### 직접 URL 접근 시 404 에러
1. frontmatter에 `routerMode: 'hash'`가 있는지 확인
2. URL이 `.../1`이 아닌 `.../#/1` 형태인지 확인

## Image Analysis Workflow

- 이미지 파일 분석이 필요할 때는 항상 Gemini CLI 헤드리스 모드를 사용
- 명령어 패턴: `gemini --include-directories "이미지가_있는_디렉토리" -p "분석 프롬프트 @이미지경로"`
- 이미지 경로는 절대 경로를 사용
- 공백 있는 경로는 백슬래시(\ )로 이스케이프
- Gemini CLI 경로: /Users/mingyukim/.nvm/versions/node/v24.12.0/bin/gemini
- 외부 폴더 접근 시 반드시 `--include-directories` 플래그 사용
