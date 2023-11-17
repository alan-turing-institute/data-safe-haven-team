# onBOARDing document: Issues, Milestones and Projects for the DSH team
Version: 1.0.0
This document lays out how to create and use this repo and associated project board for the tracking and organisation of work relating to DSH project, attending to its multi-repository nature.

The proposed structure responds to an ask from the project team to increase communication, organization and collaboration with the least possible amount of meeting time or fixed synchronous co-working time.

These Ways of Work are inspired by Agile principles and SCRUM methodology, although readers may recognize very little from the latter in the resulting practices. The main goals are to increase communication, ensure team members are directly involved in deciding how to carry out the project, protect their workloads and improve visibility of the project's impact.

They have been developed with the team. The meeting-intense research environment of the project made it challenging to introduce SCRUM ceremonies or make it mandatory for all team members to take part in each one. As a result, asynchronous reporting has been prioritised and some ceremonies blended together. To structure asynchronous elements of ceremonies or meetings we were directly inspired by Florian Haas' presentation ['No, we won't have a video call for that'](https://xahteiwi.eu/resources/presentations/no-we-wont-have-a-video-call-for-that/).

It is also important to understand that this is a multifaceted project. Several strands of work (or even full projects) are simultaneously carried out and have their own ways of work and tracking tools. Therefore the Ways of Work and tools developed here focus on coordination among those with minimal added effort and avoiding interfering with day-to-day work.

## Ways of work principles

Ways of work is not only about reporting.
It needs to help team members work better together and make their work visible.
The process should be adjusted if it does not do this.

The Ways of Work process should adhere to the following principles:

- You should only have to report in one place
- Reporting should not be an unreasonable burden
- What we collect must be useful and must not be busywork
  Ways this may be helpful could include
  - Preventing duplication of effort or clashing
  - Promoting collaborative work
  - Providing a place to ask for help or lend assistance
- Ways of work make work and workload visible
- Each role's responsibilities related to ways of work are clear
  - All team members
    - Report work, group work into stories, include links whenever possible
    - Report blockers and ask for help
    - Discuss and propose what to work on in the short term
    - Be aware of other team members' work
  - Project management
    - Process reports
    - Assess workload and prioritise effort
    - Produce necessary metrics
  - Project Leaders
    - Strategic level steering (in monthly meetings)
    - Ensure project continuity
      Using data gathered from reporting to create
      - Reports to funders and stakeholders
      - Applications for future funding

## Main elements

- Stories: issues reflecting the project strategic goals, planning and reporting is done based on them
- GH Project Roadmap and board: showing all stories by accountable team, when they are planned and their status
- Ceremonies: time spent together as a team for meetings and co-work

### Stories and other issues

```
Some details on how issues and stories are linked together will vary after GH releases Tracked & Tracked By and Tasklist features,
currently in private beta: 
https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields/about-tracks-and-tracked-by-fields
```

#### Story issues

Stories are only created in the management repo (data-safe-haven-team) and are "issues of issues",
they contain and reflect a 'Piece of Work' or goal agreed as necessary for the success of the project during an all-hands meeting or discussion (typically a Monthly meeting).
Stories will typically span longer than a month. Although they do not have a defined maximum duration, a useful reference may be a quarter (they can take longer but we may want to consider defining further intermediate goals). 

What stories to work on at any given time is decided during Planning meetings, it is also then when the effort they will require and what aspects of them to focus on are estimated. This planning and prioritisation is then brought to the Monthly meeting and shared with all stakeholders for their input.

Ideally there will be no work outside Stories. 
However, this is not realistic in the project context and some work may arise that does not fit with any defined story. 
This should be tracked to ensure non-story work is minimal and does not disrupt the delivery of the planned work.
If it becomes significant, then the whole project team and stakeholders should be made aware and agree how to reprioritise project work.

##### Content and project fields

In the body of the issue:
- The goal this story refers to
- What the work is and what it will achieve
- Define what would need to be achieved to consider the goals met, or the story as done
- Details:
  - RACI list, though Accountable is also captured in project fields it allows to reflect the whole list
  - Estimated effort, by team. Also duplicated in project fields for the Accountable team but allowing further detail in the body.
- Task and issue breakdown: all issues and important references for work done that contribute to this goal 
- Checklist

Issue fields:
- Assignees: include at least the main accountable person
- Labels: Story, always use this label as it used in the project board and roadmap to filter and distinguish issues from stories
  -  ForPrioritisation: always use this when you have created a story that still needs to be discussed and approved
  -  Funding/project: Core DSH (ELA), SATRE, TRESA
  -  Milestone: Choose a milestone by according to the time period when it should be addressed.
    -  No clear milestone?: It is okay, but please do mark its status in the project correctly. If the story is not approved it will have no status, if it has been approved to work on but not decided when then it will be part of the Backlog
  - Project: DSH unified board proposal
  
  Main project fields:
  - Status:
    - No Status: when you need to create the story but it has not yet been discussed and approved
    - Backlog: approved as necessary work for the project success, but no clarity on when to address
    - Planned: approved and planned, it has an associated milestone
  - Planned start and Planned End date: do fill when known
  - Actual start: currently unused but potentially useful in comparing plans with reality
  - FTE estimate: person time proportion that this story will take while active, minimum 0.05
  - Team Accountable: select the team
  - Project/Funding: select the funding source or subproject this story belongs to (repetitive but useful to fill in both)
  - Monthly FTE: Re-evaluated monthly it serves to plan the month ahead during monthly planning, rather than the overall effort it represents what the next month looks like. Also helps identify if the above needs reassessment
  Other project fields:
  - Iteration: no need to fill, it is there to experiment with effort tracking and analysis
  

##### Using stories

###### Story creation
Stories should not be created without consensus. 
If you DO need to create one to reflect a big piece of work you are definitely doing then add the tag 'ForPrioritisation' and take it to the team. 

To create a story, open an issue and select the Story template.
Provide a comprehensive title but especially include a comprehensive description of what the goal is and what work is required. 
Include any issues, milestones (from this repository or others) or relevant links to associated tasks and work whenever possible and sensible, the level of detail to linked work will vary with the nature of task and how they are currently tracked. 

Then fill in the project fields as best as possible:
- Project or funding it relates to
- Accountable team
- FTE estimate
- Status: if it has been discussed when the story will be addressed set it as 'Planned' or 'In Progress' otherwise set as 'Backlog'

It is the responsibility of the Accountable team or person, with help from the RPM where necessary, to create and complete a story.

###### Monthly planning

At the end of each month the team will use stories and roadmap to plan the coming month, assigning effort in FTE to each story under 'Monthly FTE'. 
This is the right time to update the scope of the story or associated work

**Progress reporting**
The Research Project Manager (RPM) will update at least monthly the main comment to reflect the progress and updates reported during weekly meetings.

Stories' status will then be updated accordingly to mark them as having updates, blockers, or requiring further discussion.
The RPM will later return them to their previous status (likely 'In progress').

During monthly review meeting the team will go through the stories and share updates based on what reporting is written on them.

#### Tasks and other issues from your day to day
Stories are intended to link and group to our day to day work, allowing reporting at a more aggregated level.
It is not required to create issues for every task but do so every time it is appropiatte.

Link issues, milestones or other documents and links to stories to which they contribute to.

Try to ask the following question each time you start a task: does it contribute to an ongoing or planned story?

##### I do not know what Story this issue belongs to, Should I create this issue?
All work and the related issues should clearly contribute to agreed upon goals, and their corresponding stories.
If you are unable to assign an issue to a story consider whether to create it in the first place,
if you think it is work that the project needs, add it for discussion during the next weekly meeting or open a thread in the corresponding channel.


If this happen regularly it should be addressed, either there is a deviation from plans and goals or these are loosing validity.
The next monthly meeting should be longer, at least two hours, and focused on the roadmap and project strategy rather than progress.

##### Do we need stories? Discussion point

Creating an issue of issue or meta issue may seem confusing, 
and some aspects of it may be (the importance of the label Story lies here, because the project views are configured to provide clarity based on it).
Yet they are necessary to keep an organised overview of goals and progress while:
- Allowing day to day issues to be created as it is best for the person, team or repo tackling them. This way we do not need to unify criteria, which may prove difficult when some tasks are very managerial/contractual and others are code
- Being able to assign team and people
- Reflect discussions and progress within
- Reflecting them in a roadmap

###### Why not milestones?

Milestones are much more information limited, cannot be shown in the same way in boards or roadmaps and are repository bound. In summary they are a deprecated feature that do not allow the analysis and tracking we require.



### Project: Unified board
The main tool for project tracking is a unified, multi-repository, GitHub project which contains a Project Roadmap and Board among other useful views.
While other tools roadmapping and tracking tools are avaialble, and other projects may prefer them, GitHub Projects has enough functionality and customization options while keeping all information in one single place.

Here is where all stories are reflected, broken down by accountable team and showing effort estimates and planned dates.
It also serves to quickly overview the status of stories and monthly priorities.

While orginally designed to also reflect all day-to-day issues and tasks this proved too burdensome for the team, as work at that level is already managed and tracked in more specific repositories.

This project is associated to the data-safe-haven-team repo, 
but is designed to reflect work across any number of (ATI or public) repositories.
To do this stories and project fields are key (we cannot modify labels or milestones in repositories we do not own, but can do what we want with project fields).

The main fields have been presented above but are further listed and explained here, they can be adapted and changed as the needs of the project changes.

- Status: Main way of tracking issues and stories progress
  - No Status: issues (of any kind) can be created at any moment if needed, but until they are agreed as necessary they should remain without status. It is important for effective coordination and resource management that nothing is added to Backlog, especially stories, until discussed.
  - Backlog: this will be the status for any agreed but unplanned work, task level issues will be easier to agree on but stories will need at least an all hands slack discussion and likely a monthly or strategy meeting.
  - Planned: issues will be here once they have a planned start date, end date or associated Milestone 
  - In Progress: issues we are actively working on
  - Blocked: stories that require help, or to elevate actions. Progress cannot be made
  - Updates: stories to present during the monthly review meeting but which do not require further action
  - For Discussion: stories that need to be brought to the attention of everyone including project leadership/stakeholders during the monthly review meeting
  - Done: over and done with, This will be used to periodically build the reports
- FTE estimate: overall effort from the Accountable team that we estimate the story to require in order to be complete
- Monthly FTE: Re-evaluated monthly it serves to plan the month ahead during monthly planning, rather than the overall effort it represents what the next month looks like. Also helps identify if the above needs reassessment
- Team Accountable: select the team who will lead for this goal or task, it is important to fill in because it allows to generate graphs and calculate effort by team
- Project/Funding: what is either the source of funding or the sub-project it belongs to?
- Planned start date and Planned end date: this are the dates that currently the roadmap shows, they are especially important for stories (so we do not spend too much time planning small tasks)
- Other fields: project fields are highly configurable, speak to you RPM and team to discuss any needs.

In any view changing the filters will allow you to quickly view issues and effort by team, subproject or time period. The Story label will allow to filter and distinguish between stories and the rest of issues.

#### Roadmap - Story

This is the main view for the long term vision and resource planning, 
by default it is organised by team accountable and shows only the stories each is accountable for and when they are planned for (Planned start date and Planned end date).

Dragging and dropping a story in the calendar will automatically fill in or modify the planned start and end.

#### Monthly Board

Overview of stories by status, this is the main view to be used during monthly review meetings.

#### Table

How to best use it will be discussed and developed together, no direct or immediate use yet (do suggest!)

#### Graphs
To be developed

### Milestones

Milestones allow to group issues of any kind and associate them to a specific delivery,
currently they have been created by quarter.

They are not heavily used yet as the information they offer is also contained via project fields (Planned end data + Team Accountable) yet they offer a good visual for the roadmap and allow to quickly track the progress (as completed issues out of milestone totals) of each time for a specific deadline.
There is room to improve their use if wanted.

In addition to the team's milestones there is an ongoing milestone (to the project's end) for meetings and other formalities that involve the whole team.

## Ceremonies: Meetings & Co-working

Synchronous meeting has been minimised according to team's preference and due to the already meeting intensive schedule,
therefore the focus is in maintaining up to date repositories and communicating in advance via written reports.

Meeting time should be focus on collaboration and group decisions.

### Weekly team meeting
Key facts

- Mondays 10.00 to 10.30
- Attended by Project working team
- Agenda:
  - Asynchronous items
    - What we've done this week
    - Things that are blocking me
    - Coworking session suggestions
  - Synchronous items
    - Identify blockers and arrange to solve. Do not spend time fixing problems in this meeting
    - Write plans for the week. Meeting organisers leads a group discussion on task prioritisation.

These meetings are the main way for the team to coordinate and structured around active stories,
they are attended by all team members accountable for carrying out the work to deliver the project.

Its asynchronous elements are as important as the actual meeting time and require everyone to update their issues and stories.
It is by filling the weekly meeting that team members report about their work, for this reason it is key to provide comprenhensive updates that the RPM can take to stories for reporting.
This way each team member needs to provide updates in a single place.


### Weekly coworking
Key facts


- Wednesdays 09.30 to 10.30
- Attended by Project working team
- Purpose: work together in issues identified during weekly or which arise during the week

Co-working time is an unstructured hour for synchronous work. It has proved 

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


#### Planning & Report (meeting outputs)

These issues will be primarly maintained by the RPM and be used to reflect the planned work and progress made either weekly, monthly or quarterly.
Monthly and quarterly issues will have associated PRs in which the team is expected to take part.

##### Weekly issue

The purpose of this issue is to better communicate and coordinate with DSH team members directly working on project tasks.

It should reflect what was done during the week, any blockers, and serve to plan work for the following week, minimising the need for synchronous meeting time

The RPM will be responsible to create and update it each week.
Everyone is responsible for updating issues worked on and planned and report in the collaborative notes here.

The issue will be permanent and updated via comments to avoid drowning the repo.
Meeting minutes will not be reflected here but stored in Sharepoint and as files in this repo. 
This issue will therefore only track status of issues so the PM can maintain the team's Project.

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

Potentially monthly issues will be reduced to their PR without creating an issue to keep the repo cleaner.


All attendees should make the time to read over the report and prepare their questions and feedback.

