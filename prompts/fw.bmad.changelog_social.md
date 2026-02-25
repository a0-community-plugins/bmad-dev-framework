# BMAD Changelog Social Media Generator

Generate engaging social media announcements from changelog entries for Discord, Twitter, and LinkedIn.

## Workflow

### Step 1: Extract Changelog Entry

Read the project's `CHANGELOG.md` and extract the latest version entry. Parse:

- **Version number** (e.g., `2.1.0`)
- **Features** -- New functionality, enhancements
- **Bug Fixes** -- Fixes users care about
- **Documentation** -- New or improved docs
- **Maintenance** -- Dependency updates, tooling improvements

### Step 2: Get Git Contributors

Use git log to find contributors since the previous version:

```bash
git tag --sort=-version:refname | head -5
git log <previous-tag>..<current-tag> --pretty=format:"%h|%s|%an" --grep="#"
```

Extract PR numbers from commit messages. Compile unique contributors.

### Step 3: Generate Discord Announcement

Limit: 2,000 characters per message. Split into multiple messages if needed.

Structure:
- Version headline with brief hype sentence
- Key highlight -- one-line summary of the biggest change
- Categorized bullet points (Features, Fixes, Docs)
- Stats (commits, PRs merged, files changed)
- Contributors with shout-outs
- Install/update command
- Support links

### Step 4: Generate Twitter Post

Aim for 1,500-3,000 characters. Focus on user impact and what is better for them. Match the Discord style minus Discord-specific formatting.

### Step 5: Generate LinkedIn Post (Major Releases Only)

Professional tone for major or minor releases with significant features. Include community milestone information.

## Content Selection Guidelines

**Include:**
- New features that change workflows
- Bug fixes for annoying/blocking issues
- Documentation that helps users
- Performance improvements
- Breaking changes (call out clearly)

**Skip/Minimize:**
- Internal refactoring
- Dependency updates (unless user-facing)
- Test improvements
- Minor style fixes

**Emphasize:**
- "Finally fixed" issues
- "Faster" operations
- "Easier" workflows
- "Now supports" capabilities

## Content Strategy

- Focus on **user impact** -- what is better for them?
- Highlight **annoying bugs fixed** that frustrated users
- Show **new capabilities** that enable workflows
- Keep it **punchy** -- use emojis and short bullets
- Add **personality** -- excitement, humor, gratitude

## Output

Write files to a `social/` output directory:
1. `discord-{version}.md` -- Discord announcement
2. `twitter-{version}.md` -- Twitter post
3. `linkedin-{version}.md` -- LinkedIn post (if applicable)
