# claude-workspace

Claude Code와 함께 일하기 위한 폴더 양식입니다.
폴더마다 역할이 정해져 있어서, Claude가 "무엇을 어디서 찾고 어디에 저장할지" 헤매지 않고, 사람도 한눈에 파악할 수 있습니다.

## 폴더 구성

| 폴더 | 용도 | 예시 |
|---|---|---|
| `00_inbox` | 어디 둘지 모르는 파일 임시 보관 | 다운받은 파일, 캡처 |
| `10_project` | 끝이 있는 작업 | 랜딩페이지 제작 |
| `20_daily` | 계속 돌아가는 자동화 | 매일 아침 광고 성과 슬랙 알림 |
| `30_resource` | 여러 작업에서 같이 보는 참고자료 | 브랜드 가이드, 시장조사 |
| `40_toolkit` | 직접 만든 스킬·에이전트 | 워드 문서 생성 스킬 |
| `90_manual` | 반복 업무 매뉴얼 + 새 폴더 틀 | Netlify 배포 방법 |
| `98_output` | 완성된 결과물 | 2026-10-01_견적서.docx |
| `99_archive` | 끝난 작업 보관 | 종료된 캠페인 |

각 폴더의 `README.md`는 사람용 설명, `CLAUDE.md`는 Claude가 따르는 규칙입니다.

## 시작하기

### Claude에게 맡기기 (추천)

Claude Code를 열고 아래 문구를 그대로 붙여넣으세요. `[기존 폴더 경로]`만 내 자료가 있는 폴더로 바꾸면 됩니다.
작업공간을 만들고, 기존 자료를 어디로 옮길지 표로 먼저 보여준 뒤, 확인을 받고 복사합니다. (원본은 그대로 남습니다)

```
https://github.com/dkyun-lee/claude-workspace 양식으로 내 Claude 작업공간을 만들어줘.

1. 만들기
   - 위치: ~/Desktop/claude-workspace (다른 곳이 낫다면 먼저 물어봐)
   - README.md와 각 폴더 CLAUDE.md를 읽고 규칙을 이해한 뒤 시작해줘.

2. 기존 자료 옮기기
   - 옮길 곳: [기존 폴더 경로. 예: ~/Documents/업무, ~/Desktop/작업]
   - ~/.claude 안에 내가 직접 만든 스킬·에이전트·CLAUDE.md·메모리가 있으면 그것도 대상.
   - 먼저 전부 훑어보고 "파일·폴더 | 무슨 내용 | 옮길 곳(번호 폴더)" 표로 제안만 해줘.
     내가 확인하기 전엔 아무것도 옮기지 마.
   - 확인 후엔 이동이 아니라 "복사"로. 원본은 내가 직접 지울게.
   - 분류 기준:
     · 끝이 있는 작업 → 10_project/이름/ (templates/project 틀 적용)
     · 계속 도는 자동화·봇 → 20_daily/이름/ (실행 위치 꼭 기재)
     · 참고자료 → 30_resource/주제/ + _index.md 목차
     · 직접 만든 스킬·에이전트 → 40_toolkit/ 로 옮기고 ~/.claude 엔 심링크
     · 반복 업무 절차 → 90_manual/ 매뉴얼
     · 완성본 → 98_output/ (날짜_내용 이름)
     · 끝난 일 → 99_archive/
     · 애매한 것 → 00_inbox/
   - API 키·비밀번호가 보이면 문서에서 빼서 .env 로 옮기고, 어디서 발견했는지 알려줘.
   - 기존 CLAUDE.md나 메모리에 있던 내 규칙은 루트 CLAUDE.md 아래 "내 전용 규칙"에 합쳐줘.

3. 마무리
   - 옮긴 결과를 폴더별로 요약해주고, 분류 못 한 것 목록을 따로 보여줘.
```

### 직접 설치하기

1. 저장소 받기
   ```
   git clone https://github.com/dkyun-lee/claude-workspace.git
   cd claude-workspace
   ```
2. (스킬이 있다면) 스킬 연결 — `40_toolkit/README.md` 참고
3. claude-workspace 폴더에서 Claude Code 실행
   ```
   claude
   ```

## Claude에게 이렇게 말하면 됩니다

- "새 프로젝트 my-landing 만들어줘"
- "매일 아침 광고 성과 알려주는 봇 새로 만들자"
- "inbox 정리해줘"
- "이 PDF 브랜드 자료로 정리해줘"
- "Netlify 배포해줘" (매뉴얼이 있으면 매뉴얼대로 진행)
- "my-landing 끝났어, 보관해줘"

## 공유 범위

GitHub에는 **빈 틀(폴더 구조·규칙·틀·매뉴얼·스킬)만** 올라갑니다.
`00_inbox`, `10_project`, `20_daily`, `30_resource`, `98_output`, `99_archive`의 실제 파일과 `.env`(비밀값)는 각자 컴퓨터에만 남습니다.
