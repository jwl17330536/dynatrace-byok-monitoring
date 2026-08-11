# Contributing

## Developer Workflow

1. Edit files under `src/`.
2. Rebuild workflow artifacts:

```bash
./build.sh
```

3. Upload or apply rebuilt workflow JSON to validate behavior.

## Local Scaffolding Workflow

Use local-only files for personal configuration and notes:

1. `.env.local` or `.env.*.local` for local environment values.
2. `local-only/` for private notes or machine-specific runbooks.
3. `*.local.md` for local documentation drafts.

Do not commit local-only files. See `.gitignore` for enforced patterns.

## Quality Gates

Before submitting changes:

1. Run repository hygiene checks:

```bash
bash scripts/repo-hygiene-check.sh
```

2. Confirm no secrets or tenant-specific values are introduced.
3. Keep README and QUICK_START in sync with behavior changes.
