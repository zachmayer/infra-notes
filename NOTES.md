# Infra Notes

Scratchpad for infrastructure setup and recurring fixes.

## DNS
- Internal zones resolve via the split-horizon resolver.
- TTLs kept low (60s) during migrations, raised back to 1h afterward.

## Backups
- Nightly snapshots, 30-day retention.
- Quarterly restore drill — last run was clean, ~40 min to full restore.

## Recurring fixes
- If the scheduler wedges, drain the queue and restart the leader.
- Cert renewal is automated, but double-check the wildcard each cycle.
