# Notifications and badges

Use when: deciding what to push, how it reads, and how urgent it is. Sources: [Notifications](https://developer.apple.com/design/human-interface-guidelines/notifications), [Managing notifications](https://developer.apple.com/design/human-interface-guidelines/managing-notifications).

| Rule | Check |
|---|---|
| Get consent before sending any notification; ask in context ([permissions-privacy.md](permissions-privacy.md)). | Permission requested after the user shows interest. |
| Make each notification concise and informative; no duplicates for the same event, even without a response. | Dedupe logic exists. |
| Do not tell people to perform tasks in the app; do not repeat the app name or icon (the system shows them). | Read sample payloads. |
| Do not put sensitive or confidential data in the notification; provide generic text for when previews are hidden. | Preview-off appearance is meaningful. |
| Use an alert, not a notification, to show an error. | No error-only pushes. |
| Handle notifications gracefully while the app is in the foreground. | No duplicate banner on the current screen. |
| Up to four action buttons; make them beneficial and prefer nondestructive; do not offer an action that just opens the app. | Each action completes something. |
| Interruption levels: Passive, Active (default), Time Sensitive, Critical (needs entitlement). Use Time Sensitive only for things relevant right now; never for marketing. | Level matches real urgency. |
| Marketing or promotional notifications need explicit agreement. | Separate opt-in exists. |
| Offer in-app notification settings by type. | Settings screen lists categories. |
| Badge = count of unread notifications only; keep it current; never the only carrier of essential information. | Badge clears when read. |

Android counterpart: channels and the Android 13 runtime permission in [../mobile-android.md](../mobile-android.md).

## Audit procedure
1. List every notification type with trigger, copy, interruption level, actions and opt-in path.
2. Test with previews hidden and while the app is in the foreground.
3. Check frequency: could one event produce more than one notification? Could a burst be grouped?
4. Check that promotional content has a separate, explicit opt-in and never uses Time Sensitive.
