---
name: ios26-liquidglass-swiftui
description: Use when building or refactoring iOS 26 SwiftUI interfaces that need Liquid Glass styling, glass morphing transitions, or system glass controls such as tab bars, toolbars, sheets, and glass buttons.
---

# iOS 26 Liquid Glass in SwiftUI

## Overview

Implement Liquid Glass with native iOS 26 SwiftUI APIs, not custom blur stacks. Favor semantic structure first, then add glass to interactive surfaces that should float above content.

Read `references/quick-reference.md` when selecting APIs.
Read `references/checklist.md` before finalizing UI behavior.

## Workflow

1. Confirm the feature truly targets iOS 26.
2. Map interaction surfaces that should use glass: navigation bars, tab bars, toolbars, sheets, and high-priority actions.
3. Apply core APIs (`glassEffect`, glass button styles, and container-level patterns) to those surfaces only.
4. Add morphing with shared IDs where controls change size, position, or context.
5. Validate accessibility, contrast, reduce-transparency behavior, and performance.

## Core Rules

- Prefer system components first. Let iOS manage adaptive glass behavior in bars, sheets, and menus.
- Use `glassEffect()` for standalone custom surfaces.
- Use `GlassEffectContainer` to coordinate nearby glass items and improve blending/morphing behavior.
- Use `glassEffectID(_:in:)` with a shared `Namespace` to morph related controls across state transitions.
- Use `.buttonStyle(.glass)` or `.buttonStyle(.glassProminent)` for tappable controls.
- Keep glass layers sparse. Overuse reduces hierarchy clarity and can hurt frame pacing.

## SwiftUI Patterns

### Basic glass surface

```swift
VStack(spacing: 12) {
    Text("Daily Move")
        .font(.headline)
    Text("742 kcal")
        .font(.title2.weight(.semibold))
}
.padding(16)
.glassEffect()
```

### Glass buttons

```swift
HStack(spacing: 12) {
    Button("Start") {
        startWorkout()
    }
    .buttonStyle(.glassProminent)

    Button("Details") {
        showDetails = true
    }
    .buttonStyle(.glass)
}
```

### Morph between related controls

```swift
@Namespace private var glassNamespace

GlassEffectContainer(spacing: 10) {
    if expanded {
        ExpandedPlayerView()
            .glassEffect()
            .glassEffectID("player", in: glassNamespace)
    } else {
        MiniPlayerView()
            .glassEffect()
            .glassEffectID("player", in: glassNamespace)
    }
}
.animation(.spring(response: 0.45, dampingFraction: 0.85), value: expanded)
```

## Implementation Guardrails

- Avoid layering custom `Material`, blur, and gradients on top of Liquid Glass unless a requirement explicitly needs it.
- Do not force glass on every card. Reserve it for controls, chrome, and elevated interaction surfaces.
- Keep hit targets and content legible when glass sits over dynamic imagery.
- Preserve semantic focus order and VoiceOver labels when introducing animated glass transitions.
- If deployment target is below iOS 26, implement a clearly scoped fallback path instead of partial Liquid Glass behavior.

## Completion Standard

Before claiming completion, run the checklist in `references/checklist.md` and confirm:
- expected API usage matches intent,
- transitions are stable,
- accessibility and performance checks are complete.
