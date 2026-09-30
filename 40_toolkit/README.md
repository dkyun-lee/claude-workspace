# 40_toolkit
직접 만든 Claude 스킬과 에이전트의 원본을 두는 곳입니다.

Claude Code는 `~/.claude/` 안의 스킬만 인식하기 때문에, 여기 원본을 두고 바로가기(심링크)로 연결해서 씁니다.
여기서 고치면 바로 반영됩니다.

## 처음 받았을 때 연결하기
claude-workspace 폴더에서 스킬·에이전트마다 한 번씩 실행:
```
ln -s "$PWD/40_toolkit/skills/스킬명" ~/.claude/skills/스킬명
ln -s "$PWD/40_toolkit/agents/에이전트명.md" ~/.claude/agents/에이전트명.md
```
