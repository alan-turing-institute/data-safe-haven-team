# onBOARDing document: Issues, Milestones and Projects for the DSH team
V: Beta
This document lays out how to create and use this repo and associated project board for the tracking and organisation of work relating to DSH project, attending to its multi-repository nature.

The proposed structure responds to an ask from the project team to increase communication, organization and collaboration with the least possible amount of meeting time or fixed synchronous co-working time.

This is a first proposal so please do propose changes via PR.

## Main elements

### Issues
of which there are 3 types

```
Some details on how issues and stories are linked together will vary after GH releases Tracked & Tracked By and Tasklist features,
currently in private beta: 
https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields/about-tracks-and-tracked-by-fields
```


#### Tasks or standard issues
These are issues as normally used, they are created in their corresponding repository (most likely data-safe-haven, TRESA, SATRE, TPS PM or this same one).
When created in another repository try to still apply these rules as much as possible but do attend first to specific issue requirements present there. 

- Duration: strive to create issues that do not (or are not expected to) exceed a month, 
- Add to the Project [DSH unified board proposal](https://github.com/orgs/alan-turing-institute/projects/111) during creation or afterwards
- Mention in the body or comment the Story this issue contributes to if possible
- Create the issue
- Fill the following project fields via the dropdown menu (you can also go to the [project table view](https://github.com/orgs/alan-turing-institute/projects/111/views/3) for it)
  - Set Status:
    - No Status: if this issue has no clear Story and it has not being agreed as necessary
    - Backlog: if it has been agreed as necessary work
    - Planned: agreed and we know when to address it or by when it needs done 
  - Points (effort): assign a value effort from 2 to 9. A value of 1 typically means that the task is so short it would be better merged with another, a 10 means that it is probably best split in more than one issue (maybe it needs to be a story instead of an issue); if you really want to assign a 1 or 10 (cannot be merged or split) do so
  - FTE: estimate % of person time while ongoing this issue will take, for example 2 people dedicating 1 day a week, wiht an issue duration of a month would be about 0.26.
    - Important! Update this when closing
  - Add planned dates when known
  - Add actual dates when closing
  - Story Effort: leave blank, does not apply to base issues
  - Team Accountable: who is the momentum generator for this task?
  - Project/Funding: which project within DSH does this task belong to?

##### **I do not know what Story this issue belongs to**, Should I create this issue?**
All work and the related issue should clearly contribute to agreed upon goals, and their corresponding stories.
If you are unable to assign an issue to a story consider whether to create it in the first place,
if you think it is work that the project needs add it for discussion during the next weekly meeting or open a thread in the corresponding channel.

When the team agrees that it is indeed necessary create the issue, include the label 'For Prioritisation' (if created in this repository), add it to the project and do not set a status, never include it in Backlog, Planned or any other status at this stage.

During the next monthly meeting the whole team will discuss its prioritisation,
or review the project roadmap if it turns out it is not reflected the actual work being carried out or necessary for the project's success.

```
This situation may arise in the beginning, while we fully complete the roadmap and configure the repository, after that it should be rare.
```
If this happen regularly it should be addressed, either there is a deviation from plans and goals or these are loosing validity.
The next monthly meeting should be longer, at least two hours, and focused on the roadmap rather than progress.

At any given moment the number of active stories you are directly working on should be fairly limited, do not worry about having to keep many in mind to choose the right one (take it to the RPM otherwise and they will help out)

#### Story issues

Stories are only created in this repo (data-safe-haven-team) and are "issues of issues",
they contain and reflect a 'Piece of Work' or goal agreed as necessary for the success of the project during an all-hands meeting or discussion (typically a Monthly meeting).
Stories will typically span longer than a month, while they do not have a defined maximum duration an useful reference may be a quarter (they can take longer but we may want to consider defining further intermediate goals). 

Stories should not be created without consensus, if you DO NEED to create one to reflect a big piece of work you are for certain doing then add the tag 'ForPrioritisation' and take it to the team. 

It is the responsibility of the Accountable team or person, with help from the RPM where necessary, to create and complete a story.

Active stories are expected to be updated at least once a month via a comment on their progress

In the body of the issue:
- Specify the goal this story refers to
- Describe what the work is and what it will achieve
- Define what would need to be achieved to consider the goals met, or the story as done
- In details:
  - Complete the RACI list, a team or person should always be accountable (ensures the necessary work is done), often some other team or person will be responsible (has an active role in the success).
  - Add details of the estimated effort this will take (you can later updated it, even better if you come back to it after closing and reflect estimated vs actual effort it took)
- Task and issue breakdown, this is why stories exist please complete and keep up to date: add all issues across repositories that contribute to this goal 
- Checklist: it will take you through these same steps.

Issue fields:
- Assignees: include at least the main accountable person
- Labels: Story, always use this label as it used in the project board and roadmap to filter and distinguish issues from stories
  -  ForPrioritisation: use this always that you have created a story that still needs to be discussed and approved
  -  Funding/project: Core DSH (ELA), SATRE, TRESA
  -  Milestone: Choose a milestone by according to the time period when it should be addressed.
    -  No clear milestone?: It is okay, but please do mark its status in the project correctly. If the story is not approved it will have no status, if it has been approved to work on but not decided when then it will be 
  - Project: DSH unified board proposal
  
  Main project fields, strive to complete when creating:
  - Status:
    - No Status: when you need to create the story but it has not yet been discussed and approved
    - Backlog: approved as necessary work for the project success, but no clarity on when to address
    - Planned: approved and planned, it has an associated milestone
  - Planned start and Planned End date: do fill when known
  - FTE estimate: person time proportion that this story will take while active, minimum 0.05
  - Story effort: select if the overall effort is low, med or high (*the interval will change as become better at estimating effort)
  - Team Accountable: select the team
  - Project/Funding: select the funding source or subproject this story belongs to (repetitive but useful to fill in both)
  Other project fields:
  - Iteration: no need to fill
  - Points (effort): no need to fill
  - Actual start: Fill in (here or via boards) when you start working on this story (*this field and how to use it need revision*)
  - Actual end: add the date when closing the story, or report it closure so the RPM can add it (*to be revised, ideally to automate when closing*)

##### Do we need stories? Discussion point

Creating an issue of issue or meta issue may seem confusing, 
and some aspects of it may be (the importance of the label Story lies here, because the project views are configured to provide clarity based on it).
Yet they are necessary to keep an organised overview of goals and progress while:
- Allowing day to day issues to be created as it is best for the person, team or repo tackling them. This way we do not need to unify criteria, which may prove difficult when some tasks are very managerial/contractual and others are bugs
- Being able to assign team and people
- Reflect discussions and progress within
- Reflecting them in a roadmap

**Why not milestones?** Because they are much more information limited, cannot be shown in the same way in boards or roadmaps and are repository bound. In summary they are a deprecated feature that do not allow the analysis and tracking we require

#### Planning & Report (meeting outputs)

These issues will be primarly maintained by the RPM and be used to reflect the planned work and progress made either weekly, monthly or quarterly.
Monthly and quarterly issues will have associated PRs in which the team is expected to take part.

##### Weekly issue

Purpose of this issue is to better communicate and coordinate with DSH team members directly working on project tasks.

It should reflect what was done during the week, blockers and serve to plan work for the following week minimising the need for synchronous meeting time

RPM will be responsible to create and update it each week,
everyone is responsible to update issues worked on and planned and report in the collaborative note here

The issue will be permanent and updated via comments to avoid drowing the repo, meeting minutes will not be reflected here but stored in Sharepoint and as files in this repo. This issue will therefore only track status of issues so PM can maintian the team's Project.

From Thursdays and before the weekly meeting (Monday 10 AM) each team member will have to:
- Make updates in the issues they have worked on via comments
- Change their status in the project where appropiate
- Update fields where appropiate
- Fill in the meeting collaborative note here: https://hackmd.io/nPewceMuQcmXD7jfqYFpzw?edit

The weekly standup will then take place, discussing blockers and planning work.
Team members should update the collaborative note as appropiate to reflect plans for the week and any agreed actions

The RPM will:
- Update the weekly issue to reflect the team overall work for the last week and plans for this week
- Review roadmap and boards to ensure it reflects the current project status
- Add any necessary points for discussion for the monthly meeting

A member of the REG team will be asked to archive the meeting minute in the collaborative note in Sharepoint [here](https://thealanturininstitute.sharepoint.com/sites/SafeHaven/Shared%20Documents/Forms/AllItems.aspx?id=%2Fsites%2FSafeHaven%2FShared%20Documents%2FMeetings&viewid=10151919%2Deeef%2D4a8b%2Db4c0%2D26a3b155773b)

##### Monthly issue

The monthly issue will be used to update the [month by month report](https://github.com/alan-turing-institute/data-safe-haven-team/blob/main/Reports/Monthly.md),
as well as put together the agenda for the monthly meeting.

After the monthly meeting the RPM will reflect in the issue any necessary updates to roadmap, stories or issues.
It will allocate responsibility across teams to make those updates effective.

```
Potentially monthly issues will be reduced to their PR without creating an issue to keep the repo cleaner.

```

##### Open discussion

How to best use these issues is up for discussion,
they are necessary to better link directly to work done and so they can be part of the roadmap and be reflected as work (they represent a lot of what we do!),
but there is ample room for change as we use them.

### Project: Unified board proposal

This project is associated to the data-safe-haven-team repo, 
but is designed to reflect work across any number of (ATI or public) repositories.
To do this stories and project fields are key (we cannot modify labels or milestones in repositories we do not own, but can do what we want with project fields).

The main fields have been presented above but are further listed and explained here, they can be adapted and changed as the needs of the project changes.

- Status: Main way of tracking issues and stories progress
  - No Status: issues (of any kind) can be created at any moment if needed, but until they are agreed as necessary they should remain without status. It is important for effective coordination and resource management that nothing is added to Backlog, especially stories, until discussed.
  - Backlog: this will be the status for any agreed but unplanned work, task level issues will be easier to agree on but stories will need at least an all hands slack discussion and likely a monthly or strategy meeting.
  - Planned: issues will be here once they have a planned start date, end date or associated Milestone 
  - Todo-Monthly: issues planned for this month, will make the most sense for task level issues. Stories are likely to be best placed as In Progress as soon as their issues start to be worked on
  - In Progress: issues we are actively working on
  - For Review: Issues, specially stories, that have been completed and are ready to be presented as part of progress made before being closed. Not every issue will need to stop here before closing (Done), in particular task level issues are likely to be closed directly following your own criteria (still good to ask your team and tell about it in the weekly meeting)
  - Done: over and done with, This will be used to periodically build the reports
- Points (effort): currently only applies to task level issues, in a subjective way they measure effort for each task from 1 to 10. This allows each task in each repository to keep the format and form they need to have but unify at a team level what effort they entail, and therefore track total effort by team (this takes a wee while, as we collectively figure out what we can do in each period, but then is very effective)
  - Assigning effort: assign a value effort from 2 to 9. A value of 1 typically means that the task is so short it would be better merged with another, a 10 means that it is probably best split in more than one issue (maybe it needs to be a story instead of an issue); if you really want to assign a 1 or 10 (cannot be merged or split) do so.
- Story Effort: currently only applying to stories, simple effort scale for stories that will need to evolve sooner than later. It works to plan work and asses capacity, as an heuristic to start with no team should have more than 2 High effort and a Medium effort in any given quarter.
  - Assigning effort: High means it will for certain keep the team busy for a whole quarter (or we are quite uncertain on what needs done, figuring that out will take time), Medium means we are confident we can sccomplish the story well within the quarter and have clarity about it, Low is low hanging fruit that will be easily accomplished this quarter. As an heuristic you can consider that H=2M=4L
- Team Accountable: select the team who will lead for this goal or task, it is important to fill in because it allows to generate graphs and calculate effort by team
- Project/Funding: what is either the source of funding or the sub-project it belongs to?
- Planned start date and Planned end date: this are the dates that currently the roadmap shows, they are especially important for stories (so we do not spend too much time planning small tasks)
- Iteration: these are cycles of work currently configured to last for a month, they are most useful for task level issues, and allow the Roadmap-Tasks view to show tasks distributed in time without you having to exactly define dates. As you plan work for the week or month you can "drop" them in the corresponding iteration in the Roadmap-Tasks and move them as necessary
- Actual start and Actual end: this are to register when an issue is actually addressed and closed, subject to revision how to best use them or their utility
- Other fields: project fields are highly configurable, speak to you RPM and team to discuss any needs.

In any view changing the filters will allow you to quickly view issues and effort by team, subproject or time period. The Story label will allow to filter and distinguish between stories and the rest of issues.

#### Roadmap - Story

This is the main view for the long term vision and resource planning, 
by default it is organised by team accountable and shows only the stories each is accountable for and when they are planned for (Planned start date and Planned end date).

Dragging and dropping a story in the calendar will automatically fill in or modify the planned start and end.

Creating a new issue from this view will automatically have its accountable team filled.

#### Roadmap - Tasks

Similar to the above but representing only task level issues,
this view uses iterations as date fields instead of planned dates.

It allows to quickly view the total effort (as a sum of points) that each team has in their plate.

#### Board

Likely to be the most day to day view, it shows issues by status.
For simplicity only one view exists, where task level issues and stories cause confusion use the Story label to filter.
By default it is filtered to show only tasks.

What statuses to use and how can evolve with use, the most important rule to follow is to respect the backlog as agreed upon work.

It is recommended task issues are updated weekly.

#### Workload

A table view filtered so workload can be analysed,
by default grouped by Accountable Team and filtered by planned stories.

It shows the sum of current FTE.

#### Table

How to best use it will be discussed and developed together, no direct or immediate use yet (do suggest!)

#### Graphs
To be developed

### Milestones

Milestones allow to group issues of any kind and associate them to a specific delivery,
currently they have been created by quarter and end of exsitng funding/subproject.

They are not heavily used yet as the information they offer is also contained via project fields (Planned end data + Team Accountable) yet they offer a good visual for the roadmap and allow to quickly track the progress (as completed issues out of milestone totals) of each time for a specific deadline.
There is room to improve their use if wanted.

In addition to the team's milestones there is an ongoing milestone (to the project's end) for meetings and other formalities that involve the whole team.

## Meetings & Co-working

Synchronous meeting has been minimised according to team's preference and due to the already meeting intensive schedule,
therefore the focus is in maintaining up to date repositories and communicating in advance via written reports.

Meeting time should be focus on collaboration and group decisions.

### Weekly meeting
Key facts
- Mondays 10.00 to 10.30
- Attended by Project working team
- Purpose:
  - communicate work done and plans (Async)
  - address blockers
  - plan the week and co-working time
  - (If needed) reasign work
  - (If needed) Contribute discussion points for Monthly meeting, or elevate decisions

These meetings are the main way for the team to coordinate,
they are attended by all team members accountable for carrying out the work to deliver the project.

It's asynchronous elements are as important as the actual meeting time and require everyone to update their issues and stories.

The weekly meeting is the time to discuss and agree any new work or reprioritise existing work.
This is not expected to happen each week,
yet it is likely that after monthly meetings or main milestones (quarters, end of funding) this becomes the focus of the meeting.
It is during this meeting that any inclussion of issues in the backlog is discussed (and elevated to the Monthly when necessary), 
and when issues are taken from the backlog into planned work.

### Weekly coworking
Key facts
- Wednesdays 09.30 to 10.30
- Attended by Project working team
- Purpose: work together in issues identified during weekly

Co-working time is an unstructured hour for synchronous work

### Monthly meeting
Key facts
- Second Monday of the month 13.00 to 14.00
- Attended by whole DSH members and invited stakeholders
- Purpose:
  - Show progress and work
  - Receive feedback and approve deliverables
  - Address project blockers
  - Reprioritise goals (stories) and review roadmap
  - Approve changes to the Backlog
 
Meeting structure:
- Update Report Pull Request (Async)
- RPM: welcome and agenda
- RPM: Project updates at a glance
- Accountable teams:
  - REG update, including issues for discussion (blockers, backlog, roadmap changes)
  - RAM update, including issues for discussion (blockers, backlog, roadmap changes) 
  - RCM update, including issues for discussion (blockers, backlog, roadmap changes)
  - RPM update, including issues for discussion (blockers, backlog, roadmap changes)
- PI and stakeholders: feedback
- All: Decision and actions for Blockers, backlog, roadmap

This meeting is how we communicate work and make any decisions regarding the overall goals of the project,
it is the time to elevate blockers or important changes to the roadmap or backlog (any inclussion of a story issue should be addressed and discussed).

As with weeklys and to make use of the synchronous times this meetings have a strong asynchronous component,
each team will update their stories and make changes to a monthly report PR that the RPM will prepare in advance.

All attendees should make the time to read over the report and prepare their questions and feedback.

