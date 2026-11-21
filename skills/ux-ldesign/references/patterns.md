# Interaction patterns

Use when: designing or auditing navigation/IA, search, empty states, loading, progressive disclosure, data tables, notifications, onboarding.

## Navigation and information architecture

| Rule | Check | Source |
|---|---|---|
| Keep primary navigation visible, not hidden behind a menu icon. In NN/g tests hidden nav was used 27% of the time on desktop vs 48% visible; on mobile 57% hidden vs 86% combo (visible + hidden); content discovery without search dropped over 20%; tasks rated 21% harder (179 users, 6 sites). | Top-level destinations visible on desktop; mobile shows the key ones plus a menu for the rest. | [NN/g hamburger menus](https://www.nngroup.com/articles/hamburger-menus/) |
| Group by user mental model (card sorting); label with the most informative word first; labels distinct from each other; each option listed once. | Card-sort or tree-test result; no duplicate labels. | [NN/g mega menus](https://www.nngroup.com/articles/mega-menus-work-well/) |
| Hover menus: open after the pointer rests about 0.5 s, show within 0.1 s, close after about 0.5 s outside, tolerate diagonal travel; menu also works by keyboard and screen reader; start with simple link-to-landing-page navigation. | Diagonal mouse move does not close the menu; Tab/Enter opens it. | NN/g mega menus |
| Keep navigation in the same relative order across pages (WCAG 3.2.3, AA) and identify repeated components consistently (3.2.4, AA). | Compare nav on 3 page types. | [WCAG 2.2](https://www.w3.org/TR/WCAG22/) |
| Provide more than one way to find a page (WCAG 2.4.5, AA). | Nav plus search, sitemap or links. | WCAG 2.2 |

## Search

- Show a type-in box (not a link) on the home page, top of page, upper right (upper left nearly as good); on complex interior pages too. Width fits a typical query. Making useit.com's search a box instead of a link raised search use 91%. Check: box visible on every key page without scrolling. [NN/g search](https://www.nngroup.com/articles/search-visible-and-simple/)

## Empty states

- Tell the status (loading vs error vs truly empty; never flash "no records" while loading), give a learning cue (what the feature is for), and give a direct action (button, link, steps). Check: each list/table/panel has a designed empty, loading and error state. [NN/g empty states](https://www.nngroup.com/articles/empty-state-interface-design/)

## Loading and perceived performance

| Rule | Check | Source |
|---|---|---|
| Response limits: up to 0.1 s feels instant (no feedback needed); up to 1 s keeps flow, delay noticed; beyond 1 s show that work is happening; around 10 s is the attention limit, so show percent-done and a way to cancel. | Time each action; add feedback at the matching limit. | [NN/g response times](https://www.nngroup.com/articles/response-times-3-important-limits/) |
| Under 1 s: no spinner or skeleton (flash feels jarring). 2-10 s: spinner for a module, skeleton for a full page that mirrors the real layout. Over 10 s or uploads/conversions: progress bar with estimate. No frame-only skeletons (header/footer only). | Skeleton shape matches loaded layout. | [NN/g skeleton screens](https://www.nngroup.com/articles/skeleton-screens/) |
| Core Web Vitals, 75th percentile of page loads, mobile and desktop separately: LCP good <= 2.5 s, poor > 4.0 s; INP good <= 200 ms, poor > 500 ms; CLS good <= 0.1, poor > 0.25. | Field data (CrUX/RUM), not only lab. | [web.dev LCP](https://web.dev/articles/lcp), [INP](https://web.dev/articles/inp), [CLS](https://web.dev/articles/cls), [vitals](https://web.dev/articles/vitals) |
| Optimistic UI: apply the user's change instantly and reconcile with the server; on failure roll back and say so with a retry. The 0.1 s link is a design inference, not an NN/g rule; the rollback-with-error-message pattern is documented engineering practice (React, TanStack Query). | Kill the network: UI reverts and explains. | NN/g response times, [React useOptimistic](https://react.dev/reference/react/useOptimistic), [TanStack Query](https://tanstack.com/query/latest/docs/framework/react/guides/optimistic-updates) |

## Progressive disclosure

- Show frequent options first, rare ones behind a visible, well-labelled control (strong information scent); two levels is the practical maximum; avoid several paths to the same secondary options. Decide the split from task analysis and usage frequency. Check: usage data supports what is primary; users find the secondary level in testing.
- Staged disclosure (wizard) fits steps with little interdependence; avoid it when users must jump back and forth. [NN/g progressive disclosure](https://www.nngroup.com/articles/progressive-disclosure/)

## Data tables ([NN/g](https://www.nngroup.com/articles/data-tables/))

- First column is a human-readable record name, not an ID; default columns ordered by importance, related ones adjacent.
- Filters discoverable with a clear indicator when active; support sort, search and scanning together.
- Freeze header row/column when the table exceeds the screen; row separators, zebra or hover to keep place; low-effort hide/reorder columns with a state indicator; never drag-only reordering (offer a menu).
- Edit: in-place only for narrow tables; avoid modals for deep edit (they hide neighbours); prefer a non-modal side panel.
- Actions: 1-2 inline; more in a menu; batch actions via row checkboxes, plus "Select all" when whole-set actions are common.
- Check: all four tasks (find, compare, edit one row, act on records) completed in a test.

## Notifications, toasts, alerts

| Rule | Check | Source |
|---|---|---|
| Match channel to type: indicator (passive cue), validation (tied to input, must be fixed), notification (system event, action-required or passive). Toasts only for passive/confirmations, never for errors that need action (one user missed an error that faded after 5 s). | No error exists only in a toast. | [NN/g indicators, validations, notifications](https://www.nngroup.com/articles/indicators-validations-notifications/) |
| Reserve modal dialogs for severe errors; use banners or inline labels for minor ones. | Modal count per flow. | [NN/g error messages](https://www.nngroup.com/articles/error-message-guidelines/) |
| Status messages must be announced without moving focus (WCAG 4.1.3, AA): `role="status"` for results/progress, `role="alert"` for errors. | Screen reader announces the message. | [WCAG 4.1.3](https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html) |
| Banner (GOV.UK): one per page, placed before the `<h1>`, text heading such as "Success" so meaning is not colour-only, not for validation errors and not alongside an error summary; skip banners in linear journeys (use a confirmation page). | Max one banner. | [GOV.UK notification banner](https://design-system.service.gov.uk/components/notification-banner/) |
| Toast with undo stays long enough to read and act (Google Drive example vanishes after a few seconds); do not make undo the only recovery path. | Same change is reversible from history or the item itself after the toast is gone. | [NN/g user control](https://www.nngroup.com/articles/user-control-and-freedom/) |

## Onboarding

- Often unnecessary: NN/g found tutorials did not improve task performance; let users learn by doing. Avoid deck-of-cards tours; if used, one concept per card, minimal cards, visible Skip.
- Prefer contextual help at first encounter with an actionable feature, and teachable moments in error messages; interactive walkthroughs only for complex or unfamiliar workflows.
- Ask for personal data or permissions only when it is justified; say why and how it will be used; defer otherwise.
- Check: new user completes the first key task without the tour; Skip is one tap. [NN/g mobile onboarding](https://www.nngroup.com/articles/mobile-app-onboarding/)
