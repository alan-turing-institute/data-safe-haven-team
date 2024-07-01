# Data Safe Haven project report

**Period: [February 2024-August 2024]**

This update: 08 April 2024 to 24 June 2024

## Progress

This section contains a summary of progress across all stories in the [project roadmap](https://github.com/orgs/alan-turing-institute/projects/111/views/1).
It maps stories according to the (main) pillar and priority they contribute to.

### June summary 

June has continued to be focused on development and UK TRE community, with the addition of DSPT submission.

Development saw the completion (or very near, this week) of [rc2 milestone](https://github.com/alan-turing-institute/data-safe-haven/milestone/20). This milestone had two main goals: for users to reduce costs, simplify user management and a more coherent CLI; For developers a simpler deployed architecture and a better structure for configuration and command line.

Previous bulk of the work was to migrate, now we are entering actual changes and improvements (no longer the same thing with a different deployment technology).

The UK TRE Community work has been lighter, as all co-chairs needed a breather after quarterly event. But we have been organising for very important things: September annual in person meeting and UKRI Skills grant. The latter we might be able to jump back into as partners.

DSPT submission completed! thanks to everyone involved. The last stretch required a bit of work and putting some things in place like a spot check or new ROPA specific for TRESA. Several areas of improvement have been identified and we need to follow up soon with the team and DP how to improve.

### May summary

May has continued to be marked by codebase development. There are two main things to highlight:
- [Milestone 20](https://github.com/alan-turing-institute/data-safe-haven/milestone/20) has been reprioritised to accommodate user facing features and DATE MOVED to end of June to be on time for RSEcon.
- Upcoming patch release: TRESA discovered a bug with Guacomole preventing correct deployment, this has been fixed and a release with it will be made

The UK TRE Community has been the other focus of the month,
been marked by a transition phase towards an unfunded period,
support for the new Working Groups and preparation of the 5 June quarterly events.

While new members are stepping up resource load for project PM has prevented work on other areas.
This made sense in the lead up to the quarterly event and wrap up of funded phase activities but is not sustainable.

### April summary

April was a month focused on development of the Pulumi codebase (now the development branch), wrapping up the UK TRE Community funded phase and RAM handover.
TRESA has also updated to the latest powershell version and is preparing for the May DSG.

Development has been marked by the 5.0.0rc2 milestone.

The UK TRE Community work ended with the Working Groups day that was well attended with members being active in WGs (Funding & Sustainability WG re-emerged).
The new website is ready but migration is pending, the Governance documents were published in their first iteration with a section for pending discussions.


### Codebase development

Running projects working with sensitive data safely
Running cutting edge data science projects effectively

#### Manage codebase releases and testing: [#50](https://github.com/alan-turing-institute/data-safe-haven-team/issues/50)

Contributes to:

- Running projects working with sensitive data safely
- Running cutting edge data science projects effectively

##### Goal

Support for deployments of the Data Safe Haven at Turing and beyond

##### Progress

###### June 2024

Patch release [v4.2.2](https://github.com/alan-turing-institute/data-safe-haven/pull/1955)
  - Fixes SSL bug
  - Running test deployment

###### April-May 2024

Helping TRESA upgrade prod4 to v4.2.0 in place and Working through a from-scratch deployment and bug-fixing along the way

###### February-March 2024

Having completed development of v4.2.0 we prepared the release which included preparing a release branch and deployment in an environment for pen testing.

Extensive time was allocated to deploying and the errors/bugs that arose,
as well as preparing for pen testing.
This included deployment but also requesting specific tests like changes to the network and firewall configuration.

Pen testing was arranged and carried out, managing to spend within the 2023-2024 FY.
iSTORM kept better communications than last time and did not find concerning issues.
All reported vulnerabilities were known to us before the test and we are confident all are mitigated by technical or process controls.
We don't believe any of the vulnerabilities identified present a strong risk of enabling unauthorised data ingress or egress.

#### Codebase maintenance: [#47](https://github.com/alan-turing-institute/data-safe-haven-team/issues/47)

Contributes to:

- Running projects working with sensitive data safely
- Running cutting edge data science projects effectively

##### Goal

Ensure that codebase is kept up-to-date with bug fixes, security updates, external API changes etc.

- Ensure that DSH code is always deployable
- Ensure that known security issues are remediated/minimised as soon as possible
- Ensure that documentation is up-to-date with code base

##### Progress

###### June 2024

Over this period we have identified bugs in production that have been fixed, resulting in a new v4.2.1:

- [Fix broken link in docs](https://github.com/alan-turing-institute/data-safe-haven/pull/1949)
- [Fix SSL cert error](https://github.com/alan-turing-institute/data-safe-haven/pull/1939)
  - It was possible for users to enter a domain name which isn't supported by Let's Encrypt.
- [Fix error when deploying virtual gateway](https://github.com/alan-turing-institute/data-safe-haven/issues/1947)
    - Azure no longer supports the use of a basic public IP address SKU

###### April-May 2024

Worked on providing clearer error messages for context related commands, making using the CLI more user friendly.

Also worked in replacing Log Analytics/OMS agent with Azure Monitor Agent as OMS agent is being retired in August 2024, and should be replaced with Azure Monitor Agent.
In the same way updated to using Entra ID instad of Azure AD
   

###### February-March 2024

Have worked on updating software used within SREs to ensure the security and functionality of the environment:

- Guacamole server updated [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1741)
- Nexus server updated [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1744)
- CodiMD server updated [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1743)

Added and tested a script to handle SAS access tokens renewal, currently expiring yearly.
These are required manage access to data storage (and therefore ingress and egress).
The relevant PR is here https://github.com/alan-turing-institute/data-safe-haven/pull/1739.
In the process we realised SAS tokens are bound to Store Access Policies which could be modified to have no end date,
we are currently considering the covenience of this approach versus potential security issues in https://github.com/alan-turing-institute/data-safe-haven/issues/1751 .

Improved use of hardcoded domain names and IPs.
The hardcoded lists are difficult to maintain and are prone to going out of date.
Despite not fully stopping use of hardcoded domains and IPs, improvements have been made for the 4.2.0 release by relaxing rules where security allows.
For this the team checked individuals cases and applied where possible,
no security issues where found and we added this as a specific thing to pent test.
Related PR is https://github.com/alan-turing-institute/data-safe-haven/pull/1745 and explanatory issue is https://github.com/alan-turing-institute/data-safe-haven/issues/1549 .

An issue with Jupyter notebooks not being able to use Python when launched from the menu was found,
despite extensive work a fix was not found and decided to let it be by documenting the right workaround: launching Jupyter Notebooks from the terminal.
The issue is https://github.com/alan-turing-institute/data-safe-haven/issues/1584.

Updated documentation to reflect Azure Active Directory name change to Microsoft Entra.

#### Identify and implement core IAC changes: [#28](https://github.com/alan-turing-institute/data-safe-haven-team/issues/28)

##### Goal

Make DSH deployment more robust and development easier through using IAC and configuration management.

- Take advantage of IAC and configuration management in the DSH codebase which will
  - Make deployments faster
  - Make deployments more reliable
  - Make development easier
- Move away from non-idempotent, bespoke scripts (Powershell, bash, cloud-init)



###### Definition of done

On the release of a new major version which removes legacy, script-based deployment.

##### Progress

Story DONE: with the merge of the Pulumi codebase into development IAC has become the sole focus of development efforts,
the core necessary changes have been identified and implemented and [a roadmap](https://github.com/alan-turing-institute/data-safe-haven/blob/develop/ROADMAP.md), milestones and goals identified.
This story has achieved:

- New and complete Pulumi version of the codebase. See [5.0.0rc1 pre-release](https://github.com/alan-turing-institute/data-safe-haven/releases/tag/v5.0.0-rc.1)
- More efficient and robust codebase and deployment process
- Improved experience for TRE admnis: reduced cost, simpler user management, more coherent CLI. See [5.0.0rc2 milestone for more details](https://github.com/alan-turing-institute/data-safe-haven/milestone/20)

It is no longer useful for this story to contain development efforts or to distinguish IAC work from the rest of development work.

New stories will be created with specific goals for development,
in particular [#79 'Develop outside-run inside'](https://github.com/alan-turing-institute/data-safe-haven-team/issues/79) is the immediate follow up story to the work previously reported here.

[Milestone rc2 is the last one reported under this story](https://github.com/alan-turing-institute/data-safe-haven/milestone/20).

###### June 2024

- Milestone review
  - Our aims for rc2
    - Remove SHM (but really merge context and SHM)
    - Use Ubuntu Jammy (pen test in the future to double check snap security)
    - Get ansible/workspace software stuff in
  - Next milestone is rc3, not a final release
  - In the next phase we will continue outstanding bug fixes
  - All new feature work must be related to RSECon - develop outside, run inside
  - I will arrange some meetings for scoping that feature
    - So that we can consider some options for this
    - Sketch what our solution will look like
- [Logging changes](https://github.com/alan-turing-institute/data-safe-haven/pull/1936)
  - Cleaner console output
  - Logs verbose/debugging information to a file by default
- [Fixes for pulumi output through logger](https://github.com/alan-turing-institute/data-safe-haven/pull/1957)
- [Improvement of multiline log message rendering](https://github.com/alan-turing-institute/data-safe-haven/pull/1953)
- [Collect console formatting and user interaction functions in a new console module](https://github.com/alan-turing-institute/data-safe-haven/pull/1948)
- [Fix OSError during tests](https://github.com/alan-turing-institute/data-safe-haven/pull/1951)
- [Separate SHM and SRE config](https://github.com/alan-turing-institute/data-safe-haven/pull/1943)
  - Changes user interface
  - Removes the need to specify SREs (or explicitly specify no SREs) when creating an SHM
  - Paves the way to combine Context/SHM and rename to SHM


- Investigating potential issues with updating to Ubuntu 22.04 [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1909)
    - Ubuntu 22.04+ installs some packages from the Canonical Snap store
    - We have to provide VMs with access to the endpoints for Snap/snapcraft, but it is unclear if this risks allowing a form of egress
    - Currently appears it is not possible to build snaps on a VM and upload to the snap store, as building snaps requires additional downloads that are blocked by existing firewall rules
- Logging and stdout changes
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1936)
  - Improve output format/verbsoity
  - Cleaner CLI for users
  - Clearer guidlines for developers
  - Removing unused or uneeded code
- Remove SRE index
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1930)
  - Move towards separating SHM and SRE
- Move log analytics to SRE
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1928)
  - Move logging workspace to SRE and make a first attempt at connecting SRE resources to it


- Co working on snapd problems
    - Necessary for continuing work on updating to newer version of Ubuntu, see [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1909)
- A number of small PRs focused on user experience, clarity of errors
  - Continue working on [context command errors](https://github.com/alan-turing-institute/data-safe-haven/pull/1916)
  - [Clarify subscription arugment of context add](https://github.com/alan-turing-institute/data-safe-haven/pull/1919)
  - [Validate arguments for 'user' commands](https://github.com/alan-turing-institute/data-safe-haven/pull/1921)
  - [Supress Pydantic warnings when calling `dsh config template`](https://github.com/alan-turing-institute/data-safe-haven/pull/1920)

###### April-May 2024

- Upgrading Ubuntu VMs to Gen 2 and newer versions of Ubuntu
    - [Draft PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1909)
    - Azure will be defaulting to using Gen2 VMs at some point in the future, so we need to test them now
    - We currently use Ubuntu 20.04, which is now 2 Long Term Support versions behind - latest is 24.04
    - Investigating updating to 22.04, which may need further input before it can be completed
    - Not clear if 24.04 is fully supported by Azure Update Management etc yet, but can be tested.
- Debugging issues with user synchronisation
    - users were not synchronising correctly between Entra ID and the workspace user databases, so was not possible to connect to workspaces
- Configuration management and packages experimenting
- Small bug fixes/corrections



- Add protection against configuration changes
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1881)
- Co working on maintenance configuration
  - Adding resource f
- v5.0.0-rc2 milestone review
  - Review project labels
  - Closing closed issues
  - Moving low priority issues to future milestones, or adding non-essential label
- Arbitrary pulumi commands
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1888)
  - Add ability to run Pulumi CLI commands using project and stack combinations from a DSH deployment
  - Useful for developers and admins for debugging, importing resources
- Merged protection for configuration changes
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1881)
- Started working on minimal workspace software + configuration management
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1892)
- Moved firewall from SHM to SRE
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/issues/1871)

    Reviewed PRs
        Merge develop branch into python-migration branch, bringing it up to parity with the latest powershell codebase PR
        Minor fixes to python/pulumi deployment codePR
    [name=James]
        Got Apricot server (mostly) working!


    Merging development branches
        pwsh development into python
        python into develop, the default branch
        Represents that the Python codebase is actively developed and pwsh is deprecated
    Fixing container image update workflow
        Ensures container image versions are current
        Open Issue to improve how container images and versions are specified in the repository to make this clearer and more robust
    Apricot overview
        Detailed look at the code we will use in v5.0.0rc2 to remove the need for domain controllers
    Entra ID integration PR
        Preparation for replacing domain controllers with Apricot
        Extra functionality for admins to manage TRE users
    Migrating new networking rules PR
        Implementing the networking rules from v4.2.0 in Pulumi

- Integrating Apricot
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1778)
  - Important step in removing domain controllers
  - Will reduce cost
  - Will reduce complexity
  - Potential for wider adoption of Apricot as an independent package
- Add UniqueList annotated type
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1815)
  - Simple, robust way to ensure user supplied data is valid
- Removing magic numbers
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1819)
  - Good code hygiene, will likely save us headaches in the future
- Moving pulumi state from configutation
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1820)
  - Should simplify configuration
  - Helps multiple people manage one TRE (as it will become simpler to spot conflicts)
  - Will attempt to also simplify local files necessary to run dsh
- Integrating dependabot
  - Regularly notifies and opens PRs for dependency updates
  - Creates security alerts
- Update dependencies and support Python version
  - Aiming for simplicity, supporting only one Python release
- Remove SHM DC from Pulumi code
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1805)
  - This is unused now we have switched to Apricot
- Fix a broken GitHub action that updates Docker images
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1822)
- Add local DNS entry for Apricot server
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1821)
  - Allow Apricot to be referenced by URI not just IP address
- Fix Dependabot update logic
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1827)
  - Replace broken Dependabot logic with a GitHub Action


- Pulumi configuration changes
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1820)
  - Work has grown
  - More tidying where variables are stored
  - Decoupling Config and Context
  - The structure of the code should improve, less risk of circulate dependencies, less contrived logic
  - New base class for configuration synced to Azure storage
  - Separate base classes
    - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1840)
- Fix dependabot issues
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1827)
  - This wasn't correctly updating Python packages
- Fix automated Docker image update
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1822)
  - This was targeting the wrong branch
- Add local DNS record for the SRE identity server
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1821)
  - This makes it easier to manage private-IP changes from the Azure Container Instance
- Deployment co working
  - Drafting user instructions for deployment
  - Identifying bugs and improvements
  - PRs proposing bug fixes
  - New issues opened for later work



- Finishing pulumi persistent data split PR
- Improving package file structure PR
- Configuration rationalisation PR
- Examining testing framework 
- Test deployment and debugging of problems that arose
    - recursive attempts to login if subscription name incorrect in context file
    - issues with identity container group when deploying SRE
- Reviewing [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1847) for moving update servers to SRE
- https://github.com/alan-turing-institute/data-safe-haven/pull/1853
- Bug fix to remove circular dependency
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1853)
- File restructuring (stylistic)
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1848)
- Add tests for help function
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1855)
- Update and lint Caddyfiles
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1856)
- Bug fix to allow test suite to run
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1857)
- Drop unnecessary SHM dependence when provisioning SRE
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1858)
- Remove unused SHM data component
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1860)



- Fix identity server deployment
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1865)
- Fix deployment, sharing encrypted key between all pulumi projects 
  - This bug prevented the deployment of a TRE
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1854)
- Restructure CLI
  - Makes the user interface more consistent, easier for users to understand
  - Tidy directory structure for commands
    - More idiomatic user of the typer package, easier for developers to understand
  - [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1870)
- Working on adding maintenance scheduling for regular installation of Linux OS updates
    - [Draft PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1885)
- Working on documenting and standardising use of custom exceptions
    - [Draft PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1873)

###### February-March 2024


Over this period the story has not been prioritised instead focusing on identifying and scoping future work which will be a priority after v4.2.0 release.
The DSH code repo contains milestones that reflect related and planned issues (v5.x.y milestones) https://github.com/alan-turing-institute/data-safe-haven/milestones.

Additionally a first version of a project [roadmap](https://github.com/alan-turing-institute/data-safe-haven/blob/develop/ROADMAP.md) for DSH has been put in place.
This links to milestones but also records potential desired features that are not currently planned.
A roadmap provides value,

- For users, to understand and have confidence in upcoming features and how to influence development.
- For funders, to see the products longer term vision/strategy and as evidence of maturity and continuity.

### Information governance & standards

Infrastructure adhering to the latest agreed upon standard
Identifying, co-creating and supporting a TRE standard used across TRE infrastructures

#### SATRE: stakeholder engagement and community buy in [#66](https://github.com/alan-turing-institute/data-safe-haven-team/issues/66)

##### Goal

Ensure that institutions evaluate themselves against SATRE and that the momentum is maintained between funded phases

At the end of the funded phase of SATRE there was a growing community interest,
with institutions and stakeholders affirming they would evaluate themselves against it and contribute feedback.

Without ongoing resources the necessary support to ensure that happens cannot be provided and SATRE may end up not being adopted.

##### Definition of Done

There are a number of self evaluations completed,
there is feedback on the spec repository and, ideally, there is an active WG within the TRE Community continuing to work on it.

##### Progress

###### April-May 2024

###### February-March 2024


NHS-E R&D Programme Director stated during the UK TRE Community March event that SATRE has become the reference framework for TREs within the Subnational SDE programme,
placing SATRE as a key reference for what TREs are.
A recording of the event is available here https://youtu.be/KJVcy_ZKyVE?si=mbf64cZOLMHAxjwk and the notes of the day will be added to a report publicily available on the community website

We have also seen how institutions that already have other accreditations opt to self evaluate with SATRE because it is the only one specific to TREs.

SATRE has continued to attract the interest of the community,
with many attendees to its meeting wanting to be involved.

### Community building

Creating resources for all stakeholders (including members of the public) to engage in the TRE conversation
Creating and maintaining open and active communication spaces & workspaces (Slack, GH)
Identifying and documenting everything that can be openly documented

#### UK TRE Community leadership [#52](https://github.com/alan-turing-institute/data-safe-haven-team/issues/52)

Contributes to:

- Creating resources for all stakeholders (including citizens) to engage in the TRE conversation
- Creating and maintaining open and active communication spaces & workspaces (Slack, GH)

##### Goal

Provide a space for those involved in building, using and responsible for governance of TREs to discuss and recommend best practices.

- Host online working spaces, events and workshops to support the UK TRE Community
- Share best practices _e.g._ for making radiology data available for researchers
- Empower the community to help influence policy decisions

##### Progress

###### June 2024

- Quarterly event on 5th June: with 60 online participants the event had a keynote by Pete Barnsley on the Crick's TRE and also focused on Working Groups, marking the official community review for these and presenting them.
    - main hackmd with agenda for the day and notes is here https://hackmd.io/NE1-gvLtST6aJTdRzwL-gg
    - Github view for community review https://github.com/orgs/uk-tre/projects/1/views/7
- The other call to action during the event and recent focus is the preparation of the UKRI skills network grant. We asked for letters of support and involvement.
    - Deadline has been extended to 2 October, which might give us the opportunity to become formally involved


- Preparing 5 June event: agenda, community reminders, get prompts from speakers
- Update via web PR both agenda and working groups (old web) to offer a more comprehensive view of the current work and focus
- Weekly meeting an organisation
- Collate working groups information (charters) which is available here https://docs.google.com/document/d/1uvqALeVixK6PqdkzLFVwDVhc0fPUuBdddyfQzZsRtm4/edit?usp=sharing
- Cybersecurity risk WG now has a new repo

###### April-May 2024

- June 5 event organisation
- Running weekly meeting
- Work on Skills grant


- Processed expenses for Working Group day
- Weekly meeting
- June event organisation and list management
- Support Funding Working group set up (mail list, shared drive, documents)
- This is taking more RPM time than planned, natural due to transition phase (yesterday we were doing everything for the community), started to delegate back to other chairs/cmwg members

Held weekly meeting, coordinated Scriberia feedback with community and scriberia (lots of opinions!) and organised and announces WG day for the 29 April



    Prep for Working Groups day on 29/04
    Wrote up and finalised UK TRE Community WG report


- Prep for Working Groups meeting
    - Managing attendees
    - Preeping agenda/content
- Migrating to Hugo website
    - Adding all governance docs to site - [Issue](https://github.com/uk-tre/hugo-website/issues/17)

- UK TRE Community Working Groups Day!

- w/c 22 April: extensive time in preparing the [Working Groups day](https://hackmd.io/RtiQ_TH0THK0PQwnVXWzqg). Including registrations, materials (slide, agenda), travel approval for those who requested support, room booking and testing, catering order
- Working groups day event: full day on Monday (see agenda above) very well attended with minimal no shows (20 in person, 25 online). Several attendees were relatively new in the community and got directly involved, a new working group was created on Funding and Sustainability and the recent Cybersecurity WG defined.
    - very positive feedback from attendees
    - several requests for connections between members
    - All working groups advanced in their charters and plans
    - Department of Health & Social care Senior Policy Lead interested in Funding & Sustainability WG
    - Lesson: Pure proved a good provider for catering that can be ordered via credit card
    - Lesson: hybrid worked better via separate general discussion and by separating groups in different physical rooms each with joining a zoom breakout room. YET the online experience can be improved, something that has been suggested is to make everyone behave "as if online" which can be difficult in large discussion but could be encouraged in breakouts (add to facilitation tips/recommendations)
- With the event done, funding ended and our RAM gone the Community does enter into a new phase where numbers have grown and WGs started but no formal support is available for its management.

###### February-March 2024


Funded phase came to an end on 31 March,
along reporting,
it is necessary to organise and put together what we have produced but we have:

- Created a first version of all governance documents. Some will include pending conversations that may turn in the next version of those documents, for example the endorsement of outputs (v1 will only have community approval). This is the issue referencing to all documents https://github.com/orgs/uk-tre/projects/1/views/1?pane=issue&itemId=53738648
- Created a new website, not launched yet.
- Created a public community calendar, for "official" events and all those happening in the space and that people may want to include and promote.

We celebrated the March quarterly event with very positive feedback from participants.
Keynote was delivered by NHS England R&D programme Director on the subnational SDEs programme,
this followed a request by community members to know more about it during the December event.
Full notes can be found here while we produce a report https://hackmd.io/6t-s4x-wQN6riL6gPJLuWg

With funding ending we received a community request/push to ensure we put the workshop budget to good use. In response we elaborated two event proposals that align with the goal of this grant: finalising governance docs with the community participation and setting up WGs for success.

- Documentation sprints (https://hackmd.io/ty_bEhtBTrKjmYsJEEP8Qw). Held across several days on 29 February, 4 March and 5 March
- Working groups day (https://hackmd.io/nTAAo7fOT_quE18y0NYjnA). Which will be held on 29 April (This also implied figuring out a way to spend beyond March given it is not feasible to run the WGs day effectively before late April).

Lastly we have been working with Scriberia to use the remaining funding to produce an illustration that can represent the community in a number of ways.
The most immediate use will be for the production of physical stand up banners for events.
Due to timeline DSH will cover the actual banner while DARE funds have covered the illustration itself.

#### Communication and outreach [#35](https://github.com/alan-turing-institute/data-safe-haven-team/issues/35)

Contributes to:

- Creating and maintaining open and active communication spaces & workspaces (Slack, GH)
- Creating resources for all stakeholders (inc. Citizens) to engage in the TRE conversation

##### Goal

- Supporting the user community of the DSH codebase
- Publicising our work via blogposts, reports or papers
- Communicating our work through conference/workshop talks or posters

##### Progress

###### April-May 2024

- Drafting RSECon talk
  - [notes](https://hackmd.io/@nHslnPpLRmCxPOmQBcOW-g/BkMo-88WA/edit)
 
- Prepared and submitted [talk (45 min) for RSEcon24](https://hackmd.io/pVcsy89ZR7-MnRgJlgQ2pg) which will focus on discussing the balance between productivity and security and demonstrate our approach and experience. We differentiate ourselves in that we take a more pragmatic approach enabled by our security features and the fact environments are effectively isolated, reducing risk to specific environments
    - "we share the lessons of 6 years of working with over 50 data providers to support access to sensitive data for research under a flexible framework of information governance and technical controls."

###### February-March 2024


AI UK has been a priority for this story and the project.
Held on 19-20 March DSH had its own stand, through a likert scale exercise on TREs (and a bowl of sweets) we engaged attendees to introduce them to TREs and the work of the project which we stressed to be not only an open codebase but also the governance & standards and the community.

The stand was busy on the first day and quieter on the second, in part due to its location out of sight from the rest,
but that left time to properly engage in conversation with those who did (NHS England, Head of cyber-physical & digital twins at Innovate UK, Chief Exec of RSS).
Overall the impression of those there has been that there was important potential leads even if less conversations than last year,
we have added to our private sharepoint for follow up.

### TRESA

Over the year TRESA has increased its autonomy from the DSH research project,
in terms of work ownership and management.
Therefore, TRESA stories have not been independently updated and this section is an update on the service area as a whole.

This warrants updating and reviewing the stories we keep under the DSH roadmap, focusing on communicating with the service area rather than planning or prioritising for them.

#### TRESA team updates

#### Other TRESA related stories

(Stories and work directly impacting TRESA but still lead from the research project)

##### TRESA Costs and cost recovery [#36](https://github.com/alan-turing-institute/data-safe-haven-team/issues/36)

###### Goal

An agreed and formal process to recharge ATI projects being served by TRESA.

###### Progress

**April-May**

- Not worked on this despite priority (due to re-prioritisation of grant management)

- Met with finance to restart conversation, was asked to prepare a clear example with numbers. Will have a meeting with Fiona next week

**February-March**

TRESA has now its own code, people time has been changed in forecast to this code and Azure subscriptions associated to it (although currently covered by core).

Next step is to formalise the recharge process, projects engaging with TRESA have already been advised there will be a staff related cost in addittion to their specific subscription.


##### Review of requirements for security accreditation [37](https://github.com/alan-turing-institute/data-safe-haven-team/issues/37)

###### Goal

A clear list of requirements and necessary steps that DSH would need to take to be ISO027001 compliant.

This work will include pulling a list of requirements for the specification that includes a clear idea of the steps to take and the effort involved.

It also includes the work relating to DSPT certification: resubmitting and adapting answers if necessary.

###### Definition of Done

DSH remains DSPT compliant

There is a documented plan for DSH to be ISO027001 compliant.

###### Progress

###### June 2024

- Two sessions to review answers, resulting in most being checked and ready but also several actions identified as needed
    - For this submission: 
        - MRC courses required for all team members
        - Create unified list of project
        - Complete recovery plan
        - Test plan (this is actually only testing backup recovery rn)
    - For next year submission: actions identified that will be summarised to improve compliance
- see issue for more details: https://github.com/alan-turing-institute/trusted-research/issues/158#issuecomment-2135124214
    - Do we want an issue per action?


###### April-May 2024


- DSPT: meeting with Data Protection to review answers related to DP, 3 documents need put in place or updating (Spot check, training needs analysis, list of all project). [Details in issue](https://github.com/alan-turing-institute/trusted-research/issues/158)

###### February-March 2024


Revised DSPT v6 requirement, there being no effective changes for category 3 organisations (us).
Reviewed and copied last year answers for all mandatory requirements and made progress updating links and references (ongoing).
Held team meeting to review non mandatory requirements identifying a full list of them that could be positively answered.

Issue is [here](https://github.com/alan-turing-institute/trusted-research/issues/158#issuecomment-1965134444) and document with in progress submission can be found on TRESA sharepoint (private as it contains internal information).

### Project management and strategy

Work and stories that do not belong directly in any pillars but are necessary for all.

#### Project strategy and ways of working [#43](https://github.com/alan-turing-institute/data-safe-haven-team/issues/43)

##### Goal

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

##### Progress

###### April-May 2024


    Project progress and priorities report https://github.com/alan-turing-institute/data-safe-haven-team/pull/71
    Monthly agenda

Review Feb-Aug 2024 report

HARI HANDOVER (add docs and main bullets)
- Hari's handover session [notes](https://hackmd.io/@nHslnPpLRmCxPOmQBcOW-g/H1Y3vAlGR/edit)

###### February-March 2024


On 13 February the DSH had its second strategy session, based on last year's work it tried to define and prioritise specific work and activities for the project by creating milestones by project workstream.
While we discussed aspects of the Community workstream in depth there was no time for other workstreams.

Therefore the definition of milestones and their prioritisation needs to be continued and more effectively integrated into monthly discussions. A current priority once the FY has ended is to revisit ways of work and specifically roadmap management.

A first effort in that direction has been the creation of a first project report to be used to better communicate and discuss some elements of the monthly meeting, in this way it resembles more weeklies where the asynchronous elements help make better use of the meeting time.

As further improvement to ways of work a proposal on how to better engage with PIs was developed, but not yet discussed.

#### Contracts, legal and budget work [#53](https://github.com/alan-turing-institute/data-safe-haven-team/issues/53)

All work related to agreements, policies, expenses, contracts, budget.

##### Progress

###### April-May 2024

Wrote up and finalised UK TRE Community WG report

###### February-March 2024


Work has focused on managing UK TRE Community grant, which included ensuring actual allocation of costs to project and workign with DARE to agree on a reprofile that allowed us to use almost the totally of funds while delivering a final event past the grant end date.

Substantial work has also gone into aligning project actuals with Finance records for an appropriate management of internal and external Institute funds.

- Met with Finance to ensure project codes reflect invoicing to funder

- Prepared and completed [6 monthly Turing report](https://thealanturininstitute.sharepoint.com/:w:/s/rid/EQMRhhtbkLBOh7etA4dbg_QBu-Z8gDDAQFQ_82aEyhOCEA?e=MUeT7u)
- Included preparing a [funding summary](https://thealanturininstitute.sharepoint.com/:w:/s/rid/EWr9m2ZtPPdPr6R8DriAZdMBeGUqk6y9f35XtNNzBpFauw?e=bq2JVn)

- Some missalignment between project actuals as reported by us and the final numbers on Finance systems have required extensive revision. Sent a line by line analysis of staffing cost and a comparison between Finance record and actuals
    - No immediate consequence for team or project

#### [Manage grant opportunities and pipeline](https://github.com/alan-turing-institute/data-safe-haven-team/issues/51)

##### Goal

##### Progress

##### April-May 2024

- Co-working on proposal
- Grant reading and preparing DSH proposal

- Spent co-working discussing and prioritising grant to submit to, see notes LINK
- Grant planning and drafting
  - [notes](https://hackmd.io/@nHslnPpLRmCxPOmQBcOW-g/By6XSlGXC/edit)
- High level planning of next steps
- Target is currently both Biomedical and Skills grants, for two weeks we will "dream big" while RPM figures out practical steps

#### Promotion, opportunities and new work venues

##### Goal

##### Progress

##### June 2024

- [Conversation](https://thealanturininstitute.sharepoint.com/sites/SafeHaven/Shared%20Documents/External_engagement/University_of_Nottingham) with Philip Quinlan (Nottingham)
  - Use of DSH at Nottingham and East Midlands NHS SDE
  - Collaboration opportunities (TREFX)
  - User feedback, bug reports, feature requests
 
  
##### April-May 2024

NEW STORY!

    Send email to NHS England RAP Community of Practice
        sharepoint directory
        Proposing talking about areas where we can align to promote reproducibility in trusted research
        Signposting DSH, The Turing Way
    Further email to Sam Hollings (NHS-E)
        More signposting for The Turing Way
    ESRC initial catch-up
        Signposted to UK TRE Community and SATRE, no clear future next steps but was a productive chat!

- Engaging with Sam Hollings from NHS-E RAP CoP
  - [CRM](https://thealanturininstitute.sharepoint.com/:f:/s/SafeHaven/Ein6UMM7p_5HsdDCPf4qs6ABFTUWaDgZuFc72q-h2Z65WQ?e=7ZSh1G)
  - Joined TTW collab café
  - Talking about reproducibility, open source culture in the public sector, merging RAP CoP and TTW
  - Expressed that DSH would be interested in improving support for reproducible workflows in collaboration
- Prepared and delivered DSH presentation to Met Office

- Meeting OpenMined to find out morea bout their work and whether there's room for collab with us 

## Plans and priorities

This section contains project plans and priorities,
currently focusing on work to be done over the next month it should eventually encompass longer term plans.

### Blockers, challenges and other discussions

### July priorities

#### Manage codebase releases and testing #50

Similar to last month there is a bug that needs fixing and making an associated patch release, not made yet because focus on development but will happen.

Priority yes, not a lot of time spent on it.

We are in patch mode, doing what needs done but not focusing on new releases.

#### UK TRE Leadership #52

Continue to be a priority for @Davsarper, focusing on September event, skills grant and general community management. This comes at the expense of RPM time.

WARNING: August I cannot do much of this, we need to focus on project end.

#### Develop outside-run inside, RSEcon24

Absolute priority for development and the main focus of effort/people.

This new story will contain development efforts towards new features for ingressing code,
this will be more detailed in rc3 milestone (scoping in progress).

It will also refer to all necessary work to deliver the presentation at rsecon24

### May

- Long weekend did wonders but motivation last week was an issue (general state of affairs)
- So much to do for the Community, if this does not improve next week after June event I might ask for some help on it (Aida, Kirstie) and more "formally" take a step back myself


Not exactly a blocker but spent most time on non-prioritised stories (Grants & TRE Community)

- UK TRE Community is taking more RPM time than planned, natural due to transition phase (yesterday we were doing everything for the community), started to delegate back to other chairs/cmwg members. Hope to "solve" this in the short term (probably after 5 June event)


- Need some steer from PIs on grants.
  - What is our pitch?
  - _Who_ is writing the proposals?

### Monthly priorities: April

The list of priority stories can be found here https://github.com/orgs/alan-turing-institute/projects/111/views/11

#### Communication and outreach [35](https://github.com/alan-turing-institute/data-safe-haven-team/issues/35)

Follow up on conversations from AI UK to keep momentum going,
as resources are limited this month the work here should be to establish connections but any meetings or further work left for furhter ahead.

#### Project Strategy and Ways of work [43](https://github.com/alan-turing-institute/data-safe-haven-team/issues/43)

@davsarper keen to prioritise as possible to:

- Create due reports
- Revisit reports and monthlies format
- Propose and discuss PIs WoW

#### Manage codebase releases and testing [50](https://github.com/alan-turing-institute/data-safe-haven-team/issues/50)

This story was a March priority and the release completed,
with less time dedicated there will be follow up actions.
Including any fixes and also required communications about the release.

#### Identify and implement core IAC changes [28](https://github.com/alan-turing-institute/data-safe-haven-team/issues/28)

April work will focus on identifying and planning work within this story so it can be a top priority in May.

#### UK TRE Community [52](https://github.com/alan-turing-institute/data-safe-haven-team/issues/52)

Having finalised the funding phase there is three important things to do:

- Wrap up outputs, and celebrate WGs event
- Transition and knowledge transfer: ensure the community can continue delivering work

#### Manage grant opportunities and pipeline [51](https://github.com/alan-turing-institute/data-safe-haven-team/issues/51)

It is a priority to at least think and plan,
this story can be directly linked to PI work and how we better coordinate.
So not a high resources story but still very important one.

#### DSPT submission [37](https://github.com/alan-turing-institute/data-safe-haven-team/issues/37)

Finalise submission,
it should not require intensive effort but it will include revision by project PIs and possibly Data Protection (as Manager changed between submissions).

New non-mandatory requirements that can be easily completed will be (already identified).

#### TRESA costs and cost recovery [36](https://github.com/alan-turing-institute/data-safe-haven-team/issues/36)

While capacity is stretched with the new year we have to clarify recharges process and prepare for the announcement in May's catch up.

#### Not doing or prioritising

This month we are not leaving much out (please add anything you believe we should keep in mind),
with the new FY we are doing a bit everywhere in a month characterised by planning ahead.

### Next up: upcoming priorities and work the will be necessary

_under construction: please add anything relevant, with dates where possible_
