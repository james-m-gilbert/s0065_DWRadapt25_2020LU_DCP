<!-- omit in toc -->
# Contributing to 2023 DCR Base Studies

See the [Table of Contents](#table-of-contents) for information about getting the study set up on your machine, and how to make make changes to the `main` branch.

- [Branch Management](#branch-management)
- [Pull Requests](#pull-requests)
- [Commit Messages](#commit-messages)


# Branch Management

The project is using [GitFlow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) for branch management. Typical development involves three types of branches:

- `main`
    - Stores official release history (tags)
    - Contains abridged history of the project
- `develop`
    -  Serves as an integration branch for features
    -  Contains the complete history of the project
    - Commit messages on `develop` should summarize the changes made to inputs, and the effects on the results of the model since most commits to develop come from a feature branch
- `feat-`
    - Branched from `develop`.
    - Used to develop new features for the upcoming or a distant future release.
    - Exists as long as the feature is in development but will eventually be merged into develop
    - Commit messages should follow [these basic guidelines](https://commit.style/)
    - Never interacts directly with `main`.

The project may open the following branch types on a case by case basis:

- `bugfix`/`hotfix`/`release`


# Making a contribution

## 1. Create a new __feat__ branch 
- Branch name should start with the stem `feat-` , and follow the kebab case style
- The name should be:
    - descriptive
    - specific to the work being done 
    - not reference the developer of the branch

__Bad branch names would be `feat-updates`, or `feat-zach-roy-work`.__

__Good branch names would be `feat-flow-feather-river`, or `feat-delivery-mwd`.__


## 2. Make your model changes
- Commit changed input files every time you run the model, this helps keep track of your train of thought when making changes
- Commit messages should follow the style guide below
- Do not commit outputs at every step in the investigation branch

## 3. Open a Pull Request on `develop`
- See the [section](#pull-requests) below

## 4. Create a folder in the Sequence Directory
- [SWP Climate Adaptation Plan - Investigations](https://cawater.sharepoint.com/:f:/r/sites/dwr-callite/Shared%20Documents/SWP%20Climate%20Adaptation%20Plan/CalSim%203%20models/investigations?csf=1&web=1&e=6luxLl)
- This folder should be structured like the `Investigations` folder on `CVM_Inventory`: `//nasbdo/CVM_Inventory/_DeliveryCapabilityReport/2023_DCR_Studies/_cc_adaptation/_investigations`

# Pull Requests

Pull requests need to be opened on `develop` when incorporating work from a feature branch.

Pull requests should:

- Start with the stem `WIP` so they are not automatically given a release number 
- Use a title that references the branch being incorporated
- Include a discussion of:
    - Motivation for the updates
    - Conceptually, what was changed to satisfy the motivation
    - Technically, what was changed in the model inputs
    - Conceptually, how the results changed
- Include links to any relevant Gitea Issues that are being addressed by the branch

# Branch Management Visual Example                                    
```                          
v0.1                              v0.2             v0.3    
A---------------------------------B----------------C                 main
|                                /                /
|                        E--Y---Z----------------F                   release
|                       /        \              / \
G----------------------H----------J------------K---AA                develop
|\                     |\                      |
| L---M---N            | |                     |                     feat-tucp
|\                    /  |                     |    
| ---------------O---P   |                     |                     feat-casp
\                        |                    /
 Q---R---S---T-----------U---V---------------W                       feat-dcp
```

Notes:

- Pull requests should be opened prior to commits `H` and `K` on `develop`.
- The `feat-tucp` branch was never merged
- Changes in `H` were pulled into the feature branch `feat-dcp` through commit `U` prior to a pull request
- Release branches were branched off develop on commits `E`, and `F`. No new features can be added after this point-only bug fixes, documentation generation, and other release oriented-tasks should go in this branch as represented by commit `Y` and `Z`. Once ready to ship, the `release` branch gets merged and tagged into `main`. It should also be merged to `develop` (represented by commits `J` and `AA`)  which may have advanced since the release was initiated.
- Tags on `A`, `B`, and `C` are the official release history stored on `main`.

# Commit Messages

Commit messages should follow the [simple style guide from Tim Pope](https://commit.style/).

```
Commit message style guide for Git

The first line of a commit message serves as a summary.  When displayed
on the web, it's often styled as a heading, and in emails, it's
typically used as the subject.  As such, you should capitalize it and
omit any trailing punctuation.  Aim for about 50 characters, give or
take, otherwise it may be painfully truncated in some contexts.  Write
it, along with the rest of your message, in the imperative tense: "Fix
bug" and not "Fixed bug" or "Fixes bug".  Consistent wording makes it
easier to mentally process a list of commits.

Oftentimes a subject by itself is sufficient.  When it's not, add a
blank line (this is important) followed by one or more paragraphs hard
wrapped to 72 characters.  Git is strongly opinionated that the author
is responsible for line breaks; if you omit them, command line tooling
will show it as one extremely long unwrapped line.  Fortunately, most
text editors are capable of automating this.
```
