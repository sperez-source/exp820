# Code quality finding: unimplemented retry backoff

Tracking note for a temporary review PR. Stop at PR creation; do not merge.

## Finding

- Location: `lib/partial-implementations/webhook-retry/retry_policy.py`
- Symbol: `compute_backoff_seconds`
- Issue: function is a stub (`NotImplementedError`) with an explicit TODO to implement exponential backoff (`base * 2^attempts`).
- Severity (manual): medium — retry dispatcher cannot schedule delays until this is implemented.
- GitHub Code Quality API: finding #1 was not readable (403 / resource not accessible). This note stands in for that finding.

## Intended fix (not applied on this branch)

Implement `return BASE_DELAY_SECONDS * (2 ** attempts)` and keep `should_retry` gated on `MAX_ATTEMPTS`.
