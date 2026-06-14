#  AgenticInsight

**AgenticInsight** is a multi-agent AI research platform that autonomously researches a topic, gathers information from the web, analyzes sources, generates a structured report, and critiques its own output for quality.

Built using **LangChain**, **Groq LLMs**, **Tavily Search**, **BeautifulSoup**, and **Streamlit**, AgenticInsight demonstrates how multiple AI agents can collaborate to perform complex research tasks.

---

## Screenshot
<img width="1828" height="896" alt="Image" src="https://github.com/user-attachments/assets/3ee6326f-3820-45f3-96d8-8424333f7921" />
<img width="1878" height="882" alt="Image" src="https://github.com/user-attachments/assets/c96bb760-7047-416a-8315-c97eed47bed3" />
<img width="1787" height="858" alt="Image" src="https://github.com/user-attachments/assets/6c841b84-3a24-4014-965d-3cfd0dc6a422" />

## ✨ Features

### 🔍 Research Agent

* Searches the web for relevant and recent information.
* Uses Tavily Search API for high-quality search results.
* Extracts titles, URLs, and summaries.

### 📖 Reader Agent

* Scrapes selected web pages.
* Cleans and extracts meaningful content.
* Removes unnecessary HTML elements such as:

  * Scripts
  * Styles
  * Navigation menus
  * Footers

### ✍️ Writer Agent

* Generates professional research reports.
* Creates:

  * Introduction
  * Key Findings
  * Conclusion
  * Sources

### 🧐 Critic Agent

* Reviews generated reports.
* Scores report quality.
* Highlights strengths.
* Suggests improvements.
* Provides an overall verdict.

### 🎨 Modern Streamlit UI

* Interactive research dashboard.
* Real-time pipeline visualization.
* Download generated reports as Markdown files.

---

# 🏗️ Architecture

```text
User Topic
     │
     ▼
┌──────────────────┐
│  Search Agent    │
│ (Tavily Search)  │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│  Reader Agent    │
│  (Web Scraping)  │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│  Writer Chain    │
│ Report Creation  │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│  Critic Chain    │
│ Quality Review   │
└────────┬─────────┘
         │
         ▼
    Final Report
```

---

# 🛠️ Tech Stack

### AI & Agents

* LangChain
* LangChain Agents
* ChatGroq
* Groq LLM

### Search & Retrieval

* Tavily Search API

### Web Scraping

* BeautifulSoup4
* Requests

### Frontend

* Streamlit

### Environment Management

* Python Dotenv

---

# 📁 Project Structure

```text
AgenticInsight/
│
├── app.py
├── agent.py
├── tools.py
├── pipeline.py
├── requirements.txt
├── pyproject.toml
├── .env
│
└── assets/
```

### app.py

Streamlit user interface and pipeline orchestration.

### agent.py

Contains:

* Search Agent
* Reader Agent
* Writer Chain
* Critic Chain

### tools.py

Contains:

* Web Search Tool
* URL Scraping Tool

### pipeline.py

CLI version of the research workflow.

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/Bharrguv/AgenticInsight.git

cd AgenticInsight
```

---

## Create Virtual Environment

### Windows

```bash
python -m venv .venv

.venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv .venv

source .venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

or

```bash
pip install -e .
```

---

# 🔑 Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key

TAVILY_API_KEY=your_tavily_api_key
```

---

# ▶️ Running The Application

Launch Streamlit:

```bash
streamlit run app.py
```

Open:

```text
http://localhost:8501
```

---

# 💻 CLI Mode

You can also run the research pipeline directly from the terminal.

```bash
python pipeline.py
```

Enter a topic when prompted.

Example:

```text
Enter research topic:

Future of Agentic AI
```

---

# 🔄 Research Workflow

### Step 1 — Search

The Search Agent:

* Finds relevant sources.
* Collects URLs.
* Extracts summaries.

### Step 2 — Read

The Reader Agent:

* Scrapes source content.
* Cleans HTML.
* Extracts useful information.

### Step 3 — Write

The Writer Chain:

* Organizes findings.
* Generates a structured report.

### Step 4 — Critique

The Critic Chain:

* Reviews report quality.
* Assigns a score.
* Suggests improvements.

---

# 📊 Example Output

```text
Topic:
Future of Agentic AI

Score: 8.5/10

Strengths:
- Well-structured report
- Comprehensive research
- Strong source coverage

Areas to Improve:
- More real-world examples
- Additional industry statistics

Verdict:
A strong research report with good factual grounding.
```

---

# 🚧 Current Limitations

* Depends on publicly accessible websites.
* Scraped content is truncated.
* Search quality depends on available web results.
* LLM outputs may vary slightly between runs.

---

# 🔮 Future Improvements

* Multi-agent planning system
* Memory-enabled research workflows
* RAG integration
* Citation verification
* PDF export
* Report versioning
* Source ranking
* Autonomous research loops
* Multi-model support

---

# 🎯 Why This Project Matters

AgenticInsight demonstrates practical AI Engineering concepts:

* Agentic AI
* Multi-Agent Systems
* Tool Calling
* Web Search Integration
* Web Scraping
* LLM Orchestration
* Prompt Engineering
* Streamlit Deployment

It serves as an excellent portfolio project for aspiring:

* AI Engineers
* GenAI Developers
* LangChain Developers
* Agentic AI Builders

---

# 👨‍💻 Author

Built with ❤️ using LangChain, Groq, Tavily, and Streamlit.

If you found this project useful, consider giving it a ⭐ on GitHub.
