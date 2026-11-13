# custom-build

This branch only holds the workflow that builds a custom
[Calibre-Web-Automated](https://github.com/crocodilestick/Calibre-Web-Automated) image:
the latest upstream release with the commits of the branches listed in
`PATCH_BRANCHES` applied on top.

- Image: `ghcr.io/privatepenguinzero/calibre-web-automated:latest`
  (plus `<release>-<id>` tags for each build)
- Runs nightly. A new image is published only when the release or the patches
  change, the patches apply cleanly and the upstream unit tests pass.
  Otherwise the run fails and nothing is published.
- Patches already merged upstream are skipped automatically.
- Current patches: `feat/amazon-store-region` (upstream PR #1671).

`BUILDS.txt` lists the published builds.
