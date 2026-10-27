# Medoz TV — Prayer, Location & Weather Specification

## 1. Purpose

Define how Medoz TV handles prayer times, location selection, clock display, weather information, and offline behavior.

The interface must be reliable, Arabic-first, easy to read from a TV viewing distance, and consistent with the premium navy-and-gold design.

## 2. Clock and Date

- Display the current time using the 12-hour format.
- Use Arabic AM/PM indicators: ص and م.
- Display the date in Arabic.
- Use the device's local time zone when available and reliable.
- Do not hardcode Cairo time or any other city's time zone.
- If the device time or time zone cannot be determined, provide a clear settings option rather than silently displaying incorrect information.

## 3. Prayer Times

Display prayer times in this order:

1. الفجر
2. الشروق
3. الظهر
4. العصر
5. المغرب
6. العشاء

### Important rules

- Sunrise is informational and must not be presented as one of the five obligatory prayers.
- Display prayer times in 12-hour format using ص and م.
- Highlight the next upcoming prayer with a gold visual indicator.
- Show the remaining time until the next prayer when the required time data is available.
- After Isha, determine the next prayer according to the selected location's next-day schedule.
- Do not display fabricated prayer times or a countdown based on missing or invalid data.
- If prayer-time calculation fails, explain the issue and provide a way to review location and calculation settings.

## 4. Location Selection

Support two location modes.

### Automatic location

- Use automatic location only when the TV platform actually supports a suitable location source.
- Request permission when required.
- Never assume that every Samsung TV provides GPS or precise location.
- If automatic location is unavailable or permission is denied, switch to manual city selection.

### Manual location

- Allow the user to select a city from a searchable list.
- Store the selected city locally so it remains selected after restarting the app.
- Clearly show the currently selected city in settings.
- Allow the user to change the city at any time.

### Location fallback

The app must remain usable without automatic location access. Manual selection is the standard fallback and must not be hidden behind advanced settings.

## 5. Prayer-Time Calculation

- Use a documented prayer-time calculation method.
- Make the calculation method configurable where practical.
- Support relevant calculation conventions and Asr settings where the chosen calculation library allows them.
- Apply location-specific time-zone and date rules.
- Keep the selected calculation settings between sessions.
- Validate calculation results before displaying them.
- Do not silently substitute a different city or calculation method when an error occurs.

## 6. Weather Card

The home screen includes a small weather card that fits the established navy-and-gold layout.

When online data is available, the card may display:

- Current temperature.
- A concise weather condition.
- A suitable weather icon.
- Selected city.
- Last successful update time when useful.

### Weather behavior

- Fetch weather data only through a configured, permitted source.
- Do not assume that a weather service or API key is already available.
- Refresh data according to a reasonable interval and the source's usage limits.
- Avoid repeated network requests when the TV is offline.
- Cache the last successful response when permitted.
- Show the cached data's age when the information may be outdated.
- Never present stale cached data as verified current weather.
- If no weather data is available, show a neutral offline or unavailable state instead of invented temperatures.

## 7. Offline Operation

The following must remain usable offline whenever the device and implementation permit:

- Main dashboard layout.
- Sidebar navigation.
- Clock, if the device clock is available.
- Previously saved city and settings.
- Previously cached prayer-time data, with its date and validity checked.
- Local Quran audio and local audio files.
- Locally stored favorites and user preferences.

Online weather updates and internet radio require network access.

If the app loses connectivity:

- Keep the interface responsive.
- Do not freeze the dashboard while waiting for a network response.
- Show a clear connection or data-availability indicator where needed.
- Preserve saved settings and favorites.
- Resume online updates when connectivity returns.

## 8. Error and Data-Validity States

Provide clear Arabic messages for these cases:

- لم يتم تحديد المدينة.
- تعذر حساب مواقيت الصلاة.
- لا تتوفر بيانات الطقس حاليًا.
- لا يوجد اتصال بالإنترنت.
- بيانات الطقس المعروضة قديمة.
- تعذر تحديد المنطقة الزمنية.

Messages must be concise and must not expose technical stack traces to the user.

## 9. Visual Requirements

- Maintain the approved premium navy-and-gold palette.
- Keep prayer times legible from a normal TV viewing distance.
- Use a gold highlight for the next prayer without overwhelming the dashboard.
- Keep the weather card compact.
- Preserve RTL alignment and Arabic typography.
- Avoid overlapping the clock, date, prayer schedule, and weather card.
- Support navigation by Samsung TV remote control.

## 10. Acceptance Criteria

The feature is ready for testing when:

- Prayer times appear in the required order.
- Sunrise is clearly separated from the five prayers.
- Clock and prayer times use the 12-hour Arabic format.
- The next prayer and countdown update correctly.
- Manual city selection works without location permission.
- Invalid or missing data never produces fabricated times or temperatures.
- Cached data is distinguishable from current online data.
- The dashboard remains usable during internet outages.
- The interface remains consistent with the approved Medoz TV design.

## 11. Compatibility Note

All location, weather, background execution, storage, and network capabilities must be verified against the target Samsung TV model and its installed Tizen version before implementation is considered complete.
