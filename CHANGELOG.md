# Changelog — task-runner

All notable changes to this skill are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.0.0] — 2026-02-17

### Added
- Initial release of the task-runner skill
- Multi-task intake: parse natural-language task lists into structured JSON objects
- Task types: info-lookup, file-creation, code-execution, agent-delegation, reminder-scheduling, messaging, unknown
- Execution loop with retry logic (configurable max retries, default 3)
- Per-task verification using type-appropriate checks (references/verification-guide.md)
- Per-task user notification on done/blocked/skipped
- Final summary table after all tasks reach terminal state
- Blocked task handling with `user_action_required` instructions
- Parallel execution support for independent info-lookup and file-creation tasks
- Configurable `TASK_RUNNER_DIR` (TOOLS.md) and `TASK_RUNNER_MAX_RETRIES` (env var)
- Persisted task state to `YYYY-MM-DD-tasks.json` with merge support
- Edge case handling: ambiguous tasks, tool unavailability, task dependencies, 20+ task batching
- Full test suite in `tests/`
- References: `task-types.md`, `verification-guide.md`
