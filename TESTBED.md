# Testbed case: `cmd-injection-helper-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | command injection (CWE-78) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/p06_helper_indirection` |

Tool input reaches the shell through a helper function.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-helper-py`
