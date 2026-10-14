# Testbed case: `cmd-injection-getattr-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | command injection (CWE-78), obfuscated |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/p04_getattr_obfuscation` |

Sink called through getattr (known gap today).

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-getattr-py`
