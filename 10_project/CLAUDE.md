# 10_project — 끝이 있는 작업

## 역할
완성하면 끝나는 작업 공간. 웹페이지 제작, 기획서, 캠페인 준비 등.
프로젝트 1개 = 폴더 1개. 각 프로젝트 폴더 안 CLAUDE.md에 그 프로젝트 전용 규칙.

## 넣는 것 / 넣지 않는 것
- 넣음: 계속 고쳐가는 작업물(코드, 기획 문서), 그 프로젝트 전용 자료
- 안 넣음: 매일 도는 자동화 (20_daily), 여러 프로젝트 공용 자료 (30_resource), 한 번 뽑고 끝나는 완성본 (98_output)

## 구조
10_project/프로젝트명/
- CLAUDE.md — 목적, 스택, 규칙
- README.md — 실행·확인 방법
- docs/plan.md — 기획 (목표, 타겟, 핵심 기능)
- docs/progress.md — 진행 로그

## 작업 규칙
1. 새 프로젝트: 90_manual/templates/project/ 통째 복사 → 이름 변경 → CLAUDE.md·plan.md 빈칸을 사용자와 채우기.
2. 기존 프로젝트 작업 시작: 그 폴더 CLAUDE.md → docs/progress.md 마지막 항목 확인 후 이어서.
3. 작업 끝날 때: progress.md에 날짜 + 한 일 + 다음 할 일 기록.
4. 결과물 파일(PDF, 캡처 등)은 98_output/에 저장.
5. 완료로 보이면 99_archive 보관 제안.

## 금지
- 프로젝트 파일을 10_project/ 바로 아래 두기 (반드시 프로젝트 폴더 안)
- 같은 파일 복사본 만들기 (index_final.html 등). 버전은 git으로
