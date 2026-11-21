# Accessibility

Use when: checking or designing for accessibility, or when a legal accessibility scope matters (EU, US public sector).

## Legal and standards baseline (checked 2026-11)

| Item | Fact | Source |
| --- | --- | --- |
| Design target | Use WCAG 2.2 AA as the practical target unless the project sets another; clarify scope. WCAG 2.2 is a superset of 2.1 (4.1.1 Parsing removed as obsolete). | [WCAG 2.2](https://www.w3.org/TR/WCAG22/) · [New in 2.2](https://www.w3.org/WAI/standards-guidelines/wcag/new-in-22/) |
| EU: European Accessibility Act | Directive (EU) 2019/882; measures apply from 2025-06-28. Covers e-commerce services, consumer banking, e-books, electronic communications, audiovisual media access, passenger transport (air, bus, rail, waterborne), 112 and certain products (consumer computers, e-readers, payment/ATM/ticketing terminals). Service microenterprises (under 10 staff, turnover or balance sheet up to EUR 2 m) are exempt. Transitional periods run to 2030 for existing service contracts and products. Check that an accessibility statement and a feedback channel exist (unverified: article not fetched). | [EUR-Lex](https://eur-lex.europa.eu/eli/dir/2019/882/oj) |
| EU technical standard | EN 301 549 V3.2.1 (2021-03) is the harmonised standard; its web clause reflects WCAG 2.1, not 2.2. W3C notes a 2026 version of EN 301 549 uses WCAG 2.2. Treat 2.1 AA as the legal floor and 2.2 AA as the design target; confirm the current citation for the case. | [ETSI EN 301 549 V3.2.1](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/03.02.01_60/en_301549v030201p.pdf) · [W3C WCAG overview](https://www.w3.org/WAI/standards-guidelines/wcag/) |
| US: ADA Title II web rule | Public entities must meet WCAG 2.1 AA. Dates after the April 2026 interim final rule: 2027-04-26 (population 50,000 or more), 2028-04-26 (smaller entities and special districts). | [ADA.gov](https://www.ada.gov/resources/web-rule-first-steps/) |
| WCAG 3.0 | Working Draft (2026-09-10); "inappropriate to cite ... as other than a work in progress". Never present it as a requirement. | [WCAG 3.0](https://www.w3.org/TR/wcag-3.0/) |
| ISO | WCAG 2.2 (Oct 2023 text) is ISO/IEC 40500:2025. | [W3C WAI](https://www.w3.org/WAI/standards-guidelines/wcag/) |

This is not legal advice; for a formal claim ask the owner for the applicable jurisdiction and standard version.

## Checks

For native interfaces check platform rules, system settings and real screen-reader operation. Numbers below are WCAG 2.2 criteria.

| What | How to check |
| --- | --- |
| Contrast and colour | Measure text contrast in all applicable states. 1.4.3: 4.5:1 normal text, 3:1 large text, with stated exceptions. 1.4.11: 3:1 for needed graphics and control boundaries or states. 1.4.1: no signal carried by colour alone. |
| Keyboard and focus | Walk the flow with Tab, Shift+Tab and pattern keys. Check action reachability, exit from components, order and focus visibility (2.1.1, 2.1.2, 2.4.3, 2.4.7). For a modal check entry, close and sensible focus return. Sticky UI must not fully hide the focused component (2.4.11). 2.4.1: a way to bypass repeated blocks (skip link or landmarks). |
| Semantics and feedback | Check accessible name, role, value and state, heading structure, alternatives for meaningful images, announcements of dynamic changes. Walk the key path with a screen reader manually (1.1.1, 1.3.1, 4.1.2, 4.1.3). 3.1.1: page language set. |
| Pointer and touch | 2.5.8 (AA): pointer target at least 24 x 24 CSS px, with exceptions incl. spacing between small targets. 2.5.7: single-pointer alternative to dragging. 2.5.1: multipoint or path gestures need a single-pointer alternative. 2.5.2: actions fire on up-event or can be aborted or undone. 2.5.3: the accessible name contains the visible label text. 2.5.5 (AAA, 44 x 44 CSS px) is a useful design target for touch. |
| Zoom, reflow, spacing | 1.4.4: text to 200%. 1.4.10: reflow at 320 CSS px width for vertically scrolling content, with exceptions for two-dimensional content. 1.4.12 (AA): no loss of content when line height is 1.5x, paragraph spacing 2x, letter spacing 0.12x, word spacing 0.16x the font size. 1.4.13 (AA): hover or focus content is dismissible, hoverable and persistent. |
| Forms and sign-in | Labels, required marks, instructions, specific error text with a suggestion when known (3.3.1-3.3.4). 1.3.5 (AA): inputs about the user carry autocomplete purpose tokens. 3.3.7: no redundant re-entry. 3.3.8: authentication without a cognitive-function test (paste and password managers allowed). |
| Consistency | 3.2.6 (A) Consistent Help: help mechanisms (contact, chat, FAQ link) sit in the same relative place across pages. |
| Motion | Pause, stop or hide auto-moving content (2.2.2); flash limits (2.3.1). For interaction animation honour the reduced-motion setting. |

Supplement automated scans with manual walks of real tasks. Record routes, states, browsers and assistive technologies tested. A formal conformance claim needs evaluation of applicable criteria across whole processes. [W3C WAI on evaluating accessibility](https://www.w3.org/WAI/test-evaluate/)
