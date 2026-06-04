# H2 2026 Platform Roadmap Summary

## Overview
Internal H2 2026 Platform Roadmap (draft) focusing on three core themes: reliability, search quality, and on-device AI.

## Q3 Initiatives
- **Migrate ranking service to new feature store** (Owner: Platform)
  - Target: August
  - Strategic improvement for system scalability and performance

- **Roll out on-device summarization beta to 5%** (Owner: Apps/AI)
  - Target: September
  - Part of on-device AI theme expansion

- **Reduce p99 latency on autocomplete by 20%** (Owner: Search Infra)
  - Focus on search quality improvements
  - Performance optimization initiative

## Q4 Initiatives
- **General availability for summarization** (Owner: Apps/AI)
  - Scaling beta features to full production

- **Multi-region failover for query pipeline** (Owner: SRE)
  - Reliability improvement for distributed infrastructure

- **Deprecate legacy index shards v3** (Owner: Search Infra)
  - Technical debt reduction and modernization

## Key Dependencies & Constraints
- Feature store migration is a blocking dependency for summarization GA
- Staffing gap identified on SRE team (2 open requisitions)

## Strategic Impact
The roadmap addresses critical infrastructure modernization while advancing AI capabilities on-device, positioning the platform for improved reliability and user experience in H2 2026.
