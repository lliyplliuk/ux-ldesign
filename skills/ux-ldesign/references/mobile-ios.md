# iOS / iPadOS overview

Use when: reviewing or designing a native iPhone/iPad screen, or a cross-platform app shipping to iOS. Detail (icons, haptics, more): [apple-hig/index.md](apple-hig/index.md). Android: [mobile-android.md](mobile-android.md). Checked against HIG 2026-11-21.

| Area | Must-know rule | Source |
|---|---|---|
| Targets | Control default 44x44 pt, minimum 28x28 pt; about 12 pt padding around bezeled elements, 24 pt around unbezeled. | [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility) |
| Layout | Respect safe areas; decide by size class, not device; keep critical controls off the bottom edge. | [Layout](https://developer.apple.com/design/human-interface-guidelines/layout) |
| Navigation | Tab bar navigates, never acts; do not hide or disable tabs; symbol plus label; Keep Back visible; edge swipe is a shortcut. | [Tab bars](https://developer.apple.com/design/human-interface-guidelines/tab-bars), [Gestures](https://developer.apple.com/design/human-interface-guidelines/gestures) |
| Modality | Sheets for short focused tasks, one at a time, swipe to dismiss, Cancel/Done; alerts rare, verbs on buttons, Cancel beside destructive. | [Sheets](https://developer.apple.com/design/human-interface-guidelines/sheets), [Alerts](https://developer.apple.com/design/human-interface-guidelines/alerts) |
| Type | Default 17 pt, minimum 11 pt; use text styles; layout survives largest Dynamic Type. | [Typography](https://developer.apple.com/design/human-interface-guidelines/typography) |
| Colour | Semantic system colours; contrast 4.5:1 up to 17 pt, 3:1 at 18 pt or bold; support Dark Mode and Increase Contrast; never colour alone. | [Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode), [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility) |
| Permissions | Ask in context, honest purpose string, a pre-screen has one button into the system alert, never lead or reward. | [Privacy](https://developer.apple.com/design/human-interface-guidelines/privacy) |
| Notifications | Consent first, concise, no sensitive data, interruption level matches urgency, no marketing at Time Sensitive. | [Managing notifications](https://developer.apple.com/design/human-interface-guidelines/managing-notifications) |
| Launch and onboarding | Launch instantly, launch screen mirrors first screen, restore state; onboarding fast and optional. | [Launching](https://developer.apple.com/design/human-interface-guidelines/launching), [Onboarding](https://developer.apple.com/design/human-interface-guidelines/onboarding) |
| Input | Right keyboard type, secure fields for secrets, never prefill a password, minimise typing. | [Entering data](https://developer.apple.com/design/human-interface-guidelines/entering-data) |
| Loading and errors | Show something at once, say what is loading, explain why a command cannot run, offer undo. | [Loading](https://developer.apple.com/design/human-interface-guidelines/loading), [Feedback](https://developer.apple.com/design/human-interface-guidelines/feedback) |

## Cross-platform rules (shared with Android)
- Follow each platform's navigation and back conventions, or record a deliberate shared design; tab bars, sheets and back are where users notice.
- Touch targets: 44 pt on iOS ([HIG](https://developer.apple.com/design/human-interface-guidelines/accessibility)) and 48 dp on Android ([Android quality](https://developer.android.com/docs/quality-guidelines/core-app-quality)).
- Respect insets, text-size, dark theme and reduced motion; ask permissions in context; test with OS settings on a device or simulator, not a browser.
- Framework vocabulary: safe area = insets API; size classes = width breakpoints; Dynamic Type = OS font scale; sheet = bottom sheet/modal.

Deeper lookup: [HIGAgentSkills](https://github.com/justinwetch/HIGAgentSkills) (MIT, 157 condensed HIG pages with routing index).
