# WatchtowerGPT Slack Integration

This app connects WatchtowerGPT to Slack via a custom slash command.

## 🔧 Setup Instructions

1. Create a Slack App at https://api.slack.com/apps
2. Add scopes:
   - chat:write
   - commands
   - app_mentions:read
   - channels:history (optional)
3. Create a Slash Command `/watchtower` with the URL: `https://<your-domain>/slack/events`
4. Add the following environment variables:
   - `SLACK_BOT_TOKEN`
   - `SLACK_SIGNING_SECRET`
   - `OPENAI_API_KEY`
5. Run the app:
```bash
pip install -r requirements.txt
flask run --port=3000
```

Use [ngrok](https://ngrok.com/) for local development:
```bash
ngrok http 3000
```
