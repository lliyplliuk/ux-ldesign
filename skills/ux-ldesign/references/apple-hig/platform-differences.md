# iPad, Watch, Vision, multitasking

Use when: adapting an iPhone design to other Apple devices. Sources: [Designing for iPadOS](https://developer.apple.com/design/human-interface-guidelines/designing-for-ipados), [watchOS](https://developer.apple.com/design/human-interface-guidelines/designing-for-watchos), [visionOS](https://developer.apple.com/design/human-interface-guidelines/designing-for-visionos), [Multitasking](https://developer.apple.com/design/human-interface-guidelines/multitasking), [Layout](https://developer.apple.com/design/human-interface-guidelines/layout).

## iPad
- Use the large display to raise the content people care about, with fewer modal interfaces and full-screen transitions; place controls where they are easy to reach.
- Size and density follow viewing distance and input mode; support touch, keyboard, trackpad and Apple Pencil, and combinations.
- Apps can run windowed or with other apps: pause tasks needing attention when switched away, handle audio interruptions, finish user-initiated tasks in the background, and adapt smoothly to arbitrary window sizes (size classes, [layout.md](layout.md)). People may think the app is broken if it resists multitasking.
- Prefer a tab bar that can become a sidebar; at most two sidebar levels ([navigation.md](navigation.md)).

## Apple Watch
- Glanceable, single-screen interactions delivering critical information with one or two gestures; shallow hierarchy.
- Use complications and notifications for timely information; let the app work independently of the iPhone app.
- Minimum control size 28x28 pt, default 44x44 pt; default text 16 pt, minimum 12 pt ([Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility)).

## Apple Vision Pro
- Prioritise comfort and safety; place content within the person's field of view relative to the head; avoid overwhelming, jarring or fast motion without a stationary reference.
- Offer indirect (eyes plus pinch) interaction; direct gestures only for infrequent use; control minimum 28x28 pt, default 60x60 pt; text default 17 pt, minimum 12 pt.
- Avoid encouraging a lot of movement in fully immersive experiences.

## Decision aid
| Question | Rule |
|---|---|
| Same codebase, many form factors? | Branch on size class, not device model. |
| Feature on phone only? | Keep the core function parity across classes. |
| Watch version needed? | Only for glanceable, timely tasks. |
