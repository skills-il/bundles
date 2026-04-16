# Israeli Dev Toolkit Bundle

Building software for the Israeli market comes with unique challenges: RTL layout, Hebrew text handling, ID validation, phone number formatting, and localization quirks that most international frameworks don't handle out of the box. This bundle gives you five AI skills that solve the most common Israeli development tasks.

## Key facts

- **Teudat zehut (Israeli ID)**: **9 digits** with a check digit validated by a Luhn-like algorithm — essential server-side validation before accepting as a primary key or for KYC.
- **Israeli phone format**: mobile numbers start with `05X` (050, 052, 053, 054, 055, 058), landlines use area codes `02, 03, 04, 08, 09`. International format is `+972` dropping the leading zero.
- **ITU-T E.164**: recommended canonical format for stored phone numbers (`+972501234567`).
- **Currency**: ILS / NIS (shekel, `₪`, ISO 4217 code `ILS`), 2 decimal places (agorot).
- **Locale code**: `he-IL` for Hebrew (Israel); fallback `he` is also widely accepted.
- **Timezone**: `Asia/Jerusalem` — observes daylight saving time (IDT = UTC+3 in summer, IST = UTC+2 in winter).
- **Currency symbol position**: shekel sign `₪` typically follows the number in Hebrew text (e.g. `100 ₪`) but precedes in English formatting.

## Who is this for?

- **Developers** building apps or websites for Israeli users
- **Teams** adding Hebrew/RTL support to existing products
- **Startups** launching in the Israeli market
- **Freelance developers** working with Israeli clients

## What you get

1. **Hebrew i18n** -- complete internationalization setup for Hebrew, covering translations, date/number formatting, and locale configuration
2. **Hebrew RTL Best Practices** -- CSS logical properties, bidirectional text, and RTL-first development patterns
3. **Israeli ID Validator** -- validate Teudat Zehut numbers with the correct check digit algorithm
4. **Israeli Phone Formatter** -- normalize and format all Israeli phone number types (mobile, landline, toll-free, international)
5. **Hebrew Tailwind Preset** -- pre-configured Tailwind CSS setup with Hebrew fonts, RTL utilities, and Israeli design patterns
