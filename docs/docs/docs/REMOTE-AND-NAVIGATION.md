# Medoz TV — Remote Control and Navigation

## 1. Design Goal
Provide a premium, smooth, and accessible television experience controlled primarily by the physical TV remote.

## 2. Main Navigation
Use a fixed sidebar with the following sections in this order:

1. الصفحة الرئيسية
2. القرآن الكريم
3. الأذكار والرقية
4. الراديو
5. IPTV
6. التطبيقات
7. البث من الموبايل
8. الطقس
9. الإعدادات

## 3. Remote Buttons
- Up / Down: Move between navigation items and cards.
- Left / Right: Move horizontally between cards and supported controls.
- OK / Enter: Open the selected item or confirm an action.
- Back: Return to the previous screen.
- Media buttons: Control playback where supported by the remote and TV platform.

## 4. Focus and Selection
- Use a clear gold outline and subtle glow for the focused item.
- Keep the selected item visible while navigating.
- Never rely on color alone to communicate selection.
- Avoid tiny text and crowded controls.
- Prevent focus from becoming lost between the sidebar and content area.

## 5. Audio Playback
- Display the current track or station.
- Provide play, pause, stop, and supported seek controls.
- Show loading, playback, and error states.
- Handle unavailable online streams gracefully.
- Preserve favorites and last-played information where possible.

## 6. Error and Offline States
- Show a clear message when a network feature requires internet.
- Keep local settings and favorites available offline.
- Do not present stale weather or prayer information as freshly updated.
- Provide a retry option when a network operation fails.

## 7. Accessibility and Performance
- Use readable Arabic typography.
- Maintain consistent spacing and high contrast.
- Keep animations smooth and restrained.
- Respect reduced-motion preferences where supported.
- Test all navigation using the actual Samsung TV remote.

## 8. Development Gate
This document defines intended behavior only. Do not begin implementation until the user approves the final visual design and feature scope.
