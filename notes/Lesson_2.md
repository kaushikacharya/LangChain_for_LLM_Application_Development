# Memory

- Basically how do you remember previous parts of the conversation and feed that into the language model so that they can have this conversational flow as you're interacting with them.
- Large Language Models are **"stateless"**.
  - Each transaction is independent.
- Chatbots appear to have memory by providing the full conversation as "context".
  - But this becomes expensive as LLMs charge per token basis.
- LangChain provides several convenient kinds of "memory" to store and accumulate the conversation.

- Memory Types
  - [ConversationBufferWindowMemory](https://python.langchain.com/docs/modules/memory/types/buffer_window/)
  - [ConversationTokenBufferMemory](https://python.langchain.com/docs/modules/memory/types/token_buffer/)
    - We need to pass LLM as input parameter as different LLMs compute the token count differently.
    - Utilizes [tiktoken](https://github.com/openai/tiktoken): a fast Byte Pair Encoding tokenizer
  - [ConversationSummaryBufferMemory](https://python.langchain.com/docs/modules/memory/types/summary_buffer/)

- Additional Memory Types
  - Vector Data Memory
    - Stores text (from conversation or elsewhere) in a vector database and retrieves the most relevant blocks of text.
  - Entity memories
    - Using an LLM, it remembers details about specific entities.

- Multiple memories can also be used at one time.
  - e.g. Conversation memory + entity memory to recall individuals.
- Conversation can also be stored in a conventional database (e.g. key-value store or SQL).

## Notebook

- [Jupyter Notebook](../code/L2-Memory.ipynb)
