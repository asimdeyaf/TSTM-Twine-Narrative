# AGENTS.md (Twine Workspace)

## Scope
- Applies to `/Users/asimdeyaf/Documents/Twine`.
- Primary target for story-script tasks:
- `/Users/asimdeyaf/Documents/Twine/Stories/tstm-story-script.html`
- Explicitly out-of-scope unless requested:
  - `/Users/asimdeyaf/Documents/Twine/Stories/tstm-animatic.html`

## Working Rules
- Treat the Twine story file as a structured narrative source, not a plain text dump.
- Preserve passage names and branching structure unless a requested change requires structural edits.
- For dialogue synchronization tasks, coordinate with Unity-side VO dialogue sheets under:
  - `Assets/__TSTM__/READMEs/VO_Dialogue/`
- When changes are ambiguous, prefer producing a reconciliation proposal before applying edits.

## Session Start Git Sync Check
- Before making edits, run:
  - `git fetch origin --prune`
  - `git status -sb`
- If local is behind `origin/main`, run `git pull --rebase origin main` before any file changes.
- If local has uncommitted changes from another session, reconcile those first (commit, stash, or explicitly continue).

## Local and Cloud Git Behavior
- Codex Local and Codex Cloud are separate Git clones of the same repository.
- Editing in Cloud does not update GitHub automatically; changes must be committed and pushed.
- `git push` only sends commits. Uncommitted file edits cannot be pushed.
- Always do `pull -> edit -> commit -> push` in whichever environment is active.
- When switching environments, sync first (`git fetch origin --prune`, `git status -sb`, and `git pull --rebase origin main` if behind).

## Work Logs
- Work logging is required for every meaningful edit block (story changes, structure changes, or documentation updates).
- Keep a running daily work log in:
  - `READMEs/WorkLogs/Asim_WorkLog_YYYY-MM-DD.md`
- Add an entry for each meaningful work block with:
  - local timestamp (`HH:MM` with timezone)
  - operator name (`Asim Deyaf`, plus collaborator when relevant)
  - sync status (`git status -sb`)
  - files changed
  - short summary of narrative or structure edits
  - commit hash (if committed)

## Cross-References
- Unity cross-tool sync process:
  - `Assets/__TSTM__/READMEs/Documentation/Process/CrossTool/README-TwineVODSyncWorkflow.md`
- Twine script format standard:
  - `Assets/__TSTM__/READMEs/Documentation/Standards/CrossTool/README-TwineStoryScriptFormat.md`
