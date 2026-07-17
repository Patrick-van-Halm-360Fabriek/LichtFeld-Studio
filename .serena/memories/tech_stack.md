# Tech stack
- CMake project `LichtFeld-Studio`; native languages C++23, CUDA, and C.
- Requires CUDA Toolkit 12.8+ and NVIDIA hardware/driver.
- CMake uses vcpkg manifest mode via `VCPKG_ROOT/scripts/buildsystems/vcpkg.cmake` unless a toolchain is explicitly supplied; dependency manifests are `vcpkg.json` and `vcpkg-configuration.json`.
- Primary native dependencies include SDL3, RmlUi, Torch, and embedded Python/nanobind.
- Ninja is the CI generator on Linux and Windows.
- GoogleTest is used through CTest when `BUILD_TESTS=ON`; `BUILD_UNICODE_TEST_ONLY=ON` provides the isolated Unicode path test.
- Documentation has its own Node package under `docs/`.