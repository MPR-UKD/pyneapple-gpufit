# Vendored third-party code

This directory contains code and prebuilt binaries from
[Gpufit](https://github.com/gpufit/Gpufit), an open-source toolkit for
GPU-accelerated curve fitting. They are redistributed under the MIT license
(see below).

## Origin

| | |
|---|---|
| Upstream project | <https://github.com/gpufit/Gpufit> (MIT) |
| Fork used for the CUDA kernels | <https://github.com/darksim33/GPUfit> (`main`, MIT) |
| Python bindings (`pygpufit/*.py`) | Gpufit `pygpufit` 1.2.0 (see `pygpufit/version.py`) |

The fork adds bi- and tri-exponential model functions and fixes to their
derivative calculations (see the plugin `CHANGELOG.md`).

## Prebuilt binaries

| File | Platform | Size (bytes) | Added in | SHA-256 |
|---|---|---|---|---|
| `pygpufit/Gpufit.dll` | Windows x64 | 4967424 | `4bec165` (2026-03-30) | `ebfca281abc70c6bc6ab26ed9521c59a89206bb9b7500ec7aa856d7c23febbdc` |
| `pygpufit/libGpufit.so` | Linux x86-64 | 3353120 | `904a178` (2026-04-01) | `daaefa4802cf1307fb714a5f44f837d7e7de7b3fee7bb9840977b6495c52ce0c` |

### Build provenance

Both binaries are built from the [`darksim33/GPUfit`](https://github.com/darksim33/GPUfit) fork.

> **Status: unverified.** The commits below were inferred from file timestamps, not recorded at build time. Delete this line once the binaries have been rebuilt from the commits listed.

| | `Gpufit.dll` | `libGpufit.so` |
|---|---|---|
| GPUfit commit | [`b89fd634ebba8966d887c2e65bc6561ec062dd48`](https://github.com/darksim33/GPUfit/commit/b89fd634ebba8966d887c2e65bc6561ec062dd48) | [`ae0f2a2e9a91369a83b3ffdb15a869613271b508`](https://github.com/darksim33/GPUfit/commit/ae0f2a2e9a91369a83b3ffdb15a869613271b508) |
| CUDA toolkit | _not recorded_ | _not recorded_ |
| Compiler / CMake flags | _not recorded_ | _not recorded_ |
| Build OS | Windows | Linux |

## Verifying the binaries

```bash
sha256sum pyneapple_gpufit/_vendor/pygpufit/Gpufit.dll \
          pyneapple_gpufit/_vendor/pygpufit/libGpufit.so
```

The output must match the table above. Update this file whenever a binary is
replaced.

## License

Gpufit is distributed under the MIT license:

```
MIT License

Copyright (c) 2017 Mark Bates, Adrian Przybylski, Björn Thiel, and Jan Keller-Findeisen

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

The remainder of this package is licensed under GPL-3.0-or-later (see the
top-level `LICENSE`).
