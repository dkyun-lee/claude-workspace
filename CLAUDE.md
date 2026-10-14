# claude-workspace — Claude 작업공간
모든 업무를 번호 폴더로 나눠 관리하는 작업공간. 이 파일은 길 안내, 세부 규칙은 각 폴더 CLAUDE.md.

## 작업 시작 전
- 폴더 작업 전 그 폴더 CLAUDE.md 먼저 읽기 (새 파일 생성만 할 때도).
- 어디 둘지 애매하면 사용자에게 묻기. 임의로 새 최상위 폴더 만들지 않기.

## 상황별 가이드
| 상황 | 볼 곳 | 할 일 |
|---|---|---|
| 새 프로젝트 시작 | 90_manual/templates/project/ | 복사 → 10_project/이름/ → CLAUDE.md 빈칸 채우기 |
| 새 자동화 봇 | 90_manual/templates/daily/ | 복사 → 20_daily/이름/ → 실행 위치 기재 |
| 기존 프로젝트·봇 수정 | 해당 폴더 CLAUDE.md, docs/progress.md·changelog.md | 읽고 시작, 끝나면 기록 |
| 배포·DB 등 반복 업무 | 90_manual/ | 매뉴얼대로. 없으면 공식 문서로 진행 후 매뉴얼 작성 |
| 브랜드·시장·경쟁사 자료 필요 | 30_resource/주제/_index.md | 목차 먼저, 필요한 파일만 열기 |
| 결과물(docx·pdf·이미지) 생성 | 98_output/ | YYYY-MM-DD_내용.확장자 로 저장 |
| 스킬·에이전트 제작·수정 | 40_toolkit/, 90_manual/templates/skill/ | 원본은 40_toolkit, ~/.claude엔 심링크 |
| 받은 파일·분류 미정 | 00_inbox/ | 일단 여기. "inbox 정리" 요청 시 분류 |
| 끝난 프로젝트·멈춘 봇 | 99_archive/CLAUDE.md | 보관 절차대로 이동 |
| 과거 작업 찾기 | 99_archive/ | 사용자가 요청할 때만 열기 |

## 공통 규칙
- 이름: 폴더 = 영어 소문자-하이픈 (my-landing). 결과물 파일 = 날짜_한글 가능.
- 비밀값(API 키·토큰)은 .env에만. 문서·매뉴얼·코드에 직접 쓰기 금지.
- 팀 공유 폴더: 개인 경로(옵시디언, 개인 드라이브 등) 링크 금지. 공용 자료는 30_resource에 실제 파일로.
- 확인 먼저 받을 행동: 삭제, 외부 전송(배포·푸시·메시지 발송), 봇 실행·중지.
- 규칙이 바뀌면 해당 CLAUDE.md를 고친다 (Claude 메모리에만 두지 않기).

## 폴더 지도
- 00_inbox/ — 임시 보관함
- 10_project/ — 끝이 있는 작업 (1개 = 폴더 1개)
- 20_daily/ — 계속 돌아가는 자동화 (1개 = 폴더 1개)
- 30_resource/ — 공통 참고자료 (주제별)
- 40_toolkit/ — 스킬·에이전트 원본
- 90_manual/ — 반복 업무 매뉴얼 + 새 폴더 틀(templates/)
- 98_output/ — 완성 결과물
- 99_archive/ — 보관소
