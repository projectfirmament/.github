# Project Firmament

**Enterprise AI Venture Studio OS** — orchestrating multiple businesses through a hierarchy of AI agents on dedicated hardware.

## Architecture

```
Client (Twenty.com) → Altitude (Orchestrator) → BUPs → Departments
```

A 7-node Mac Mini M4 cluster connected via Tailscale, where each machine runs a specialized AI agent. Altitude (Python/LangGraph) manages work orders and governance. All other agents run OpenClaw (Node.js) and communicate with Altitude via MCP.

## Repos

| Repo | Description |
|------|-------------|
| [`altitude`](https://github.com/projectfirmament/altitude) | Central orchestrator — FastAPI + LangGraph, work order management, policy enforcement |
| [`agents`](https://github.com/projectfirmament/agents) | 6 OpenClaw agent workspaces — 2 BUPs + 4 shared departments |
| [`shared`](https://github.com/projectfirmament/shared) | Shared Python package — data models, state enums, DB layer |
| [`firmament-ops`](https://github.com/projectfirmament/firmament-ops) | Infrastructure — Docker compose, deploy scripts, Tailscale ACL |

## Agents

| Agent | Role | Specialization |
|-------|------|---------------|
| **Altitude** | Orchestrator | Work orders, routing, governance |
| **Ascend** | Business Unit Partner | WatchSkins (NFT/Web3 watch faces) |
| **Torque** | Business Unit Partner | Options Warehousing (contract warehousing/freight) |
| **Forge** | Department | Engineering & Intelligence |
| **Render** | Department | Content & Creative |
| **Ignite** | Department | Marketing & Growth |
| **Habano** | Department | Operations & Deployment |

## Built by

**XIS Labs** — Faizan + Abdul Ahad
