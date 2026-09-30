# SCARCE-Bench: Project Specification & Budget Breakdown

## Executive Summary
This document outlines the scope, budget, and execution roadmap for SCARCE-Bench during a 12-week technical research sprint ($20,000 total funding).

---

## Itemized Budget Allocation

| Category | Amount | Technical Scope & Justification |
| :--- | :--- | :--- |
| **Lead Researcher Stipend** | **$11,000** | Full-time execution (12 weeks @ 40 hrs/wk / ~$3,666/mo) to finalize 150 prompts, write Python test harnesses, run 2,250 evaluations, perform statistical analysis, and author the empirical report. |
| **Frontier Model API Tokens** | **$4,000** | 2,250 multi-step evaluation calls, embedding generations, dense RAG queries, and red-teaming iterations across GPT-4, Claude, Gemini, and Llama flagship endpoints. |
| **External Expert Validation** | **$3,000** | Honorariums ($100–$150/hr) to recruit and compensate specialist archivists, domain experts, and secondary evaluators for double-coding and inter-rater reliability. |
| **Cloud Vector Infrastructure** | **$1,000** | 3 months of hosted vector database infrastructure (Pinecone and AWS Bedrock) and proxy evaluation environments. |
| **Repository Tooling & Dissemination** | **$1,000** | Hugging Face dataset formatting, interactive Gradio demo hosting on Hugging Face Spaces, GitHub documentation, and release materials. |

---

## 12-Week Execution Roadmap
* **Weeks 1–2:** Finalize 150-prompt dataset and configure Pinecone/AWS Bedrock vector retrieval baseline.
* **Weeks 3–4:** Build Python evaluation harnesses and system prompt testing frameworks for all 4 LLM families.
* **Weeks 5–7:** Execute 2,250 evaluation runs across API endpoints and log raw response completions.
* **Weeks 8–9:** Conduct blinded primary scoring and recruit expert archivists for secondary double-coding.
* **Week 10:** Calculate inter-rater reliability ($Krippendorff's \alpha$) and resolve scoring disagreements.
* **Week 11:** Build interactive Gradio demo interface and format public Hugging Face dataset.
* **Week 12:** Publish final empirical research report and release open-source evaluation toolkit.
