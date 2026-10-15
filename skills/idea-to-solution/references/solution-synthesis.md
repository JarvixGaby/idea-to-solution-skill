# Solution Synthesis

Compare coverage from complete products and multi-capability candidates first, then map resources and gaps against the capability list. Combine them into routes that accomplish the user's job rather than producing a simple ranking:

- Adopt or adapt a complete product that covers most of the goal.
- Combine one multi-capability project with a small number of supplementary components.
- Use a smaller library, official API, platform feature, or service.
- Change the workflow and accomplish the JTBD in a simpler way.

Make the capability map easy to scan: show which parts have mature GitHub repositories that can be adopted directly, which have only components that need integration or adaptation, and which may need development or further research. Cite a specific resource and evidence for each item. A multi-capability repository may appear on several rows or use a coverage marker. Do not force a repository into every row to claim full coverage.

Show only complete routes with real evidence and meaningful trade-offs. For each route, describe core coverage, remaining work, reuse approach, main dependencies, license and integration risks, and assumptions not yet verified. A repository covering several capabilities is valuable, but account for the cost of adapting it. Several repositories that appear to cover everything do not prove that the combination works.

State the product implication clearly. If an existing complete product can meet an acceptable first version, suggest trying or adapting it first. If one part is missing, identify the smallest supplement. If several projects must be combined, describe the integration points and ongoing maintenance. If an ambiguous term changes the result, give separate conclusions for reasonable and strict interpretations. Do not treat custom development as the default. Keep claims such as “fully automatic,” “fully offline,” or “production ready” unverified unless evidence supports them.

Do not force a final choice when the user only wants options. When evidence supports a recommendation and the user needs one, name the route worth investigating first and explain why. Candidates can be ranked if the criteria and conditions are clear. Make “what to validate next” as small and concrete as possible, such as checking whether an interface accepts the required input and returns the needed output. This is a recommendation for a later development workflow; the Skill does not perform it.

When no reliable candidate is found, report the search scope, near matches, and unknowns. Suggest changing terminology, using a non-repository approach, or estimating development of a specific gap in a later workflow. Say “no directly reusable resource found in this search; estimate custom development for now” only after enough research to support it. If access failed or no search was done, say “unknown.” Never fabricate projects to fill a table.
