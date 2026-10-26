# Jenkins push 자동 실행 확인

2.5 실습에서는 `main`에 push한 변경으로 Jenkins의 `devops-app` Job이 자동 시작되는지 확인합니다.

- GitHub Webhook: Content type은 `application/json`, 이벤트는 push로 설정합니다.
- Payload URL: 실행 중인 ngrok 공개 HTTPS 주소 뒤에 `/github-webhook/`을 붙입니다.
- Jenkins: `GitHub hook trigger for GITScm polling`을 활성화하고 `*/main`을 감시합니다.
- Pipeline 경로: `devops-lab/ch03-jenkins/Jenkinsfile`

Recent Deliveries 성공은 요청 전달 확인입니다. 자동 실행된 빌드의 결과는 Jenkins에서 별도로 확인합니다.
실습 중에는 ngrok 프로세스를 유지하고, 공개 주소가 바뀌면 Payload URL도 수정합니다.
