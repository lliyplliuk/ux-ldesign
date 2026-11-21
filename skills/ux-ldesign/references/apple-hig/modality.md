# Modality: sheets, alerts, action sheets

Use when: presenting a focused task, a confirmation or an error that interrupts. Sources: [Modality](https://developer.apple.com/design/human-interface-guidelines/modality), [Sheets](https://developer.apple.com/design/human-interface-guidelines/sheets), [Alerts](https://developer.apple.com/design/human-interface-guidelines/alerts), [Action sheets](https://developer.apple.com/design/human-interface-guidelines/action-sheets).

| Rule | Check |
|---|---|
| Present modally only with a clear benefit; keep the task short and simple; do not build an "app within the app". | Modal flow has one purpose and a visible end. |
| Make the task identifiable (title) and let people leave it; confirm before closing when data would be lost. | Close with unsaved input shows a confirmation. |
| Dismiss a modal before presenting another; show one sheet at a time from the main interface. | No stacked sheets. |
| Sheet buttons: Cancel/Close dismisses without saving, Done saves, Back goes to a previous step. Do not show all three together; Cancel sits at the leading top edge for single-view sheets. | Button set per sheet. |
| Resizable iPhone sheet: support the medium detent for progressive disclosure, include a grabber, support swipe to dismiss. | Drag and swipe both work. |
| Use sheets for brief, occasional interactions; use a non-modal panel when people repeatedly enter data and watch results. | Not used for long workflows. |

## Alerts
| Rule | Check |
|---|---|
| Use sparingly; not for pure information, not on app launch, not for common undoable actions. | Count alerts per flow. |
| Title states the situation briefly; message only if it adds value; do not explain the buttons. | Read the copy aloud. |
| At most three buttons, with specific verbs; avoid "OK" unless the alert is purely informational. | Button labels are verbs. |
| Destructive style for destructive actions the user did not deliberately choose; always include Cancel. | Cancel present with destructive action. |
| Offer choices related to an intentional action in an action sheet, not an alert. | Action sheet for "Delete / Archive / Cancel". |
| Avoid alerts that scroll; let people suppress repeating alerts. | Short text; suppress option for repeats. |
| Use a dedicated alert, not a notification, to show an error ([notifications.md](notifications.md)). | No error text sent as push. |
