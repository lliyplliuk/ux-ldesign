# Icons and SF Symbols

Use when: choosing glyphs for tab bars, toolbars, buttons and labels. Sources: [SF Symbols](https://developer.apple.com/design/human-interface-guidelines/sf-symbols), [Buttons](https://developer.apple.com/design/human-interface-guidelines/buttons), [Tab bars](https://developer.apple.com/design/human-interface-guidelines/tab-bars).

| Rule | Check |
|---|---|
| Use SF Symbols wherever a symbol exists: they match San Francisco text weight and scale, and adapt to Dark Mode and accessibility settings. | No mixed web icon sets beside symbols. |
| Four rendering modes: monochrome, hierarchical, palette, multicolour. Confirm the chosen mode works in every context. | Check light, dark, tinted. |
| Match symbol weight (nine weights) to adjacent text; use scale (small, medium default, large) to change emphasis without breaking weight matching. | Icon next to label looks the same weight. |
| Variants carry state: outline for toolbars and lists, fill for iOS tab bars and swipe actions and selected states; slash for off. | Selected tab uses fill. |
| Use variable colour to show a changing value (volume, strength), not for depth. | Value maps to layers. |
| Associate familiar actions with familiar icons; add text when a short label is clearer than the icon. | Icon-only controls pass a first-click test; each has an accessibility label. |
| Make custom icons visually consistent with the system set, in vector format, and test in both appearances; add dark variants if edges vanish. | Check edges on dark and light backgrounds. |
| Availability varies by OS version; check the target version. | Fallback exists for older systems. |

Buttons: always include a press state for a custom button; the preferred action uses a prominent style (not size); one primary-role button per view; never give the primary role to a destructive action. Source: [Buttons](https://developer.apple.com/design/human-interface-guidelines/buttons).

## Audit procedure
1. Screenshot the main screens at the largest text size; icons and labels should still align and scale.
2. Flag non-system glyphs next to system symbols (weight, optical size, stroke style differences).
3. Verify tab bar selected states use the fill variant and unselected states use outline.
4. Confirm every icon-only button has a text label for assistive technologies and a plausible meaning without it.
