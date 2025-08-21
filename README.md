# Hive MCP NFT Analytics

## Overview
Model Context Protocol (MCP) server for Non-Fungible Token (NFT) analytics and marketplace data. This MCP provides comprehensive tools for analyzing NFT collections, marketplace activity, and digital collectible trends across multiple blockchain networks.

## Connection Details
- **Transport**: HTTP (Remote only)
- **URL**: `https://mcp.hiveintelligence.xyz/hive_nft_analytics/mcp`
- **Protocol**: Model Context Protocol (MCP)

## Features
- NFT collection statistics and rankings
- Floor price tracking and analysis
- Sales volume and transaction monitoring
- Rarity score calculations
- Holder distribution analysis
- Marketplace aggregation
- Whale wallet tracking
- Mint monitoring and alerts
- Collection trending analysis
- NFT valuation models
- Wash trading detection
- Blue chip index tracking

## Usage

### Claude Desktop Configuration
Add to your Claude Desktop configuration file:

```json
{
  "mcpServers": {
    "hive-nft-analytics": {
      "url": "https://mcp.hiveintelligence.xyz/hive_nft_analytics/mcp",
      "transport": "http"
    }
  }
}
```

### MCP Client Integration
```javascript
import { Client } from '@modelcontextprotocol/sdk';

const client = new Client({
  name: 'nft-analytics-client',
  version: '1.0.0'
});

await client.connect({
  url: 'https://mcp.hiveintelligence.xyz/hive_nft_analytics/mcp',
  transport: 'http'
});
```

## Available Tools

### `get_collection_stats`
Retrieve comprehensive collection statistics
```json
{
  "tool": "get_collection_stats",
  "params": {
    "collection": "0x...",
    "metrics": ["floor_price", "volume", "holders", "listed"]
  }
}
```

### `track_floor_price`
Monitor floor price movements
```json
{
  "tool": "track_floor_price",
  "params": {
    "collections": ["bayc", "cryptopunks", "azuki"],
    "timeframe": "7d",
    "alert_threshold": 10
  }
}
```

### `analyze_sales`
Analyze NFT sales data
```json
{
  "tool": "analyze_sales",
  "params": {
    "collection": "0x...",
    "period": "24h",
    "min_price": 1
  }
}
```

### `calculate_rarity`
Calculate NFT rarity scores
```json
{
  "tool": "calculate_rarity",
  "params": {
    "collection": "0x...",
    "token_id": "1234",
    "include_traits": true
  }
}
```

### `detect_wash_trading`
Identify potential wash trading activity
```json
{
  "tool": "detect_wash_trading",
  "params": {
    "collection": "0x...",
    "timeframe": "30d",
    "sensitivity": "medium"
  }
}
```

## Keywords
NFT, non-fungible token, digital collectibles, NFT analytics, floor price, rarity, marketplace, OpenSea, collection stats, sales volume, holder analysis, whale tracking, mint monitoring, trending collections, NFT valuation, wash trading, blue chip NFTs, metadata, traits, rarity score, NFT liquidity, MCP, Model Context Protocol, Web3, blockchain, HTTP MCP server, remote MCP, Hive Intelligence, ERC721, ERC1155, digital art, PFP, generative art, metaverse

## License
MIT

## Support
For issues and feature requests, please open an issue on GitHub.

## About Hive Intelligence
Part of the Hive Intelligence suite of blockchain analytics MCP servers.