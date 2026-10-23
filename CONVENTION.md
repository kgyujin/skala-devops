# 명명 규칙 (Naming Convention)

- 같은 반은 계정 하나, namespace 하나를 공유한다. 이름 앞에 **개인 ID**(훈련생 번호, 예 `g001`)를 붙인다
- 반 번호는 `<N>`(1~4), 개인 ID는 `<ID>` 로 적는다. 소문자·숫자·하이픈만 사용한다

| 자원 | 이름 | 공유 범위 | 개인 구분 |
| --- | --- | --- | --- |
| AWS profile | `skala-gj<N>` | 반 전체 | 없음 (같은 키) |
| namespace | `skala-gj<N>` | 반 전체 | 이름 `<ID>-...`, label `owner: <ID>` |
| Harbor 프로젝트 | `harbor.skala-gj.com/skala-gj<N>` | 반 전체 | repository `<ID>-devops-lab-app` |
| Argo CD 계정 | `skala-gj<N>` (AppProject 이름도 같다) | 반 전체 | Application `<ID>-...` |
| Ingress host | `*.skala-gj.com` | 4개 반 전체 | `skala-gj<N>-<ID>-...` |
| GitHub repository | `devops-lab`, `devops-lab-manifests` | 본인 | 본인 계정 |

Argo CD Application 이름은 4개 반이 공유한다. **myapp** 같은 흔한 이름은 이미 다른 반이 사용하고 있어 등록이 거부된다.
