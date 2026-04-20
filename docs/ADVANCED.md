# Advanced: OAuth discovery & verification

This page is for **integrators and curious power users**. Normal Claude setup only requires pasting:

`https://www.sellonllm.com/api/mcp`

## Unauthenticated MCP request

Calling the MCP endpoint without a Bearer token should return **401** with a `WWW-Authenticate` header pointing at protected-resource metadata:

```bash
curl -i https://www.sellonllm.com/api/mcp
```

Expect something like:

- `HTTP/2 401`
- `www-authenticate: Bearer realm="MCP", resource_metadata="https://www.sellonllm.com/.well-known/oauth-protected-resource"`

## Discovery endpoints

| URL | Purpose |
|-----|---------|
| `https://www.sellonllm.com/.well-known/oauth-protected-resource` | RFC 9728 — MCP as OAuth protected resource |
| `https://www.sellonllm.com/.well-known/oauth-authorization-server` | RFC 8414 — authorization server metadata |

Quick check:

```bash
curl -s https://www.sellonllm.com/.well-known/oauth-protected-resource | head
curl -s https://www.sellonllm.com/.well-known/oauth-authorization-server | head
```

## Dynamic client registration

Custom MCP clients may use **Dynamic Client Registration** (RFC 7591) against SellOnLLM’s registration endpoint as documented in the live metadata responses above.

## Notes

- Production traffic should use **`https://www.sellonllm.com`** (www) so issuers and discovery URLs stay consistent.
- **Claude.ai** performs OAuth and token exchange on your behalf after you add the custom connector; you typically never handle raw tokens manually.
