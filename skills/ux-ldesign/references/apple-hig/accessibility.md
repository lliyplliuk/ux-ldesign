# Accessibility on Apple platforms

Use when: auditing any iOS/iPadOS screen for accessibility. Sources: [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility), [VoiceOver](https://developer.apple.com/design/human-interface-guidelines/voiceover), [Motion](https://developer.apple.com/design/human-interface-guidelines/motion). For the web, use [../accessibility.md](../accessibility.md).

## Numbers
| Item | iOS / iPadOS value |
|---|---|
| Control size | default 44x44 pt, minimum 28x28 pt |
| Padding | about 12 pt around bezeled elements, about 24 pt around elements without a bezel |
| Text size | default 17 pt, minimum 11 pt |
| Contrast | up to 17 pt: 4.5:1; 18 pt: 3:1; bold at any size: 3:1 |

## Checks
| Rule | Check |
|---|---|
| Every key interface element has an accessibility label; meaningful images are described; decorative images are hidden from VoiceOver. | Swipe through with VoiceOver on: each stop is understandable. |
| Use titles and headings, and specify grouping, order and linking; announce content or layout changes. | Rotor navigation by heading works. |
| Charts and infographics are accessible (summary or data alternative). | VoiceOver reads the data meaning. |
| Convey information with more than colour; prefer system colours. | See [color-dark-mode.md](color-dark-mode.md). |
| Support Dynamic Type; text does not truncate at large sizes. | See [typography-dynamic-type.md](typography-dynamic-type.md). |
| Provide alternatives to gestures; support Voice Control, keyboard and Switch Control. | All actions reachable without a gesture. |
| Keep actions simple; minimise time-boxed UI elements. | No auto-dismissing critical content. |
| Captions, subtitles, transcripts and audio descriptions for media; haptics and visual cues beside audio cues. | Mute the device: nothing is lost. |
| Motion: make it optional, avoid fast or blinking animation, offer opt-out of flashing, replace big transitions with fades when Reduce Motion is on, tighten springs. | Toggle Reduce Motion and replay main transitions. |
| Assistive Access: for a simplified mode keep core functionality, break flows into one interaction per screen, and confirm hard-to-undo actions twice. | Only if you support it. |

Related heuristics and WCAG mapping: [../accessibility.md](../accessibility.md).
