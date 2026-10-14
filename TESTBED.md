# Testbed case: `deserialization-pickle-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | unsafe deserialization (CWE-502) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/p09_pickle_loads` |

pickle.loads on tool input.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/deserialization-pickle-py`
