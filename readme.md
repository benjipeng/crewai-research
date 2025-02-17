# CrewAI playground and Beyond

CrewAI CLI offers a streamlined way to run crews, especially for simpler setups. We adapted our project to work with it.

## Getting Ready & Configuration
```bash
crewai create crew chemistry-scriptwriter
cd chemistry-scriptwriter
# Install core dependencies
crewai install
```

In the `.env` file, put in the API Keys
```bash
OPENAI_API_KEY=your-key-here
SERPER_API_KEY=your-key-here  # For research capabilities
```
