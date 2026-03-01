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
- Twine file is the VO script source of truth (no separate CSV handoff).
- Unity-side VO assets:
  - Unity project root: `/Users/asimdeyaf/Dropbox/VR Sim Labs LLC/_UNITY/_OfficalCollabProjects/TheSimulationTM`
  - Note: folder name is intentionally referenced as on disk (`_OfficalCollabProjects`).
  - `Assets/__TSTM__/Audio/VO/` (story VO and call-outs)
  - `Assets/__TSTM__/Audio/VO/CivilianCallouts/`
  - `Assets/__TSTM__/Audio/VO/CombatCallouts/`
  - `Assets/__TSTM__/Audio/SFX/`
- Deprecated references (kept for historical context, not active workflow):
  - `Assets/__TSTM__/READMEs/Documentation/Process/CrossTool/README-TwineVODSyncWorkflow.md`
  - `Assets/__TSTM__/READMEs/Documentation/Standards/CrossTool/README-TwineStoryScriptFormat.md`
