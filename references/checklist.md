# Liquid Glass Delivery Checklist (SwiftUI)

## Pre-Implementation

- Confirm minimum deployment target includes iOS 26 for Liquid Glass APIs.
- Identify exactly which surfaces need glass semantics.
- Decide which views need morphing continuity.

## Implementation

- Use `glassEffect()` only on selected elevated surfaces.
- Use `GlassEffectContainer` for groups of related glass elements.
- Use `glassEffectID(_:in:)` for source/destination morph pairs.
- Use `.buttonStyle(.glass)` or `.buttonStyle(.glassProminent)` for actions.
- Avoid custom blur stacks unless explicitly required.

## Verification

- Confirm animations remain stable across repeated state toggles.
- Confirm touch targets remain clear and reliable.
- Confirm no clipped corners or visual seams while animating.
- Confirm bars/sheets still behave natively after custom glass additions.

## Accessibility

- Check contrast in light and dark appearances.
- Check VoiceOver labels, order, and actionable hints.
- Check Reduce Transparency behavior.
- Check Dynamic Type overlap or truncation on glass surfaces.

## Performance

- Profile on a physical device for transition-heavy views.
- Check scrolling and animation frame pacing with glass enabled.
- Reduce unnecessary overlapping glass layers when frame drops appear.
