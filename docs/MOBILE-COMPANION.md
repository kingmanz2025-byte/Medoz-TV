# Medoz TV — Android Companion Specification

## 1. Purpose
Provide an Android companion app for discovering and controlling a compatible Samsung Tizen TV running Medoz TV, where the TV platform and network permit it.

## 2. Main Screen
- Medoz TV branding using navy and gold.
- Connection status: connected, disconnected, or connecting.
- TV discovery action.
- Manual TV IP address entry.
- Clear error and retry messages.

## 3. Remote Control
- Directional navigation.
- OK / Enter.
- Back.
- Home shortcut where supported.
- Playback controls where supported.
- Optional keyboard input only where the TV app and connection protocol support it.

## 4. Connection
- Discover compatible devices on the local network where permitted.
- Allow manual IP entry as a fallback.
- Explain when the phone and TV need to be on the same Wi-Fi network.
- Request only the Android permissions needed for the selected connection method.
- Show connection failures clearly.
- Do not assume that every Samsung TV exposes a public remote-control API.

## 5. Installation Assistance
- Provide guidance for supported installation methods.
- Do not bypass TV security, certificates, developer-mode requirements, or platform restrictions.
- Confirm compatibility with the exact TV model and Tizen version before promising installation.

## 6. Privacy and Security
- Do not collect location or personal information unless required for a clearly explained feature.
- Request permissions only when needed.
- Keep connection details on the device where practical.
- Do not transmit credentials or sensitive data to unrelated services.

## 7. Visual Design
- Premium navy and gold identity.
- Arabic right-to-left interface.
- Large touch targets.
- Simple connection flow.
- Consistent visual style with the TV application.

## 8. Development Gate
This document specifies intended behavior only. No implementation should begin until the user approves the final design and feature scope.
