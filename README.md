# TIG240 Portfolio

A shared portfolio site built collectively by the 14 project groups in **TIG240 — Data-Driven Organizational Development**, Spring 2026.

The site has three purposes:

1. **Showcase** the work of all groups externally.
2. **Position** each app against the others in the same challenge.
3. **Raise the quality floor** by making everyone's work visible to everyone else.

## Status

This repository is a **seed**. The architectural decisions (purpose, schema, coupling, axes of variation) are made by the class during **Workshop Session 1** and recorded under `docs/decisions/`. The individual group pages are added by groups during **Workshop Session 2**.

| File | Status |
|---|---|
| `docs/decisions/purpose.md` | Filled in Session 1 |
| `docs/decisions/schema.md` | Filled in Session 1 |
| `docs/decisions/coupling.md` | Filled in Session 1 |
| `docs/decisions/axes-of-variation/<challenge>.md` | Drafted in Session 1, refined async |
| `docs/challenges/<challenge>/<park>.md` | Created by each group in Session 2 |

## Run locally

```bash
pip install mkdocs-material
mkdocs serve
```

Then open <http://127.0.0.1:8000>.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the PR workflow used in Session 2.

## First-time setup (instructor)

After pushing this repository to GitHub for the first time:

1. **Settings → Pages → Source** — set to **GitHub Actions**. Required for the deploy workflow to publish the site.
2. **Settings → Branches → Branch protection rules** — add a rule for `main`:
   - Require a pull request before merging
   - Require approvals: **1**
   - Require review from Code Owners
   - Block force pushes
   - Block deletions
   - (Optional) Require status checks to pass — select the `build` job from the deploy workflow once it has run at least once.
3. **`.github/CODEOWNERS`** — replace the `@TRACK-LEAD-*` and `@INSTRUCTOR` placeholders with the real GitHub usernames (track leads nominated in Session 1, instructor's own handle).

Until step 3 is done, "Require review from Code Owners" should be left **off** — GitHub silently ignores rules whose owners don't resolve, but the placeholders will produce confusing reviewer prompts.

## License

MIT — see [LICENSE](LICENSE).