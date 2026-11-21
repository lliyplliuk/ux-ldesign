# Apple HIG routing index

Use when: a task needs detail on an Apple platform (iPhone, iPad, Watch, Vision) beyond the overview in [../mobile-ios.md](../mobile-ios.md). Open the topic file for the screen element in question, not the whole folder.

All rules below were re-read on 2026-11-21 from the official pages at `developer.apple.com/design/human-interface-guidelines/<slug>` and are paraphrased. HIG changes often (Liquid Glass update, Dec 2025 typography update): when a number decides a verdict, open the linked page.

| Topic | File | Open when |
|---|---|---|
| Screen structure, safe areas, size classes | [layout.md](layout.md) | any new screen, iPad/landscape/resizable windows, spacing questions |
| Tab bar, toolbar, back, search, sidebar | [navigation.md](navigation.md) | choosing top-level navigation or placing actions |
| Sheets, alerts, action sheets, modality | [modality.md](modality.md) | any interruption, confirmation, or focused sub-task |
| Gestures and edge-swipe | [gestures.md](gestures.md) | custom gestures, swipe actions, back navigation |
| Type sizes, Dynamic Type | [typography-dynamic-type.md](typography-dynamic-type.md) | font sizing, text scaling, truncation |
| Color, contrast, Dark Mode | [color-dark-mode.md](color-dark-mode.md) | palettes, tints, dark appearance, contrast numbers |
| Icons and SF Symbols | [icons-sf-symbols.md](icons-sf-symbols.md) | icon choice, tab/toolbar glyphs |
| Haptics | [haptics.md](haptics.md) | adding or auditing tactile feedback |
| Permissions and privacy | [permissions-privacy.md](permissions-privacy.md) | any system permission prompt, data collection, sign-in |
| Notifications and badges | [notifications.md](notifications.md) | push content, interruption levels, badges |
| Onboarding, launch, tips | [onboarding-launch.md](onboarding-launch.md) | first run, launch screen, state restore, in-app help |
| Text fields, keyboards, forms | [text-input-keyboard.md](text-input-keyboard.md) | data entry, validation, keyboard types |
| Accessibility and VoiceOver | [accessibility.md](accessibility.md) | any audit; target sizes, contrast table, labels, motion |
| Loading, feedback, errors, undo | [feedback-errors-offline.md](feedback-errors-offline.md) | async states, failure messages, reversibility |
| iPad, Watch, Vision, multitasking | [platform-differences.md](platform-differences.md) | adapting beyond iPhone |
| Generative AI features | [../ai-ux.md](../ai-ux.md) | Apple's AI page is summarised there |

## Attribution and method

- Structure (routing table by screen element, accessibility-first audit order, size-class thinking, cross-platform vocabulary) was inspired by [dickwu/apple-design-skill](https://github.com/dickwu/apple-design-skill) (no licence declared: ideas only, no text copied) and [justinwetch/HIGAgentSkills](https://github.com/justinwetch/HIGAgentSkills) (MIT; routing-index idea and per-topic split). Content here is rewritten from Apple's pages, not from those repos.
- Apple's wording is Apple's. Link the source page when quoting a rule in a finding.
- For exhaustive lookup (157 pages, exact values) install or read HIGAgentSkills, then verify against the official page.
