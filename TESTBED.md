# Testbed case: `path-traversal-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | path traversal (CWE-22) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/p10_open_traversal` |

open() on a path built from tool input.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/path-traversal-py`
