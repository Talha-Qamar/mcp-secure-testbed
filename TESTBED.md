# Testbed case: `cmd-injection-exec-ts`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | command injection (CWE-78) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/t01_exec_template` |

TypeScript exec with a template string.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-exec-ts`
