# Raw LLM vs. Mellea: Reliable Structured Output

Compare raw LLM calls with Mellea's structured extraction for invoice parsing using local Ollama models.

## What You'll Learn

- Raw LLM returns untyped JSON strings requiring manual parsing
- Mellea returns typed Pydantic objects with automatic validation
- Custom validation with `Requirement` objects and the instruct-validate-repair workflow
- Using `ModelOption` for backend-agnostic configuration
- When to use `check_only=True` to avoid the purple elephant effect

## Key Concepts

**Mellea Features Demonstrated:**

- `start_session()` - Initialize LLM backend connection
- `instruct()` - Send instructions with template variables, structured output via `format` parameter
- `Requirement` objects - Define validation rules with automatic repair
- `ModelOption` enum - Backend-agnostic options (TEMPERATURE, SEED, MAX_NEW_TOKENS)
- `@generative` decorator - Advanced structured output from function docstrings
- `req()` and `check()` - Shorthand constructors for requirements

## Prerequisites

- Python 3.11 or 3.12
- [Ollama](https://ollama.com/) installed with a model like `granite4.1:8b`

```bash
ollama pull granite4.1:8b
```

## Run This Recipe

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/generative-computing/mellea-cookbook/blob/main/recipes/RawLLMvsMellea/RawLLMvsMellea.ipynb)

## Related Recipes

- [Quick Start](../QuickStart/QuickStart.ipynb) - Mellea basics
- [Instruct-Validate-Repair](../InstructValidateRepair/InstructValidateRepair.ipynb) - Deep dive into validation patterns
