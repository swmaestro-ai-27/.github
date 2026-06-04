# The Demo Day Incident

**The Demo Day Incident**는 데모데이 전날 발생한 사건을 조사하는 AI 추리 게임입니다.
플레이어는 탐정이 되어 사건 개요, 증거 카드, 인물 정보, 권한 로그를 확인하고 여러 Persona Agent의 추리 결과를 비교하며 진실에 접근합니다.

이 프로젝트는 완성형 상용 게임보다 **Agentic Workflow를 짧고 명확하게 시연하는 것**에 초점을 둡니다.
같은 사건을 두고도 Agent마다 역할, 기억, 권한, 조회 가능한 도구가 다르기 때문에 서로 다른 판단을 내립니다.
플레이어는 답을 바로 듣는 것이 아니라, 각 Agent가 어떤 정보를 조회했고 어떤 근거로 의심을 만들었는지 비교합니다.

## 핵심 경험

- 사건 개요와 기본 증거 카드 확인
- 민재, 하린, 도윤, ARIA 등 Persona Agent 선택
- Agent별 권한 범위 안에서 생성되는 답변과 추리 비교
- Agent가 사용한 정보, 도구 호출, 판단 근거 확인
- 후반부 시스템 운영 로그를 통해 결정적 단서 획득
- 최종 범인, 동기, 결정적 증거 제출

## 프로젝트 포인트

- **Persona Agent**: 역할과 관점이 다른 NPC Agent가 사건을 해석합니다.
- **권한 기반 정보 조회**: Agent는 자신에게 허용된 데이터와 현재 공개된 증거만 사용할 수 있습니다.
- **Tool Calling**: 사건 정보, 증거 목록, 인물 정보, 권한 로그를 도구 호출로 조회합니다.
- **근거 기반 추론**: 각 Agent의 추리에는 사용한 근거와 조회 정보가 함께 표시됩니다.
- **Evaluator-Optimizer**: 아직 공개되지 않은 증거나 최종 진실이 답변에 새지 않도록 검증합니다.
- **GUI 기반 시연**: 플레이어가 직접 증거를 보고 Agent를 선택하는 웹 인터페이스로 구성합니다.

## 게임 흐름

1. 초반 기본 증거와 인물 정보를 확인합니다.
2. 대화할 Persona Agent를 선택해 질문합니다.
3. Agent별 추리 결과와 근거를 비교합니다.
4. 시스템 운영 로그 증거 카드를 획득합니다.
5. 최종 추리를 제출하고 사건의 진실을 확인합니다.

## 기술 구성

| 영역 | 구성 |
| --- | --- |
| Frontend | React, Next.js, 카드형 UI, 텍스트 어드벤처 스타일 UX |
| Backend | FastAPI, REST API, 사건/증거/인물 데이터 관리 |
| AI Workflow | Persona Agent, Tool Calling, ReAct, Prompt Chaining, Evaluator-Optimizer |
| Data | 사건 개요, 증거 카드, 인물 카드, 권한 로그, 시스템 운영 로그, ToolCallLog |

## Repositories

| Repository | 역할 |
| --- | --- |
| [the-demo-day-incident](https://github.com/swmaestro-ai-27/the-demo-day-incident) | 공통 기획, 설계, 회의록, 협업 규칙 |
| [frontend](https://github.com/swmaestro-ai-27/frontend) | 클라이언트 화면, 사용자 인터랙션, 프론트엔드 상태 관리 |
| [backend](https://github.com/swmaestro-ai-27/backend) | API, 데이터 모델, 게임 진행 로직, 서버 인프라 |

## 협업 원칙

- 작업은 GitHub Issue를 먼저 생성한 뒤 시작합니다.
- 브랜치는 `<prefix>/<issue-number>` 형식을 사용합니다.
- 커밋과 PR 제목은 Conventional Commits 형식을 사용하고 한국어로 요약합니다.
- 공통 설계와 의사결정은 `the-demo-day-incident`에 기록합니다.
- 프론트엔드와 백엔드 구현은 각각의 전용 레포에서 진행합니다.

## 목표

이 조직은 AI Agent가 단순히 답변을 생성하는 것을 넘어, **역할과 권한, 도구 접근 범위에 따라 어떻게 다르게 추론하는지**를 보여주는 데모 프로젝트를 개발합니다.
