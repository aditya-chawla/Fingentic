# Fingentic – Agentic AI for Financial Exploration

**Fingentic** is a voice- and text-enabled AI assistant that helps non-technical users — like students, journalists, and amateur investors — explore company data, stock prices, and financial trends using natural language.

Whether you're asking:
- “Who are the top energy companies in Japan?”
- “Plot Tesla’s price trend over the last 2 weeks”
- “What’s Apple’s profit and who is their CEO?”

Fingentic provides clear, data-driven answers using charts, tables, or high-quality reference summaries — no coding, no SQL, just curiosity.

---

## What It Does

Fingentic uses agentic AI orchestration to route your question to the right tool:
- SQL queries over the Forbes financial database (SQLite)
- Stock charting using Yahoo Finance
- Real-time prices via Finnhub API
- Web-based RAG (DuckDuckGo) for CEO bios and company descriptions with source links

Users can interact via:
- Text input
- Voice input (powered by Whisper)

Behind the scenes, it uses Gemma-27B to classify queries, generate SQL, extract tickers, and summarize financial responses using Langraph workflows.

---

## Responsible and Secure by Design

Fingentic is built with responsibility in mind:
- It includes protection against SQL prompt injection attacks.
- Each query is checked through guardrails and intent validation.
- When using external sources, the assistant cites reliable web links and summaries, ensuring transparency and traceability.

These features make it safe for use in journalism, academics, and financial analysis.

---

## How It Works

1. You ask a question — in voice or text.
2. The assistant classifies it (SQL, chart, price, or web search).
3. It runs the right tool — generates SQL, fetches API data, or performs a web search.
4. Results are shown as clear responses, visuals, or trusted source summaries.

Fingentic also handles fallback scenarios when data is missing or ambiguous, switching tools intelligently.

---

## Built With

- Languages: Python
- LLMs: Gemma-27B, Mistral-7B (via Together AI)
- UI: Gradio
- Speech Input: Whisper
- Data: Forbes 2000 CSV in SQLite
- APIs: yFinance, Finnhub, DuckDuckGo
- Libraries: pandas, matplotlib, PIL


