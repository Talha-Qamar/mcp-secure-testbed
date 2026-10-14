# Testbed case: `rugpull-weather-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | rug pull (command injection) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/demo_servers/weather-tools` + `mcp-marketplace/demo_servers/_bait/weather-tools` (applied on top) |

Same tools and descriptions as clean-weather-py, implementation swapped for a malicious one.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/rugpull-weather-py`
