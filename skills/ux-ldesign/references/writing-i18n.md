# UX writing and internationalisation

Use when: writing or reviewing interface text (buttons, errors, labels, help) or preparing a product for other languages, scripts, RTL and locale formats.

## UX writing

| Rule | Check | Source |
|---|---|---|
| Button text describes the action in sentence case and matches what happens: "Continue" (nothing saved), "Save and continue", "Save and come back later", "Add another", "Pay", "Sign out"; add words when needed ("Add another address"). | Read the button alone: does it say verb + object without the page? No "OK/Submit/Yes" on consequential actions. | [GOV.UK button](https://design-system.service.gov.uk/components/button/) |
| Say "select" not "click" (not all users click); no "please", "e.g.", "i.e.", "utilise"; active voice; write "cannot" instead of negative contractions. | Search copy for these strings. | [GOV.UK A to Z style guide](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/style-guides/a-to-z-style-guide/) |
| Sentence case everywhere (titles, labels, service names); only proper nouns capitalised. | No Title Case Headings. | GOV.UK style guide |
| Links: front-load the relevant terms, active and specific; never "click here". | Link text makes sense out of context (also WCAG 2.4.4). | GOV.UK style guide; [WCAG 2.2](https://www.w3.org/TR/WCAG22/) |
| Plain language: sentences about 15-20 words; reading grade 6-8 for a general audience (10-12 for expert audiences); one idea per paragraph; web copy under half the words of print; no slang, idioms or internal brand terms. | Readability score on the text; 5-second comprehension test. | [NN/g plain language](https://www.nngroup.com/articles/plain-language-experts/) |
| Dates: "2 June", no ordinals, no comma between month and year; ranges with "to"; numerals for 2-9 in running text, commas above 999. | Consistent across screens. | GOV.UK style guide |
| Use the user's word (the term the audience would search), not internal names. | Match terms in search logs or tests. | NN/g plain language |

### Error message formula

Say what happened + how to fix it, in the field's own words; no blame, no codes.
- Empty: instruction ("Enter your name"). Too long: rule ("Name must be 35 characters or less"). Wrong format: "Enter a National Insurance number in the correct format". Rule breach: describe the rule ("The date your passport was issued must be in the past").
- Avoid "please", "sorry", "valid/invalid", "you forgot", "oops", "illegal", "incorrect"; no humour (it wears thin on repeats); do not restate hint text; identical wording beside the field and in the summary.
- Check: each message answers "what is wrong?" and "what do I do?" without the user reading anything else.
- Sources: [GOV.UK error message](https://design-system.service.gov.uk/components/error-message/), [NN/g error-message guidelines](https://www.nngroup.com/articles/error-message-guidelines/). Placement and timing: see forms-commerce.md.

## Internationalisation basics ([W3C i18n quick tips](https://www.w3.org/International/quicktips/))

- UTF-8 for content, forms, server and database; actual characters, not escapes. Declare `lang` on the document and `lang` on foreign passages (WCAG 3.1.1 A, 3.1.2 AA). Show language switcher entries in each language's own name and script.
- Check: paste Arabic, Japanese, emoji and an accented name into every text field; it round-trips unchanged.

## RTL and logical CSS

| Rule | Check | Source |
|---|---|---|
| Set direction once with `dir="rtl"` on `<html>`; never set base direction with CSS; `lang` does not imply direction. | Switch to `dir="rtl"`: layout mirrors with no extra CSS. | [W3C: html dir](https://www.w3.org/International/questions/qa-html-dir) |
| Use `dir="auto"` on inputs/inserted text of unknown direction (not foolproof, verify), wrap inserted fragments in `<bdi>`, send direction with `dirname`. | Mixed Hebrew + English username renders in order. | same |
| Use flow-relative CSS: `margin-inline-start`, `padding-block`, `inset-inline`, `text-align: start/end` instead of left/right/top/bottom. Spec is a W3C Working Draft (4 Dec 2025); parts already ship. | `grep` CSS for `margin-left`, `padding-right`, `left:`, `text-align: left`. | [CSS Logical Properties L1](https://www.w3.org/TR/css-logical-1/) |
| Mirror directional icons (arrows, back, progress) but not logos, clocks, media controls or numbers (unverified: mirroring exceptions not fetched from a primary W3C page). | Review icon set in RTL screenshot. | - |

## Text expansion and layout

- Translations grow: IBM averages cited by W3C for English to European languages are 200-300% for strings up to 10 characters, 180-200% for 11-20, 160-180% for 21-30, 140-160% for 31-50, 130% over 70. Short strings expand the most. [W3C text size in translation](https://www.w3.org/International/articles/article-text-size)
- Use flexible layouts, no fixed-width buttons/tabs, no text in images, generous field widths; avoid saving space with abbreviations; allow long compound words (German, Finnish, Dutch) to wrap or break; give CJK and Thai/Arabic/Devanagari enough line height; also check overly short translations leave awkward gaps. Same source.
- Check: pseudo-localise (pad strings 40-50%, add accents) and review every screen for clipping or overlap.

## Locale formats

| Item | Rule | Source |
|---|---|---|
| Dates | Numeric 03/04/2025 is ambiguous across locales; use month names with four-digit year, or ISO 8601 (YYYY-MM-DD) where sortability matters; format by locale, not by hand-written regional copies. | [W3C date formats](https://www.w3.org/International/questions/qa-date-format) |
| Names | One full-name field unless parts are needed; avoid "first/last name"; allow long names, single names, single-letter names, hyphens, apostrophes, spaces and original casing; no forced uppercase; "Previous name" not "maiden name"; titles optional; add a phonetic field where sorting needs it; do not auto-parse. | [W3C personal names](https://www.w3.org/International/questions/qa-personal-names) |
| Addresses | Labels "Address line 1", "Postal code" (not "Zip"); postal code optional unless every target country uses one; form adapts to the selected country; accept input with or without separators and normalise server-side. | [W3C address formats](https://www.w3.org/International/questions/qa-address-formats) |
| Plurals | CLDR defines six categories (zero, one, two, few, many, other); Russian needs one/few/many/other, Welsh uses six. Do not write "1 hour(s)" or build sentences from fragments; keep whole messages per category. | [CLDR plural rules](https://cldr.unicode.org/index/cldr-spec/plural-rules); W3C quick tips (item 7) |
| Numbers, currency | Format with the locale's separators and currency position (use platform locale APIs, e.g. `Intl.NumberFormat`); show currency code or symbol unambiguously. (unverified: no primary source fetched for separator conventions) | - |

Check: run the top three target locales (including one RTL and one CJK) through the key flow; no clipped text, correct formats, no concatenated fragments.
