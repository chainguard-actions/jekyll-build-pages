# Hardening Report: actions--jekyll-build-pages/v1.0.9

> This file was generated automatically by the hardening agent.

**Policy SHA:** `ff50f15e4b79bfbf764dafdfd2579175a6ea9771`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `1`

Action **actions--jekyll-build-pages/v1.0.9** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The `runs.image` field in action.yml references the Docker image `docker://ghcr.io/actions/jekyll-build-pages:v1.0.9` using a mutable tag (`v1.0.9`) instead of an immutable SHA digest. This means the image could be silently replaced with a different version (potentially malicious) without any change to the action definition, creating a supply-chain attack risk. It should be pinned to a full SHA256 digest, e.g. `docker://ghcr.io/actions/jekyll-build-pages@sha256:<64-hex-char-digest>`

Locations:

- `action.yml:32`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Replaced the mutable Docker image tag `ghcr.io/actions/jekyll-build-pages:v1.0.9` with its immutable SHA256 digest `ghcr.io/actions/jekyll-build-pages@sha256:24451ed8095993a68b5d343bd93837357f3f3c2b5e9aa42095f63b6228897bc6` in action.yml line 32. The original tag is preserved as a comment outside the YAML quotes for readability.

