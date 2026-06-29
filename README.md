# AI Lead Scoring Automation — n8n + Google Gemini

An intelligent lead scoring workflow that uses **Google Gemini AI** to automatically analyze, score, and prioritize incoming leads.

## What It Does

1. **Webhook** receives a new lead (Name, Email, Company, Job Title, Message)
2. **Google Gemini AI** analyzes the lead and returns a score (1–10), tier (Hot/Warm/Cold), reasoning, and recommended action
3. **Google Sheets** stores the lead with AI-generated score and tags
4. **Gmail** sends an instant notification with the full AI analysis

## AI Scoring Output

```json
{
  "score": 8,
  "tier": "Hot",
  "reason": "VP-level at a 500+ employee SaaS company — high budget authority",
  "priority_action": "Call within 2 hours, prepare enterprise pricing deck"
}
```

## Tech Stack

- [n8n](https://n8n.io) — workflow automation
- Google Gemini 2.0 Flash-Lite — AI analysis (free tier)
- Google Sheets — lead database
- Gmail — instant notifications
- Webhook — real-time trigger

## Workflow

```
[Webhook] → [Gemini AI] → [Google Sheets] → [Gmail Notification]
```

## Setup

1. Import `workflow.json` into n8n
2. Add your Gemini API key (get free at aistudio.google.com)
3. Connect Google Sheets and Gmail credentials
4. Activate — every new lead gets scored automatically

## About

Built by **Dilovar Sam** — AI & Automation Freelancer
📍 Houston, TX | n8n · Zapier · Make · API integrations
🔗 [Upwork Profile](https://www.upwork.com)
