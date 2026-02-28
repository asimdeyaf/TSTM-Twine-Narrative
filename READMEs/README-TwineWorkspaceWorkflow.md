# Twine Workspace Workflow

## Purpose
This workspace is the local source for Twine story editing and related narrative sync tasks.

Primary story target:
- `/Users/asimdeyaf/Documents/Twine/Stories/tstm-story-script.html`

Out of scope unless explicitly requested:
- `/Users/asimdeyaf/Documents/Twine/Stories/tstm-animatic.html`

## Session Start Checklist
Run these before editing:

```bash
cd /Users/asimdeyaf/Documents/Twine
git fetch origin --prune
git status -sb
```

If behind `origin/main`:

```bash
git pull --rebase origin main
```

## Editing and Logging Flow
1. Confirm sync status.
2. Make Twine story changes.
3. Add/update daily log in `READMEs/WorkLogs/Asim_WorkLog_YYYY-MM-DD.md` with local timestamp and operator name (`Asim Deyaf`).
4. Commit and push when ready.

## Commit and Push
```bash
git add .
git commit -m "Short, clear message"
git push origin main
```

## Cross-Tool References
- Unity sync workflow:
  - `Assets/__TSTM__/READMEs/Documentation/Process/CrossTool/README-TwineVODSyncWorkflow.md`
- Twine format standard:
  - `Assets/__TSTM__/READMEs/Documentation/Standards/CrossTool/README-TwineStoryScriptFormat.md`
