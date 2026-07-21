# Automated-AI-Triage-System
Automated AI-powered support ticket triage pipeline using n8n, LLMs, and Telegram API to reduce manual support load.

# AI-Powered Customer Support Triage Pipeline

## 📌 The Business Problem
Customer support teams often spend up to 30% of their time manually reading and categorizing incoming tickets. Critical issues (e.g., billing failures or server downtime) can get lost in the general queue, negatively impacting SLA and customer retention.

## 💡 The Solution
An automated, AI-driven workflow that intercepts incoming support tickets, analyzes the text sentiment and context using an LLM, assigns a priority level, and instantly escalates critical issues to the on-call team via Telegram.

## 🛠 Tech Stack & Tools
* **Orchestration:** n8n 
* **AI/LLM Engine:** DeepSeek / OpenAI (via OpenRouter API)
* **Integration:** Telegram Bot API, REST Webhooks
* **Core Skills:** API Integration, Prompt Engineering, JSON Parsing, Workflow Automation

## ⚙️ How It Works (Pipeline Architecture)
1. **Trigger:** A webhook receives the incoming ticket data (simulating a website form or helpdesk integration).
2. **AI Analysis:** The payload is sent to an LLM via direct HTTP request with a strict system prompt to categorize the issue (Billing, Bug, Feature Request) and output a structured JSON response.
3. **Smart Routing:** A switch node parses the AI's JSON output.
4. **Escalation:** If the priority is evaluated as `High`, the system automatically formats an alert and pushes it to a Telegram channel/bot for immediate human intervention.

## 📺 Demonstration
[Insert link to your Loom/YouTube video here]
