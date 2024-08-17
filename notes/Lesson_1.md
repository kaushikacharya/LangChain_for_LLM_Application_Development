# Models, Prompts and Parsers

- Models
  - Language models
- Prompts
  - Style of creating inputs to pass into the models.
- Parsers
  - Taking the output of these models and parsing it into a more structured format which is utilized by the downstream tasks.

- Why use prompt templates?
  - Prompts can be long and detailed.
  - Reuse good prompts when you can!
  - Langchain also provides prompts for common operations.
    - e.g. Summarization, Question Answering, Connecting to SQL databases, Connecting to different APIs

- LangChain output parsing works with prompt templates
  - LangChain library functions parse the LLM's output
  - Assumption: LLM's output will use certain keywords
    - Example uses `Thought`, `Action`, `Observation` as keywords for Chain-of-Thought Reasoning (ReAct)
    - If you have a prompt that instructs the LLM to use these specific keywords, then this prompt can be coupled with a parser to extract out the text that has been tagged with these specific keywords.

## Notebook

- [Jupyter notebook](../code/L1-Model_prompt_parser.ipynb)
  - Tasks
    - Change style and tone of language
    - Extract product information in JSON format
- openai version: 0.27.7
  - This is the version hosted on the course's notebook.
  - The codebase in this course's notebook is based on [pre v1.0.0 migration](https://github.com/openai/openai-python/discussions/742).
