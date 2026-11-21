# Color, contrast, Dark Mode

Use when: defining palettes, tints, backgrounds, or reviewing appearance modes. Sources: [Color](https://developer.apple.com/design/human-interface-guidelines/color), [Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode), [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility).

| Rule | Check |
|---|---|
| Use system-defined (semantic) colours; do not hard-code their values or redefine their meaning. | Code uses named colours, not hex copies of system colours. |
| One colour, one meaning; never rely on colour alone to differentiate, indicate interactivity or convey essential information. | Greyscale screenshot still readable. |
| Contrast minimum for text: 4.5:1 up to 17 pt; 3:1 at 18 pt, and for bold text of any size. For custom colours aim for 7:1, especially small text. | Measure from real values in every appearance. |
| If default contrast is below the minimum, provide a higher-contrast scheme when Increase Contrast is on. | Toggle Increase Contrast and re-test. |
| Support Light, Dark and Auto appearance; Auto can switch while the app runs. No app-specific appearance switch unless the product is permanently dark by design (e.g. immersive media). | Live-switch the appearance with the app open. |
| Dark palette is not a plain inversion: dimmer backgrounds, brighter foregrounds. | Review each screen in dark, not an auto-inverted copy. |
| Prefer system background colours: base vs elevated backgrounds separate layered surfaces (sheets, popovers). | No custom flat background under a sheet. |
| Use system label colours (primary to quaternary) for text. | Text colours come from the label set. |
| Soften white image backgrounds in dark mode; supply separate dark assets when a single asset fails. | Check images and icons on both backgrounds. |
| Test Dark Mode combined with Increase Contrast and Reduce Transparency, separately and together. | Four-combination pass. |
| Limit the palette; keep colour in large areas or bold text; if the user picks a system accent other than multicolour, it replaces yours. | Accent adapts. |
| Liquid Glass material: no solid or tinted backing under controls; use colour sparingly on glass; avoid label colours that resemble the colourful content beneath. | Controls legible over busiest content. |

Related: [accessibility.md](accessibility.md); WCAG contrast in [../accessibility.md](../accessibility.md).
