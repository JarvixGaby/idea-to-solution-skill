# Broad Candidate-Pool Search

After the JTBD and product breakdown, use varied queries, a candidate pool, deduplication, classification, deeper review, and a search log to broaden discovery. Run this full process only when a broad candidate pool can improve the decision. Do not move a fixed Top N or repeated confirmation into the idea stage.

Use this mode only when the user explicitly requests extensive search or sets `search_breadth=extensive`. For ordinary `focused` or `broad` tasks, use the dynamic search strategy. Invoke this mode explicitly during testing. Do not fabricate queries, result counts, quotas, or candidate fields to satisfy a format.

## 1. Define the Search Target

Before searching, record the JTBD, input-to-outcome flow, ambiguities that could change selection, hard constraints, target form (complete application, multi-capability solution, component, API, or alternative workflow), exclusions, and research budget. Continue directly when the user asks to skip follow-up questions or the current information is sufficient. Ask only when missing information creates mutually exclusive directions that cannot be searched in parallel. Capability breakdown is a search aid, not a quota of one repository per capability.

## 2. Plan and Run 5–10 Purposeful Query Groups

State the recall goal for each query group. After running it, record the query terms, search entry point, and whether it helped. Combine different search angles rather than changing only one term:

1. **Short product category:** a common product name for the whole JTBD, avoiding an overly narrow intersection of feature terms.
2. **Synonyms and adjacent situations:** user phrasing, developer terminology, and naming in nearby industries.
3. **Situation and form:** personal/local/self-hosted, application/plugin/framework/SDK, and similar distinctions.
4. **Multi-capability intersection:** projects that may cover several key outcomes at once.
5. **Key outcome:** platform name plus a concrete output to find specialist projects.
6. **Source-native and alternative routes:** official APIs, built-in features, and simpler workflows.
7. **Seed expansion:** topics, README terms, and related projects from promising candidates.

A query group may cover several angles, but do not put every feature term into one query. The original process suggests reviewing 30–50 results per group when pagination and the research budget allow. If a tool exposes fewer results, truncates, or rate-limits, record the number actually visible; do not count unread results as candidates. Use a shorter query or another search entry point to improve recall. Do not repeat ineffective queries just to reach five groups.

## 3. Build an Auditable Candidate Pool

Deduplicate results by normalized `owner/repo`. Record the source query, URL, description, Stars, archive status, visibility, language, update date, topics, license, and first-pass type. Write “not available” for missing fields. A search snippet alone supports only “possibly relevant,” not a feature claim.

Use three layers instead of a single cutoff:

- **Basic exclusions:** clearly unrelated projects, empty shells, dead mirrors, archived projects that cannot be used, and projects that violate hard constraints. Keep the reason for each exclusion. An archived project with reference value may remain in a reference layer, but must not be presented as a currently adoptable complete product.
- **Conservative maturity pool:** public, non-archived candidates with verifiable signs of maintenance and use. You may separately record the subset with at least 100 Stars to observe the candidate distribution, but Star count is not an admission rule or proof of maturity.
- **Direct-fit exceptions:** candidates under 100 Stars, with unavailable Star data, or from the user's Stars remain eligible when they directly cover a key outcome. Keep investigating and flag maturity risks in the final result. The strict pool must not silently discard them.

When the user has authorized access to personal Stars, use them as a first candidate source and supplement them with public results. If the user skips Stars, search public sources directly. Do not claim to have searched Stars you could not access.

## 4. Reduce Noise, Classify, and Rerank

Remove accidental keyword matches, documentation lists mistaken for products, and projects whose licenses or deployment clearly do not fit. Classify candidates as complete applications, multi-capability subsystems, libraries/SDKs, platform APIs, directories/research materials, or alternative workflows. One project may cover multiple capabilities.

Rerank promising candidates for goal relevance, fit to the situation, maintenance activity, engineering maturity, and community signals. The first two factors matter most; Stars are only a weak signal. Give each factor a simple label such as “strong,” “medium,” “weak,” or “unknown” with one sentence of evidence, then compare. Do not make up decimal scores for missing data. A candidate that violates a core constraint must not rank first because of high Stars. For the same outcome, prefer a personal-use route with less remaining maintenance. Keep one candidate in a different form that could overturn the leading choice.

## 5. Read Deeply and Look for Counterevidence

For finalists and candidates that could overturn the first choice, at minimum verify the README's stated purpose, key features or quick start, and recent maintenance or release signals. Also check the license, deployment, external services, privacy, and interface requirements. A specific capability needs direct support from official documentation or relevant files. If the key outcome still lacks direct evidence, do one focused search for a specialist through another entry point. Distinguish README claims, code evidence, and actual runtime results. This Skill does not run candidates and must not claim a successful runtime test.

## 6. Deliver and Stop

Within the Idea/JTBD → breakdown → candidates → gaps → routes structure, add a compact **search audit**: query purposes, visible result counts when available, deduplicated count, conservative maturity pool, direct-fit exceptions, shortlist size, tool failures, and unsearched boundaries. For each candidate, say what it is, why it fits this idea, what it cannot do, and what the user would still need to maintain. Rank by the current goal; do not pad the list to reach a Top N.

Call this mode complete only when the queries were actually run, results entered the candidate pool, and shortlist evidence was checked. If rate limits, connector errors, or the user's budget interrupt the process, label it “candidate-pool process partially completed” and show completed steps and likely omissions. Stop early when later queries only repeat candidates or the key routes already have sufficient evidence, and explain that the suggested query or result volume was not reached. More searching is not success by itself.
