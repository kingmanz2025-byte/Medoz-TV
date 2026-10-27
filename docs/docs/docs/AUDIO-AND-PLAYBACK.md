# Medoz TV — Audio & Playback Specification

## 1. Purpose

Define the audio experience across Quran recitations, Azkar, Ruqyah, radio stations, and locally stored audio files.

The experience must be reliable, remote-friendly, Arabic-first, and consistent with the premium Medoz TV visual identity.

## 2. Supported Audio Sources

### A. Local Audio

- Allow playback of supported local audio files when the TV platform permits access.
- Support browsing available files through a clear interface.
- Organize files into playlists where supported.
- Display the file name and playback status.
- Provide clear feedback when a file is missing, inaccessible, or unsupported.
- Do not assume the application can browse every USB device or protected storage location.

### B. Quran

- Provide a dedicated Quran section.
- Organize available content by reciter and available surah or playlist information.
- Allow the user to select a reciter and start playback.
- Support play, pause, resume, and stop.
- Preserve the last selected reciter and playback preferences where practical.
- Clearly distinguish downloaded or local content from internet streams.

### C. Azkar and Ruqyah

- Provide separate sections for Azkar and Ruqyah.
- Support playlists or categorized audio where available.
- Display the current item and playback status.
- Allow the user to stop playback immediately.
- Do not automatically start religious audio after application launch unless the user explicitly enables that behavior.

### D. Internet Radio

- Provide a radio directory organized by category.
- Display each station's name and available logo.
- Allow the user to save favorite stations.
- Support compatible direct audio streams, subject to the TV platform's media capabilities.
- Show loading, buffering, playing, and failed states.
- Explain when an internet connection is required.

## 3. Playback Controls

The following controls must be available wherever applicable:

- تشغيل.
- إيقاف مؤقت.
- استكمال التشغيل.
- إيقاف.
- رفع وخفض الصوت using the TV remote when supported.
- Previous and next track for playlists.
- Add or remove favorites.
- Return to the previous screen without accidentally restarting playback.

Use the TV remote's directional buttons and OK button for navigation and selection.

The Back button must have predictable behavior and must not unexpectedly exit the app or interrupt playback without appropriate handling.

## 4. Playback Status

Display a clear status for:

- جاري التحميل.
- جاري الاتصال بالمحطة.
- جاري التخزين المؤقت.
- يعمل الآن.
- متوقف مؤقتًا.
- تعذر التشغيل.
- لا يوجد اتصال بالإنترنت.
- صيغة الملف غير مدعومة.

Do not leave the interface stuck in a loading state after a playback failure.

## 5. Internet Stream Recovery

For internet radio and other supported streams:

- Detect playback errors when the platform exposes them.
- Provide a retry action.
- Avoid retry loops that consume excessive bandwidth or CPU.
- Use a reasonable connection timeout.
- Stop retrying after repeated failures and let the user retry manually.
- Preserve the selected station when a connection fails.
- Do not claim that a station is available until playback or a successful connection has been verified.

Automatic reconnection may be offered as a configurable feature, subject to platform limitations.

## 6. Audio Focus and Conflicts

- Avoid playing two independent audio sources simultaneously unless the user explicitly requests a supported mixing feature.
- Starting a new audio source should handle the existing source predictably.
- Make it clear which source is currently active.
- Stop or pause audio when required by application navigation or platform lifecycle rules.
- Do not promise background playback while the TV app is suspended unless that capability has been verified on the target device.

## 7. Playlists and Favorites

- Allow users to save favorite radio stations and supported audio items.
- Store favorites locally when possible.
- Preserve favorites across app restarts.
- Handle unavailable stations without deleting the user's saved favorite.
- Keep the interface simple enough to navigate with directional buttons.

## 8. Audio Data and Copyright

- Use audio files supplied by the user, legitimately licensed material, or sources that expressly permit the intended use.
- Do not bundle copyrighted recordings or redistribute streams without the necessary rights.
- Keep internet stream URLs configurable rather than embedding unverified or unauthorized sources.
- Clearly distinguish local files from online content.
- Do not require a paid subscription for Medoz TV's own features.

## 9. Offline Behavior

When the TV has no internet connection:

- Continue to offer supported local audio.
- Keep saved favorites visible.
- Explain that internet radio requires a connection.
- Do not repeatedly attempt to load online streams in the background.
- Resume online functionality when connectivity returns, without unexpectedly starting audio.

## 10. Visual and Accessibility Requirements

- Follow the approved navy-and-gold design.
- Use large, readable Arabic labels.
- Provide a clear gold focus indicator for remote navigation.
- Display the current track or station prominently.
- Keep primary playback controls visible and easy to reach.
- Avoid unnecessary animation while audio is playing.
- Provide accessible focus states and readable error messages.

## 11. Acceptance Criteria

The feature is ready for testing when:

- Supported local audio can be selected and played.
- Quran, Azkar, and Ruqyah sections are clearly separated.
- Compatible radio streams can be played and stopped.
- Playback errors are handled without freezing the interface.
- Remote controls work consistently.
- Favorites persist when supported.
- Offline mode does not repeatedly retry unavailable streams.
- The application does not unexpectedly play audio on startup.
- Playback behavior has been tested on the target Samsung TV and Tizen version.

## 12. Platform Compatibility

Supported formats, local file access, stream protocols, audio focus, background playback, and remote volume controls must be verified against the target device.

Do not treat a feature as supported merely because it works in a desktop browser or Android application.
