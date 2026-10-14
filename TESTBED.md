# Testbed case: `path-traversal-ts`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | path traversal (CWE-22) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/t03_readfile_traversal` |

readFile on a path built from tool input.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/path-traversal-ts`
