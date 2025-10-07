# Xmentorcompanion-
AI-powered Twitter bot that provides personalized career mentorship advice. Responds to mentions with actionable guidance using xAI's Grok API. Features rate limiting, secure credential management, and easy deployment. Perfect for automated career coaching on Twitter.
# X Mentor Companion

An AI-powered Twitter bot that delivers personalized career mentorship using xAI’s Grok API. Mention the bot in your tweet, and get actionable, concise career advice, right in your mentions.

---

## 🚀 Features

- **Automatic Twitter responses:** Replies to mentions with career guidance
- **AI-driven advice:** Uses xAI Grok for tailored, actionable feedback
- **Spam protection:** 60-second cooldown per user
- **Secure:** API keys managed via environment variables
- **Twitter-friendly:** Responses fit within 280 characters

---

## 🛠️ Prerequisites

- Python 3.8+
- Twitter Developer account (API keys)
- xAI API key ([Get one here](https://x.ai/api))

---

## ⚡ Quickstart

1. **Clone the repo:**
    ```bash
    git clone https://github.com/YOUR_USERNAME/x-mentor-companion.git
    cd x-mentor-companion
    ```

2. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3. **Setup environment variables:**
    - Copy `.env.example` to `.env`:
      ```bash
      cp .env.example .env
      ```
    - Add your secrets:
      ```env
      CONSUMER_KEY=your_consumer_key
      CONSUMER_SECRET=your_consumer_secret
      ACCESS_TOKEN=your_access_token
      ACCESS_TOKEN_SECRET=your_access_token_secret
      BEARER_TOKEN=your_bearer_token
      XAI_API_KEY=your_xai_api_key
      ```

---

## 🔑 Getting API Credentials

### Twitter

- [Twitter Developer Portal](https://developer.twitter.com/en/portal/dashboard)
- Create an app → Keys and tokens → Generate/copy:
    - Consumer Key (API Key)
    - Consumer Secret (API Secret)
    - Access Token
    - Access Token Secret
    - Bearer Token

### xAI

- [xAI API](https://x.ai/api) → Sign up and get your API key

---

## 🏃 Usage

Start the bot:
```bash
python mentor_bot.py
```

- Authenticates with Twitter
- Listens for @mentions
- Replies with Grok-powered career advice

Stop with `Ctrl+C`.

---

## ⚙️ Configuration

Edit `mentor_bot.py` to tweak:
- `RESPONSE_COOLDOWN` (default: 60 seconds)
- `max_tokens` for Grok (default: 100)
- `temperature` for response creativity (default: 0.7)

---

## 🌐 Deployment

**Server:**  
- `nohup python mentor_bot.py &`  
- Or use `screen`, `tmux`, or a systemd service (see `mentor-bot.service`)

**Cloud:**  
- Heroku (see `Procfile`)
- AWS EC2, DigitalOcean, Railway, Render

---

## 📁 Project Structure

```
x-mentor-companion/
├── mentor_bot.py
├── requirements.txt
├── .env.example
├── .gitignore
├── README.md
├── LICENSE
└── Procfile
```

---

## 🧩 Troubleshooting

- **Auth errors:** Check API keys and permissions in `.env`
- **No responses:** Verify Bearer Token & bot account username, check logs
- **Grok/xAI errors:** Check API key, rate limits, model settings

---

## 🤝 Contributing

1. Fork & branch
2. Commit your changes
3. Open a Pull Request

---

## 📄 License

MIT. See [LICENSE](LICENSE).

---

## ❗ Disclaimer

Career advice is AI-generated; verify with professionals for critical decisions. The bot owner is not responsible for the accuracy of responses.

---

## 💬 Support

- Open an issue
- [Tweepy docs](https://docs.tweepy.org/)
- [xAI API docs](https://x.ai/api)

---

Made with ❤️ using Tweepy and xAI Grok.
