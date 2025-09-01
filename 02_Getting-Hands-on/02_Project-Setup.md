함께 작업할 프로젝트가 있으면 Claude Code 사용이 더 흥미로워집니다.
Claude Code로 탐색해 볼 작은 프로젝트를 하나 준비했습니다. 이전 비디오에서 보여드린 것과 동일한 UI 생성 앱입니다. 참고: 이 프로젝트를 꼭 실행할 필요는 없습니다. 원하신다면 여러분 자신의 코드 베이스로 남은 과정을 계속 따라오셔도 됩니다!

### 설치
이 프로젝트는 약간의 설정이 필요합니다:
1.  이 강의에 첨부된 `uigen.zip` 파일을 다운로드하여 압축을 해제하세요.
2.  프로젝트 디렉토리에서 `npm run setup`을 실행하여 종속성을 설치하고 로컬 SQLite 데이터베이스를 설정하세요.
3.  **선택사항:** 이 프로젝트는 Anthropic API를 통해 Claude를 사용하여 UI 컴포넌트를 생성합니다. 앱의 모든 기능을 테스트하고 싶다면, Anthropic API에 접근하기 위한 API 키를 제공해야 합니다. **이 과정은 선택사항입니다. API 키가 제공되지 않아도 앱은 정적인 가짜 코드를 생성합니다.** API 키를 설정하는 방법은 다음과 같습니다:
    * [https://console.anthropic.com/](https://console.anthropic.com/) 에서 Anthropic API 키를 발급받으세요.
    * 발급받은 API 키를 `.env` 파일에 넣어주세요.
4.  `npm run dev`를 실행하여 프로젝트를 시작하세요.

### 다운로드
* [uigen.zip](https://cc.sj-cdn.net/instructor/4hdejjwplbrm-anthropic/assets/1750970894/uigen.zip?response-content-disposition=attachment&Expires=1756736532&Signature=KwAFnWSRkGz6Msq3o52MoLKIbX4qOEsIiS8WD2sdxPgk~E290Dc10G73pCtCbgBEcZKXdKp3Q4ktXBA-wjUHF04XEn0xreENzoMWd0PwZaCNs6Jtbp~a1xmjxcu7OZ2ZeALolKRvIbcYRTfD-LaujYGjk2qbf2pWdsAx8EQ8LaPL-shv217A0Eq6SyND7xbrPKmM93bUaoz4dJm947HDYQgloz7V2wopf-kzEepQkgnGWMb3zDJaBV2RIPMqBZG5y7RvIgRNvoEY7gRjNFaMJzb8hUp3OBsYEwqa05P~MEoWByKLC1jknsPi7kGRkPNHhC8ze~FTVaHU4FhsfizhEg__&Key-Pair-Id=APKAI3B7HFD2VYJQK4MQ)