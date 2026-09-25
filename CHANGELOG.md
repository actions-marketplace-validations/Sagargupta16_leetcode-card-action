# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-09-25

### Added

- Composite action that renders an animated LeetCode card into your repo, `assets/leetcode.svg` by default: the contest rating history as a line that draws itself in with the peak marked, plus badge, rating, top percentage, contests, solved count and Easy/Medium/Hard progress bars.
- Inputs `username` (required), `output`, `accent` and `title`. `{contests}` in `title` becomes the number of rated contests attended.
- Outputs `rating`, `badge`, `solved` and `contests`.
- A shorter card without the chart for users with fewer than two rated contests, reading "No contests yet" when there are none, and the rating in place of the badge for users without one.
- Fallback when LeetCode fails: the existing card is kept and the run warns. The step fails only when there is no card to keep yet.
- CI: ruff, pytest on Python 3.12, 3.13 and 3.14, and a job that runs `action.yml` against a live profile.

[1.0.0]: https://github.com/Sagargupta16/leetcode-card-action/releases/tag/v1.0.0
