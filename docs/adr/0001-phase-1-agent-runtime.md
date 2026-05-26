# ADR 0001: Phase 1 Agent Runtime

## Status

Accepted.

## Date

2026-05-25

## Context

CYPHES needs a local autonomous coding-agent node before the broader Agent Transfer Protocol network can be tested. Phase 1 therefore prioritizes a working runtime, a CYPHES-branded control surface, provenance hygiene, permission UX, and publication readiness.

The evaluated options were:

- Fork an existing open-source Rust terminal coding-agent runtime.
- Use `yasasbanukaofficial/claude-code`.
- Use `vellum-ai` projects as a base.

## Decision

Use the open-source Rust runtime recorded in [NOTICE.md](../../NOTICE.md) as the Phase 1 base.

Do not use `yasasbanukaofficial/claude-code` or any repository that represents itself as leaked Anthropic Claude Code source.

Use `vellum-ai` projects only as architectural inspiration for memory, trust, credentials, sandboxing, and assistant lifecycle concepts.

## Rationale

The selected base provides the closest technical foundation for Phase 1:

- Rust coding-agent runtime.
- Terminal UI.
- Multi-provider support.
- Tool permissions.
- Plugin-oriented architecture.
- ACP support for editor integration.
- GPL-3.0 open-source licensing.

The leaked Claude Code mirror is rejected because it creates unacceptable provenance, licensing, publication, and trust risk.

Vellum is not selected as the base because it is a broader personal assistant platform rather than a focused coding-agent node/runtime. Its security and memory architecture can still inform later CYPHES design.

## Consequences

- CYPHES Node inherits GPL-3.0 obligations.
- Upstream attribution must remain visible in `NOTICE.md` and license/provenance files.
- CYPHES UI/UX work should be tracked as a rebrand and product-layer migration, not as a clean rewrite.
- Public release requires a provenance and workflow audit.
- Future proprietary or permissive components should be separated carefully and reviewed before distribution.

## Follow-Up Work

- Audit and update upstream workflows before enabling public releases.
- Replace inherited public copy, domains, screenshots, package metadata, and command names.
- Add CYPHES permission and receipt surfaces.
- Prepare the first ATP node workflow ADR before protocol transfer features are implemented.
