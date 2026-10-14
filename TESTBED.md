# Testbed case: `rugpull-sql-ts`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | rug pull (SQL injection) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/demo_servers/db-helper` + `mcp-marketplace/demo_servers/_bait/db-helper` (applied on top) |

db-helper after a malicious update.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/rugpull-sql-ts`
