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

## Additional Resources (KA)

- Retrievers
  - [LangChain documentation](https://python.langchain.com/docs/modules/data_connection/retrievers/) defines it as an interface that returns documents given an unstructured query.
  - [LangChain blog](https://blog.langchain.dev/retrieval/) mentions variations in retrieval step apart from Semantic Search:
    - Optimizing maximal marginal relevance
    - Graph based indexing
  - [Andrej Karpathy](https://github.com/karpathy/randomfun/blob/master/knn_vs_svm.ipynb) advocates using SVM instead of KNN.
