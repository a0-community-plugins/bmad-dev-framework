# BMAD Game Engine Setup Guide

Guides for configuring game projects with BMAD Game Dev Studio (BMGD) workflows across three major engines: Godot, Unity, and Unreal.

## Engine Selection

| Engine | Best For | Language |
|--------|---------|---------|
| **Godot** | Indie, 2D, lightweight 3D, open source | GDScript, C# |
| **Unity** | Mobile, cross-platform, medium-scale 3D | C# |
| **Unreal** | AAA, large-scale 3D, photorealism | C++, Blueprints |

## Common Setup Workflow

Regardless of engine, the BMGD setup follows the same phases:

### Phase 1: Project Context Generation

Create `project-context.md` as the single source of truth:
- Project name and description
- Target platforms (PC, mobile, web, console)
- Engine version and renderer choice
- Performance budgets
- Critical technical decisions

### Phase 2: Brainstorming and Brief

1. **Brainstorm Game** -- Guided ideation to generate and refine game ideas
2. **Create Game Brief** -- Capture vision, audience, market positioning, art/audio direction

### Phase 3: Game Design Document (GDD)

1. Select game type from 24 available templates
2. Define core gameplay mechanics
3. Design progression systems
4. Plan levels and content
5. Specify art and audio requirements

Output: `gdd.md`

### Phase 4: Technical Architecture

Engine-specific architecture document covering:
- Project structure (scenes/prefabs/assets organization)
- System architecture (game loop, component patterns)
- Engine-specific patterns and best practices
- Performance budgets and optimization strategy
- Export configurations and platform settings

Output: `architecture.md`

### Phase 5: Sprint Planning and Implementation

1. Sprint planning from epics and GDD
2. Story creation with acceptance criteria
3. Implementation with test-driven development
4. Code review and sprint retrospectives

## Godot-Specific Setup

### Recommended Project Structure

```
res://
  scenes/
    levels/
    characters/
    ui/
    components/
  scripts/
    autoload/
    utils/
  assets/
    art/
    audio/
    data/
  project.godot
```

### Key Patterns

- **Autoload Singletons** -- Global managers (game state, audio, saves)
- **Scene Composition** -- Reusable scenes (player, enemies, pickups)
- **Signal Patterns** -- Decoupled communication between nodes

### Testing

GUT (Godot Unit Test) for unit and integration tests.

### Performance Targets

- 60 FPS for most games
- 30 FPS for mobile with heavy computation
- 144+ FPS for competitive games

## Unity-Specific Setup

### Recommended Project Structure

```
Assets/
  Scenes/
  Scripts/
    Core/
    Gameplay/
    UI/
  Prefabs/
  Materials/
  Audio/
  Resources/
```

### Key Patterns

- **ScriptableObjects** -- Data-driven design for game config
- **Prefab Composition** -- Reusable game object templates
- **Event Systems** -- Decoupled communication between components
- **Assembly Definitions** -- Organize code into compilation units

### Testing

Unity Test Framework with Edit Mode and Play Mode tests.

## Unreal-Specific Setup

### Recommended Project Structure

```
Content/
  Blueprints/
  Maps/
  Characters/
  UI/
  Audio/
  Materials/
Source/
  ProjectName/
    Core/
    Gameplay/
    AI/
```

### Key Patterns

- **GameInstance** -- Persistent data across levels
- **GameMode/GameState** -- Game rules and state management
- **Component Architecture** -- Reusable behavior components
- **Subsystems** -- Engine-level service patterns
- **Gameplay Ability System** -- Complex ability/skill management

### Testing

Unreal Automation Framework and Gauntlet for automated testing.

## Quick Flow vs Full Production

| Quick Flow | Full Production |
|-----------|----------------|
| Working alone or tiny team | Larger team |
| Speed over process | Need formal documentation |
| Prototyping or game jams | Working with stakeholders/publishers |
| Skip full planning phases | Long-term maintainability critical |

Use Quick Flow for rapid prototyping. Use Full Production for serious development.
