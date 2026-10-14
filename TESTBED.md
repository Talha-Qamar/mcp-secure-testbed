# Testbed case: `hidden-dist-entrypoint-ts`

**Intentionally vulnerable test fixture for MCP Secure. Do not install or run this server.**

| | |
|---|---|
| Threat | hiding: committed dist/ differs from src/ |
| Correct verdict | **FAIL** |
| Source | `mcp-marketplace/eval/adversarial/s06_committed_dist_entrypoint` |

package.json runs dist/index.js, which is not the reviewed src/.

Scan it: `https://github.com/Talha-Qamar/mcp-secure-testbed/tree/hidden-dist-entrypoint-ts`
