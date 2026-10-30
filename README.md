# ai_skills

개인적으로 쓰는 AI 코딩 에이전트용 스킬 모음. 각 스킬을 Claude Code 버전(`claude/`)과 Codex CLI 버전(`codex/`)으로 나눠 둔다.

## 구조

```
ai_skills/
├── claude/
│   ├── dev-work-principles/
│   └── requirements-analysis/
└── codex/
    ├── dev-work-principles/
    └── requirements-analysis/
```

두 도구용 버전의 본문 원칙·템플릿은 동일하다. `codex/` 버전은 frontmatter 바로 아래에 Codex 적용 참고(설치 경로, 도구별 기능 매핑)만 추가로 붙어 있다.

## 스킬 목록

| 스킬 | 역할 |
|---|---|
| [dev-work-principles](claude/dev-work-principles/SKILL.md) | 코드를 설계·구현·테스트·검증할 때 지키는 11가지 작업 원칙 — 보안 데이터 비유출, 계획 먼저 세우기, 모듈화, edge case 테스트, 실제 동작 검증 보고서, 서브에이전트를 통한 독립 검토, 오버엔지니어링 판단 등 |
| [requirements-analysis](claude/requirements-analysis/SKILL.md) | 요구사항 문서를 사용자가 직접 해석하도록 돕는 스킬 — AI가 먼저 해석하지 않고, 사용자의 해석 확인·누락 점검·담당자 질문 다듬기·결정 기록을 보조 |

## 설치

### Claude Code
`claude/<스킬명>/` 폴더를 프로젝트의 `.claude/skills/<스킬명>/` 또는 개인 설정의 `~/.claude/skills/<스킬명>/`에 둔다.

### Codex CLI
`codex/<스킬명>/` 폴더를 프로젝트의 `.codex/skills/<스킬명>/` 또는 개인 설정의 `~/.codex/skills/<스킬명>/`에 둔다. 각 스킬의 `SKILL.md`에 있는 "Codex 적용 참고" 블록 참고.

둘 다 `SKILL.md`의 `description` 필드로 자동 트리거되므로, 트리거 문구에 해당하는 요청을 하면 별도 호출 없이 적용된다.
