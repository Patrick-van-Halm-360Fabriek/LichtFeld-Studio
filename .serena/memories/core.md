# LichtFeld Studio
- Native workstation for 3D Gaussian Splatting: training, real-time visualization, Gaussian/scene editing, exports, embedded Python/plugins, and MCP automation.
- Source domains under `src/`: `app` composition; `core` shared infrastructure/tensors/CUDA; `training`; `rendering`; `visualizer` GUI; `geometry`; `io`; `preprocessing`; `sequencer`; `python`; `mcp`; `tcp`; `diagnostics`.
- Runtime/user assets live in `resources/`; third-party source in `external/`; tests in `tests/`; documentation in `docs/`.
- Repo-local MCP bridge/config can launch the app and proxy its local MCP endpoint; follow `AGENTS.md` and `docs/docs/development/mcp/` for runtime/UI operations.
- Build/toolchain details: `mem:tech_stack`.
- Common commands: `mem:suggested_commands`.
- Coding conventions: `mem:conventions`.
- Required completion checks: `mem:task_completion`.