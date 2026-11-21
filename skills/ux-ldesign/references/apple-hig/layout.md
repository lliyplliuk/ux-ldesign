# Layout, safe areas, size classes

Use when: laying out a screen, reviewing spacing/orientation behaviour, or adapting iPhone UI to iPad or resized windows. Source: [Layout](https://developer.apple.com/design/human-interface-guidelines/layout).

| Rule | Check |
|---|---|
| Stay inside the safe area: system bars, Dynamic Island and home indicator must not cover content or controls. | Run on a device with a Dynamic Island and a home-indicator device; nothing tappable under system UI. |
| Do not put critical controls or information at the very bottom edge of a window. | Primary actions are reachable without sitting on the window edge (matters for resizable iPad windows). |
| Decide layout by size class (compact/regular, per axis), not by device model or orientation. | Resize the window / rotate / Split View: all four combinations render, same functions available. |
| Keep functionality the same when size classes change; keep the layout recognisably iPhone- or iPad-like. | Feature list identical at compact and regular width. |
| Order content by importance, align to aid scanning, group related items, use progressive disclosure. | First screen shows the primary task; secondary options sit behind a disclosure. |
| Differentiate controls from content; let full-screen backgrounds extend under bars and sidebars. | Background art runs edge to edge; controls still legible over it. |
| Plan for text-size change: stack horizontally adjacent views vertically, let rows grow, avoid cropped or overlapping text. | See [typography-dynamic-type.md](typography-dynamic-type.md). |
| Test on several devices, size classes, localisations (incl. right-to-left, longer text) and text sizes. | Test matrix recorded in the review. |
| Even landscape-only or orientation-locked apps must resize cleanly across devices and windows. | Run on iPad and a small iPhone. |

Spacing: Apple gives about 12 pt around bezeled controls and about 24 pt around unbezeled ones ([Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility)). The tvOS/visionOS margin numbers on the Layout page do not apply to iPhone.

Cross-platform notes (React Native, Flutter): map "safe area" to the framework's insets API; map size classes to width breakpoints (see [../mobile-ios.md](../mobile-ios.md)).
