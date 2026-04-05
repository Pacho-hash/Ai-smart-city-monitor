# 🏙️ AI Smart City Alert System (Riyadh)

An automated, AI-driven data pipeline built to monitor real-time city conditions and proactively alert logistics, supply chain, and operations teams during severe weather or traffic events. 


## ⚙️ Architecture & Tech Stack

- **Orchestration:** [n8n](https://n8n.io/) (Workflow Automation)
- **AI / LLM:** Google Gemini 2.5 Flash (Data Analysis & Decision Making)
- **Data Ingestion:** OpenWeatherMap API (Real-time environmental data)
- **Alerting:** Discord/Slack Webhooks (Automated notifications)

## 🚀 How It Works

This system replaces manual dashboard monitoring with an intelligent autonomous agent.

1. **Scheduled Trigger:** An n8n cron job wakes the system automatically every hour.
2. **Data Fetch:** The workflow pulls real-time environmental JSON data for Riyadh, Saudi Arabia.
3. **AI Contextualization:** Google Gemini acts as an Operations Analyst, reading the raw JSON data and determining if conditions (e.g., temperatures > 45°C, sandstorms, heavy rain) pose a threat to city logistics.
4. **Conditional Logic:** 
   - If conditions are safe, the workflow terminates silently, saving API costs and preventing alert fatigue.
   - If a threat is detected, the AI generates a structured warning report.
5. **Notification:** The warning is immediately pushed to a designated Slack/Discord channel for operations managers to take action.

## 🛠️ How to Run Locally

You can run this exact pipeline in your own environment in under 5 minutes.

1. Clone this repository.
2. Ensure you have [n8n](https://docs.n8n.io/hosting/installation/docker/) installed via Docker or Node.js (`npx n8n`).
3. Open your n8n canvas and click **Import from File**.
4. Select the `smart-city-alert-workflow.json` file included in this repo.
5. Double-click the nodes to add your own API credentials:
   - `OpenWeatherMap API Key`
   - `Google Gemini API Key`
   - `Discord/Slack Webhook URL`
6. Click **Test Workflow**!

## 📈 Business Value & Use Cases

- **Logistics & Delivery:** Automatically reroute delivery fleets before a severe sandstorm hits.
- **Construction & Contracting:** Halt outdoor labor operations when AI detects unsafe heat index levels, ensuring compliance with local safety regulations.
- **Event Management:** Alert organizers of sudden weather changes for outdoor events (e.g., Riyadh Season).

---
*Built by [Pacho-hash](https://github.com/Pacho-hash) .*
