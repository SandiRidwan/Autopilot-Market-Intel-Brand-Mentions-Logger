# 🚀 AI Brand Tracker Autopilot
**Automated Market Intelligence & Share of Voice (SoV) Tracker for LLMs**

![Make.com](https://img.shields.io/badge/Platform-Make.com-purple.svg?style=for-the-badge&logo=make)
![Groq API](https://img.shields.io/badge/LLM_Engine-Groq_Llama_3.1-orange.svg?style=for-the-badge&logo=meta)
![Google Sheets](https://img.shields.io/badge/Database-Google_Sheets-green.svg?style=for-the-badge&logo=googlesheets)
![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)

---

## 📌 Project Overview
An advanced automation system built on **Make.com** that audits how AI models (LLMs) perceive and recommend brands. This tool tracks "Share of Voice" by repeatedly querying AI models via **Groq API**, extracting structured brand data, and logging it for statistical analysis.

> **Problem:** How often does ChatGPT or Llama recommend *your* brand vs competitors?  
> **Solution:** This autopilot system runs daily audits to track AI brand bias and recommendations.

---

## 🛠️ Tech Stack & Integrations

| Tool | Role |
| :--- | :--- |
| **Make.com** | Workflow Orchestration & Logic |
| **Groq (Llama 3.1)** | Ultra-fast LLM Inference for Tracking & Data Extraction |
| **Google Sheets** | Dynamic Prompt Management & Weekly Logs |
| **Gmail API** | Automated Daily Summary Reports |
| **Regex & Parsers** | Transforming Unstructured AI Text to Structured Data |

---

## ⚙️ How the Engine Works

### 1️⃣ The Trigger (Search Rows)
The system wakes up daily and fetches custom market-related prompts (e.g., *"What are the best electrical SLO services in Indonesia?"*) from the **Prompts** tab.

### 2️⃣ The Multiplier (Repeater)
To ensure statistical consistency, each prompt is executed **10 times**. AI responses vary; this captures the full spectrum of recommendations.

### 3️⃣ The Inference (Groq Engine)
* **Module A (The Tracker):** Generates a natural AI response to the prompt.
* **Module B (The Extractor):** A specialized "Data Cleaning" pass that strips conversational fluff and returns ONLY brand names in CSV format.

### 4️⃣ The Vault (Data Logging)
Results are appended to the **Weekly_Logs** tab with:
* ✅ Full AI Response
* ✅ Extracted Brand Names
* ✅ **Primary Mention** (First brand recommended)
* ✅ Brand Count (Density of mentions)

### 5️⃣ The Report (Gmail)
Once the batch is done, you receive a clean summary email of today's AI sentiment.

---

## 📊 Key Features & Logic

* **⚡ Groq Powered:** Optimized for speed using Llama 3.1 (8B/70B) via Groq's low-latency engine.
* **🛡️ Anti-Rate Limit:** Built-in "Sleep" tools and batching (Max 3 prompts/day) to stay within free-tier API quotas.
* **📈 Pivot-Ready:** Data is saved in a structured format, ready for Google Sheets Pivot Tables to visualize *Share of Voice*.
* **💰 Cost $0:** Fully functional using Free Tier accounts of Make.com and Groq.

---

## 🚀 Setup Instructions

1.  **Import Blueprint:** Download `blueprint.json` from this repo and import it into your **Make.com** dashboard.
2.  **API Connections:**
    * Add your **Groq API Key**.
    * Authorize your **Google Workspace** (Sheets & Gmail).
3.  **Spreadsheet Setup:** Create a sheet with two tabs: `Prompts` and `Weekly_Logs`.
4.  **Schedule:** Set the scheduling to **Daily** (e.g., 08:00 AM).

---

## 📝 License
This project is open-source and available under the **MIT License**.

---
**Developed by Sandi** *Electrical Engineer | Automation Enthusiast | AI Specialist*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/sandi-ridwan/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-lightgrey?style=flat-square&logo=github)](https://github.com/SandiRidwan)
