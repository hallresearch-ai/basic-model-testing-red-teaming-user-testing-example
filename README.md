# Supplying an OpenAI API Key

The notebooks look for an API key in the `OPENAI_API_KEY` environment variable. If that variable is not set, the notebooks ask you to paste the key into a secure prompt.

## macOS or Linux

```bash
export OPENAI_API_KEY="your_api_key_here"
```

Then start Jupyter or run the notebook from the same terminal session.

## Windows PowerShell

```powershell
$env:OPENAI_API_KEY = "your_api_key_here"
```

Then start Jupyter or run the notebook from the same PowerShell session.

## Secure Notebook Prompt

If you do not set `OPENAI_API_KEY`, run the connection cell and paste your key when prompted:

```python
api_key = os.getenv("OPENAI_API_KEY")

if not api_key:
    api_key = getpass("Enter your OpenAI API key: ")

client = OpenAI(api_key=api_key)
```

Do not commit API keys to this repository.
