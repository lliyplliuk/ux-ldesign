# Forms and checkout

Use when: designing or auditing forms, validation, error messages, cart or checkout flows.

## Fields and labels

| Rule | Check | Source |
|---|---|---|
| Every input has a visible label above it, short, sentence case, no trailing colon. | Each field has a `<label for>`; label stays visible while typing. | [GOV.UK text input](https://design-system.service.gov.uk/components/text-input/) |
| Never use a placeholder as label, hint or example. It vanishes on typing, hurts review and error recovery, and is often low contrast. | No field whose only name is placeholder text. | [NN/g placeholders](https://www.nngroup.com/articles/form-design-placeholders/), GOV.UK above |
| Mark every required field (asterisk or the word "Required"); optionally mark optional ones. Login forms may skip markers. | Required state is visible per field, not only in a note at the top. Baymard: 32% of test participants skipped a required field when only optional ones were marked; 50% of sites mark neither or only one kind. | [NN/g required fields](https://www.nngroup.com/articles/required-fields/), [Baymard](https://baymard.com/blog/current-state-of-checkout-ux) |
| Use `autocomplete` tokens wherever an input purpose applies (WCAG 1.3.5, AA). | Name, email, address, card fields carry the right token; browser autofill fills them. | [WCAG 1.3.5](https://www.w3.org/WAI/WCAG22/Understanding/identify-input-purpose.html) |
| Whole numbers: `inputmode="numeric"`; decimals: `inputmode="decimal"`. Avoid `type="number"` (scroll changes value, weak feedback). `spellcheck="false"` on names, emails, reference numbers. | Phone opens numeric keypad for codes; no value change on mouse-wheel. | [GOV.UK text input](https://design-system.service.gov.uk/components/text-input/) |
| Size input widths to expected content (postcode short, name wide). | Width hints at answer length. | GOV.UK text input |
| Accept messy input: ignore spaces, hyphens, brackets, full stops in numbers and codes; reject only what cannot be correct or is ambiguous. | Paste "0123 456-789" into a phone/card field: accepted and normalised. | [GOV.UK validation](https://design-system.service.gov.uk/patterns/validation/) |
| Do not ask for the same data twice in one process (WCAG 3.3.7, A). | Shipping to billing, previously entered values prefilled or selectable. | [WCAG 3.3.7](https://www.w3.org/TR/WCAG22/) |

## Validation timing

Sources disagree; pick one and state it in the spec.

- GOV.UK: validate on submit ("Wait until they try to move to the next part of the service"), not on leaving a field and not while typing; always validate on the server; `novalidate` on the form, no `required` attribute. [GOV.UK validation](https://design-system.service.gov.uk/patterns/validation/)
- NN/g: inline validation once the user has finished a field; never show errors while the user is still typing; success indicator only for complex fields (username, password strength). [NN/g](https://www.nngroup.com/articles/errors-forms-design-guidelines/)
- Check: no error appears mid-keystroke; server rejects bad input even with JS off.

## Errors

| Rule | Check | Source |
|---|---|---|
| On submit with errors: error summary at top, keyboard focus moved to it, each item links to its field. | Tab lands on summary; link jumps to field. | GOV.UK validation |
| Also an error message next to each bad field, same wording as in the summary. | Message sits after label/hint, before input. | [GOV.UK error message](https://design-system.service.gov.uk/components/error-message/) |
| Do not rely on the summary alone; no tooltips or hover-only errors. | Error visible without hover. | NN/g errors |
| Error = text + icon/border, not colour only (WCAG 1.4.1); prefix hidden text "Error:" for screen readers; prefix page `<title>` with "Error: ". | Greyscale screenshot still shows the error. | GOV.UK validation, error message |
| Say what went wrong and how to fix it, plain language, matching the field label. Empty: instruction ("Enter your name"). Too long: rule ("Name must be 35 characters or less"). No "invalid", "please", "you forgot", codes, blame. | Each message answers "what" and "what now" without a code. | GOV.UK error message; NN/g (explicit, polite, constructive) |
| Never clear fields after an error: redisplay valid and invalid answers as entered. | Submit with one bad field: all others keep values. | GOV.UK validation |
| Same error repeated by users 3+ times: review analytics, retest, rewrite message. | Error-rate per field is tracked. | NN/g errors |
| Error identified in text and suggestion given (WCAG 3.3.1, 3.3.3, A/AA). | See accessibility.md. | [WCAG 3.3](https://www.w3.org/TR/WCAG22/) |

## Checkout and cart (Baymard)

Benchmarks change; Baymard announced retested checkout research for Q2 2027, so re-check numbers then. [Baymard](https://baymard.com/blog/current-state-of-checkout-ux)

- Why users leave (average cart abandonment 70.22%, mean of 50 studies 2006-2025; reasons exclude "just browsing"): extra costs too high 40%, delivery too slow 20%, distrust of card handling 19%, forced account 18%, long/complex checkout 17%, errors or crashes 17%, returns policy 13%, total cost not visible up front 12%, card declined 10%, too few payment methods 9%. [Baymard abandonment list](https://baymard.com/lists/cart-abandonment-rate)
- Show shipping, tax and fees before the final step (earliest: cart or product page). Check: total on the cart equals the total on the pay button.
- Guest checkout always available and prominent; offer account creation on the confirmation page after purchase. Baymard: 56% of sites do not move account creation to confirmation. [Baymard](https://baymard.com/blog/current-state-of-checkout-ux)
- Cut fields: average 11.3 fields (2024), most sites need about 8. Use one "Full name" field, collapse "Address line 2" behind a link, default billing = shipping and hide the billing fields until unchecked, offer address lookup/autocomplete. Check: count fields on the default path. [Baymard fields](https://baymard.com/blog/checkout-flow-average-form-fields)
- Phone number: explain why it is needed or drop it; 68% of respondents were reluctant to give one, 47% of sites give no reason. [Baymard](https://baymard.com/blog/current-state-of-checkout-ux)
- Collapse completed accordion steps into summaries (72% of sites do not); show delivery dates, not only speed names (48% show speed only); quantity control as buttons or button + text field in the cart (95% do not). Same source.
- Payment: show accepted card types up front, tolerate spaces in card numbers, state clearly when a card is declined and what to try (declines hit 10% of abandoners). Show returns policy near price and pay button (13% cite it). Source: abandonment list.
- Cart survives reload and return visits; edit quantity or remove without leaving the page (unverified: Baymard cart-persistence detail not fetched; from the audit's recall).
- Trust: put security and payment cues beside card fields (19% abandon from distrust). Abandonment list.
