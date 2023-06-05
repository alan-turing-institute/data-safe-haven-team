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

#### Story issues

Stories are only created in this repo (data-safe-haven-team) and are "issues of issues",
they contain and reflect a 'Piece of Work' or goal agreed as necessary for the success of the project during an all-hands meeting or discussion (typically a Monthly meeting).
Stories will typically span longer than a month, while they do not have a defined maximum duration an usefull reference may be a quarter (they can take longer but we may want to consider deifning further intermediate goals). 

Stories should not be created without consensus, if you DO NEED to create one to reflect a big piece of work you are for certain doing then add the tag 'ForPrioritisation' and take it to the team. 

It is the responsibility of the Accountable team or person, with help from the PM where necessary, to create and complete a story.

In the body of the issue:
- Specify the goal this story refers to
- Describe what the work is and what it will achieve
- Define what would need to be achieved to consider the goals met, or the story as done
- In details:
  - Complete the RACI list, a team or person should always be accountable (ensures the necessary work is done), often some other team or person will be responsible (has an active role in the success).
  - Add details of the estimated effort this will take (you can later updated it, even better if you come back to it after closing and reflect estimated vs actual effort it took)
- Task and issue breakdown, this is why stories exist please complete and keep up to date: add all issues across repositories that contribute to this goal 
- Checklist: it will take you through these same steps.

Issue and project fields:
- 


