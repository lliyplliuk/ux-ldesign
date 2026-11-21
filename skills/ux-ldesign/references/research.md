# UX research: methods, tests, metrics

Use when: choosing a method, planning or reading a usability test, or reporting numbers. Severity scale and heuristic review live in [workflow.md](workflow.md); do not duplicate them here. Run problems found through that scale.

## Choosing a method
Source: [NN/g, When to Use Which UX Research Method](https://www.nngroup.com/articles/which-ux-research-methods/).
| Question to answer | Rule | Check |
|---|---|---|
| What people say or what they do? | Attitudinal methods report stated beliefs, limited by what people know and will say; behavioural methods observe use. Usability studies should lean behavioural. | Findings state which kind of evidence supports them. |
| Why or how many? | Qualitative gives insight from direct observation; quantitative uses predetermined data (task time, success, clicks) for numbers. | The method fits the question, not the team's habit. |
| Which phase? | Early: pick the direction (discovery). Design phase: formative methods that inform improvements. After build: summative methods compare against earlier versions or competitors. | Plan names the decision the study will inform. |
| One method enough? | Nearly all projects benefit from several methods combined. | At least two evidence sources for a major decision. |
| Information architecture? | Card sorting reveals users' mental model; tree tests measure findability without interface influence ([NN/g](https://www.nngroup.com/articles/ab-testing-and-ux-research/)). | Labels validated before visual design. |

## Usability test planning
| Rule | Check | Source |
|---|---|---|
| Qualitative round: about 5 users per round finds roughly 85% of problems when a single user finds about 31% (typical L); run several small rounds and fix between them instead of one big study. | Plan 3 rounds of 5 rather than 1 of 15. | [NN/g 5 users](https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/) |
| The 5-user rule holds for comparable users. With 2 distinct groups test 3-4 per group; with 3 or more groups test 3 per group. | Recruit per segment. | same |
| Caveat: statistics need more. Quantitative studies need at least 20 users for significant numbers, more for tight confidence intervals; questionnaires such as SUS typically 20-30. | Do not report percentages from 5 people as population values. | [NN/g How many test users](https://www.nngroup.com/articles/how-many-test-users/), [NN/g SUS](https://www.nngroup.com/articles/measuring-perceived-usability/) |
| Representative participants and representative tasks; define the user goals first. | Screener matches real users. | [NN/g task scenarios](https://www.nngroup.com/articles/task-scenarios-usability-testing/) |

## Task wording (no leading)
Source: [NN/g, Turn User Goals into Task Scenarios](https://www.nngroup.com/articles/task-scenarios-usability-testing/).
- Write a realistic scenario with context and a reason, not a bare command or a feature to hunt for. Poor: "Purchase a pair of orange Nike running shoes." Better: "Buy a pair of shoes for less than $40."
- Ask people to do the action, not to describe it. Poor: "Tell me where you would click." Better: "Look up the results of your midterm exams."
- Do not give steps or use words that appear in the interface (labels, button names): that hides whether the label works. Give specifics that make the task concrete (date, doctor's name).
- Check: pilot every task on a colleague; strike any word that appears on screen.

## Think-aloud
Source: [NN/g, Thinking Aloud](https://www.nngroup.com/articles/thinking-aloud-the-1-usability-tool/).
- Give representative tasks, ask participants to verbalise continuously, and mostly stay quiet; prompt only to keep them talking.
- Weaknesses: unnatural monologue, filtered statements, and facilitator prompts that can bias behaviour; it does not give detailed statistics.
- Check: recordings show participants speaking while acting and facilitator talk below participant talk.

## Metrics
| Metric | Rule | Source |
|---|---|---|
| Task success | Share of users who complete the task at all; also the basic measure of usability along with satisfaction. | [NN/g Usability Metrics](https://www.nngroup.com/articles/usability-metrics/) |
| Time on task, errors | Performance measures on the same task set; define the task set before testing, count backtracking or off-path steps if needed. | same |
| SUS | Ten Likert items. Odd items score (position minus 1), even items (5 minus position); sum, multiply by 2.5, giving 0-100. It is not a percentage; a commonly cited average is 68. Keep item wording and order unchanged. | [Brooke 1996 PDF](https://hell.meiert.org/core/pdf/sus.pdf), [NN/g SUS](https://www.nngroup.com/articles/measuring-perceived-usability/) |
| Reporting | State sample size, task set and method beside every number. | n/a |

## A/B tests
Source: [NN/g, Define Stronger A/B Test Variations Through UX Research](https://www.nngroup.com/articles/ab-testing-and-ux-research/).
- A/B shows which tested variation wins on micro and macro conversion metrics; it does not explain why, and variations built on guesses only find the best of the guesses.
- Use research first to find causes: intent and objections (on-site surveys), interface flaws (usability tests), findability (tree tests), then clean up variations before going live.
- Narrow the hypotheses with research instead of testing every idea (brute force exposes users to poor variations); write the cause theory, hypothesis and metric down before launch.
- Sample size, duration and significance thresholds are not covered by the NN/g source. Convention, not a universal rule: plan sample size from power analysis, and run at least one full week to capture the weekly cycle, longer if novelty or primacy effects are suspected ([Kohavi and Longbotham, Online Controlled Experiments and A/B Tests](https://exp-platform.com/Documents/2023-03-11EncyclopeiaMLDSABTestingFinal.pdf)). Set the exact thresholds with the owner or a statistician.
