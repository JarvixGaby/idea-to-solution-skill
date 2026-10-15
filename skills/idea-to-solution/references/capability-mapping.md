# Capability Mapping

Work down from user-observable outcomes: `job goal → product workflow → core/optional capabilities → inputs, outputs, and dependencies → possible technical approaches`. Draft the capability list and open questions before search; after search, use the same list to map reusable resources and gaps. Use `decomposition_granularity` to control how far to break things down.

Start with the objects and actions the user actually encounters, such as “existing photo folder → find groups of similar images to review → process them safely,” rather than beginning with image vector databases, map services, and deduplication scripts. Define one observable acceptance example for each core outcome. Break down a lower-level capability only if doing so could change repository selection. Keep ambiguities such as “human-confirmed or automatic,” “runs on my device or fully offline,” and “use an existing folder or migrate to a new library” as alternatives for candidate comparison; do not default to the more difficult interpretation.

- `product`: the situation, primary outcome, and a few key capabilities.
- `capability`: capabilities, interfaces or dependencies, and core/optional/deferred status.
- `engineering`: platform, data format, runtime, and interface constraints only when they help select candidates; do not write implementation plans or code.

A resource may cover several capabilities, and one capability may be met by different resources, an official API, a service, or a workflow change. Before search, label capabilities as core or optional and distinguish user-confirmed needs from hypotheses. After search, classify coverage as “mature repository can be adopted directly,” “component can be integrated or adapted,” “candidate exists but evidence is insufficient,” or “currently appears to require custom development or another approach.” The last category describes this research result; it does not prove that no repository exists. If a complete solution is found, roll back lower-level breakdowns it makes irrelevant. If a new platform constraint appears, revisit the capability assumptions.

Consider source-native signals based on the input. For updates to GitHub projects, check Releases or APIs; for articles, consider RSS or browser clipping. Compare source-native features with general-purpose extractors when they can achieve the user's outcome. Do not overlook them just because they are not a new repository. The breakdown should ultimately answer “what does adopting the whole product save, and what would I still have to maintain?” rather than merely list feature names.

Prioritize constraints that determine the route, such as operating system, offline needs, data privacy, existing stack, and acceptable integration effort. Do not invent every engineering detail.
