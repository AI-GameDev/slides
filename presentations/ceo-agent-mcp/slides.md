---
theme: slidev-theme-tahta
routerMode: 'hash'
mdc: true
aspectRatio: '16/9'
canvasWidth: 980
themeConfig:
  variant: soft
layout: cover
kicker: 아이유노글로벌 · CEO 교육 5 / 5
title: 직원은 뽑았는데,<br><span class="accent2">계정</span>이 없습니다
subtitle: MCP — AI를 회사 시스템에 연결하는 표준 · 김민규
---

<!-- 다섯 번의 교육 중 마지막입니다. 지금까지 직원을 채용하고, 매뉴얼을 주고, 팀을 짜고, 사규를 만들었습니다. 오늘은 그 직원에게 사내 시스템 계정을 발급하는 이야기입니다. -->

---
layout: agenda
kicker: 경영자가 AI 도입에서 실제로 묻는 것 — 오늘 다루지 않는 것은 설정 파일 문법과 서버 제작입니다
title: 오늘 <span class="accent2">답할</span> 네 가지 질문
items:
  - { topic: "AI를 도입했는데 왜 여전히 사람이 자료를 나르나", desc: "시스템에 직접 연결하면 된다" }
  - { topic: "그거 결국 개발 프로젝트 아닌가", desc: "명령 한 줄과 로그인 한 번이다" }
  - { topic: "특정 회사 기술에 묶이는 것 아닌가", desc: "업계 공동 표준이다" }
  - { topic: "회사 데이터를 열어주는 건데 안전한가", desc: "통제 수단이 있다. 대신 지킬 원칙이 있다" }
---

<!-- 오늘 다루는 것은 하나입니다 — AI를 회사 시스템에 연결하는 표준, MCP. 설정 파일 문법이나 서버 제작은 실무자의 영역이고, 오늘은 경영자가 판단할 것만 봅니다. 네 질문 모두 실제 경영 회의에서 나오는 질문입니다. -->

---
layout: section
index: "01"
kicker: Part 1
title: 왜 필요한가
subtitle: 좋은 직원을 뽑아놓고, 사내 시스템 계정을 안 줬습니다
---

<!-- 다룰 내용 — 복습(우리는 지금까지 무엇을 만들었나), 진짜 병목은 복사-붙여넣기다, MCP란 무엇인가. -->

---
layout: diagram
kicker: 복습
title: 매뉴얼도, 팀도, 사규도 <span class="accent2">있다</span>
note: 그런데 이 직원은 아직 <strong>회사 시스템에 로그인할 수 없다.</strong>
---

<Figure src="/images/ceo5-01-employee-no-account.png" alt="스킬=매뉴얼, 서브에이전트=조직, Hook=사규를 갖춘 직원이 잠긴 회사 시스템 문 앞에 서 있는 그림" />

<!-- 네 번의 교육에서 만든 것을 왼쪽에 모아뒀습니다. 스킬은 매뉴얼, 서브에이전트는 조직, Hook은 사규였습니다. 준비는 다 됐는데 문이 잠겨 있습니다. -->

---
layout: default
kicker: 그래서 지금 벌어지는 일
title: 사람이 자료를 <span class="accent2">날라다</span> 준다
---

- 사람이 **찾아서 · 복사해서 · 붙여넣어** 준다
- 직원이 유능할수록, 이 심부름이 더 아깝다

<Callout icon="lucide:key-round">문제는 직원의 능력이 아니다. <strong>계정이 없는 것</strong>이다.</Callout>

<!-- 지난 네 번의 교육에서 직원의 능력은 충분히 끌어올렸습니다. 그런데도 성과가 안 나온다면, 남은 병목은 능력이 아니라 접근 권한입니다. -->

---
layout: diagram
kicker: 진짜 병목
title: 사람을 <span class="accent2">거치느냐</span>, 직접 연결하느냐
note: 붙여넣은 자료는 그 시점에 멈추지만, 연결된 자료는 <strong>항상 현재 상태</strong>다.
---

<Figure src="/images/ceo5-02-copy-paste-bottleneck.png" alt="연결 전에는 사람이 여러 시스템과 AI 사이를 오가며 자료를 나르고, 연결 후에는 시스템이 AI에 직선으로 연결되는 비교 그림" />

<!-- 왼쪽의 엉킨 화살표가 지금 우리 회사의 모습입니다. 사람이 허브가 되어 있습니다. 오른쪽은 사람이 빠진 그림이 아니라, 사람이 운반에서 빠진 그림입니다. -->

---
layout: default
kicker: 공식 문서가 말하는 판단 기준
title: 언제 <span class="accent2">연결할</span> 때인가
---

> 다른 도구에서 데이터를 채팅창에 **복사해 넣고 있다면**, 그때가 연결할 때다.

- 사람의 역할이 **자료 운반**에서 **판단**으로 바뀐다
- 판단 기준이 단순하다 — 지금 손으로 나르고 있는가

<Callout icon="lucide:message-circle-question">우리 회사에서 사람이 시스템 사이를 오가며 나르는 자료는 <strong>무엇입니까?</strong></Callout>

<!-- 여기서 한 번 멈추고 답을 받으세요. 주간 보고, 회의록, 이슈 현황 — 대개 서너 개가 바로 나옵니다. 그게 오늘 이후의 첫 연결 대상입니다. -->

---
layout: diagram
kicker: 공식 비유
title: AI 애플리케이션을 위한 <span class="accent2">USB-C 포트</span>
note: USB-C 포트가 있으면 어떤 케이블이든 꽂히듯, MCP를 지원하는 AI는 <strong>어떤 서비스와도 같은 방식</strong>으로 연결된다.
---

<Figure src="/images/ceo5-03-usb-c-port.png" alt="문서·메신저·이슈·데이터베이스·결제 아이콘이 각각 케이블로 MCP라고 적힌 기기의 USB-C 포트 하나에 꽂히는 그림" />

<!-- 이 비유는 제가 만든 게 아니라 공식 문서의 표현입니다. 포트가 표준이면 케이블 종류를 걱정하지 않아도 되는 것과 같습니다. -->

---
layout: define
kicker: 용어
term: MCP (Model Context Protocol)
definition: AI가 외부 도구·데이터에 연결되는 방식을 <span class="accent2">표준화한 약속</span>
points:
  - Linux Foundation 산하의 개방형 표준이다
  - 한 회사의 제품이 아니라, 업계가 함께 쓰는 규격이다
---

<!-- 프로토콜이라는 말이 낯설면 "약속"으로 바꿔 들으시면 됩니다. 전기 콘센트 규격 같은 것입니다. -->

---
layout: default
kicker: 오늘의 경영 비유 — 설명을 위한 것이며 공식 용어가 아니다
title: MCP = 그 직원에게 발급하는 <span class="accent2">사내 시스템 계정</span>
---

| | 의미 |
|---|---|
| AI 직원 | 이미 채용 완료 |
| **MCP** | 그 직원에게 발급하는 **사내 시스템 계정** |

<Callout tone="warn" icon="lucide:triangle-alert"><strong>용어 주의 — "MCP 서버"의 '서버'는 서버 컴퓨터가 아니다.</strong> 내 노트북에서 도는 작은 프로그램일 수도 있다. "서버를 구축해야 하나?"의 답은 <strong>아니오</strong>다.</Callout>

<!-- 이 계정 비유는 이해를 돕기 위한 것이지 공식 용어가 아닙니다. 공식 비유는 앞 장의 USB-C 하나뿐입니다. 그리고 '서버'라는 단어 때문에 인프라 구축 프로젝트로 오해하는 경우가 많은데, 그게 아니라는 점을 여기서 확실히 짚고 가세요. -->

---
layout: section
index: "02"
kicker: Part 2
title: 무엇이 달라지는가
subtitle: 연결하면, 지시할 수 있는 문장이 달라집니다
---

<!-- 다룰 내용 — 연결하면 할 수 있게 되는 말, 비개발 업무에서의 세 장면, 붙이는 데 실제로 드는 것. -->

---
layout: reference
kicker: 공식 문서의 예시 — 전부 한 문장 지시다
title: 연결하면 할 수 있게 되는 <span class="accent2">말</span>
items:
  - { term: 이슈 + 코드 저장소, desc: "\"ENG-4521에 적힌 기능을 만들고 PR까지 올려줘\"" }
  - { term: 모니터링, desc: "\"지난 24시간 가장 많이 난 오류가 뭔지 알려줘\"" }
  - { term: 데이터베이스, desc: "\"이 기능을 쓴 사용자 10명의 이메일을 찾아줘\"" }
  - { term: 디자인 도구, desc: "\"새로 올라온 디자인 기준으로 우리 이메일 템플릿을 고쳐줘\"" }
  - { term: 메일, desc: "\"이 10명에게 피드백 세션 초대 메일 초안을 만들어줘\"" }
---

<!-- 다섯 문장의 공통점을 물어보세요. 전부 "자료를 줄 테니 처리해줘"가 아니라 "가서 보고 해줘"입니다. 자료를 첨부하지 않았다는 것이 핵심입니다. -->

---
layout: default
kicker: 개발 조직이 아니어도 바로 쓰이는 곳
title: 비개발 업무에서의 <span class="accent2">세 장면</span>
---

| 장면 | 기존 | 연결 후 |
|---|---|---|
| **회의록 → 할 일** | 읽고 손으로 옮겨 적음 | 담당자별로 분류해 **문서 도구에 직접 등록** |
| **흩어진 결정 찾기** | "그거 어디서 정했더라" | 메신저 이력을 검색해 **정식 문서로 정리** |
| **주간 보고서** | 도구 3~4개를 오가며 취합 | **한 번에 모아 한 장으로** |

- 절약되는 것은 작업 시간이 아니라 **도구 사이를 오가는 전환 비용**이다
- 이 일은 대개 **가장 비싼 사람**이 하고 있다

<Callout icon="lucide:message-circle-question">우리 회사의 주간 보고서는 <strong>몇 개 시스템</strong>에서 취합됩니까?</Callout>

<!-- 세 장면 모두 개발과 무관합니다. 마지막 불릿이 경영자에게 가장 중요한 문장입니다 — 이 운반 작업을 하고 있는 사람은 대개 조직에서 가장 인건비가 높은 사람입니다. -->

---
layout: diagram
kicker: 붙이는 데 실제로 드는 것
title: 이게 <span class="accent2">전부</span>다
note: 2단계의 로그인은 <strong>평소 그 서비스에 로그인하는 것과 동일하다.</strong>
---

<Figure src="/images/ceo5-04-three-steps-to-connect.png" alt="1 명령 한 줄, 2 로그인 한 번, 3 연결 확인의 3단계를 원형 아이콘과 화살표로 나타낸 그림" />

<!-- 실무자가 하는 일은 이 세 단계가 전부입니다. 개발이 아니라 설정입니다. -->

---
layout: default
kicker: 도입 판단의 기준이 바뀐다
title: 기술 결정이 아니라 <span class="accent2">거버넌스 결정</span>
---

- 개발도, 서버 구축도, 별도 계약도 필요하지 않다
- 이미 만들어진 연결을 **고르는 것**이지 만드는 것이 아니다

<Callout icon="lucide:scale">판단의 기준이 "개발 리소스가 있는가"가 아니라 <strong>"권한을 줄 것인가"</strong>로 바뀐다.</Callout>

<!-- 그래서 이 안건은 개발팀에 넘길 안건이 아니라 경영진이 판단할 안건입니다. 물어야 할 것은 "만들 수 있나"가 아니라 "열어줘도 되나"입니다. -->

---
layout: section
index: "03"
kicker: Part 3
title: 무엇을 연결할 수 있는가
subtitle: 이미 만들어져 있습니다. 고르기만 하면 됩니다
---

<!-- 다룰 내용 — 이미 준비된 연결 대상, 특정 회사에 묶이는 것 아닌가, 우리 회사 시스템은 어떻게 되나. -->

---
layout: diagram
kicker: 이미 준비된 연결 대상
title: 만드는 것이 아니라 <span class="accent2">고르는 것</span>
note: 검증을 거친 연결 목록이 <strong>공식 디렉터리</strong>로 제공되고, 공개된 연결 대상은 <strong>수만 건 규모</strong>로 집계된다.
---

<Figure src="/images/ceo5-05-connectable-domains.png" alt="문서·메신저·이슈·코드·모니터링·디자인·데이터베이스·결제 여덟 개 분야를 나타내는 아이콘 그리드" />

<!-- 서버 개수는 정확한 숫자로 말하지 마세요. 집계 출처가 서드파티이고 변동이 큽니다. "수만 건 규모"까지만. -->

---
layout: reference
kicker: 여덟 개 분야 — 검증된 연결이 이미 존재한다
title: 무엇을 <span class="accent2">할 수 있게</span> 되나
items:
  - { term: 문서·지식 관리, desc: "회의록·프로젝트 노트를 찾고, 결과를 다시 저장" }
  - { term: 메신저, desc: 과거 대화를 검색 가능한 지식창고로 활용 }
  - { term: 이슈·일정 관리, desc: "진행 현황 파악, 이슈 자동 생성" }
  - { term: 코드 저장소, desc: 변경 이력·리뷰 현황 확인 }
  - { term: 모니터링, desc: 장애·오류 현황 실시간 확인 }
  - { term: 디자인 도구, desc: 색상·폰트·규격을 문서로 정리 }
  - { term: 데이터베이스, desc: 자연어로 데이터 질문 }
  - { term: 결제, desc: 거래·정산 내역 조회 }
---

<!-- 이 중 우리 회사가 이미 돈을 내고 쓰고 있는 서비스가 몇 개인지 세어보게 하세요. 대개 절반 이상입니다. -->

---
layout: diagram
kicker: CEO가 반드시 묻는 질문 — 답은 명확하다
title: 한 회사 기술이 아니라 <span class="accent2">업계 공동 표준</span>
note: Anthropic · OpenAI · Google이 함께 기술 운영 위원회를 구성하고, AWS · Microsoft · Cloudflare 등이 참여한다.
---

<Figure src="/images/ceo5-06-standard-governance.png" alt="2024년 11월 Anthropic 공개에서 2025년 12월 Linux Foundation 이관으로 이어지는 타임라인과, 업계 공동 표준 아래 Anthropic·OpenAI·Google이 놓인 구조도" />

<!-- 이 장은 근거가 가장 명확한 부분입니다. Linux Foundation 이관과 공동 운영 체계는 공식 발표 기준이므로 자신 있게 답변하세요. -->

---
layout: default
kicker: 벤더 종속 관점
title: 종속을 <span class="accent2">늘리는</span> 결정이 아니라 <span class="accent2">줄이는</span> 결정
---

> 한 번 연결해두면 **다른 AI로 갈아타도 그대로 쓴다.**
> ChatGPT · Gemini · Copilot 모두 같은 표준을 지원한다.

- 연결 자산이 특정 AI 제품이 아니라 **표준**에 쌓인다
- AI 도구를 바꾸는 결정과 시스템을 연결하는 결정이 **분리**된다

<Callout icon="lucide:unlink">"이 회사에 묶이는 것 아닌가"의 답 — <strong>오히려 반대다.</strong></Callout>

<!-- 경영자가 가장 자주 묻는 질문이고, 여기서 확실히 답이 되면 도입 저항의 상당 부분이 사라집니다. -->

---
layout: diagram
kicker: 사내 시스템을 연결할 때의 경제성
title: 각각 연결하면 <span class="accent2">15</span>개, 표준 창구를 두면 <span class="accent2">8</span>개
note: AI 3종과 사내 시스템 5개를 붙일 때의 차이다. 새 AI를 도입해도 <strong>사내 시스템을 다시 연결하지 않는다.</strong>
---

<Figure src="/images/ceo5-07-fifteen-vs-eight.png" alt="AI 3개와 시스템 5개를 각각 직접 연결한 15개의 엉킨 선과, 가운데 표준 창구 하나를 두어 8개로 줄어든 연결을 비교한 그림" />

<!-- 왼쪽은 AI를 하나 더 도입할 때마다 선이 5개씩 늘어납니다. 오른쪽은 1개만 늘어납니다. 이게 표준의 실익입니다. -->

---
layout: columns
kicker: 우리 회사 시스템은 어떻게 되나
title: 두 가지 <span class="accent2">경우</span>뿐이다
columns:
  - title: 이미 쓰는 상용 서비스
    items:
      - 대부분 이미 연결 대상이 존재한다
      - 고르면 된다
      - 만드는 비용 없음
  - title: 우리가 만든 사내 시스템
    items:
      - 연결 창구를 한 번 만들면 된다
      - 표준이라 어느 AI 도구에서든 그대로 쓴다
      - 만드는 비용은 한 번뿐
---

<!-- 사내 시스템 연결은 개발이 필요한 유일한 경우입니다. 다만 그 개발도 AI 도구마다 반복되지 않고 한 번으로 끝난다는 점이 앞 장의 15 대 8 그림입니다. -->

---
layout: section
index: "04"
kicker: Part 4
title: 조직 관점
subtitle: 계정을 준다는 것은, 권한을 준다는 것입니다
---

<!-- 다룰 내용 — 연결 범위 3단계, 권한을 통제하는 방법, CEO가 실무자에게 물어야 할 질문. -->

---
layout: diagram
kicker: 같은 연결이라도 어디에 걸어두느냐에 따라 성격이 달라진다
title: 연결 범위는 <span class="accent2">3단계</span>
note: Hook에서 배운 구조와 같다 — <strong>안쪽(좁은) 단계가 바깥 단계를 덮어쓴다.</strong>
---

<Figure src="/images/ceo5-08-three-scopes.png" alt="개인 전체 상자 안에 팀 공유 표시가 붙은 프로젝트 상자가 있고, 그 안에 개인 상자가 들어 있는 3중 중첩 구조도" />

<!-- Hook 덱의 3단계와 구조는 같지만 세 번째가 다릅니다. Hook은 개인/프로젝트/조직이었고, MCP는 개인/프로젝트/개인 전체입니다. 혼동하지 마세요. -->

---
layout: compare
kicker: 세 단계의 성격
title: 개인 도구인가, <span class="accent2">팀 표준</span>인가
columns: [단계, 적용 범위, 성격, 공유]
rows:
  - { metric: 개인, before: 내 작업 하나에만, after: 개인 도구, delta: 공유 안 됨 }
  - { metric: 프로젝트, before: 그 프로젝트 전체, after: 팀 표준, delta: 팀원과 공유됨 }
  - { metric: 개인 전체, before: 내 모든 작업, after: 개인 상시 도구, delta: 공유 안 됨 }
---

<!-- 팀 단위로 공유된 연결은 처음 쓸 때 승인을 한 번 받습니다 — 모르는 사이에 붙지 않습니다. 조직 차원에서 특정 연결을 차단하는 설정도 별도로 존재합니다. 경영자가 볼 것은 가운데 줄입니다. 팀 표준으로 올리는 순간 그건 개인의 선택이 아니라 조직의 결정입니다. -->

---
layout: diagram
kicker: 계정을 준다는 것은 권한을 준다는 것
title: 통제는 <span class="accent2">세 겹</span>이다
note: 세 관문을 모두 통과해야 실행된다 — 어느 하나만으로 막는 구조가 아니다.
---

<Figure src="/images/ceo5-09-three-layer-control.png" alt="연결 승인, 계정 권한 범위, 작업 단위 승인 세 개의 관문을 화살표가 차례로 통과하는 그림" />

<!-- 통제 수단이 없는 게 아니라 세 겹으로 있습니다. 다만 세 번째 관문은 사람이 읽어야 작동합니다 — 뒤에서 다시 나옵니다. -->

---
layout: steps
kicker: 세 겹의 통제
title: 어디서 <span class="accent2">막을</span> 수 있는가
steps:
  - { title: 연결 승인, desc: 어떤 시스템에 붙일지 결정, icon: "lucide:plug" }
  - { title: 계정 권한 범위, desc: 그 계정이 볼 수 있는 것까지만 볼 수 있음, icon: "lucide:id-card" }
  - { title: 작업 단위 승인, desc: "실행 직전에 \"이거 해도 됩니까\" 확인", icon: "lucide:shield-check" }
---

<!-- 핵심 원칙 하나만 기억하면 됩니다 — AI에게 주는 계정도 사람에게 주는 계정과 같은 기준으로 발급합니다. 읽기만 필요하면 읽기 권한만 줍니다. 사람 직원에게 전 시스템 관리자 권한을 주지 않는 것과 똑같습니다. -->

---
layout: agenda
kicker: 오늘 회의실을 나가서 바로 쓸 수 있는 질문
title: CEO가 실무자에게 던질 <span class="accent2">질문 3개</span>
items:
  - { topic: "AI가 접근하는 시스템은 무엇입니까", desc: "그 계정 권한은 어디까지입니까" }
  - { topic: "그 연결은 개인 것입니까, 팀 표준입니까", desc: "팀 표준이면 조직의 결정입니다" }
  - { topic: "우리가 만들지 않은 연결을 쓰고 있습니까", desc: "있다면 누가 검토했습니까" }
---

<!-- 이 세 질문이 오늘 세션의 실무적 산출물입니다. 답이 막히면 그 자체가 점검이 필요하다는 신호입니다. -->

---
layout: section
index: "05"
kicker: Part 5
title: 리스크
subtitle: 계정을 준 상대를 믿을 수 있어야 합니다
---

<!-- 다룰 내용 — 남이 만든 연결을 믿는다는 것, 읽은 문서가 지시가 될 수 있다, 비용과 성능은 걱정해야 하나. -->

---
layout: diagram
kicker: 남이 만든 연결을 믿는다는 것
title: 출처 불명 연결은 <span class="accent2">내 권한 그대로</span> 움직인다
note: 특히 <strong>내 컴퓨터에서 실행되는 방식</strong>의 연결은 내 파일과 내 열쇠에 그대로 닿는다.
---

<Figure src="/images/ceo5-10-untrusted-server.png" alt="물음표가 그려진 출처 불명 상자가 내 컴퓨터 경계 안의 폴더와 열쇠에 연결되는 그림" />

<!-- 상자에 물음표가 있다는 게 핵심입니다. 안에 뭐가 들었는지 모르는 채로 내 컴퓨터 안쪽에 연결선을 잇는 것입니다. -->

---
layout: default
kicker: 공식 경고문 — 연결하기 전에 각 서버를 신뢰할 수 있는지 확인하라
title: "\"연결만 하는 건데 뭐가 <span class=\"accent2\">위험해</span>\""
---

| 오해 | 실제 |
|---|---|
| "연결만 하는 건데 뭐가 위험해" | 연결 대상이 **내 파일과 계정에 접근**한다 |
| "유명한 도구니까 안전하겠지" | 널리 쓰이던 연결 도구에서 **심각도 최상위 취약점이 실제로 보고**됨 |

<Callout tone="warn" icon="lucide:shield-alert"><strong>원칙 — 공식 디렉터리 또는 해당 서비스 공식 문서 기준으로만 연결한다.</strong></Callout>

<!-- Hook에서 했던 이야기와 같습니다 — 남이 보낸 직원을 신원 확인 없이 들여놓지 않습니다. CVE 번호는 읽지 마세요. 질문이 나오면 답변만 하시면 됩니다 — CVE-2025-6514(연결 도구 mcp-remote, 2025년 7월 공개)와 CVE-2025-49596(공식 디버깅 도구, 2025년 패치) 두 건입니다. -->

---
layout: diagram
kicker: 가장 이해하기 어렵지만, 가장 중요한 위험
title: 읽은 문서가 <span class="accent2">지시</span>가 될 수 있다
note: AI는 <strong>읽은 내용</strong>과 <strong>받은 지시</strong>를 항상 완벽히 구분하지는 못한다.
---

<Figure src="/images/ceo5-11-prompt-injection.png" alt="문서 안에 숨겨진 한 줄이 화살표를 타고 AI에게 받은 지시처럼 작동하는 그림" />

<!-- 문서 본문 중 한 줄에 색이 칠해져 있고, 그 줄이 지시처럼 작동합니다. 사람이라면 "이건 문서 내용이지 내 상사의 지시가 아니다"라고 구분하지만, AI는 항상 그렇지 못합니다. -->

---
layout: default
kicker: 경영 언어로 옮기면
title: 해킹이라기보다 <span class="accent2">사회공학</span>
---

| | 의미 |
|---|---|
| 위험의 성격 | 해킹이라기보다 **사회공학** — 문서로 직원을 속이는 것 |
| 노출 지점 | **외부에서 들어오는 자료**를 읽는 모든 연결 |
| 방어 | 승인 프롬프트를 **읽고** 판단, 권한을 **좁게** 부여 |

<Callout tone="warn" icon="lucide:mouse-pointer-click">그래서 <strong>"승인하시겠습니까"를 습관적으로 누르는 것</strong>이 가장 위험한 습관이다.</Callout>

<!-- 앞에서 본 세 겹의 통제 중 세 번째 관문이 여기서 무력화됩니다. 기술이 아니라 습관의 문제입니다. 조직에 이 습관을 어떻게 심을지가 경영자의 숙제입니다. -->

---
layout: vs
kicker: 한때 실재했던 우려 — "연결을 많이 붙이면 AI가 느려지고 비용이 올라간다"
title: 비용과 성능은 <span class="accent2">걱정해야</span> 하나
label: →
left:
  title: 예전
  items:
    - 연결된 도구 설명을 전부 미리 들고 있음
    - 붙일수록 부담 증가
right:
  title: 현재
  items:
    - 필요할 때만 꺼내 씀
    - 붙여도 영향이 미미
    - 이 개선은 기본값으로 켜져 있다
---

<!-- 이 장은 리스크가 아니라 안심 파트입니다. 시중 자료 상당수가 "MCP는 컨텍스트를 크게 잡아먹는다"고 쓰고 있는데, 현재 기본 설정에서는 도구 정의를 지연 로딩하므로 상당 부분 해소됐습니다. 옛 경고를 그대로 옮기면 틀린 설명이 됩니다. -->

---
layout: default
kicker: 다만 여전히 유효한 원칙
title: 줄이는 이유는 비용이 아니라 <span class="accent2">보안과 관리</span>
---

| 원칙 | 이유 |
|---|---|
| 실제 쓰는 연결만 유지 | 관리·감사 대상이 늘어남 |
| 안 쓰는 연결은 정리 | 열어둔 계정은 **닫아야 할 계정**이다 |

<Callout icon="lucide:door-closed">퇴사자 계정을 정리하는 것과 같은 일이다 — <strong>주기적으로 해야 한다.</strong></Callout>

<!-- 비용 걱정은 덜어드렸지만, 관리 부담은 남습니다. 이건 IT 자산 관리와 같은 성격의 일입니다. -->

---
layout: default
kicker: 작게 시작하는 것이 정답이다
title: 도입 <span class="accent2">체크리스트</span>
---

| 순서 | 할 일 |
|---|---|
| 1 | **읽기 전용** 연결 하나로 시작 |
| 2 | 가장 자주 **복사-붙여넣기 하는 시스템**을 첫 대상으로 |
| 3 | 계정 권한은 **필요한 범위까지만** |
| 4 | 공식 디렉터리 **밖의 연결은 검토 후** 사용 |
| 5 | 개인용으로 써보고, 팀 표준으로 올릴지 **나중에 판단** |
| 6 | 안 쓰는 연결은 **정리** |

<Callout icon="lucide:megaphone">실무자에게 이렇게 말하면 된다 — <strong>"[X] 시스템을 읽기 권한만 주고 연결해봅시다. 공식 문서에 있는 방식으로만 붙이고, 되면 팀에 공유할지 그때 판단합시다."</strong></Callout>

<!-- 마지막 Callout 문장을 그대로 읽어주세요. 이 한 문장이면 실무자에게 지시가 끝납니다. 2번 항목의 답은 아까 받아둔 "사람이 나르는 자료"입니다. -->

---
layout: bigtype
kicker: 오늘의 결론
title: 채용은 끝났다, 이제 <em>계정</em>을 준다
---

<!-- 다섯 번의 교육을 한 문장으로 묶으면 이렇습니다. -->

---
layout: default
kicker: 한 장 요약
title: 오늘의 <span class="accent2">결론</span>
---

| | 오늘의 결론 |
|---|---|
| 문제 | 유능한 직원에게 **시스템 계정이 없다** |
| 해법 | MCP로 **직접 연결** — 사람이 자료를 나르지 않는다 |
| 표준 | 한 회사 기술이 아니라 **업계 공동 표준** |
| 통제 | 연결 승인 · 계정 권한 · 작업 승인 **세 겹** |
| 주의 | **믿을 수 있는 연결만**, 승인 창은 **읽고** |
| 시작 | 읽기 전용 연결 하나 |

<Callout icon="lucide:quote">사람이 시스템 사이를 오가며 자료를 나르고 있다면, 그건 AI의 한계가 아니라 <strong>계정을 안 준 것</strong>입니다.</Callout>

<!-- 마지막 문장이 오늘 가져가실 한 줄입니다. -->

---
layout: end
title: 고맙습니다
subtitle: 다섯 번의 교육이 여기서 끝납니다
contact: 김민규 · 아이유노글로벌 CEO 교육 5 / 5
---
