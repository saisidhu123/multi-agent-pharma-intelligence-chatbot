# Multi-Agent Pharma Intelligence Chatbot

Full-stack **multi-agent pharma intelligence chatbot** built with **React UI + FastAPI backend + cloud LLM services**.

> Resume flagship project — LangGraph supervisor agents, AWS Bedrock RAG, Cohere Rerank, DynamoDB sessions, S3 docs, RBAC, Jenkins CI/CD.

## Highlights
- **LangGraph supervisor multi-agent** routing between Structured and Unstructured agents
- **RAG** over pharma knowledge with **AWS Bedrock** retrieval + **Cohere Rerank**
- Session memory in **DynamoDB**, document storage in **S3**
- **RBAC** for secure access; **Jenkins** CI/CD pipeline
- Clean API contract between React frontend and FastAPI backend

## Tech stack
`Python` `FastAPI` `React.js` `LangGraph` `LangChain` `AWS Bedrock` `RAG` `Cohere Rerank` `S3` `DynamoDB` `RBAC` `Jenkins`

## Architecture (high level)
```
User (React UI)
    │
    ▼
FastAPI (auth / RBAC / session)
    │
    ▼
LangGraph Supervisor
   ├── Structured Agent  (tables / structured pharma data)
   └── Unstructured Agent (docs via Bedrock RAG + Cohere Rerank)
    │
    ▼
DynamoDB (sessions) · S3 (documents)
```

## Local setup (outline)
```bash
# backend
cd backend
python -m venv .venv
# Windows: .venv\Scripts\activate
pip install -r requirements.txt
uvicorn app.main:app --reload

# frontend
cd frontend
npm install
npm run dev
```

Configure AWS / Bedrock / Cohere credentials via environment variables (never commit secrets).

## Author
**Sai Sidhu Vemulapally** · [github.com/saisidhu123](https://github.com/saisidhu123) · saisidhu558@gmail.com
