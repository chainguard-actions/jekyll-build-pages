# Hardening Report: actions--jekyll-build-pages/v1.0.13

> This file was generated automatically by the hardening agent.

**Policy SHA:** `ff50f15e4b79bfbf764dafdfd2579175a6ea9771`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `1`

Action **actions--jekyll-build-pages/v1.0.13** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The action.yml uses a Docker image reference with a mutable tag instead of a SHA digest. The image 'docker://ghcr.io/actions/jekyll-build-pages:v1.0.13' uses the tag 'v1.0.13', which can be silently replaced by a different (potentially malicious) image. It should be pinned to a specific SHA256 digest, e.g. 'ghcr.io/actions/jekyll-build-pages@sha256:<64-hex-char-digest>'.

Locations:

- `action.yml:30`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned the Docker image reference in action.yml from the mutable tag 'ghcr.io/actions/jekyll-build-pages:v1.0.13' to the immutable digest 'ghcr.io/actions/jekyll-build-pages@sha256:6791ebfd912185ed59bfb5fb102664fa872496b79f87ff8b9cfba292a7345041', with the original tag preserved as a comment.

