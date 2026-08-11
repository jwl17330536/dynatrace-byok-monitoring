# AGENTS

This repository is public and must remain easy for non-developers to deploy while supporting contributor iteration.

## Non-negotiable rules

1. Keep one canonical end-user install path in `README.md` and `QUICK_START.md`.
2. Keep contributor-only workflows in `CONTRIBUTING.md`.
3. Keep tenant-specific values and secrets out of tracked files; use placeholders and local overrides.
4. Keep local/private scaffolding untracked (`.local.*`, `local-only/`, private notes).
5. Public repo behavior must not depend on private/internal sibling repos.
6. Keep workflow artifacts and setup docs synchronized on every behavior change.
7. Keep strict PII/secret checks and required branch protections green before release.

## Publishing expectations

1. Setup docs must be current and executable by someone without IDE-specific context.
2. Keep focused vs extended workflow behavior clearly documented.
3. Add troubleshooting and verification guidance whenever configuration behavior changes.
