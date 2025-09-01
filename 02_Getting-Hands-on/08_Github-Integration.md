원문 : https://anthropic.skilljar.com/claude-code-in-action/303240

Claude Code는 GitHub Actions 내에서 Claude를 실행할 수 있게 해주는 공식 GitHub 통합 기능을 제공합니다. 이 통합 기능은 이슈 및 풀 리퀘스트(PR)에서의 멘션 지원과 자동 풀 리퀘스트 리뷰라는 두 가지 주요 워크플로우를 제공합니다.

### 통합 기능 설정하기

시작하려면, Claude에서 `/install-github-app`을 실행하세요. 이 명령어는 다음과 같은 설정 과정을 안내합니다:

1.  GitHub에 Claude Code 앱 설치
2.  API 키 추가
3.  워크플로우 파일이 포함된 풀 리퀘스트 자동 생성

생성된 풀 리퀘스트는 저장소에 두 개의 GitHub Actions를 추가합니다. 이것이 병합(merge)되면, `.github/workflows` 디렉토리에 워크플로우 파일이 생성됩니다.

### 기본 GitHub Actions

이 통합 기능은 두 가지 주요 워크플로우를 제공합니다:

**멘션 액션 (Mention Action)**
이슈나 풀 리퀘스트에서 `@claude`를 사용하여 Claude를 멘션할 수 있습니다. 멘션되면, Claude는 다음과 같이 작동합니다:

  * 요청을 분석하고 작업 계획을 생성합니다.
  * 코드베이스에 대한 전체 접근 권한으로 작업을 실행합니다.
  * 이슈나 PR에 직접 결과로 응답합니다.

**풀 리퀘스트 액션 (Pull Request Action)**
풀 리퀘스트를 생성할 때마다, Claude는 자동으로 다음을 수행합니다:

  * 제안된 변경 사항을 리뷰합니다.
  * 수정 사항의 영향을 분석합니다.
  * 풀 리퀘스트에 상세한 보고서를 게시합니다.

### 워크플로우 사용자 정의하기

초기 풀 리퀘스트를 병합한 후, 프로젝트의 필요에 맞게 워크플로우 파일을 사용자 정의할 수 있습니다. 다음은 멘션 워크플로우를 개선하는 방법입니다:

**프로젝트 설정 추가하기**
Claude가 실행되기 전에, 환경을 준비하는 단계를 추가할 수 있습니다:

```yaml
- name: Project Setup
  run: |
    npm run setup
    npm run dev:daemon
```

**맞춤형 지시사항**
Claude에게 프로젝트 설정에 대한 컨텍스트를 제공하세요:

```yaml
custom_instructions: |
  모든 종속성이 설치된 상태로 프로젝트 설정이 완료되었습니다.
  서버는 이미 localhost:3000에서 실행 중입니다. 서버 로그는
  logs.txt에 기록됩니다. 필요하다면 'sqlite3' cli로
  데이터베이스를 쿼리할 수 있습니다. 필요하다면 mcp__playwright
  도구 세트를 사용하여 브라우저를 실행하고 앱과 상호작용하세요.
```

**MCP 서버 설정**
Claude에 추가 기능을 제공하기 위해 MCP 서버를 설정할 수 있습니다:

```yaml
mcp_config: |
  {
    "mcpServers": {
      "playwright": {
        "command": "npx",
        "args": [
          "@playwright/mcp@latest",
          "--allowed-origins",
          "localhost:3000;cdn.tailwindcss.com;esm.sh"
        ]
      }
    }
  }
```

**도구 권한**
GitHub Actions에서 Claude를 실행할 때는, 허용된 모든 도구를 명시적으로 나열해야 합니다. 이는 MCP 서버를 사용할 때 특히 중요합니다.

```yaml
allowed_tools: "Bash(npm:*),Bash(sqlite3:*),mcp__playwright__browser_snapshot,mcp__playwright__browser_click,..."
```

로컬 개발 환경과 달리, GitHub Actions에서는 권한 설정에 대한 단축키가 없습니다. 각 MCP 서버의 각 도구를 개별적으로 모두 나열해야 합니다.

### 모범 사례

Claude의 GitHub 통합 기능을 설정할 때의 모범 사례는 다음과 같습니다:

  * 기본 워크플로우로 시작하여 점진적으로 사용자 정의하세요.
  * 맞춤형 지시사항을 사용하여 프로젝트별 컨텍스트를 제공하세요.
  * MCP 서버를 사용할 때는 도구 권한을 명시적으로 설정하세요.
  * 복잡한 작업 전에 간단한 작업으로 워크플로우를 테스트하세요.
  * 추가 단계를 설정할 때는 프로젝트의 특정 요구 사항을 고려하세요.

GitHub 통합 기능은 Claude를 개발 어시스턴트에서 GitHub 워크플로우 내에서 직접 작업을 처리하고, 코드를 리뷰하며, 통찰력을 제공할 수 있는 자동화된 팀원으로 변모시킵니다.