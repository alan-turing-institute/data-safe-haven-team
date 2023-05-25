# Data Safe Haven team repo

This is a project management repo for the Data Safe Havens in the Cloud team at The Alan Turing Institute. Learn more about the project [here](https://www.turing.ac.uk/research/research-projects/data-safe-havens-cloud).

## README Contents

- [Useful links](#useful-links)
- [New starters checklist](#new-starters-checklist)
    - [First steps](#first-steps-for-all-starters)
    - [Developer steps](#next-steps-for-developers)
- [Contacts](#contacts)

## Useful links

### Data Safe Haven Project

- [DSH repo](https://github.com/alan-turing-institute/data-safe-haven) (public) which hosts the open source codebase (and the docs code)
- [DSH docs](https://data-safe-haven.readthedocs.io/en/develop/index.html) (public) which includes user and deployment documentation
- [DSH team repo (this repo)](https://github.com/alan-turing-institute/data-safe-haven-team) (public) used for team mangement and issues not related to the codebase
- [DSH Team project board](https://github.com/orgs/alan-turing-institute/projects/40/views/1) (private) where the the issues from the above repos that the team intend to work on are organised
- [Turing DSH Sharepoint link](https://thealanturininstitute.sharepoint.com/sites/SafeHaven) (private)

### Trusted Research Environments Service Area (TRESA)

- [Turing TRE docs](https://alan-turing-institute.github.io/trusted-research/) (public) which contains all the information on processes for managing "production" instances of DSH at Turing and the relevant people and tasks
- [Trusted research repo](https://github.com/alan-turing-institute/trusted-research) (private) which contains the code for the Turing TRE docs and issues for the 2 project boards below
- [TRESA - SRE board](https://github.com/orgs/alan-turing-institute/projects/25/views/1?layout=board) (private) which contains info of all the current/future/past SRE deployments at Turing under the production (prod4) SHM
- [TRESA management board](https://github.com/orgs/alan-turing-institute/projects/52/views/1?layout=board) (private) which is for managing service area general issues

### Standardised Architecture for Trusted Research Environments (SATRE)

- [SATRE proposal](https://thealanturininstitute.sharepoint.com/sites/SafeHaven/Shared%20Documents/Forms/AllItems.aspx?id=%2Fsites%2FSafeHaven%2FShared%20Documents%2FExternal%20Funding%20Applications%2F2%2E0%20Applications%20%2D%20Other%20org%20as%20lead%2FDARE%20Phase%201b%2F2022%2D12%2D14%20SATRE%20Proposal%2Epdf&viewid=10151919%2Deeef%2D4a8b%2Db4c0%2D26a3b155773b&parent=%2Fsites%2FSafeHaven%2FShared%20Documents%2FExternal%20Funding%20Applications%2F2%2E0%20Applications%20%2D%20Other%20org%20as%20lead%2FDARE%20Phase%201b) (private) link to proposal doc in DSH sharepoint
- [SA-TRE](https://github.com/sa-tre) (public) GitHub org
- [SATRE team repo](https://github.com/sa-tre/satre-team) (public) project management repo
- [SATRE spec doc repo](https://github.com/sa-tre/satre-specification) (public) repo used for hosting/writing the specification doc/ reference architecture (work package 1)
- [SATRE backlog board](https://github.com/orgs/sa-tre/projects/1) (public) for managing issues from the above repos


## New starters checklist

Welcome to the Data Safe Haven team! 🎉

You should read this page and follow the instructions if you're joining the project for the first time at The Alan Turing Institute.

### First steps for *all starters*

1. **Bookmark** this page and the other [useful links](#useful-links) above
2. **Read up:** On the [documentation site](https://data-safe-haven.readthedocs.io/en/develop/index.html), click the `Overview` tab, where you will find links to resources that explain what Data Safe Haven is and why someone would want to use it.
    - In particular, it's worth studying the [diagram](https://figshare.com/articles/poster/Data_Safe_Havens_in_the_Cloud/11815224) which displays the overall architecture of DSH, including the distinction between the Safe Haven Management (SHM) and Secure Research Environments (SREs) and the data classification system.
3. **Access:** We have internal discussions about the project via Slack and manage our work via a combination of GitHub and Microsoft Sharepoint:
    - **Slack:** Ensure you have access to the Alan Turing Institute Slack workspace and join the following channels: `#data-safe-haven` and `#data-safe-haven-team` (the latter is private and you may need to request a team member to add you, see [contacts](#contacts)).
    - **Slack:** You can also join the external-facing Slack workspace called `Turing Data Safe Haven`, used for release announcements and other communications with the community of DSH users. Ask a team member to add you (see [contacts](#contacts)).
    - **Sharepoint:** Internal documents are stored on [sharepoint](https://thealanturininstitute.sharepoint.com/sites/SafeHaven). You will need to have your Turing SSO set up. Ask a team member to add you to the group with access rights (see [contacts](#contacts)).
    - **GitHub:** We use a GitHub [project board](https://github.com/orgs/alan-turing-institute/projects/40/views/1) to manage who is working on what. [Familiarise yourself](https://docs.github.com/en/github-ae@latest/issues/organizing-your-work-with-project-boards/managing-project-boards/about-project-boards) if you haven't used one before and check you can add issues to the `data-safe-haven-team` or `data-safe-haven` repos from the project board view.
4. **Explore:** Ask one of the existing Data Safe Haven team (see [contacts](#contacts)) to create a non-privileged user account in the test SRE called `sandbox`, so you can log in explore it from a user perspective and familiarise yourself with how it works. This is available at https://sandbox.prod4.turingsafehaven.ac.uk/

### Next steps for *developers*

1. **Deploy:** The best way to familiarise yourself with the codebase is to have a go at deploying either an SRE to an existing SHM, or if time permits, a new SHM and attached SRE. Click on the `Deployment` tab in the [DSH documentation](https://alan-turing-institute.github.io/data-safe-haven/) and follow the guides available there. Either choose the latest release docs or try `develop` if you're feeling adventurous!
    - Note: When you're done with any test SHM/SREs, you should follow the "Tear down" instructions in the respective guides.
2. **Open issues:** If you notice any bugs in the Safe Haven code when deploying an SHM or SRE, open an issue [on the main repo](https://github.com/alan-turing-institute/data-safe-haven/issues). Take care to follow the issue template.
3. **Contribute code:** If you want to contribute changes to the code base, perhaps to fix an issue that you have identified during deployment, create a fork of the main repository on your personal Github account, modify the relevant code on your fork, and then create a [pull request](https://github.com/alan-turing-institute/data-safe-haven/pulls).

## Contacts

The DSH team includes a longer list of people at The Alan Turing Institute, but the people you should contact with queries about the information in this README are as follows:

- James Robinson
- Jim Madge
- Ed Chalstrey
- Matt Craddock

Turing new starters with a `@turing.ac.uk` email should be able to find the email addresses of the above via Microsoft Outlook, if they have any queries.
