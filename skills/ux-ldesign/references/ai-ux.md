# AI and generative-AI interfaces

Use when: a product has predictions, recommendations, chat, agents or generated content. Sources: Microsoft HAX guidelines (Amershi et al., [CHI 2019](https://doi.org/10.1145/3290605.3300233); microsoft.com/haxtoolkit returned 403, so the paper's Table 1 was read from an archived copy of Microsoft's PDF), Google [People + AI Guidebook](https://pair.withgoogle.com/guidebook/) chapters, Apple [Generative AI](https://developer.apple.com/design/human-interface-guidelines/generative-ai).

## HAX 18 guidelines (CHI 2019, Table 1)
| Phase | Guideline | Check |
|---|---|---|
| Initially | G1 Make clear what the system can do | A new user can list capabilities without trial and error. |
| | G2 Make clear how well it can do it | Accuracy/limits stated near the feature. |
| During interaction | G3 Time services based on context | Suggestions appear when relevant, not constantly. |
| | G4 Show contextually relevant information | Output ties to the current task and environment. |
| | G5 Match relevant social norms | Tone and behaviour fit the context. |
| | G6 Mitigate social biases | Outputs reviewed for stereotyping across user groups. |
| When wrong | G7 Support efficient invocation | One step to request the AI feature. |
| | G8 Support efficient dismissal | One step to ignore or dismiss it. |
| | G9 Support efficient correction | Editing a wrong result is easy. |
| | G10 Scope services when in doubt | With low certainty, narrow, ask or defer. |
| | G11 Make clear why the system did what it did | Explanation available on demand. |
| Over time | G12 Remember recent interactions | Context carries across the session. |
| | G13 Learn from user behaviour | Personalisation visible and useful. |
| | G14 Update and adapt cautiously | Changes in behaviour do not surprise users. |
| | G15 Encourage granular feedback | Per-item feedback, not only global. |
| | G16 Convey the consequences of user actions | Users see how actions change future output. |
| | G17 Provide global controls | Settings to adjust or turn off AI behaviour. |
| | G18 Notify users about changes | Model or capability changes announced. |

## Topic checks (PAIR and Apple)
| Topic | Rule | Check | Source |
|---|---|---|---|
| Expectation setting | Explain the benefit, not the technology; introduce AI features in stages and only when needed; state limits clearly and avoid implying human-like abilities. | Onboarding copy names outcomes and limits. | [PAIR Mental models](https://pair.withgoogle.com/chapter/mental-models/), [Apple](https://developer.apple.com/design/human-interface-guidelines/generative-ai) |
| Labelling | Communicate where the app uses AI. | AI-generated content is identifiable. | [Apple](https://developer.apple.com/design/human-interface-guidelines/generative-ai) |
| Confidence | First decide whether showing confidence helps; if so pick a form (categorical, N-best alternatives, numeric, visualisation) the audience can use for decisions. | Users in a test act correctly on the display. | [PAIR Explainability + Trust](https://pair.withgoogle.com/chapter/explainability-trust/) |
| Uncertainty and hallucination | Raise awareness of and minimise hallucinations; scope the output when in doubt. | Known-wrong prompts are handled visibly. | [Apple](https://developer.apple.com/design/human-interface-guidelines/generative-ai), HAX G10 |
| Citations and sources | State what data sources an output uses so users know when to apply their own judgement. | Each factual output links to its source. | [PAIR Explainability + Trust](https://pair.withgoogle.com/chapter/explainability-trust/) |
| Correction and undo | Let people refine or revert generated results and acknowledge when their correction takes effect; get permission before irreversible or problematic actions. | Undo works for every AI action. | [Apple](https://developer.apple.com/design/human-interface-guidelines/generative-ai), HAX G9 |
| Latency and streaming | Under 0.1 s feels instant, 1 s keeps flow, 10 s is the attention limit: show progress for long generation, let people do other things. Streaming partial output is a way to meet this (inference, not a source claim). | Time to first visible output measured. | [NN/g Response Times](https://www.nngroup.com/articles/response-times-3-important-limits/) |
| Failure modes | Classify errors (system, user, context), weigh stakes, give paths forward: feedback options, return control to the user, assume subversive use. | Failed-request flow tested, not a dead end. | [PAIR Errors + Graceful Failure](https://pair.withgoogle.com/chapter/errors-failing/) |
| Blocked results | Help people improve requests when blocked or undesirable results occur. | Refusal message suggests a next step. | [Apple](https://developer.apple.com/design/human-interface-guidelines/generative-ai) |
| Feedback | Align feedback with model improvement; show how feedback changes the experience; allow opting out and editing. | Feedback control appears beside output. | [PAIR Feedback + Control](https://pair.withgoogle.com/chapter/feedback-controls/) |
| Consent for data use | Ask permission before using personal and usage data; disclose how the app and model use and store it; process locally where possible. | Consent and disclosure screens exist. | [Apple](https://developer.apple.com/design/human-interface-guidelines/generative-ai), [permissions-privacy](apple-hig/permissions-privacy.md) |
| Fallback | The experience works when AI features are unavailable or declined. | Turn AI off; core tasks still work. | [Apple](https://developer.apple.com/design/human-interface-guidelines/generative-ai) |

Legal duties for AI disclosure and consent: [ethics-dark-patterns.md](ethics-dark-patterns.md).
