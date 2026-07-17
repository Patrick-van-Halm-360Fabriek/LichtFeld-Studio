# Task completion
- For changed C/C++/CUDA files, run `clang-format -i <changed-files>`; CI's exhaustive formatter covers `cpp,hpp,cc,c,h,cu,cuh`.
- Configure and build the affected target: `cmake -B build -S . -G Ninja ...`, then `cmake --build build -j "$(nproc)"`.
- When behavior is testable, configure with `-DBUILD_TESTS=ON` and run `ctest --test-dir build --output-on-failure`; narrow with `-R <pattern>` during iteration.
- For runtime/UI behavior, validate through the repo MCP bridge, discover current state first, perform the operation, and confirm the resulting state/job.
- Before handoff, inspect `git status --short` and keep unrelated user changes untouched.