# Cross-Role Workflows

This document captures workflows that span multiple roles to provide a cohesive view of integrated processes.

## Role Interaction Protocol

```mermaid
sequenceDiagram
    participant I as Initializer
    participant P as Planner
    participant Im as Implementer
    participant C as Checker
    participant T as Tracker
    
    I->>P: Memory Bank Created
    Note over I,P: Complete structure ready
    P->>Im: Task Definition Package
    Note over P,Im: Includes acceptance criteria
    Im->>C: Implementation Complete
    Note over Im,C: Code + doc changes
    C-->>Im: Issues Found
    Note over C,Im: Iteration if needed
    C->>T: Verification Passed
    Note over C,T: With evidence
    T->>P: Status Updated
    Note over T,P: Ready for next task
```

## Work Package Lifecycle

```mermaid
stateDiagram-v2
    [*] --> DRAFT: Planner Creates
    DRAFT --> APPROVED: Checker Reviews
    APPROVED --> IN_PROGRESS: Implementer Starts
    IN_PROGRESS --> COMPLETED: Checker Verifies
    IN_PROGRESS --> FAILED: Issues Found
    FAILED --> DRAFT: Revision Needed
```

## Act Mode Operation

```mermaid
flowchart TD
    I[Implementer Active] --> RW[Read Work Package]
    RW --> EX[Execute Task]
    EX --> DC[Document Changes]
    DC --> C[Checker Verifies]
    C -->|Issues| RW
    C -->|Passed| T[Tracker Updates Status]
    T --> P[Planner Reviews Next Steps]
```

In Act Mode:
1. **Implementer**
   - Reviews work package
   - Executes defined tasks
   - Documents changes
   - Creates verification evidence

2. **Checker**
   - Validates against acceptance criteria
   - Reviews documentation updates
   - Verifies Memory Bank consistency
   - Reports verification results

3. **Tracker**
   - Updates progress status
   - Records completed tasks
   - Updates version history
   - Maintains cross-references

4. **Planner**
   - Reviews completion
   - Plans next steps
   - Adjusts task sequence if needed
   - Updates project timeline

## Transition Protocol

```mermaid
stateDiagram-v2
    [*] --> Initializer: New Project
    Initializer --> Planner: Memory Bank Created
    Planner --> Implementer: Work Package Ready
    Implementer --> Checker: Task Complete
    Checker --> Implementer: Issues Found
    Checker --> Tracker: Verification Passed
    Tracker --> Planner: Status Updated
```

## Update Sequence

```mermaid
flowchart TD
    Start[Update Required] --> Verify[Verify Current State]
    Verify --> Read[Read Affected Files]
    Read --> Cross[Cross-Reference Check]
    Cross --> Update[Make Updates]
    Update --> Version[Update versions.md]
    Version --> Validate[Validate Changes]
    Validate --> Active[Update activeContext.md]
```

## Synchronization Triggers

MUST verify and update Memory Bank when:
1. Starting any task
2. Completing any step
3. Updating status
4. Switching modes
5. Creating/modifying files
6. Marking items complete
7. Recording decisions
8. Handling async operations

## Memory Bank Initialization Flow

```mermaid
flowchart TD
    Start[New Project] --> Init[Initializer Activated]
    Init --> Structure[Create Directory Structure]
    Structure --> Files[Initialize Core Files]
    Files --> Templates[Apply Templates]
    Templates --> Version[Set Initial Version]
    Version --> Document[Document Setup]
    Document --> Handoff[Switch to Planner]
    Handoff --> FirstTask[Begin First Tasks]
```
