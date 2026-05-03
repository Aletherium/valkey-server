# valkey-server

Pre-built Valkey server binaries for development environments.

## What is this?

This repository provides cross-platform Valkey binaries built from [valkey-io/valkey](https://github.com/valkey-io/valkey) via GitHub Actions. Valkey does not provide pre-built binaries for macOS — this repository fills that gap for development tools that embed Valkey as an infrastructure dependency.

## Platforms

| File | Platform |
|------|----------|
| `valkey-server-linux-amd64` | Linux x64 |
| `valkey-server-linux-arm64` | Linux ARM64 |
| `valkey-server-darwin-amd64` | macOS x64 (Intel) |
| `valkey-server-darwin-arm64` | macOS ARM64 (Apple Silicon) |

Windows is not supported — Valkey (a C project) does not compile for Windows natively.

## Download

Binaries are available on the [Releases](https://github.com/Aletherium/valkey-server/releases) page. Each release includes SHA256 checksums.

## Build details

Binaries are compiled with:
- `MALLOC=libc` — standard C allocator for maximum portability
- `BUILD_TLS=no` — TLS disabled (not needed for localhost development)
- Linux ARM64 cross-compiled with `aarch64-linux-gnu-gcc`

These are development binaries optimized for portability, not production performance. For production deployments, use the official Valkey packages with jemalloc and TLS support.

## Source & License

Built from [valkey-io/valkey](https://github.com/valkey-io/valkey) — the open-source high-performance key/value store.

Distributed under the [BSD 3-Clause License](LICENSE), the same license as Valkey.

This project is NOT affiliated with, endorsed by, or sponsored by the Valkey contributors or the Linux Foundation.