# GitHub Starred Repo Ingestion Skill

## Description
Automatically fetches, categorizes, and learns from GitHub starred repositories to create reusable AI skills. This skill transforms your GitHub stars into actionable knowledge.

## Features
- Fetches starred repositories from GitHub API
- Categorizes repos into domains (Bitcoin/Lightning, AI/ML, Privacy, etc.)
- Generates skill files for each category
- Creates comprehensive reports
- Designed for daily cron job integration

## Installation
1. Ensure GitHub CLI is installed and authenticated
2. Clone this repository
3. Place the skill file in your `~/.hermes/skills/` directory

## Usage
```bash
# Fetch and process starred repos
gh auth login  # Authenticate if needed
./fetch_starred_repos.sh

# Process and categorize
python categorize_repos.py

# Generate skills
python generate_skills.py
```

## Configuration
Create a `.env` file with your GitHub token:
```
GITHUB_TOKEN=your_personal_access_token_here
```

## Output Structure
- `starred_repos.json` - Raw repository data
- `reports/` - Generated reports with timestamps
- `skills/` - Category-specific skill files

## Categories
- Bitcoin/Lightning
- AI/ML
- Privacy/Security
- Finance
- Development Tools
- Social Media
- Health
- Travel
- Voice/Audio
- Video

## Cron Job Integration
```bash
# Example cron entry for daily sync
0 9 * * * /path/to/StarLearner-Nexus/daily_sync.sh
```

## Requirements
- GitHub CLI (gh)
- Python 3.8+
- curl
- jq (for JSON processing)

## License
MIT License - Free to use, modify, and distribute

## Contributing
Pull requests welcome! Focus areas:
- Additional categorization algorithms
- Improved skill generation templates
- Integration with other Git platforms

## Marketplace
This skill is available on the AI Skills Marketplace where creators earn recognition and compensation for their contributions.

## Support
For issues or questions, open a GitHub issue or contact the maintainer.

---

Created by StarLearner-Nexus - Transforming stars into knowledge since 2024.