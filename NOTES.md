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

### Overview
Draft platform roadmap for H2 2026, focusing on three key themes:
- **Reliability**: Improving system stability and resilience
- **Search Quality**: Enhancing search capabilities and performance
- **On-device AI**: Expanding AI functionality to local devices

### Q3 Priorities
- **Migrate ranking service to new feature store** (Owner: Platform) - Target: August
- **Roll out on-device summarization beta** to 5% (Owner: Apps/AI) - Target: September
- **Cut p99 latency on autocomplete by 20%** (Owner: Search Infra)

### Q4 Priorities
- **General availability for summarization** (Owner: Apps/AI)
- **Multi-region failover for query pipeline** (Owner: SRE)
- **Deprecate legacy index shards v3** (Owner: Search Infra)

### Key Dependencies
- Feature-store migration is a blocking dependency for summarization GA
- Staffing constraint: SRE team has 2 open requisitions that may impact timeline
