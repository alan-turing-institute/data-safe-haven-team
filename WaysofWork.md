# onBOARDing document: Issues, Milestones and Projects for the DSH team
V: Beta
This document lays out how to create and use this repo and associated project board for the tracking and organisation of work relating to DSH project, attending to its multi-repository nature.

The proposed structure responds to an ask from the project team to increase communicaiton, organizaiton and collaboration with the least possible ammount of meeting time or fixed synchronous co-working time.

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
  - Points (effort): assign a value effort from 2 to 9. A value of 1 typically means that the task is so short it would be better merged with another, a 10 means that it is probably best split in more than one issue (maybe it needs to be a story instead of an issue); if you really want to assing a 1 or 10 (cannot be merged or split) do so
  - Add planned dates when known
  - Story Effort: leave blank, does not apply to base issues
  - Team Accountable: who is the momentum generator for this task?
  - Project/Funding: which project within DSH does this task belong to?

##### I do not know what Story this issue belongs to
**Should you create this issue?**
All work and the related issue should clearly contribute to agreed upon goals, and their corresponding stories.
If you are unable to assign an issue to a story consider whether to create it in the first place,
if you think it is work that the project needs add it for discussion during the next weekly meeting or open a thread in the corresponding channel.

When the team agrees that it is indeed necessary create the issue, include the label 'For Prioritisation' (if created in this repository), add it to the project and do not set a status, never include it in Backlog, Planned or any other status at this stage.

During the next monthly meeting the whole team will discuss its prioritisation,
or review the project roadmap if it turns out it is not reflected the actual work being carried out or necessary for the project's success.

```
This situation may arise in the begining, while we fully complete the roadmap and configure the repository, after that it should be rare.
```
If this happen regularly it should be addressed, either there is a deviation from plans and goals or these are loosing validity.
The next monthly meeting should be longer, at least two hours, and focused on the roadmap rather than progress.

At any given moment the number of active stories you are directly working on should be farily limitted, do not worry about having to keep many in mind to choose the right one (take it to the RPM otherwise and they will help out)

#### Story issues

Stories are only created in this repo (data-safe-haven-team) and are "issues of issues",
they contain and reflect a 'Piece of Work' or goal agreed as necessary for the success of the project during an all-hands meeting or discussion (typically a Monthly meeting).
Stories will typically span longer than a month, while they do not have a defined maximum duration an usefull reference may be a quarter (they can take longer but we may want to consider deifning further intermediate goals). 

Stories should not be created without consensus, if you DO NEED to create one to reflect a big piece of work you are for certain doing then add the tag 'ForPrioritisation' and take it to the team. 

It is the responsibility of the Accountable team or person, with help from the RPM where necessary, to create and complete a story.

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
- Labels: Story, always use this label as it used in the project board and roadmao to filter and distinguish issues from stories
  -  ForPrioritisation: use this always that you have created a story that still needs to be discussed and approved
  -  Funding/project: Core DSH (ELA), SATRE, TRESA
  -  Milestone: Choose a milestone by typing the team accountable and then selecting the time period when it should be addressed.
    -  No clear milestone?: It is okay, but please do mark its status in the project correctly. If the story is not approved it will have no status, if it has been approved to work on but not decided when then it will be 
  - Project: DSH unified board proposal
  
  Main project fields, strive to complete when creating:
  - Status:
    - No Status: when you need to create the story but it has not yet been discussed and approved
    - Backlog: approved as necessary work for the project success, but no clarity on when to address
    - Planned: approved and planned, it has an associated milestone
  - Story effort: select if the overall effort is low, med or high (*the interval will change as become better at stimating effort)
  - Team Accountable: select the team
  - Project/Funding: select the funding source or subproject this story belongs to (repetitive but useful to fill in both)
  Other project fields:
  - Iteration: no need to fill
  - Points (effort): no need to fill
  - Planned start and Planned End date: do fill when known
  - Actual start: Fill in (here or via boards) when you start working on this story (*this field and how to use it need revision*)
  - Actual end: add the date when closing the story, or report it closure so the RPM can add it (*to be revised, ideally to automate when closing*)

##### Do we need stories? Discussion point

Creating an issue of issue or meta issue may seem confusing, 
and some aspects of it may be (the importance of the label Story lies here, because the project views are configured to provide clarity based on it).
Yet they are necessary to keep an organised overview of goals and progress while:
- Allowing day to day issues to be created as it is best for the person, team or repo taclking them. This way we do not need to unify criteria, which may prove difficult when some tasks are very managerial/contractual and others are bugs
- Being able to assign team and people
- Reflect discussions and progress within
- Reflecting them in a roadmap

**Why not milestones?** Because they are much more information limited, cannot be shown in the same way in boards or roadmaps and are repository bound.

#### Planning & Report (meeting outputs)

These issues will be primarly maintained by the RPM and be used to reflect the planned work and progress made either weekly, monthly or quarterly.
Monthly and quarterly issues will have associated PRs in which the team is expected to take part.

##### Weekly issue

This will be used to reflect issues where progress was made or blockers arose during the previous week and track issues or work planned for the week.
They will open on Thursdays and close the following Friday (*automation pending*).

From Thursdays and before the weekly meeting (Monday 10 AM) each team member will have to:
- Make updates in the issues they have worked on via comments
- Change their status in the project where appropiatte
- Update fields where appropiatte
- Fill in the meeting collaborative note here: https://hackmd.io/3KNjlfj-Sn-giEk8DOnqyA

The weekly standup will then take place, discussing blockers and planning work.
Team members should update the collaborative note as appropiatte to reflect plans for the week and any agreed actions

The RPM will:
- Update the weekly issue body to reflect the team overall work for the last week and plans for this week
- Review roadmap and boards to ensure it reflects the current project status
- Add any necessary points for discussion for the monthly meeting

A member of the REG team will be asked to archive the meeting minute in the collaborative note in Sharepoint [here](https://thealanturininstitute.sharepoint.com/sites/SafeHaven/Shared%20Documents/Forms/AllItems.aspx?id=%2Fsites%2FSafeHaven%2FShared%20Documents%2FMeetings&viewid=10151919%2Deeef%2D4a8b%2Db4c0%2D26a3b155773b)

##### Monthly issue (WIP)

The monthly issue will be used to update the [month by month report](https://github.com/alan-turing-institute/data-safe-haven-team/blob/main/Reports/Monthly.md),
as well as put together the agenda for the monthly meeting.

After the monthly meeting the RPM will reflect in the issue any necessary updates to roadmap, stories or issues.
It will allocate responsibility across teams to make those updates effective.

##### Open discussion

How to best use these issues is up for discussion,
they are necessary to better link directly to work done and so they can be part of the roadmap and be reflected as work (they represent a lot of what we do!),
but there is ample room for change as we use them.

### Project: Unified board proposal

This project is associated to the data-safe-haven-team repo, 
but is designed to reflect work across any number of (ATI or public) repositories.
To do this stories and project fields are key (we cannot modify labels or milestones in repositories we do not own, but can do what we want with project fields).

The main fields have been presented above but are furhter listed and explained here, they can be adapted and changed as the needs of the porject changes.

- Status: Main way of tracking issues and stories progress
  - No Status: issues (of any kind) can be created at any moment if needed, but until they are agreed as necessary they should remain without status. It is important for effective coordination and resource management that nothing is added to Backlog, especially stories, until discussed.
  - Backlog: this will be the status for any agreed but unplanned work, task level issues will be easier to agree on but stories will need at least an all hands slack discussion and likely a monthly or strategy meeting.
  - Planned: issues will be here once they have a planned start date, end date or associated Milestone 
  - Todo-Monthly: issues planned for this month, will make the most sense for task level issues. Stories are likely to be best placed as In Progress as soon as their issues start to be worked on
  - In Progress: issues we are actively working on
  - For Review: Issues, specially stories, that have been completed and are ready to be presented as part of progress made before being closed. Not every issue will need to stop here before closing (Done), in particular task level issues are likely to be closed directly following your own criteria (still good to ask your team and tell about it in the weekly meeting)
  - Done: over and done with, This will be used to periodically build the reports
- Points (effort): currently only applies to task level issues, in a subjective way they measure effort for each task from 1 to 10. This allows each task in each repository to keep the format and form they need to have but unify at a team level what effort they entail, and therefore track total effort by team (this takes a wee while, as we collectively figure out what we can do in each period, but then is very effective)
  - Assigning effort: assign a value effort from 2 to 9. A value of 1 typically means that the task is so short it would be better merged with another, a 10 means that it is probably best split in more than one issue (maybe it needs to be a story instead of an issue); if you really want to assing a 1 or 10 (cannot be merged or split) do so.
- Story Effort: currently only applying to stories, simple effort scale for stories that will need to evolve sooner than later. It works to plan work and asses capacity, as an heuristic to start with no team should have more than 2 High effort and a Medium effort in any given quarter.
  - Assigning effort: High means it will for certain keep the team busy for a whole quarter (or we are quite uncertain on what needs done, figuring that out will take time), Medium means we are confident we cana ccomplish the story well within the quarter and have clarity about it, Low is low hanging fruit that will be easily accomplished this quarter. As an heuristic you can consider that H=2M=4L
- Team Accountable: select the team who will lead for this goal or task, it is important to fill in because it allows to generate graphs and calculate effort by team
- Project/Funding: what is either the source of funding or the sub-project it belongs to?
- Planned start date and Planned end date: this are the dates that currently the roadmap shows, they are especially important for stories (so we do not spend too much time planning small tasks)
- Iteration: these are cycles of work currently configured to last for a month, they are most useful for task level issues, and allow the Roadmap-Tasks view to show tasks distrubuted in time without you having to exactly define dates. As you plan work for the week or month you can "drop" them in the corresponding iteration in the Roadmap-Tasks and move them as necessary
- Actual start and Actual end: this are to register when an issue is actually addressed and closed, subject to revision how to best use them or their utility
- Other fields: project fields are highly configurable, speak to you RPM and team to discuss any needs.

#### Roadmap - Story

#### Roadmap - Tasks

#### Board

#### Table


