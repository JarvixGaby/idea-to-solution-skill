# Search Strategy

## Search Brief and Environment Check

After product breakdown and convergence, inspect the GitHub repository search, file reading, code search, and web search tools actually available in the current session. Record missing tools and access limits. Treat a repository supplied by the user as a candidate and source of terminology, not as proof that the goal is solved.

## Search the User's Stars First

First check whether the current tools can **read-only** list repositories the user has starred. A connected GitHub account does not necessarily mean the connector can read Stars. If available, search that list for complete products, multi-capability projects, and key components, then verify them against the user's goal. Do not recommend based on Star recency or count. Stars indicate user interest or familiarity, not maturity. Skip this source if the user says not to use Stars.

If the user is not connected, lacks permission, or the tools cannot read Stars, briefly explain the specific state. Do not ask the user to paste a token or guess their private Stars from public information. If the user explicitly says “search only my Stars,” explain that the search cannot continue in that scope and ask whether to connect access or switch to public search. For other tasks, proceed with public GitHub search after noting the limitation; do not interrupt the research flow for optional personalization. If the Stars contain no relevant result, do not adequately cover the core goal, lack credible evidence, or lack useful alternatives, expand to public search. Distinguish “from your Stars” from “found in public search” in the report. Do not claim to have searched every Star unless the list was actually read in full.

The search brief should list the core outcomes to verify, target platform/deployment/license constraints, the possibility of a complete or multi-capability solution, known seed projects, and high-risk gaps. Each query group needs a clear purpose. Compared with a direct keyword search, add JTBD synonyms, cross-capability combinations, seed expansion, rechecks for negative findings, and source verification. Evaluate whether this improves results through same-prompt comparisons; more queries alone do not prove better search.

Turn the brief into a small coverage grid of “source/input → desired output,” such as “video link → timestamped transcript” or “web page → Markdown with images preserved.” One integrated repository may cover several cells, but a media downloader alone does not prove transcript or caption support. Prioritize core outcomes and high-risk gaps that could change the route; do not enumerate every possible platform combination mechanically. Keep two cells when ambiguity implies different outputs. Search them with shared broad terms first, then verify the differences.

## Query Design

For each query group, know which recall gap it is meant to address; there is no need to show the user the full query log. Search first for products that cover the whole JTBD and subsystems that cover several key outcomes, then target the uncovered capabilities. Do not mechanically issue one query for every capability in a table. The first round should include at least one **short product category or common project name**, such as `workout tracker`. Do not use only a dense intersection of feature terms like `GPX FIT heatmap segments`; it can miss complete products whose README describes the features but whose name is ordinary. Mix these angles as needed:

1. Job and whole-product terms: the user's goal, common product categories, and adjacent situations.
2. Synonyms and adjacent domains: different names, English terminology, user phrasing, and developer terminology.
3. Multi-capability combinations: products or subsystems that cover several core outcomes.
4. Gap capabilities: repositories, SDKs, or implementations only for needs still missing from whole-product and combined routes.
5. Alternative routes: platform features, official APIs, hosted services, and simpler workflows.
6. Seed expansion: topics, README terminology, dependencies, and alternative projects mentioned by promising repositories.

For an idea with platform-specific inputs, also search a **source-native capability** route, such as GitHub Releases, RSS, the system photo library, or browser clipping. If this is more direct than a general-purpose tool, include it in the route comparison. It may be an official API or built-in feature rather than a repository.

After screening whole products, select the **single outcome most likely to determine the product's success**, such as “ask questions inside Obsidian and jump to the cited PDF page,” rather than the broad “PDF management.” If the leading whole product has no direct evidence for that outcome, combine the user's current workflow or platform name with the outcome in a short query for a specialized app or plugin. Verify its actual scope and maturity. If repository search still returns only general projects or no direct evidence, cross-check once through a **different search entry point and result terms**, such as web search for `site:github.com Obsidian PDF exact page citations local plugin` or the platform's official plugin catalog for “PDF page / cited answers.” Send a directly matching niche project to evidence review even if it has few Stars; its absence from the top results of a general repository query does not prove it does not exist. If the cross-check finds no credible candidate, stop and report the search boundary instead of scanning every capability.

Use GitHub repository search to discover candidates. Code search is better for checking a specific interface or finding an implementation; a code snippet alone does not prove that a project is suitable. Use web search for terminology, platform constraints, and non-GitHub routes. If the current tool treats multiword queries as an overly strict intersection, returns only a few weak candidates, or returns nothing, immediately try short category terms or one concept and cross-check with web search or candidate READMEs. Do not keep adding restrictive terms. GitHub search syntax and connector parameters differ by tool; inspect the current tool's documentation and do not transfer one tool's qualifiers to another.

## Iteration Rules

- Start with whole-solution and adjacent-product searches. If the user asks about one focused capability, start there.
- Results are too broad: add a situation, target platform, input/output, or technical form, then exclude accidental matches during evaluation.
- Results are too narrow: remove premature language, Stars, or update-date filters; try synonyms or move up to the user-job level.
- Results are repetitive: look for different solution routes instead of collecting more similar repositories.
- A promising seed appears: check what it covers before searching for gaps.
- Several whole products or multi-capability projects appear: compare core coverage and reuse friction first, then decide which gaps warrant deeper searches. Do not break them into a homogeneous list of components.
- Before concluding that a capability needs custom development or ranking a whole product first, identify the kind of more complete or simpler project that could overturn the conclusion. Check one different short category term or source-native route; skip this check when evidence is already sufficient.
- A core outcome is only indirectly covered: run one focused search for the desired output, such as checking subtitles or official transcripts separately from media downloads. Compare specialist components with integrated projects on maintenance, license, and integration costs.
- A candidate seems ready to adopt: review recent README changes, releases, or key issues for counterevidence such as abandonment, broken upstream interfaces, or sign-in requirements. This evidence can change its recommendation level.

Do not set a default `stars >= 100`, a fixed five-to-ten query groups, or a fixed Top N. Stars, recent commits, and archived status are contextual signals; a small, precise repository may be more useful. Before stopping, review every core cell: a credible solution, a candidate that clearly needs validation, or a gap within the stated search scope. Do not let discovery of one cross-platform downloader skip transcript, article, and archiving routes for each source. Also check whether you searched a short whole-product category, considered source-native features, found direct evidence or a specialist candidate for the key outcome, and ruled out nearby alternatives that could overturn the preferred route. If successive queries only repeat candidates or produce weak matches, stop expanding and explain the coverage boundary.
