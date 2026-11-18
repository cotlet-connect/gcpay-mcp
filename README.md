# GCPay MCP server for ChatGPT and Claude

GCPay publishes no public API and no MCP server, checked 16 November 2026. Cotlet runs a hosted GCPay MCP server with 17 tools in your own signed-in GCPay account.

Source: [GCPay integration page](https://cotlet.dev/integrations/gcpay-api-mcp-server?utm_source=github&utm_medium=readme&utm_campaign=gcpay).

## Tools

The live page lists these 17 hosted tools: `list_submittals`, `view_project`, `manage_projects`, `add_tier_vendor`, `manage_schedule_of_values`, `review_schedule_of_values`, `manage_pay_applications`, `review_pay_application`, `release_retainage`, `set_export_status`, `manage_change_orders`, `review_change_order`, `manage_lien_waivers`, `review_lien_waiver`, `add_waiver_template`, `upload_compliance_document`, `verify_compliance_items`. Read tools show projects and submittals. Write tools manage schedules of values, pay applications, change orders, lien waivers, compliance documents and retainage. Approvals, submissions and anything that reaches a subcontractor wait for your OK.

## Example requests

> Show pay applications waiting for my review.

> List missing compliance documents for the Riverside project.

> Prepare this month’s pay application and ask before submitting.

> Review lien waivers that need approval.

> Show change orders awaiting my decision.

> Release retainage at closeout after I confirm.

## Connect

1. Sign in to GCPay at `https://gcpay.com/login.do` in your Cotlet Cloud Browser.
2. Add `https://cotlet.dev/mcp/v1/connect` as the MCP connector URL in ChatGPT or Claude.
3. For scripts and editors, create a Cotlet API key and use `https://cotlet.dev/mcp/v1` with a Bearer token.

## Local wrapper

This repository includes a standard-library Python wrapper with seven generic browser helpers. Set `COTLET_API_KEY` before calling it; `guide` is available without a key.

```bash
export COTLET_API_KEY="your-key"
python3 gcpay_agent.py serve
```

## FAQ

**Does GCPay have a public API or official MCP server?**

The Cotlet.dev integration page reports no public API, developer documentation, API keys, official MCP server or official ChatGPT or Claude connector, checked 16 November 2026.

**What can the GCPay tools do?**

They read projects and submittals and manage schedules of values, pay applications, change orders, lien waivers, compliance documents and retainage.

**Do writes require approval?**

Approvals, submissions and anything that reaches a subcontractor wait for your confirmation.

**Is this official?**

No. Cotlet.dev is independent and is not affiliated with GCPay.
