# H2 2026 Platform Roadmap

## Overview
Internal platform roadmap focusing on three key themes: reliability, search quality, and on-device AI.

## Q3 2026 Goals

- **Migrate ranking service to new feature store** (Owner: Platform)
  - Target: August 2026

- **Roll out on-device summarization beta to 5%** (Owner: Apps/AI)
  - Target: September 2026

- **Cut p99 latency on autocomplete by 20%** (Owner: Search Infra)

## Q4 2026 Goals

- **General availability for summarization** (Owner: Apps/AI)

- **Multi-region failover for query pipeline** (Owner: SRE)

- **Deprecate legacy index shards v3** (Owner: Search Infra)

## Dependencies & Constraints

- Feature-store migration blocks summarization GA
- SRE staffing gap: 2 open requisitions

## Key Themes

1. **Reliability** - Focus on failover capabilities and infrastructure improvements
2. **Search Quality** - Performance improvements and latency optimization
3. **On-Device AI** - Expanding summarization capabilities to users
