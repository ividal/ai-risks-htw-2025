# AI Risks & Vulnerabilities Workshop - Supporting Materials

This repository contains supporting materials for the **AI Risks & Vulnerabilities Workshop** at HTW Berlin.

## Workshop Information

For detailed information about the workshop schedule, objectives, and structure, please see [index.html](index.html).

## Recommended Tools Installation

Before attending the workshop, we recommend installing the following tools:

### 1. uv (Python Package Manager)
A fast Python package installer and resolver.

**macOS & Linux:**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows (PowerShell):**
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

**Installation Guide:** https://docs.astral.sh/uv/getting-started/installation/

### 2. Docker
Containerization platform for consistent development environments.

**Download and Installation:** https://docs.docker.com/get-docker/

### 3. Ollama
![Ollama Logo](https://ollama.ai/ollama.png)

Local large language model runner for offline AI development. Ollama serves as a backup option for participants who don't have access to API keys from commercial LLM providers (such as OpenAI, Anthropic, or Mistral AI).

**Installation Guide:** https://ollama.ai/download

#### Using Ollama

After installing Ollama, here's how to get started:

**1. Pull and Run Models:**
```bash
# Pull a model (e.g., Llama 3.1 8B)
ollama pull llama3.1:8b

# Run a model interactively
ollama run llama3.1:8b

# Run a model with a specific prompt
ollama run llama3.1:8b "What is artificial intelligence?"
```

**2. Check if Ollama is Working:**
```bash
# Check Ollama service status
ollama list

# Test with a simple prompt
ollama run llama3.1:8b "Hello, are you working?"
```

**3. Call Models via cURL:**
```bash
# Generate a response
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "llama3.1:8b",
  "prompt": "Explain AI risks in one sentence"
}'

# Chat completion (conversation)
curl -X POST http://localhost:11434/api/chat -d '{
  "model": "llama3.1:8b",
  "messages": [
    {
      "role": "user",
      "content": "What are the main risks of AI systems?"
    }
  ]
}'
```

**4. Popular Models for AI Risk Analysis:**
```bash
# Pull models suitable for AI risk analysis
ollama pull llama3.1:8b      # Good balance of performance and speed
ollama pull llama3.1:70b     # Higher quality, slower
ollama pull mistral:7b       # Fast and efficient
ollama pull codellama:7b     # Good for code-related analysis
```

**5. Ollama API Documentation:**
For complete API reference and advanced usage, visit: https://github.com/ollama/ollama/blob/main/docs/api.md

### 4. any-agent (Mozilla AI)
Open-source framework for building AI agents.

**Installation Guide:** https://mozilla-ai.github.io/any-agent/

## Repository Contents

- `index.html` - Workshop overview and detailed schedule
- `ai_landscape_infographic.html` - Visual representation of AI landscape
- `toy_qa/` - Example agent implementation and evaluation materials
- `LICENSE` - Repository license information

## Getting Started

1. Clone this repository
2. Install the recommended tools above
3. Review the workshop materials in `index.html`
4. Explore the example agent in the `toy_qa/` directory

