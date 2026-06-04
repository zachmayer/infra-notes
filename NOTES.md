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

## H2 2026 Platform Roadmap Summary

**Status:** Draft

**Q3 2026 Initiatives:**
- Migrate ranking service to new feature store (Platform team, August 2026)
- Roll out on-device summarization beta (Apps/AI team, September 2026) - Beta to 5% of users
- Cut p99 latency on autocomplete by 20% (Search Infrastructure team, Q3 2026)

**Q4 2026 Initiatives:**
- General availability for summarization (Apps/AI team)
- Multi-region failover for query pipeline (SRE team)
- Deprecate legacy index shards v3 (Search Infrastructure team)

**Key Dependencies:**
- Ranking service migration must complete before summarization GA
- SRE team has 2 open requisitions impacting multi-region failover capacity
