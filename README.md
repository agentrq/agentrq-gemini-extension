# AgentRQ Gemini CLI Extension

Human-in-the-loop task manager for agents. This extension connects Gemini CLI to the [AgentRQ](https://agentrq.com/) platform via the AgentRQ supervisor MCP server, allowing the AI agent to manage workspaces(sub agents), tasks, and communicate directly with human operators.

## Installation

You can install this extension using the Gemini CLI:

```bash
gemini extensions install https://github.com/agentrq/agentrq-gemini-extension
```

Once installed, the extension connects to `https://mcp.agentrq.com/mcp` and securely authenticates using your AgentRQ account.

## Available MCP Tools

This extension exposes the following tools to Gemini via the AgentRQ Supervisor MCP server:

### Workspace Management
- **`listWorkspaces`**: Overview of all active and archived workspaces.
- **`createWorkspace`**: Bootstrap new project environments.
- **`getWorkspace`**: Retrieve details of a specific workspace by ID.
- **`updateWorkspace`**: Modify workspace settings and metadata.
- **`getWorkspaceStats`**: Retrieve high-level analytics and performance data for a workspace.

### Task Management
- **`listAllTasks`**: Search and filter tasks across the entire platform.
- **`listTasks`**: List tasks within a specific workspace.
- **`createTask`**: Create a new task in a specific workspace.
- **`getTask`**: Retrieve details of a specific task.
- **`updateTaskStatus`**: Change a task's status (e.g. notstarted, ongoing, blocked, completed).
- **`updateTaskOrder`**: Reorder a task in the list.
- **`updateTaskAssignee`**: Change the assignee of a task.
- **`updateTaskAllowAll`**: Toggle `allow_all_commands` permission for a task.
- **`updateScheduledTask`**: Modify a scheduled/cron task.

### Communication & Files
- **`replyToTask`**: Post a message to a task's chat thread.
- **`respondToTask`**: Submit an allow/deny verdict for a permission request.
- **`getAttachment`**: Retrieve data as base64 and metadata for a specific attachment.

## License
Apache-2.0
