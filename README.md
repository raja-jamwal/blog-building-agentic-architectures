# Building Agents in Python and n8n (2026 Edition)

[![Blog](https://img.shields.io/badge/Read_on-Substack-orange?style=for-the-badge&logo=substack)](https://rajajamwal.substack.com/p/building-agents-in-python-and-n8n)
[![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/LangChain-LCEL-green?style=for-the-badge)](https://www.langchain.com/)
[![LangGraph](https://img.shields.io/badge/LangGraph-Stateful-red?style=for-the-badge)](https://langchain-ai.github.io/langgraph/)

This repository is the code companion to the **"Building Agents in Python and n8n"** blog series. 

It contains a complete curriculum of **21 Agentic Design Patterns**, taking you from basic prompt chaining to complex, self-correcting multi-agent swarms using **LangChain** and **LangGraph**. While the code is written in Python, every pattern includes conceptual mappings for implementing the same logic in **n8n**.

## 📂 Repository Structure

The curriculum is divided into two main modules: **LangChain (The Patterns)** and **LangGraph (The Architecture)**.

### Module 1: LangChain (The Foundation)
Located in `/langchain`, these notebooks cover the fundamental building blocks of agentic reasoning.

| Part | Title | Key Patterns Covered |
| :--- | :--- | :--- |
| **01** | **The Foundation** | • **Prompt Chaining:** Sequential pipelines.<br>• **Routing:** Conditional logic (If/Else).<br>• **Parallelization:** Running tasks simultaneously. |
| **02** | **Reasoning & Tools** | • **Reflection:** Self-correction loops.<br>• **Tool Use:** Connecting LLMs to functions.<br>• **Planning:** Chain-of-Thought architecture. |
| **03** | **Context & Learning** | • **Multi-Agent Collaboration:** Researcher + Writer flows.<br>• **Memory:** Managing conversation history.<br>• **Few-Shot Learning:** Teaching via examples. |
| **04** | **Infrastructure** | • **MCP (Model Context Protocol):** Standardized tool connections.<br>• **Goal Setting:** Loops that run until success.<br>• **Exception Handling:** Graceful fallbacks. |
| **05** | **Trust & Connection** | • **Human-in-the-Loop (HITL):** Approval gates.<br>• **RAG:** Retrieval-Augmented Generation.<br>• **Inter-Agent Comm:** Agent-to-Agent webhooks. |
| **06** | **Safety & Optimization** | • **Resource Awareness:** Dynamic routing (Cheap vs. Expensive models).<br>• **Reasoning:** Chain of Thought (CoT).<br>• **Guardrails:** Pydantic structured outputs. |
| **07** | **Strategy** | • **Evaluation:** LLM-as-a-Judge pipelines.<br>• **Prioritization:** Automated triage systems.<br>• **Exploration:** Proactive discovery agents. |

### Module 2: LangGraph (The Architecture)
Located in `/langgraph`, these notebooks move beyond linear chains into cyclic state graphs.

| Part | Title | Architecture Built |
| :--- | :--- | :--- |
| **01** | **State Machines** | Building a **Self-Correcting Agent** with explicit memory and Human-in-the-Loop interrupts using `StateGraph`. |
| **02** | **Multi-Agent Systems** | Building a **Hierarchical Supervisor** architecture where a "Manager" LLM delegates tasks to "Worker" agents (Researcher, Coder). |

---

## 🚀 Getting Started

### Prerequisites
*   Python 3.10+
*   An OpenAI API Key

### Installation

You can directly run any of the file by forking in google collab. Each one is a complete script.

### Running the Code
The files are provided as Jupyter Notebooks (`.ipynb`). You can run them using:
*   VS Code (Recommended)
*   Jupyter Lab
*   Google Colab (Badges included in files)

---

## ⚡ The n8n Connection

If you are following the series to build in **n8n**, use this repository as your logic reference. The notebooks explain *how* the data flows.

**Common Mappings:**
*   **Chaining** $\rightarrow$ Connecting n8n nodes linearly.
*   **Routing** $\rightarrow$ `Switch` or `If` Node.
*   **Parallelization** $\rightarrow$ Multiple outputs merging into a `Merge` Node.
*   **Tools** $\rightarrow$ `AI Agent` Node connected to `HTTP Request` or `Calculator` tools.
*   **Memory** $\rightarrow$ `Window Buffer Memory` Node.
*   **HITL** $\rightarrow$ `Wait` Node (Wait for Webhook).
*   **Supervisor** $\rightarrow$ An `AI Agent` node configured to output JSON routing decisions.

## 📚 Resources

*   **Blog Series:** [Subscribe on Substack](https://rajajamwal.substack.com)
*   **LangChain Docs:** [python.langchain.com](https://python.langchain.com)
*   **LangGraph Docs:** [langchain-ai.github.io/langgraph](https://langchain-ai.github.io/langgraph/)

---

*Created by Raja Jamwal. Star the repo if you found it useful!* ⭐
