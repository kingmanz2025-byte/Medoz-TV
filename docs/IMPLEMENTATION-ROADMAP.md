# Medoz TV — Implementation Roadmap

## Phase 0 — Requirements and approval
- Review all specification documents.
- Confirm target TV model code and Tizen version.
- Decide first-release scope and installation/distribution method.
- Approve the final visual reference.

## Phase 1 — Platform proof of concept
- Create a minimal Tizen app that launches on the target device.
- Verify Arabic RTL, fonts, remote navigation, storage, and media APIs.
- Record platform limitations before building the full interface.

## Phase 2 — Design system and dashboard
- Implement palette, typography, spacing, cards, sidebar, focus states, and responsive viewport behavior.
- Add the dashboard with local placeholder data.
- Compare implementation with the approved design reference.

## Phase 3 — Offline core
- Add settings, themes, favorites, navigation, and supported local content.
- Handle missing files and corrupted preferences.

## Phase 4 — Prayer, clock, and weather
- Implement city selection and documented prayer-time calculation.
- Add 12-hour Arabic clock, next-prayer logic, and validated cache.
- Add weather integration only after choosing a suitable data provider.

## Phase 5 — Audio and streams
- Add supported local audio, Quran/Azkar/Ruqyah categories, and compatible radio streams.
- Verify format and background limitations on device.

## Phase 6 — Optional integrations
- Evaluate IPTV, casting, app shortcuts, and mobile remote one by one.
- Include only capabilities that can be implemented lawfully and tested.

## Phase 7 — QA and release
- Execute the compatibility test plan.
- Fix critical navigation, stability, and data correctness issues.
- Document installation and recovery instructions.
- Publish a release only through a supported distribution route.

## Rule
Do not treat roadmap items as completed until implementation and test evidence exist.
