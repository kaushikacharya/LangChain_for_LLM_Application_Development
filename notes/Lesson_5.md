# Evaluating LLM Applications

- Manually we can create question-answer pairs from the document.
- To scale this we can automate Q&A generation using `QAGenerateChain`.
  - It uses LLM to generate Q&A.
- What's actually happening inside the chain?
  - What is the actual prompt?
  - What are the documents that it retrieves?
  - For complex chain with multiple steps, what are the intermediate results?
- Solution
  - `import langchain`
  - `langchain.debug = True`
- In Q&A, often times when a wrong result is returned, it's not necessarily the language model that's messing up but it's  the retrieval step that's messing up.
- LangChain evaluation platform

## Notebook

- Here we will evaluate chain from [previous lesson](./Lesson_4.md#notebook)
- Issue faced:
  - LLM-generated Q&A examples under the key: `qa_pairs`
    - `{'qa_pairs': {'query': <query>, 'answer': <answer>}}`
    - Correction done on the notebook by me to handle this issue.
  - LangChain Plus seems to be no more accessible.
