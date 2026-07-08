# AI Study Guide Generator

A small multi-agent AI system built with Python, Google ADK, LiteLLM, and Ollama. It receives a programming topic and generates a Markdown study guide.

## Project Structure

```
ai-agents-intro/
├── agents/
│   ├── explainer_agent.py
│   ├── practice_designer_agent.py
│   └── reviewer_agent.py
├── tools/
│   ├── file_writer.py
│   └── validation.py
├── output/
│   └── study_guide.md
├── data/
│   └── topic_examples.json
├── .env.example
├── .gitignore
├── requirements.txt
├── README.md
└── main.py
```

## Model Provider

By default, this project uses a local model served through **Ollama**, connected via **LiteLLM**. See `.env.example` for configuration. Other LiteLLM-compatible providers (Gemini, OpenAI, Claude) can be used instead by updating the `.env` file.

## Setup

1. Clone the repository.
2. Create a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Copy `.env.example` to `.env` and fill in your configuration.
5. Make sure Ollama is running locally with the model set in `.env`.

## Usage

```bash
python3 main.py
```

This will run the agent workflow and generate a study guide in `output/study_guide.md`.

## Status

Project structure created. Agent logic and tools are being implemented in the following tasks.

## Author

Soufiane Filali — [Souf-F](https://github.com/Souf-F)
