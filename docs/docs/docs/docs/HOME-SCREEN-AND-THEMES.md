# Medoz TV — Home Screen & Themes Specification

## 1. Purpose

Define the home screen layout, visual hierarchy, theme customization, background behavior, and remote-control focus states for Medoz TV.

The application must retain the approved premium cinematic identity: deep navy backgrounds, elegant gold accents, Arabic RTL layout, and rich visual cards.

## 2. Core Visual Identity

### Primary palette

- Deep navy: primary application background.
- Dark blue-gray: secondary panels and cards.
- Gold: selected items, focus borders, important indicators, and key actions.
- White or soft ivory: primary text.
- Muted gray: secondary labels and unavailable information.

Exact color values should be centralized in theme variables so they can be adjusted without rewriting individual screens.

### Visual principles

- Premium and cinematic, not flat or generic.
- Clear contrast between the background, cards, and text.
- Consistent spacing and alignment.
- Restrained use of gold so important controls remain visually distinct.
- Arabic-first typography with proper RTL alignment.
- Large text and controls suitable for viewing from a couch.
- No unnecessary clutter or excessive animation.

## 3. Home Screen Layout

The home screen must include the following regions.

### A. Fixed Sidebar

- Keep the primary navigation in a fixed sidebar.
- Preserve its position while the main content changes.
- Highlight the active section using the gold accent.
- Show a clear focus indicator when navigating with the remote.
- Keep labels readable and avoid overcrowding.
- On a narrow viewport, adapt the sidebar only when necessary and preserve remote navigation.

### B. Header Area

Display:

- Current time in 12-hour format with ص/م.
- Current date in Arabic.
- Selected city when useful.
- A compact connection or data-status indicator when needed.

The header must not overlap the sidebar, weather card, or prayer schedule.

### C. Main Hero Area

Use a large cinematic visual area for the featured section or selected content.

Requirements:

- High-quality background imagery where available.
- A subtle dark overlay behind text.
- Strong text contrast.
- A clear title and short description.
- A primary action with a visible focus state.
- No automatic video playback unless explicitly enabled and supported.

Background imagery must not make text unreadable or slow down the dashboard unnecessarily.

### D. Prayer Schedule

- Display the six entries in the specified order: Fajr, sunrise, Dhuhr, Asr, Maghrib, and Isha.
- Sunrise must be identified as informational, not as an obligatory prayer.
- Highlight the next upcoming prayer.
- Use the 12-hour Arabic time format.
- Avoid overlapping labels on smaller supported TV viewports.

### E. Weather Card

- Keep the weather card compact.
- Show the selected city, temperature, condition, and suitable icon when valid data is available.
- Indicate unavailable or outdated information clearly.
- Never show invented weather data.

### F. Service Cards

The home screen may display cards for:

- القرآن الكريم.
- الأذكار.
- الرقية الشرعية.
- الراديو.
- الملفات الصوتية.
- مواقيت الصلاة.
- المفضلة.
- إعدادات التطبيق.

Additional approved services may be added without overcrowding the home screen.

## 4. Card Design

Cards must look like part of one premium design system.

- Use consistent corner radii and spacing.
- Use high-quality icons or suitable artwork.
- Keep titles short and readable.
- Provide normal, focused, selected, disabled, and unavailable states where relevant.
- Use gold for important focus and selection states.
- Avoid excessive borders, gradients, and decorative effects.
- Do not make every card visually dominant at the same time.

The main service cards should be visually rich enough to match the approved reference design.

## 5. Remote Focus and Selection

When the user presses the directional buttons:

- Move focus predictably between visible interactive elements.
- Display a distinct gold focus border or equivalent high-contrast indicator.
- Avoid changing the selected section simply because focus moves over it.
- Activate an item only after the user presses OK.
- Preserve a logical focus order when content changes.
- Restore focus to a sensible location after returning from a service.
- Prevent focus from becoming invisible or trapped in a hidden element.

Back must return to the previous screen or section according to a consistent navigation model.

## 6. Theme Customization

Provide a theme settings section that can support:

- The default Medoz navy-and-gold theme.
- Additional approved color variations.
- Background selection from supported local images.
- Restore-default-theme action.
- Persistence of the selected theme between sessions.

### Theme safety rules

- The default Medoz identity remains the primary theme.
- Theme changes must not reduce text contrast below an acceptable level.
- Background images must not cover or obscure controls.
- If a selected image cannot be loaded, fall back to the default background.
- Do not promise access to every folder or external storage device; that depends on the TV platform.

## 7. Background Performance

- Prefer appropriately sized and compressed images.
- Avoid downloading large images on every dashboard visit.
- Cache assets when permitted.
- Keep animations subtle and optional.
- Respect the TV's available memory and rendering performance.
- Avoid excessive blur, transparency, and layered effects if they cause performance issues.
- Provide a static fallback when animation or media is unsupported.

## 8. Responsive Layout

The interface must be tested at the actual supported Samsung TV resolution and viewport.

- Use a layout that adapts to the available viewport.
- Keep important content inside the visible screen area.
- Avoid clipping at the edges.
- Do not assume that every Samsung TV uses the same browser behavior or available resolution.
- Check overscan and safe-area behavior on the target device.
- Keep text and remote focus indicators visible at all times.

## 9. Loading and Empty States

The home screen must remain visually complete when some services have no data.

Examples:

- No favorites yet.
- No local audio files available.
- Weather data unavailable.
- Prayer schedule not configured.
- Internet disconnected.

Use concise Arabic messages and clear actions where appropriate. Do not leave empty cards or broken-image placeholders.

## 10. Accessibility and Usability

- Maintain readable text contrast.
- Use Arabic RTL consistently.
- Avoid controls that require a mouse or touchscreen.
- Make focus states clearly visible.
- Keep primary actions easy to reach.
- Avoid relying on color alone to communicate errors or status.
- Use consistent terminology throughout the application.

## 11. Acceptance Criteria

The home screen is ready for testing when:

- The overall layout matches the approved design direction.
- The sidebar remains fixed and usable.
- The clock, date, prayer schedule, and weather card do not overlap.
- All primary services can be reached using the remote.
- Gold focus indicators remain visible.
- Theme and background settings persist where supported.
- The interface remains usable when offline or when data is missing.
- Rendering performance is acceptable on the target Samsung TV.

## 12. Design Approval Gate

Before implementation begins, compare the implemented home screen against the approved visual reference.

Any major change to the sidebar, card hierarchy, palette, or dashboard layout must be reviewed before being treated as the final design.
