# Azure Local Foundry — Local RAG Application (LangChain + Chroma)

This notebook demonstrates how to build a fully local Retrieval-Augmented Generation (RAG) application using Azure Local Foundry, LangChain, HuggingFace embeddings, and ChromaDB — all running directly on your device with zero cloud dependency.

**The goal of this project is simple:**
Show how Azure Local Foundry makes it easy to run optimized LLMs locally and integrate them into a RAG workflow.

## 🚀 Overview

This sample project walks through:
- Setting up Azure Local Foundry
- Loading a locally accelerated AI model (Qwen, Phi, etc.)
- Building a local semantic search pipeline using embeddings + Chroma
- Running a local RetrievalQA workflow using LangChain's modern chains
- Running everything offline, with predictable performance and full privacy

The code is intentionally simple so developers can easily replicate and extend it.

## 🔍 Why Azure Local Foundry?

Azure Local Foundry makes running AI models locally easy, portable, and hardware-optimized.

It solves some critical developer pain points:

### ✔ Runs Fully Offline
Perfect for:
- Low-connectivity environments
- Travel
- High-latency networks
- On-premise / secure systems

### ✔ Private by Design
Your:
- prompts
- documents
- embeddings
- inference output

…never leave your device.

### ✔ Cross-Hardware Portability
Foundry Local automatically picks the best execution provider:
- NVIDIA GPUs (CUDA)
- Intel CPUs/GPUs (OpenVINO)
- AMD GPUs
- Qualcomm NPUs
- macOS Metal backend

The same application package works everywhere with no code changes.

### ✔ Predictable Costs
- Local inference = free.
- No API usage fees.
- No unpredictable billing.

### ✔ Simplified Developer Experience
Foundry Local handles:
- model downloads
- caching
- runtime selection
- hardware acceleration
- cross-platform packaging

So you focus on the app, not device quirks.

## 📘 What This Notebook Implements

1. Load & normalize documents (PDF)
2. Split text using LangChain text splitters
3. Create embeddings with HuggingFace
4. Build a Chroma vector store locally
5. Retrieve & rank relevant chunks
6. Load a local LLM via Azure Local Foundry Python SDK
7. Run a Retrieval-Augmented Generation (RAG) query end-to-end

Everything happens on your device.

## 🛠️ Requirements

- Windows or macOS
- Python 3.10+
- Azure Local Foundry installed
- A supported local model from Foundry Local (e.g., Qwen 2.5 0.5B)

## 🧩 Install Azure Local Foundry (Windows)

Open PowerShell and run:
```powershell
winget install Microsoft.FoundryLocal
```

That's it — no Azure subscription required.

## 📜 See Available Models

To see the quantized models supported on your device:
```bash
foundry model list
```

## ▶️ Running the Notebook

1. Install Python dependencies:
```bash
pip install -r requirements.txt
```

2. Launch Jupyter or VS Code and open the notebook.
3. Run all cells — your local RAG app will be ready in seconds.

## 🔧 How the RAG Pipeline Works

### Document Loading
PDF is loaded and split into small text chunks.

### Embedding Generation
Uses HuggingFace BGE or any other embedding model.

### Vector Store (Chroma)
Chunks are embedded + stored locally.

### Retriever
Fetches top-k similar text segments.

### Local LLM (via Azure Foundry Local)
Generates final answer grounded in retrieved documents.

All steps run on your machine — no online API calls happen.

## 🌟 Why Local RAG?

Local RAG ensures:
- No data leaks
- Instant inference
- Lower total cost
- Works in offline / edge scenarios
- Can run on almost any consumer hardware
- Cross-platform portability for developers

Foundry Local + LangChain makes local AI practical and easy.

## 🧪 Example Queries to Try

- "What defines an AI Agent?"
- "Summarize this document section."
- "Explain the key idea in simple terms."

## 📚 Resources & Reference Links

### Microsoft:
- [Foundry Local Samples](https://github.com/microsoft/foundry-local-samples)
- [How to use LangChain with Foundry Local](https://docs.microsoft.com/foundry-local/langchain)

### Other Guides:
- [Install Foundry Local (Windows/macOS)](https://docs.microsoft.com/foundry-local/install)

## 🤝 Contributing

This repository is released under the MIT License.

PRs, bug fixes, and improvements are welcome — feel free to contribute!

## 📄 License

This project is licensed under the MIT License.
