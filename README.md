# travel-ceo-daily

**"대표인 나는 오늘 무엇을 해야 할까"** — 매일 아침 AI가 비즈니스 모델·브랜드·진행 상황을 읽고 오늘 할 일 3가지를 정리해 주는 저장소입니다.

- 브랜드: **여행사 대표의 비밀노트** (쓰레드 [@travel_ceo_note](https://www.threads.com/@travel_ceo_note))
- 실행: Claude Code **클라우드 루틴**, 매일 08:30 (한국 시간). 컴퓨터가 꺼져 있어도 실행됩니다.
- 결과: [`reports/`](reports/) 폴더에 날짜별 보고서 → 같은 내용이 [Issues](../../issues)로 열려 **알림 메일**로 도착

## 구조
```
CLAUDE.md          ← 루틴이 따르는 작업 지시서
context/           ← AI가 읽는 자료 (브랜드, 규칙, 비즈니스 모델 요약, 진행 상황, 로드맵)
reports/           ← 매일 생성되는 보고서
.github/workflows/ ← 보고서가 올라오면 이슈를 열어 메일 알림
```

## 흐름
1. 매일 08:30 클라우드 루틴 시작 → 이 저장소를 받아 `CLAUDE.md`대로 실행
2. `context/` + 최근 보고서 2개를 읽고 `reports/YYYY-MM-DD.md` 작성 → 커밋·푸시
3. GitHub Actions가 새 보고서를 이슈로 등록 → GitHub 알림 메일

> "해줘" 강의 36강 챌린지(예약 실행 자동화) 과제로 만들었습니다. 비밀키·개인정보는 넣지 않습니다.
