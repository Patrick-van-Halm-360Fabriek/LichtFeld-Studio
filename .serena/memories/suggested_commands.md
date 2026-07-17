# Suggested commands
- Configure Linux similarly to CI: `cmake -B build -S . -G Ninja -DCMAKE_BUILD_TYPE=Release -DCMAKE_CUDA_COMPILER=/usr/local/cuda/bin/nvcc -DBUILD_PYTHON_STUBS=OFF -DLFS_DEV_IMPORT_SOURCE_PYTHON=OFF -DLFS_DEV_IMPORT_SOURCE_RESOURCES=OFF -DCUDA_DEVICE_DEBUG=OFF`.
- Build: `cmake --build build -j "$(nproc)"`.
- Enable unit tests during configure with `-DBUILD_TESTS=ON`, then run `ctest --test-dir build --output-on-failure`.
- Isolated path test: configure with `-DBUILD_UNICODE_TEST_ONLY=ON`, run `ninja -C build unicode_path_test`, then `ctest --test-dir build -R UnicodePathTest --output-on-failure`.
- Install the repository hook: `cp tools/pre-commit .git/hooks/`.
- Portable install after a portable build: `cmake --install build --prefix ./dist`.
- Runtime/UI automation: initialize the MCP server from `.mcp.json`, then discover resources/tools per `AGENTS.md`; do not guess operator or UI ids.