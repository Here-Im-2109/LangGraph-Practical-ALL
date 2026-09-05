# LangGraph Practical Workflows

This repository contains a collection of practical LangGraph examples that demonstrate how to build structured AI workflows using Python, LangChain, and modern LLM providers.

The notebooks in this folder are designed to help you understand and experiment with agentic patterns such as:

- simple single-step LLM workflows
- prompt chaining
- parallel execution
- content moderation
- review loops
- iterative optimization
- state-based workflow orchestration

---

## Project Overview

LangGraph is used to model workflows as graphs where each node performs a task and passes state between steps. This project is a hands-on learning set for building multi-step AI systems with clear control flow and state transitions.

Each notebook focuses on a different pattern and serves as a practical example of how to move from a basic prompt to a reusable workflow graph.

---

## Folder Structure

- `1_Temperature_Conversion_workflow.ipynb` – converts temperature values using a simple workflow graph
- `2_Simple_QA_LLM_Workflow.ipynb` – basic question-answering workflow using an LLM
- `3_Prompt_Chaining_Workflow.ipynb` – chained prompts for multi-step reasoning or transformation
- `4_Parallal_workflow.ipynb` – demonstrates branching and parallel task execution
- `5_Essay_Parallel_workflow.ipynb` – parallel generation of essay-related outputs
- `6_Content_Moderation_Workflow.ipynb` – checks and filters content using a moderation-style workflow
- `7_Review_workflow.ipynb` – review and feedback loop for generated output
- `8_Iterative_Workflows.ipynb` – iterative improvement workflow with evaluation and optimization loops
- `requirements.txt` – Python package dependencies

---

## Tech Stack

This project uses:

- Python
- LangGraph
- LangChain
- OpenAI API
- Groq API
- Google Gemini API
- Python dotenv for environment variable management

---

## Prerequisites

Before running the notebooks, make sure you have:

- Python 3.10+ installed
- An active virtual environment (recommended)
- API keys for the model provider(s) you plan to use
- Jupyter Notebook or VS Code with notebook support

---

## Setup

1. Clone the repository
2. Create and activate a virtual environment

```bash
conda create -p name_of_the_env python=3.11 -y
```

On Windows or ubuntu:

```bash
conda activate name_of_the_env
```


3. Install dependencies

```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root with your API keys:

```env
OPENAI_API_KEY=your_openai_key_here
GROQ_API_KEY=your_groq_key_here
GOOGLE_API_KEY=your_google_api_key_here
```

> The notebooks may use different model providers depending on the example. You only need to configure the keys for the providers you plan to test.

---

## Run the Notebooks

You can run the notebooks in either of these ways:

```bash
jupyter notebook
```

or

```bash
jupyter lab
```

Then open any `.ipynb` file from this folder and run the cells in order.

---

## Common Workflow Pattern

Most notebooks follow this pattern:

1. Load environment variables
2. Initialize one or more LLMs
3. Define the workflow graph using `StateGraph`
4. Add nodes for processing, evaluation, or transformation
5. Connect the nodes using `START` and `END`
6. Compile and execute the graph

This structure makes it easy to build reusable, controllable AI pipelines.

---

## Learning Goals

This project is intended to help you learn:

- how to create LangGraph state graphs
- how to model multi-step AI flows
- how to pass state between workflow nodes
- how to design parallel and iterative processes
- how to use different LLM providers with the same workflow patterns

---

## Notes

- Some notebooks may require API access to external LLM providers.
- If a model call fails, check your environment variables and API key validity.
- The code is meant for learning and experimentation, so feel free to modify and extend the workflows.

---

## License

This project is for educational and learning purposes. Add your preferred license if you plan to share or distribute it publicly.

---

## Suggested Next Steps

- Try modifying the prompts to improve output quality
- Add logging and tracing around each workflow node
- Replace one provider with another to compare performance
- Build your own domain-specific workflow on top of these examples

---

## Author

This folder is a practical LangGraph learning project for building intelligent, stateful AI workflows with Python.