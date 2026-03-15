# Quick Reference: iOS 26 Liquid Glass (SwiftUI)

## API Selection

- `glassEffect()`
  Use for custom floating surfaces that should adopt Liquid Glass appearance.

- `GlassEffectContainer(spacing:content:)`
  Use to group nearby glass elements so blending and coordinated transitions behave naturally.

- `glassEffectID(_:in:)`
  Use with a shared `Namespace` to morph related elements across view state changes.

- `.buttonStyle(.glass)`
  Use for secondary actions that should keep standard glass affordance.

- `.buttonStyle(.glassProminent)`
  Use for primary actions needing stronger emphasis.

## System Surfaces

- Tab bars, navigation bars, toolbars, sheets, and menus gain native glass behavior in iOS 26.
- Prefer system containers before building custom chrome.
- Add custom glass only where system behavior does not cover the interaction need.

## Morphing Recipe

1. Create one shared namespace.
2. Wrap related controls in `GlassEffectContainer`.
3. Assign the same `glassEffectID` to source and destination views.
4. Animate state changes with a spring curve and verify continuity.

## Performance Notes

- Limit simultaneous glass layers on screen.
- Avoid stacked translucency effects that compete with system rendering.
- Profile animation-heavy scenes on device, not only simulator.

## Accessibility Notes

- Verify text/icon contrast over variable backgrounds.
- Check VoiceOver order during morph transitions.
- Validate behavior with Reduce Transparency enabled.
