# Intake and JTBD

## Identify the Decision the User Wants to Make

| Input | First action | What can be skipped |
|---|---|---|
| Rough idea | Draft a job hypothesis as “who wants what outcome in which situation,” and identify assumptions that may constrain the idea | Do not lock in a technology stack yet |
| Clear requirements | Extract success conditions, hard constraints, and priorities | Repeating open-ended brainstorming |
| Known repository | Review its purpose, main capabilities, license, and limits; then compare alternatives or complements | An unrelated industry survey |
| Focused question | Define the target capability and necessary interfaces or environment | Full product planning |

Separate facts the user has confirmed, assumptions that are safe to use temporarily, and assumptions that need testing. Offer a draft product breakdown for discussion instead of asking the user to fill out a form from scratch. If missing information about the platform, offline or privacy needs, knowledge-base storage, license usage, or target users would change the capability breakdown and candidate set, explain which decision depends on the answer and ask one or two critical questions. Wait for the answer before doing search that depends on it; continue any independent research. If the information would only change candidate ranking, state an assumption and proceed.

Use a short **outcome contract** to guide the breakdown: What does the user give the tool? When and how often do they use it? What should they get back? How will they tell whether it helped? Which actions require human confirmation? This distinguishes “use an existing application” from “build a new capability” better than a technical module list. For personal tools, also ask whether the user is willing to maintain servers, models, and platform adapters. If unknown, treat this as a condition rather than assuming the user accepts the burden.

Keep multiple reasonable interpretations of ambiguous terms when they would change search. For example, “find duplicate routes” could mean match routes the user has already defined or discover shared routes that have never been defined; “local” could mean data stays on the user's device or that the software works entirely offline. If the user has not answered, search both interpretations and label the existing capabilities and additional work for each. Do not let a stricter interpretation hide a complete product that supports the more common workflow.

A JTBD is not the feature list the user first proposed. Consider whether an existing product with minor adaptation, a built-in platform feature, or a simpler interaction can get the job done sooner. List one to three routes only when the differences change the search direction; do not invent branches to meet a quota.

Before searching, check that the desired outcome is clear, core and optional capabilities are separated, an existing product or source-native feature could shorten the route, and no unresolved answer would change the search. If these are clear enough, write a short search brief and continue without asking the user to approve the formality. Stop at this stage if the user wants to discuss the product first or explicitly defers search.

Example: If the user wants to build a digital business card, first clarify whether the job is to present identity, exchange contact information, or manage follow-up relationships. QR codes, NFC, and vCards are possible approaches, not predetermined modules.
