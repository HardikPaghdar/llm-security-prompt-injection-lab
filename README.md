# LLM Security & Prompt Injection Testing Lab

A deterministic regression lab for known prompt-injection phrases and deny-by-default tool permissions.

## Features
- Editable attack-pattern corpus
- Categories for instruction override, secret exfiltration, and tool abuse
- Tool-policy checks for read-only tools
- Sample test cases, pytest coverage, and CI
- Explicit warning that no match does not prove safety

## Run
```bash
pip install -r requirements.txt
uvicorn app:app --reload
```
API docs: http://127.0.0.1:8000/docs.

## Security limitations
This is a teaching/regression scaffold, not a complete prompt-injection defense. Pattern matching misses paraphrases and can produce false positives. Real deployments need defense in depth: least-privilege tools, schema validation, isolation, secrets boundaries, human approval for consequential actions, and adversarial evaluation.

## Stack
Python, FastAPI, Pydantic, pytest. No paid APIs required.
