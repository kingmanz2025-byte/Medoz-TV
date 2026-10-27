# Medoz TV — Audio & Playback Specification

## Sources
- Local audio files, when the platform exposes supported access.
- Quran recitations.
- Azkar and Ruqyah playlists.
- Internet radio using compatible direct streams.

Do not assume every USB folder, audio format, background playback mode, or stream protocol is supported. Verify against the target TV.

## Controls
Support applicable play, pause, resume, stop, previous/next, and favorites. Use the TV remote and expose only controls supported by the runtime. Back navigation must be predictable.

## Statuses
Provide clear Arabic states for loading, connecting, buffering, playing, paused, failed, unsupported format, and offline. Never leave an indefinite loading state after an error.

## Stream recovery
- Provide retry after a failure.
- Use reasonable timeouts and avoid endless retry loops.
- Preserve the selected station after failure.
- Resume network functionality after reconnection without unexpectedly starting audio.

## Audio conflicts
Avoid simultaneous independent sources unless explicitly supported. Clearly identify the active source. Do not promise background playback while suspended until tested.

## Favorites and playlists
Save favorites locally where possible and preserve them across restarts. An unavailable station should not automatically erase its favorite entry.

## Rights and sources
Use user-provided files, properly licensed content, or sources that permit the intended use. Do not bundle or redistribute copyrighted recordings or unauthorized streams. Keep stream sources configurable.

## Offline behavior
Local audio remains available where supported. Internet radio should show an offline message and should not retry continuously in the background.

## Acceptance criteria
- Local audio and compatible streams tested on target TV.
- Remote controls work consistently.
- Failures do not freeze the UI.
- Favorites persist where supported.
- No unexpected autoplay on startup.
