# Medoz TV — Compatibility & Test Plan

## Target device
First target reported by the user: Samsung UA7000, 58-inch. Record the exact model code, year, Tizen version, firmware, resolution, and available developer options before implementation testing.

## Installation and launch
- Verify package format, signing, installation path, and required permissions.
- Verify cold launch, relaunch, exit, and recovery after a crash.
- Record any developer-mode or account requirements.

## Remote and layout
- Test arrows, OK, Back, focus order, and all screens.
- Check Arabic RTL, font rendering, text clipping, safe areas, and overscan.
- Test focus visibility at normal viewing distance.

## Network and offline
- Test Wi-Fi connected, disconnected, slow, and restored.
- Verify dashboard remains responsive during timeouts.
- Check cached data labels and refresh behavior.

## Prayer and weather
- Verify city selection, time zone, calculation method, date transitions, and next-prayer countdown.
- Confirm sunrise is informational only.
- Confirm 12-hour Arabic time format.
- Confirm stale weather is labeled and missing data is not fabricated.

## Media
- Test each supported local audio format and radio stream type.
- Test play, pause, stop, recovery, favorites, and behavior after leaving a screen.
- Test memory use and long playback sessions.

## Companion app and casting
- Verify discovery, pairing, remote commands, and permissions.
- Test each advertised casting protocol on both endpoints.
- Verify unsupported functions are clearly communicated.

## Performance and stability
- Measure startup time, navigation responsiveness, memory usage, and long-session stability.
- Test missing images, invalid URLs, corrupted settings, and failed requests.

## Release gate
No feature should be advertised as supported until it passes on the target TV and documented firmware/Tizen version. Keep a test-results table with date, device, software version, steps, result, and notes.
