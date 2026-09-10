# Automatic Garbanzo

GitHub PR이 병합될 때마다 lead time을 계산하는 간단한 GitHub Actions 예제 프로젝트입니다.

## 목적

- PR 생성 시점과 병합 시점의 차이를 계산합니다.
- 팀의 개발 속도와 처리 시간을 추적할 수 있습니다.
- GitHub Actions 기반으로 쉽게 실험하고 확장할 수 있습니다.

## 동작 방식

워크플로우는 `pull_request` 이벤트의 `closed` 타입에서 실행됩니다.

- PR이 병합된 경우에만 동작합니다.
- `created_at`과 `merged_at`을 비교합니다.
- 초 단위로 lead time을 계산해 로그에 출력합니다.

## 파일 구조

```text
.
├── .github/
│   └── workflows/
│       └── metrics.yml
├── LICENSE
├── README.md
└── .gitignore
```

## 사용 방법

1. 이 저장소를 GitHub에 push합니다.
2. PR을 생성하고 병합합니다.
3. GitHub Actions 탭에서 워크플로우 실행 로그를 확인합니다.
4. 로그에 출력된 lead time을 확인합니다.

## 예시 출력

```text
Lead Time: 86400 seconds
```

## 참고

이 프로젝트는 GitHub Actions 실습용으로 만들어졌으며, 이후에는 다음과 같은 기능을 확장할 수 있습니다.

- Slack / Discord 알림 전송
- CSV, JSON 데이터 저장
- 저장소별 평균 lead time 집계
- 대시보드 연동

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
