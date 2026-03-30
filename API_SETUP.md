# Echo 2.0: API Setup Guide

## OpenAI / Claude API

### Get Your API Key
1. Go to https://platform.openai.com/api-keys
2. Click "Create new secret key"
3. Copy and save (you'll only see it once)

### Test Connection
\`\`\`bash
curl https://api.openai.com/v1/models \
  -H "Authorization: Bearer $OPENAI_API_KEY"
\`\`\`

### Pricing
- GPT-4 Turbo: $0.01/$0.03 per 1k tokens
- GPT-3.5: $0.0005/$0.0015 per 1k tokens
- Average post generation: ~$0.10

## Composio Setup

### Create Account
1. Go to https://app.composio.dev
2. Sign up (free)
3. Go to "Connections"

### Connect Platforms
1. **LinkedIn**
   - Click "Connect"
   - Authenticate with LinkedIn
   - Grant permissions

2. **Twitter/X**
   - Click "Connect"
   - Authenticate with Twitter Dev Account
   - Grant permissions

3. **Email** (if using)
   - Click "Connect"
   - Authenticate with email provider
   - Grant permissions

### Get API Key
1. Go to Settings
2. Copy API Key
3. Add to .env file

## Notion Setup

### Create Integration
1. Go to https://www.notion.so/my-integrations
2. Click "Create new integration"
3. Name: "Echo Bot"
4. Copy Internal Integration Token

### Create Database
1. In Notion, create new database
2. Add columns:
   - Post Content (Text)
   - Platform (Select)
   - Posted Date (Date)
   - Views (Number)
   - Likes (Number)
   - Comments (Number)
   - Shares (Number)
   - Status (Select)

3. Right-click → "Add connections"
4. Select "Echo Bot" integration

### Get Database ID
1. Open database in Notion
2. Copy URL: notion.so/workspace/ID
3. Extract ID (32 characters)
4. Add to .env as NOTION_DATABASE_ID

## Environment File (.env)

Create file with:
\`\`\`
OPENAI_API_KEY=sk-your-key-here
COMPOSIO_API_KEY=your-composio-key
NOTION_API_KEY=your-notion-api-key
NOTION_DATABASE_ID=your-32-char-id
\`\`\`

## Testing

### Test All Connections
\`\`\`python
import os
from dotenv import load_dotenv

load_dotenv()

print("OPENAI:", "✓" if os.getenv("OPENAI_API_KEY") else "✗")
print("COMPOSIO:", "✓" if os.getenv("COMPOSIO_API_KEY") else "✗")
print("NOTION:", "✓" if os.getenv("NOTION_API_KEY") else "✗")
print("NOTION_DB:", "✓" if os.getenv("NOTION_DATABASE_ID") else "✗")
\`\`\`

## Troubleshooting

### OpenAI Key Rejected
- Ensure key starts with "sk-"
- Check for extra spaces
- Verify account has credits
- Test at platform.openai.com

### Composio Connection Failed
- Verify platform (LinkedIn/Twitter) accounts are active
- Re-authenticate if tokens expired
- Check platform-specific OAuth scopes

### Notion Database Not Found
- Verify database ID (32 hex characters)
- Confirm integration is shared with database
- Check database is not archived

## Support
Refer to platform-specific documentation or open GitHub issue.
