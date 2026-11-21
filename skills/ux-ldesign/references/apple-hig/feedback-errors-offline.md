# Loading, feedback, errors, undo

Use when: designing async states, failures, confirmations and reversibility on Apple platforms. Sources: [Loading](https://developer.apple.com/design/human-interface-guidelines/loading), [Feedback](https://developer.apple.com/design/human-interface-guidelines/feedback), [Undo and redo](https://developer.apple.com/design/human-interface-guidelines/undo-and-redo), [Progress indicators](https://developer.apple.com/design/human-interface-guidelines/progress-indicators). Response-time limits (0.1 s, 1 s, 10 s): [../workflow.md](../workflow.md). The HIG has no dedicated offline page; offline states follow these rules.

| Rule | Check |
|---|---|
| Show something as soon as possible; let people do other things while content loads. | Throttle the network; the first screen shows structure quickly. |
| Say that content is loading and, when known, how long it will take; give something interesting to view if the wait is unavoidably long. | Wait states have an indicator. |
| Download large assets in the background to shorten install and launch. | Not blocking first use. |
| Match the weight of feedback to the importance of the event; make all feedback accessible. | Small action, modest response; major action, clear confirmation. |
| Integrate status into the interface rather than using alerts; use alerts for critical, ideally actionable information. | Alert only for what truly interrupts. |
| Warn before actions that cause unexpected, irreversible data loss; confirm completion of significant tasks. | Delete flow shows what is lost. |
| When a command cannot run, say so and explain why. | Disabled actions give a reason on tap. |
| Provide undo and redo that people can repeat, with a short precise description of the operation, and show the result; do not redefine standard undo gestures. | Shake/undo behaves as expected; label names the action. |
| Offer to revert several changes at once where useful. | Multi-step revert exists for editors. |

Pair with the NN/g heuristic on error recovery in [../workflow.md](../workflow.md) and the severity scale there. Android: [../mobile-android.md](../mobile-android.md).
