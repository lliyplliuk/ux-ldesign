# Design, review and research

Use when: planning or reviewing a flow, rating findings, or choosing how to confirm a result.

## From task to interface

- Record where the user comes from, what they want, which data and constraints exist, and where the task ends. For a long path mark handoffs between screens, devices and people.
- Break information architecture into groups, labels, navigation and search. For grouping doubts use card sorting; for finding a section by task use a tree test without visual cues.
- Walk the main actions and relevant states: first launch, loading, no data, empty search, error, no permission, success, back, retry. For long operations clarify when cancel or resume is possible. Account for preserving entered data and the consequences of double submission.
- Support hierarchy with content and composition. Check that the main action is visible in context, interactive and static elements differ, and the interface survives a narrow screen, enlarged text, translation and real long values. Check ordinary keyboard and touch operation where relevant.
- In microcopy name the action and its result. An error message says what happened and how to fix it, appears next to the input where possible and keeps the entered value. An empty state explains what exactly is missing and the next step if one exists. [GOV.UK validation pattern](https://design-system.service.gov.uk/patterns/validation/)
- For purchase, subscription, permissions and personal data check visibility of price, terms and consequences. Compare how easy it is to accept, decline and cancel. See [ethics-dark-patterns.md](ethics-dark-patterns.md); [FTC workshop](https://www.ftc.gov/news-events/events/2021/04/bringing-dark-patterns-light-ftc-workshop).

## Response-time limits

Source: [NN/g, Response Times: The 3 Important Limits](https://www.nngroup.com/articles/response-times-3-important-limits/).

| Limit | Meaning | Check |
| --- | --- | --- |
| 0.1 s | Feels instantaneous; the user feels direct manipulation, no extra feedback needed. | Taps, toggles, typing respond within ~0.1 s. |
| 1 s | Flow of thought stays uninterrupted, but the delay is noticed; signal that the system is working. | Anything slower than ~1 s shows an indicator. |
| 10 s | Limit of keeping attention on the task. | Over ~10 s show percent-done progress and a way to interrupt; expect task switching. |

## Ten Nielsen heuristics

| Heuristic | What to check |
| --- | --- |
| 1. Visibility of System Status | After an action it is clear whether it was accepted, whether processing continues and how it ended. |
| 2. Match Between the System and the Real World | Names, order and formats match the user's language and process. |
| 3. User Control and Freedom | The user can go back, cancel or restore data where feasible. |
| 4. Consistency and Standards | Same names and components behave the same. Platform conventions are followed. |
| 5. Error Prevention | Validation and constraints prevent costly errors in time. Before an irreversible action the object and consequences are visible. |
| 6. Recognition Rather than Recall | Options, previous values and needed hints are available at the moment of action. |
| 7. Flexibility and Efficiency of Use | A clear main path for novices; frequent operations accelerated for experts. |
| 8. Aesthetic and Minimalist Design | Every element helps understand the task, act or navigate. |
| 9. Help Users Recognize, Diagnose, and Recover from Errors | The error is located, phrased plainly, states the cause and gives a real recovery path. |
| 10. Help and Documentation | Help is where it is needed and gives steps for the current task. |

Sources: [Nielsen's heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) · [Heuristic evaluation method](https://www.nngroup.com/articles/how-to-conduct-a-heuristic-evaluation/)

## Severity scale (NN/g 0-4)

Source: [NN/g, How to Rate the Severity of Usability Problems](https://www.nngroup.com/articles/how-to-rate-the-severity-of-usability-problems/).

| Rating | Label | Action |
| --- | --- | --- |
| 0 | Not a usability problem | No action. |
| 1 | Cosmetic problem only | Fix only if time is available. |
| 2 | Minor usability problem | Low priority. |
| 3 | Major usability problem | High priority. |
| 4 | Usability catastrophe | Must be fixed before release. |

Rate with three factors: frequency (how often), impact (how hard to overcome), persistence (one-time or repeatedly bothersome); market impact also counts. A single evaluator's ratings are unreliable: use the mean of about three independent raters when possible; otherwise label the rating as one reviewer's judgement. Rate against the full list of problems, not one at a time.

## Confirming the result

- Check first what affects the decision. Interviews give context and reasons, task walk-throughs show interaction difficulty, analytics estimates frequency when events and a suitable sample exist.
- For a task test set the start state and goal in plain words without naming the button. Record completion, errors, backtracking, need for help and, if needed, time. Describe conditions and segment. For before/after use the same success definitions and comparable conditions.
- In review rank higher the obstacles that make a key flow unavailable, lose data or lead to a decision with serious unintended consequences. Then assess friction, workarounds and frequency. If frequency is unknown say so and propose a check.
- With limited data write the exact observable fact, then the expected consequence and how to verify. In a screenshot report leave keyboard, live validation and real response time as items to check on a working interface.

## Example finding

**Severity 3 (major) · checkout.** On retrying payment after a network error the form clears the delivery address. The buyer re-enters data and may abandon checkout. Fix: keep the address and show whether the payment was confirmed before offering a retry. Check in a test environment through network drop, recovery and retry: address kept, first payment status clear, exactly one order created. Effect on abandonment is verified separately from funnel events.
