# Data Safe Haven project report

This document contains a summary of progress across all stories in the [project roadmap](https://github.com/orgs/alan-turing-institute/projects/111/views/1).
It maps stories according to the (main) pillar and priority they contribute to.

## Infrastructure as code
Running projects working with sensitive data safely
Running cutting edge data science projects effectively


### Manage codebase releases and testing
https://github.com/alan-turing-institute/data-safe-haven-team/issues/50

Contributes to:
- Running projects working with sensitive data safely
- Running cutting edge data science projects effectively

#### Goal
Support for deployments of the Data Safe Haven at Turing and beyond

#### Progress
- Pen testing done: little found
- Penetration tested arranged and will be done in September
- Preparation for release v4.1.0: Deployment of different SRE variants, Security checklist
- Reviewing v4.1.0:  No significant problems is deployment logs, Problems found in security checklist relating to MSRDS
- Working on [Release 4.1.0](https://github.com/alan-turing-institute/data-safe-haven/issues/1544): fixes bugs and introduces necessary updates 


### Codebase maintenance
https://github.com/alan-turing-institute/data-safe-haven-team/issues/47

Contributes to:
- Running projects working with sensitive data safely
- Running cutting edge data science projects effectively

#### Goal
Ensure that codebase is kept up-to-date with bug fixes, security updates, external API changes etc.
- Ensure that DSH code is always deployable
- Ensure that known security issues are remediated/minimised as soon as possible
- Ensure that documentation is up-to-date with code base

#### Progress

- Working on debugging PostgreSQL permissions issues
- DBeaver driver fix https://github.com/alan-turing-institute/data-safe-haven/issues/1666
- Improve handling of file paths [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1705)
- Checking out Azure feature retirement warnings [Issue](https://github.com/alan-turing-institute/data-safe-haven/issues/1697)
- Investigating issues with Julia on AMD processors:  During the building of VM images for deployment in SREs, Julia created and stored compiled versions of packages that were suitable only for Intel systems, causing crashes when users wanted to use AMD systems
- Investigating issues with DBeaver on Tier 2+ SREs:  DBeaver drivers were not installing correctly during VM building, so it tries to download them from the internet. No problem on T1, but fails on T2.
- Testing solutions for cross-platform deployment: When deploying on Windows, some scripts fail if there are any spaces in the file path
- There has been work to address and improve issues and bugs related to last release while preparing for release 4.2.0.
- Factoring storage creation and account deployments out of main deployment script now allows for a more resilient process (not having to re-run everything when one fails)
- Also MS changing Azure Directory to Microsoft Entra ID has made necessary to spend time updating documentation and code, with the increased challenge that MS themsleves have not yet ocnsitently made the change.
- Name changing: [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1665) for changes to documentation - [Issue](https://github.com/alan-turing-institute/data-safe-haven/issues/1664) for changes to code
- Factor SHM storage creation out of main deployment script [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1673)
- 4.2.0 milestone related issues https://github.com/alan-turing-institute/data-safe-haven/milestone/21
- Add all contributors table to project README and docs
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1649)
  - Helps us better recognise contributors, especially those who do not appear in the commit history
  - Will require maintainers to upkeep the list
- Fixed an issue where the user could provide an invalid name for storage accounts
- [Removal of MSRDS](https://github.com/alan-turing-institute/data-safe-haven/pull/1535) which reduces support burden and codebase complexity, instead Guacamole implementaiton is more robust and secure
- [Removal of CoCalc](https://github.com/alan-turing-institute/data-safe-haven/pull/1554) Reduces support burden for future releases by removing a largely unused feature
- Investigating adding arrow R package support
- Development/features
  - [Drop Microsoft Remote Desktop](https://github.com/alan-turing-institute/data-safe-haven/issues/1159) primarly for increased security as it shows more issues than Guacamole, in doing this several other open issues are resolved
- Fixes/maintenance
 - Documentation improvements alan-turing-institute/data-safe-haven/pull/1484  and updates https://github.com/alan-turing-institute/data-safe-haven/pull/1535

### Identify and implement core IAC changes
https://github.com/alan-turing-institute/data-safe-haven-team/issues/28

#### Goal
Make DSH deployment more robust and development easier through using IAC and configuration management.
- Take advantage of IAC and configuration management in the DSH codebase which will
  - Make deployments faster
  - Make deployments more reliable
  - Make development easier
- Move away from non-idempotent, bespoke scripts (Powershell, bash, cloud-init)

##### Definition of done
On the release of a new major version which removes legacy, script-based deployment.

#### Progress
Arrived at a IAC MVP version of the code, available as a penetration tested [pre-release](https://github.com/alan-turing-institute/data-safe-haven/releases/tag/v5.0.0-rc.1).

This new code is better and easier for users to deploy, however some incompatibilities with the old code would require extensive work. 
As PowerShell heads to its final release it was decided not to work on fixing these.

Since finishing migration a lot of the work is focusing on structuring the code, small improvements aimed at the user experience and robustness.

These are main references and milestones, a more complete list is available on the [story issue](https://github.com/alan-turing-institute/data-safe-haven-team/issues/28)
- Codebase pre-release https://github.com/alan-turing-institute/data-safe-haven/releases/tag/v5.0.0-rc.1
- Next version milestone https://github.com/alan-turing-institute/data-safe-haven/milestone/20

## Information governance & standards
Infrastructure adhering to the latest agreed upon standard
Identifying, co-creating and supporting a TRE standard used across TRE infrastructures

## Community building
Creating resources for all stakeholders (inc. Citizens) to engage in the TRE conversation
Creating and maintaining open and active communication spaces & workspaces (Slack, GH)
Identifying and documenting everything that can be openly documented


