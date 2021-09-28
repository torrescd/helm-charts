
### cronjobs

If `cronjobs` field is set, then cronjobs will be deployed instead of a deployment.

Any of the "global" values can be overridden in each cronjob definition.

The following values can be overwritten on the first container in each cronjob definition: `command`, `args`, `resources`.

```yaml
# default settings
cronjobs:
- schedule:
  concurrency: 'Allow' ('Allow', 'Forbid', 'Replace')
  suspend: false
  retries: 3
  timeout:
```

```yaml
# explanations

cronjobs:
- schedule: the cron schedule for the job
  concurrency: allow concurrent runs of the cronjob, forbid them, or force new jobs to replace old ones
  suspend: disable this cronjob, can be used for creating on-demand jobs
  retries: number of retries to attempt on failed jobs
  timeout: number of seconds to allow this job to run in
```
