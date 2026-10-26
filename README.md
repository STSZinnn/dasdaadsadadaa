# Sovereign SMP v1.6 - 16x16 Custom Particle Sprites

Paper 1.21.11 / Java 21. The Sovereign Mace remains a unique special weapon; Echo Scythe remains Artifact I / VII.

- Added 10 new exact 16x16 pixel art effect sprites, not hyper-realistic textures.
- Mace: gravity pulse ring, shards, stars, void core, collapse spark.
- Scythe: echo soul, sculk spore, echo ring, sculk rune, sonic arc.
- Vanilla effects remain available without a resource pack.
- Plugin renders short-lived sprites as small billboard ItemDisplay entities using custom item_model IDs. This intentionally avoids globally replacing the built-in vanilla particle atlas.
- All custom sprite displays have bounded lifetimes, a global server-side cap, and are removed on plugin disable or restart.
- No physical items, combat balance, ownership IDs, tooltips, or ordinary blocks are changed by this particle update.

## Install
1. Build project with the included GitHub Actions workflow.
2. Put JAR on Paper server, remove old Sovereign jar, restart.
3. Players enable SovereignSMP_Particle_Pack_v1.6_1.21.11.zip in Minecraft (or the combined pack).
4. OP: `/sovereign config` -> **Custom Particle Sprites** -> Enable.
5. If you see magenta missing-texture squares, disable the setting until the resource pack is active.

## Notes
- These are display-entity sprites styled like particles, not newly registered native particle types; Paper plugins cannot define brand-new client particle IDs without mods.
- All original particle effects still run; these add custom visuals.
- Max live sprite entities defaults to 90. Adjust in config for busy servers.
- Resource pack and Java must match for custom sprite IDs.
- Not tested in a live Paper server; use GitHub to compile and test in game.
