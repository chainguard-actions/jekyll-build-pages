# Hardening Report: actions--jekyll-build-pages/v1.0.11

> This file was generated automatically by the hardening agent.

**Policy SHA:** `ff50f15e4b79bfbf764dafdfd2579175a6ea9771`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `1`

Action **actions--jekyll-build-pages/v1.0.11** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The `runs.image:` field in action.yml references the Docker image `docker://ghcr.io/actions/jekyll-build-pages:v1.0.11` using a mutable version tag (`v1.0.11`) rather than an immutable SHA digest. This means the image could be replaced with a different (potentially malicious) version without changing the action.yml reference, creating a supply-chain attack risk. It should be pinned to a specific SHA digest, e.g. `image: ghcr.io/actions/jekyll-build-pages@sha256:<64-hex-char-digest>`

Locations:

- `action.yml:28`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned the Docker image reference in action.yml from the mutable tag `ghcr.io/actions/jekyll-build-pages:v1.0.11` to the immutable digest `ghcr.io/actions/jekyll-build-pages@sha256:95257bba091ab696903356491d35da5e27a335895dc234fff0cb4e6383277f47`, with the original tag preserved as a comment.

