# 📦 ECS Colony Sim – GitHub Project Board

## Phase 1 – Project Setup
- [ ] Initialize Rust project and Git repository
- [ ] Add `bevy`, `bevy_ecs_tilemap`, and relevant crates
- [ ] Set up `src/` folder structure (`components/`, `systems/`, `plugins/`, etc.)
- [ ] Create `CorePlugin` and wire it up in `main.rs`
- [ ] Set up logging / debug output

## Phase 2 – Core Data Modeling
- [ ] Create `Position`, `Velocity`, `Health`, `Needs` components
- [ ] Create `TileType`, `Passable`, `Liquid` components
- [ ] Add `TimeState` and `MapResource` as `Resource`s
- [ ] Create enums for `ItemType`, `JobType`, `Skill`

## Phase 3 – World Generation
- [ ] Initialize and fill `MapResource`
- [ ] Create world generator to spawn basic terrain (grass, stone, water)
- [ ] Spawn tile entities with `TileType` and `Position`
- [ ] Display tilemap visually (temporary debug color coding or tileset)

## Phase 4 – Entity Spawning
- [ ] Create dwarf spawner (`spawn_dwarf()` in `entities/`)
- [ ] Create spawners for trees, rocks, animals
- [ ] Add default inventory/equipment to entities
- [ ] Create `Name`, `AIState`, `Skills` components

## Phase 5 – Systems & Simulation Loop
- [ ] Add `movement_system`
- [ ] Add `hunger_system`
- [ ] Add `decay_system` for items and needs
- [ ] Create event-based job system (e.g., spawn `Job` entity)

## Phase 6 – Jobs & Basic AI
- [ ] Define `Job` component and `JobAssignment` system
- [ ] Match idle dwarves to available jobs (based on `Skills`)
- [ ] Implement pathfinding system using `MapResource`
- [ ] Track job progress and completion state

## Phase 7 – UI Windows
- [ ] Create `UiWindowState` resource
- [ ] Add HUD with time and dwarf count
- [ ] Create inventory window with toggling (`KeyCode::I`)
- [ ] Create entity inspection panel

## Phase 8 – Input & Interaction
- [ ] Implement mouse tile selection
- [ ] Add keyboard input mapping
- [ ] Create zone designation tool (drag-to-dig)
- [ ] Add tile hover tooltips

## Phase 9 – Rendering & Animation
- [ ] Replace debug tile display with tileset or sprite atlas
- [ ] Add animation system for walking, idle, mining
- [ ] Add fog of war or unexplored tile overlay
- [ ] Create smooth camera movement & zoom

## Phase 10 – Advanced Simulation
- [ ] Add production chains (e.g., mining → smelting → smithing)
- [ ] Implement combat and injuries
- [ ] Add relationships, moods, and mental states
- [ ] Introduce nobles, mandates, and social systems

## Extras
- [ ] Create debug overlay to toggle system output
- [ ] Document all components and systems
- [ ] Add in-game pause and save/load functionality
- [ ] Modularize into Bevy plugins per system (AIPlugin, UIPlugin, etc.)
