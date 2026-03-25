# Agent Community — Protocol & Integration Support

> Last updated: 2026-03-25
> Research for the awesome-agentic-web catalog

## Legend

- ✅ = Confirmed support (official docs/repos)
- 🔌 = Community/third-party integration exists
- ❌ = No evidence of support
- ➖ = Not applicable to this company's domain

## Protocol Support Matrix

| Company | MCP | A2A | AID | OpenAPI | WebSocket | GNAP | Other |
|---------|-----|-----|-----|---------|-----------|------|-------|
| **Cline** | ✅ Native MCP client — discovers & calls MCP servers directly from IDE | ❌ | ❌ | ❌ | ❌ | ❌ | VS Code extension API |
| **Factory** | ✅ Built-in MCP registry (40+ pre-configured servers, OAuth support) | ❌ | ❌ | ❌ | ❌ | ❌ | Droid CLI |
| **Composio** | ✅ MCP server hub (mcp.composio.dev), provider integrations for Claude/OpenAI | ❌ | ❌ | ✅ OpenAPI spec at backend.composio.dev/api/v3/openapi.json | ❌ | ❌ | 1000+ tool integrations, unified API layer |
| **Lindy** | ✅ Blog discusses MCP as natural fit; platform supports modular agent architecture | ❌ | ❌ | ✅ REST API, webhooks, sandbox environment | ❌ | ❌ | 3000+ integrations, SSO/Social login |
| **LobeHub** | ✅ MCP Servers Marketplace, full MCP plugin support (tools, resources, prompts) | ❌ | ❌ | ❌ | ❌ | ❌ | Plugin system, OpenAI-compatible API |
| **Julep AI** | ❌ | ❌ | ❌ | ✅ Builds tools from OpenAPI specs; REST API + SDKs (Python/JS) | ❌ | ❌ | Serverless workflow engine, session memory |
| **AGNT** | ❌ | ❌ | ❌ | ✅ Enterprise-grade APIs, version control for agents | ❌ | ❌ | Dynamic agent composition, multi-account platform |
| **Bitte.ai** | ❌ | ❌ | ❌ | ✅ Agents defined via OpenAPI Specification; core to architecture | ❌ | ❌ | NEAR Protocol + EVM blockchain; Bitte Runtime orchestration |
| **Operator** (OpenAI) | ✅ OpenAI Responses API supports MCP connectors (SSE + streaming HTTP) | ❌ | ❌ | ✅ OpenAI API | ✅ Realtime API via WebSocket | ❌ | Browser automation (CUA), Deep Research |
| **Apify** | ✅ Official MCP server (mcp.apify.com) — discover & run Actors via MCP | ❌ | ❌ | ✅ REST API for all platform features | ❌ | ❌ | Zapier, Make, n8n, LangChain integrations |
| **Twilio** | ✅ A2H protocol (Agent-to-Human) built on MCP tool-calling patterns | ❌ | ❌ | ✅ Extensive REST API (SMS, Voice, Video, etc.) | ✅ Media Streams WebSocket for real-time audio | ❌ | A2H (open-sourced Agent-to-Human protocol) |
| **Sourcegraph** | ✅ One of first MCP supporters; Cody uses MCP for agentic context gathering | ❌ | ❌ | ✅ GraphQL + REST API | ❌ | ❌ | Code intelligence, Cody AI assistant |
| **Langfuse** | ✅ MCP tracing support; community MCP server for observability | ❌ | ❌ | ✅ Public REST API with OpenAPI spec, SDKs (Python/JS) | ❌ | ❌ | LLM observability, prompt management |
| **Kiln AI** | ✅ Tools & MCP integration; connects MCP servers for tool calling | ❌ | ❌ | ❌ | ❌ | ❌ | Local desktop app, 100+ model support, eval framework |
| **MindsDB** | ✅ Built-in MCP server (localhost:47334/api/mcp/v1); federated data routing | ❌ | ❌ | ✅ REST API | ❌ | ❌ | SQL interface for AI, 200+ data source connectors |
| **Together AI** | ❌ | ❌ | ❌ | ✅ OpenAI-compatible API (chat, vision, images, embeddings, speech) | ❌ | ❌ | Inference platform, open-source model hosting |
| **Ollama** | 🔌 Community MCP servers & clients exist (not native) | ❌ | ❌ | ✅ REST API + OpenAI-compatible endpoint (Responses API supported) | ❌ | ❌ | Local LLM runtime, model library |
| **Brave** | ✅ Official brave-search-mcp-server on GitHub | ❌ | ❌ | ✅ Brave Search REST API | ❌ | ❌ | Search, local, image, video, news, AI summary |
| **Vapi** | ✅ MCP integration for assistants + Vapi MCP Server (mcp.vapi.ai) | ❌ | ❌ | ✅ REST API for calls, assistants, tools | ✅ WebSocket transport for real-time bidirectional audio | ❌ | Voice AI platform, phone/web/mobile SDKs |
| **Paperclip** | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ Works with GNAP via OpenClaw ecosystem | Agent orchestration for zero-human companies; governance, cost monitoring |
| **A1Base** | ❌ | ❌ | ✅ Agent Identity & Discovery — core product (verified agent identity, phone, email) | ✅ REST API for agent communication | ❌ | ❌ | WhatsApp, SMS, email, Discord, Telegram channels; anti-spam |
| **SWARM Protocol** | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | Custom: Truth Protocol — decentralized AI-agent swarms with ZK proofs, consensus verification, on-chain settlement |
| **Agent Relay** | ❌ | ❌ | ❌ | ❌ | ✅ Real-time WebSocket messaging between agents | ❌ | Custom: Channel-based agent-to-agent messaging; SDK (Python/JS/TS); spawns Claude/GPT agents into shared channels |

## Key Observations

### MCP Dominance
MCP (Model Context Protocol) is the most widely adopted standard — **16 out of 23 companies** have some form of MCP support. It has become the de facto standard for agent-to-tool communication.

### A2A Still Emerging
Despite Google's A2A protocol gaining attention, **none of the surveyed companies have implemented it yet** as a primary integration. It remains complementary to MCP rather than competitive.

### AID (Agent Identity)
A1Base is the **only company** focused specifically on agent identity and discovery, providing verified identities for AI agents across communication channels.

### GNAP
GNAP (Git-Native Agent Protocol) is used within the **OpenClaw/Paperclip ecosystem** for agent task coordination via git repos. It's a niche but practical protocol for agent orchestration.

### OpenAPI as Foundation
**14 out of 23 companies** offer REST APIs, with many using OpenAPI specifications. This remains the baseline for programmatic access, though MCP is rapidly becoming the preferred AI-native interface layer on top.

### WebSocket for Real-Time
WebSocket support is limited to companies with **real-time communication needs**: Vapi (voice), Twilio (audio streams), Operator (realtime API), and Agent Relay (agent messaging).

### Protocol Convergence Pattern
The emerging pattern is: **OpenAPI (foundation) → MCP (AI-native tool layer) → A2A (future agent-to-agent)**. Most companies are at the MCP adoption stage.

## Sources
- Official documentation sites for each company
- GitHub repositories (official MCP servers)
- Brave Search API research (March 2026)
- Company blog posts and developer guides
