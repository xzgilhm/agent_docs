# Mermaid Patterns

Use these templates to generate diagrams quickly.

## Pattern A: System Context

```mermaid
flowchart LR
    U([User]) --> S[System]
    S --> E[/External Service/]
    S --> D[(Data Store)]
```

## Pattern B: Container View

```mermaid
flowchart LR
    U([User]) --> G[Gateway]
    G --> A[Agent Session]
    A --> K[Skill]
    A --> T[Tools]
    T --> W[(Workspace)]
    A --> M[(Memory)]
```

## Pattern C: Request Flow

```mermaid
sequenceDiagram
    participant U as User
    participant G as Gateway
    participant A as Agent
    participant T as Tools
    U->>G: Send message
    G->>A: Create / resume session
    A->>T: Read / write / exec
    T-->>A: Results
    A-->>G: Reply
    G-->>U: Deliver response
```

## Pattern D: Deployment View

```mermaid
graph TD
    C[Chat Surface] --> G[Gateway]
    G --> S[Main Session]
    S --> SA[Subagent]
    S --> WF[(Workspace Files)]
    S --> MEM[(Memory Files)]
    G --> N[Connected Node]
```

## Pattern E: Troubleshooting Flow

```mermaid
flowchart TD
    A[Symptom] --> B{Gateway reachable?}
    B -- No --> C[Check service status]
    B -- Yes --> D{Session running?}
    D -- No --> E[Inspect runtime logs]
    D -- Yes --> F[Check tools / config]
```

## Quality Checks

Before finalizing a diagram, verify:
- node names are human-readable
- arrows have a clear meaning
- the diagram matches the user's question
- there are not too many components for one picture
- the diagram could be explained in under one minute
```