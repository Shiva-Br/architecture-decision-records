# Team Engagement

## Context

In our organization, we are considering the adoption of a monorepo architecture for our projects. While the monorepo approach has several technical advantages, it brings significant implications for team engagement and collaboration. This ADR focuses on the consequences of using a monorepo in the context of team dynamics, communication, and shared responsibilities in the engineering organization.

## Decision Drivers

- **Collaboration and Shared Work**: Teams will need to work together on shared components, which can lead to both positive synergies as well as potential friction.
- **Alignment and Ownership**: With shared codebases, team ownership can become ambiguous, leading to questions about accountability for changes and maintenance.
- **Code Quality and Standards**: Ensuring consistent coding standards and practices across multiple teams becomes crucial to maintain code quality.
- **Communication Overhead**: The reliance on communication will increase since multiple teams must coordinate on shared components and releases.

## Consequences

1. **Increased Communication Needs**: Teams will need to communicate frequently to agree on changes, especially when working on interdependent components.

   - **Potential Side Effect**: Increased meeting overhead and potential bureaucratic delays in decision-making.

2. **Ambiguity in Ownership**: It may become unclear which team is responsible for specific areas of the codebase, leading to “it’s not my job” attitudes.

   - **Potential Side Effect**: Reduced accountability and slower response to bugs or required updates in shared components.

3. **Cultural Clashes**: Teams with different practices and cultural norms may struggle to align on shared development practices.

   - **Potential Side Effect**: Disputes over coding standards, tool choices, and processes could arise, impacting morale and productivity.

4. **Shared Learning Opportunities**: Conversely, a monorepo can facilitate knowledge sharing as teams encounter each other’s work more frequently.

   - **Potential Side Effect**: Opportunity for cross-team mentorship and skill development can arise if managed properly.

5. **Obsolete Code**: With multiple teams working in the same repository, there is a risk of features or code becoming obsolete or poorly maintained.
   - **Potential Side Effect**: Technical debt could accumulate from components that are not actively taken care of by any particular team.

## Proposed Solutions

1. **Establish Clear Ownership with Clear Documentation**:

   - Assign explicit owners for each component or subsystem within the monorepo. This should be documented and made visible to all teams.
   - Create a joint collaboration document outlining responsibilities, ownership, and contribution guidelines.

2. **Regular Cross-Team Sync Meetings**:

   - Implement periodic cross-team meetings or stand-ups focused on shared components to synchronize efforts, share knowledge, and address issues early.
   - Encourage informal catch-ups and team-building activities to enhance inter-team relationships.

3. **Incorporate Review Processes**:

   - Develop a robust code review process that includes members from multiple teams to encourage diverse input and foster shared ownership.
   - Consider rotating review responsibilities to ensure all teams are engaged with different parts of the codebase.

4. **Define and Enforce Standard Development Practices**:

   - Establish a set of organization-wide coding standards and software development practices that all teams agree to follow.
   - Use automated tools to maintain consistency in code quality across the monorepo.

5. **Mentoring and Pair Programming Opportunities**:

   - Encourage pair programming and mentoring across teams to facilitate knowledge sharing and skill development.
   - Organize training sessions to help team members become familiar with all parts of the monorepo.

6. **Use of Feature Toggles and Branching Strategies**:

   - Implement feature toggles to allow teams to work on new features independently while maintaining stability in the main codebase.
   - Adopt a branching strategy that allows teams to develop in isolation before merging with the main branch. This helps mitigate the impact of changes on shared components.

7. **Monitor and Evaluate Engagement**:
   - Continuously collect feedback from teams regarding their experiences and challenges with the monorepo setup.
   - Use surveys or retrospectives to identify issues and promote an environment of constant improvement.

## Code Ownership

Even though all code is in the same repository, it is important to set virtual boundaries. Teams should be free to work on code for their own projects. If they need to modify other code, especially shared code, those changes should be reviewed by other teams.

Generally project code is owned by the teams working on the project while shared code is managed by specific Disciplines.

### Disciplines

Disciplines connect teams to discuss issues, share knowledge and make decisions.

Each discipline has a discipline manager that organises regular discipline meetings, manages agendas and publishes meeting minutes and decisions. During a discipline meeting, it's the manager's role to keep discussions productive and decide if something needs further research or a vote.

Meetings are open to interested parties but should be attended by at least one person from each active team that are part of the discipline. Discipline members can submit items to the agenda. Each item on the agenda should have an owner that presents the item and any proposals for discussion.

Discipline meetings should be used to get decisions on smaller issues and communicate best practices across teams. The goal is to discuss, decide and move along.

Currently there are 3 disciplines, but this may change as needed at any time.

**Dev:**

- Responsible for the monorepo, dependencies, tooling and shared code.

**Devops:**

- Responsible for CI, CD, operations and monitoring.

**Design:**

- Responsible for the brand, design system, UX and consistent design across projects.

## Solution

It is important to document all important decisions made in this project. This might, for instance, be a choice between a library (e.g., moment vs date-fns), or a decision on features (e.g., pagination vs infinite scroll). Design documentation is important to enable people understanding the decisions later on.
Decisions should be documented using ADR formatting in the same project or a different repository.

## Resulting Context

By carefully considering team engagement within a monorepo structure, we can foster a collaborative and accountable environment. Implementing the aforementioned solutions will help mitigate potential negative consequences while leveraging the advantages of having a unified codebase.

## Conclusion

Adopting a monorepo architecture necessitates a deep understanding of how teams will interact with each other and with the codebase. By proactively addressing the potential side effects on team dynamics and engagement, we can create a healthy and productive culture in which teams collaborate effectively and take joint ownership of shared components.
