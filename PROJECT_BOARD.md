# 📦 ECS Colony Sim – GitHub Project Board

## Phase 1 – Project Setup
- Initialize Rust project and Git repository  
- Add `bevy`, `bevy_ecs_tilemap`, and relevant crates  
- Set up `src/` folder structure (`components/`, `systems/`, `plugins/`, etc.)  
- Create `CorePlugin` and wire it up in `main.rs`  
- Set up logging / debug output  
- Continuous integration: `cargo check`, `clippy`, `fmt`  
- Add unit‑test skeletons in `tests/`  

## Phase 2 – Core Data Modeling
- Create `Position(Vec3)`, `Velocity`, `Health`, `Needs` components  
- Create `DepthLayer(Vec3)` component for vertical positioning  
- Create `TileType`, `Passable`, `Liquid` components  
- Add `TimeState` and `MapResource` as `Resource`s  
- Create enums for `ItemType`, `JobType`, `Skill`  
- Create `UiWindowState` resource  

## Phase 3 – World Generation
- Initialize and fill `MapResource`  
- Create world generator to spawn basic terrain (grass, stone, water)  
- Spawn tile entities with `TileType` and `Position(Vec3)`  
- Display **spatial cellmap** visually (debug colors or tileset)  

## Phase 4 – Entity Spawning
- Create dwarf spawner (`spawn_dwarf()`)  
- Create spawners for trees, rocks, animals  
- Add default inventory/equipment to entities  
- Create `Name`, `AIState`, `Skills` components  
- Add `AIPlugin` skeleton (behaviour systems container)  
- Prepare `job_priority_queue` resource  

## Phase 5 – Systems & Simulation Loop
- **Register systems** with `.add_systems(Startup/Update)` + execution‑order hints  
- Add `movement_system`  
- Add `hunger_system`  
- Add `decay_system` for items and needs  
- Add `event_system` (jobs, alerts, UI triggers)  
- Add `component_cleanup_system` (despawn / recycle)  
- Create event‑based job system (spawn `Job` entities)  

## Phase 6 – Jobs & Basic AI
- Define `Job` component and `JobAssignment` system  
- Match idle dwarves to jobs via `Skills` + `job_priority_queue`  
- Implement pathfinding using `MapResource`  
- Track job progress and completion state  

## Phase 7 – UI Windows & State
- Add `UiPlugin` (window, state, focus tracking)  
- HUD with time and dwarf count  
- Inventory window toggle (`KeyCode::I`)  
- Entity inspection panel  
- UI state machine (build / inspect / pause)  
- Integrate `bevy_egui` for rapid prototyping  

## Phase 8 – Input & Interaction
- Implement mouse tile selection  
- Add keyboard input mapping  
- Zone designation tool (drag‑to‑dig)  
- Tile hover tooltips  

## Phase 9 – Rendering & Animation
- Replace debug tiles with tileset / sprite atlas  
- Animation system for walking, idle, mining  
- Fog‑of‑war / unexplored overlay  
- Smooth camera movement & zoom  
- Camera vertical‑layer navigation (depth slice viewer)  

## Phase 10 – Advanced Simulation
- Production chains (mining → smelting → smithing)  
- Combat and injuries  
- Relationships, moods, mental states  
- Nobles, mandates, social systems  
- In‑game pause  

## Extras
- Serialization for save/load (`ron`, `serde`)  
- Deterministic simulation mode for debugging  
- ECS execution‑graph trace tool (optional)  
- Debug overlay to toggle system output  
- Modularize into Bevy plugins per system (AIPlugin, UIPlugin, etc.)
