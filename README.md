# seo-agent-N8N
<img width="1103" height="471" alt="image" src="https://github.com/user-attachments/assets/53560aa6-8ae0-47d2-b281-7d9f14c82a91" />

# Demo:

https://drive.google.com/file/d/1x8-Sd_b0lOeVR52RoWbspT7fulKQAct-/view?usp=drive_link

# 🚀 AI-Powered SEO Agent Workflow

This repository hosts a robust, automated workflow designed to perform comprehensive SEO audits, competitor analysis, and content optimization, leveraging AI to generate actionable insights and suggestions. Built for scalability and efficiency, this agent streamlines the entire SEO process from data collection to final report generation.

## ✨ Features

*   **Fully Automated SEO Audit:** Conducts competitor research, performance analysis, and content optimization in a single, streamlined pass.
*   **AI-Driven Insight Generation:** Utilizes advanced GPT models for in-depth analysis, content suggestion, and report summary creation, minimizing manual interpretation.
*   **Modular & Customizable:** Each workflow module is designed to be modular, allowing for easy addition, removal, or modification of steps to fit specific SEO strategies (e.g., integrating backlink analysis, schema generation).
*   **Scalable Performance:** Capable of running across hundreds of URLs automatically, making it ideal for large-scale SEO operations.


## 🛠️ How It Works (Workflow Overview)

The workflow is structured into several key stages, ensuring a holistic approach to SEO analysis and optimization:

1.  **Workflow Preparation:**
    *   **Trigger:** Initiated via webhook or manual trigger (e.g., new URL submission).
    *   **Data Setup:** Collects environment variables, API keys (Google PageSpeed Insights, SERP scrapers, OpenAI), client info, and target URLs.
    *   **Purpose:** Centralizes input collection and initializes the automation environment.

2.  **SERP Analysis & Competitor Research:**
    *   **Get SERPs:** Pulls live Google Search results for target keywords/URLs using a scraper or SEO API.
    *   **Related Searches & FAQs:** Scrapes "Related Searches" and extracts/generates "People Also Ask" (PAA) questions to identify long-tail keywords and content opportunities.
    *   **Analyze Competitors:** Crawls top SERP competitors, extracting headings, keyword usage, and metadata for benchmarking.
    *   **Purpose:** Understands current ranking landscape and establishes benchmarks.

3.  **URL Inspection & Page Speed Check:**
    *   **Fetch PageSpeed:** Utilizes Google PageSpeed Insights to assess load times, mobile/desktop performance, and Core Web Vitals.
    *   **Parse & Save Data:** Extracts key performance metrics (FCP, LCP, CLS, TBT) and stores them alongside SERP insights.
    *   **Purpose:** Diagnoses page experience issues and benchmarks technical performance.

4.  **Performance Analysis:**
    *   **Fetch & Save Data:** Queries historical performance metrics (optional GSC integration) and updates a database/Google Sheet.
    *   **Parse Data:** Prepares clean performance data for the optimization module.
    *   **Purpose:** Determines how technical performance impacts SEO ranking.

5.  **Crawl Article to be Optimized:**
    *   **Crawl & Parse:** Visits the target URL, downloads HTML/text content, and extracts title, meta description, headings (H1-H6), word count, and keyword frequency.
    *   **Purpose:** Provides a comprehensive view of the page's current content structure and SEO readiness.

6.  **(Optional) Translation:**
    *   **Translate Content:** Applies language translation (e.g., DeepL or GPT) for multi-language SEO or competitor content insights.
    *   **Purpose:** Facilitates multilingual analysis and content generation.

7.  **Data Analysis Using AI (GPT Nodes):**
    *   **Generate Insights:** Multiple GPT nodes generate SEO audit summaries, compare pages against competitors, and score readability, keyword optimization, and structure.
    *   **Common Prompts:** Includes prompts like "How does this page compare to competitors?", "Summarize SEO weaknesses," and "Suggest title/meta improvements."
    *   **Purpose:** Automates expert-level SEO audits without manual interpretation.

8.  **Article Optimization Suggestions:**
    *   **AI-Driven Recommendations:** Generates suggestions for SEO Titles, Meta Descriptions, FAQ Content Blocks, and internal linking.
    *   **Optimized Content Blocks:** Produces content blocks with keyword enhancements.
    *   **Purpose:** Provides plug-and-play SEO content for writers and CMS integrators.

9.  **Formatting Final Report:**
    *   **Compile:** Merges all gathered data: SERP & FAQ data, performance metrics, competitor insights, and GPT-generated suggestions.
    *   **Format:** Formats the final document (Markdown, HTML, Google Docs/Sheets).
    *   **Purpose:** Prepares client-facing or internal reports for implementation.

10. **Store Report in Google Drive:**
    *   **Upload:** Pushes the final report to a specified Google Drive folder, optionally named by domain/keyword/date.
    *   **Notifications:** Can trigger Slack/Email notifications.
    *   **Purpose:** Ensures organized and easily retrievable documentation.

## ⚙️ Technologies & Tools

*   **Orchestration:** n8n (for workflow design and execution)
*   **Programming Languages:** JS
*   **AI/LLMs:** OpenAI (GPT models:4.1 mini,gpt5 nano,4.O mini)
*   **Data Scraping & Search Result :** Crawl4ai & SerpApi
*   **Deployment:** N8N Cloud
*   **Cloud & Services:** Google Cloud Platform(GCP), Google Sheets , Google Drive,Google Search Console API,Bigquery,Google PageSpeed Insights API

