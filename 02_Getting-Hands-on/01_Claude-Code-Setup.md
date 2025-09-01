이제 Claude Code를 로컬에 설치할 시간입니다!
전체 설치 안내는 여기에서 찾을 수 있습니다: [https://docs.anthropic.com/en/docs/claude-code/setup](https://docs.anthropic.com/en/docs/claude-code/setup)

간단히 말해, 다음 단계를 따르시면 됩니다:
* **NodeJS가 설치되어 있는지 확인**하세요. 이미 설치했는지 확실하지 않다면, [https://nodejs.org/en/download](https://nodejs.org/en/download) 에서 설치 프로그램을 받을 수 있습니다.
* 터미널에서 `npm install -g @anthropic-ai/claude-code`를 실행하세요.
* 설치가 끝나면 터미널에서 `claude`를 실행하세요. 이 명령어를 처음 실행하면 인증을 요청하는 메시지가 표시됩니다.

만약 AWS Bedrock이나 Google Cloud Vertex를 사용하신다면, 추가 설정이 필요합니다:
* **AWS Bedrock 특별 안내**: [https://docs.anthropic.com/en/docs/claude-code/amazon-bedrock](https://docs.anthropic.com/en/docs/claude-code/amazon-bedrock)
* **Google Cloud Vertex 특별 안내**: [https://docs.anthropic.com/en/docs/claude-code/google-vertex-ai](https://docs.anthropic.com/en/docs/claude-code/google-vertex-ai)