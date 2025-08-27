# BlindE: Memory-Safe Prevention of Data Exposure and Injection in AI Agents

BlindE separates LLM planning from data execution, enabling agents to orchestrate tasks using blind references without observing sensitive data. This memory-safe architecture prevents data leakage and injection attacks by design.

## Features
- **Blind Planning**: Agents use data references they cannot observe
- **Policy Enforcement**: Validates all data flows before execution  
- **Secure Runtime**: Executes tools with real data in isolation

## How It Works
Agent generates blind execution plan → Tool calls process data without returning to LLM → Policy validates data flow at all times → Only authorized results returned

## Security
Provides guarantees against indirect prompt injection (XPIA), data exfiltration, and tool confusion through architectural separation.

## Research-stage
We investigate this prototype and security pattern in more detail in [this preliminary paper](https://docs.google.com/document/d/1FwzQNX0IdaevenZVpwQ6Ph_1BA0fdE8OeqEkKx8-dfo/edit?tab=t.0)

## Getting Started
You can open the notebook directly in [google colab](https://colab.research.google.com/github/its-emile/memory-safe-agent/blob/main/Memory_safe_Agent.ipynb)

Alternatively for local execution:
```bash
git clone https://github.com/its-emile/memory-safe-agent
jupyter notebook Memory_safe_Agent.ipynb
```

BlindE is an example of patterns to mitigate data exopsure risks in AI agents, for more mitigations for AI agent security risks see [OWASP Agentic AI Security Guide](https://owasp.org/www-project-top-10-for-large-language-model-applications/).
