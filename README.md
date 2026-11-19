# Hi, I'm Sajib Sarker 👋

**Full-Stack & Backend Engineer · DevOps · AI Platform**

I build scalable SaaS platforms, serverless systems, and cloud infrastructure, and I'm now focused on AI platform engineering (RAG, vector search, LLM integration, streaming, cost and latency measurement). Open to remote roles.

📍 Bangladesh (Remote) · 🔗 [LinkedIn](https://linkedin.com/in/sajibs1104003) · ✉️ sajibsarker1104003@gmail.com 
[Professional Github](https://github.com/ssarker-coder-ops)

---

## 🤖 AI & Platform Engineering

- **RAG services:** document ingestion, embeddings, vector similarity search, and LLM-backed answers
- **Retrieval quality and cost control:** distance-threshold filtering so unrelated questions never reach the LLM (no token cost), and request validation on the API
- **Streaming responses:** token-by-token answers over Server-Sent Events, with JWT auth and error handling kept intact and upstream LLM calls cancelled on client disconnect
- **Cost and latency measurement:** per-request token usage, time to first token and latency, plus a baseline script for P50/P95 latency and cost per query
- **Vector databases:** PostgreSQL + pgvector
- **Embeddings:** self-hosted embedding models (1024-dim) alongside hosted LLM providers such as Groq
- **AI integration:** shipping AI-powered services behind production backend APIs
- **Secure access:** JWT authentication, separated user and document databases
- **Engineering docs:** architecture docs, ADRs, and benchmark notes alongside the code

### ⭐ Featured: [nest-rag-service](https://github.com/sajibsarker-1104003/nest-rag-service)

A NestJS Retrieval-Augmented Generation service with pgvector, local embeddings, JWT auth, SSE streaming, and a similarity threshold. First baseline on a small test set: about 0.8 s median latency and under $0.0001 per query.

```mermaid
flowchart LR
    C[Client] --> API[NestJS API<br/>JWT auth + validation]
    API --> U[(Users DB)]
    API --> E[Embedding model]
    E --> V[(Docs DB<br/>pgvector)]
    V -->|distance filter| API
    API --> L[LLM provider<br/>Groq]
    L -->|SSE tokens + usage| API
    API -->|SSE stream| C
```

**Stack:** NestJS · Prisma · PostgreSQL · pgvector · JWT · SSE · Vitest

---

## 🔧 Skills

| Area | Technologies |
|---|---|
| **Languages** | TypeScript, JavaScript, C#, C, Python, Bash |
| **Backend** | NestJS, Express, Node.js, Microsoft .NET, REST APIs, Server-Sent Events, Domain-Driven Design |
| **Frontend** | React, Next.js |
| **AI / Data** | RAG, pgvector, embeddings, LLM integration, streaming, similarity thresholds, cost and latency benchmarking |
| **ORM** | Prisma, Entity Framework, Sequelize, Mongoose, MongoDB .NET Driver |
| **Databases** | PostgreSQL, MySQL, MongoDB, Redis, DynamoDB, S3 |
| **Cloud** | AWS (Lambda, API Gateway, Fargate, ECR, VPC), Azure |
| **Infrastructure as Code** | Terraform, CloudFormation |
| **Containers** | Docker, Kubernetes |
| **CI/CD** | GitHub Actions, Jenkins |
| **Monitoring** | ELK, Datadog |
| **Testing** | Jest, Vitest |
| **Collaboration** | Jira, Confluence, Slack |

---

## 💼 What I've Built

- **Risk Management SaaS platform:** led backend and cloud automation across Enterprise, Project, Audit, Compliance, Cybersecurity, and Incident Management modules (NestJS, .NET, Prisma, PostgreSQL, DDD).
- **Serverless on AWS:** provisioned infrastructure with Terraform and built cost-efficient, secure architectures on Lambda and API Gateway.
- **Microservices:** containerized services with Docker and ran them on Kubernetes and AWS Fargate with automated deployment and scaling.
- **CI/CD:** built GitHub Actions pipelines for testing, integration, and releases.
- **Performance:** added Redis caching to cut database load and latency.
- **Cloud networking:** designed secure AWS VPC environments with planned subnets and security groups.
- **Full-stack SaaS:** shipped an event-based SaaS product with NestJS, Next.js, serverless payment endpoints, and Terraform.
- **AI and blockchain integrations:** delivered AI-powered services and blockchain-based authentication behind backend APIs.
- **RAG service with streaming:** built a NestJS RAG API with pgvector and local embeddings, added SSE streaming, a distance threshold that skips the LLM for unrelated questions, and per-request token, cost and latency metrics, and documented the decisions in ADRs.

---

## 🌱 Currently

Building and open-sourcing AI platform projects (next: document chunking, vector index, document ownership, an evaluation set, then agents and observability), and sharpening my full-stack and DevOps portfolio. Looking for **Backend, Full-Stack, DevOps, or AI Platform Engineer** roles.

Let's connect, I'm always happy to talk about SaaS, cloud automation, and AI systems.
