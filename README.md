# The Signal Lost â€” GamesTest

A Unity game prototype used as a testbed for game mechanics: player movement, physics interaction, and level flow. Contains an exported Windows build alongside the project evaluation work.

> **Note:** The `SignalLost/` folder holds a **compiled Windows build** (executables, managed DLLs, Mono runtime), not source. Build output generally should not live in version control â€” see *Repository Hygiene* below.

## What This Is

A scratch space for prototyping and validating game feel before committing concepts to a fuller project. The focus is on getting mechanics right: how movement responds, how physics reads, how a level guides the player.

## Contents

```
SignalLost/            # Exported Windows player build + Mono runtime (build artifact)
  SignalLost.exe
  SignalLost_Data/     # Compiled assemblies and game data
  MonoBleedingEdge/    # Bundled Mono runtime
```

## Repository Hygiene

This repo currently tracks a compiled build. Recommended cleanup for a game project:

1. Add a `.gitignore` covering Unity build output:
   ```
   /[Bb]uild/
   /[Bb]uilds/
   /[Ll]ogs/
   /[Uu]ser[Ss]ettings/
   *.exe
   *.dll
   ```
2. Commit **source** (`Assets/`, `Packages/`, `ProjectSettings/`) rather than binaries
3. Publish builds as GitHub Releases instead of raw commits

Sibling repos `rolling-ball` and `unity-demo` follow this source-first pattern.

## Tech Stack

- Unity (C#)
- Built with MCP tooling for editor automation

**Author:** Raliq Hidayat BM3
