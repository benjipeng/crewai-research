```python
# Cell 1: Secure API Key Input
from getpass import getpass
import os

api_key = getpass("Enter your OpenAI API key (input will be hidden): ")
os.environ["OPENAI_API_KEY"] = api_key.strip()

# Verification
if not api_key.startswith("sk-"):
    raise ValueError("Invalid API key format. Must start with 'sk-'")
```
