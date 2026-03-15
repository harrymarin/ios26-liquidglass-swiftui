# ios26-liquidglass-swiftui

[English](#english) | [中文](#中文)

---

## 中文

`ios26-liquidglass-swiftui` 是一个可分发的 Codex skill，用来指导 AI coding agent 将 SwiftUI 页面改造成 iOS 26 Liquid Glass 风格。

它聚焦于使用原生 SwiftUI / iOS 26 能力来实现 Liquid Glass 体验，而不是依赖自定义模糊层、伪玻璃特效或不可维护的视觉 hack。

### 特性

- 聚焦 iOS 26 原生 Liquid Glass API
- 面向 SwiftUI 页面重构和新页面开发
- 提供实现 workflow、快速参考和交付检查清单
- 可直接安装到 `~/.codex/skills/`

### 包含内容

```text
ios26-liquidglass-swiftui/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── quick-reference.md
    └── checklist.md
```

### 适用场景

- 把现有 SwiftUI 页面改成 iOS 26 Liquid Glass 风格
- 为 tab bar、toolbar、sheet 和高优先级操作加入原生 glass 语义
- 为相关控件加入 glass morphing transition
- 检查页面的 Liquid Glass 实现是否符合 iOS 26 语义

### 核心 API / 模式

- `glassEffect()`
- `GlassEffectContainer`
- `glassEffectID(_:in:)`
- `.buttonStyle(.glass)`
- `.buttonStyle(.glassProminent)`

### 安装

```bash
mkdir -p ~/.codex/skills
cp -R ios26-liquidglass-swiftui ~/.codex/skills/
```

如果你拿到的是 zip 包，可以先解压再复制：

```bash
unzip ios26-liquidglass-swiftui.zip
cp -R ios26-liquidglass-swiftui ~/.codex/skills/
```

### 使用

```text
Use $ios26-liquidglass-swiftui to refactor this SwiftUI screen into an iOS 26 Liquid Glass style.
```

或者直接使用自然语言：

```text
把这个 SwiftUI 页面改成 iOS 26 Liquid Glass 风格
```

### 为什么做这个 skill

很多所谓 “Liquid Glass 风格” 最后只是 blur、透明度和渐变的叠加。这个 skill 的目标不是做“像玻璃”的视觉，而是帮助 agent 用更接近 iOS 26 原生设计语言的方式去实现真正可交付的 SwiftUI 界面。

---

## English

`ios26-liquidglass-swiftui` is a distributable Codex skill for guiding AI coding agents to refactor SwiftUI screens into the iOS 26 Liquid Glass style.

It focuses on native SwiftUI / iOS 26 APIs rather than custom blur stacks, fake glass effects, or hard-to-maintain visual hacks.

### Features

- Focused on native iOS 26 Liquid Glass APIs
- Built for SwiftUI refactors and new screen implementation
- Includes workflow guidance, a quick reference, and a delivery checklist
- Easy to install into `~/.codex/skills/`

### Package Contents

```text
ios26-liquidglass-swiftui/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── quick-reference.md
    └── checklist.md
```

### Good Fit For

- Refactoring an existing SwiftUI screen into the iOS 26 Liquid Glass style
- Adding native glass semantics to tab bars, toolbars, sheets, and high-priority actions
- Introducing glass morphing transitions for related controls
- Reviewing whether a Liquid Glass implementation matches iOS 26 semantics

### Main APIs / Patterns Covered

- `glassEffect()`
- `GlassEffectContainer`
- `glassEffectID(_:in:)`
- `.buttonStyle(.glass)`
- `.buttonStyle(.glassProminent)`

### Installation

```bash
mkdir -p ~/.codex/skills
cp -R ios26-liquidglass-swiftui ~/.codex/skills/
```

If you received a zip archive, unzip it first:

```bash
unzip ios26-liquidglass-swiftui.zip
cp -R ios26-liquidglass-swiftui ~/.codex/skills/
```

### Usage

```text
Use $ios26-liquidglass-swiftui to refactor this SwiftUI screen into an iOS 26 Liquid Glass style.
```

### Why This Exists

Many so-called “Liquid Glass” implementations end up being stacks of blur, opacity, and gradients. This skill is meant to help agents produce SwiftUI work that feels aligned with the iOS 26 design language and is suitable for real delivery.
