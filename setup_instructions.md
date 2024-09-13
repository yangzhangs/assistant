## DBF-Assistant Setup Instructions
DBF-Assistant leverages the Large Language Model (LLM) and Retrieval Augmented Generation (RAG) to incorporate DBF knowledge to better answer developers’ questions about DBFs.

### Components: 
- Use [Ollama](https://ollama.com/) to upport tool calling with LLM models.
- Use [Nomic Embed model](https://ollama.com/library/nomic-embed-text) to generate embeddings.
- Use [Google’s Gemma 2 model](https://ollama.com/library/gemma2) to learn knowledge and generate response.
- Use open source framework [Dify](https://github.com/langgenius/dify) to manage models and DBF knowledge.

### Instructions:
- Download the `docker` folder to local machine
- Copy the environment configuation file: `cp .env.example .env`
- Start the Docker containers: `docker compose up -d`
- Access web interface: `http://localhost` or `http://your_server_ip`
- Download Ollama: Visit https://ollama.ai/download to download the Ollama client for your system
- Run Ollama: `ollama run llava`
- Ollama starts an API service on local port 11434, which can be accessed at `http://localhost:11434`
- Integrate Ollama, configure Google’s Gemma 2 model and Nomic Embed model
- Go to the `documents` folder, upload our DBF knowledge documents to the `Knowledge base` of Dify
- Segment and clean the document, and preview the effect
- Wait for the chunks to be embedded
- Define system configuration and load MLOps knowledge
- Deploy the agent
