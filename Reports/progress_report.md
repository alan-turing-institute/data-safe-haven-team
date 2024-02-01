# Data Safe Haven project report

This document contains a summary of progress across all stories in the [project roadmap](https://github.com/orgs/alan-turing-institute/projects/111/views/1).
It maps stories according to the (main) pillar and priority they contribute to.

Included stories are those that were scheduled and/or prioritised over this period (February 2023-February 2024), some not scheduled stories are included when there are updates for them regardless (indirect contirbutions from other stories, relevant work recently started, or something to report in general).

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

### Co-create a TRE standard (SATRE)
https://github.com/alan-turing-institute/data-safe-haven-team/issues/23

Contributes to:
- Identifying, co-creating and supporting a TRE standard used across TRE infrastructures

#### Goal
Develop the SATRE specification that UK TREs can evaluate themselves against

##### Definition of done
SATRE specification published

#### Progress
[SATRE specification](https://satre-specification.readthedocs.io/en/stable/) published, and available for contribution and reproducibility in its [open repository](https://github.com/sa-tre/satre-specification).

Currently Turing and HIC have self-evaluated against it and evaluations are available openly, several conversations ongoing about other institutions doing the same and making them available.

- Outputs:
  - SATRE specification V1 and [associated technical paper](https://zenodo.org/records/10053383)
  - Internal DARE report, link will be added and published openly
  - [User report](https://zenodo.org/records/10066800): characterises users, with a wider notion than we started of what users are. Lays the fundation for futher usability work, going beyong technicla features and into training and documentation
  - UK TRE Community - SATRE WG: the ongoing work and evolution of the specification is now a working group within the Uk TRE Community

### Documentation management
https://github.com/alan-turing-institute/data-safe-haven-team/issues/32

Contributes to:
- Identifying, co-creating and supporting a TRE standard used across TRE infrastructures
- Creating resources for all stakeholders (inc. Citizens) to engage in the TRE conversation
- Identifying and documenting everything that can be openly documented

#### Goal
Comprehensive and clear documentation for the DSH, SATRE & TRESA will ensure open, reproducible outputs from this project.
- Ensure all relevant information is captured in documentation
- Test accessibility and discoverability of docs with relevant groups
- Iterate documentation in line with wider project work (e.g. TRESA processes, DSH updates)
- Determine what can/can't be documented (e.g. from an IG perspective).

#### Definition of Done
When funding ends for the project and we have openly documented everything that we feel we can

#### Progress
Documentation management have not been a story actively worked in, yet some processes have been updated and documented and needs identified.
While the story goes beyond Production processes it is worth noting that those have been handed over to TRESA, who are already suggesting and appliying changes.

### SATRE: stakeholder engagement and community buy out
https://github.com/alan-turing-institute/data-safe-haven-team/issues/66

#### Goal
Ensure that institutions evaluate themselves against SATRE and that the momentum is maintained between funded phases

At the end of the funded phase of SATRE there was a growing community interest, with institutions and stakeholders affirming they would evaluate themselves against it and contribute feedback.

Without ongoing resources the necessary support to ensure that happens cannot be provided and SATRE may end up not being adopted.

#### Definition of Done
There are a number of self evlauaitons completed, there is feedback on the spec repository and, ideally, there is an active WG within the TRE Community continuing to work on it.

#### Progress
Work is folded into the [UK TRE Community](https://github.com/alan-turing-institute/data-safe-haven-team/issues/52), already SATRE is formally becoming a UK TRE Community WG.

## Community building
Creating resources for all stakeholders (inc. Citizens) to engage in the TRE conversation
Creating and maintaining open and active communication spaces & workspaces (Slack, GH)
Identifying and documenting everything that can be openly documented

### Stakeholder landscape review
https://github.com/alan-turing-institute/data-safe-haven-team/issues/30

Contributes to:
- Creating resources for all stakeholders (inc. Citizens) to engage in the TRE conversation
- Creating and maintaining open and active communication spaces & workspaces (Slack, GH)

#### Goal
Across a lot of our work (DSH project, SATRE, UK TRE community) there has been a lot of discussion around who the impacted parties are, how they are categorised, what their interests/needs are etc.

An effective stakeholder map showing all parties we think we should engage with will help us prioritise who to collaborate with, and strengthen our work in community building within the TRE space (which is kind of where this project is heading, above and beyond getting others to use the DSH).

- [ ] Brainstorm and identify potential stakeholder groups
- [ ] Engage different groups through interviews/workshops to better understand them
- [ ] Create engagement pipeline & priority for different groups

#### Definition of Done
- When we have an intended end-output from engagement with our established groups (e.g. by the end of the project, we want X group to be part of the UK TRE community, we want Y group to have contributed to the DSH repo...)

#### Progress
The work done in [SATRE](https://github.com/alan-turing-institute/data-safe-haven-team/issues/23) and the [UK TRE Community](https://github.com/alan-turing-institute/data-safe-haven-team/issues/52) have directly contributed to estbalishing a relationship with key stakeholders, identify and characterise them.

Direct and explicit work on this story have not been carried out (not scheduled in this period).

We are now establishing the engagement pipleline by creating an internal CRM (sharepoint based currently).

### UK TRE Community leadership
https://github.com/alan-turing-institute/data-safe-haven-team/issues/52

Contributes to:
- Creating resources for all stakeholders (inc. Citizens) to engage in the TRE conversation
- Creating and maintaining open and active communication spaces & workspaces (Slack, GH)

#### Goal
Provide a space for those involved in building, using and responsible for governance of TREs to discuss and reccomend best practices.
- [ ] Host online working spaces, events and workshops to support the UK TRE Community
- [ ] Share best practices i.e. for making radiology data available for researchers
- [ ] Empower the community to help influence policy decisions

#### Progress
A lot of of effort has been put this year into the UK TRE Community, this year has seen the community mature and evolve from the original RSE TRE Community.
Currently we are delivering a funded project to ensure its sustainability which focuses one establishing the necessary spaces and governance processes.

All work and progress during the funded phase can be consulted in [its board](https://github.com/orgs/uk-tre/projects/1)

- The UK TRE Community event was held in Swansea on 4 September as a RSEcon23 satellite event. The event was very well attended with around 90 people in person and 50 online (figure to be revised), attendees were active on the day and had very positive feedback.
  - [Report and notes](https://www.uktre.org/en/latest/events/wg_workshops/2023-09-04-september-meeting/index.html#provisional-schedule)
- We were awarded the DARE UK Community call. It was prepared and submitted to DARE UK community call, with full agreement and participation of the community itself
- Celebrated December community event (virtual). We presented the plans and work within this funded phase, which included a vision and mission for the community
  - [Report and notes](https://www.uktre.org/en/latest/events/wg_workshops/2023-12-05-december-meeting/index.html)
- The first version of the Community Website is ready, it has been done using Hugo to balance quality and sustainability (being easily maintained and updated by the community after funding ends)
- Governance processes are being established, striving for simplicity in this phase. The conversation and work is open and welcomes all input and feedback. This is the [most active issue](https://github.com/uk-tre/community-management/pull/54) and a good starting point

### Communication and outreach
https://github.com/alan-turing-institute/data-safe-haven-team/issues/35

Contributes to:
- Creating and maintaining open and active communication spaces & workspaces (Slack, GH)
- Creating resources for all stakeholders (inc. Citizens) to engage in the TRE conversation

#### Goal
- Supporting the user community of the DSH codebase
- Publicising our work via blogposts, reports or papers
- Communicating our work through conference/workshop talks or posters 

#### Progress
This story has changed in scope along the year, work done here has been tha tof presenting DSH externally via events and talks.

Yet we have identified work to be done within this story to define and establish a DSH community and user base, what this means and entails needs to be discussed and agreed yet.

- We have established a shared slack channel with UCL to discuss common approaches to information governance processes
-  [AI UK demonstration proposal](https://thealanturininstitute.sharepoint.com/:x:/s/SafeHaven/EfKD3w8Gi9NFv6JBshOkugsBOnn4v3ZdU-FTeIcy5obQcg?e=Rhq9w4)
  - [proposal collaborative note](https://hackmd.io/AmcYdsyETU2dVgtIdfVL-g)
  - We are following a similar format to last year but want to bring forward the community work and the satre specification. We want to have an interactive activity that blends role playing the different stakeholder groups and collectively deciding on specification features. The demo challenge last year did not work so the technical side this year will be demonstrated by a video and project members "touring" the repositories, docs and environment
- Met with Nottingham to support them as users of the DSH codebase
- The team worked together on the content for DSH activities on RSEcon  as well as the UK TRE community satellite event #46 . 
- The team visited the Bennett Institute for a show and tell about DSH and OpenSafely https://github.com/alan-turing-institute/tps-project-management/issues/157
  - No immediate collaboration but agreed to be involved in the specification and TRE community
- For discussion: this story needs to be redefined to include external engagement or a new one created

## TRESA

## Meta
Work and stories that do not belong directly in any pillars but are necessary for all

### Project strategy and ways of work
https://github.com/alan-turing-institute/data-safe-haven-team/issues/43

#### Goal
The aim is to develop a project strategy and revise best ways of work to achieve it

Through several strategy sessions we will:
- Define our north star (vision & mision)
- Establish the project pilars or areas, defining what success looks like for each
- Prioritise the measure of success, which are essential to consider the project succesful
- Identify work required to achieve success
- Allocate work by team
- Produce an initial roadmap
- Evaluate required effort for the work against team capacity
- Develop and agree new ways of work, including meeting structure and use of project's repositories and projects

#### Progress

##### Strategy

Through several team wide sessions we jointly produced a [project strategy](https://thealanturininstitute.sharepoint.com/:p:/s/SafeHaven/Ebrp4Iyc9M1NpPTgpgHdj5kB7HPvH-2gM0oNd97jJu6oxw?e=eN0ZFw)https://thealanturininstitute.sharepoint.com/:p:/s/SafeHaven/Ebrp4Iyc9M1NpPTgpgHdj5kB7HPvH-2gM0oNd97jJu6oxw?e=eN0ZFw a long, medium and short term levels.

This resulting in a clear Vision & Mision that have allowed internal alignment and improved external communications

>To remove barriers to working safely and effectively with sensitive data, 
by promoting and demonstrating a culture of open, community-led development
of interoperable foundational infrastructure and governance.

We also agreed the pillars of the project and estbalished a [roadmap](https://github.com/orgs/alan-turing-institute/projects/111/views/1)https://github.com/orgs/alan-turing-institute/projects/111/views/1 of the necessary work for success.

##### Ways of work
Troughout this year we have also iterated our ways of work which are [openly available here](https://github.com/alan-turing-institute/data-safe-haven-team/blob/main/WaysofWork.md), they are focused in increased communication and work prioritisation.
