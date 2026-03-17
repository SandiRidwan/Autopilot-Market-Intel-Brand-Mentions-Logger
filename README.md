# AI Brand Tracker Autopilot 🚀

An automated Market Intelligence system built on **Make.com** that tracks brand mentions and "Share of Voice" across Large Language Models (LLMs) using the **Groq API**.

## 📌 Project Overview
This project automates the process of auditing AI responses. It triggers daily to ask specific market-related questions to the **Llama 3** model, repeats the queries to ensure statistical consistency, and logs the extracted brand data directly into **Google Sheets**.

## 🛠️ Tech Stack
- **Automation Platform:** [Make.com](https://make.com)
- **LLM Engine:** Groq (Llama 3.1 8B / 70B)
- **Database:** Google Sheets API
- **Communication:** Gmail API
- **Logic:** Repeater, Sleep Tools, and Data Parsers

## ⚙️ How It Works
1. **Search Rows:** The system fetches custom prompts from a Google Sheet "Prompts" tab.
2. **Repeater:** Each prompt is executed 10 times to capture the AI's consistency and variety in brand recommendations.
3. **Groq Integration (The Tracker):** Generates high-speed responses using the Llama 3 model.
4. **Groq Integration (The Extractor):** A second AI pass to clean the data, extracting ONLY brand names in a comma-separated format.
5. **Data Logging:** Results are appended to a "Weekly_Logs" tab, including:
   - Full AI Response
   - Extracted Brands
   - First Mentioned Brand (Primary recommendation)
   - Brand Count per response
6. **Notification:** Sends a daily summary email via Gmail once the batch is completed.

## 📊 Key Features
- **Cost-Efficient:** Optimized for Free Tier APIs by using Groq's high-speed, low-latency engine.
- **Anti-Rate Limit Logic:** Implements specialized "Sleep" delays and batching (Daily limit of 3 prompts) to stay within API quotas.
- **Data Structure:** Automatic parsing of unstructured AI text into structured data for easy Pivot Table analysis.

## 🚀 Setup Instructions
1. Import the provided `blueprint.json` into your Make.com dashboard.
2. Connect your **Groq API Key** to the Groq modules.
3. Link your **Google Sheets** account and select your target spreadsheet.
4. Set the scheduling to **Daily** at your preferred time.

## 📝 License
This project is open-source and available under the MIT License.

---
**Developed by Sandi** - *Electrical Engineer & Automation Enthusiast*
