# Medoz TV — Final Design Specification

## Product identity
- Product: Medoz TV
- Target: Samsung Tizen Smart TV; first target device reported as Samsung UA7000, 58-inch. Exact model code and Tizen version must be verified on-device.
- Language: Arabic-first, RTL.
- Business model: free, no in-app subscriptions or paid themes; no in-app ads are intended.
- Visual identity: premium navy and gold, cinematic background, fixed sidebar, large rich cards.

## Dashboard regions
1. Fixed sidebar and active-section marker.
2. Header with local clock and Arabic date.
3. Hero panel with artwork, short text, and primary action.
4. Service cards: Quran, Azkar, Ruqyah, Radio, Local Audio, Prayer Times, Favorites, Settings.
5. Prayer schedule with next prayer highlighted.
6. Compact weather card.

## Interaction
- Direction keys move focus; OK activates; Back returns predictably.
- Gold focus indicator must be visible from normal viewing distance.
- Focus and activation are separate states.
- Preserve sensible focus when returning from a screen.

## Time display
Use a 12-hour clock with Arabic ص/م. Show Arabic date. Use device time zone only when available and valid.

## Themes
Default theme is Medoz Navy & Gold. Additional free themes and local backgrounds may be supported. Maintain readable contrast, offer restore-default, and fall back safely if an image fails.

## Offline-first goals
The UI, saved preferences, favorites, supported local audio, and valid cached prayer data should remain usable offline where platform capabilities allow. Online radio, refreshed weather, and online IPTV data require connectivity.

## Compatibility disclaimer
This specification does not guarantee support for every Samsung TV, Tizen version, installation method, casting protocol, background audio behavior, or system-level remote command. Verify on the target device.
