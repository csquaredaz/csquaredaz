# Chad Countryman

**Senior Salesforce Engineer.** Apex, Lightning Web Components, integrations and event-driven systems.

I've been building software for 20+ years, 10+ of them on Salesforce. I care about code that holds up in production: bulk-safe, secure by default, testable without the database, and documented well enough that the next engineer can change it with confidence. The repositories below are clean-room builds of patterns I've used on large production orgs, rebuilt in a neutral domain so anyone can read, run and judge them.

## Repositories

| Repo | What it is | Highlights |
| --- | --- | --- |
| [apex-event-ingestion](https://github.com/csquaredaz/apex-event-ingestion) | Idempotent inbound event ingestion for Salesforce | Message store, Command and Composite dispatch, Finalizer recovery with exponential backoff, Claim Check, stall detection. 238 tests, 100% coverage. |
| [apex-core-lib](https://github.com/csquaredaz/apex-core-lib) | Apex platform foundation, released as an unlocked package | Metadata-driven DI, FFLIB-style layers, trigger framework with kill switch, user-mode data access, retrying callout client. 195 tests, 100% coverage. |
| [apex-platform-logging](https://github.com/csquaredaz/apex-platform-logging) | Observability for apex-core-lib | Rollback-safe Platform Event logging, persistence and retention, Slack Block Kit alerts through ports and adapters. |
| [apex-design-patterns](https://github.com/csquaredaz/apex-design-patterns) | A catalog of 16 GoF and Enterprise Integration Patterns in Apex | Each pattern leads with when **not** to use it, has a 200-record bulk test, and links to its production form in the repos above. |
| [claude-code-salesforce-skills](https://github.com/csquaredaz/claude-code-salesforce-skills) | Claude Code plugins for Salesforce engineering | Skills and agents that encode FFLIB, security, testing and code-review standards. The other repos are built with them. |

**How they fit together:** `apex-core-lib` is the foundation. `apex-platform-logging` and `apex-event-ingestion` build on it. `apex-design-patterns` teaches the patterns and links to where each one runs at full size. `claude-code-salesforce-skills` holds the standards that every repo follows.

## How I build

- **Tested by default.** Apex unit tests with Stub API mocks, integration tests with real DML as Minimum Access users, and a 90% coverage gate.
- **CI on every pull request.** Each PR deploys to a fresh scratch org, runs the full suite and Salesforce Code Analyzer, then deletes the org.
- **Decisions are written down.** Every repo has Architecture Decision Records that explain each choice and the alternative it rejected.
- **AI-assisted, human-reviewed.** I use Claude Code under codified standards (each repo has a `CLAUDE.md`). Every AI-assisted commit carries a `Co-Authored-By: Claude` trailer and goes through the same PR review and CI gates as everything else.

## Also

- **SalesforceChaCha:** co-author of a bi-weekly Salesforce engineering newsletter with 650+ subscribers.
- **25 certifications,** including Salesforce Application and System Architect, Platform Developer I and II, JavaScript Developer I, MuleSoft Developer and Claude Certified Associate.

## Connect

[LinkedIn](https://www.linkedin.com/in/csquaredaz) · [Trailblazer](https://www.salesforce.com/trailblazer/csquaredaz)
