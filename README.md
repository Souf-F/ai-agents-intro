# AI Study Guide Generator

Multi-agent pipeline that takes a programming topic and produces a structured Markdown study guide. Built with Python, Google ADK, LiteLLM, and Ollama.

## Pipeline

```
topic input
     │
     ▼
┌────────────────┐
│   Explainer    │  explains the concept clearly
│     Agent      │
└───────┬────────┘
        │
        ▼
┌────────────────┐
│   Practice     │  designs exercises and challenges
│   Designer     │
└───────┬────────┘
        │
        ▼
┌────────────────┐
│   Reviewer     │  checks quality and consistency
│     Agent      │
└───────┬────────┘
        │
        ▼
  output/study_guide.md
```

## Model provider

Default: local model via **Ollama** + **LiteLLM**.
Swap to Gemini, OpenAI, or Claude by updating .

## Setup

```bash
python3 -m venv venv && source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
python3 main.py
```

## Structure

```
├── main.py
├── agents/
│   ├── explainer_agent.py
│   ├── practice_designer_agent.py
│   └── reviewer_agent.py
├── tools/
│   ├── file_writer.py
│   └── validation.py
├── data/
│   └── topic_examples.json
└── output/
    └── study_guide.md
```

## Requirements

- Python 3.10+
- Ollama running locally, or any LiteLLM-compatible provider (Gemini, OpenAI, Claude)

---

Soufiane Filali · Holberton School France
