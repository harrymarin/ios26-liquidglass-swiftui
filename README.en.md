[![English](https://img.shields.io/badge/English-Current-green)](./README.en.md)
[![中文](https://img.shields.io/badge/中文-点击查看-blue)](./README.md)
[![Install](https://img.shields.io/badge/Install-Guide-orange)](#installation)
[![Structure](https://img.shields.io/badge/Structure-Architecture-purple)](#repository-structure)
[![Release](https://img.shields.io/github/v/release/harrymarin/ios26-liquidglass-swiftui?style=flat-square)](https://github.com/harrymarin/ios26-liquidglass-swiftui/releases)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](./LICENSE)

# iOS 26 Liquid Glass SwiftUI

`ios26-liquidglass-swiftui` is a distributable Codex skill for guiding AI coding agents to refactor SwiftUI screens into the iOS 26 Liquid Glass style.

It focuses on native SwiftUI / iOS 26 APIs rather than custom blur stacks, fake glass effects, or hard-to-maintain visual hacks.

## Quick Navigation

- [Why This Skill Exists](#why-this-skill-exists)
- [Good Fit For](#good-fit-for)
- [Core APIs / Patterns](#core-apis--patterns)
- [Quick Start](#quick-start)
- [Installation](#installation)
- [Usage](#usage)
- [Repository Structure](#repository-structure)

## Quick Start

1. Download the repo or release zip
2. Copy the folder into `~/.codex/skills/`
3. Invoke `$ios26-liquidglass-swiftui`
4. Provide the SwiftUI screen or component context

Example:

```text
Use $ios26-liquidglass-swiftui to refactor this SwiftUI screen into an iOS 26 Liquid Glass style.
```

## Why This Skill Exists

Many so-called “Liquid Glass” implementations end up being stacks of blur, opacity, and gradients. This skill is meant to help agents produce SwiftUI work that feels aligned with the iOS 26 design language and is suitable for real delivery.

## Good Fit For

- refactoring an existing SwiftUI screen into the iOS 26 Liquid Glass style
- adding native glass semantics to tab bars, toolbars, sheets, and high-priority actions
- introducing glass morphing transitions for related controls
- reviewing whether a Liquid Glass implementation matches iOS 26 semantics

## Core APIs / Patterns

- `glassEffect()`
- `GlassEffectContainer`
- `glassEffectID(_:in:)`
- `.buttonStyle(.glass)`
- `.buttonStyle(.glassProminent)`

## Installation

```bash
mkdir -p ~/.codex/skills
cp -R ios26-liquidglass-swiftui ~/.codex/skills/
```

If you received a zip archive, unzip it first:

```bash
unzip ios26-liquidglass-swiftui.zip
cp -R ios26-liquidglass-swiftui ~/.codex/skills/
```

## Usage

```text
Use $ios26-liquidglass-swiftui to refactor this SwiftUI screen into an iOS 26 Liquid Glass style.
```

## Repository Structure

```text
ios26-liquidglass-swiftui/
├── SKILL.md
├── README.md
├── README.en.md
├── LICENSE
├── agents/
│   └── openai.yaml
└── references/
    ├── quick-reference.md
    └── checklist.md
```

## License

MIT
