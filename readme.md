# CrewAI playground and Beyond

## Intro

The CrewAI CLI offers a streamlined way to run crews, especially for simpler setups. We'll adapt our project to work with it. Instead of main.py, we'll have a crew.py (or similar name) that defines the crew, and we'll execute it using the CLI.

### Overall Project
```bash
ai_research_team/
├── .env
├── pyproject.toml
└── src/
    └── ai_research_team/
        ├── config/
        │   ├── agents.yaml
        │   └── tasks.yaml
        ├── crew.py
        ├── main.py
        └── tools/
```