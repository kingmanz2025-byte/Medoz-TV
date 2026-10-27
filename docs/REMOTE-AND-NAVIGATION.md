# Medoz TV — Remote & Navigation

## Navigation model
- Sidebar sections, in RTL order, should remain consistent across screens.
- Suggested sections: الرئيسية، القرآن، الأذكار، الرقية، الراديو، الملفات الصوتية، المفضلة، الإعدادات.
- Keep the sidebar fixed while changing the main content.
- A selected section is not activated merely because focus passes over it. Press OK to activate.

## Remote controls
- Up/Down/Left/Right: move focus using predictable spatial navigation.
- OK/Enter: activate the focused control.
- Back: return to the previous screen or close the current overlay.
- Play/Pause/Stop and volume keys: use only when exposed by the device and application runtime.
- Do not claim the app can control system volume or other apps unless tested.

## Focus appearance
- Use a high-contrast gold border, glow, or equivalent clear focus treatment.
- Keep focus visible on cards, buttons, list items, and settings.
- Avoid focus traps, hidden focused elements, and unexpected focus jumps.
- After closing a dialog, return focus to the control that opened it when possible.

## Back behavior
- Close the topmost dialog first.
- Otherwise return to the prior screen.
- Ask for confirmation before leaving a critical unsaved workflow.
- Do not stop audio unexpectedly unless leaving the audio screen requires it or the user selects Stop.

## Error states
Use concise Arabic messages, a clear next action, and never expose stack traces.
