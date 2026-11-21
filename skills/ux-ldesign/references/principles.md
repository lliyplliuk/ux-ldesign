# Interaction design principles as checklists

Use when: a heuristic review needs a second lens beyond Nielsen's ten ([workflow.md](workflow.md)) and the UX laws ([laws.md](laws.md)), or to name why a screen feels wrong. Each line is a question to answer yes/no with evidence from the screen. The lists overlap on purpose: report a problem once, under the clearest principle.

## Shneiderman's Eight Golden Rules
Source: [Ben Shneiderman, The Eight Golden Rules (UMD)](https://www.cs.umd.edu/users/ben/goldenrules.html); the page says they need validation for specific domains.
| # | Rule | Question |
|---|---|---|
| 1 | Strive for consistency | Are action sequences, terminology, colour, layout and capitalisation the same in similar situations, with few and understandable exceptions? |
| 2 | Seek universal usability | Do novices get explanations and experts get shortcuts and faster pacing; are disabilities, age and language variations covered? |
| 3 | Offer informative feedback | Does every action produce a response, modest for frequent minor actions and substantial for rare major ones? |
| 4 | Design dialogs to yield closure | Do multi-step sequences have a clear beginning, middle and end with completion feedback? |
| 5 | Prevent errors | Is the serious error made impossible where feasible, and otherwise is recovery guidance simple, constructive and specific without retyping everything? |
| 6 | Permit easy reversal of actions | Can single actions, data-entry tasks and groups of actions be undone? |
| 7 | Keep users in control | Does the interface avoid surprises, tedious entry and changes to familiar behaviour? |
| 8 | Reduce short-term memory load | Does the user ever have to remember something from one screen to use on another? |

## Tognazzini's First Principles (condensed)
Source: [Bruce Tognazzini, First Principles of Interaction Design](https://asktog.com/atc/principles-of-interaction-design/).
| Principle | Question |
|---|---|
| Anticipation | Is every tool or piece of information needed for the next step already on screen? |
| Autonomy | Does the user keep control of their environment and decisions, within responsible limits? |
| Colour | Is information conveyed by colour also given a secondary cue, and is colour-blind perception tested? |
| Consistency | Is the interface consistent with platform standards, in-house patterns and user expectations? |
| Defaults | Are defaults intelligent and easy to replace? |
| Discoverability | Are necessary controls visibly accessible at all times, not hidden for elegance? Test it. |
| Efficiency | Does it save the user's time, not the computer's? |
| Explorable interfaces | Is there always a way out, undo, and stable landmarks for orientation? |
| Fitts's law | Are frequent targets large and near the pointer or thumb? |
| Latency | Is waiting minimised, hidden by background work, and explained when it occurs? |
| Protect users' work | Is work never lost, state tracked, and storage and protection of information stated? |
| Readability | Is text high contrast, large enough, and tested with the oldest expected users? |
| Visible navigation | Is navigation visible, with few screen counts achieved via overlays? |

## Norman's design concepts
Sources: [Wikipedia, The Design of Everyday Things](https://en.wikipedia.org/wiki/The_Design_of_Everyday_Things) (secondary; the book was not fetched), [IxDF: Signifiers](https://www.interaction-design.org/literature/topics/signifiers), [NN/g: The Two UX Gulfs](https://www.nngroup.com/articles/two-ux-gulfs-evaluation-execution/).
| Concept | Question |
|---|---|
| Affordance | Does the object's apparent action possibility match what it does for this user? |
| Signifier | Is there a perceptible cue showing where and how to act (marks, labels, sounds)? |
| Mapping | Is the relation between controls and effects, and between system state and what is visible, evident? |
| Feedback | Does the user receive full, continuous feedback about results of actions? |
| Constraints | Does the design limit invalid actions rather than only report them? (unverified: constraints not on the fetched pages) |
| Conceptual model | Does the system image give a coherent, consistent model that bridges the gulf of execution (how do I do it?) and the gulf of evaluation (what state is it in?)? |

## ISO 9241-110:2020 interaction principles
iso.org returned 403; the seven names come from the secondary source [Wikipedia, ISO 9241](https://en.wikipedia.org/wiki/ISO_9241). Questions are derived from the names, not from the standard's text (unverified wording): read the standard before citing clauses.
| Principle | Question |
|---|---|
| Suitability for the user's tasks | Does the interface support the task the user is actually doing, without extra steps? |
| Self-descriptiveness | Is it clear at every step what the user can do and what state they are in? |
| Conformity with user expectations | Does it behave as users expect from context, convention and earlier use? |
| Learnability | Can new users learn it quickly with support in the interface? |
| Controllability | Can the user steer pace, sequence and settings (this includes the former individualisation principle)? |
| Use error robustness | Can the user reach the goal despite mistakes, with little or no correction effort? |
| User engagement (new in 2020) | Does the interface motivate sustained, pleasant use where that matters? |
