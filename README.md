# Rightmove Property Scraper — New Listings & Price-Drop Alerts — MCP Server

Watch any Rightmove property search from your AI agent or MCP client and get only what changed — new listings and price drops since your last run, as clean structured records: address, price, previous price, bedrooms, property type, agent name and listing URL. A one-shot fetch of the search's current listings is also available when an agent just needs the properties on the market now.

This repo is the MCP listing for the [Rightmove Property Scraper — New Listings & Price-Drop Alerts](https://apify.com/magnova/rightmove-listings-monitor) Actor by Magnova on Apify. The server is hosted by Apify at the pinned endpoint below — there is nothing to install or run from this repository; you just point your MCP client at the URL.

## Tools

The pinned connection loads a focused tool set:

- **magnova--rightmove-listings-monitor** — Watch a Rightmove property search for new listings and price changes, or fetch the search's current listings in one shot. Returns structured records: address, price, previous price, bedrooms, property type, agent name, listing URL.
- **fetch-actor-details** — Fetch the Actor's full input schema, pricing, and documentation, so an agent can check parameters and cost before running it.
- **get-actor-run / get-dataset-items** — Run and storage helpers, loaded automatically, used to fetch the results a run produced.

## Connect

Pinned endpoint (Streamable HTTP):

```
https://mcp.apify.com?tools=fetch-actor-details,magnova/rightmove-listings-monitor
```

On first connect, your client will ask you to sign in with your Apify account (OAuth). If your client cannot do OAuth, pass your Apify API token as an `Authorization: Bearer <YOUR_APIFY_TOKEN>` header instead.

### Cursor / VS Code / other Streamable HTTP clients

```json
{
  "mcpServers": {
    "rightmove-listings-monitor": {
      "url": "https://mcp.apify.com?tools=fetch-actor-details,magnova/rightmove-listings-monitor"
    }
  }
}
```

### Claude Desktop

Claude Desktop's config file only runs local commands, so use the `mcp-remote` bridge:

```json
{
  "mcpServers": {
    "rightmove-listings-monitor": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com?tools=fetch-actor-details,magnova/rightmove-listings-monitor"
      ]
    }
  }
}
```

The same pinned URL also lives in this repo's `.mcp.json`, and `server.json` is the listing for the Official MCP Registry, published as `io.github.memeanalyst/rightmove-listings-monitor-mcp`.

## Pricing

Pay per event, billed to your own Apify account: **$0.01 per listing returned — $10 per 1,000 listings**. No start fee, no subscription, and you are only charged for records actually delivered.

## Links

- Actor on Apify Store: https://apify.com/magnova/rightmove-listings-monitor
- MCP endpoint: https://mcp.apify.com?tools=fetch-actor-details,magnova/rightmove-listings-monitor

*Listing records come from Rightmove's public search pages.*
