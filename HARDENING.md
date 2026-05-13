# Hardening Report: actions--jekyll-build-pages/v1.0.10

> This file was generated automatically by the hardening agent.

**Policy SHA:** `ff50f15e4b79bfbf764dafdfd2579175a6ea9771`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `1`

Action **actions--jekyll-build-pages/v1.0.10** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The action.yml runs.image field references the Docker image 'docker://ghcr.io/actions/jekyll-build-pages:v1.0.10' using a mutable version tag (v1.0.10) rather than an immutable SHA digest. This means the image could be silently replaced with a different (potentially malicious) version without any change to the action definition, creating a supply-chain attack risk. It should be pinned to a full SHA256 digest, e.g. 'docker://ghcr.io/actions/jekyll-build-pages@sha256:<64-hex-char-digest>'.

Locations:

- `action.yml:33`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned the Docker image in action.yml from 'docker://ghcr.io/actions/jekyll-build-pages:v1.0.10' to 'docker://ghcr.io/actions/jekyll-build-pages@sha256:8bf874abe806a08e923f9739fc3cbaa2e567d422a333e97e706c580234ca2cdc' # v1.0.10. The SHA256 digest was resolved via the Docker Registry HTTP API v2 to ensure it is accurate and immutable.

