# Product Hunt Launch Tracker

Track and analyze Product Hunt launches. Get daily summaries of trending products, category insights, and competitive intelligence delivered to your inbox or Slack.

## Features

- 📊 Daily trending products tracking
- 🏷️ Category-based filtering
- 📈 Vote and comment analytics
- 🔔 Slack/Telegram notifications
- 📅 Scheduled daily reports
- 🔍 Maker and hunter insights

## Setup

### 1. Fork this repository

### 2. Add Repository Secrets

Go to Settings → Secrets and variables → Actions, and add:

| Secret | Description | Required |
|--------|-------------|----------|
| `PRODUCT_HUNT_API_TOKEN` | Product Hunt API token | Yes |
| `SLACK_WEBHOOK_URL` | Slack webhook for notifications | Optional |
| `TELEGRAM_BOT_TOKEN` | Telegram bot token | Optional |
| `TELEGRAM_CHAT_ID` | Telegram chat ID | Optional |

### 3. Get Product Hunt API Token

1. Go to [Product Hunt API](https://www.producthunt.com/v2/oauth/applications)
2. Create a new application
3. Get your Developer Token

### 4. Enable GitHub Actions

The workflow runs automatically every day at 9 AM UTC. You can also trigger it manually.

## Local Development

```bash
# Install dependencies
pip install -r requirements.txt

# Run locally
export PRODUCT_HUNT_API_TOKEN=your_token
python tracker.py
```

## Output

The tracker generates:
- Daily trending products with metrics
- Category breakdown
- Top makers and hunters
- Markdown report saved to `reports/`

## License

MIT
