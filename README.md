# 🔍 Apollo B2B Leads Generation & Cold Email Automation (n8n)

This n8n workflow automates the entire process of:
1. Collecting leads from Apollo.io by organization name or domain
2. Verifying emails using Hunter
3. Generating personalized cold emails using OpenAI
4. Storing results in Google Sheets
5. (Optional) Sending or drafting emails via Gmail

---

## 📌 Features

- 🌐 **Apollo Scraping** by domain or company
- ✅ **Hunter Email Validation** (only uses valid/risky emails)
- ✨ **Cold Email Generation** using GPT (ChatGPT via OpenAI API)
- 📊 **Google Sheets Logging** (raw + final leads + email content)
- 📤 **Gmail Integration** to draft or send messages automatically

---

## 🛠️ Requirements

- n8n instance (Cloud or Self-Hosted)
- [Apify account](https://www.apify.com/)
- [Apollo API Key](https://apollo.io/)
- [Hunter.io API Key](https://hunter.io/)
- [OpenAI API Key](https://platform.openai.com/)
- Google account with Sheets & Gmail access

---

## 🔐 Environment Variables & Credentials

| Name                | Description                          | How to Set                        |
|---------------------|--------------------------------------|-----------------------------------|
| `APIFY_API_KEY`     | Apify token for actor run            | n8n Credential Manager            |
| `APOLLO_API_KEY`    | Apollo enrichment API key            | n8n HTTP Header (x-api-key)       |
| `HUNTER_API_KEY`    | Email verification                   | n8n Credential Manager            |
| `OPENAI_API_KEY`    | Used for GPT cold email generation   | n8n Credential Manager            |
| `GOOGLE_SHEET_URL`  | Target Google Sheet for storing data | Set in node parameter             |
| `GMAIL_ACCOUNT`     | Gmail account to send/draft emails   | n8n OAuth2 Gmail credential       |

> ⚠️ **Important**: Do **not** hardcode API keys. Use environment variables or n8n’s encrypted credentials.
