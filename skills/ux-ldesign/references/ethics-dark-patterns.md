# Ethics and dark patterns

Use when: reviewing flows for deceptive design (sign-up, checkout, consent, cancellation, notifications) or checking EU/US legal exposure. Not legal advice; flag findings for counsel. Legal state checked 2026-11-21.

## Pattern checklist ([deceptive.design/types](https://www.deceptive.design/types))

| Pattern | Detect by |
|---|---|
| Sneaking | Walk the flow: any fee, add-on or condition first shown after commitment? |
| Hidden costs | Advertised price vs final total; fees appearing only at the last step. |
| Hidden subscription | Does one-off purchase or free trial enrol into recurring charges? Is that stated next to the button? |
| Forced action | Extra unwanted step (account, newsletter, data) needed to reach the goal. |
| Hard to cancel | Count steps/channels to cancel vs to sign up (online sign-up, phone-only cancel = fail). |
| Obstruction | Time/steps to find info or finish a task the business dislikes (delete account, refund). |
| Preselection | Pre-ticked boxes, default-on add-ons, default paid tier. |
| Trick wording | Double negatives, "Don't not send me..."; buttons whose label does the opposite of expected. |
| Visual interference | Decline link low contrast/tiny; accept button large and coloured; hidden close icon. |
| Confirmshaming | Decline copy blames the user ("No, I hate saving money"). |
| Fake urgency / fake scarcity | Countdown resets on reload; "only 2 left" static; same banner for every product. |
| Fake social proof | Unverifiable reviews, "12 people viewing" not tied to data. |
| Nagging | Same prompt re-shown after the user already decided. |
| Disguised ads | Ads styled as content or navigation with no clear label. |
| Comparison prevention | Plans or unit prices cannot be compared side by side. |
| Addictive design | Infinite feeds, streaks, variable rewards with no stopping cues, especially for minors. |
| Currency confusion | Virtual-currency prices with no real-money equivalent. |

Test: give 5 users the flow and ask "what did you agree to and what will it cost?"; any wrong answer is a finding.

## EU law

| Rule | What it requires (design consequence) | Source |
|---|---|---|
| DSA Art. 25(1) | Online platforms must not design, organise or operate interfaces that deceive or manipulate users or materially distort or impair free, informed decisions. Art. 25(3) names: giving more prominence to certain choices; repeated requests after a choice is made (esp. interfering pop-ups); making termination harder than subscribing. Art. 25(2): not applied to practices already covered by UCPD or GDPR. | [Reg. (EU) 2022/2065](https://eur-lex.europa.eu/eli/reg/2022/2065/oj) |
| UCPD 2005/29/EC Art. 6-7 | Misleading actions (false or deceptive overall presentation) and misleading omissions of material information are unfair. | [Dir. 2005/29/EC](https://eur-lex.europa.eu/eli/dir/2005/29/oj) |
| UCPD Annex I (always unfair) | Item 6 bait and switch; 7 false "very limited time" claims; 11 paid editorial content not disclosed (advertorial); 20 calling a product "free" when the consumer pays beyond unavoidable cost; 26 persistent unwanted solicitations; 29 demanding payment for unsolicited products. Numbering from the original text; later amended. | same |
| UCPD Annex I 23b/23c (added by Dir. (EU) 2019/2161, applies from 28 May 2022) | Claiming reviews come from real purchasers without reasonable checks; commissioning or submitting fake reviews. | [Dir. 2019/2161](https://eur-lex.europa.eu/eli/dir/2019/2161/oj) |
| GDPR Art. 7(3) | Consent can be withdrawn at any time; "It shall be as easy to withdraw as to give consent." Check: if accept is one click, reject/withdraw is one click with equal prominence. | [Reg. (EU) 2016/679](https://eur-lex.europa.eu/eli/reg/2016/679/oj) |
| EDPB Guidelines 03/2022 (v2.0, 24 Feb 2023) | Scope: social media platform interfaces. Names six categories: overloading, skipping, stirring, obstructing, fickle, left in the dark. States consent obtained by one click but withdrawn through more steps or time is not valid. Apply by analogy to other consent UIs, not as binding text. | [EDPB](https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-032022-deceptive-design-patterns-social-media_en) |
| Dir. (EU) 2023/2673, new Art. 11a of Dir. 2011/83/EU | For distance contracts concluded through an online interface, trader must offer a withdrawal function labelled "withdraw from contract here" (or unambiguous equivalent), continuously available during the withdrawal period, prominent and easy to access. Member States apply the measures from 19 June 2026 (transposition due 19 Dec 2025). Note: this is the statutory right of withdrawal, not subscription termination, and the directive's title concerns financial-services contracts; check the national law for scope. | [Dir. 2023/2673](https://eur-lex.europa.eu/eli/dir/2023/2673/oj) |

Check for cancellation symmetry: the path to end a contract uses the same channel, a similar number of steps and similar prominence as the path to start it (Art. 25(3)(c) DSA as the explicit example).

## Pending EU change

Digital Fairness Act: the Commission adopted its proposal on 11 Nov 2026. It is a proposal, not law; it targets dark patterns, easier online cancellation, reminders before free trials convert, and conscious choice for auto-renewal. Press reports say it would replace the UCPD (unverified: not read from the Commission text). Do not cite it as binding. [Euronews report](https://www.euronews.com/2026/11/11/eu-targets-subscription-traps-addictive-design-and-hidden-fees-with-new-digital-rules)

## US state

- FTC "click-to-cancel" amendments to the Negative Option Rule were vacated by the Eighth Circuit on 8 July 2025 (*Custom Communications v. FTC*, 142 F.4th 1060) for skipping a required preliminary regulatory analysis; the pre-2024 rule was restored by a final rule of 12 Feb 2026. FTC issued an ANPRM on 13 Mar 2026 (91 FR 12318; comments closed 13 Apr 2026). No replacement rule is in force. [FTC Negative Option Rule](https://www.ftc.gov/legal-library/browse/rules/negative-option-rule), [Federal Register ANPRM](https://www.federalregister.gov/documents/2026/03/13/2026-04952/rule-concerning-the-use-of-prenotification-negative-option-plans)
- ROSCA remains the federal tool for online negative-option sales; the ANPRM calls it the only federal law primarily designed for this, limited to internet transactions. State auto-renewal laws exist (the "about 30 states" figure is from law-firm summaries; unverified). Same FTC sources.
- Practical rule: design cancellation as symmetric anyway; US and EU direction of travel is the same.
