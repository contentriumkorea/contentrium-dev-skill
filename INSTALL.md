# 설치 및 사용 안내

[← 첫 페이지로](README.md)

## 설치

Node.js와 Git이 준비된 터미널에서 실행하고 사용할 에이전트를 선택하세요.

```sh
npx skills add contentriumkorea/contentrium-dev-skill --skill contentrium-dev-skill
```

Codex와 Claude Code에 개인용으로 설치하려면:

```sh
npx skills add contentriumkorea/contentrium-dev-skill --skill contentrium-dev-skill --agent codex claude-code --global --copy
```

Cursor, Gemini CLI, GitHub Copilot 등 다른 Agent Skills 지원 도구도 설치 과정에서 선택할 수 있습니다. 지원 목록은 [Skills CLI 안내](https://github.com/vercel-labs/skills#supported-agents)에서 확인하세요. 기존 설치가 있다면 설치 도구의 교체 안내를 확인하세요. 같은 스킬을 여러 경로에 중복 설치하지 않는 것을 권장합니다.

### ZIP으로 직접 설치

[최신 설치 패키지](https://github.com/contentriumkorea/contentrium-dev-skill/releases/latest/download/contentrium-dev-skill.zip)를 압축 해제하고 **`contentrium-dev-skill` 폴더 전체**를 아래 위치로 복사합니다. `SKILL.md`만 복사하면 이미지와 참고자료가 빠집니다.

| 에이전트 | 개인용 설치 위치 | 프로젝트용 설치 위치 |
| --- | --- | --- |
| Codex | `~/.agents/skills/contentrium-dev-skill/` | `.agents/skills/contentrium-dev-skill/` |
| Claude Code | `~/.claude/skills/contentrium-dev-skill/` | `.claude/skills/contentrium-dev-skill/` |

Windows의 `~`는 사용자 홈 폴더입니다. 다른 에이전트는 해당 제품의 스킬 폴더에 동일한 폴더 전체를 복사하세요. 목록에 나타나지 않으면 새 세션을 열거나 에이전트를 재시작하세요.

### 사용 예시

Codex:

```text
$contentrium-dev-skill 영상 편집용 Windows 데스크톱 앱을 만들어줘. 아직 공개 배포하지 마.
```

Claude Code:

```text
/contentrium-dev-skill 기존 앱의 설치기를 만들고 설치·제거 동작을 확인해줘.
```

다른 에이전트에서는 “Contentrium Dev Skill을 적용해서 작업해줘”라고 요청하거나 해당 도구의 스킬 선택 기능을 사용하세요.


## 업데이트

프로젝트용 설치를 업데이트하려면:

```sh
npx skills update contentrium-dev-skill -p
```

개인용 설치는 `-p` 대신 `-g`를 사용하세요. ZIP으로 설치했다면 최신 ZIP의 폴더 전체로 교체하세요. 직접 수정한 내용이 있다면 먼저 별도로 보관하세요.
## 호환성과 검증 범위

표준 Agent Skills 형식이며 별도 실행 파일이나 서버를 설치하지 않습니다. Codex용 표시 정보는 선택 사항이므로 다른 에이전트의 사용을 막지 않습니다. 이 스킬을 설치한다고 GitHub 인증, 이미지 생성 도구 또는 브라우저가 함께 설치되지는 않습니다. 실제 작업에는 각 환경에서 사용 가능한 도구와 사용자 권한이 필요합니다.

Codex·Claude Code·Cursor·Gemini CLI·GitHub Copilot 대상으로 격리된 프로젝트 폴더 설치를 검증한 이력이 있습니다. 현재 패키지는 고정 README 템플릿을 포함한 15개 파일이며 설치본·ZIP과 원본의 일치를 확인했습니다. 공통 경로를 사용하는 에이전트는 같은 설치 폴더를 공유합니다. 모든 에이전트에서 실제 앱 개발·배포 전체를 실행했다는 의미는 아닙니다. 일반 웹 채팅에 파일을 첨부하는 것과 로컬 에이전트에 스킬을 설치하는 것은 다릅니다.

## English quick start

An Agent Skills package for desktop app development and GitHub presentation, authorized distribution, and release management of apps, skills, and plugins. Desktop installation and startup UI requirements apply only to desktop apps; skills and plugins retain their native packaging. Install with the command in the installation section. Copy the complete skill directory to preserve references and previews. Background imagery must match each app's purpose; text and controls remain real UI. No automatic publishing or conversion of plugins/web apps into desktop apps.

## 참고 및 라이선스

- [Codex 스킬 안내](https://developers.openai.com/codex/build-skills)
- [Claude Code 스킬 안내](https://code.claude.com/docs/en/skills)
- [Skills CLI](https://github.com/vercel-labs/skills)
- [MIT License](LICENSE): 본 저장소의 문서와 코드에 적용합니다. 이름·로고 등 상표에 대한 권리는 부여하지 않습니다. 이미지 자료는 디자인 참고용으로 포함되며 제3자 권리를 대신 허가하지 않습니다.
