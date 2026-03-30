# Echo 2.0: Complete Setup Guide

## System Requirements
- Python 3.8+
- OpenAI/Claude account
- Composio account
- Notion workspace with edit access

## Installation

### 1. Clone Repository
\`\`\`bash
git clone https://github.com/yourusername/echo-govcon-automation
cd echo-govcon-automation
\`\`\`

### 2. Install Dependencies
\`\`\`bash
pip install -r requirements.txt
\`\`\`

## Configuration

### API Keys
Create `.env` file (DO NOT COMMIT):
\`\`\`
OPENAI_API_KEY=sk-your-key-here
COMPOSIO_API_KEY=your-composio-key
NOTION_API_KEY=your-notion-api-key
NOTION_DATABASE_ID=your-database-id
\`\`\`

### Notion Database Setup
1. Create database with columns:
   - Post Content (Text)
   - Platform (Select: LinkedIn / Twitter)
   - Posted Date (Date)
   - Views (Number)
   - Likes (Number)
   - Comments (Number)
   - Shares (Number)
   - Status (Select: Draft / Published / Analyzed)

2. Share database with your integration

## Usage

### Generate Content
\`\`\`python
from echo.content_generator import generate_post

prompt = "Create a post about SDVOSB advantages"
post = generate_post(prompt)
print(post)
\`\`\`

### Track Performance
\`\`\`python
from echo.performance_tracker import log_performance

performance = {
    'post_id': 'post_123',
    'views': 1250,
    'likes': 45,
    'comments': 8,
    'shares': 3
}
log_performance(performance)
\`\`\`

### Monthly Analysis
\`\`\`python
from echo.analyzer import generate_monthly_report

report = generate_monthly_report()
print(report)
\`\`\`

## Folder Structure
\`\`\`
echo-govcon-automation/
├── prompts/
│   ├── PROMPT_LIBRARY.json
│   ├── content_creation_prompts.json
│   ├── analysis_prompts.json
│   ├── strategy_prompts.json
│   ├── idea_generation_prompts.json
│   └── optimization_prompts.json
├── examples/
│   ├── example_post.json
│   └── monthly_report_template.json
├── src/
│   ├── content_generator.py
│   ├── performance_tracker.py
│   └── analyzer.py
├── docs/
│   ├── README.md
│   ├── QUICKSTART.md
│   ├── ARCHITECTURE.md
│   ├── API_SETUP.md
│   └── GITHUB_SETUP.md
└── requirements.txt
\`\`\`

## Troubleshooting

### API Key Issues
- Check `.env` file exists and is NOT committed
- Verify keys are valid at their respective platforms
- Don't share keys publicly

### Notion Connection Failed
- Verify integration is shared with database
- Check NOTION_DATABASE_ID is correct
- Ensure database has required columns

### Posts Not Publishing
- Check API credentials
- Verify platform accounts are connected
- Review error logs in console

## Support
See documentation or open GitHub issue.
