# Contributing to Echo

Welcome! We love contributions from the community.

## How to Contribute

### 1. Fork & Clone
\`\`\`bash
git clone https://github.com/yourusername/echo-govcon-automation
cd echo-govcon-automation
git checkout -b feature/your-feature-name
\`\`\`

### 2. Make Changes
- Add new prompts to PROMPT_LIBRARY.json
- Update documentation
- Fix bugs
- Improve performance

### 3. Test
\`\`\`bash
# Validate JSON
python -m json.tool PROMPT_LIBRARY.json

# Test documentation links
\`\`\`

### 4. Commit
\`\`\`bash
git add .
git commit -m "feat: add new SDVOSB prompts"
\`\`\`

### 5. Push & PR
\`\`\`bash
git push origin feature/your-feature-name
\`\`\`

Then open Pull Request on GitHub.

## Contribution Types

### 1. New Prompts
Add to PROMPT_LIBRARY.json with:
- Unique ID
- Category (content/analysis/strategy/ideas/optimization)
- Clear instructions
- Example output
- Use cases

### 2. Bug Reports
Open issue with:
- What happened
- Expected behavior
- Steps to reproduce
- Your environment

### 3. Documentation
- Fix typos
- Add examples
- Clarify instructions
- Add troubleshooting

### 4. Performance Data
After 30 days of live posts, share:
- Real performance metrics
- What worked/didn't work
- Audience feedback
- Lessons learned

## Code Style
- JSON: Valid, properly formatted, no trailing commas
- Markdown: Clear headings, code blocks with language
- Python: Follow PEP 8

## Licensing
By contributing, you agree your contribution is under MIT License.

## Questions?
- Open an issue
- Check existing discussions
- Email the maintainer

Thanks for contributing to Echo! 🚀
