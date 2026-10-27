# Medoz TV — Offline, Privacy & Security

## Offline-first behavior
Keep the dashboard, saved preferences, theme selection, favorites, and supported local media available offline. Prayer data may be cached only with date/validity checks. Weather and internet streams require connectivity.

## Data minimization
- Store only settings required for app operation.
- Do not collect precise location unless supported, necessary, and explicitly permitted.
- Manual city selection must remain available.
- Do not upload local files or playback history without clear consent.
- Avoid analytics or tracking by default.

## Local storage
- Use platform-supported storage mechanisms.
- Handle corrupted or missing settings gracefully.
- Provide reset options for user preferences.
- Do not store secrets or provider credentials in plain-text logs.

## Network behavior
- Use trusted endpoints and encrypted transport where supported.
- Set reasonable timeouts.
- Avoid unnecessary polling and infinite retry loops.
- Explain network-dependent features.

## Family controls
A local PIN or profile lock may be considered. It must be described as an in-app restriction, not a substitute for Samsung system-level parental controls.

## Acceptance criteria
The app remains responsive offline, handles invalid cached data safely, does not request unnecessary permissions, and explains what data is stored.
