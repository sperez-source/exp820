# Advisory tracking: GHSA-rcr2-hggw-43wm

Temporary tracking note for a global GitHub Security Advisory.
This is not a repo-local code scanning, Dependabot, or secret-scanning alert.
Those products are not enabled or not accessible on this repository.

- GHSA: [GHSA-rcr2-hggw-43wm](https://github.com/advisories/GHSA-rcr2-hggw-43wm)
- CVE: CVE-2026-55211
- Package: `surfio` (pip)
- Severity: critical
- CWE: CWE-125 (out-of-bounds read)
- Affected: surfio < 0.0.19
- Fixed: 0.0.19

## Action

If this repository (or a downstream environment) ever depends on `surfio`, require version 0.0.19 or later. Do not add the package unless needed.
