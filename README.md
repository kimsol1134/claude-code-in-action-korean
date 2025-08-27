# Claude Code in Action (한국어 번역)

이 레포지토리는 Anthropic의 **'Claude Code in Action'** 영상 시리즈의 주요 내용을 한국어로 번역하고 정리한 자료입니다. Claude Code를 활용한 코딩 방법을 배우고자 하는 한국 개발자들을 위해 제작되었습니다.

---

## 📖 주요 내용

이 문서는 Claude Code의 핵심 기능과 실용적인 활용법을 다룹니다.

### 1. Claude Code 소개 (Introduction)
- 코딩 어시스턴트란 무엇이며, Claude가 가진 강점은 무엇인지 알아봅니다.
- Claude Code의 주요 기능 시연 (성능 최적화, 데이터 분석, 인프라 검토 등)을 살펴봅니다.

### 2. 실습 (Getting Hands-on)
- **컨텍스트 관리:** `Claude.md` 파일, `@` 기호, `메모리 모드(#)`를 활용하여 Claude에게 필요한 정보를 효율적으로 제공하는 방법을 배웁니다.
- **변경 사항 적용:** `플랜 모드(Shift + Tab)`, `씽킹 모드("Ultra think")`를 통해 복잡한 작업을 처리하는 고급 기술을 알아봅니다.
- **컨텍스트 제어:** `Escape`, `Compact`, `Clear` 명령어로 긴 대화에서 Claude의 집중도를 유지하는 방법을 배웁니다.
- **커스텀 커맨드:** 자주 사용하는 작업을 자동화하기 위한 `/` 커스텀 커맨드를 생성하는 방법을 알아봅니다.
- **외부 연동:** MCP 서버(Playwright 등)와 GitHub Actions를 연동하여 워크플로우를 확장하는 방법을 알아봅니다.

### 3. 후크와 SDK (Hooks and the SDK)
- **후크(Hooks):** Claude가 툴을 실행하기 전후에 커스텀 명령어를 실행하여 워크플로우를 제어하는 방법을 배웁니다. `pre-tool use` 후크를 사용해 `.env` 파일 접근을 차단하거나, `post-tool use` 후크로 타입 체크를 자동화하는 예제를 다룹니다.
- **Claude Code SDK:** 파이썬, 타입스크립트 등으로 Claude Code의 기능을 스크립트에 통합하는 방법을 알아봅니다.

---

## 📂 폴더 구조

이 프로젝트의 폴더 구조는 아래와 같습니다. 각 폴더와 파일은 원본 강의의 목차를 따릅니다.

```
/Claude-Code-in-Action
├── README.md              # 프로젝트 소개 및 전체 목차
├── 01_Introduction/       # 'What is Claude Code?'
│   ├── 01_What-is-Claude-Code.md
│   ├── 02_What-is-a-Coding-Assistant.md
│   └── 03_Claude-Code-in-Action-Demo.md
├── 02_Getting-Hands-on/    # 'Getting hands on'
│   ├── 01_Claude-Code-Setup.md
│   ├── 02_Project-Setup.md
│   ├── 03_Adding-Context.md
│   ├── 04_Making-Changes.md
│   ├── 05_Controlling-Context.md
│   ├── 06_Custom-Commands.md
│   ├── 07_MCP-Servers-with-Claude-Code.md
│   └── 08_Github-Integration.md
├── 03_Hooks-and-the-SDK/  # 'Hooks and the SDK'
│   ├── 01_Introducing-Hooks.md
│   ├── 02_Defining-Hooks.md
│   ├── 03_Implementing-a-Hook.md
│   ├── 04_Gotchas-around-Hooks.md
│   ├── 05_Useful-Hooks.md
│   ├── 06_Another-Useful-Hook.md
│   └── 07_The-Claude-Code-SDK.md
└── 04_Wrapping-up/        # 'Wrapping up'
    ├── 01_Quiz-on-Claude-Code.md
    └── 02_Summary-and-Next-Steps.md
```

---

## 🔗 원본 자료

- **원본 강의 링크:** [https://anthropic.skilljar.com/claude-code-in-action/303235](https://anthropic.skilljar.com/claude-code-in-action/303235)






