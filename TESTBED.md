# Testbed case: `hidden-skipped-dir-py`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | hiding: runtime code under examples/ |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/s04_code_in_skipped_dir` |

The tool imports its implementation from a directory scanners usually skip.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/hidden-skipped-dir-py`
