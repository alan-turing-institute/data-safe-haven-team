# Data Safe Haven progress report October 2024 to March 2025

## Introduction

Creating file for 6 monthly report, associated to ELA phase closedown and final report of DSP as RPM.

This report will have up to two reporting formats in the same file,
the first one will follow internal Turing structure and is a necessary part of the formal closedown of this phase
as well as part of the RPM leaving exercise.

## Turing 6 monthly report format

### Key info

Title: Data Safe Havens

Investigators:

Martin O’Reilly (The Alan Turing Institute),
Kirstie Whitaker (The Alan Turing Institute),
James Robinson (The Alan Turing Institute),
Jim Madge (The Alan Turing Institute)

Funding:

SPF (ASG) Turing Institute Director’s Fund (Jun 2019 – Aug 2021),
Towards Turing 2.0 (Sept 2021 – Oct 2022),
Ecosystem Leadership Fund (Oct 2022 – Aug 2024),
DARE UK (Feb 2023 - Oct 2023),
DARE UK (Nov 2023 - March 2024),
DARE UK (Jan 2025 - Dec 2025).

| Nov 2018 – present | Project webpage

### Summary

Safe access to and productive use of sensitive data sets has been a long-standing challenge across academia,
government,
industry,
and the third sector.
This has been particularly highlighted with the critical role sensitive data has played in the UK and international pandemic response.

There is widespread recognition that access to data to support research and government decision making needs to be made easier.
However,
the reaction to the government’s recent proposal to share GP records more widely is also a reminder that retaining societal consent for the use of personal data is critical as we seek to make access to data more widespread.

Trustworthy Research Environments (TREs) such as the Data Safe Haven are a critical part of safely providing more widespread access to data and there has been much high profile activity in this area recently,
including the HDR UK work on standards for TREs and the Goldacre review into the use of health data,
with TREs even being mentioned in parliament by the health secretary.
This is a clear example of where we can engage with others to play a lead role in a national priority area.

Development of the Turing’s Safe Haven over the past 7 years has resulted in an open source,
re-usable platform that supports the deployment of secure,
scalable,
cloud-based secure research environments supporting a range of compute capability and the full suite of data science software and tooling required to do leading edge data science research securely and at scale.
Our platform has been deployed at multiple other organisations,
including Nottingham University and one of the NHS Sub-National Secure Data Environments (SN-SDEs).
The Turing’s own deployment of the platform has been compliant with the NHS Data Security Protection Toolkit (DSPT) for the past two years,
and further work is continuing to certify the system against other standards to enable its deployment at a wider range of partner organisations.

Recently the DSH has been awarded a grant to develop a new Kubernetes codebase,
the FRIDGE project will develop a new TRE based on the learning of DSH that can be deployed on any platforms and specifically targets High-Performance Computing Centres.
The team is working with both existign AIRR sites on its development.

On top of the technical development the project has led on establishing a vibrant UK Trusted Research Environment (TRE) Community with over 250 members,
and the development of the first TRE standards (SATRE - in collaboration with University of Dundee, UCL, Research Data Scotland and University of Ulster).
These standards are being progressively adopted across the community, including by NHS England as the basis for the standards for its 11 Secure Data Environments (SDEs).
The UK TRE Community has engaged enthusiastically with the development and adoption of the SATRE standards,
and a working group has been set up within the UK TRE Community to maintain momentum on this work.
It is anticipated that both the standards and community work Turing has been leading will be strong contenders for future funding from DARE as part of its Phase 2 work.

### Notable/substantive activity/outcomes in research progress

- Released [version 5.1 to 5.4.1](https://github.com/alan-turing-institute/data-safe-haven/releases).
- Pulumi based codebase (v5) is now the one in production and have been used in Data Study Groups and is supporting Turing projects (CVD-net).
- Conducted pen test of latest version in production.
- Updated production processes and approach towards DSPT acreditation, now including tier 2 within DSPT project as well as more flexibily including external researchers in project teams.

### Status of progress against goals/milestones, any blockers to progress

The Data Safe Haven team has succeded in producing an open source TRE that can be used by anyone while satisfying Turing needs for its own projects with sensitive data.
The project was launched after identifying a gap in the features of existing TRE that were too rigid for research project needs, the resulting codebase reflects the approach 'as secure as needed, as flexible as possible' towards which the TRE space is slowly shifting following the Data Safe Haven example.

The project is now closing formally as a research project but it has succesfully morfed into a permanent internal area of the Insittute,
now focused on support to other projects (production).
In this role the team has supported a 2-week online DSG in January which had 55 participants,
from 12 different countries.
The team has also deployed TREs for the project CVD-Net and support is embedded in the project to ensure Data Safe Haven continues to provide the necessary features.

The team has also prepared its self assessment for NHS's DSPT in advance of next submission, adapting its approach to be more flexible and include external researchers while maintaining security.

At the same time the team has secured funding to continue developing new iterations of open source TREs,
in particular the [FRIDGE project](https://www.turing.ac.uk/research/research-projects/fridge-federated-research-infrastructure-data-governance-extension) which was [awarded by DARE UK](https://dareuk.org.uk/news-and-events/dare-uk-launches-six-projects-to-support-early-adoption-of-new-capabilities-for-sensitive-data-research/) will develop a new platform agnostic TRE that targets High-Performance Computing Centres ([starting with AIRR sites](https://www.ukri.org/news/300-million-to-launch-first-phase-of-new-ai-research-resource/)) based on the learnings through the Data Safe Haven project lifecycle.

### Conference/workshop talks presented

The project Technical Lead Jim Madge [presented the data Safe Haven project](https://virtual.oxfordabstracts.com/event/49081/session/118339) during [RSEcon24](https://rsecon24.society-rse.org/) with a focus on its disctinctive security approach and how the codebase actualises it.

### Papers submitted or published

none

### Articles/blogs/press releases published

no update

### Software/code/tools/methods developed/released

The data Safe Haven team has made several releases, with v5.4.1 being the latest, over this period.
This reflects a lower time to release that is related with the merge between the production and development teams,
with releases reflecting requested and necessary changes for research project and Data Study Group teams.

Therefore these releases focus on improved usability for production teams (or TRE operators) as well as researchers.

A key highlight is that the new version of Data Safe Haven now minimises shared resources across projects,
this not only allows to track and allocate costs better but hugely decreases ongoing central costs.

- [See releases](https://github.com/alan-turing-institute/data-safe-haven/releases)

The FRIDGE project has created its repository and can be accessed [here](https://github.com/alan-turing-institute/fridge)

### New datasets created/accessed

No update/non applicable

### External engagement, influence, impact (Academic/ industry/ government/ public/ international)

The Data Safe Haven team has continued the support for the UK TRE Community which has held its annual conference as well as quarterly events for December and March,
on top of that the Community has run specialised events lead by Working Groups which is a highly positive sign of its activity and members involvement.
All events can be accessed through the [Community's page](https://www.uktre.org/en/latest/events/index.html), with links to presentations in [Zenodo](https://zenodo.org/communities/uktre/records?q=&l=list&p=1&s=10&sort=newest) and [recordings available on YouTube](https://www.youtube.com/channel/UCd7AZjyH33aCmIojGHMfqEg).

The SATRE specification continues to increase its impact, even without dedicated resources for its promotion:

- All Scottish safe havens/TREs are evaluating and comparing themselves using SATRE, as part of a Scottish federation project.
- The [DARE federation blueprint v2](https://zenodo.org/records/14192786) builds on it.
- In Europe the EOSC-ENTRUST have used SATRE and the DARE blueprint as the basis for [their own federation blueprint](https://zenodo.org/records/14362388).

 ### Funding: Further funding, leveraged funding/support, in-kind contributions
 
The [FRIDGE project](https://www.turing.ac.uk/research/research-projects/fridge-federated-research-infrastructure-data-governance-extension) which was [awarded by DARE UK](https://dareuk.org.uk/news-and-events/dare-uk-launches-six-projects-to-support-early-adoption-of-new-capabilities-for-sensitive-data-research/) will develop a new platform agnostic TRE that targets High-Performance Computing Centres ([starting with AIRR sites](https://www.ukri.org/news/300-million-to-launch-first-phase-of-new-ai-research-resource/)) based on the learnings through the Data Safe Haven project lifecycle.
The project has a budget of £500k and includes UCL as well as both AIRR sites, DAWN and ISAMBARDAI, as project partners with Turing as lead.

### Patents (drafted/applied for/granted)

no update

### Awards/recognition



