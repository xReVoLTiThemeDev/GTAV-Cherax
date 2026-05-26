# GTA V Cherax Lua Projects

A curated archive of my GTA V Cherax Lua mods, tools, experiments, and open-source projects.

Created by **Animus / xReVoLTiThemeDev**  
Discord: **animusx1337**  
GitHub: **https://github.com/xReVoLTiThemeDev/GTAV-Cherax**

Estimated Development Time: **~82 hours** as of **06/26/2026**

---

## Overview

This repository is a collection of Lua-based projects, experiments, tools, and modding systems created for **GTA V Cherax**.

The goal of this repo is to preserve my work, organize my scripts, share development progress, and provide both release-ready Lua builds and modular source files where possible.

Projects in this repository may include:

- Drift and vehicle handling scripts
- DriftGod development builds
- SuperDrive / momentum experiments
- Experimental traction and grip tuning
- Stunt and trick systems
- PTFX / particle effect testing
- HUD and intro UI experiments
- Vehicle tools
- Minigame-style concepts
- Utility scripts
- Modular Lua source folders
- Built single-file Lua releases

Some scripts are polished.  
Some scripts are experimental.  
Some scripts are kept for archival, testing, or reference purposes.

Use them with that in mind.

---

## Featured Project: DriftGod

**DriftGod** is a Cherax Lua drifting project focused on creating a more stylish, arcade-like, and customizable drifting experience in GTA V.

The project was inspired by older mod-menu drifting systems from the Impulse / 2Take1 era, with the goal of bringing back that type of fun drifting feel while expanding it with new systems, tuning options, visuals, stunts, HUD elements, and experimentation.

### DriftGod Preview

YouTube preview:  
https://www.youtube.com/watch?v=0s6jtqomePs&t=9s

### DriftGod Goals

DriftGod is built around the idea of making drifting feel:

- Fun
- Stylish
- Tunable
- Arcade-like
- Momentum-friendly
- Showcase-friendly
- Experimental
- Easy to iterate on

It is not meant to be a perfect simulation drift system.  
It is meant to feel fun, expressive, and customizable.

---

## DriftGod Features

Depending on the build, DriftGod may include:

- Custom drift tuning
- Experimental traction controls
- Experimental grip controls
- SuperDrive momentum support
- Camera-based direction experiments
- Vehicle-based direction experiments
- Stunt and trick systems
- Drift scoring logic
- Collision / slide-out run handling
- Intro HUD
- Logo intro display
- Startup ASCII banner
- Build/version logging
- PTFX and particle effect experiments
- Stunt safety caps
- Modular source structure
- Built single-file release builds

Because DriftGod is still actively being developed, features may change between builds.

---

## Release Types

Projects in this repository may use release tags to make development status clear.

These tags may appear in file names, README notes, changelogs, or startup logs.

### ALPHA

**ALPHA** builds are active development builds.

These builds may contain:

- New experimental systems
- Debug tools
- Partially tested features
- Unfinished cleanup
- Rapid prototype code
- Known rough edges
- Behavior that may change quickly

```

ALPHA builds are useful for testing ideas, gathering logs, and rapidly improving features.

### BETA

**BETA** builds are more stable than alpha builds, but they may still contain bugs.

These builds are intended for wider testing once major systems are mostly working.

Example:

```txt
DriftGod v6.13.xx BETA
```

BETA builds should be cleaner than alpha builds, but still may need feedback and polish.

### RELEASE

**RELEASE** builds are intended to be stable public builds.

These should have:

- Less debug spam
- Cleaner menus
- More consistent behavior
- Fewer experimental leftovers
- Better documentation
- More reliable startup logs

Example:

```txt
DriftGod v1.0.0 RELEASE
```

---

## Built Releases vs Modular Source

Some projects may include both **built release files** and **modular source files**.

### Built Releases

Built releases are usually one large Lua file designed for easy loading, sharing, or submission.

Example:

```txt
releases/
  DriftGod_Release.lua
```

A built release may be generated from multiple smaller Lua modules.

The goal of a built release is convenience:

- Easier to upload
- Easier to load
- Easier to share
- Better for platforms that only accept one Lua file

### Modular Source

Modular source is the development version of a project.

Example:

```txt
DriftGod/
  core/
  systems/
  ui/
  data/
  assets/
```

Modular source is easier to:

- Debug
- Maintain
- Refactor
- Update
- Organize
- Understand system-by-system

For larger projects like DriftGod, modular source is much cleaner than keeping everything in one huge Lua file during development.

### Why Both Exist

The modular version is for development.  
The built version is for release.

This allows the project to stay organized while still supporting single-file release builds when needed.

---

## Assets

Some scripts may use external assets such as images, icons, or other media files.

Example:

```txt
DriftGod/assets/DriftGod.png
```

Assets may be handled in one of several ways:

- Included directly in the repository
- Downloaded from a hosted location
- Cached locally on first run
- Referenced by the Lua script from an `assets` folder
- Disabled or replaced in single-file builds if needed

For DriftGod, image assets such as the logo may be stored in an assets folder or hosted separately and downloaded/cached by the script.

A typical asset path may look like:

```txt
Documents/Cherax/Lua/DriftGod/assets/DriftGod.png
```

If a release build requires assets, the script or README should explain where those assets belong.

---

## AI Assistance Transparency

Some parts of these projects were developed with assistance from AI tools such as ChatGPT.

AI was used as a coding assistant for:

- Prototyping
- Refactoring
- Debugging
- Documentation
- Build organization
- Code cleanup
- Explaining errors
- Testing ideas faster
- Converting large systems into cleaner structures

However, the project concepts, feature direction, in-game testing, tuning decisions, cleanup choices, and final behavior were manually directed and reviewed.

These scripts are not intended to be blind AI-generated dumps.

They are actively tested, adjusted, and maintained through real in-game use.

### What This Means

AI assistance may have helped generate or refactor portions of code, but the projects were shaped through:

- Manual testing
- Game logs
- In-game behavior checks
- Repeated bug fixing
- Feature removal when something did not work
- Iterative tuning
- Personal design decisions
- Community feedback
- Practical Cherax testing

The goal is to use AI as a tool, not as a replacement for testing, judgment, or ownership.

---

## Development Notes

This repository may contain projects at different stages of completion.

Some files may be:

- Experimental
- Deprecated
- Partially tested
- Kept for reference
- In active development
- Intended only for debugging
- Older versions preserved for comparison

Development builds may include debug logs, test menus, or systems that are later removed.

Release builds should be cleaner and may remove:

- Debug spam
- Broken experiments
- Duplicate systems
- Test-only buttons
- Unused fallback code
- Old prototype behavior

---

## Code Style Goals

The long-term goal is to keep the code clean, readable, and consistent.

Preferred style:

```lua
DG.SuperDriveTick()
DG.ApplyExperimentalGrip()
DG.StartIntroHud()
DG.ClampStuntForce()
DG.ResetRunState()
```

The `DG.` namespace is used to keep DriftGod functions grouped, searchable, and easy to identify.

Good comments should explain **why** something exists, especially when it came from a past bug or design change.

Example:

```lua
-- Past issue:
-- A/D yaw assist made steering feel unnatural, so DriftGod no longer
-- modifies A/D. GTA handles normal steering now.
```

Comments should be useful when revisiting the code later.

The goal is not to over-comment obvious code.  
The goal is to document important decisions, fixes, and lessons learned.

---

## DriftGod Development Philosophy

DriftGod is built through trial, testing, and iteration.

Many systems have gone through multiple versions, including:

- SuperDrive behavior
- A/D steering behavior
- Experimental traction
- Experimental grip
- Intro logo rendering
- Startup HUD timing
- Stunt force balancing
- PTFX testing
- Asset loading
- Modular source organization
- Single-file release planning

Some ideas worked.  
Some ideas were removed.  
Some ideas were kept only after repeated testing.

That development history is part of the project.

---

## Startup Logs and Build Info

DriftGod builds may print version information when loaded.

Example:

```txt
============================================================
DRIFTGOD
Drift Like a God
============================================================
Author: Animus / xReVoLTiThemeDev
Discord: animusx1337
Repo: https://github.com/xReVoLTiThemeDev/GTAV-Cherax
Version: v6.12.xx
Channel: ALPHA
Build: 2026.xx.xx.xxx
Last Updated: 2026-xx-xx
============================================================
```

This helps identify which build someone is using when reporting issues.

Useful log fields include:

- Project name
- Author
- Discord username
- GitHub repo
- Version
- Build channel
- Build number
- Last update date

This is especially useful for debugging community reports.

---

## Repository Structure

The repository may evolve over time, but a typical structure may look like:

```txt
GTAV-Cherax/
  README.md
  LICENSE
  .gitignore

  DriftGod/
    core/
    systems/
    ui/
    data/
    assets/

  releases/
    DriftGod_Release.lua

  tools/
    builder/
      build.lua

  docs/
    changelogs/
    notes/
```

Possible folder purposes:

```txt
core/       Base config, state, save, utility, boot logic
systems/    Gameplay systems such as drift, stunts, SuperDrive, grip
ui/         Menus, HUD, intro screens, visual overlays
data/       Presets, trick lists, ranks, tips, unlocks
assets/     Images, icons, logos, media files
releases/   Built one-file Lua releases
tools/      Builder scripts or helper tools
docs/       Notes, changelogs, development logs
```

---

## Building Single-File Lua Releases

Some projects may eventually use a builder script that combines modular source files into one large Lua file.

Example:

```txt
Input:
DriftGod/core/config.lua
DriftGod/systems/superdrive.lua
DriftGod/ui/menu.lua

Output:
releases/DriftGod_Release.lua
```

A builder may:

- Read files in the correct load order
- Combine modules into one Lua file
- Strip development-only comments if needed
- Keep release headers
- Keep version/build information
- Preserve required startup logic
- Exclude private/debug-only files

This allows development to remain modular while still supporting one-file submissions.

---

## Credits

Created by:

```txt
Animus / xReVoLTiThemeDev
Discord: animusx1337
GitHub: xReVoLTiThemeDev
```

Special thanks to:

- The GTA V modding community
- The Cherax Lua community
- People who provide testing ideas, feedback, and native references
- Community members who help explain better Lua practices
- Anyone who reports bugs, shares logs, or helps improve the project

---

## Disclaimer

These scripts are provided for educational, archival, and personal modding purposes.

Use at your own risk.

I am not responsible for:

- Game crashes
- Broken sessions
- Lost settings
- Corrupted configs
- Unexpected behavior
- Bans
- Account issues
- Network issues
- Conflicts with other Lua scripts
- Conflicts with Cherax updates
- Conflicts with GTA V updates

Scripts may break after updates to GTA V, Cherax, Lua APIs, natives, or related tools.

Always test carefully.

---

## License

This repository is intended to be open source.

See the repository license file for usage terms.

Recommended license for this type of project:

```txt
GPL-3.0
```

GPL-3.0 helps keep modified/distributed versions open-source as well.

If a different license is used, refer to the license file included in the repository.

---

## Final Notes

This repository is a work in progress.

Some projects are polished.  
Some projects are experimental.  
Some projects are archived for reference.  

The main goal is to document, preserve, and improve my GTA V Cherax Lua work over time.

If you are using one of these scripts, make sure you are using the correct build type:

```txt
ALPHA   = experimental
BETA    = testing
RELEASE = stable
```

And when reporting issues, please include:

```txt
Script name
Version
Build channel
Build number
Cherax log
What you were doing
What happened
Whether other Lua scripts were loaded
```
