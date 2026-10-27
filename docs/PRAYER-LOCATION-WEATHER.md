# Medoz TV — Prayer, Location & Weather Specification

## 1. Clock and date
- Display time in 12-hour format using Arabic ص/م.
- Display the date in Arabic.
- Use the device time zone when available and valid; never hardcode Cairo time.
- If time-zone information is unavailable, provide a clear settings fallback.

## 2. Prayer-time order
Display exactly in this order:
1. الفجر
2. الشروق
3. الظهر
4. العصر
5. المغرب
6. العشاء

Sunrise is informational and must not be presented as one of the five obligatory prayers.

## 3. Next prayer
- Highlight the next upcoming prayer using the gold accent.
- Show a countdown only when the schedule and device time are valid.
- After Isha, use the next day's schedule.
- Never invent times or silently substitute another city or calculation method.

## 4. Location
- Use automatic location only if the TV platform supports a suitable source and permission is granted where required.
- Do not assume the TV has GPS.
- Always provide manual city selection as a fallback.
- Save the selected city locally when possible and display it in settings.

## 5. Calculation settings
- Use a documented prayer-time calculation method.
- Expose calculation method and Asr convention settings where supported and practical.
- Apply location, date, and time-zone rules correctly.
- Validate data before showing it.

## 6. Weather card
When valid data is available, show temperature, concise condition, icon, selected city, and update time where useful.
- Use a configured source; do not assume an API key is available.
- Respect provider limits and avoid excessive requests.
- Cache the last successful result where permitted.
- Mark stale data clearly; never present it as verified current weather.
- If data is unavailable, show a neutral unavailable/offline state, not an invented temperature.

## 7. Offline behavior
Keep the dashboard, saved city, preferences, favorites, local audio, and valid cached prayer data available where the platform permits. Validate cached prayer data's date and label stale data. Internet weather updates and internet radio require connectivity.

## 8. Arabic status messages
- لم يتم تحديد المدينة.
- تعذر حساب مواقيت الصلاة.
- لا تتوفر بيانات الطقس حاليًا.
- لا يوجد اتصال بالإنترنت.
- بيانات الطقس المعروضة قديمة.
- تعذر تحديد المنطقة الزمنية.

## 9. Acceptance criteria
- Correct prayer order and 12-hour Arabic formatting.
- Sunrise clearly distinguished from prayers.
- Correct next-prayer logic and countdown.
- Manual city selection works without location permission.
- Missing data never creates fabricated times or temperatures.
- Offline behavior is clear and does not freeze the UI.
- Test all capabilities on the target Samsung TV and Tizen version.
