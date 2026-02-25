# BMAD Game Types Reference

Reference for selecting and using the 24 supported game type templates from the BMAD Game Dev Studio (BMGD). When creating a Game Design Document (GDD), these templates provide genre-specific sections ensuring coverage of mechanics and systems relevant to your game's genre.

## Game Type Categories

### Action & Combat

**Action Platformer** -- Side-scrolling or 3D platforming with combat mechanics (Hollow Knight, Celeste, Mega Man).
GDD sections: Movement systems, combat mechanics, level design patterns, boss design.

**Shooter** -- Projectile combat with aiming mechanics (FPS, TPS, arena shooters).
GDD sections: Weapon systems, aiming/accuracy, enemy AI, level/arena design, multiplayer.

**Fighting** -- 1v1 combat with combos and frame data (traditional and platform fighters).
GDD sections: Frame data systems, combo mechanics, character movesets, competitive balance, netcode.

### Strategy & Tactics

**Strategy** -- Resource management with tactical decisions (RTS, 4X, grand strategy).
GDD sections: Resource systems, unit/building design, AI opponents, map design, victory conditions.

**Turn-Based Tactics** -- Grid-based movement with turn order (XCOM-likes, tactical RPGs).
GDD sections: Grid/movement systems, turn order, cover/positioning, unit progression, procedural missions.

**Tower Defense** -- Wave-based defense with tower placement.
GDD sections: Tower types/upgrades, wave design, economy, map patterns, meta-progression.

### RPG & Progression

**RPG** -- Character progression with stats, inventory, and quests.
GDD sections: Stats/leveling, inventory/equipment, quest system, combat system, skill trees.

**Roguelike** -- Procedural generation with permadeath and run-based progression.
GDD sections: Procedural generation, permadeath/persistence, run structure, item synergies, meta-progression.

**Metroidvania** -- Interconnected world with ability gating.
GDD sections: World map connectivity, ability gating, backtracking flow, secrets, power-up progression.

### Narrative & Story

**Adventure** -- Story-driven exploration (point-and-click, narrative adventure).
GDD sections: Puzzle design, narrative delivery, exploration mechanics, dialogue systems, story branching.

**Visual Novel** -- Narrative choices with branching story.
GDD sections: Branching narrative, choice/consequence, character routes, UI/presentation, save/load.

**Text-Based** -- Text input/output games (parser games, choice-based IF, MUDs).
GDD sections: Parser/choice systems, world model, narrative structure, text presentation, save states.

### Simulation & Management

**Simulation** -- Realistic systems with management and building (tycoons, sim games).
GDD sections: Core simulation loops, economy modeling, AI agents, building/construction, failure states.

**Sandbox** -- Creative freedom with building and minimal objectives.
GDD sections: Creation tools, physics/interaction, persistence/saving, sharing, optional objectives.

### Sports & Racing

**Racing** -- Vehicle control with tracks and lap times.
GDD sections: Vehicle physics, track design, AI opponents, progression/career, multiplayer.

**Sports** -- Team-based or individual sports simulation.
GDD sections: Sport-specific rules, player/team management, AI opponents, season/career, multiplayer.

### Multiplayer

**MOBA** -- Multiplayer team battles with hero selection.
GDD sections: Hero/champion design, lane/map design, team composition, matchmaking, economy.

**Party Game** -- Local multiplayer with minigames.
GDD sections: Minigame design, controller support, round/game structure, scoring, player count flexibility.

### Horror & Survival

**Survival** -- Resource gathering with crafting and persistent threats.
GDD sections: Resource gathering, crafting systems, hunger/health/needs, threat systems, base building.

**Horror** -- Atmosphere and tension with limited resources.
GDD sections: Fear mechanics, resource scarcity, sound design, lighting/visibility, enemy/threat design.

### Casual & Progression

**Puzzle** -- Logic-based challenges and problem-solving.
GDD sections: Puzzle mechanics, difficulty progression, hint systems, level structure, scoring.

**Idle/Incremental** -- Passive progression with upgrades and automation.
GDD sections: Core loop, prestige systems, automation unlocks, number scaling, offline progress.

**Card Game** -- Deck building with card mechanics.
GDD sections: Card design framework, deck building rules, mana/resource systems, rarity/collection, competitive balance.

**Rhythm** -- Music synchronization with timing-based gameplay.
GDD sections: Note/beat mapping, scoring systems, difficulty levels, music licensing, input methods.

## Hybrid Game Types

Many games combine multiple genres. Select 2-3 types maximum:

| Hybrid | Components |
|--------|-----------|
| Action RPG | Action Platformer + RPG |
| Survival Horror | Survival + Horror |
| Roguelike Deckbuilder | Roguelike + Card Game |

One type should be primary (most gameplay time). Others add flavor.

## Game Type Selection Tips

1. **Start with core fantasy** -- What does the player primarily DO?
2. **Consider the loop** -- Session-based runs? Long progression? Quick matches?
3. **Do not over-combine** -- 2-3 types maximum
4. **Pick a primary** -- One type drives the core experience
