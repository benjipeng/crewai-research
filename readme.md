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
### Agent Configuration (`config/agents.yaml`)

```yaml
chemistry_educator:
  role: Chemistry Education Specialist
  goal: Create structured lesson scripts with logical Q&A progression
  backstory: |
    Expert in breaking down complex chemistry concepts into digestible 
    educational content for freshman students. Skilled in pedagogical
    structuring and logical flow design.
  tools:
    - web_search
    - knowledge_base
  verbose: true
  max_iter: 5
```

### Task Configuration (`config/tasks.yaml`)

```yaml
script_development:
  name: Chemistry Lesson Script Creation
  description: |
    Develop a 3-subtopic structure with 3 Q&A pairs per subtopic,
    ensuring logical progression from basic to advanced concepts
  expected_output: |
    Markdown document with:
    - Main topic overview
    - 3 subtopics with explanations
    - 3 Q&A pairs per subtopic
    - Progressive difficulty structure
  tools:
    - web_search
  agent: chemistry_educator
```