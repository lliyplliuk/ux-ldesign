# Haptics

Use when: adding tactile feedback to iPhone interactions. Source: [Playing haptics](https://developer.apple.com/design/human-interface-guidelines/playing-haptics).

| Rule | Check |
|---|---|
| Prefer standard components (switches, sliders, pickers): they already play system haptics. | Do not add a second haptic on top. |
| Use the three predefined feedback families as documented: notification (success, warning, error outcomes), impact (physical collision metaphor), selection (values changing). | Each haptic maps to its documented meaning. |
| Keep haptics consistent: the same event always feels the same. | Audit all haptic calls by event. |
| Complement visual and audio feedback; never make a haptic the only signal. | Feature works with haptics disabled or on iPad. |
| Do not overuse: short haptics for discrete events, not continuous buzz in routine UI. | Count haptics in a typical session. |
| Make haptics optional where they could annoy or affect other experiences (e.g. audio playback). | A setting or system respect exists. |
| Custom patterns (transient taps, continuous vibration, sharpness and intensity) fit games and specialised apps. | Reserve for those cases. |

Haptics depend on device and input hardware; the interface must work without them.

## Audit procedure
1. List every user event that triggers a haptic (code search for feedback generators plus standard components).
2. Classify each as notification, impact or selection; flag any that do not fit the documented meaning.
3. Flag events with two haptics at once (standard component plus a custom one) and events that fire continuously.
4. Confirm each event still communicates through visuals or sound when haptics are unavailable or switched off.
5. Report the result as a table: event, haptic type, meaning match (yes/no), fallback (yes/no).

Haptics are supplementary, never a requirement: report any flow that fails when haptics are off.
