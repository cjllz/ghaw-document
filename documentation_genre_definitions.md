# Documentation Genre Categories and Their Definitions

## Scope and coding principle

This document defines the 11 primary documentation genres used in the paper-oriented classification of the 212 selected GitHub Agentic Workflows. A documentation genre identifies **the principal documentation artifact or communicative purpose targeted by a workflow**. It does not identify the maintenance action (for example, generating, reviewing, validating, or repairing) or the GitHub channel used to deliver the result (for example, a pull request, issue, comment, or release).

Each workflow receives one primary genre. Specific genres take precedence over broad genres. The final category, *General or Multi-Type Technical Documentation*, is used conservatively only when a workflow targets documentation broadly, targets multiple genres without a dominant target, or lacks sufficient evidence for a more specific assignment.

The category set combines practitioner-oriented document genres from *Software Documentation: The Practitioners' Perspective*, repository-documentation concepts from *What's in a GitHub Repository? -- A Software Documentation Perspective*, and explicit extensions required by an agentic-workflow corpus.

## Categories at a glance

| ID | Documentation Type | Definition | Workflow count |
| --- | --- | --- | ---: |
| T1 | Project, Process, and Repository Metadata | Documentation describing a project's purpose, organization, repository structure, governance policies, development processes, collaboration practices, and associated project resources. | 17 |
| T2 | Introduction and Getting-Started Documentation | Documentation helping first-time users understand a project's purpose, core concepts, prerequisites, and basic setup, typically guiding them toward a minimal working example. | 1 |
| T3 | How-To Guides and Tutorials | Task-oriented or learning-oriented documentation that teaches users or developers how to accomplish specific goals through step-by-step instructions, examples, lessons, workshops, or exercises. | 24 |
| T4 | Deployment Guides | Documentation describing the prerequisites, environment configuration, security considerations, deployment procedures, operational steps, and troubleshooting information required to deploy software. | 1 |
| T5 | API Reference Documentation | Structured technical documentation specifying APIs, commands, parameters, configuration options, schemas, return values, constraints, examples, and other programmatic interfaces. | 8 |
| T6 | Architecture, Design, and Specification Documentation | Documentation describing system architecture, component relationships, technical requirements, design decisions, architectural rationale, schemas, blueprints, and formal technical specifications. | 13 |
| T7 | Release Notes and Changelogs | Documentation recording software releases and evolution, including new features, bug fixes, breaking changes, deprecations, compatibility updates, upgrade information, and other version-specific changes. | 36 |
| T8 | Frequently Asked Questions | Question-and-answer documentation addressing recurring questions commonly raised by users, developers, contributors, or other project stakeholders. | 1 |
| T9 | Community Knowledge | Documentation that captures and organizes knowledge contributed or accumulated through community interactions, including wikis, knowledge bases, glossaries, troubleshooting knowledge, discussions, issues, and contribution records. | 13 |
| T10 | Agent-Facing Instructions, Skills, and Prompts | Persistent documentation artifacts that provide AI coding agents with project-specific context, behavioral rules, tool-use guidance, reusable skills, task instructions, and prompts. | 14 |
| T11 | General or Multi-Type Technical Documentation | Documentation targeted by workflows that maintain technical documentation in general, an entire documentation site, or multiple documentation genres without identifying one dominant type. | 84 |

The category counts sum to 212 workflows.

## T1. Project, Process, and Repository Metadata
 
**name:** Project, Process, and Repository Metadata  
**Count:** 17

This genre covers documentation about how a project is organized, governed, maintained, and collaboratively operated. Its principal purpose is to explain project-level context rather than a software feature, API, release, or end-user task.

Typical artifacts include project strategy documents, team working agreements, contribution and review processes, governance policies, repository-structure descriptions, resource collections, project-level README material, planning documents, and policy or procedure documentation.

Include a workflow in this category when its main target concerns project organization, collaboration, strategy, repository operation, governance, or engineering practice. A README belongs here when it primarily presents repository-level information, project resources, or collaboration context.

Do not use this category for a README whose principal purpose is beginner onboarding; use T2 instead. Do not use it for agent instructions, which belong in T10, or for a wiki/knowledge-base artifact whose main purpose is community knowledge sharing, which belongs in T9.

## T2. Introduction and Getting-Started Documentation
 
**name:** Introduction and Getting-Started Documentation  
**Count:** 1

This genre covers entry-point documentation for first-time users or contributors. Its purpose is to explain what a project is, introduce its most important concepts, state minimal prerequisites, and help a reader reach a first successful use or minimal working example.

Typical artifacts include getting-started pages, quick-start guides, onboarding pages, beginner guides, first-run instructions, and minimal runnable examples.

Use this category only when the primary audience is new to the project and the document's main function is initial orientation and rapid setup. A detailed task guide belongs in T3; a repository overview focused on organization or resources belongs in T1.

## T3. How-To Guides and Tutorials
 
**name:** How-To Guides and Tutorials  
**Count:** 24

This genre covers instructional documentation that teaches a reader how to complete a task or learn a software capability. It is task-oriented or learning-oriented and usually relies on sequential steps, worked examples, lessons, exercises, workshop material, or training content.

Typical artifacts include how-to guides, tutorials, walkthroughs, courses, workshops, curricula, cheatsheets, exercises, and example-driven learning material.

Use this category when the central communicative goal is to teach a human reader how to use, configure, extend, or understand the software through guided action. Use T4 when deployment is the document's dominant goal. Use T5 when the document is a structured interface reference rather than a guided learning resource.

## T4. Deployment Guides
 
**name:** Deployment Guides  
**Count:** 1

This genre covers documentation for installing, configuring, deploying, operating, or troubleshooting software in a target environment. It generally serves maintainers, operators, platform engineers, or advanced developers responsible for making software available in development, test, staging, or production environments.

Typical content includes deployment prerequisites, environment configuration, infrastructure patterns, security requirements, credentials and permissions, rollout steps, operational checks, rollback procedures, and deployment troubleshooting.

Use this category only when deployment or operational rollout is the document's main purpose. General installation or user-operation instructions should normally be coded as T3 unless deployment is clearly dominant. An architecture diagram of deployment components belongs in T6 when its main purpose is to explain structure rather than guide deployment activity.

## T5. API Reference Documentation

**name:** API Reference Documentation  
**Count:** 8

This genre covers structured, precise documentation of programmatic interfaces. Its purpose is to enable developers, integrators, or tool users to understand how an interface is called, what inputs it accepts, what it returns, and which constraints govern its behavior.

Typical artifacts include REST or GraphQL API references, OpenAPI documentation, CLI command and flag references, SDK documentation, MCP tool references, XML API documentation, public API difference reports, interface contracts, and configuration or schema references.

Use this category when the principal target is a callable interface, command, parameter, schema, tool capability, or public technical contract. Use T6 for high-level architecture or system specifications whose main focus is component structure or design rationale rather than consumer-facing interface use.

## T6. Architecture, Design, and Specification Documentation
 
**name:** Architecture, Design, and Specification Documentation  
**Count:** 13

This genre covers documentation that explains how a system is structured, why it was designed in a particular way, how its components interact, or which technical constraints and specifications govern its design.

Typical artifacts include architecture documents, design documents, architecture decision records (ADRs), blueprints, state-machine diagrams, dependency matrices, feature matrices, technical schemas, package specifications, layout specifications, threat specifications, and system-level contracts.

Use this category when the workflow's main target is system architecture, component relationships, design rationale, formal technical specification, or a design decision. Use T5 for user- or developer-facing API reference material. Use T1 for project-level policies and processes rather than technical system design.

## T7. Release Notes and Changelogs
 
**name:** Release Notes and Changelogs  
**Count:** 36

This genre covers documentation that records and communicates software evolution across releases, milestones, versions, or change ranges. Its central purpose is to explain what changed and what those changes mean to users, developers, integrators, or maintainers.

Typical artifacts include release notes, changelogs, changesets, release highlights, milestone changelogs, release-blog drafts, compatibility notices, deprecation notices, support-policy updates, and upgrade information.

Use this category whenever the documentation target is principally tied to a release, a version, a tagged change range, or a collection of software changes. It applies whether the result is written to a Markdown file, GitHub Release, Issue, Discussion, or pull request.

Do not code a workflow as T7 merely because it runs during a release pipeline. The workflow must create, update, check, or otherwise target release-oriented documentation.

## T8. Frequently Asked Questions

**name:** Frequently Asked Questions  
**Count:** 1

This genre covers question-and-answer documentation that addresses recurring questions raised by users, developers, contributors, or other project stakeholders. Its main function is to provide concise, reusable answers to common problems or uncertainties.

Typical artifacts include FAQ pages, `FAQ.md` files, and curated question-answer sections derived from recurring community questions.

Use this category only when the document is explicitly organized around frequently asked questions and answers. Broader wikis, knowledge bases, glossaries, or troubleshooting collections belong in T9 unless an FAQ format is the dominant form.

## T9. Community Knowledge

**name:** Community Knowledge  
**Count:** 13

This genre covers documentation that captures, curates, or organizes collectively accumulated knowledge. The knowledge may be contributed directly by a community or extracted from community interactions such as issues, pull requests, discussions, forums, or support exchanges.

Typical artifacts include GitHub Wiki pages, knowledge bases, glossaries, troubleshooting collections, contributor-attribution pages, curated community resources, and documentation consolidated from multiple community-facing sources.

Use this category when the target artifact primarily serves as a shared knowledge repository or community-support resource. Use T8 for an explicitly question-and-answer FAQ. Use T1 for project governance or repository-management documentation, even if community participation is mentioned.

## T10. Agent-Facing Instructions, Skills, and Prompts
  
**name:** Agent-Facing Instructions, Skills, and Prompts  
**Count:** 14

This genre covers persistent documentation artifacts whose principal reader or executor is an AI coding agent rather than a human end user. These artifacts supply project-specific context, behavioral constraints, reusable knowledge, tool-use instructions, prompts, and task guidance.

Typical artifacts include `AGENTS.md`, `CLAUDE.md`, Copilot instruction files, Cursor rules, agent skills, agent prompts, workflow prompts, reusable agent rules, and instruction or learning-atom files.

Use this category when the document directly guides an agent's reasoning, file changes, tool use, task execution, or context management. A human-facing README, guide, or API document does not belong here merely because an agent generated or maintains it. This category is an explicit extension required for the GitHub Agentic Workflow corpus; it is not separately represented in the three source documentation studies.

## T11. General or Multi-Type Technical Documentation
  
**name:** General or Multi-Type Technical Documentation  
**Count:** 84

This category covers workflows that target technical documentation generally, maintain an entire documentation site, or span several documentation genres without specifying a single dominant documentation target.

Typical cases include workflows described only as "documentation updater," "documentation review," "docs drift," or "documentation site validator" when the workflow snapshot does not identify a primary subgenre. It also includes workflows that simultaneously address heterogeneous targets such as README material, reference pages, tutorials, and documentation-site pages.

This is a residual category, not a quality label. It does not mean that the documentation is generic, low quality, or unimportant. It indicates that the available workflow evidence does not support a reliable, more specific primary genre assignment. A specific type is assigned whenever the workflow explicitly identifies an API, release note, tutorial, agent instruction, FAQ, architecture artifact, or another narrower target.

## Decision rules and precedence

The following rules were used to maintain stable boundaries between genres:

1. **Classify the primary documentation target, not the workflow action.** A link checker can target an API reference, tutorial, wiki, agent instruction, or general documentation site. "Checking links" is a maintenance task, not a genre.
2. **Classify by communicative purpose, not by storage format.** A Markdown file may be a release note, a tutorial, an architecture decision record, an agent instruction, or a FAQ. File extension and repository path are insufficient on their own.
3. **Classify by target, not by GitHub output channel.** A release-note draft filed as an Issue remains T7. A documentation review posted as a pull-request comment does not become a pull-request genre.
4. **Prefer the most specific supported genre.** For example, an OpenAPI document is T5 rather than T11; an `AGENTS.md` file is T10 rather than T1; an ADR is T6 rather than T11.
5. **Use T11 only as a conservative fallback.** It is used when the workflow is explicitly broad or multiple target genres are equally central, or when the snapshot lacks sufficient semantic evidence for a narrower classification.

## Relationship to the maintenance-task taxonomy

Documentation genre and maintenance task are orthogonal dimensions. A workflow may, for example, validate links in T5 API Reference Documentation, synchronize T7 Release Notes and Changelogs with commits, refactor T10 Agent-Facing Instructions, or generate a T6 architecture diagram. The corresponding maintenance operations are defined separately in [documentation_maintenance_task_definitions.md](documentation_maintenance_task_definitions.md).
