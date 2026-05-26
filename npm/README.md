# CYPHES npm package

**CYPHES Phase 1 package surface for the local ATP node.**

[![License](https://img.shields.io/badge/License-GPL--3.0-blue?style=flat-square)](https://github.com/CYPHES-ATP/node/blob/main/LICENSE.md)

## Status

The npm package is not ready for public CYPHES publication yet. Phase 1 is auditing release automation, package names, binary names, and installer behavior before public distribution.

For local testing, build from source:

```bash
git clone https://github.com/CYPHES-ATP/node
cd node/src-rust
cargo run -p cyphes -- --print "explain this repo"
```

## Supported platforms

| Platform | Architecture |
|----------|-------------|
| macOS    | x64, arm64 (Apple Silicon) |
| Linux    | x64, arm64 |
| Windows  | x64 |

## Links

- [GitHub](https://github.com/CYPHES-ATP/node)
- [Documentation](https://github.com/CYPHES-ATP/node/tree/main/docs)
- [Issues](https://github.com/CYPHES-ATP/node/issues)
