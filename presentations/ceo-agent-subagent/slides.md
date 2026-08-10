---
theme: slidev-theme-tahta
routerMode: 'hash'
colorSchema: 'light'
mdc: true
aspectRatio: '16/9'
canvasWidth: 980
themeConfig:
  variant: soft
  accent: '#0f766e'
layout: cover
kicker: 아이유노글로벌 · CEO 교육 3 / 5
title: 서브에이전트
subtitle: AI에게 일을 <span class="accent2">떼어 맡기는</span> 법
---

<!-- 발표자 — 김민규. 오늘은 기능 소개가 아니라, AI가 일하는 자리가 어떻게 생겼는지 보는 시간입니다. 청중이 이미 클로드 코드를 쓰고 있으면 앞의 비유 구간을 압축하고 "직접 보기"로 빨리 넘어가세요. -->

---
layout: default
kicker: 오늘 답할 질문 하나
title: 왜 갈수록 <em>헤매고</em>, 뭘로 푸는가
---

<v-clicks>

- 오늘은 **기능 소개가 아니다**
- **AI가 일하는 자리**가 어떻게 생겼는지 보는 시간이다
- 이걸 알면 **속도와 비용**이 달라진다

</v-clicks>

<Callout v-click icon="lucide:target">질문은 하나입니다 — 왜 갈수록 헤매는가, 그리고 무엇으로 푸는가.</Callout>

<!-- 오늘 하나만 가져가신다면 이 질문입니다. 뒤에 나오는 모든 장면은 이 두 가지에 대한 답입니다. -->

---
layout: section
index: "01"
kicker: Part 1
title: AI의 책상
subtitle: 성능이 아니라, 자리의 문제입니다
---

<!-- 여기서 오늘의 유일한 전문용어가 나옵니다. 딱 한 번만 쓰고, 이후로는 계속 "책상"이라고 부르겠습니다. -->

---
layout: vs
kicker: 겪어보셨을 장면
title: 성능이 나빠진 게 아니라, <span class="accent2">자리가 좁아진</span> 것이다
label: →
left:
  title: 처음엔 잘한다
  items:
    - 시키는 대로 정확히 한다
    - 맥락도 잘 잡는다
right:
  title: 그런데 대화가 길어지면
  items:
    - 앞에서 말한 걸 다시 물어본다
    - 이미 고친 걸 또 고친다
    - 답이 느려지고, 요금은 올라간다
---

<!-- 다들 겪어보셨을 장면입니다. 여기서 대부분 "모델이 멍청해졌나" 하고 생각하시는데, 그게 아닙니다. 자리가 좁아진 겁니다. -->

---
layout: diagram
kicker: 오늘의 유일한 전문용어
title: 사람은 치우면서 일하고, AI는 <span class="accent2">펼친 걸 그대로 둔다</span>
note: 사람의 한계는 <strong>피로</strong>지만, AI의 한계는 <strong>넓이가 정해져 있다는 것</strong>이다.
---

<Figure src="/images/ceo3-01-two-desks.png" alt="사람의 책상은 정리되어 있고 AI의 책상은 문서로 가득 찬 비교 그림" />

<!-- 사람은 다 본 서류를 치웁니다. AI는 안 치웁니다. 한 번 펼친 것은 대화가 끝날 때까지 그대로 책상 위에 남아 있습니다. -->

---
layout: define
kicker: 용어 — 오늘 딱 한 번만
term: 컨텍스트 윈도우
definition: AI가 한 번에 <span class="accent2">펼쳐놓을 수 있는 책상의 넓이</span>
points:
  - 영어로는 Context Window — 앞으로는 그냥 "책상"이라고 부릅니다
  - 넓이는 정해져 있고, 스스로 치우지 않습니다
---

<!-- 전문용어는 이것 하나입니다. 여기서 한 번 말하고, 이후 끝까지 "책상"으로 통일합니다. 용어를 외우실 필요는 없습니다. -->

---
layout: diagram
kicker: 책상이 차면 벌어지는 일
title: 길어질수록 느리고, <span class="accent2">비싸지고, 부정확해진다</span>
note: 실패한 시도 · 긴 로그 · 다시 볼 일 없는 검색 결과가 <strong>그대로 남아</strong>, 매 응답마다 부담으로 얹힌다.
---

<Figure src="/images/ceo3-02-desk-filling.png" alt="빈 책상이 점점 문서로 가득 차면서 정확도 하락과 비용 상승으로 이어지는 그림" />

<!-- 쌓인 내용은 사라지지 않고 매번 다시 얹힙니다. 그래서 대화가 길어질수록 느려지고, 요금이 올라가고, 답이 흐려집니다. -->

---
layout: section
index: "02"
kicker: Part 2
title: 위임이라는 해법
subtitle: 더 똑똑하게 만드는 게 아니라, 책상을 정리합니다
---

<!-- 문제를 봤으니 해법입니다. 해법은 AI를 더 똑똑하게 만드는 쪽이 아닙니다. -->

---
layout: define
kicker: 해법
term: 서브에이전트 (Subagent)
definition: 곁가지 일을 <span class="accent2">다른 책상에서</span> 처리하고, <span class="accent2">결과만</span> 가져오는 도우미
points:
  - 도우미는 자기 책상에서 파일 수십 개를 뒤진다
  - 내 책상에는 정리된 결과 한 장만 올라온다
  - AI가 더 똑똑해지는 기능이 아니라, 책상을 정리하는 기능이다
---

<!-- 핵심은 마지막 줄입니다. 성능을 올리는 기능이 아니라 자리를 지키는 기능입니다. -->

---
layout: diagram
kicker: 위임이라는 그림
title: 뒤지는 건 저쪽 책상, 올라오는 건 <span class="accent2">결과 한 장</span>
note: 지시서를 보내고, 정리된 결과 한 장을 받는다. 그 사이에 오간 수십 장의 원문은 <strong>내 책상에 올라오지 않는다</strong>.
---

<Figure src="/images/ceo3-03-delegate-desk.png" alt="내 책상에서 지시서를 보내고 도우미 책상에서 결과 한 장만 돌아오는 그림" />

<!-- 이 그림이 오늘 강의의 중심 이미지입니다. 왼쪽이 깨끗하게 유지되는 것이 목적입니다. -->

---
layout: diagram
kicker: 비유입니다
title: 가방에 <span class="accent2">담기지 않는 것</span>이 중요하다
note: <strong>규칙은 자동, 상황은 수동</strong> — 회사 규정은 알아서 챙겨 가지만, 지금까지 나눈 대화는 모른다.
---

<Figure src="/images/ceo3-04-what-carries.png" alt="회사 규정과 지시서는 가방에 담기지만 지금까지 나눈 대화는 담기지 않는 그림" />

<!-- 이건 비유라고 반드시 말로 짚어주세요. "AI 직원을 채용한다" 같은 자율성을 암시하는 표현은 피합니다. 그리고 "아무것도 모른다"고 뭉뚱그리지 마세요 — 공통 규칙 문서(CLAUDE.md)와 git 상태는 자동으로 따라가고, 대화 이력만 안 따라갑니다. 실무 사고는 대부분 여기서 납니다. -->

---
layout: section
index: "03"
kicker: Part 3
title: 직접 보기
subtitle: 지금부터는 말이 아니라 화면입니다
---

<!-- 이 강의의 중심 구간입니다. 시간을 가장 많이 쓰는 곳입니다. 화면 전환 준비하세요. -->

---
layout: steps
kicker: 지금부터 직접 보여드립니다
title: <span class="accent2">4단계</span>로 봅니다
steps:
  - { title: 위임 없이, desc: 시켰을 때 — 책상이 더러워지는 장면, icon: "lucide:layers" }
  - { title: 위임해서, desc: 같은 일 — 결과 한 장만 돌아오는 장면, icon: "lucide:send" }
  - { title: 정체 확인, desc: 그 도우미는 대체 무엇인가, icon: "lucide:file-text" }
  - { title: 성격 변경, desc: 도우미의 성격을 바꾸는 법, icon: "lucide:sliders-horizontal" }
---

<!-- 네 장면입니다. 각 단계가 끝날 때마다 무엇을 봤는지 한 문장으로 정리하고 넘어가세요. -->

---
layout: code-explain
kicker: ① 위임 없이 시켜보기
title: 고객 피드백 문서가 쌓인 <span class="accent2">폴더 하나</span>
notes:
  - "<strong>파일을 하나씩 여는 기록</strong>이 계속 쌓인다."
  - "<strong>문서 원문</strong>이 화면을 가득 채운다."
  - "<strong>결론은 맨 마지막에</strong> 잠깐 나온다."
---

```text
이 폴더의 문서를 전부 읽고,
고객이 반복적으로 제기한 불만 3가지를 근거 문장과 함께 정리해줘.
```

<!-- 결과물 자체는 나쁘지 않습니다. 봐야 할 것은 결과가 아니라 화면에 쌓이는 양입니다. 스크롤을 올려서 원문이 얼마나 찼는지 보여주세요. -->

---
layout: default
kicker: ① 책상 사용량 확인
title: 방금 그 작업 하나로 <span class="accent2">얼마나 찼는지</span> 숫자로 본다
---

<Terminal title="claude" :lines="[{cmd: '/context'}]" />

- 방금 그 작업 하나로 책상이 얼마나 찼는지 **숫자로 나온다**
- 이 상태에서 다음 일을 시키면 — **좁은 책상 위에서** 시작하는 것이다
- 대화를 이어갈수록 이 숫자는 계속 올라간다

<!-- 이 숫자를 꼭 소리 내어 읽어주세요. 뒤에서 위임 후 숫자와 비교할 기준점입니다. -->

---
layout: code-explain
kicker: ② 같은 일을 위임하기
title: 앞의 <span class="accent2">/clear</span>로 책상을 비운 뒤
notes:
  - "도우미가 <strong>따로 일하는 표시</strong>가 뜬다."
  - "<strong>문서 원문은 내 화면에 안 올라온다.</strong>"
  - "<strong>정리된 결과만</strong> 돌아온다."
  - "<code>/context</code>로 다시 확인 → 책상이 훨씬 덜 찼다."
---

```text
서브에이전트에게 맡겨서 이 폴더의 문서를 조사하고,
고객이 반복적으로 제기한 불만 3가지만 요약해서 알려줘.
근거 문장은 각 항목당 한 줄이면 충분해.
```

<!-- 같은 폴더, 같은 목적입니다. 달라진 건 "서브에이전트에게 맡겨서" 한 마디뿐입니다. 실행 후 반드시 /context를 다시 실행해서 ①의 숫자와 나란히 비교해 주세요. -->

---
layout: diagram
kicker: 공식 문서의 컨텍스트 시뮬레이션 수치
title: 같은 일을 하고도 내 자리에 남는 건 <span class="accent2">15분의 1 이하</span>
note: 도우미는 <strong>6,100</strong>만큼 읽었지만, 내 책상에 올라온 건 <strong>420</strong>이다.
---

<Figure src="/images/ceo3-05-6100-vs-420.png" alt="도우미가 읽은 양 6,100과 내 책상에 올라온 양 420을 비교한 막대 그림" />

<!-- 6,100 / 420은 공식 컨텍스트 시뮬레이션 수치입니다 — 파일 읽기 6,100, 반환 420. 방금 화면에서 본 /context 차이와 같은 이야기라는 점을 연결해 주세요. -->

---
layout: code-explain
kicker: ③ 이 도우미의 정체
title: 채용 공고가 아니라, <span class="accent2">지시서 한 장</span>을 쓰는 일
notes:
  - "<strong>어디에</strong> — <code>~/.claude/agents/</code> 는 내 개인용 도우미 서랍이다."
  - "<strong>무슨 일을</strong> — 역할을 말로 설명하면 된다."
  - "<strong>어디까지</strong> — 읽기 전용, 고치기 불가로 제한한다."
  - "<strong>어느 급으로</strong> — 단순한 일이면 값싼 모델로."
---

```text
~/.claude/agents/ 에 '고객불만-요약'이라는
개인용 서브에이전트를 만들어줘.
폴더 안의 문서를 읽어서 반복되는 불만을 찾고,
근거 문장과 함께 정리하는 역할이야.
읽기 전용으로 만들고, 모델은 sonnet을 써줘.
```

<!-- 만들어달라고 말로 시키면 파일이 생깁니다. 여기가 ③④ 중 첫 번째 강한 장면입니다 — "채용이 아니라 지시서를 쓰는 것". -->

---
layout: code-explain
kicker: ③ 도우미 = 파일 한 장
title: 열어보면 <span class="accent2">이게 전부</span>다
notes:
  - "<strong>name</strong> — 이 도우미의 이름."
  - "<strong>description</strong> — 어떤 일에 부를지 판단하는 기준."
  - "<strong>tools</strong> — 쓸 수 있는 연장. 여기선 <strong>읽기만</strong>, 고치기 불가."
  - "<strong>model</strong> — 어느 급의 AI를 쓸지."
  - "<strong>아래 본문</strong> — 직무기술서. 여기가 진짜 내용이다."
---

````markdown {2|3|4|5|8-9}
---
name: 고객불만-요약
description: 문서 폴더에서 반복되는 고객 불만을 찾아 근거와 함께 정리
tools: Read, Grep, Glob
model: sonnet
---

당신은 고객 피드백 분석 담당입니다.
문서를 읽고 반복되는 불만을 찾아, 각 항목마다 근거 문장을 붙여 정리하세요.
````

<!-- 한 줄씩 클릭해서 넘기세요. 프로그램이 아니라 문서 한 장이라는 것이 요점입니다. 마지막 본문이 직무기술서에 해당합니다. -->

---
layout: two-cols
kicker: ④ 성격을 바꿔보면
title: 프로그램을 고친 게 아니라 <span class="accent2">지시서를 고친 것</span>
---

**지시서 본문에 한 줄 추가**

```text
불만을 심각도가 높은 순으로 정렬하고,
각 항목에 담당 부서를 추정해서 붙이세요.
```

- 같은 도우미, 같은 폴더
- **결과 형식만 바뀐다**

::right::

**이름을 직접 지목해서 재실행**

```text
@agent-고객불만-요약 이 폴더를 다시 분석해줘.
```

<Callout icon="lucide:at-sign"><code>@</code>로 이름을 지목하면 <strong>그 도우미가 반드시 실행된다.</strong> 그냥 말로 시키면 클로드가 알아서 판단한다.</Callout>

<!-- @agent- 지목이 실행을 보장합니다. 자연어 위임은 클로드의 판단이라 실패할 수 있으니 시연에서는 반드시 @로 지목하세요. 입력할 때 @를 치면 목록이 뜨므로 거기서 골라도 됩니다. -->

---
layout: agenda
kicker: 방금 보신 것
title: 기술 문제가 아니라 <span class="accent2">지시</span>의 문제다
items:
  - { topic: 위임 없이 시키면, desc: "내 책상이 더러워진다" }
  - { topic: 위임하면, desc: "결과만 올라온다" }
  - { topic: 도우미의 정체는, desc: "지시서 한 장이다" }
  - { topic: 성격은, desc: "지시서를 고쳐서 바꾼다" }
---

<!-- 네 장면을 한 문장씩으로 정리하고 넘어갑니다. 결론은 "지시를 얼마나 잘 쓰느냐"입니다. -->

---
layout: section
index: "04"
kicker: Part 4
title: 얻는 것과 내주는 것
subtitle: 공짜가 아닙니다
---

<!-- 여기서부터는 판단 기준입니다. 좋은 점만 말하고 끝내면 현장에서 오용됩니다. -->

---
layout: diagram
kicker: 저울에 올려놓고 보면
title: 책상은 아끼지만, <span class="accent2">공짜는 아니다</span>
note: 얻는 것과 내주는 것을 같이 봐야 언제 쓸지 판단할 수 있다.
---

<Figure src="/images/ceo3-08-tradeoff-scale.png" alt="위임으로 얻는 것과 내주는 것을 저울에 올린 그림" />

<!-- 이 저울 그림 하나로 다음 장의 표를 예고하고 넘어가세요. -->

---
layout: vs
kicker: 트레이드오프
title: 무엇을 얻고, 무엇을 <span class="accent2">내주는가</span>
label: ↔
left:
  title: 얻는 것
  items:
    - 내 책상이 깨끗하게 유지된다
    - 여러 건을 동시에 굴릴 수 있다
    - 역할별 지시서로 결과가 안정적이다
    - 연장을 제한해 사고를 막는다
right:
  title: 내주는 것
  items:
    - 도우미는 그동안의 대화를 모른다 (규정은 따라간다)
    - 도우미마다 준비 비용이 따로 붙는다
    - 내 화면엔 요약만 남는다 (전체 기록은 따로 보관)
    - 자잘한 일은 직접 하는 게 더 빠르다
---

<!-- 오른쪽 첫 줄이 실무에서 가장 자주 사고 나는 지점입니다. "규정은 따라간다"를 빼먹지 마세요. -->

---
layout: diagram
kicker: 참고 수치 — AI 에이전트 방식 일반에 대한 Anthropic 측정
title: 도우미를 많이 띄울수록 <span class="accent2">총 사용량은 늘어난다</span>
note: 일반 채팅 <strong>1배</strong> · 에이전트에게 맡길 때 <strong>4배</strong> · 여러 에이전트를 동시에 <strong>15배</strong>.
---

<Figure src="/images/ceo3-06-cost-multiplier.png" alt="일반 채팅 1배, 에이전트에게 맡길 때 4배, 여러 에이전트 동시 사용 시 15배를 비교한 막대 그림" />

<!-- 4배·15배는 Anthropic 엔지니어링 블로그 수치이지만 Research 멀티에이전트 기준입니다. "AI 에이전트 방식 일반"이라는 범위를 반드시 밝히고 말하세요. -->

---
layout: default
kicker: 비용에 대한 오해 하나
title: 아끼는 건 <span class="accent2">책상</span>, 돈은 별개입니다
---

도우미를 부를 때마다 **자기 몫의 준비 비용**이 따로 들고, 많이 띄울수록 총 사용량은 늘어납니다. 그래서 이렇게 씁니다 —

- 큰 조사 · 검토처럼 **원래 오래 걸리는 일**에 붙인다
- 한 줄 고치기 같은 일에는 **안 붙인다** — 준비 비용이 더 크다
- 단순한 일은 **값싼 모델로 돌려** 비용을 낮출 수 있다

<Callout tone="warn" icon="lucide:wallet">책상을 아끼는 것과 요금을 아끼는 것은 <strong>다른 이야기</strong>입니다.</Callout>

<!-- 여기서 오해를 정리하지 않으면 "위임하면 싸진다"로 잘못 기억하십니다. 다만 값싼 모델 라우팅은 실제 비용 이점이므로 완전히 부정하지는 마세요. -->

---
layout: diagram
kicker: 판단 기준은 한 줄
title: 중간 과정을 <span class="accent2">안 봐도 되는 일</span>인가
note: <strong>예</strong> → 자료 조사 · 전수 검토 · 오래 걸리는 일 &nbsp;·&nbsp; <strong>아니오</strong> → 근거를 하나하나 확인해야 하는 일 · 30초면 끝나는 일
---

<Figure src="/images/ceo3-07-decision-fork.png" alt="중간 과정을 안 봐도 되는 일인가라는 질문에서 예는 위임한다, 아니오는 직접 한다로 갈리는 그림" />

<!-- 이 한 줄만 가져가셔도 됩니다. "예" 쪽은 자료 조사·전수 검토·결과만 있으면 되는 일·오래 걸리는 일이고, "아니오" 쪽은 근거를 하나하나 확인해야 하는 일·앞의 대화 맥락이 계속 필요한 일·30초면 끝나는 일입니다. 참석자 업무를 하나 받아서 즉석에서 이 질문에 넣어보세요. -->

---
layout: compare
kicker: 자주 하는 오해
title: 세 가지만 <span class="accent2">바로잡고</span> 갑니다
columns: [오해, 실제로는]
rows:
  - { metric: "도우미가 내 대화를 다 알고 있다", before: "회사 규정은 따라가지만 대화 내용은 모른다" }
  - { metric: "많이 띄울수록 좋다", before: "역할이 겹치고 비용만 늘어난다" }
  - { metric: "알아서 적임자를 골라준다", before: "대체로 골라주지만, @로 지목해야 반드시 실행된다" }
---

<!-- 첫 번째가 실무에서 사고가 가장 많이 나는 지점입니다. 상황과 배경은 지시서에 써서 넘겨야 한다고 한 번 더 강조하세요. -->

---
layout: section
index: "05"
kicker: Part 5
title: 우리 회사에 적용하기
subtitle: 남은 건 판단입니다
---

<!-- 여기부터는 참여 유도 구간입니다. 참석자 업무를 즉석에서 매핑해 보세요. -->

---
layout: columns
kicker: 우리 업무 중 무엇을 뗄 수 있을까
title: 떼기 좋은 일에는 <span class="accent2">조건</span>이 있다
columns:
  - title: 떼기 좋은 일의 조건
    items:
      - 자료가 여러 곳에 흩어져 있다
      - 읽는 데 오래 걸린다
      - 결론만 있으면 된다
  - title: 후보 예시
    items:
      - 여러 문서에 흩어진 요구사항을 한 장으로 모으기
      - 지난 분기 기록에서 반복된 문제 찾기
      - 긴 자료를 정해진 형식으로 요약하기
---

<!-- 세 번째 조건이 핵심입니다. 참석자에게 직접 업무 하나씩 말해보게 하고 세 조건에 대어 보세요. -->

---
layout: feature
kicker: 시작 전에 정해둘 것
title: 도구보다 <span class="accent2">먼저</span> 정할 세 가지
columns: 3
features:
  - { icon: "lucide:folder-lock", title: 자료, desc: "어떤 자료를 넣어도 되는가 — 넣으면 안 되는 자료의 목록" }
  - { icon: "lucide:user-check", title: 책임, desc: "결과의 책임자는 누구인가 — AI 산출물의 최종 확인자" }
  - { icon: "lucide:archive", title: 기록, desc: "언제까지 남기는가 — 전 과정이 자동 저장되지만 기본 30일 뒤 삭제" }
---

<!-- 사내 보안·컴플라이언스 정책을 확인한 뒤 문구를 확정해야 하는 슬라이드입니다. 지금은 "정해야 한다"까지만 말하세요. -->

---
layout: diagram
kicker: 세 번째가 가장 자주 빠집니다
title: 전부 남지만, <span class="accent2">기본 30일 뒤 지워진다</span>
note: 나중에 근거를 되짚어야 하는 업무라면 <strong>보존 기간을 늘리거나 따로 보관하는 규칙</strong>을 먼저 정해야 한다.
---

<Figure src="/images/ceo3-09-30day-retention.png" alt="작업 종료 후 기록이 파일로 남다가 30일 시점 이후 삭제되는 타임라인 그림" />

<!-- 화면에는 요약만 보여도 도우미가 한 일은 전부 파일로 남습니다. 문제는 그게 기본 30일 뒤 지워진다는 점입니다. 보존 기간은 cleanupPeriodDays 설정으로 조정할 수 있습니다. -->

---
layout: steps
kicker: 닫는 질문
title: 업무 하나를 떠올리고, <span class="accent2">세 가지만</span> 확인해 보십시오
steps:
  - { title: 떼어낼 수 있는 일인가, desc: 자료가 흩어져 있고 읽는 데 오래 걸리는가, icon: "lucide:scissors" }
  - { title: 중간 과정을 생략해도 되는가, desc: 결론만 있으면 되는 일인가, icon: "lucide:eye-off" }
  - { title: 추가 비용을 감수할 값어치가 있는가, desc: 준비 비용보다 아끼는 시간이 큰가, icon: "lucide:scale" }
---

<!-- 셋 다 "예"라면 위임하십시오. 하나라도 "아니오"라면 직접 하는 편이 낫습니다. 이 문장으로 닫으세요. -->

---
layout: end
title: 고맙습니다
subtitle: 떼어낼 수 있는 일 하나만 정하고 돌아가시면 됩니다
contact: 김민규 · 아이유노글로벌 CEO 교육 3 / 5
---

<!-- 질문 대비 — "대화 맥락을 그대로 물려주는 방법은 없나요?" → /subtask(대화 포크)가 있습니다. 맥락은 물려받고 작업만 밖에서 합니다. 단 v2.1.212 이상이 필요하고 공식 문서상 실험적 기능이라 슬라이드에는 넣지 않았습니다. "딴 책상" 그림과 충돌하므로 먼저 꺼내지 마세요. -->

---
layout: compare
aside: 질문이 나올 때만
kicker: 부록 — 헷갈리는 옆 개념
title: 서브에이전트와 <span class="accent2">무엇이 다른가</span>
columns: [개념, 한 줄, 서브에이전트와의 차이]
rows:
  - { metric: "스킬 (Skills)", before: 매뉴얼, after: "일꾼이 아니라 참고 문서" }
  - { metric: "MCP", before: 외부 연결선, after: "판단이 아니라 연결 담당 (Slack · DB 등)" }
  - { metric: "훅 (Hooks)", before: 자동 실행 버튼, after: "AI 판단 없이 정해진 시점에 무조건 실행" }
  - { metric: "에이전트 팀 (Agent Teams)", before: 진짜 팀, after: "세션이 여러 개, 팀원끼리 직접 소통 (실험 기능)" }
---

<!-- 본문에서는 다루지 않는 백업 슬라이드입니다. 질문이 나올 때만 이 장으로 넘어오세요. 스킬은 교육 2, 훅은 교육 4, MCP는 교육 5에서 각각 다룹니다. -->
