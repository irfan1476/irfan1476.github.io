Platforms & models (last 6 months)

OpenAI

GPT‑5 launched Aug 7 (consumer + developer), with new safety/system docs. 

o3 & o4‑mini (Apr–Jun): smaller/faster reasoning variants; strong AIME results; in API. 

Realtime API for low‑latency voice/screen experiences; now supported via Azure as well. 

Project‑only Memory (Aug 22): enterprise‑friendly scoped memory for ChatGPT/Projects. 


Anthropic

Claude Opus 4.1 (Aug 5): upgrades coding/agentic tasks; expanded availability (API, Bedrock, Vertex). Sonnet 4 now supports 1M‑token context (Aug 12). 

New safeguard: models can end rare abusive chats (Aug 15). 


Google

Gemini Live upgrades: camera/screen‑share with visual guidance + deeper Android app integration (Aug 2025; I/O updates in May). 

Vertex AI Agent Engine: VPC/CMEK security features (Aug 21). Memory Bank preview (July 8). 


Meta (open source)

Llama 4 announced Apr 5 with new multimodal directions. 


Alibaba / Qwen

Qwen3 models updated July 2025 (thinking & instruct variants). 


Mistral

Product cadence continues; “Deep Research (preview) + Audio‑in, Projects” (July 17). Docs also note small new reasoning models in 2025. 


GitHub Copilot (adoption signal)

20 million users; enterprise customers +75% QoQ; 90% of Fortune 100 use Copilot (Jul 30). 



Agent interoperability & memory (new foundations)

Agent‑to‑Agent (A2A) moved to Linux Foundation (June 23): vendor‑neutral standard for secure agent comms; AWS is implementing/evangelizing. 

Model Context Protocol (MCP) roadmap refreshed (July 22) with near‑term priorities; growing enterprise interest. 

OpenAI Project‑only Memory (Aug 22) and Vertex Memory Bank (July 8) make “remembering” safe & scoped. 


What stacks are actually shipping (reference architectures you can teach)

RAG at scale, cheaper

Amazon S3 Vectors (preview): native vector store in S3 (up to ~90% lower cost vs conventional setups), plugs straight into Bedrock Knowledge Bases; AWS published hands‑on “how‑to” guides. 

Vertex AI Vector Search remains the high‑scale managed option on GCP (recent guidance). 


Enterprise agents (governed, multi‑tool)

Amazon Bedrock AgentCore (preview): identity/permissions for agents, a Gateway to expose your APIs as tools (MCP support), managed Browser Tool, plus observability—designed to run multi‑agent workflows. 

Azure AI Agent Service: public‑preview updates incl. Java SDK and built‑in tools (Search grounding, Functions, Code Interpreter). 

Vertex AI Agent Engine: private networking (PSC) + CMEK, aligning with enterprise security baselines. 


Realtime, multimodal assistants

OpenAI Realtime API (and Azure support) for voice+screen agent UX; Gemini Live for camera/screen “show me” interactions. 


Inference & deployment

NVIDIA NIM: prebuilt inference microservices; recent add‑ons include FLUX.1 image‑editing NIM (Aug 13). 

vLLM keeps pushing serving throughput (V1 architecture announced Jan; active releases Aug). Ollama added tool‑calling + multimodal engine in May for local stacks. 



Orchestration & build frameworks (actively used in industry)

LangGraph (LangChain): stateful, graph‑based multi‑agent orchestration (handoffs, retries, per‑node memory). AWS shows how to pair LangGraph with Bedrock in production patterns. 

Microsoft AutoGen (0.4 line): event‑driven, scalable multi‑agent framework from MSR; continued updates this year. 

LlamaIndex: complements the above when data connectivity/RAG is the focus (see recent comparisons). 

