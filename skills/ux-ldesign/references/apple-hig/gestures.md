# Gestures and edge-swipe

Use when: designing swipe actions, custom gestures, or back navigation. Source: [Gestures](https://developer.apple.com/design/human-interface-guidelines/gestures).

| Rule | Check |
|---|---|
| Use standard gestures with their standard meaning; do not give tap or swipe an app-specific meaning, and do not invent a gesture for a standard action. | Each gesture matches its common system use. |
| Always provide another way: voice, keyboard, Switch Control users cannot rely on a gesture. | Every gesture action also has a visible control. |
| A side-edge swipe for back is a shortcut: keep the Back button visible. | Back button present on pushed screens. |
| Do not define custom gestures that clash with system gestures (edge swipes, app-switcher, Control Center). | Try the gesture from every screen edge. |
| Respond immediately and give feedback while the gesture is in progress; communicate extent of movement needed. | Content tracks the finger. |
| Show when a gesture is unavailable (locked item, disabled control), so the app does not seem frozen. | Unavailable state looks distinct. |
| Add a custom gesture only for a frequent, specialised task not covered by standard gestures (drawing, games); make it distinct, easy to learn, and teach it. | Test with first-time users ([../research.md](../research.md)). |
| Use shortcut gestures only to supplement standard routes; people must still reach the task with an extra tap or two. | Full path without custom gestures exists. |
| Simultaneous recognition of several gestures is rarely useful outside games. | Gesture conflicts tested. |

Related: swipe-to-dismiss on sheets ([modality.md](modality.md)); gesture alternatives for accessibility ([accessibility.md](accessibility.md)).

## Audit procedure
1. Inventory gestures: standard ones (tap, swipe, drag, pinch, touch and hold) and custom ones.
2. For each custom gesture, name the frequent task it serves, the visible alternative control, and the way users learn it.
3. Test every screen edge and the bottom and top system areas for conflicts with system gestures.
4. Run the flows with VoiceOver and Switch Control: each action must complete without the gesture.
