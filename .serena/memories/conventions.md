# Conventions
- Apply the repository root `.clang-format` to C/C++/CUDA files.
- Formatting essentials: 4-space indentation, no tabs, left-aligned pointers, custom brace rules, no column limit, latest language standard.
- Contribution rules require formatting before commit and recommend the repository pre-commit hook.
- Preserve module boundaries expressed by per-domain `src/*/CMakeLists.txt`; shared low-level infrastructure belongs under `src/core`.
- For runtime/UI changes, use MCP resource discovery before reading implementation code; verify mutations through state resources/tools as directed by `AGENTS.md`.
- Long-running app operations must be monitored with runtime jobs/events instead of sleeps.