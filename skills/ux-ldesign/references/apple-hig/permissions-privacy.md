# Permissions, privacy, accounts

Use when: any system permission prompt, data collection, sign-in or account deletion. Sources: [Privacy](https://developer.apple.com/design/human-interface-guidelines/privacy), [Managing accounts](https://developer.apple.com/design/human-interface-guidelines/managing-accounts). The page "Requesting permission" no longer exists as its own URL; its guidance is inside Privacy.

## Asking for access
| Rule | Check |
|---|---|
| Request only data the feature truly needs; be transparent about collection and use; process on-device where possible. | List every permission and the feature that needs it. |
| Ask when the user reaches the feature that needs access, so context explains the request. | No permission prompts at first launch unless the app cannot function without them (then ask during onboarding, see [onboarding-launch.md](onboarding-launch.md)). |
| Purpose string: one brief, specific, complete sentence in sentence case, active voice, saying how the data is used. | Read the string in the prompt; it names the benefit. |
| A custom pre-permission screen is allowed only with a single button that clearly leads to the system alert; no other actions, no close or cancel, and no button titled "Allow". | The only way forward is into the system prompt. |
| Never mislead before the system alert: no incentives, no screen styled as the request, no image of the alert, no annotating the alert. These cause App Store rejection. A legally required consent screen is allowed. | Review against the list. |
| For one-off location needs use the system location button (one-time access, like "Allow Once"). | Consider for share-my-location features. |
| Handle denial gracefully: the app stays usable; explain in context how to enable the setting. | Deny each permission and walk the flow. |

Protected data that needs permission includes location, health, contacts, calendar, photos/media, camera and microphone, Bluetooth, local network and the advertising identifier.

## Accounts and sign-in
- Require an account only if core functionality needs it; delay sign-in as long as possible and explain the benefits.
- Prefer Sign in with Apple; otherwise prefer passkeys over passwords. Label biometric buttons with the specific method ("Sign In with Face ID") and only where available; avoid an in-app biometrics opt-in, since the system controls it.
- Never prepopulate a password field ([text-input-keyboard.md](text-input-keyboard.md)).
- If people can create an account in the app they must be able to delete it, not just deactivate; start deletion in-app or link directly to the web page, keep both flows equally simple, tell people when it finishes, and explain subscription billing after deletion.

Legal framing for consent and dark patterns: [../ethics-dark-patterns.md](../ethics-dark-patterns.md).
