# 40_toolkit — 스킬·에이전트 원본

## 역할
직접 만든 Claude 스킬·에이전트의 원본 보관소.
Claude Code는 ~/.claude/skills·agents에서만 읽으므로, 원본은 여기 두고 심링크로 연결.

## 넣는 것 / 넣지 않는 것
- 넣음: 직접 만든 스킬, 에이전트
- 안 넣음: 스킬 테스트 결과물 (98_output), 아직 절차가 굳지 않은 업무 (90_manual 매뉴얼로 먼저)

## 구조
- skills/스킬명/SKILL.md (필수) + changelog.md (+ 선택: scripts/, references/)
- agents/에이전트명.md

## 작업 규칙
1. 새 스킬: 90_manual/templates/skill/ 복사 → skills/스킬명/ → SKILL.md 작성.
2. 연결: `ln -s "$PWD/skills/스킬명" ~/.claude/skills/스킬명` (에이전트는 agents/이름.md 동일)
3. 연결 확인: `ls -l ~/.claude/skills/스킬명` 이 wade 원본을 가리키는지. 새 세션에서 스킬 목록에 뜨는지 사용자에게 확인 요청.
4. 수정 시 changelog.md에 날짜 + 변경 + 이유.
5. 매뉴얼에서 승격된 스킬이면 해당 매뉴얼에 "스킬로 승격: 스킬명" 표기.

## 금지
- ~/.claude/skills에서 직접 수정 (원본은 여기)
- 스킬 안에 키·개인 경로 하드코딩
