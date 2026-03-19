[![English](https://img.shields.io/badge/English-Click_to_View-blue)](./README.en.md)
[![中文](https://img.shields.io/badge/中文-当前-green)](./README.md)
[![Install](https://img.shields.io/badge/Install-Guide-orange)](#安装)
[![Structure](https://img.shields.io/badge/Structure-Architecture-purple)](#仓库结构)
[![Release](https://img.shields.io/github/v/release/harrymarin/ios26-liquidglass-swiftui?style=flat-square)](https://github.com/harrymarin/ios26-liquidglass-swiftui/releases)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](./LICENSE)

# iOS 26 Liquid Glass SwiftUI

`ios26-liquidglass-swiftui` 是一个可分发的 Codex skill，用来指导 AI coding agent 将 SwiftUI 页面改造成 iOS 26 Liquid Glass 风格。

它聚焦于使用原生 SwiftUI / iOS 26 能力来实现 Liquid Glass 体验，而不是依赖自定义模糊层、伪玻璃特效或不可维护的视觉 hack。

## 快速导航

- [为什么做这个 skill](#为什么做这个-skill)
- [适用场景](#适用场景)
- [核心 API / 模式](#核心-api--模式)
- [快速开始](#快速开始)
- [安装](#安装)
- [使用](#使用)
- [仓库结构](#仓库结构)

## 快速开始

1. 下载仓库或 release zip
2. 把目录复制到 `~/.codex/skills/`
3. 在对话里调用 `$ios26-liquidglass-swiftui`
4. 提供 SwiftUI 页面或组件上下文

示例：

```text
Use $ios26-liquidglass-swiftui to refactor this SwiftUI screen into an iOS 26 Liquid Glass style.
```

## 为什么做这个 skill

很多所谓 “Liquid Glass 风格” 最后只是 blur、透明度和渐变的叠加。这个 skill 的目标不是做“像玻璃”的视觉，而是帮助 agent 用更接近 iOS 26 原生设计语言的方式去实现真正可交付的 SwiftUI 界面。

## 适用场景

- 把现有 SwiftUI 页面改成 iOS 26 Liquid Glass 风格
- 为 tab bar、toolbar、sheet 和高优先级操作加入原生 glass 语义
- 为相关控件加入 glass morphing transition
- 检查页面的 Liquid Glass 实现是否符合 iOS 26 语义

## 核心 API / 模式

- `glassEffect()`
- `GlassEffectContainer`
- `glassEffectID(_:in:)`
- `.buttonStyle(.glass)`
- `.buttonStyle(.glassProminent)`

## 安装

```bash
mkdir -p ~/.codex/skills
cp -R ios26-liquidglass-swiftui ~/.codex/skills/
```

如果你拿到的是 zip 包，可以先解压再复制：

```bash
unzip ios26-liquidglass-swiftui.zip
cp -R ios26-liquidglass-swiftui ~/.codex/skills/
```

## 使用

```text
Use $ios26-liquidglass-swiftui to refactor this SwiftUI screen into an iOS 26 Liquid Glass style.
```

或者直接使用自然语言：

```text
把这个 SwiftUI 页面改成 iOS 26 Liquid Glass 风格
```

## 仓库结构

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
