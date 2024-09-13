# DBF-Assistant Info

We implement a knowledge-based application named DBF-Assistant to assist developers in understanding and fixing DBFs.

## Workflow overview
![image](https://github.com/user-attachments/assets/70fbda87-12d9-422f-b472-408449bb642f)

DBF-Assistant involves the interaction with developers through a chat interface (i.e., front-end module), which ensures that the interaction is conversational and user-friendly. DBF-Assistant’s back-end module engages in a multi-stage process to provide a valuable answer: 

- Stage-1. Knowledge preparation: DBF-Assistant utilizes a Text splitter to break down and process the original DBF knowledge documents into smaller, more manageable chunks. Then, these chunks are subsequently converted into embeddings and stored in a vector database. This preparation is essential for efficient knowledge retrieval and interaction. Note that this stage is operated only once at the beginning and the knowledge can be updated subsequently.
- Stage-2. Knowledge retrieval: After a query being initiated, DBF-Assistant uses the Embedding model and Vector DB to interpret the query, semantically search for relevant context within the knowledge base, and rank contexts based on their relevance to the input query.
- Stage-3. Response generation: Once relevant context is identified, DBF-Assistant formulates a model input that combines system prompt, query, and retrieved context. The model input is then processed through a pretrained LLM, providing LLM with a more comprehensive understanding of the domain-specific knowledge. Then, LLM uses its in-context learning abilities to generate a coherent and contextually appropriate response. Finally, the response is sent back to the developer through the chat interface.

## Setup instructions
DBF-Assistant is implemented in Dify and Ollama frameworks. The detaied setup instructions can be found in `setup_instructions.md`

- The framework code can be found in `docker` folder
- The MLOps knowledge documents can be found in `documents` folder

## Snapshot
![1726235130(1)](https://github.com/user-attachments/assets/31f32765-6569-4df9-81e3-fcd90fd73471)

![1726235085(1)](https://github.com/user-attachments/assets/c3262bfc-930b-4d34-b20e-d904b988906e)

