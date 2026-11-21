# Text input, keyboards, forms on iOS

Use when: designing data entry or reviewing keyboard behaviour. Sources: [Text fields](https://developer.apple.com/design/human-interface-guidelines/text-fields), [Virtual keyboards](https://developer.apple.com/design/human-interface-guidelines/virtual-keyboards), [Entering data](https://developer.apple.com/design/human-interface-guidelines/entering-data). Web forms: [../forms-commerce.md](../forms-commerce.md).

| Rule | Check |
|---|---|
| Ask for as little as possible: get information from the system where permitted, offer choices instead of typing, allow paste and drag-and-drop. | Count typed fields per flow; prefill from system data. |
| Say clearly what is needed and which fields are required before people can continue. | Required fields marked before submit. |
| Show a hint (placeholder) of the field's purpose; match field size to expected text length. | Hint disappears sensibly; width fits content. |
| Use secure text fields for private data; never prepopulate a password field. | Characters are masked. |
| Choose the keyboard type that matches the content (email, number, phone, URL). | Focus each field on a device; the right keys appear. |
| Customise the Return key when it clarifies the action (Next, Search, Done). | Return label matches what it does. |
| Validate dynamically when it helps and format numeric data with a formatter. | Errors appear while fixing is still easy. |
| Offer a Clear button at the trailing end for erasing input. | Present on free-text fields. |
| Tabbing/Next between fields follows reading order. | Next key walks the form top to bottom. |
| Use the keyboard layout guide so the keyboard is part of the layout; place custom controls above it deliberately. | Focused field and its submit action stay visible with the keyboard open. |
| Play the standard key sound for custom input views; provide an obvious switch between keyboards in custom keyboards. | Only if you build custom input. |
| Present a text field only when it is necessary; short input only (use a text view for long text). | Alternatives considered. |

Reviewer shortcut: open every input screen with the keyboard, largest text size and Dark Mode; the submit control must remain reachable.
