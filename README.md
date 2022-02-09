## How does it work?

This project uses GitHub actions to wake up every instant configured in (`.github/health-check.yml`) file and run a shell script (`health-check.sh`). This script runs `curl` on every url in your config and appends the result of that run to a log file and commits it to the repository. This log is then pulled dynamically from `index.html` and displayed in a easily consumable fashion. You can also run that script from your own infrastructure to update the status page more often.

## What does it not do (yet)?

1. Incident management.
2. Outage duration tracking.
3. Updating status root-cause.
