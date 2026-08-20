# Quality finding: incomplete webhook retry dispatcher

**Source:** `lib/partial-implementations/webhook-retry/dispatcher.py`

GitHub Code Quality findings are not enabled/accessible on this repository (`403` on `/code-quality/findings/1`). Manual review found these outstanding TODOs:

```python
# TODO: HTTP POST to event.url with event.payload
# TODO: on failure, mark_attempt and schedule backoff via compute_backoff_seconds
```

`dispatch_pending()` currently only calls `mark_attempt` and never delivers the webhook or applies backoff. This is the same gap tracked in issue #11 (Add webhook retry backoff) and issue #4 (Webhook retry test fails intermittently).

Temporary branch for tracking only. Safe to delete after review.
