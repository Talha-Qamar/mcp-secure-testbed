# Testbed case: `cmd-injection-os-system-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | command injection (CWE-78) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/p01_os_system_concat` |

os.system with string concatenation.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-os-system-py`
