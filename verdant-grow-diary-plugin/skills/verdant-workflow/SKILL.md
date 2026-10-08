---
name: verdant-workflow
description: >
  This skill should be used when the user asks to "implement a task in Verdant Grow Diary",
  "work on verdant-grow-diary", or requires strict adherence to the Verdant OS development workflow.
metadata:
  version: "0.1.0"
---

# Verdant Grow Diary Workflow

Follow the strict standard operating procedure detailed in `references/sop.md` when working on tasks in the `verdant-grow-diary` repository.

1. **Verify State**: Always re-read current repository instructions and re-check head, dirty state, ownership, and overlap before writing. Stop on drift, conflicting claims, missing required evidence, or a needed change outside the allowlist.
2. **Behavior Changes**: Observe the regression test fail for the intended reason before implementation. Use isolated fixtures. Then implement the smallest typed, null-safe fix using the existing architecture. Preserve separation of library logic and JSX presentation.
3. **Docs-only Changes**: Verify the actual path/link instead of claiming behavioral TDD.
4. **Preserve Controls**: Keep hooks, locks, protections, checks, and ownership controls intact. Do not touch auth, RLS, schema, Edge Functions, billing, telemetry, security workflows, Action Queue behavior, or devices.
5. **No Dangerous Actions**: No dependency or lockfile changes, unrelated cleanup, rebase, force-push, direct push to the base branch, PR, merge, enqueue, deployment, or production writes.
6. **Testing**: Run the approved targeted checks and repository-required broader checks after the final edit. Record exact commands, environment, UTC time, commit/diff identity, exit codes, and observed pass/fail/skip counts. Report pre-existing failures separately. Label unavailable checks BLOCKED and unmeasured claims NOT_MEASURED. Do not weaken checks to pass.
7. **Self-check**: Verify correctness, simplicity, architecture, security, and performance. This self-check is not independent acceptance review.
8. **Final Output**: Return exactly: changed files and why; patch/diff identity; RED/GREEN or docs verification evidence; broader check results; unresolved risks; rollback note; current ownership; exact next step for the reviewer. Then stop.
