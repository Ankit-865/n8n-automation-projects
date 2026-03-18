# n8n-automation-projects
1 News AI agent
# 🤖 News AI Agent — n8n Workflow

An automated AI-powered news briefing agent built with n8n that fetches the latest tech headlines, formats them using Google Gemini AI, and delivers a clean email to your Gmail inbox every morning — completely free.

---

## 📌 What It Does

Every morning at 8 AM, this workflow automatically:

1. **Fetches** the latest technology headlines using News API
2. **Formats** them into a clean, readable briefing using Google Gemini AI
3. **Delivers** the final email straight to your Gmail inbox

No manual work. No copy-pasting. Just wake up and your news is already waiting for you.

---

## 🔧 Workflow Overview

```
Schedule Trigger → HTTP Request (News API) → Google Gemini AI → Gmail
```

| Node | Purpose |
|------|---------|
| Schedule Trigger | Runs the workflow daily at 8 AM |
| HTTP Request | Fetches top 5 latest tech headlines from News API |
| Google Gemini | Formats articles into a clean email briefing |
| Gmail | Sends the briefing to your inbox |

---

## 🛠️ Tools & APIs Used

| Tool | Cost |
|------|------|
| [n8n](https://n8n.io) | Free (Cloud) |
| [News API](https://newsapi.org) | Free tier |
| [Google Gemini API](https://aistudio.google.com) | Free |
| Gmail | Free |

**Total running cost = ₹0/day** 🎉

---

## 📋 Prerequisites

Before setting up this workflow, make sure you have:

- [ ] n8n account (cloud.n8n.io)
- [ ] News API key — sign up at [newsapi.org](https://newsapi.org)
- [ ] Google Gemini API key — get it at [aistudio.google.com](https://aistudio.google.com)
- [ ] Gmail account connected to n8n

---

## 🚀 Setup Instructions

### Step 1 — Import Workflow
1. Download the `news-ai-agent.json` file from this repo
2. Open n8n → Click **"Add Workflow"** → **"Import from file"**
3. Select the downloaded JSON file

### Step 2 — Configure News API
1. Open the **HTTP Request** node
2. Replace `YOUR_API_KEY` in the URL with your News API key
3. Customize the topic by changing `q=technology` to any topic you want

```
https://newsapi.org/v2/everything?q=technology&language=en&sortBy=publishedAt&pageSize=5&apiKey=YOUR_API_KEY
```

### Step 3 — Configure Google Gemini
1. Open the **Google Gemini** node
2. Add your Gemini API key as a new credential
3. Select model: `gemini-2.0-flash` or latest available

### Step 4 — Configure Gmail
1. Open the **Gmail** node
2. Connect your Google account via OAuth2
3. Update the **To** field with your email address

### Step 5 — Activate
1. Save the workflow (`Ctrl + S`)
2. Click **Publish** / toggle **Active**
3. Done! Your first briefing arrives tomorrow at 8 AM ✅

---

## 📧 Sample Output

```
📰 Daily News Briefing - 18 Mar 2026

---

**Nvidia Makes a $1T Prediction**
Nvidia's CEO Jensen Huang predicts the company will generate $1 trillion 
in revenue from AI chips by 2027.
Source: Newser
URL: https://...

---

**How to survive a nuclear winter**
An article outlines survival strategies for a nuclear winter...
Source: Reuters
URL: https://...
```

---

## 🎯 Customization Ideas

- Change `q=technology` to `q=sports` or `q=india` for different news topics
- Change `pageSize=5` to get more or fewer articles
- Modify the Gemini prompt to change the email format
- Add multiple email recipients in the Gmail node
- Change the schedule time to evening instead of morning

---

## 📚 What I Learned

- How to use free public APIs in n8n
- Chaining multiple nodes to pass data between steps
- Using Google Gemini AI to process and format raw API data
- Setting up Gmail OAuth2 authentication in n8n
- Automating workflows with Schedule Trigger

---

## 🔗 Connect With Me

If you found this useful or want to build something similar, feel free to connect!

- LinkedIn: [Your LinkedIn Profile]
- GitHub: [Your GitHub Profile]

---

## 📄 License

MIT License — feel free to use, modify and share!

---

⭐ If this helped you, consider giving this repo a star!
