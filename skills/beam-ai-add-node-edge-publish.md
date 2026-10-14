---
name: beam-ai-add-node-edge-publish
description: Add a node to an agent graph, connect it with an edge, and publish the updated graph.
api: openapi/beam-ai-openapi.json
operations:
- AgentGraphController_addNode
- AgentGraphController_addEdge
- AgentGraphController_publishGraph
generated: '2026-10-14'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/beam-ai-openapi.json ; every operationId checked against the contract
---

# beam-ai-add-node-edge-publish

Add a node to an agent graph, connect it with an edge, and publish the updated graph.

## Steps

1. 1. Call `AgentGraphController_addNode` with the required request body fields for the new node and include an authentication header (`Authorization: Bearer <token>` or `x-api-key: <key>`).
2. 2. Call `AgentGraphController_addEdge` with the required request body fields specifying the source and target node IDs and include an authentication header.
3. 3. Call `AgentGraphController_publishGraph` with the graph ID in the path and include an authentication header.

## Rules

- Authentication: Provide either a Bearer token in the `Authorization` header or an API key in the `x-api-key` header.
- Idempotency: Not required for these operations.
- Pagination: Not applicable.
- Errors: Follow standard HTTP error responses as defined by the API (e.g., 4xx for client errors, 5xx for server errors).
