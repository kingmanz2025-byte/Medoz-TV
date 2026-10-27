# Medoz TV — Home Screen & Themes Specification

## Identity
- Deep navy background; gold for focus, selection, and key indicators.
- White/ivory primary text and muted secondary text.
- Arabic-first typography and consistent RTL alignment.
- Cinematic, premium composition rather than generic flat tiles.

## Layout
1. Fixed sidebar with active-section highlight.
2. Header with clock, Arabic date, and optional selected city/status.
3. Large hero area with suitable artwork, overlay, title, and one primary action.
4. Service cards for Quran, Azkar, Ruqyah, Radio, Local Audio, Prayer Times, Favorites, and Settings.
5. Prayer schedule with next prayer highlighted.
6. Compact weather card.

## Cards
Use consistent spacing, corner radius, and image treatment. Include normal, focused, selected, disabled, and unavailable states as needed. Keep titles short and readable. Avoid making every card dominant at once.

## Remote focus
- Directional navigation must be predictable.
- Use a clearly visible gold focus state.
- Focus movement must not activate an item; OK activates.
- Restore focus sensibly when returning from a screen.

## Themes and backgrounds
- Default theme: Medoz Navy & Gold.
- Additional themes and local backgrounds may be supported.
- Provide preview and restore-default options.
- Preserve text contrast and controls above imagery.
- Cache appropriately sized assets where permitted.
- Fall back to the default background if an image fails.

## Performance and viewport
- Optimize image size and avoid excessive blur, transparency, and animation.
- Keep content within the safe visible area.
- Test overscan and actual viewport dimensions on the target TV.
- Provide static fallbacks for unsupported effects.

## Empty and error states
Handle no favorites, no local files, missing prayer configuration, unavailable weather, and offline mode with concise Arabic messages and useful actions.

## Acceptance criteria
The sidebar, cards, clock, prayer schedule, and weather do not overlap; all core functions are reachable by remote; theme settings persist where supported; and performance is acceptable on the target TV.
