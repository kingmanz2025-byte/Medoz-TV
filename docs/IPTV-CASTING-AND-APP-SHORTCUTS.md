# Medoz TV — IPTV, Casting & App Shortcuts

## IPTV sources
- Support only user-provided or otherwise authorized IPTV sources and compatible formats.
- Do not bundle unauthorized channel lists, credentials, or paid content.
- Do not promise compatibility with every M3U, HLS, DASH, DRM, or provider configuration.
- Validate supported formats on the target Tizen version.
- Keep source configuration transparent and protect sensitive credentials.

## Playback behavior
- Show channel name and clear loading, playing, buffering, and error states.
- Provide retry and a way to remove a source.
- Avoid indefinite retries and background network loops.
- Explain when a source or codec is unsupported.

## Casting from mobile
- Treat casting as an optional capability.
- Select a documented protocol supported by both the TV and sending device.
- Do not claim that all Android apps or media can be cast.
- Provide clear discovery, pairing, and connection status when supported.
- Require explicit user action before sending media.

## App shortcuts
- Show shortcuts only for applications that can be discovered or configured through supported mechanisms.
- Do not assume an app can be launched by arbitrary package name on every Tizen version.
- Removing a Medoz shortcut must not delete the underlying application.
- If launch is unsupported, explain this rather than silently failing.

## Legal and security requirements
- No bypassing DRM, app signing, platform security, or access controls.
- No unauthorized installation or distribution of third-party applications.
- Protect user-supplied URLs and credentials.

## Acceptance criteria
Test every advertised stream type, casting path, and shortcut behavior on the actual target TV and phone. Unsupported functions must be clearly identified before release.
