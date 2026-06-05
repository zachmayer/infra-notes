# Service Configuration Reference

## service-config

Service config

### Routing Configuration Notes

Defaults applied across the request-routing tier. Change via PR; updates roll
out on the next config sync (top of the hour).

#### Timeouts
- Upstream connect: 250ms
- Upstream read: 2s
- Client idle keepalive: 75s

#### Rate limits
- Per-token: 600 req/min, burst 50
- Per-IP fallback: 120 req/min

#### Owners
- Routing tier: Dana Whitfield
- Config sync job: Marcus Olawale

#### Open items
- Revisit keepalive after the connection-pool change lands.
- Confirm burst settings hold under the Tuesday traffic peak.
