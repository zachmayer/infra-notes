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

Internal draft of the H2 2026 platform roadmap with focus on three core themes: reliability, search quality, and on-device AI capabilities.

### Q3 2026 Initiatives
- **Migrate ranking service to new feature store** (Platform team, target Aug)
  - Critical foundation work enabling downstream Q4 projects
- **Roll out on-device summarization beta** (Apps/AI team, target Sep)
  - 5% beta rollout to test on-device AI capabilities
- **Reduce autocomplete p99 latency by 20%** (Search Infra team)
  - Performance improvement goal for search quality theme

### Q4 2026 Initiatives
- **General availability for summarization** (Apps/AI team)
  - Follow-on from Q3 beta, depends on feature-store migration
- **Multi-region failover for query pipeline** (SRE team)
  - Reliability initiative for improved service robustness
- **Deprecate legacy index shards v3** (Search Infra team)
  - Technical debt reduction, modernization effort

### Key Dependencies & Risks
- **Feature-store migration** is a blocking dependency for summarization GA
- **Staffing constraint**: 2 open SRE positions may impact reliability work
