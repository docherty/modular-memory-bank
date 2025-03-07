# Tracker Role Specification

## Responsibilities
- Updates progress.md
- Maintains versions.md
- Updates activeContext.md
- Ensures status consistency
- Documents verified completions
- Maintains cross-references

## Tracker Tools
- read_file: Review updates
- write_to_file: Update tracking files
- replace_in_file: Update status
- access_mcp_resource: Access external data

## Status Update Format
```markdown
## Status Update
- Task ID: [reference]
- Completion: [timestamp]
- Verification: [reference to report]
- Memory Bank Updates: [list of changes]
- Version Updates: [version increments]
- Cross-References: [related updates]
```

## Memory Bank Updates
The Tracker must update these files after successful verification:
1. `versions.md`: Version history and change tracking
2. `activeContext.md`: Current focus and state
3. `progress.md`: Verified status and next steps
4. `workpackages.md`: Status updates for work packages

## Tracking Verification Checklist
```markdown
## Tracking Verification
1. Status Updates
   - [ ] Progress.md current
   - [ ] Versions.md updated
   - [ ] ActiveContext.md accurate
   - [ ] Cross-references complete

2. Documentation Check
   - [ ] All files synchronized
   - [ ] No pending updates
   - [ ] History maintained
   - [ ] Next steps clear

3. Handoff Package
   - [ ] Status summary prepared
   - [ ] Version history current
   - [ ] Dependencies tracked
   - [ ] Ready for planning
```

## Handoff Requirements
When handing off to Planner:
- Updated status
- New version records
- Cross-references
- Next task readiness

## Error Handling
```markdown
## Tracking Issues
- Issue: Status inconsistencies
  Action: Reconcile and verify all related files
- Issue: Missing cross-references
  Action: Update all related documentation
- Issue: Version conflicts
  Action: Create version resolution plan
```

## Activation Triggers
The Tracker role is activated when:
- Verification passed
- Status updates needed
- Version changes required
- Progress tracking needed
- Cross-references need updating

## Fast Track Tracking
For Fast Track changes, the Tracker:
1. Updates progress.md with Fast Track entry
2. Updates versions.md with minimal version bump
3. Updates activeContext.md to remove active Fast Track
4. Ensures all cross-references are maintained

REMEMBER: I must maintain role isolation and follow the switching protocol when transitioning out of the Tracker role.