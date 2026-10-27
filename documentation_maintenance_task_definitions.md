# Documentation Maintenance Task Categories and Their Definitions

## Scope and coding principle

This document defines the 11 primary documentation maintenance tasks used in the paper-oriented classification of the 212 selected GitHub Agentic Workflows. A maintenance task identifies **what a workflow is principally designed to do to, for, or about documentation**. It does not identify the documentation genre being targeted or the GitHub output channel used by the workflow.

Each workflow receives one primary maintenance task. A secondary task may be recorded only when the workflow text explicitly describes an additional, independent maintenance activity. For example, a workflow can validate documentation and then repair it; its primary task reflects the principal end goal, while validation can be retained as a secondary step.

The task taxonomy is an operational classification designed for this workflow corpus. It is informed by documentation-maintenance problems in *Software Documentation Issues Unveiled*, but it does not claim that the eleven task labels are taken directly from that study.

## Categories at a glance

| ID | Maintenance Task | Definition | Workflow count |
| --- | --- | --- | ---: |
| M1 | Release Documentation Generation and Maintenance | Workflows that generate, aggregate, update, or maintain release-oriented documentation, including release notes, changelogs, changesets, release highlights, release blogs, compatibility notices, and version-support information. | 36 |
| M2 | Drift Detection and Synchronization | Workflows that compare documentation with source code, APIs, configuration, commits, releases, upstream sources, or other authoritative information, and synchronize documentation when inconsistencies or staleness are identified. | 55 |
| M3 | Documentation Impact and Gap Assessment | Workflows that analyze code changes, pull requests, interfaces, releases, or user-facing changes to determine whether documentation is missing, insufficient, or needs to be updated. | 13 |
| M4 | Correctness, Clarity, and Quality Review | Workflows that perform semantic, editorial, or expert-style reviews of documentation to identify factual inaccuracies, ambiguity, poor clarity, weak usability, incomplete explanations, or general quality concerns. | 34 |
| M5 | Link, Format, Example, and Site Validation | Workflows that execute rule-based or automated checks on documentation artifacts, such as link checking, Markdown linting, spelling checks, code or configuration example validation, schema validation, documentation-site testing, and accessibility checks. | 19 |
| M6 | Documentation Creation and Content Authoring | Workflows that create new documentation artifacts or produce substantial new documentation content, such as technical pages, API descriptions, drafts, guides, reports, or documentation-site content. | 14 |
| M7 | Refactoring, Simplification, Organization, and Deduplication | Workflows that improve documentation structure without primarily adding new subject matter, including reorganizing content, consolidating overlapping documents, removing duplication, simplifying text, and maintaining a coherent information structure. | 9 |
| M8 | Translation and Localization | Workflows that translate documentation into another language, synchronize translations with source-language content, identify outdated translations, or improve localized documentation while preserving its technical meaning. | 3 |
| M9 | Knowledge-Base, Catalog, Index, and Glossary Maintenance | Workflows that curate, update, organize, or expand documentation collections such as wikis, knowledge bases, resource catalogs, indexes, directories, glossaries, FAQs, and community knowledge artifacts. | 20 |
| M10 | Diagram, Screenshot, and Visual Material Generation | Workflows that generate or update visual documentation artifacts, including architecture diagrams, state-machine diagrams, screenshots, visual explanations, and other graphics used to support documentation. | 4 |
| M11 | Process, Strategy, and Policy Alignment | Workflows that maintain, assess, or align documentation about project processes, engineering practices, governance policies, strategic decisions, team procedures, or organizational rules with actual project activity. | 5 |

The category counts sum to 212 workflows.

## M1. Release Documentation Generation and Maintenance
  
**name:** Release Documentation Generation and Maintenance  
**Count:** 36

This task covers workflows whose main goal is to create, aggregate, update, or maintain documentation associated with a release, milestone, version range, or software evolution event.

Typical targets include release notes, changelogs, changesets, release highlights, release-blog drafts, milestone changelogs, deprecation notices, compatibility notices, support-policy pages, and upgrade information.

Typical actions include extracting notable changes from commits or pull requests, generating release-note drafts, updating changelog entries, replacing release-note placeholders, maintaining support matrices, and preparing human-readable release communications.

Use M1 whenever release-oriented documentation is the central target, even if the workflow creates new content. Do not assign M6 merely because the workflow generates text. A workflow that runs as part of a release pipeline is not automatically M1; it must actually target release documentation.

## M2. Drift Detection and Synchronization
 
**name:** Drift Detection and Synchronization  
**Count:** 55

This task covers workflows that identify or resolve documentation drift: a mismatch between documentation and an authoritative source of current information.

Authoritative sources can include source code, runtime behavior, API definitions, configuration, schemas, commits, merged pull requests, tags, releases, upstream documentation, or another verified project artifact.

Typical actions include comparing documentation with recent code changes, detecting stale README or docs-site content, synchronizing API or CLI documentation with implementation, checking whether translations are current, and opening an Issue or pull request when a mismatch is found.

Use M2 when an existing document is being kept accurate and current relative to a source of truth. Use M3 instead when the main question is whether a change requires documentation at all, or which documentation is missing. Use M8 when cross-language translation or localization is the central purpose.

## M3. Documentation Impact and Gap Assessment
 
**name:** Documentation Impact and Gap Assessment  
**Count:** 13

This task covers workflows that assess whether software changes create a documentation obligation, or that identify missing, insufficient, or undocumented information.

Typical inputs include merged pull requests, public-interface changes, breaking changes, new features, releases, configuration changes, and user-facing behavior changes. Typical outputs include documentation-impact reports, Issues, pull-request comments, proposed documentation work, or a draft documentation pull request.

Examples include checking whether a merged PR needs documentation updates, detecting undocumented breaking changes, identifying documentation gaps in a CLI or public API, and filing a request for a documentation update.

Use M3 when the workflow's main goal is to decide whether documentation is needed or where coverage is missing. Use M2 when it is already known which document should be synchronized with a changed source. Use M4 when the workflow reviews the quality of an existing document rather than its coverage.

## M4. Correctness, Clarity, and Quality Review
 
**name:** Correctness, Clarity, and Quality Review  
**Count:** 34

This task covers semantic, editorial, or expert-style reviews of documentation. The purpose is to identify quality concerns that often require contextual judgment rather than a purely deterministic test.

Typical review dimensions include factual accuracy, consistency with intended behavior, clarity, conciseness, terminology, completeness, organization, usefulness, user experience, and appropriateness for a particular audience such as a new contributor, technical writer, or agent user.

Typical actions include reviewing a documentation pull request, evaluating a guide from a novice user's perspective, identifying vague or inaccurate explanations, assessing prompt or skill quality, and posting editorial findings in an Issue or comment.

Use M4 when the core work is a semantic or editorial quality judgment. Use M5 when the workflow performs a concrete rule-based check, such as verifying HTTP links, linting Markdown, validating an example against a schema, or testing a documentation site.

## M5. Link, Format, Example, and Site Validation
 
**name:** Link, Format, Example, and Site Validation  
**Count:** 19

This task covers automated, rule-based, or executable validation of documentation artifacts. The defining feature is that the workflow tests a property that can be checked against an explicit rule, tool, build, schema, endpoint, or runtime behavior.

Typical checked objects include external and relative links, Markdown structure, spelling, grammar, code snippets, YAML or JSON examples, schemas, command examples, static-site builds, assets, search, sitemaps, mobile responsiveness, accessibility, and HTTPS behavior.

Typical actions include running a link checker, linting Markdown, validating code or configuration examples, checking live documentation pages, testing a Docusaurus or GitHub Pages site, creating Issues for violations, or applying straightforward fixes to broken links.

Use M5 even when the workflow can repair a detected violation, provided that validation is its central design purpose. Use M4 for open-ended quality reviews and M2 for source-to-documentation synchronization rather than rule-based validation.

## M6. Documentation Creation and Content Authoring

**name:** Documentation Creation and Content Authoring  
**Count:** 14

This task covers workflows whose primary output is new documentation or substantial new documentation content, rather than a diagnosis of an existing issue or a synchronization of an established document.

Typical outputs include new technical pages, documentation-site content, API descriptions, package documentation, guides, reports, drafts, Markdown files, and generated explanatory material.

Typical actions include generating API documentation from code, creating Docusaurus pages, drafting technical documentation from a specified topic, creating new documentation sections, and organizing source information into a first version of a document.

Use M6 when content creation is the workflow's dominant goal. Use M1 when the new content is principally a release note or changelog. Use M2 when content is produced primarily to repair known drift. Use M7 when the principal outcome is restructuring existing content rather than adding substantive information.

## M7. Refactoring, Simplification, Organization, and Deduplication
  
**name:** Refactoring, Simplification, Organization, and Deduplication  
**Count:** 9

This task covers workflows that improve documentation maintainability, structure, conciseness, and information organization without primarily introducing new subject matter or synchronizing documentation to an external change.

Typical actions include consolidating overlapping pages, detecting duplicate instructions or resources, removing redundant material, shortening overly verbose text, reorganizing sections, improving information architecture, normalizing titles, and reducing context bloat in instruction files.

Typical problems include duplicate content, overly long files, weak information organization, near-duplicate headings, and documentation that is unnecessarily difficult to maintain.

Use M7 when restructuring, simplification, organization, or deduplication is the main purpose. Use M4 when the workflow primarily identifies a quality problem but does not focus on structural improvement. Use M9 when the primary target is ongoing curation of a knowledge base, catalog, index, or glossary.

## M8. Translation and Localization
 
**name:** Translation and Localization  
**Count:** 3

This task covers workflows whose principal purpose is language conversion or adaptation of documentation for a target locale. It includes creating translations, synchronizing a translation with updated source-language content, identifying stale translations, and polishing translated documentation.

Typical actions include translating documentation files, filing translation content for review, comparing translated pages with their source-language counterparts, and correcting terminology or technical meaning in localized material.

Use M8 when cross-language transformation is central to the workflow. A general documentation synchronizer that incidentally handles translated content should remain M2 unless translation itself is its primary stated goal.

## M9. Knowledge-Base, Catalog, Index, and Glossary Maintenance
 
**name:** Knowledge-Base, Catalog, Index, and Glossary Maintenance  
**Count:** 20

This task covers the curation and sustained maintenance of documentation collections and navigational knowledge artifacts. Its focus is not only a single page, but also the completeness, organization, and discoverability of a body of shared knowledge.

Typical targets include wikis, knowledge bases, FAQ collections, glossaries, documentation indexes, resource directories, catalogs, curated lists, community bundles, extension collections, contributor-attribution pages, and searchable knowledge repositories.

Typical actions include updating a glossary from code changes, maintaining Wiki pages, accepting resource submissions, adding catalog entries, curating community knowledge, maintaining documentation indexes, and proposing updates based on recent issues or pull requests.

Use M9 when maintaining a knowledge collection, catalog, index, glossary, or community documentation resource is the primary objective. Use M7 for structural refactoring or deduplication of content. Use M3 for identifying missing documentation rather than maintaining the knowledge asset itself.

## M10. Diagram, Screenshot, and Visual Material Generation

**name:** Diagram, Screenshot, and Visual Material Generation  
**Count:** 4

This task covers workflows whose principal documentation output is visual rather than prose. The workflow creates, updates, or maintains diagrams, screenshots, or other graphics that explain software structure, behavior, or use.

Typical outputs include architecture diagrams, state-machine diagrams, Mermaid diagrams, UML diagrams, dependency visualizations, interface screenshots, and visual explanatory material embedded in documentation.

Typical actions include deriving a state machine from workflow files, generating an architecture diagram from repository changes, producing screenshots for a documentation page, and refreshing visual material after a design change.

Use M10 when visual material is the workflow's main documentation contribution. Use M6 when the main output is textual documentation and visual content is only supplementary. Use M6 or M2 when a diagram is merely an incidental by-product rather than the primary maintained artifact.

## M11. Process, Strategy, and Policy Alignment
 
**name:** Process, Strategy, and Policy Alignment  
**Count:** 5

This task covers workflows that maintain, assess, or align documentation about project processes, engineering practices, governance policies, strategic decisions, team procedures, or organizational rules with actual project activity.

Typical targets include team working-agreement documents, strategy documents, governance policies, review procedures, project decision records, workflow contracts, engineering standards, process documentation, and policy-related rules.

Typical actions include comparing meeting records or Issue discussions with stated strategy, identifying process drift, generating a team retrospective, updating a "how we work" document, checking compliance with engineering rules, and annotating strategy documents with alignment evidence.

Use M11 when process, policy, governance, or strategy alignment is the central goal. Use M2 when the workflow primarily aligns technical documentation with code, APIs, or releases. Use M4 for a general quality review that does not principally concern process or governance.

## Key decision boundaries

| Potentially overlapping tasks | Decision rule |
| --- | --- |
| M2 Drift Detection and Synchronization vs. M3 Documentation Impact and Gap Assessment | M2 updates or checks an existing document against an authoritative source; M3 decides whether documentation is needed and where documentation coverage is missing. |
| M3 Documentation Impact and Gap Assessment vs. M4 Quality Review | M3 concerns missing coverage or documentation obligations; M4 concerns the quality of documentation that already exists. |
| M4 Quality Review vs. M5 Validation | M4 requires semantic, editorial, or audience-sensitive judgment; M5 uses explicit, executable, or rule-based checks. |
| M5 Validation vs. M2 Drift Detection and Synchronization | M5 validates links, formatting, snippets, schemas, or site behavior; M2 compares documentation with a changing source of truth such as code, APIs, commits, or releases. |
| M6 Content Authoring vs. M1 Release Documentation | A new document is M1 when it principally records release or version evolution; otherwise, substantive new general documentation is M6. |
| M6 Content Authoring vs. M7 Refactoring | M6 introduces substantive content; M7 reorganizes, simplifies, or deduplicates existing content. |
| M7 Refactoring vs. M9 Knowledge-Base Maintenance | M7 improves structure and reduces redundancy; M9 curates a knowledge collection, index, catalog, glossary, or Wiki. |
| M8 Translation and Localization vs. M2 Drift Detection and Synchronization | Assign M8 when cross-language transformation is central; assign M2 when translation is only one incidental aspect of general synchronization. |
| M10 Visual Material Generation vs. M6 Content Authoring | M10 produces diagrams, screenshots, or other visual documentation as the main output; M6 principally produces text. |
| M11 Process, Strategy, and Policy Alignment vs. M2 Drift Detection and Synchronization | M11 aligns process, governance, policy, and strategy documents with organizational activity; M2 aligns technical documentation with technical sources of truth. |

## Recommended paper wording

> Each workflow was assigned one primary maintenance task according to its principal intended action. The maintenance task captures what the workflow is designed to do to, for, or about documentation, rather than the genre of the documentation being maintained or the GitHub channel through which the workflow delivers its result. Where a workflow explicitly performed an additional independent maintenance activity, this activity was recorded as a secondary task.

