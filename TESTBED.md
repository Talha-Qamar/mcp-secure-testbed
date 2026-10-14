# Testbed case: `cmd-injection-shell-runner-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | command injection (CWE-78) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/demo_servers/shell-runner` |

Two tools pass input straight to the shell.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-shell-runner-py`
