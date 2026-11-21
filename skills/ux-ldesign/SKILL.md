---
name: ux-ldesign
description: "Design and review UX for websites and apps: user flows, navigation, forms and checkout, states, microcopy, Nielsen heuristics, UX laws, accessibility (WCAG 2.2, EAA), dark patterns, mobile UX (iOS/Android), AI-interface UX, and usability research. Use for UX audits, interface problem analysis, interaction design and usability-test planning; use for pure visual styling only when there is a UX task. Also triggers on Russian requests: «UX-аудит», «юзабилити», «проверь UX», «сценарии пользователя», «доступность»."
---

# UX design

Reply in the user's language. Start from the user's task, context of use, platform and an observable success signal. Take constraints from the request, the product and the design system. If an interface is accessible, walk the flow. For a mockup or screenshot, conclude only on what is visible and mark interactions that need checking. Match depth to the request.

- **Design.** Describe entry point, main path, user decisions, outcome and recovery from failure. Choose familiar patterns; compare options by real cost: extra work, errors, learnability, accessibility. Deliver the action flow, states, key copy and verifiable acceptance criteria. Implement changes if the task includes it.
- **Review.** Walk the task to its result and check the relevant branches. For each problem give location and conditions, observation, consequence for the task, severity, fix and how to re-check. Rank by damage, frequency (if data exists) and recoverability. For a review request, deliver findings without edits.
- **Research.** Name the doubt, pick a method and user segments. Phrase tasks without hinting the path. Separate observations, analytic hypotheses and research-confirmed conclusions. Keep caveats about sample and data access.

For each decision pick the principles that explain the concrete effect. Use research numbers only within their measurement conditions. Check applicable accessibility requirements by standard and platform. When principles conflict, compare options against the user's task and test the key assumption.

## References

- `references/laws.md` — pick a UX law by problem and learn its limits.
- `references/workflow.md` — design/review/research steps, ten heuristics, response-time limits, severity scale, example finding.
- `references/accessibility.md` — legal baseline (EAA, EN 301 549, ADA), WCAG 2.2 criteria and manual checks.
- `references/forms-commerce.md` — forms, validation, errors, checkout and product-list rules.
- `references/ethics-dark-patterns.md` — deceptive design, consent, cancellation, EU/US rules.
- `references/patterns.md` — empty states, search, tables, notifications, onboarding, performance.
- `references/writing-i18n.md` — UX writing, microcopy, localisation, RTL.
- `references/mobile-ios.md` — iOS rules (targets, safe areas, Dynamic Type, navigation, permissions).
- `references/apple-hig/index.md` — detailed Apple HIG by topic; open via the index after mobile-ios.md.
- `references/mobile-android.md` — Android / Material 3 rules (targets, edge-to-edge, predictive back, adaptive layouts).
- `references/principles.md` — Shneiderman, Tognazzini, Norman, ISO 9241-110 as complementary checklists.
- `references/ai-ux.md` — AI/LLM interface guidelines (uncertainty, correction, disclosure).
- `references/research.md` — research methods, sample sizes, metrics; severity scale lives in workflow.md.
- `references/skill-landscape.md` — compare approaches and sources of other UX skills; mobile deep references to load on demand.
