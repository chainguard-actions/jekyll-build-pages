# Hardening Report: actions--jekyll-build-pages/v1.0.12

> This file was generated automatically by the hardening agent.

**Policy SHA:** `ff50f15e4b79bfbf764dafdfd2579175a6ea9771`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `1`

Action **actions--jekyll-build-pages/v1.0.12** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The action.yml uses a Docker image reference with a mutable version tag instead of an immutable SHA digest. `image: 'docker://ghcr.io/actions/jekyll-build-pages:v1.0.12'` uses the tag `v1.0.12`, which can be silently updated to point to a different (potentially malicious) image. It should be pinned to a specific SHA256 digest, e.g. `image: 'docker://ghcr.io/actions/jekyll-build-pages@sha256:<64-hex-char-digest>'`.

Locations:

- `action.yml:27`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Replaced the mutable Docker image tag `ghcr.io/actions/jekyll-build-pages:v1.0.12` with its immutable SHA256 digest `ghcr.io/actions/jekyll-build-pages@sha256:6d640f98eee14dd0998b7387470f0dfb4bc064a53f605ba2427786bc8462631e` in action.yml line 27. The original tag is preserved as a comment for readability.

