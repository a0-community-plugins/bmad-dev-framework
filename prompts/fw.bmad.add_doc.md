# BMAD Documentation Authoring Guide

Guided workflow for creating Diataxis-compliant documentation. Helps structure, classify, and place documentation correctly.

## Critical Rules

- NEVER commit or push -- let the user review first
- ALWAYS ask before creating files -- get approval on location and content
- Educate as you guide -- explain WHY documents belong in certain places
- Show structure first -- present the template before writing content

## Step 1: Understand the User's Goal

Ask questions to understand:
1. What is the core topic?
2. Who is the audience? (beginners, experienced users, reference lookups)
3. What does the user want to accomplish? (teach a concept, explain a process, document a reference)

## Step 2: Determine Document Type (Diataxis)

Use the Diataxis framework to classify the document:

| Type | Goal | User State | Structure |
|------|------|------------|-----------|
| **Tutorial** | Learn by doing | Beginner, needs hand-holding | Linear, step-by-step |
| **How-to** | Solve a specific problem | Knows basics, stuck on X | Sequential steps |
| **Explanation** | Understand concepts | Wants depth/clarification | Scannable sections |
| **Reference** | Look up information | Experienced, needs facts | Organized for lookup |

Common confusions:
- "Teach someone to X" = Tutorial (not How-to)
- "How do I do X?" = How-to (not Tutorial)
- "What is X?" = Explanation (not Tutorial)
- "API docs for X" = Reference (not Explanation)

## Step 3: Confirm Location

| Location | Type |
|----------|------|
| `/docs/tutorials/` | Tutorial |
| `/docs/how-to/` | How-to guide |
| `/docs/explanation/` | Explanation |
| `/docs/reference/` | Reference |

Filename conventions (kebab-case):
- Tutorial: `create-your-first-{topic}.md` or `create-{topic}.md`
- How-to: `{action}-{topic}.md`
- Explanation: `what-are-{topic}.md` or `{topic}-architecture.md`
- Reference: `{topic}-schema.md` or `{topic}-reference.md`

## Step 4: Apply Style Rules

| Rule | Fix |
|------|-----|
| No horizontal rules (`---`) | Use `##` headers or admonitions |
| No `####` headers | Use bold text or admonitions |
| No "Related" or "Next:" sections | Remove -- sidebar handles navigation |
| No deeply nested lists | Break into sections |
| 1-2 admonitions per section max | Consolidate or remove |
| Table cells / list items | Keep to 1-2 sentences max |
| Header budget | 8-12 `##` per doc; 2-3 `###` per section |

## Step 5: Gather Content and Write

1. Start with the hook -- help write 1-2 compelling sentences
2. Work through sections sequentially -- do not jump ahead
3. Ask for specific content -- "What are the 3-5 things they will learn?"
4. Suggest improvements -- "This could be more action-oriented"
5. Present the full content for final review before writing

## Step 6: Post-Creation

After creating the document:
1. Suggest validation for Diataxis compliance
2. Ask if other docs should link to this new one
3. Check if index files need updating
4. Suggest a build check to verify no errors
