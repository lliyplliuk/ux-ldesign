# Typography and Dynamic Type

Use when: choosing font sizes/weights or verifying text scaling. Source: [Typography](https://developer.apple.com/design/human-interface-guidelines/typography) (updated Dec 2025 with emphasised weights).

| Rule | Check |
|---|---|
| iOS/iPadOS default text size is 17 pt, minimum 11 pt. | No body text below 11 pt at default setting; body at 17 pt. |
| Prefer the built-in text styles (Large Title through Caption 2) and modify them only when needed; do not embed or hard-code system fonts. | Code uses text-style APIs, not fixed point sizes. |
| iOS Body and Headline are 17 pt (Headline semibold); Large Title 34 pt, Title 1 28, Title 2 22, Title 3 20, Callout 16, Subhead 15, Footnote 13, Caption 1 12, Caption 2 11 at the default "Large" setting. | Compare design tokens with the table on the Typography page. |
| SF Pro is the system font on iOS/iPadOS; minimise the number of typefaces. | At most one extra brand face, in display text. |
| Avoid light weights; use weight, size and colour to express hierarchy. | Small text is Regular or heavier. |
| Maximise contrast between text and its container; bold text with no background. | See contrast table in [accessibility.md](accessibility.md). |
| Custom fonts: legible at small sizes and implement scaling with Dynamic Type. | Custom font scales with the setting. |

## Dynamic Type checks
- Set the largest sizes (including accessibility sizes) and walk the main flow.
- Layout adapts: side-by-side views stack, rows grow, text is not cropped or overlapping; keep truncation to a minimum.
- Meaningful icons grow with text; information hierarchy stays the same at every size.
- At large sizes prioritise important content; consider a different layout for the largest sizes.
- Tracking and leading come from the system styles; if mockups are in a design tool, adjust tracking per the page's tracking table rather than guessing.

Cross-platform: map text styles to the framework's type scale and honour the system text-scale setting (e.g. `allowFontScaling` in React Native, `textScaler` in Flutter); test with the OS slider, not only in-app.
