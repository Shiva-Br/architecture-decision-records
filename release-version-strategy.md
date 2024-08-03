# Version/Release Strategy

## Context

We need to establish a clear versioning and release strategy for our monorepo application to manage dependencies efficiently and ensure a streamlined release process. This strategy should help in tracking changes, maintaining compatibility, and facilitating continuous integration and delivery.

## Decision Drivers

- **Consistency**: Ensure a uniform versioning scheme across all packages in the monorepo.
- **Clarity**: Provide clear communication of changes and updates to internal and external stakeholders.
- **Automation**: Support automated build, test, and release workflows.
- **Simplicity**: Avoid complexity in the versioning and release process to streamline development and maintenance.

## Considered Options

**Release Strategy:**

- **Continuous delivery**
  Continuous Delivery is a software development discipline where you build software in such a way that the software can be released to production at any time.
- **Release trains**
  Release on a set interval of time, like trains departing on a regular schedule. Developers choose which train to catch when they have completed their feature.

## Decision

We decided to adopt Semantic Versioning (Semver) for versioning the individual packages in our monorepo and choose Continuous delivery as release strategy.

## Rationale

- The software is deployable throughout its lifecycle.
- The team prioritizes keeping the software deployable over working on new features.
- Automated feedback on the production readiness of systems is available any time somebody makes a change.
- Push-button deployments can be performed for any version of the software to any environment on demand.

## Solution

1. **Semantic Versioning (Semver):**

   - Follow the Semver guidelines:
     - Major version (`X`): Incremented for breaking changes.
     - Minor version (`Y`): Incremented for new features that are backward-compatible.
     - Patch version (`Z`): Incremented for backward-compatible bug fixes.
   - Each package in the monorepo will maintain its version using the `X.Y.Z` format.
   - For shared packages, such as `UI` components, we must carefully manage versions due to their broad impact. Changes in shared packages should clearly explain by the committer, and versioned separatedly

2. **Commit Messages:**
   - Use conventional commits for commit messages to automate version management and changelog generation.
   - Example: `feat: add new authentication module` or `fix: resolve issue with API endpoint`.

By implementing this versioning and release strategy, we aim to achieve a well-structured, maintainable, and efficient development cycle, accommodating both ongoing development and stable application releases. Special attention will be given to shared packages like UI components to prevent widespread disruption and ensure a consistent user experience across all projects.
