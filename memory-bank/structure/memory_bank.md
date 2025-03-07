# Memory Bank Structure

## Core Files

1. `versions.md`
   - Version history for all Memory Bank files
   - Change tracking and evolution
   - Cross-references to related changes
   - Timestamp for all updates

2. `projectbrief.md`
   - Foundation document
   - Core requirements and goals
   - Project scope
   - Created at project start

3. `productContext.md`
   - Project purpose
   - Problem definition
   - User experience goals
   - Expected behavior

4. `activeContext.md`
   - Current focus
   - Recent changes
   - Next steps
   - Active decisions
   - Waiting states for async operations

5. `systemPatterns.md`
   - System architecture
   - Technical decisions
   - Design patterns
   - Component relationships

6. `techContext.md`
   - Technologies used
   - Development setup
   - Technical constraints
   - Dependencies

7. `progress.md`
   - Current status (verified)
   - Completed items (with verification)
   - Known issues
   - Next steps

8. `workpackages.md`
   - Chronological work package history
   - Task definitions and criteria
   - Implementation states and transitions
   - Cross-references to related changes
   - Decision logs and rationale

## Cross-Reference System

### Reference Types
1. Task References: WP-YYYYMMDD-XX
2. Version References: v1.2.3
3. File References: file:path/to/file.ext
4. Decision References: DEC-YYYYMMDD-XX

### Cross-Reference Format
```markdown
[Type-ID](link-to-reference) - Brief context
```

## Initial File Templates

For each required file, use these basic templates when creating from scratch:

```markdown
# versions.md
## Version History
- v0.0.1 - Initial Memory Bank creation
- Created: [current timestamp]
```

```markdown
# projectbrief.md
## Project Overview
- Name: [Project Name]
- Purpose: [Brief description]
- Created: [timestamp]

## Core Requirements
- [List initial requirements]

## Project Scope
- [Define initial scope]
```

```markdown
# activeContext.md
## Current Focus
- Setting up project structure
- Initializing Memory Bank
- Gathering initial requirements

## Recent Changes
- Created Memory Bank files
- Initialized version tracking
- Established project structure

## Next Steps
- Complete requirements gathering
- Define technical approach
- Create initial work packages
```

## Async Operation Handling

Track in activeContext.md:
```markdown
## Waiting States
- Operation: [Description]
- Started: [Timestamp]
- Status: [Current State]
- Next Action: [Required Action]
- Dependencies: [Related Items]
```

## Project Intelligence (.clinerules)
The .clinerules file captures:
- Critical implementation paths
- User preferences
- Project patterns
- Known challenges
- Decision evolution
- Tool usage patterns
- Async operation patterns

## Failure Recovery
When inconsistencies found:
1. Report to user:
   ```markdown
   MEMORY BANK INCONSISTENCY DETECTED
   - File: [filename]
   - Type: [type of inconsistency]
   - Details: [specific details]
   - Suggested Fix: [steps to resolve]
   ```

2. Wait for user confirmation before proceeding
3. Document issue in activeContext.md
4. Update versions.md with resolution