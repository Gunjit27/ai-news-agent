# 📰 AI News Agent

AI News Agent is an automated crew powered by CrewAI that fetches the latest news about a topic, scrapes additional details from the web, writes a full news article, and saves it into a structured file — all without human intervention.

## 🚀 How It Works

This project uses a modular agent-task setup with CrewAI:

- **Retrieve News**: Finds the latest articles about a given topic.
- **Scrape Websites**: Extracts deeper insights from linked articles or relevant sites.
- **Write News Article**: Generates a complete, engaging article.
- **Save to File**: Writes the output into a clean, dated markdown file.

The agents and tasks are fully customizable via YAML config files.

## 🛠️ Project Structure

```bash
ai_news_agent/
├── config/
│   ├── agents.yaml
│   └── tasks.yaml
├── src/
│   └── ai_news_agent/
│       ├── main.py
│       └── crew.py
├── news/
│   └── {date}_news_article.md
├── README.md
├── requirements.txt
└── .env
```
## 📦 Installation
1. Clone the repository:

```bash
git clone https://github.com/Gunjit27/ai-news-agent.git
cd learning/ai-news-agent
```
2. Install dependancies:
```bash
pip install crewai
pip install "crewai[tools]"
```

## ⚙️ Requirements
1. Python 3.11.11
2. CrewAI
3. CrewAI Tools (crewai[tools])
4. Serper API Key for news retrieval

## 🏃‍♂️ Running the AI News Agent
To run the agent and generate a news article:
```bash
python ./ai_news_agent/src/ai_news_agent/main.py
```
The generated article will be saved inside the news/ folder, named like:
```bash
news/yy-mm-dd_news_article.md
```

## ⚡ Features
1. Modular agents and tasks for flexibility
2. Uses real-time data scraping
3. Fully automated pipeline from search to file generation
4. YAML-based configuration for easy extension
5. Environment variable support for API keys

## 📄 Configurations

### Agents: `config/agents.yaml`
Define the role, goal, and backstory of each agent.

### Tasks: `config/tasks.yaml`
Define the description, expected outputs, and agent-to-task mapping.
