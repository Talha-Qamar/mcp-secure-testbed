# MCP Secure testbed

> **Intentionally vulnerable and malicious-looking MCP servers for testing the MCP Secure scanner.
> Do not install, run or connect any of these servers to an agent.**

Every branch is one test case, with the server at the branch root, so the marketplace can scan it live
through normal git ingestion:

```
https://github.com/Talha-Qamar/mcp-secure-testbed/tree/<branch>
```

The code comes from the fixtures in the `mcp-marketplace` repository (`demo_servers/` and
`eval/adversarial/`); `TESTBED.md` on each branch names the source. Payload URLs use the reserved
`.example` TLD and resolve nowhere.

## Cases

| Branch | Threat | Correct verdict |
|---|---|---|
| [`clean-weather-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/clean-weather-py) | clean | PASS |
| [`rugpull-weather-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/rugpull-weather-py) | rug pull (command injection) | FAIL |
| [`safe-sql-ts`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/safe-sql-ts) | preference manipulation (description) | REVIEW |
| [`rugpull-sql-ts`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/rugpull-sql-ts) | rug pull (SQL injection) | FAIL |
| [`cmd-injection-shell-runner-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-shell-runner-py) | command injection (CWE-78) | FAIL |
| [`cmd-injection-os-system-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-os-system-py) | command injection (CWE-78) | FAIL |
| [`cmd-injection-fstring-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-fstring-py) | command injection (CWE-78) | FAIL |
| [`cmd-injection-aliased-import-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-aliased-import-py) | command injection (CWE-78) | FAIL |
| [`cmd-injection-helper-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-helper-py) | command injection (CWE-78) | FAIL |
| [`cmd-injection-getattr-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-getattr-py) | command injection (CWE-78), obfuscated | FAIL |
| [`cmd-injection-exec-ts`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/cmd-injection-exec-ts) | command injection (CWE-78) | FAIL |
| [`code-injection-eval-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/code-injection-eval-py) | code injection (CWE-94) | FAIL |
| [`deserialization-pickle-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/deserialization-pickle-py) | unsafe deserialization (CWE-502) | FAIL |
| [`path-traversal-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/path-traversal-py) | path traversal (CWE-22) | FAIL |
| [`path-traversal-ts`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/path-traversal-ts) | path traversal (CWE-22) | FAIL |
| [`ssrf-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/ssrf-py) | SSRF (CWE-918) | FAIL |
| [`sqli-fstring-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/sqli-fstring-py) | SQL injection (CWE-89) | FAIL |
| [`backdoor-hardcoded-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/backdoor-hardcoded-py) | backdoor (hidden hardcoded command) | FAIL |
| [`hidden-dist-entrypoint-ts`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/hidden-dist-entrypoint-ts) | hiding: committed dist/ differs from src/ | FAIL |
| [`hidden-skipped-dir-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/hidden-skipped-dir-py) | hiding: runtime code under examples/ | FAIL |
| [`runtime-description-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/runtime-description-py) | coverage: description built at runtime | REVIEW |
| [`tool-poisoning-param-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/tool-poisoning-param-py) | tool poisoning (parameter description) | FAIL |
| [`tool-poisoning-zero-width-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/tool-poisoning-zero-width-py) | tool poisoning (zero-width characters) | FAIL |
| [`tool-poisoning-classic-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/tool-poisoning-classic-py) | tool poisoning (<IMPORTANT> block) | FAIL |
| [`tool-shadowing-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/tool-shadowing-py) | tool shadowing | FAIL |
| [`benign-subprocess-argv-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/benign-subprocess-argv-py) | clean | PASS |
| [`benign-shlex-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/benign-shlex-py) | clean | PASS |
| [`benign-utility-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/benign-utility-py) | clean | PASS |
| [`benign-execfile-ts`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/benign-execfile-ts) | clean | PASS |
| [`benign-ts`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/benign-ts) | clean | PASS |
| [`benign-security-words-py`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/benign-security-words-py) | clean | PASS |
| [`unsupported-go`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/unsupported-go) | coverage: unsupported language | REVIEW |
| [`watcher-demo`](https://github.com/Talha-Qamar/mcp-secure-testbed/tree/watcher-demo) | live rug pull | PASS, then FAIL after the bait commit |

## Live rug-pull demo (`watcher-demo`)

`watcher-demo` starts as the clean weather server. Publish it in the marketplace (it is approved),
then push the bait commit and press **Poll now** on the watcher page: the watcher sees the new commit,
the code fingerprint changes, the new version is re-scanned and the listing is suspended.

```bash
node scripts/testbed.js rugpull   # in mcp-marketplace: push the malicious update
node scripts/testbed.js reset     # restore the clean version
```

## Real vulnerable MCP servers (published advisories)

Real releases with a known vulnerability, pinned to the vulnerable tag; the next tag is the fix.

| Repository | Vulnerable tag | Fixed tag | Threat |
|---|---|---|---|
| [BurtTheCoder/mcp-maigret](https://github.com/BurtTheCoder/mcp-maigret/tree/v1.0.12) | v1.0.12 | v1.0.13 | command injection |
| [cyanheads/git-mcp-server](https://github.com/cyanheads/git-mcp-server/tree/v2.1.4) | v2.1.4 | v2.1.5 | command injection |
| [jamubc/gemini-mcp-tool](https://github.com/jamubc/gemini-mcp-tool/tree/v1.1.5) | v1.1.5 | v1.1.6 | command injection |
| [translated/lara-mcp](https://github.com/translated/lara-mcp/tree/v0.0.11) | v0.0.11 | v0.0.12 | command injection |
| [ooples/token-optimizer-mcp](https://github.com/ooples/token-optimizer-mcp/tree/v5.0.1) | v5.0.1 | v5.1.0 | command injection, path traversal |
| [mobile-next/mobile-mcp](https://github.com/mobile-next/mobile-mcp/tree/0.0.48) | 0.0.48 | 0.0.49 | path traversal |
| [haris-musa/excel-mcp-server](https://github.com/haris-musa/excel-mcp-server/tree/v0.1.7) | v0.1.7 | v0.1.8 | path traversal |
| [Wolfe-Jam/claude-faf-mcp](https://github.com/Wolfe-Jam/claude-faf-mcp/tree/v5.7.1) | v5.7.1 | v5.7.2 | path traversal |
| [pipeboard-co/meta-ads-mcp](https://github.com/pipeboard-co/meta-ads-mcp/tree/1.0.113) | 1.0.113 | 1.0.115 | SSRF |
| [apache/doris-mcp-server](https://github.com/apache/doris-mcp-server/tree/0.6.0) | 0.6.0 | 0.6.1 | SQL injection |
