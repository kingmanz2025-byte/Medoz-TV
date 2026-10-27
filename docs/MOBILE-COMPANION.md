# Medoz TV — Mobile Companion Specification

## Purpose
A companion app may help users discover a compatible TV, view connection status, and provide remote controls where permitted by the TV platform.

## Discovery and connection
- Offer device discovery only using a supported, documented mechanism.
- Allow manual IP entry when the chosen connection method supports it.
- Show connection status, target TV identity when available, and actionable errors.
- Require user consent before pairing or sending commands.
- Never silently scan unrelated networks or collect credentials.

## Remote controls
- Provide a directional pad, OK, Back, and any additional controls confirmed to work on the target device.
- Keep controls large enough for touch.
- Clearly indicate when a command is unavailable.
- Do not promise system-level volume, keyboard injection, app launching, or remote installation until each is verified for the specific Tizen version and security settings.

## Installation assistance
- Explain supported developer-mode or authorized installation steps if applicable.
- Do not bypass Samsung security, signing, pairing, or platform restrictions.
- Treat direct installation as an optional capability requiring explicit compatibility testing.
- Provide clear instructions and recovery guidance if installation is unsupported.

## Privacy and security
- Store only necessary connection preferences.
- Explain what data is stored and why.
- Do not transmit local audio or personal information without explicit user action.
- Provide a way to remove saved TV entries.
- Use authenticated or platform-approved connections wherever available.

## Acceptance criteria
- Pairing requires user action.
- Connection failures are explained.
- Remote commands are tested against the target TV.
- Unsupported functions are clearly disabled or omitted.
