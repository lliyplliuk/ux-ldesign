# Navigation: tab bar, toolbar, back, search, sidebar

Use when: choosing top-level structure or placing actions on iPhone/iPad. Sources: [Tab bars](https://developer.apple.com/design/human-interface-guidelines/tab-bars), [Toolbars](https://developer.apple.com/design/human-interface-guidelines/toolbars), [Sidebars](https://developer.apple.com/design/human-interface-guidelines/sidebars), [Searching](https://developer.apple.com/design/human-interface-guidelines/searching), [Gestures](https://developer.apple.com/design/human-interface-guidelines/gestures).

## Tab bar
| Rule | Check |
|---|---|
| Tabs navigate between sections; they never perform actions. | No "Add"/"Share" tab. |
| Keep the bar visible while moving around the app. | It does not vanish on pushed screens within a section. |
| Use as few tabs as the structure needs; avoid overflow tabs. Visible count can shrink with device size and orientation. | Open on the smallest iPhone, landscape: all sections reachable. |
| If users can pick their own tabs, default to five or fewer to stay consistent between compact and regular widths. | Default tab set count. |
| Never disable or hide a tab because its content is empty; show an empty state instead. | Every tab tappable at all times. |
| Give each tab a symbol and a text label. Prefer SF Symbols. Badge only for critical information. | Labels present; badge use justified. |
| A dedicated search tab can sit at the trailing end. | If search is core, consider it. |

## Toolbar and back
- A toolbar acts on the current view, navigates, or orients. Group items by function and frequency; keep navigation and key actions (Done, Close, Save) in distinct, familiar positions. Put overflow into a More menu rather than crowding.
- Use the standard Back and Close buttons; use a prominent style only for key actions like Done or Submit.
- Large titles help orientation on scrolling screens.
- Reduce toolbar backgrounds and tinting; avoid label colours similar to the content behind. Check: icon-only controls have recognisable system symbols.

## Search
- Make content searchable in one consistent place; show the current scope; offer suggestions; think before displaying search history (privacy).

## Sidebar (iPad)
- Prefer a tab bar first; use a sidebar when the hierarchy is large. At most two levels. Allow customisation. Do not put critical actions at the bottom of a sidebar.

## Back gesture
A swipe from the screen side is a shortcut and must supplement, never replace, a visible Back button. See [gestures.md](gestures.md).
