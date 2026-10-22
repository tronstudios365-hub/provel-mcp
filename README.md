# Provel MCP

Work with [Provel](https://www.provel.co), a senior design and engineering studio for AI and Web3, straight from your AI assistant. Run website and security audits, get free quotes, set up an NDA, share files and message the team without leaving Claude, Cursor, VS Code or Codex.

This repository is the public listing for the hosted Provel MCP server. The server runs on Provel's infrastructure, so there is nothing to install or run locally.

- **Server URL:** `https://www.provel.co/api/mcp`
- **Transport:** Streamable HTTP
- **Sign-in:** OAuth 2.0 (a Provel page opens the first time you connect)
- **Docs and setup:** [provel.co/mcp](https://www.provel.co/mcp)
- **Official MCP Registry:** `co.provel/provel`

## What you can do

- **0x website audits.** 43 checks per page across 11 areas: speed, SEO, accessibility, mobile, security, vulnerabilities, links, trust, interactivity, AI readiness, and domain and email. Includes PHP2Shell (CVE-2026-109618 / CVE-2026-109619) exposure and outdated WordPress, jQuery, Bootstrap or AngularJS. Every audit includes an AI design review.
  - **0x Quick:** free, homepage, 2 a day.
  - **0x Deep:** $99, up to 20 pages, a design review of every page, 4 extra security checks (exposed files, SSL certificate, security.txt and script integrity) and ready-to-paste fixes. Paid on a Provel payment page before it starts.
- **Free quotes** for design and engineering work, from a design critique to a full product build.
- **Expert audits** by Provel's senior team.
- **NDAs** before you share anything confidential.
- **Files and messages**, so you can share designs, code or briefs and follow up with the team.

## Connect

### Claude (claude.ai, desktop and mobile)

Settings → Connectors → Add custom connector, then paste:

```
https://www.provel.co/api/mcp
```

### Claude Code

```bash
claude mcp add --transport http --scope user provel https://www.provel.co/api/mcp
```

Then type `/mcp` in Claude Code and sign in to Provel.

### Cursor

Add to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "provel": { "url": "https://www.provel.co/api/mcp" }
  }
}
```

### VS Code

Add to `.vscode/mcp.json`:

```json
{
  "servers": {
    "provel": { "type": "http", "url": "https://www.provel.co/api/mcp" }
  }
}
```

### Codex

```bash
codex mcp add provel --url https://www.provel.co/api/mcp
codex mcp login provel
```

## Tools

| Tool | What it does |
| :- | :- |
| `get_service` | Provel's services, workflow and prices. Start here. |
| `get_account` | New replies from Provel, open requests, recent audits and balance. |
| `run_audit` | Run a 0x Quick (free) or 0x Deep ($99) website audit. |
| `get_audit` | Audit results, the report link and a fix guide with code for each issue. |
| `quote_request` | Get a free price for a brief. |
| `ask_for_quote` | Send a brief to Provel for a confirmed quote. Free, nothing charged. |
| `get_payment_link` | A payment page for an agreed price. Moves no money by itself. |
| `confirm_payment` | Check whether a payment has arrived. |
| `request_nda` / `get_nda` | Set up an NDA with Provel and check its status. |
| `share_with_provel` | Share a design, code or brief with the team. |
| `get_upload_link` | A link to upload files for Provel. |
| `send_message` | Message the Provel team. |
| `get_request` / `list_requests` / `cancel_request` | Follow and manage your requests. |
| `get_delivery` / `approve_delivery` / `request_changes` | Review delivered work. |
| `submit_request` | Send a brief paid from your Provel credits, after you say yes to the exact quote. Not in the Claude directory version. |

Every tool carries `readOnlyHint` or `destructiveHint` annotations.

## Payments and safety

- Quotes are always free. The Claude directory version never spends your balance: briefs go to Provel as free quote requests, and you pay only if you go ahead, on Provel's own payment page.
- Audits are passive. They read what a site already shows every visitor and request a few standard public paths. They never send attack traffic, and exposed files are only noted, never stored.
- Text from audited websites is treated as data, never as instructions.

## Privacy and support

- **Privacy policy:** [provel.co/privacy](https://www.provel.co/privacy)
- **Terms:** [provel.co/mcp-terms](https://www.provel.co/mcp-terms)
- **Support:** [hello@provel.co](mailto:hello@provel.co)
- **Security:** [provel.co/.well-known/security.txt](https://www.provel.co/.well-known/security.txt)

## License

The contents of this repository are MIT licensed. The Provel service itself is governed by the [Provel MCP terms](https://www.provel.co/mcp-terms).
