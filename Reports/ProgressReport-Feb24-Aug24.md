# Data Safe Haven project report

**Period: [February 2024-August 2024]**

This update: 8 April 2024

## Progress

This section contains a summary of progress across all stories in the [project roadmap](https://github.com/orgs/alan-turing-institute/projects/111/views/1).
It maps stories according to the (main) pillar and priority they contribute to.

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

Having completed development of v4.2.0 we prepared the release which included preparing a release branch and deployment in an environment for pen testing.

Extensive time was allocated to deploying and the errors/bugs that arose, as well as preparing for pen testing (this included deployment but also requesting specific tests like the removal of certain hardcoded IPs)

Pen testing was arranged and carried out, managing to spend within the 2023-2024 FY. iStorm kept better communications than last time and did not find concerning issues.
- @craddm would you add here a bit on the results?


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

Have worked on updating software used within SREs to ensure the security and functionality of the environment:
- Guacamole server updated [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1741)
- Nexus server updated [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1744)
- CodiMD server updated [PR](https://github.com/alan-turing-institute/data-safe-haven/pull/1743)

Added and tested a script to handle SAS access tokens renewal, currently expiring yearly. These are required manage access to data storage (and therefore ingress and egress). The relevant PR is here https://github.com/alan-turing-institute/data-safe-haven/pull/1739. In the process we realised SAS tokens are bound to Store Access Policies which could be modified to have no end date, we are currently considering the covenience of this approach versus potential security issues in https://github.com/alan-turing-institute/data-safe-haven/issues/1751 .

Improved use of hardcoded domain names and IPs. The hardcoded lists are difficult to maintain and are prone to going out of date, despite not fully fixing the use of these improvements have been made for the 4.2.0 release by relaxing rules where security allows. For this the team checked individuals cases and applied where possible, no security issues where found and we added this as a specific thing to pent test. Related PR is https://github.com/alan-turing-institute/data-safe-haven/pull/1745 and explanatory issue is https://github.com/alan-turing-institute/data-safe-haven/issues/1549 .

An issue with Jupyter notebooks not being able to use Python when launched from the menu was found, despite extensive work a fix was not found and decided to let it be by documenting the right workaround: launching Jupyter Notebooks from the terminal. The issue is https://github.com/alan-turing-institute/data-safe-haven/issues/1584 .

Worked on updating documentation to reflect Azure Active Directory name change to Microsoft Entra.


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

Over this period the story has not been prioritised/resourced as much, focusing on identifying and scoping future work which will be a priority after v4.2 release. The DSH code repo contains milestones that reflect related and planned issues (V5.x milestones) https://github.com/alan-turing-institute/data-safe-haven/milestones.

Additionally a first version of the codebase roadmap has been put in place, linking to milestone but also recording potential desired features that are not currently planned to implement. A roadmap is a desired/required document to have in place for software funding opportunities https://github.com/alan-turing-institute/data-safe-haven/blob/develop/ROADMAP.md.

### Information governance & standards
Infrastructure adhering to the latest agreed upon standard
Identifying, co-creating and supporting a TRE standard used across TRE infrastructures


#### SATRE: stakeholder engagement and community buy out [#66](https://github.com/alan-turing-institute/data-safe-haven-team/issues/66)

##### Goal

Ensure that institutions evaluate themselves against SATRE and that the momentum is maintained between funded phases

At the end of the funded phase of SATRE there was a growing community interest, with institutions and stakeholders affirming they would evaluate themselves against it and contribute feedback.

Without ongoing resources the necessary support to ensure that happens cannot be provided and SATRE may end up not being adopted.

##### Definition of Done

There are a number of self evlauaitons completed, there is feedback on the spec repository and, ideally, there is an active WG within the TRE Community continuing to work on it.

##### Progress

NHS-E R&D Programme Director stated that SATRE has become the reference framework for TREs within the Subnational SDE programme, placing SATRE as a key reference for what TREs are.

We have also seen how institutions that already have other accreditations opt to self evaluate with SATRE because it is the only one specific to TREs.

SATRE has continued to atract the interest of the community, with many attendees to its meeting wanting to be involved.


### Community building

Creating resources for all stakeholders (inc. members of the public) to engage in the TRE conversation
Creating and maintaining open and active communication spaces & workspaces (Slack, GH)
Identifying and documenting everything that can be openly documented


#### UK TRE Community leadership [#52](https://github.com/alan-turing-institute/data-safe-haven-team/issues/52)

Contributes to:
- Creating resources for all stakeholders (inc. Citizens) to engage in the TRE conversation
- Creating and maintaining open and active communication spaces & workspaces (Slack, GH)

##### Goal

Provide a space for those involved in building, using and responsible for governance of TREs to discuss and recommend best practices.
- Host online working spaces, events and workshops to support the UK TRE Community
- Share best practices i.e. for making radiology data available for researchers
- Empower the community to help influence policy decisions

##### Progress

Funded phase came to an end on 31 March, along reporting it is necessary to organise and put together what we have produced but we have:
- Created a first version of all governance documents. Some will include pending conversations that may turn in the next version of those documents, for example the endorsement of outputs (v1 will only have community approval). This is the issue referencing to all documents https://github.com/orgs/uk-tre/projects/1/views/1?pane=issue&itemId=53738648
- Created a new website, not launched yet.
- Created a public community calendar, for "official" events and all those happening in the space and that people may want to include and promote.

We celebrated the March quarterly event with very positive feedback from participants. Keynote was delivered by NHS England R&D programme Director on the subnaitonal SDEs programme, this followed a request by community members to know more about it during the December event. Full notes can be found here while we produce a report https://hackmd.io/6t-s4x-wQN6riL6gPJLuWg

With funding ending we received a community request/push to ensure we put the workshop budget to good use. In response we elaborated two events proposals that align with the goal of this grant: finalising governance docs with the community participation and set up WGs for success.
- Documentation sprints (https://hackmd.io/ty_bEhtBTrKjmYsJEEP8Qw)
- Working groups day (https://hackmd.io/nTAAo7fOT_quE18y0NYjnA). Which will be held on 29 April (This also implied figuring out a way to spend beyond March given it is not feasible to run the WGs day effectively before late April).

Lastly we have been workign with Scriberia to use the remaining funding to produce an illustration that can represent the community in a number of ways, the most immediate one being the production of physical stand up banners for events (due to timeline DSH will cover the actual banner while DARE funds have covered the illustration itself).


#### Communication and outreach [#35](https://github.com/alan-turing-institute/data-safe-haven-team/issues/35)

Contributes to:
- Creating and maintaining open and active communication spaces & workspaces (Slack, GH)
- Creating resources for all stakeholders (inc. Citizens) to engage in the TRE conversation

##### Goal

- Supporting the user community of the DSH codebase
- Publicising our work via blogposts, reports or papers
- Communicating our work through conference/workshop talks or posters 

##### Progress

AI UK has been a priority for this story and the project. Held on 19-20 March DSH had its own stand, through a likert scale exercise on TREs (and a bowl of sweets) we engaged attendees to introduce them to TREs and the work of the project which we stressed to be not only an open codebase but also the governance & standards and the community.

The stand was busy on the first day and quieter on the second, in part due to its location out of sight from the rest, but that left time to properly engage in conversation with those who did (NHS England, Head of cyber-physica & digital twins at Innovate UK, Chief Exec of RSS). Overall the impression of those there has been that there was important potential leads, we have added to our private sharepoint for follow up.  


### TRESA
Over the year TRESA have increased its autonomy from the DSH research project, in terms of work ownership and management.
Therefore TRESA stories have not been independently updated and it is more comprehensive to update on the service area as a whole.

This warrants updating and reviewing the stories we keep under the DSH roadmap, focusing on communicating with the service area rather than planning or prioritising for them.

#### TRESA team updates

#### Other TRESA related stories

(Stories and work directly impacting TRESA but still lead from the research project)

##### TRESA Costs and cost recovery [#36](https://github.com/alan-turing-institute/data-safe-haven-team/issues/36)

###### Goal

An agreed and formal process to recharge ATI projects being served by TRESA.

###### Progress

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

On 13 February the DSH had its second strategy session, based on last year's work it tried to define and prioritise specific work and activities for the project by creating milestones by project workstream. While we discussed aspects of the Community workstream in depth there was no time for other workstreams.

Therefore the definition of milestones and their prioritisation needs to be continued and more effectively integrated into monthly discussions. A current priority once the FY has ended is to revisit ways of work and specifically roadmap management.

A first effort in that direction has been the creation of a first project report to be used to better communicate and discuss some elements of the monthly meeting, in this way it resembles more weeklies where the asynchronous elements help make better use of the meeting time.

As further improvement to ways of work a proposal on how to better engage with PIs was developed, but not yet discussed.

#### Contracts, legal and budget work [#53](https://github.com/alan-turing-institute/data-safe-haven-team/issues/53)

All work related to agreements, policies, expenses, contracts, budget.

##### Progress

Work has focused on managing UK TRE Community grant, which included ensuring actual allocation of costs to project and workign with DARE to agree on a reprofile that allowed us to use almost the totally of funds while delivering a final event past the grant end date.

Substantial work has also gone into aligning project actuals with Finance records for an appropriate management of internal and external Institute funds.


## Plans and priorities

This section contains project plans and priorities , currently focusing on work to be done over the next month it should eventually encompass longer term plans.

### Monthly priorities: April

The list of priority stories can eb found here https://github.com/orgs/alan-turing-institute/projects/111/views/11

#### Communication and outreach [35](https://github.com/alan-turing-institute/data-safe-haven-team/issues/35) 

Follow up on conversations from AI UK to keep momentum going, as resources are limited this month the work here should be to establish connections buyt any meetings or further work left for furhter ahead.

#### Project Strategy and Ways of work [43](https://github.com/alan-turing-institute/data-safe-haven-team/issues/43)

@davsarper keen to prioritise as possible to:

- Create due reports
- Revisit reports and monthlies format
- Propose and discuss PIs WoW

#### Manage codebase releases adn testing [50](https://github.com/alan-turing-institute/data-safe-haven-team/issues/50)

This story was a March priority and the release completed, with less time dedicated there will be follow up actions. Including any fixes and also required communications about the release.

#### Identify and implement core IAC changes [28](https://github.com/alan-turing-institute/data-safe-haven-team/issues/28)

April work will focus on identifying and planning work within this story so it can be a top priority in May. 

#### UK TRE Community [52](https://github.com/alan-turing-institute/data-safe-haven-team/issues/52)

Having finalised the funding phase there is three important things to do:
- Wrap up outputs, and celebrate WGs event
- Transition and knowledge transfer: ensure the community can continue delivering work

#### Manage  grant opportunities and pipeline [51](https://github.com/alan-turing-institute/data-safe-haven-team/issues/51)

It is a priority to at least think and plan, this story can be directly linked to PI work and how we better coordinate. So not a high resources story but still very important one

#### DSPT submission [37](https://github.com/alan-turing-institute/data-safe-haven-team/issues/37)

Finalise submission, it should not require intensive effort but it will include revision by project PIs and possibly Data Protection (as Manager changed between submissions).

New non-mandatory requirements that can be easily completed will be (already identified).

#### TRESA costs and cost recovery [36](https://github.com/alan-turing-institute/data-safe-haven-team/issues/36)

While capacity is stretched with the new year we have to clarify recharges process and prepare for the announcement in May's catch up.

#### Not doing or prioritising

This month we are not leaving much out (please add anything you believe we should keep in mind), with the new FY we are doing a bit everywhere in a month characterised by planning ahead.

### Next up: upcoming priorities and work the will be necessary

*under construction: please add anything relevant, with dates where possible*
