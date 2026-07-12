# Agentic RAG with LangGraph 🦜🔍

Implementation of Reflective RAG, Self-RAG & Adaptive RAG tailored towards developers and production-oriented applications for learning LangGraph🦜🕸️.

This repository contains a refactored version of the original [LangChain's Cookbook](https://github.com/mistralai/cookbook/tree/main/third_party/langchain),

See Original YouTube video:[Advance RAG control flow with Mistral and LangChain](https://www.youtube.com/watch?v=sgnrL7yo1TE)

of [Sophia Young](https://x.com/sophiamyang) from Mistral & [Lance Martin](https://x.com/RLanceMartin) from LangChain

![Logo](static/Langgraph%20Adaptive%20Rag.png)


## Features

- **Refactored Notebooks**: The original LangChain notebooks have been refactored to enhance readability, maintainability, and usability for developers.
- **Production-Oriented**: The codebase is designed with a focus on production readiness, allowing developers to seamlessly transition from experimentation to deployment.
- **Test Coverage**: Comprehensive test coverage ensures the reliability and stability of the application, enabling developers to validate their implementations effectively.
- **Documentation**: Detailed documentation and branches guides developers through setting up the environment, understanding the codebase, and utilizing LangGraph effectively.


## What You'll Learn

- **Agentic RAG Implementation**: Build a system that can make intelligent decisions about retrieving information
- **Graph-Based Control Flow**: Use LangGraph to create sophisticated control flows for your RAG pipeline
- **Document Relevance Evaluation**: Implement logic to grade document relevance and detect hallucinations
- **Adaptive Information Retrieval**: Create a system that can switch between local knowledge and web search
- **State Management**: Implement proper state handling for complex information flows

## Tutorial Structure

This repository is organized as a series of commits, each representing a video lesson in building the Agentic RAG system:

| Lesson # | Commit | Description | Key Components |
|----------|--------|-------------|----------------|
| 1 | `5b2b18e` **Start Here** | Introduction to the course and Agentic RAG concepts | Overview of the project; Introduction to LangGraph and Agentic RAG architecture |
| 2 | `2693185` **Project Structure** | Setting up the project foundation | Initialize project structure; Configure Poetry for dependency management |
| 3 | `513e3cf` **Ingestion** | Setting up the vector database | Create ingestion pipeline; Implement vector store with Chroma and OpenAI embeddings |
| 4 | `03f79ae` **State** | Defining the state management | Create GraphState class; Set up typed dictionaries for state tracking |
| 5 | `c2d71c7` **Retrieve Node** | Implementing the document retrieval | Build retrieve node; Connect retrieval to vector database |
| 6 | `9107e7a` **Grade Documents Node** | Evaluating document relevance | Create document grading functionality; Implement decision logic for document relevance |
| 7 | `6d4fdc4` **Web Search with Tavily** | Adding external search capability | Integrate Tavily search API; Implement fallback for insufficient local knowledge |
| 8 | `bc57b63` **Generation Node** | Creating the answer generation component | Build generate node; Implement context-aware response generation |
| 9 | `a450f9b` **Graph** | Constructing the complete LangGraph workflow | Connect all nodes into workflow; Implement conditional edges for adaptive behavior |
| 10 | `5400fb7` **Self-RAG** | Adding self-evaluation capabilities | Implement hallucination detection; Create feedback loops for answer improvement |
| 11 | `034e53f` **Router** | Smart query routing | Create intelligent routing between retrieval and web search; Optimize entry point for different query types |
| 12 | `d9490ca` **Formatting** | Final code formatting and cleanup | Code optimization; Final documentation improvements |

## Environment Variables

To run this project, you will need to add the following environment variables to your .env file:

```bash
OPENAI_API_KEY=your_openai_api_key_here
TAVILY_API_KEY=your_tavily_api_key_here  # For web search capabilities
LANGCHAIN_API_KEY=your_langchain_api_key_here  # Optional, for tracing
LANGCHAIN_TRACING_V2=true                      # Optional
LANGCHAIN_PROJECT=agentic-rag                  # Optional
```

> **Important Note**: If you enable tracing by setting `LANGCHAIN_TRACING_V2=true`, you must have a valid LangSmith API key set in `LANGCHAIN_API_KEY`. Without a valid API key, the application will throw an error.

## Getting Started

Clone the repository:

```bash
git clone https://github.com/siddhartxts/lang_graph.git
cd lang_graph
git checkout project/agentic-rag
```

Install dependencies:

```bash
uv sync
```

Follow along with each commit to learn the process of building an Agentic RAG system:

```bash
# View all commits in the tutorial
git log --oneline

# Check out specific lessons:
git checkout 5b2b18e  # Lesson 1: Start Here
git checkout 2693185  # Lesson 2: Project Structure
git checkout 513e3cf  # Lesson 3: Ingestion
git checkout 03f79ae  # Lesson 4: State
git checkout c2d71c7  # Lesson 5: Retrieve Node
```

## Prerequisites

- Python 3.10+
- Basic understanding of LLMs and RAG systems
- Familiarity with Python and vector databases (helpful but not required)

## Run Locally

Clone the project

```bash
  git clone https://github.com/siddhartxts/lang_graph.git
```

Go to the project directory

```bash
  cd lang_graph
```

Install dependencies

```bash
  uv sync
```

Start the Agentic Rag flow

```bash
  uv run python main.py
```

## Running Tests

To run tests, run the following command

```bash
  uv run pytest . -s -v
```
## Acknowledgements

Original LangChain repository: [LangChain Cookbook](https://github.com/mistralai/cookbook/tree/main/third_party/langchain)
By [Sophia Young](https://x.com/sophiamyang) from Mistral & [Lance Martin](https://x.com/RLanceMartin) from LangChain
![Logo](static/LangChain-logo.png)



