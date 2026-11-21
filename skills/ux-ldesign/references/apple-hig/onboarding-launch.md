# Onboarding, launch, in-app help

Use when: designing first run, launch screens, state restoration, tips. Sources: [Onboarding](https://developer.apple.com/design/human-interface-guidelines/onboarding), [Launching](https://developer.apple.com/design/human-interface-guidelines/launching), [Offering help](https://developer.apple.com/design/human-interface-guidelines/offering-help).

## Launch
| Rule | Check |
|---|---|
| Launch instantly; people may not wait more than a couple of seconds. | Cold-start the app on a mid-range device. |
| iOS displays a launch screen the moment the app starts. Make it nearly identical to the first screen, matching orientation and appearance; no text, no logo, no advertising. | No flash between launch screen and first screen. |
| It is not a splash or an About screen; if a splash is needed, show it at the start of onboarding. | Launch screen has no branding moment. |
| Restore the previous state, including scroll position, so people continue where they left off. | Kill and relaunch mid-task; the place is restored. |
| Launch in the device's current orientation when both are supported. | Rotate then relaunch. |

## Onboarding
| Rule | Check |
|---|---|
| Ideally the app is understood by using it; if onboarding is needed, make it fast, fun and optional. | A skip path exists; time to first useful action is short. |
| Teach through interactivity; prefer context-specific tips over one long flow. | No static slide deck of features. |
| Postpone non-essential setup and customisation; avoid licensing details inside onboarding. | Setup asks only what the first task needs. |
| Do not let large downloads block onboarding. | Content downloads in the background. |
| If private data is needed before the app works, fold the permission request into onboarding. | See [permissions-privacy.md](permissions-privacy.md). |
| Let people experience the app before asking for ratings or purchases. | Rating prompt after a success moment. |

## Tips and help
- Tips are small transient views; use them for simple features; keep them short, actionable and engaging; target them with rules so they reach the intended audience; do not repeat the icon already shown in the UI.
- Help must be inclusive and fit the tasks people do; open the topic related to the current context.

More patterns: [../patterns.md](../patterns.md).
