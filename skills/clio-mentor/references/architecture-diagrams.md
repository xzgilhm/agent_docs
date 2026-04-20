# Architecture Diagrams

Use this file when the user wants a system picture, component relationship diagram, data flow diagram, or deployment view.

## Diagram Modes

Choose one primary mode:
- **Context Diagram**: show system boundary, actors, and external dependencies
- **Container Diagram**: show major services, data stores, queues, and interfaces
- **Flow Diagram**: show request path, event path, or troubleshooting path
- **Deployment Diagram**: show nodes, gateways, agents, runtimes, and network boundaries
- **Comparison Diagram**: show old vs new architecture or option A vs option B

## Teaching Workflow For Diagrams

1. Confirm the goal of the diagram
2. Decide the audience: beginner, engineer, operator, interviewer
3. Pick one diagram mode only for the first pass
4. List components before drawing relationships
5. Label arrows with meaning, not just direction
6. Keep the first diagram minimal, then add detail only if needed

## Good Diagram Rules

- Show only meaningful components
- Group by responsibility, not by random implementation detail
- Prefer 5-9 nodes on the first pass
- Label important protocols, data types, or trigger types
- Mark trust boundaries, network boundaries, or failure boundaries when relevant
- If uncertainty exists, state assumptions clearly

## Output Pattern

When generating a diagram, provide these in order:
1. **Purpose**: what this diagram explains
2. **Components**: short list of nodes
3. **Relationships**: who talks to whom and why
4. **Diagram Source**: Mermaid code by default
5. **Reading Guide**: 3-5 bullets on how to read it

## Mermaid Defaults

Prefer Mermaid unless the user asks for another format.

Recommended diagram types:
- `flowchart LR` for architecture overviews
- `sequenceDiagram` for interaction flows
- `graph TD` for layered system maps

## Mermaid Style Pattern

Use short, readable labels. Example shape choices:
- actor/user -> `([User])`
- service -> `[Service]`
- datastore -> `[(DB)]`
- queue/topic -> `[[Queue]]`
- external system -> `[/External/]`

## OpenClaw-Specific Suggestions

For OpenClaw topics, common nodes may include:
- User / Telegram / Discord
- Gateway
- Agent session
- Skills
- Tools
- Memory
- Workspace files
- Subagents / ACP sessions
- Nodes / companion devices

## Closeout Options

After the diagram, optionally provide one of:
- a shorter "interview explanation" version
- a "how requests flow" version
- a "failure points" version
- a "what to learn next" version
