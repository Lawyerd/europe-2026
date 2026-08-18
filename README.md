# 2026 유럽 여행 대시보드

2026년 9월 독일·포르투갈 여행의 일정과 예약 현황을 보는 단일 HTML 대시보드.
빌드 도구 없이 `index.html` 하나로 동작한다.

- 보기: https://lawyerd.github.io/europe-2026/
- 데이터: `index.html` 최상단 `const TRIP = {...}` 객체만 고치면 화면에 반영된다.

## 개인 정보 분리

예약번호, 체크인 PIN, 항공권번호는 저장소에 올리지 않는다.
`private.js`(gitignore 대상)에 두고, 파일이 있는 기기에서만 화면에 표시된다.

```js
// private.js
const SECRETS = {
  "tw.res": "...", "ke.res": "...", "aao.res": "...", "aao.pin": "..."
};
```

예약 확인서 PDF도 `docs/`에 두되 커밋하지 않는다.

`CLAUDE.md`(작업 지침 · 예약번호와 개인 정보 포함)도 로컬에만 둔다.
