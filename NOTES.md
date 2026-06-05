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

## H2 2026 Platform Roadmap

Strategic themes: reliability, search quality, on-device AI.

**Q3 Initiatives:**
- Migrate ranking service to new feature store (Platform team, target Aug)
- Roll out on-device summarization beta to 5% (Apps/AI team, target Sep)
- Cut p99 latency on autocomplete by 20% (Search Infra team)

**Q4 Initiatives:**
- General availability for summarization (Apps/AI team)
- Multi-region failover for query pipeline (SRE team)
- Deprecate legacy index shards v3 (Search Infra team)

**Critical Dependencies:**
- Feature-store migration blocks summarization GA
- SRE team has 2 open staffing requisitions
