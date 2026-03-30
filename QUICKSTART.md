# Echo 2.0: 5-Minute Quick Start

## Prerequisites
- GitHub account
- OpenAI or Claude API key
- Composio account (free)
- Notion workspace

## Step 1: Clone Repository
\`\`\`bash
git clone https://github.com/yourusername/echo-govcon-automation
cd echo-govcon-automation
\`\`\`

## Step 2: API Setup (2 minutes)
1. Get OpenAI key from https://platform.openai.com/api-keys
2. Get Composio token from https://app.composio.dev
3. Get Notion integration token from https://www.notion.so/my-integrations

## Step 3: Environment Setup
\`\`\`bash
export OPENAI_API_KEY="sk-xxx"
export COMPOSIO_API_KEY="xxx"
export NOTION_API_KEY="xxx"
\`\`\`

## Step 4: Load Prompts
\`\`\`bash
# All 26 prompts are in PROMPT_LIBRARY.json
# Import them to your AI platform of choice
cat PROMPT_LIBRARY.json
\`\`\`

## Step 5: Create First Post
1. Pick a prompt from `content_creation_prompts.json`
2. Feed it your company details
3. Generate post via OpenAI/Claude
4. Copy to LinkedIn/Twitter

## Step 6: Track Performance
Add post metrics to Notion using template in `monthly_report_template.json`

## Next Steps
- Full setup: [GETTING_STARTED.md](GETTING_STARTED.md)
- Advanced: [ARCHITECTURE.md](ARCHITECTURE.md)
- Deploy to GitHub: [GITHUB_SETUP.md](GITHUB_SETUP.md)

**You're now ready to generate Echo content!** 🚀
