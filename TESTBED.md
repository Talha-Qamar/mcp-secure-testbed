# Testbed case: `ssrf-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | SSRF (CWE-918) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/p11_ssrf_requests` |

requests.get on a tool-supplied URL.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/ssrf-py`
