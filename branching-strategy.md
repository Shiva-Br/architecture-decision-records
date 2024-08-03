# Branching Strategy

## Context

How do we want to organise work in branches and how should changes be released?

## Decision Drivers

- We need to have confidence in our releases.

- We want more structured releases while we're still getting our footing in a shared monorepo.

- We need simplicity so different teams can plan for what is going out the door from them.

## Decision

We have chosen **gitFlow** branching standard for our project.

## solution

At the core, the development model is greatly inspired by existing models out there. The central repo holds two main branches with an infinite lifetime:

- **master**
  We consider origin/master to be the main branch where the source code of HEAD always reflects a production-ready state.

- **develop**
  We consider origin/develop to be the main branch where the source code of HEAD always reflects a state with the latest delivered development changes for the next release. Some would call this the **integration branch**. This is where any automatic nightly builds are built from.

When the source code in the develop branch reaches a stable point and is ready to be released, all of the changes should be merged back into master somehow and then tagged with a release number.

### Supporting branches

Next to the main branches master and develop, our development model uses a variety of supporting branches to aid parallel development between team members, ease tracking of features, prepare for production releases and to assist in quickly fixing live production problems. Unlike the main branches, these branches always have a limited life time, since they will be removed eventually.

The different types of branches we may use are:

- **Feature branches**
- **Release branches**
- **Hotfix branches**

Each of these branches have a specific purpose and are bound to strict rules as to which branches may be their originating branch and which branches must be their merge targets.

#### Feature branches

May branch off from:
**develop**
Must merge back into:
**develop**
Branch naming convention:
anything except master, develop, release-\*, or hotfix-\*

#### Release branches

May branch off from:
**develop**
Must merge back into:
**develop**
Branch naming convention:
release-\*

#### Hotfix branches

May branch off from:
**master**
Must merge back into:
**develop** and **master**
Branch naming convention:
hotfix-\*
