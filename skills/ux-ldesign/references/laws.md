# UX laws and effects

Use when: choosing a principle that explains a concrete interface problem, and checking where it stops applying.

The set covers the 30 concepts of [Laws of UX](https://lawsofux.com/). Names are given for lookup. The practical applications below are hypotheses to test on a specific interface.

## Orientation and understanding

| Principle | Application and check |
| --- | --- |
| Jakob's Law | Use navigation and control patterns familiar to the audience. Ask where the user expects the action, then test the first click. |
| Mental Model | Name entities and actions in users' words. Compare the expected filter behaviour with the actual one. |
| Cognitive Load | Show constraints and the next step next to the task. Count how many conditions a person must hold while filling the form. |
| Working Memory | Keep data needed for a decision visible across steps. Check whether people go back for an order number or comparison parameters. |
| Chunking | Group fields into meaningful blocks, e.g. contact and delivery. Check whether a person finds the needed field quickly. |
| Miller's Law | Reduce what must be remembered. "7 ± 2" comes from lab tasks and does not set a menu-item count. |
| Paradox of the Active User | Users start at once without reading. Put a short hint next to a new or risky action and test first launch. |
| Selective Attention | Put critical information at the object of the current task. Check whether the user notices a warning at the moment of choice. |

## Choice and action

| Principle | Application and check |
| --- | --- |
| Hick's (Hick-Hyman) Law | Group alternatives, make them easy to compare, add task-based filters. Measure choice time and errors together with the ability to find a rare option. |
| Choice Overload | Give meaningful differences between plans and a sensible default recommendation with transparent terms. Risk depends on task, knowledge and option set. |
| Fitts's Law | Enlarge the real hit area of frequent actions and check misses. Account for target size and distance. |
| Tesler's Law | Let the system fill known data or compute totals. Keep important consequences visible and editable. |
| Postel's Law | Accept unambiguous phone formats or spaces in a number. Do not silently "fix" ambiguous dates, amounts and addresses. |
| Occam's Razor | With equal explanatory power, start from the hypothesis with fewer assumptions. A simple-looking screen can still hide important information. |
| Pareto Principle | Start with scenarios that carry most of the damage or workload according to data. 80/20 is not guaranteed. Consider rare blocking problems. |
| Parkinson's Law | For a bounded task state its scope and completion criterion. Cut unnecessary work without artificial timers. |
| Cognitive Bias | Check whether order, preselection or price presentation leads to an unintended decision. Make terms and opt-outs clear. |

Studies of choice and pointing: [Hick](https://doi.org/10.1080/17470215208416600) · [Fitts](https://doi.org/10.1037/h0055392)

## Visual perception

| Principle | Application and check |
| --- | --- |
| Law of Proximity | Place a label next to its own field. Check the association after line wrap and on a narrow screen. |
| Law of Common Region | Separate independent groups with background or border when spacing alone is not enough. |
| Law of Similarity | Style elements with the same function consistently. Check that similar-looking elements do not wrongly promise the same action. |
| Law of Uniform Connectedness | Show real relationships with connectors or shared structure, e.g. in a route map. |
| Law of Prägnanz | Check that the composition reads unambiguously at a glance. Remove conflicting groupings and visual signals. |
| Von Restorff Effect | Highlight the action that is truly important in context. For status add meaningful text or a symbol so colour is not the only signal. |
| Aesthetic-Usability Effect | Account for how appearance affects impression. Check actual task completion separately from appearance ratings. |

## Time, progress and completion

| Principle | Application and check |
| --- | --- |
| Doherty Threshold | Respond to an action without a noticeable pause. For a long operation show feedback, progress where possible and cancel if supported. About 400 ms is a historical benchmark; test the threshold for your task on real devices. See the 0.1 / 1 / 10 s limits in [workflow.md](workflow.md). |
| Flow | For repetitive work make the next step predictable, keep context and avoid needless interruptions. For risky actions leave time to review. |
| Goal-Gradient Effect | Show an honest number of remaining steps when the scope is known. Check whether the person understands what is left to do. |
| Peak-End Rule | Pay attention to the hardest moment and to the ending. Confirm the result and the next step. Evaluate the whole path by observation. |
| Serial Position Effect | For sequential presentation check the visibility of the beginning and end. Order menus also by task, frequency and clarity of groups. |
| Zeigarnik Effect | Make unfinished work findable and resumable. Test the usefulness of reminders in context and leave control over them with the user. |

Feedback benchmarks: [Jakob Nielsen on response times](https://www.nngroup.com/articles/response-times-3-important-limits/)
