# Priority Field

!!! info "To update the `priority` field modify the `SA-AwsAssets - Lookup Gen` saved search. It is recommended to clone the default search before making changes (see [Clone Saved Search](../best-practice/clone-search))."

All assets are set to "medium" by default and should be updated to suite your environment.

The following is an example of how this may be set up.

```python
priority=case(
    match(category, "domain_controller"), "critical",
    match(category, "server|ubuntu|rhel|linux"), "high",
    true(), "medium"
    )
```
