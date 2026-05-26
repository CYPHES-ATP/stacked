# Provenance

CYPHES Node is a CYPHES project prepared for publication with clean source provenance.

## Source Base

- Local project name: CYPHES Node
- Repository: https://github.com/CYPHES-ATP/node
- Initial phase: CYPHES UI/UX rebrand, node naming, and governance setup
- License inherited from upstream: GPL-3.0

The Phase 1 source base was selected because it provided an open-source Rust terminal coding-agent runtime with provider support, tools, permissions, plugins, and ACP integration.

## Upstream Attribution

The original upstream repository is recorded in [NOTICE.md](../NOTICE.md) for GPL attribution and auditability. Product surfaces should use CYPHES naming; attribution records may name upstream sources where required.

## Excluded Sources

This repository must not use:

- Leaked Anthropic Claude Code source.
- Mirrors or backups that describe themselves as leaked Claude Code source.
- Proprietary source maps or recovered proprietary source.
- Generated rewrites that are derived from pasted proprietary source.

Educational or internal intent does not change this rule. The project is being prepared for publication, so clean provenance is a product requirement.

## Allowed Inputs

Contributors may use:

- Existing GPL-3.0 source already present in this fork.
- Public API documentation from model providers.
- Original implementation work.
- Clean-room behavior observations.
- CYPHES design files and product direction supplied by CYPHES.

## Contributor Certification

By contributing, you certify that:

- You have the right to submit the contribution.
- Your contribution is compatible with this repository's license.
- Your contribution does not include leaked or proprietary source code.
- Any third-party code, assets, or prompts are clearly attributed and license-compatible.

## Audit Notes

Phase 1 keeps the implementation auditable while moving visible surfaces to the CYPHES node brand. Future protocol, receipt, packaging, and network changes should document material source, license, and attribution changes in this file or in linked ADRs.
