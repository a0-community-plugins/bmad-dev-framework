# BMAD Sprint Planning

Agile sprint planning and tracking workflows for game and software development within the BMAD methodology.

## When to Use

- Completed GDD and/or Architecture document
- Ready to start implementing features
- Want to track progress through stories and sprints

## Sprint Workflow

```
sprint-planning -> create-story -> dev-story -> code-review -> sprint-status -> retrospective
                       ^______________|
                       (repeat for each story)
```

## Step 1: Generate Sprint Status from Epics

The Scrum Master reads epic files to create the sprint tracking document (`sprint-status.yaml`):

1. Read GDD and Architecture documents
2. Identify epics (large feature areas)
3. Generate stories from epics
4. Organize stories into sprints based on dependencies and priority

## Step 2: Review Sprint Status

The generated tracking file includes:

```yaml
sprint: 1
status: In Progress
stories:
  - id: story-001
    title: "Player movement system"
    status: Ready
    priority: P0
    points: 5
  - id: story-002
    title: "Basic enemy AI"
    status: Pending
    priority: P1
    points: 8
```

Priority levels:
- **P0** -- Must have for this sprint
- **P1** -- Should have if time allows
- **P2** -- Nice to have, defer if needed

## Step 3: Create Detailed Stories

Each story file includes:
- Title and description
- Acceptance criteria -- definition of done
- Technical notes from architecture
- Test cases -- what needs to be tested
- Dependencies -- other stories or systems

## Step 4: Implement Stories

For each story:
1. Read the story file and acceptance criteria
2. Reference architecture for technical guidance
3. Implement the feature
4. Create or update tests
5. Mark story complete when all criteria pass

## Step 5: Code Review

When a story is flagged "Ready for Review":
- Verify acceptance criteria are met
- Check for performance issues
- Review test coverage
- Provide feedback or approve

## Step 6: Check Sprint Status

At any time, review:
- Current sprint number and status
- Story progress (Ready, In Progress, Complete, Blocked)
- Risks and blockers
- Recommended next actions

## Step 7: Close Sprint

When all sprint stories are complete:
1. Facilitate a retrospective (what went well, what to improve, action items)
2. Run sprint planning again for the next sprint

## Story States

| State | Meaning | Next Action |
|-------|---------|-------------|
| **Pending** | Not yet ready to start | Move to Ready when dependencies complete |
| **Ready** | Ready to implement | Start development |
| **In Progress** | Currently being implemented | Complete or flag if blocked |
| **Complete** | Done and tested | Move to next story |
| **Blocked** | Cannot proceed | Resolve blocker or re-plan |

## Sprint Best Practices

- Always generate stories from GDD and Architecture -- do not write stories from scratch
- Do not start implementation without stories -- stories provide clear acceptance criteria
- Every sprint should deliver a playable/usable increment
- Follow priority order -- P0 first, then P1, then P2
- Test after every story completes -- catches issues early
- Playtest (for games) or user-test regularly -- validate against real usage

## Course Correction

When major changes are discovered mid-implementation:
1. Assess the impact on current sprint and backlog
2. Determine whether to absorb, defer, or restructure
3. Update sprint status and story priorities
4. Communicate changes to all stakeholders
