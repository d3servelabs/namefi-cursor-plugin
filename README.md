# Namefi: Instant Search

Name your startup, side project, or brand with Cursor and find out which
domain names are available. Cursor brainstorms ideas; Namefi checks the
domains so you can focus on names you can register.

## Great for

- Brainstorming startup and business names with available domains.
- Naming an app, podcast, newsletter, online shop, or personal website.
- Finding alternatives when your first choice is taken.
- Seeing where a website points and checking public email DNS records.

## Try asking

- "Suggest 10 names for my coffee subscription startup and check which .com domains are available."
- "Is mybakery.com taken? If yes, find five similar names that are available."
- "I'm starting a hiking podcast. Brainstorm names that have an available domain."
- "Check the MX, SPF, and DMARC records for namefi.io."
- "Does namefi.io have an A record? Show the IPv4 address and TTL."

## Included tools

| Tool | What it does |
| --- | --- |
| `searchAvailability` | Checks up to 20 domain names per call. Returns availability flags, without prices. |
| `dnsOverHttp` | Reads public DNS records such as A, AAAA, CNAME, MX, TXT, NS, and CAA. |

Both tools are read-only. They cannot buy, transfer, or change domains, charge a
payment method, or edit DNS. Availability can change before registration, and DNS
records alone do not prove that a website or email delivery works.

Ready to register a domain? Visit [namefi.io](https://namefi.io).

## Connection and privacy

The bundled MCP server uses `https://api.namefi.io/mcp-instant` over Streamable
HTTP. No account, sign-in, API key, or OAuth setup is needed. Domain names and
hostnames supplied to the tools are sent to Namefi; DNS queries use public
resolvers. The plugin includes no skills or local executable scripts.

## Support

- [Namefi support](https://namefi.io/agent-plugin-support)
- [Privacy policy](https://namefi.io/privacy)
- [Terms of service](https://namefi.io/tos)
- [Source code](https://github.com/d3servelabs/namefi-cursor-plugin)

Published by Namefi by D3Serve Labs Inc. Licensed under MIT.

## Test locally in Cursor

Copy `.cursor-plugin/`, `mcp.json`, and `assets/` from this repository into
`~/.cursor/plugins/local/namefi-instant/`. Restart Cursor or run **Developer:
Reload Window**, then open **Customize** and confirm the Namefi MCP server is
available. Local plugin imports must be allowed by your organization.

Try the prompts above and verify both domain availability and DNS lookup work
without signing in. Avoid installing multiple copies with the same plugin name.

## Package layout

```text
.cursor-plugin/plugin.json
mcp.json
assets/namefi-icon.png
README.md
LICENSE
```

The internal plugin identifier is `namefi-instant`. Cursor discovers the root
`mcp.json` automatically. No credentials, variables, skills, rules, agents, or
hooks are bundled.

## Marketplace submission

This repository follows the [Cursor plugin reference](https://cursor.com/docs/reference/plugins).
After testing locally, submit the public repository URL at
[Cursor Marketplace publishing](https://cursor.com/marketplace/publish).
Creating this repository does not publish a Marketplace listing.
