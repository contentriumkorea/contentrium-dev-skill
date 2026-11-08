# Mac에서 Contentrium Dev Skill 설치하기

Mac 전용 실행 파일 없이 동일한 스킬 패키지를 사용합니다. 이 안내는 스킬 자체의 설치 방법이며, 제작할 앱의 macOS 설치기 기준과는 별개입니다.

## 터미널로 개인용 설치

Node.js와 Git이 준비된 Mac 터미널에서 사용할 에이전트에 맞는 명령 하나를 실행합니다. 에이전트 자체는 별도로 설치되어 있어야 합니다.

Codex:

```sh
npx skills add contentriumkorea/contentrium-dev-skill --skill contentrium-dev-skill --agent codex --global --copy
```

Claude Code:

```sh
npx skills add contentriumkorea/contentrium-dev-skill --skill contentrium-dev-skill --agent claude-code --global --copy
```

두 에이전트에 함께 설치:

```sh
npx skills add contentriumkorea/contentrium-dev-skill --skill contentrium-dev-skill --agent codex claude-code --global --copy
```

기존 설치가 있으면 먼저 설치 위치와 직접 수정한 내용을 확인합니다. 같은 에이전트가 읽는 여러 경로에 중복 설치하지 않습니다.

## ZIP으로 직접 설치

1. [최신 스킬 ZIP](https://github.com/contentriumkorea/contentrium-dev-skill/releases/latest/download/contentrium-dev-skill.zip)을 내려받아 압축을 풉니다.
2. Finder에서 **⌘⇧G**를 누르고 아래 개인용 설치 경로의 상위 폴더로 이동합니다. 상위 폴더가 없다면 만듭니다.
3. 압축에서 나온 **contentrium-dev-skill 폴더 전체**를 복사합니다. 폴더 안에 같은 이름의 폴더를 한 번 더 넣지 않습니다.

| 에이전트 | 개인용 설치 위치 |
| --- | --- |
| Codex | ~/.agents/skills/contentrium-dev-skill/ |
| Claude Code | ~/.claude/skills/contentrium-dev-skill/ |

~는 Mac 사용자 홈 폴더입니다. 최종 경로 바로 아래에 SKILL.md, references, agents 등이 있어야 합니다. SKILL.md만 복사하면 참고자료와 디자인 시안이 누락됩니다. Node.js나 Git 없이도 ZIP을 직접 설치할 수 있습니다.

## 설치 확인과 사용

새 대화를 열고 다음처럼 요청합니다. 목록에 나타나지 않으면 에이전트를 재시작하고 설치 경로를 확인합니다.

```text
Contentrium Dev Skill을 읽고 공통·Windows·macOS 기준이 있는지 확인해줘.
```

Mac 앱 개발 요청 예시:

```text
Contentrium Dev Skill을 적용해서 macOS용 데스크톱 앱을 만들어줘.
공통 기준과 macOS 기준을 적용하고, 아직 공개 배포하지 마.
```

Mac에서 실행하는 것과 macOS 앱을 만드는 것은 별개입니다. 개발 대상이 Mac이면 macOS용이라고 명시합니다. 대상 OS에 관한 근거가 없을 때의 기본값은 Windows입니다.

## 업데이트와 검증 범위

터미널 설치본은 저장소의 [업데이트 안내](https://github.com/contentriumkorea/contentrium-dev-skill/blob/main/INSTALL.md#업데이트)를 따릅니다. ZIP 설치본은 직접 수정한 내용을 별도로 보관하고 최신 패키지의 폴더 전체로 교체합니다. 부분 파일만 교체해 다른 버전의 참고자료가 섞이지 않도록 합니다.

GitHub 인증·이미지 생성·브라우저 도구는 스킬 설치와 별개이며 각 에이전트 환경에서 준비합니다. 이 안내를 추가한 릴리스에서는 문서·설치본·배포 ZIP의 일치를 검사했으며 실제 Mac에서 설치·호출을 실행한 것은 아닙니다.
