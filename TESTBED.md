# Testbed case: `backdoor-hardcoded-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | backdoor (hidden hardcoded command) |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/p13_constant_backdoor` |

A tool runs a base64-hidden constant payload (the URL uses the reserved .example TLD and resolves nowhere).

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/backdoor-hardcoded-py`
