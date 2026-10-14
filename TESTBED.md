# Testbed case: `cmd-injection-fstring-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | command injection (CWE-78) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/p02_fstring_shell_true` |

subprocess with an f-string and shell=True.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-fstring-py`
