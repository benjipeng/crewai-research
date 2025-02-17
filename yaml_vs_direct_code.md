# Using YAML or Direct Coding

An YAML configuration likely uses the following structure:

```bash
config/
├── agents.yaml
└── tasks.yaml
src/
└── chemistry_crew.py
```

`agents.yaml` contains

```yaml
researcher:
  role: "Chemistry Researcher"
  goal: "Investigate chemical concepts"
  backstory: "PhD in Analytical Chemistry"
  verbose: true

writer:
  role: "Content Author"
  goal: "Create educational materials"
  backstory: "Textbook author with 10+ years experience"
  verbose: true
```

`tasks.yaml` looks
```yaml
research_task:
  description: "Analyze {topic} fundamentals"
  expected_output: "Markdown report with key concepts"
  agent: researcher
  output_file: "./research.md"

writing_task:
  description: "Develop Q&A pairs for {topic}"
  expected_output: "Formatted lesson script"
  agent: writer
  output_file: "./lesson.md"
```
