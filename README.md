# 2026 유럽 여행 대시보드

2026년 9월 독일·포르투갈 여행의 일정과 예약 현황을 보는 단일 HTML 대시보드.
빌드 도구 없이 `index.html` 하나로 동작한다.

- 보기: https://lawyerd.github.io/europe-2026/
- 데이터: `index.html` 최상단 `const TRIP = {...}` 객체만 고치면 화면에 반영된다.

## 개인 정보 분리

예약번호, 체크인 PIN, 확인서 PDF, 동행 모집글은 이 저장소에 없다.
비공개 저장소 `europe-2026-private` 에 두고, 로컬에서는 심볼릭 링크로 연결해 쓴다.
링크가 없어도 대시보드는 정상 동작하며, 해당 값만 "비공개"로 표시된다.

```bash
git clone https://github.com/Lawyerd/europe-2026.git
git clone https://github.com/Lawyerd/europe-2026-private.git
bash europe-2026-private/link.sh
```
