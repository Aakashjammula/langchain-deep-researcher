# LangChain Deep Research

## Overview
This project leverages LangChain and langgraph to perform deep research on any topic. it will generate a web search query, gather web search results (via Duckduckgo), summarize the results of web search, reflect on the summary to examine knowledge gaps, generate a new search query to address the gaps, search, and improve the summary for a user-defined number of cycles. It will provide the user a final markdown summary with all sources used.

## Features
- **Automated Web Research**: Uses DuckDuckGo search to fetch relevant web pages.
- **LLM-Powered Analysis**: Processes and refines search results using Google Generative AI (`gemini-2.0-flash`) or any local llm using ollama.
- **Data Deduplication & Formatting**: Ensures clean and structured output.
- **Graph-Based Processing**: Uses LangGraph to manage workflows.

## Requirements
Install dependencies using:
```bash
pip install langchain_core langchain_ollama langgraph duckduckgo_search langsmith beautifulsoup4 langchain_google_genai
```
## How It Works
- Given a user-provided topic, use a local LLM (via Ollama) or any llm using api ( in this case google) to generate a web search query

- Uses a search engine DuckDuckGo to find relevant sources

- Uses LLM to summarize the findings from web search related to the user-provided research topic Then, it uses the LLM to reflect on the summary, identifying knowledge gaps

- It generates a new search query to address the knowledge gaps

- The process repeats, with the summary being iteratively updated with new information from web search

## Usage
Run the notebook to:
1. Set up the LLM and search tools.
2. Generate a research query.
3. Fetch and process web search results.
4. Deduplicate and format extracted data.

## Customization
- Modify `max_web_research_loops` for search depth.
- Change the `llm` model in the code to switch between Gemini and Ollama.

## License
MIT License

