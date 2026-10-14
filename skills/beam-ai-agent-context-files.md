---
name: beam-ai-agent-context-files
description: Upload a context file for an agent, retrieve its download link, and optionally delete it.
api: openapi/beam-ai-openapi.json
operations:
- AgentContextFilesController_uploadFile
- AgentContextFilesController_getFileDownloadLink
- AgentContextFilesController_deleteFile
generated: '2026-10-14'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/beam-ai-openapi.json ; every operationId checked against the contract
---

# beam-ai-agent-context-files

Upload a context file for an agent, retrieve its download link, and optionally delete it.

## Steps

1. 1. Call `AgentContextFilesController_uploadFile` with the `agentId` path parameter and the file payload in the request body.
2. 2. Call `AgentContextFilesController_getFileDownloadLink` with the `agentId` and `fileId` path parameters to obtain a download URL.
3. 3. (Optional) Call `AgentContextFilesController_deleteFile` with the `agentId` and `fileKey` path parameters to remove the file.

## Rules

- Include an authentication header: either `Authorization: Bearer <token>` or `x-api-key: <key>` as defined by the provider.
- All operations are performed on the `/context/agent/{agentId}` path; ensure the correct `agentId` is supplied.
