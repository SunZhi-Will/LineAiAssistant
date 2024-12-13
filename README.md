<div align="center">

# LINE Bot with Gemini AI

[English](README.md) | [繁體中文](README.zh-TW.md)

This is a chatbot project that combines LINE Messaging API with Google Gemini AI.

</div>

---

### Features

- Integration with LINE Messaging API
- Powered by Google Gemini AI for conversation generation
- Real-time message response
- Environment variable management for sensitive information

### Requirements

- Python 3.8 or higher
- pip (Python package manager)

### Required Packages

```plaintext
python
flask==3.0.2
line-bot-sdk==3.5.1
pyngrok==7.1.5
google-generativeai==0.3.2
python-dotenv==1.0.1
```

### Installation

1. Clone the repository:

```bash
git clone [Your Repository URL]
cd [Project Directory]
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Configure environment variables:
   Create a `.env` file with the following information:

```plaintext
LINE_CHANNEL_ACCESS_TOKEN=Your LINE Channel Access Token
LINE_CHANNEL_SECRET=Your LINE Channel Secret
GEMINI_API_KEY=Your Gemini API Key
```

### Usage

1. Run the application:

```bash
python main.py
```

2. Create a tunnel using ngrok (optional):

```bash
ngrok http 5000
```

3. Set up Webhook URL in LINE Developers Console:
    - Set to `https://your-domain/callback`

### Notes

- Ensure `.env` is included in `.gitignore`
- Never commit sensitive information directly in the code
- Verify you have all required API keys and permissions before use

---
