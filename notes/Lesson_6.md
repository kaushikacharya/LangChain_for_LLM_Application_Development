# Agents

- Apart from being a knowledge base, LLM can also be used as reasoning engine.
- Tools utilized in this lesson
  - `llm-math`
    - Itself a chain which uses LLM in conjunction with a calculator
  - `wikipedia`
    - [API](https://pypi.org/project/wikipedia/) connecting to Wikipedia, allowing to run search queries on Wikipedia and get search results.
- Creating custom tool
  - We should write DocString for the function so that agent understands when and how to call the function.
  - Showed how to use LLM as a reasoning engine to take different actions and connect to other functions and data sources.

## Notebook

- [Jupyter Notebook](../code/L6-Agents.ipynb)
- Note that some of the `langchain` functionalities have been moved to `langchain_experimental`. These has been changed accordingly in the notebook.
- Library requirements:
  - [numexpr](https://github.com/pydata/numexpr): Fast numerical array expression evaluator
