# AI-DLC

AI-DLC(AI-Driven Development Life Cycle) 워크스페이스입니다. 아이디어에서 배포까지의 개발 과정을 정해진 단계(stage)로 나누고, 각 단계마다 사람의 승인을 거치도록 구성된 구조화된 개발 워크플로우를 사용합니다.

이 프로젝트는 **Kiro CLI** 환경 위에서 동작합니다.

## 개요

AI-DLC는 하나의 작업을 아이디어에서 배포된 코드까지 순서대로 진행하며, 각 단계에서 멈춰 사용자의 승인을 요청합니다. 무엇을 만들지 설명하면, 변경에 필요한 프로세스의 깊이를 스스로 판단하고, 실제로 답이 필요한 질문만 물어본 뒤 설계와 코드를 작성하고, 무엇을 왜 결정했는지 기록으로 남깁니다.

- 어떤 단계도 사용자의 승인 없이 다음으로 넘어가지 않습니다.
- 승인 지점에서 언제든 계획, 깊이, 방향을 바꿀 수 있습니다.

## 시작하기

### 사전 요구사항

- **Kiro CLI ≥ 2.6**
- `aidlc` 런타임 명령 사용 가능

### 실행

```bash
# 워크플로우 시작 또는 재개
/aidlc

# 설정 검증
/aidlc --doctor

# 프레임워크 버전 확인
/aidlc --version
```

무엇을 만들지 설명하면 워크플로우가 자동으로 구성됩니다. 별도의 셋업 명령은 없습니다.

## 프로젝트 구조

```
.kiro/          # Kiro CLI 워크스페이스 셸 (skills, agents, hooks, tools, knowledge)
aidlc/          # 워크플로우 산출물 (spaces, intents, memory)
  spaces/
    default/
      memory/   # 계층별 규칙 (org / team / project / phase)
AGENTS.md       # AI-DLC 에이전트 및 워크스페이스 설명
```

## 주요 개념

- **Stage(단계)**: 아이디어(ideation) → 착수(inception) → 구현(construction) → 운영(operation)으로 이어지는 순서화된 진행 단계
- **Approval Gate(승인 게이트)**: 각 단계 종료 시 사람이 검토하고 승인하는 지점
- **Memory(메모리)**: `org → team → project → phase` 순으로 적용되는 계층형 규칙
- **Agents(에이전트)**: 제품, 설계, 아키텍처, 개발, 품질 등 역할별 전문 에이전트

## 문서

전체 문서는 `docs/` 디렉터리를 참고하세요.

- `docs/guide/` — 사용자 가이드
- `docs/reference/` — 개발자 레퍼런스
- `docs/guide/harnesses/kiro-cli.md` — Kiro CLI 전용 가이드

## 라이선스

<!-- 라이선스 정보를 추가하세요 -->
