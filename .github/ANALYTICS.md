# GitHub Signal Analytics

These workflows are prepared locally, not run. The initial five files supplied in `assets/analytics/` are explicitly labelled static placeholders with no statistics. Successful workflows replace them automatically at the same paths; no README uncommenting is necessary. The owner-supplied profile GIF is now embedded locally after the introduction and is unrelated to these workflows; the workflows never create or modify it.

## Enable after approving and publishing the changes

1. Put the approved workflow files and placeholders on this repository's default branch. This has **not** been done by the redesign task.
2. Open **Settings → Actions → General**. Enable Actions and permit `actions/checkout`, `vn7n24fzkq/github-profile-summary-cards` and `Platane/snk` (or allow all actions). The workflows declare only `contents: write` for their single publishing job; other permissions are unset. Repository rules must permit the bot's generated-file updates to the default branch. No Pages deployment or pull-request creation permission is needed.
3. Create the read-only public-data token described below. Add it under **Settings → Secrets and variables → Actions → New repository secret**, named `PROFILE_STATS_TOKEN`.
4. Open **Actions → Profile summary → Run workflow**, select the default branch, then run it. Verify all three cards before relying on the displayed numbers.
5. Open **Actions → Contribution snake → Run workflow**, select the default branch, then run it. Verify both theme SVGs. No GIF is requested.
6. Each workflow subsequently runs once daily: summary at **01:17 UTC / 06:47 IST**, snake at **01:47 UTC / 07:17 IST**. GitHub may delay schedules and disables scheduled workflows in public repositories after extended inactivity; the Actions tab lets you re-enable them.

The shared concurrency group serializes asset publishing. Each run checks out the default branch, stages only its explicit output files, and performs a normal non-force push using the built-in token. A protected branch or concurrent external update can reject that push; the workflow will fail rather than bypass repository rules. It never edits the README. No workflow is triggered on push or pull requests.

## Tokens and permissions

**Summary data:** use a fine-grained PAT owned by the account holder, with an expiration and **Repository access: Public repositories (read-only)**. Leave account permissions at their defaults; grant no private repository access and no write/admin/workflow permissions. Save it only as `PROFILE_STATS_TOKEN`. It is supplied solely to the summary action's `GITHUB_TOKEN` environment variable.

This PAT is required for reliable account-wide profile cards: upstream documents that the repository-scoped built-in token can leave only language cards available. See the upstream [token instructions](https://github.com/vn7n24fzkq/github-profile-summary-cards#setting-up-your-github-token) and [generated-preview warning](https://github.com/vn7n24fzkq/github-profile-summary-cards/blob/v0.12.1/src/utils/file-writer.ts). Do not grant private permissions merely to obtain broader totals.

**Snake and publishing:** the built-in `${{ secrets.GITHUB_TOKEN }}` is sufficient; no additional secret is needed. `contents: write` is needed to update generated assets, not to collect public profile data. Each job's other token permissions are disabled by omission. GitHub cannot scope `contents: write` to individual paths; explicit staging limits what these workflows publish.

## Output contract

| README file / workflow output | Source | First activation |
| --- | --- | --- |
| `assets/analytics/profile-details.svg` | `profile-summary-card-output/github_dark/0-profile-details.svg` | Profile summary |
| `assets/analytics/languages-by-repository.svg` | `profile-summary-card-output/github_dark/1-repos-per-language.svg` | Profile summary |
| `assets/analytics/github-statistics.svg` | `profile-summary-card-output/github_dark/3-stats.svg` | Profile summary |
| `assets/analytics/contribution-snake-dark.svg` | `.snake-output/dark.svg` | Contribution snake |
| `assets/analytics/contribution-snake-light.svg` | `.snake-output/light.svg` | Contribution snake |

Intermediate directories exist only on the runner and are not published. The summary action's own auto-push is disabled. It generates its standard card set, but only the profile-details, repositories-per-language and statistics cards are selected. The other two intermediate SVGs, `profile-summary-card-output/github_dark/2-most-commit-language.svg` and `profile-summary-card-output/github_dark/4-productive-time.svg`, are not published or embedded. The three selected cards' frame palette is restyled without changing labels, counts, language segments or chart data. No ranks/grades are rendered by the selected upstream cards. No live statistics were generated or copied locally.

Summary cards keep an explicit graphite background in both GitHub themes. The snake has a transparent background and theme-specific empty/contribution cells: cyan snake, lime cells and coral highest-intensity highlight. `<picture>` selects dark/light versions. A reduced-motion stylesheet freezes the generated snake; the upstream SVG's base artwork supplies the static grid. This transformation and real data rendering still need confirmation on the first remote run, which was intentionally not executed.

The profile card shows GitHub-recognized contributions across available years, public non-fork repository count and a trailing-year activity chart. The statistics card shows stars, GitHub-recognized commit contributions, PRs, issues and repositories contributed to; it is not a census of every Git commit. Language distribution gives one vote to each public non-fork repository's primary language, excludes repositories without an identified language, and is not a proficiency measure. Snake cells follow the visible profile calendar, which can include anonymized private activity if the owner has enabled that GitHub setting; no private repository access is granted here.

## Local checks and public cleanup recommendation

Keep `.gitignore`: it prevents previews, caches, credentials and runner intermediates from being accidentally included. Keep `scripts/check_readme.py` if ongoing exact-case asset/link validation is desired; it has a genuine maintenance purpose and now checks `<picture>` source paths. For the leanest public tree, it can instead remain a private local utility.

Keep this file with the workflows: it documents the token, output contract, schedules and first-run recovery. Exclude `docs/profile-audit.md` and `scripts/preview_readme.py` from the eventual public commit; they are local review aids, not runtime dependencies. All four files requested for cleanup review are still present. Nothing has been deleted or committed.
