# Verdant Grow Diary Standard Operating Procedure

Task: Implement only [one approved outcome].

Repository: Verdant-OS/verdant-grow-diary
Base branch and SHA: verdant-grow-diary @ [exact SHA]
Approved working branch and starting head: [branch] @ [exact SHA]
Owner and release/reassignment evidence: [details]
Exact write allowlist: [file paths, including tests]
Approved plan: [short plan or exact plan reference]
Acceptance behavior: [observable result and edge cases]
Reviewer: [independent reviewer]
Publication permission: None. Return a patch/diff for review.

Re-read current repository instructions and re-check head, dirty state,
ownership, and overlap before writing. Stop on drift, conflicting claims,
missing required evidence, or a needed change outside the allowlist.

For behavior changes, observe the regression test fail for the intended
reason before implementation. Use isolated fixtures. Then implement the
smallest typed, null-safe fix using the existing architecture. Preserve
separation of library logic and JSX presentation. For a docs-only change,
verify the actual path/link instead of claiming behavioral TDD.

Keep hooks, locks, protections, checks, and ownership controls intact.
No dependency or lockfile changes, unrelated cleanup, rebase, force-push,
direct push to the base branch, PR, merge, enqueue, deployment, or
production writes. Do not touch auth, RLS, schema, Edge Functions,
billing, telemetry, security workflows, Action Queue behavior, or devices.

Run the approved targeted checks and repository-required broader checks
after the final edit. Record exact commands, environment, UTC time,
commit/diff identity, exit codes, and observed pass/fail/skip counts.
Report pre-existing failures separately. Label unavailable checks
BLOCKED and unmeasured claims NOT_MEASURED. Do not weaken checks to pass.

Self-check correctness, simplicity, architecture, security, and performance.
You are the builder; this self-check is not independent acceptance review.

Return: changed files and why; patch/diff identity; RED/GREEN or docs
verification evidence; broader check results; unresolved risks; rollback
note; current ownership; exact next step for the reviewer. Then stop.
