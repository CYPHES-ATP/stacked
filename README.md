# CYPHES Node

CYPHES Node is the first local node for the CYPHES Agent Transfer Protocol: an open-source autonomous coding-agent runtime for running, inspecting, and eventually transferring agent work through explicit approvals, contracts, and receipts.

The product name is CYPHES everywhere. The repository name is `CYPHES-ATP/node`.

This repository is intentionally clean-room from Anthropic's proprietary Claude Code source. See [docs/PROVENANCE.md](docs/PROVENANCE.md) and [docs/adr/0001-phase-1-agent-runtime.md](docs/adr/0001-phase-1-agent-runtime.md).

## Product Direction

CYPHES is built to make autonomous agent collaboration inspectable:

- A local node that can operate through a CYPHES-branded terminal and IDE experience.
- A permission-first interface for tool use, edits, shell commands, and external context.
- Receipts for meaningful agent actions, including provider, model, prompt hash, artifact hash, tool events, approval events, and final patch hash.
- A staged path toward CYPHES Agent Transfer Protocol networking, transfer, and settlement workflows.

The visual language follows the CYPHES system: near-black surfaces, precise grid structure, cyan/green execution accents, restrained orange risk accents, glassy panels, dense technical typography, and receipt-oriented audit surfaces.

## Phase 1 Scope

Phase 1 is the local node foundation:

- Preserve GPL-3.0 obligations and upstream provenance.
- Rebrand visible product surfaces to CYPHES.
- Replace inherited product copy, domains, package metadata, command names, screenshots, and UI language.
- Keep the agent runtime stable while the UI/UX changes are made.
- Add CYPHES approval, receipt, and provenance language before broader publication.
- Prepare GitHub issues, docs, release hygiene, and security policy for a public project.

## Phase 2 Direction

CYPHES Node v0.1 will add a three-stage collaboration loop:

1. Drafter creates a plan and proposed patch.
2. Reviewer independently critiques the draft against the contract.
3. Synthesizer resolves review findings into final output.

The user approves each stage. The system records structured receipts for the work.

## Repository Status

Visible product surfaces should say CYPHES. Legal provenance and license files may still name the upstream project where attribution is required.

## Development

The Rust workspace lives under [src-rust](src-rust).

```bash
cd src-rust
cargo check --workspace
cargo test --workspace
```

For UI/TUI changes, verify both interactive and headless paths where possible:

```bash
cd src-rust
cargo run -p cyphes -- --print "explain this repository"
cargo run -p cyphes
```

## Governance

- [Roadmap](docs/ROADMAP.md)
- [Provenance](docs/PROVENANCE.md)
- [Security](SECURITY.md)
- [Contributing](CONTRIBUTING.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [Notice](NOTICE.md)

## License

CYPHES Node is distributed under GPL-3.0. See [LICENSE](LICENSE), [LICENSE.md](LICENSE.md), and [NOTICE.md](NOTICE.md).
