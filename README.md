# Reddit-Posts-Lead-Extractor-
An n8n-based Reddit lead generation workflow that scrapes targeted subreddits, filters posts by intent keywords, uses AI (OpenAI &amp; Google Gemini) to verify genuine hiring/service requests, and saves qualified leads to Google Sheets. Fully customizable and automated for real-time client prospecting.


# Reddit Lead Generator (n8n Workflow)

## 📌 Overview
This project is an **automated lead generation workflow** for Reddit, designed in **[n8n](https://n8n.io/)**.  
It scans multiple subreddits, filters posts based on service/hiring intent, and uses AI classification to verify genuine opportunities before saving them to Google Sheets.

## 🚀 Features
- ✅ Scrapes posts from multiple subreddits (`r/hireaprogrammer`, `r/marketing`, `r/startup`)
- 🔍 Filters posts by predefined **intent keywords**
- 🤖 Uses **OpenAI GPT-4.1 Nano** and **Google Gemini 1.5 Flash** for AI-based verification
- 📄 Saves qualified leads to **Google Sheets** automatically
- ⏱ Scheduled runs (hourly or as configured)
- 🔄 Modular design — easily add/remove subreddits or change filters

## 📂 Workflow Structure
1. **Schedule Trigger** – Runs the workflow periodically.
2. **HTTP Request Nodes** – Fetch new posts from subreddits via Reddit API.
3. **Parsing & Merging** – Extracts title, content, URL, subreddit, author, and date.
4. **Keyword Filtering** – Matches posts against a set of lead-intent keywords.
5. **AI Classification** – Verifies if the post is a genuine hiring/service request.
6. **Google Sheets Append/Update** – Stores qualified leads for review.

## 🛠 Requirements
- [n8n](https://n8n.io/) installed locally or on a server
- Reddit API credentials (OAuth2)
- OpenAI API key
- Google Cloud credentials for Sheets API
- Optional: Google Gemini (PaLM) API key

## 📥 Installation
1. **Import Workflow**  
   - In your n8n dashboard, click **Import** and upload the provided `.json` file.
2. **Set Credentials**  
   - Add Reddit OAuth2, OpenAI, Google Sheets, and Gemini API credentials in n8n.
3. **Adjust Schedule**  
   - Configure the `Schedule Trigger` node to your desired interval.
4. **Update Keywords**  
   - Modify the `Keyword Filter` node to target your niche-specific keywords.

## ⚙️ Customization
- **Subreddits**: Add more `HTTP Request` nodes with relevant subreddit URLs.
- **AI Models**: Swap between OpenAI & Gemini or adjust prompts.
- **Output**: Change destination from Google Sheets to databases, CRMs, etc.

## 📜 License
This project is released under the MIT License.  
You are free to use, modify, and distribute it.

---

### 📧 Contact
For suggestions or contributions, feel free to open an issue or pull request.
