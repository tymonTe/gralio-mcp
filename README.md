# Gralio SaaS Database MCP

## 🚀 Overview

Access **3+ million SaaS reviews**, detailed pricing data, alternatives, ratings, funding information, growth metrics, user sentiment analysis, and functional feature data for over 30,000 software products.

Turn your LLM into the ultimate software research assistant—free from polluted web searches and marketing noise. All accessible via our free Gralio MCP endpoint.

## 📊 Data Highlights

Our comprehensive database includes:

- **3M+ SaaS Reviews** - In-depth user feedback and sentiment analysis
- **Detailed Pricing Data** - Comprehensive pricing tiers and feature breakdowns
- **Competitor Alternatives** - Identify and compare alternative solutions
- **Company Funding & Growth** - Track investment rounds and growth trajectories
- **User Sentiment Scores** - Aggregated sentiment from across the web
- **Functional Feature Info** - Granular details on product capabilities

## 🔍 Example Use Cases

### Finding Cheaper or Easier Alternatives
Discover cost-effective alternatives to popular SaaS tools without compromising on features.

### Discovering Tools by Use Case
Find the perfect tools based on specific feature requirements or use cases.

### Scouting Trending Competitors
Identify high-growth competitors in your market space before they become major threats.

### Quick Reviews Vibe Check
Get an overview of what users are saying about products across the web.

## ⚙️ Integration Instructions

### Cursor Integration

To connect Gralio MCP to your Cursor editor, add the following configuration in either:

- **Project Configuration**: Create `.cursor/mcp.json` in your project directory
- **Global Configuration**: Create `~/.cursor/mcp.json` in your home directory

```json
{
    "mcpServers": {
        "gralio": {
            "url": "https://market.gralio.ai/mcp/sse"
        }
    }
}
```

### Windsurf & Cascade Integration

1. Navigate to Windsurf settings (Settings > Advanced Settings)
2. Scroll down to the Cascade section
3. Add a new MCP server with the following configuration:

```json
{
    "mcpServers": {
        "gralio": {
            "url": "https://market.gralio.ai/mcp/sse"
        }
    }
}
```

### VS Code Integration

Create or modify `.vscode/mcp.json` in your project's root directory:

```json
{
    "servers": {
        "GralioSaaS": {
            "type": "sse",
            "url": "https://market.gralio.ai/mcp/sse"
        }
    }
}
```

### Claude Desktop Integration

Claude Desktop supports remote HTTP/SSE MCP servers via supergateway:

1. **Test Supergateway**:
   ```bash
   npx -y supergateway --sse "https://market.gralio.ai/mcp/sse"
   ```

2. **Configure Claude Desktop**:
   Add to your Claude MCP configuration file:

   ```json
   {
       "mcpServers": {
           "gralio_remote": {
               "command": "npx",
               "args": [
                   "-y",
                   "supergateway",
                   "--sse",
                   "https://market.gralio.ai/mcp/sse"
               ]
           }
       }
   }
   ```

3. **Restart Claude Desktop** for changes to take effect.

## 📧 Contact

For more details on the data and how to use it, please refer to our [Gralio MCP Page](https://market.gralio.ai/mcp).
