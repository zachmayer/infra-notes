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

## H2 2026 Platform Roadmap (Asana task 1215350949678983)

Themes: reliability, search quality, on-device AI.

**Q3**
- Migrate ranking service to new feature store (Platform) — target Aug
- Roll out on-device summarization beta to 5% (Apps/AI) — target Sep
- Cut p99 latency on autocomplete by 20% (Search Infra)

**Q4**
- General availability for on-device summarization (Apps/AI)
- Multi-region failover for query pipeline (SRE)
- Deprecate legacy index shards v3 (Search Infra)

**Dependencies / risks**
- Feature-store migration blocks summarization GA
- SRE staffing gap: 2 open reqs
