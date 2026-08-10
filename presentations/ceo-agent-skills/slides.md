---
theme: slidev-theme-tahta
routerMode: 'hash'
mdc: true
aspectRatio: '16/9'
canvasWidth: 980
themeConfig:
  variant: soft
  accent: '#0f766e'
layout: cover
kicker: 아이유노글로벌 · CEO 교육 2 / 5
title: AI 직원에게 <span class="accent2">매뉴얼</span>을 주는 법
subtitle: Claude Code 스킬 (Agent Skills)
---

<!-- 발표자 — 김민규. 지난 시간에 잡은 프레임을 그대로 이어받습니다. AI = 채용한 직원, CLAUDE.md = 사규집. 오늘은 그 직원에게 업무 매뉴얼을 주는 법입니다. -->

---
layout: statement
kicker: 여는 질문
title: 우리 회사에서, 같은 설명을 <em>매번</em> 반복하고 있는 일은 무엇입니까?
---

<!-- 답을 바로 받지 말고 3초쯤 두세요. 각자 머릿속에 떠오른 그 업무가 오늘 만들 첫 번째 스킬 후보입니다. -->

---
layout: default
kicker: 예를 들면
title: 사람에게도, AI에게도 <span class="accent2">매번 처음부터</span> 설명하고 있다
---

- 월 마감 보고서 양식
- 제안서에 꼭 들어가야 하는 항목
- 우리 회사 색상 · 폰트 · 말투
- 계약서 검토할 때 확인하는 목록

<Callout icon="lucide:repeat-2">네 가지 모두 <strong>이미 정해져 있는데</strong>, 정해진 그 내용이 문서가 아니라 <strong>사람 머릿속</strong>에 있다.</Callout>

<!-- 이 목록은 예시일 뿐입니다. 참석자가 방금 떠올린 업무를 한두 개 물어서 여기에 얹으면 훨씬 잘 붙습니다. -->

---
layout: vs
kicker: 지난 시간에서 오늘로
title: 채용했고, 사규집을 줬다. 이제 <span class="accent2">매뉴얼</span> 차례
label: →
left:
  title: 지난 시간
  items:
    - AI를 직원으로 채용했다
    - CLAUDE.md로 사규집을 만들었다
    - 상시로 적용되는 규칙
right:
  title: 오늘
  items:
    - 그 직원에게 업무 매뉴얼을 준다
    - 특정 업무의 절차를 적어둔다
    - 필요할 때만 꺼내 쓰는 문서
---

<!-- 사규집과 매뉴얼은 회사에서도 다른 문서입니다. 하나는 늘 적용되고, 하나는 그 업무를 할 때만 펼칩니다. 이 구분이 오늘 내용의 뼈대입니다. -->

---
layout: section
index: "01"
kicker: Part 1
title: 스킬이란 무엇인가
subtitle: 코드가 아니라 글입니다
---

<!-- 개념 → 비유 → 실체 → 작동 방식 순으로 갑니다. -->

---
layout: define
kicker: 용어
term: 스킬 (Skill)
definition: AI에게 특정 업무를 하는 방법을 미리 적어둔 <span class="accent2">폴더</span>
points:
  - 필요한 건 그 안의 파일 하나 — SKILL.md
  - 내용은 코드가 아니라 글 — "이 일은 이런 순서로 한다"
  - 한 번 써두면 계속 재사용된다
---

<!-- 여기서 가장 중요한 문장은 "프로그래밍이 아니라 매뉴얼 작성이다"입니다. 경영자가 직접 쓸 수 있는 종류의 문서라는 점을 분명히 해주세요. -->

---
layout: two-cols
kicker: 비유로 보면
title: 사규집은 <span class="accent2">얇아야</span> 하고, 매뉴얼은 두꺼워도 된다
---

- <Kbd>CLAUDE.md</Kbd> = **사규집** · 스킬 = **서랍 속 업무 매뉴얼**
- 사규집은 얇아야 한다 — **매번 읽으니까**
- 매뉴얼은 두꺼워도 된다 — **필요할 때만 꺼내니까**

<Callout icon="lucide:info">공식 용어가 아니라, 이해를 돕기 위한 <strong>비유</strong>다.</Callout>

::right::

<Figure src="/images/ceo2-01-rulebook-vs-drawer.png" alt="항상 펼쳐져 있는 CLAUDE.md 책과, 필요할 때만 꺼내는 스킬 서랍장" />

<!-- 사규집에 모든 업무 절차를 다 적으면 아무도 안 읽습니다. 회사에서 이미 겪어본 문제라 설명이 빨리 붙습니다. -->

---
layout: default
kicker: 스킬 한 개의 실체
title: 폴더 하나, 그 안에 <span class="accent2">파일 하나</span>
---

<FileTree :items="[{name: '월간보고서', children: [{name: 'SKILL.md'}]}]" />

<Kbd>SKILL.md</Kbd> 안에 들어가는 것은 두 가지뿐이다

- **① 이 매뉴얼은 무슨 일에 쓰는가** — 한두 줄
- **② 그 일을 어떻게 하는가** — 본문

<Callout icon="lucide:file-text">확장자 <strong>.md</strong> 는 <strong>마크다운</strong> — 서식이 조금 붙은 <strong>글 파일</strong>이다. 메모장으로도 열린다.</Callout>

<!-- 실제로 SKILL.md 파일 하나를 열어서 보여주면 가장 효과가 큽니다. "이게 전부입니다"라는 인상이 남아야 합니다. -->

---
layout: two-cols
kicker: 어떻게 알아서 꺼내 쓰나
title: 표지만 읽고 있다가, <span class="accent2">필요하면</span> 펼친다
---

<Figure src="/images/ceo2-02-progressive-disclosure.png" alt="제목만 본다 → 필요하면 펼친다 → 더 필요하면 더 꺼낸다" />

::right::

- 상시로 보고 있는 것은 **제목과 한 줄 소개**뿐이다
- 본문과 참고 문서는 **그 업무가 생겼을 때** 꺼낸다
- 사용자가 스킬 이름을 부르지 않아도 된다

<Callout icon="lucide:book-open">공식 용어 — <strong>점진적 공개 (progressive disclosure)</strong></Callout>

<!-- 도서관 사서가 모든 책을 외우고 있는 게 아니라 서가 목록만 알고 있는 것과 같습니다. 이 구조가 다음 슬라이드의 결론으로 이어집니다. -->

---
layout: two-cols
kicker: 그래서 쌓을수록 이득이다
title: 매뉴얼이 늘어날수록 <span class="accent2">유리해진다</span>
---

- 쓰지 않는 매뉴얼은 **비용이 거의 들지 않는다**
- 즉, **버리지 않고 계속 쌓아도 되는 자산**이다

<Callout icon="lucide:trending-up" tone="good"><strong>경영 관점의 함의</strong> — 매뉴얼은 늘어날수록 무거워지는 게 보통인데, 여기서는 <strong>늘어날수록 유리해진다</strong>.</Callout>

::right::

<Figure src="/images/ceo2-03-stack-more-is-better.png" alt="설치한 스킬 수가 늘어도 평소 차지하는 자리는 거의 늘지 않는다" caption="보통 예상(점선) vs 실제(실선)" />

<!-- 문서 관리 비용이 문서 수에 비례하지 않는다는 것이 이 구조의 핵심 이점입니다. 사내 위키가 커질수록 아무도 안 보게 되는 문제와 대비시켜 주세요. -->

---
layout: vs
kicker: 잘 꺼내 쓰게 하려면
title: 매뉴얼 <span class="accent2">표지 한 줄</span>이 전부를 좌우한다
label: →
left:
  title: ❌ 이렇게 쓰면 안 꺼내 쓴다
  items:
    - "\"문서 관련 도움\""
    - 무엇을 하는지 알 수 없다
    - 언제 쓰는지도 알 수 없다
right:
  title: ✅ 이렇게 써야 꺼내 쓴다
  items:
    - "\"월간 실적 보고서를 회사 표준 양식으로 작성한다.\""
    - "\"사용자가 월 마감·실적 보고를 요청할 때 사용한다.\""
    - 무엇을 하는가 + 언제 쓰는가
---

<!-- 스킬을 만들었는데 안 불려 나온다면 열에 아홉은 이 한 줄이 부실한 경우입니다. 두 가지를 반드시 함께 적어야 합니다. -->

---
layout: section
index: "02"
kicker: Part 2
title: 실제로 뭐가 나오나
subtitle: 설치 없이 지금 바로 쓸 수 있는 것들
---

<!-- 개념에서 결과물로 넘어가는 지점입니다. -->

---
layout: panels
kicker: 별도 설치 없이 바로 쓸 수 있는 문서 작업 스킬
title: 기본으로 들어있는 <span class="accent2">매뉴얼</span>
panels:
  - icon: "lucide:sheet"
    title: xlsx
    items:
      - 엑셀 생성 · 편집
      - 수식 · 서식
  - icon: "lucide:file-type"
    title: docx
    items:
      - 워드 문서
      - 표 · 목차 · 변경 추적
  - icon: "lucide:file-text"
    title: pdf
    items:
      - 텍스트 · 표 추출
      - 양식 채우기 · 병합 · 분할
  - icon: "lucide:presentation"
    title: pptx
    items:
      - 슬라이드 생성 · 편집
      - 차트 · 레이아웃
---

<!-- 그 외에 공개 저장소에는 브랜드 가이드, 내부 커뮤니케이션 문서, 문서 공동 작성 같은 스킬이 있습니다. 발표 전에 github.com/anthropics/skills 에서 목록이 바뀌지 않았는지 한 번 확인하세요. -->

---
layout: steps
kicker: Before / After
title: 말로 시키면 <span class="accent2">파일</span>이 나온다
steps:
  - title: 지시
    desc: "\"12개월 판매 데이터를 요약하고, 비용을 분류별로 합산해서 고위험 항목은 빨간색으로 표시한 엑셀 파일로 만들어줘\""
    icon: "lucide:message-square"
  - title: 결과
    desc: 수식과 서식이 들어간 .xlsx 파일
    icon: "lucide:file-check"
  - title: 다음 달
    desc: 데이터만 갈아끼우면 끝
    icon: "lucide:repeat"
---

<!-- 세 번째 칸이 오늘 이야기의 요점입니다. 첫 달의 결과물이 아니라, 다음 달에 반복 비용이 0에 가까워진다는 것이 스킬의 가치입니다. -->

---
layout: bigtype
kicker: 라이브 데모
title: 직접 <em>보시겠습니다</em>
subtitle: 요청 한 줄 → 파일 생성까지
---

<!-- 여기서 화면을 전환합니다. 강조할 것 하나 — 사용자는 스킬 이름을 몰라도 됩니다. 말로 시키면 알아서 꺼내 씁니다. 데모가 끝나면 다음 슬라이드로 돌아옵니다. -->

---
layout: section
index: "03"
kicker: Part 3
title: 직접 만들어보기
subtitle: 빈 종이에서 시작하지 않습니다
---

<!-- 여기서부터 실습입니다. 노트북을 열어주세요. -->

---
layout: default
kicker: 만드는 순서
title: 매뉴얼을 <span class="accent2">먼저</span> 쓰는 게 아니다
---

<Figure src="/images/ceo2-04-three-steps.png" alt="한 번 시켜본다 → 스킬로 굳힌다 → 한 줄로 부른다" caption="한 번 시켜보고, 그 과정을 굳힌다" />

<!-- 사람 직원에게도 같습니다. 한 번 같이 해보고 나서 매뉴얼을 적지, 해보지도 않은 일의 매뉴얼을 먼저 쓰지는 않습니다. -->

---
layout: code-explain
kicker: ① 한 번 시켜본다
title: 여기까지는 <span class="accent2">평소 하던 대화</span>다
notes:
  - "<strong>원하는 결과 만들기</strong> — 먼저 내용부터 뽑는다."
  - "<strong>형식까지 정해주기</strong> — 파일 이름과 형태를 지정한다."
  - "<strong>마음에 들 때까지 말로 고친다</strong> — 이 대화가 그대로 매뉴얼 초안이 된다."
---

```bash
https://www.aitimes.com/ 페이지의 내용을 확인하고
최신 뉴스 한 개만 요약 정리해줘.

이 요약 내용을 [뉴스 제목].md로 해서
마크다운 형태로 정리해줘.
```

<!-- 특별한 것이 없다는 점을 강조하세요. 스킬을 만들겠다는 생각 없이 그냥 일을 시킨 것뿐입니다. 결과가 마음에 들 때까지 말로 고치는 것까지가 이 단계입니다. -->

---
layout: code-explain
kicker: ② 스킬로 굳힌다
title: 방금까지의 작업을 읽고 <span class="accent2">대신 써 준다</span>
notes:
  - "<strong>skill-creator</strong> — 스킬 만드는 것을 돕는 스킬. 대화하듯 만들어 준다."
  - "<strong>범위 지정</strong> — project로 하면 현재 폴더에서만 쓰인다."
  - "<strong>결과</strong> — SKILL.md 를 대신 작성해 준다."
---

```bash
/skill-creator 지금까지 한 작업을 스킬로 만들어줘.
스킬은 현재 폴더에서만 사용할 거야. project 범위로 만들어줘.
```

<!-- skill-creator는 공식 마켓플레이스 플러그인입니다. 미설치 상태면 이 명령이 아예 없습니다 — 발표 전에 반드시 확인하고, 없으면 /plugin install skill-creator@claude-plugins-official 로 먼저 설치해 두세요. -->

---
layout: compare
kicker: 어디에 만들 것인가
title: 나만 쓸 것인가, <span class="accent2">팀에 넘길</span> 것인가
columns: [범위, 저장 위치, 적용]
rows:
  - { metric: 개인, before: "~/.claude/skills/", after: 내 모든 작업에서 }
  - { metric: 프로젝트, before: ".claude/skills/", after: 이 폴더에서만 }
---

<!-- 회사 업무용이라면 프로젝트 범위를 권합니다. 스킬이 폴더 안에 들어 있으니 폴더째 팀에 넘길 수 있고, 저장소에 올리면 그대로 공유됩니다. 개인 범위는 내 노트북에만 남습니다. -->

---
layout: default
kicker: 만든 스킬을 지금 세션에 반영하기
title: 알아둘 명령 <span class="accent2">세 개</span>
---

<Terminal title="claude" :lines="[{cmd: '/reload-skills'}, {out: '방금 디스크에 생긴 스킬을 이 세션에서 바로 인식시킨다'}, {cmd: '/skills'}, {out: '사용 가능한 스킬 목록 확인 — 목록만, 재적용 기능은 없다'}, {cmd: '/스킬이름'}, {out: '스킬을 직접 호출한다'}]" />

<Callout icon="lucide:refresh-cw">스킬은 대개 세션 중 자동으로 인식된다. 그래도 <strong>빈 폴더에서 첫 스킬을 만든 직후</strong>에는 <strong>/reload-skills</strong> 를 한 번 넣어 두는 편이 안전하다.</Callout>

<!-- 참석자 버전이 낮으면 /reload-skills 가 없을 수 있습니다. 그 경우 Claude Code를 재시작하면 같은 효과입니다. -->

---
layout: two-cols
kicker: ③ 다음부터는 한 줄
title: 앞의 대화 전체가 <span class="accent2">이 한 줄</span>로 줄었다
---

<Kbd>/aitimes-news-summary</Kbd>

- 이름을 몰라도 된다 — <strong>"aitimes 최신 뉴스 정리해줘"</strong> 라고 말해도 알아서 꺼내 쓴다
- 다른 사람이 같은 일을 해도 **같은 결과**가 나온다

::right::

<Figure src="/images/ceo2-06-long-to-oneline.png" alt="여러 번의 긴 대화가 한 줄로 줄어드는 그림" caption="처음 → 스킬로 만든 뒤" />

<!-- 스킬 이름은 만들 때 정해집니다. 이 슬라이드의 /aitimes-news-summary 는 예시이므로, 데모에서 실제로 만들어진 이름과 맞는지 발표 직전에 확인하세요. -->

---
layout: compare
kicker: 무엇이 달라졌나
title: 결과가 <span class="accent2">사람에 관계없이</span> 같아진다
columns: [구분, 처음, 스킬로 만든 뒤]
rows:
  - { metric: 결과 형식, before: 그때그때 다름, after: 항상 같음 }
  - { metric: 다른 사람이 할 때, before: 같은 설명을 다시, after: 같은 한 줄 }
  - { metric: 소요 시간, before: 대화 여러 번, after: 한 줄 }
---

<!-- 표준화의 실체가 이 표입니다. 품질이 올라가는 것보다 편차가 사라지는 것이 경영 관점에서 더 큰 효과입니다. -->

---
layout: statement
kicker: 이 섹션의 결론
title: 방금 만든 것은 프로그램이 아니라 <em>글 한 장</em>이다. 그런데 그 글을 읽고 일하는 직원이 생겼다.
---

<!-- 여기서 한 박자 쉬어 주세요. 오늘 교육에서 가장 중요한 문장입니다. -->

---
layout: section
index: "04"
kicker: Part 4
title: 조직에 어떤 변화가 생기나
subtitle: "이게 우리 회사에 무슨 의미가 있는가?"
---

<!-- 실습에서 경영 판단으로 넘어갑니다. -->

---
layout: two-cols
kicker: 머릿속에 있던 것이 자산이 된다
title: 회사에 <span class="accent2">남고 · 쌓이고 · 물려줄 수</span> 있다
---

<Figure src="/images/ceo2-07-head-to-files.png" alt="사람 머릿속에 있던 문서가 회사의 파일로 옮겨가는 그림" />

::right::

**지금** — "그건 김 팀장이 제일 잘 알아요" · 담당자가 바뀌면 품질이 흔들린다

**스킬로 만들면** — 회사에 남는다 · AI가 그대로 **실행까지** 한다

<Callout icon="lucide:key">매뉴얼은 원래도 만들 수 있었다. 달라진 것은 <strong>그 매뉴얼을 읽고 실행하는 주체가 생겼다</strong>는 점이다.</Callout>

<!-- 이 Callout이 이 슬라이드의 핵심입니다. 문서화 자체는 새로운 얘기가 아닙니다 — 실행하는 독자가 생겼다는 것이 새로운 부분입니다. -->

---
layout: feature
kicker: 반복되고, 양식이 정해져 있고, 사람마다 결과가 다른 일
title: 세 가지 <span class="accent2">효과</span>
columns: 3
features:
  - { icon: "lucide:ruler", title: 표준화, desc: 보고서 양식 · 브랜드 색상 · 검토 기준이 사람에 관계없이 일정 }
  - { icon: "lucide:users", title: 인수인계, desc: 담당자 교체 시, 인수인계 문서가 곧 실행 가능한 매뉴얼 }
  - { icon: "lucide:circle-slash", title: 반복 제거, desc: 같은 설명을 다시 하지 않음 — 한 번 쓰고 계속 사용 }
---

<!-- 세 가지 중 어느 것이 우리 회사에 가장 급한지 물어보면 다음 슬라이드로 자연스럽게 넘어갑니다. -->

---
layout: reference
kicker: 공통 조건 — 반복되고, 양식이 정해져 있고, 사람마다 결과가 다른 일
title: 부서별로 <span class="accent2">먼저 만들 만한</span> 스킬
items:
  - { term: 재무, desc: 월 마감 리포트 양식 · 비용 분류 기준 }
  - { term: 마케팅, desc: "브랜드 가이드(색 · 폰트 · 말투) · 분기 실적 덱" }
  - { term: 인사, desc: 지원자 정보 → 평가 양식 입력 · 공고 템플릿 }
  - { term: 커뮤니케이션, desc: 주간 업무 보고 · 사내 공지 형식 }
  - { term: 영업, desc: 제안서 구성 · 고객사 리포트 }
---

<!-- 참석자에게 자기 부서 항목을 보게 하고, 여기 없는 것을 하나씩 말하게 하면 마지막 액션 아이템으로 바로 연결됩니다. -->

---
layout: section
index: "05"
kicker: Part 5
title: 정리, 그리고 왜 지금인가
subtitle: 헷갈리는 세 가지와 업계의 변화
---

<!-- 개념 정리 후 타이밍 이야기로 갑니다. -->

---
layout: default
kicker: 헷갈리는 것 정리
title: 딱 <span class="accent2">세 가지</span>만 구분하면 된다
---

<Figure src="/images/ceo2-05-three-concepts.png" alt="CLAUDE.md 늘 지키는 규칙 · 스킬 업무의 절차 · MCP 외부와 연결" caption="MCP는 망치를 쥐여주는 것, 스킬은 망치 쓰는 법 설명서 — 공식 용어가 아닌 비유다" />

<!-- CLAUDE.md는 항상 읽히는 사규집, 스킬은 필요할 때 꺼내는 업무 매뉴얼, MCP는 사내 DB나 슬랙 같은 외부 시스템에 연결하는 통로입니다. MCP는 5회차에서 따로 다룹니다. -->

---
layout: two-cols
kicker: 왜 지금인가
title: 스킬 규격이 <span class="accent2">업계 표준</span>이 됐다
---

<Figure src="/images/ceo2-08-open-standard.png" alt="여러 도구가 하나의 SKILL.md 형식으로 모이는 그림" />

::right::

**2025년 12월 18일** — Anthropic이 스킬 규격을 **오픈 표준**으로 공개

- 발표 직후 Microsoft · OpenAI · GitHub · Figma · Cursor 등이 채택
- Canva · Stripe · Notion · Zapier가 제작한 스킬 제공
- 2026년 3월 기준 **30여 개 도구**가 같은 형식을 읽는다

<!-- 채택 도구 수는 서드파티 집계라 시점에 따라 변동합니다. 정확한 숫자보다 "여러 진영이 같은 형식을 쓴다"는 사실이 요점입니다. -->

---
layout: bigtype
kicker: 경영 관점의 의미
title: 한 번 만든 매뉴얼이, AI 도구를 <em>바꿔도 남는다</em>
subtitle: 특정 업체에 묶이지 않는다 — 도구는 계속 바뀌어도 자산은 이전 가능하다
---

<!-- 지금 쌓기 시작하는 것이 손해가 아닌 이유입니다. 도구 선택을 미루는 것이 오히려 비용이라는 얘기로 이어집니다. -->

---
layout: section
index: "06"
kicker: Part 6
title: 리스크와 우리가 정할 규칙
subtitle: 편리한 만큼 확인할 것이 있습니다
---

<!-- 마지막 파트입니다. 여기서 나오는 규칙 3줄이 오늘의 실질적 결재 사항입니다. -->

---
layout: default
kicker: 반드시 알고 계셔야 할 것
title: 스킬은 AI 직원의 <span class="accent2">권한을 그대로</span> 물려받는다
---

- 매뉴얼에 적힌 내용을 **의심 없이 수행**한다
- 파일을 읽을 수 있는 직원이라면, 매뉴얼도 **파일을 읽게 시킬 수 있다**
- 악의적인 지시는 **평범한 문장 몇 줄**로 숨길 수 있어, 기존 보안 검사로 걸러지지 않는다

<Callout tone="warn" icon="lucide:triangle-alert">비유하자면 <strong>앱스토어</strong>다 — 편리하지만, <strong>만든 사람을 보고 설치해야 한다</strong>.</Callout>

<!-- 스킬은 코드가 아니라 글이기 때문에 오히려 위험합니다. 백신이 잡을 수 있는 형태가 아닙니다. 이 점이 다음 슬라이드의 통계로 이어집니다. -->

---
layout: two-cols
kicker: 실제로 일어난 일
title: 이론적 우려가 아니라 <span class="accent2">이미 관측된</span> 사건이다
---

- 2026년 2월 기준, 공개 스킬 저장소 **3,984개를 감사**한 결과다
- 같은 시기 **335개 이상의 악성 스킬**이 인기 스킬로 위장해 정보 탈취 악성코드를 유포한 사례가 확인됐다

<Callout tone="warn" icon="lucide:shield-alert">감사 대상의 <strong>13.4%</strong> 에서 심각한 보안 결함, <strong>36%</strong> 에서 악의적 지시 삽입 정황.</Callout>

::right::

<Figure src="/images/ceo2-09-security-stats.png" alt="심각한 보안 결함 13.4%, 악의적 지시 삽입 정황 36% 도넛 차트" />

<!-- 출처 — Snyk, 2026-02-05 기준. 악성 스킬 유포는 ClawHavoc 캠페인, 2026년 2월. 숫자를 외우실 필요는 없고, "이미 벌어진 일"이라는 점만 남으면 됩니다. -->

---
layout: feature
kicker: 오늘 결재하실 것
title: 우리 회사 규칙 <span class="accent2">3줄</span>
columns: 3
features:
  - { icon: "lucide:package-check", title: 기본 · 사내 우선, desc: 기본 제공 스킬과 사내에서 만든 스킬을 우선 사용한다 }
  - { icon: "lucide:ban", title: 출처 불명 금지, desc: 출처가 불분명한 스킬은 설치하지 않는다 }
  - { icon: "lucide:user-check", title: 담당자 승인, desc: 외부 스킬 도입 시 담당자가 내용을 열어보고 승인한다 }
---

<!-- 세 줄이면 충분합니다. 복잡한 보안 정책을 만들면 아무도 안 지킵니다. -->

---
layout: default
kicker: 승인 담당자가 열어볼 때
title: 확인할 <span class="accent2">위험 신호</span>
---

<Tags :items="['실행 스크립트 포함', '외부 주소로 데이터 전송', '비밀번호 · API 키가 적혀 있음', '&quot;숨겨서&quot;', '&quot;확인 없이&quot;']" />

- 스킬은 **글 파일**이므로, 담당자가 **직접 열어서 읽을 수 있다**
- 읽어서 이해되지 않는 문장이 있다면 **그것이 곧 신호**다

<Callout icon="lucide:eye">전문 지식이 필요한 검토가 아니다 — <strong>한글로 읽어보고 이상하면 반려</strong>하면 된다.</Callout>

<!-- 이 점이 경영자에게 중요합니다. 보안 검토를 개발자에게만 맡길 필요가 없습니다. 글이니까 누구나 읽을 수 있습니다. -->

---
layout: steps
kicker: 마무리
title: 다음에 할 <span class="accent2">일</span>
steps:
  - title: 반복 업무 하나를 고른다
    desc: 가장 자주 하고, 양식이 정해져 있고, 사람마다 결과가 다른 일
    icon: "lucide:target"
  - title: 그 업무를 스킬로 만들어본다
    desc: 앞에서 본 순서 그대로 — 한 번 시켜보고, skill-creator로 굳힌다
    icon: "lucide:hammer"
  - title: 세 가지를 정한다
    desc: 사내 스킬을 어디에 모을 것인가 · 누가 승인할 것인가 · 어느 부서부터 시작할 것인가
    icon: "lucide:clipboard-check"
---

<!-- 세 번째가 오늘 자리에서 결정하실 수 있는 부분입니다. 부서 하나만 정해도 충분합니다. -->

---
layout: bigtype
kicker: 오늘의 한 문장
title: 일하는 방식을 글로 적어두면, 그걸 읽고 <em>실행하는 직원</em>이 생겼습니다.
---

<!-- 여기서 마칩니다. 다음 시간은 서브에이전트입니다. -->

---
layout: end
title: 고맙습니다
subtitle: 반복 업무 하나를 고르는 것부터 시작하시면 됩니다
contact: 김민규 · 아이유노글로벌 CEO 교육 2 / 5
---
