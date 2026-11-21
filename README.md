# ux-ldesign

A UX design and review skill for AI coding agents: Claude Code, Codex and other agents that support the Agent Skills format. It turns an agent into a careful UX reviewer and designer: it walks a task end to end, checks flows, forms, states, copy and accessibility against sourced rules, and reports findings with location, consequence, severity, fix and how to re-check.

The core (`skills/ux-ldesign/SKILL.md`) is small. Detailed reference files are loaded only when the task needs them.

## What it covers

| File | Topic |
| --- | --- |
| `skills/ux-ldesign/references/workflow.md` | Design, review and research steps; ten heuristics; response-time limits; severity scale |
| `skills/ux-ldesign/references/laws.md` | UX laws chosen by problem, with their limits |
| `skills/ux-ldesign/references/principles.md` | Shneiderman, Tognazzini, Norman, ISO 9241-110 as yes/no checklists |
| `skills/ux-ldesign/references/accessibility.md` | EAA, EN 301 549, ADA, WCAG 2.2 criteria and manual checks |
| `skills/ux-ldesign/references/forms-commerce.md` | Forms, validation, error messages, cart and checkout |
| `skills/ux-ldesign/references/patterns.md` | Navigation/IA, search, empty states, loading, tables, notifications, onboarding |
| `skills/ux-ldesign/references/writing-i18n.md` | Interface text, microcopy, localisation, scripts, RTL, locale formats |
| `skills/ux-ldesign/references/ethics-dark-patterns.md` | Deceptive design, consent, cancellation, EU/US legal exposure (not legal advice) |
| `skills/ux-ldesign/references/mobile-ios.md` | Native iPhone/iPad rules: targets, safe areas, Dynamic Type, navigation, permissions |
| `skills/ux-ldesign/references/apple-hig/` | Apple HIG by topic (16 files, routed via `index.md`) |
| `skills/ux-ldesign/references/mobile-android.md` | Android / Material 3: targets, edge-to-edge, predictive back, adaptive layouts |
| `skills/ux-ldesign/references/ai-ux.md` | AI/LLM interfaces: uncertainty, correction, disclosure |
| `skills/ux-ldesign/references/research.md` | Research methods, sample sizes, metrics, reading usability tests |
| `skills/ux-ldesign/references/skill-landscape.md` | Comparison of other UX skills and what to load for mobile detail |

## Principles

- **Every rule is checkable.** Rules are phrased so they can be answered yes/no with evidence from the interface.
- **Sourced to primary sources.** W3C, NN/g, Baymard, GOV.UK, Apple HIG, Android/Material, EUR-Lex and similar. Claims that could not be verified against a primary source are marked `(unverified)`.
- **Numbers keep their conditions.** Research figures are used only within the conditions they were measured in.
- **Progressive loading.** A small core plus references opened on demand, to keep the agent's context small.
- **Evidence over guesses.** For a mockup or screenshot the skill concludes only on what is visible and marks interactions that need checking.

## Install

### skills.sh

```bash
npx skills add lliyplliuk/ux-ldesign
```

### Claude Code plugin marketplace

```
/plugin marketplace add lliyplliuk/ux-ldesign
/plugin install ux-ldesign@ux-ldesign
```

### Manual

Clone the repository and copy the `skills/ux-ldesign` folder into your agent's skills directory:

```bash
git clone https://github.com/lliyplliuk/ux-ldesign
cp -r ux-ldesign/skills/ux-ldesign ~/.claude/skills/   # Claude Code
cp -r ux-ldesign/skills/ux-ldesign ~/.codex/skills/    # Codex
```

No scripts, hooks or network calls: the package contains instructions and references only.

## Usage

The skill triggers on UX tasks, or call it by name. Examples:

- "Review the checkout flow in this repo for UX problems and rank findings by severity."
- "Design the onboarding flow for a budgeting app: main path, states, key copy and acceptance criteria."
- "Audit this signup form against WCAG 2.2 and the forms rules."
- "Проверь UX экрана настроек на скриншоте."
- "Plan a usability test for the cancellation flow."

The skill replies in the language of the request.

## Credits

- [Laws of UX](https://lawsofux.com) (Jon Yablonski) and Nielsen Norman Group research.
- [justinwetch/HIGAgentSkills](https://github.com/justinwetch/HIGAgentSkills) (MIT): the routing-index idea for the Apple HIG material.
- [pbakaus/impeccable](https://github.com/pbakaus/impeccable) (Apache-2.0): structural inspiration.
- [dickwu/apple-design-skill](https://github.com/dickwu/apple-design-skill): ideas only, no content reused.
- [hamen/material-3-skill](https://github.com/hamen/material-3-skill): linked for deeper Material 3 detail.

Content is paraphrased and linked to official documentation. This project is not affiliated with Apple or Google.

## License

MIT. See [LICENSE](LICENSE).
