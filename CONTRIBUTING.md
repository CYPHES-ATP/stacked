# Contributing

Thanks for helping build CYPHES. This project is in Phase 1, so the highest-value contributions are careful, well-scoped changes that move the node toward a clean CYPHES experience without destabilizing the runtime.

## Ground Rules

- Do not copy or adapt leaked Anthropic Claude Code source.
- Preserve GPL-3.0 licensing and upstream attribution.
- Keep changes small enough to review.
- Prefer existing runtime architecture until a CYPHES replacement is explicitly designed.
- Avoid broad rewrites during Phase 1 unless an issue or ADR calls for them.
- Never commit secrets, provider keys, private prompts, or local receipt artifacts.

## Development Setup

```bash
cd src-rust
cargo check --workspace
```

For Rust changes, run:

```bash
cargo fmt --all
cargo check --workspace
cargo test --workspace
```

For focused package work, run the smallest relevant test first, then expand as risk increases.

## Rebrand Work

When replacing inherited UI/UX with CYPHES:

- Update user-facing copy before internal identifiers when possible.
- Preserve compatibility aliases until the migration plan says otherwise.
- Keep NOTICE and provenance accurate.
- Use the CYPHES design language: dark execution surfaces, cyan/green status accents, orange risk accents, grid structure, glass panels, compact technical controls, and receipt-oriented audit states.

## Pull Requests

Every PR should include:

- What changed.
- Why it changed.
- How it was tested.
- Any license, provenance, or security considerations.

Use the pull request template and link related issues.

## Commit Hygiene

- Keep commits focused.
- Do not bundle unrelated refactors.
- Do not rewrite upstream history.
- Do not force-push shared branches without maintainer approval.
