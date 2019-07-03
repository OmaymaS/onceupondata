---
title: 'The Reporting/Dashboarding Dilemma!'
subtitle: 'Data scientists and dashboards: a complicated relationship'
date: '2019-07-03'
slug: dashboards-dilemma
categories: []
tags: [dashboards, data science]

---


A couple of weeks ago I read a discussion on twitter initiated by a tweet from [David Neuzerling](https://twitter.com/mdneuzerling) who highlighted an observation about data science teams being pushed towards reporting/dashboarding inside organizations. 

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Observation: any data science team will always face pressure from within an organisation to become a reporting/dashboarding team.</p>&mdash; David Neuzerling (@mdneuzerling) <a href="https://twitter.com/mdneuzerling/status/1141202330349555713?ref_src=twsrc%5Etfw">June 19, 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


I had some reflections from a previous experience and various discussions so I thought about gathering them in a blog post for future reference and further discussions. 

**In this post, I will discuss the dynamics of this pressure, how it affects the newly hired data scientists as well as the team leader, what are the common arguments in this context and more.**


### Why do companies hire data science teams in the first place?

The obvious answer is because they need them; they have data to extract value from, support their decisions, build data products, etc. They have a plan and they need data scientists to work on and implement solutions. **But Surprise Surprise**, many companies do not really know whether it is the best time to hire data scientists or not, they don't have a good infrastructure, they don't have a plan to support the first data scientist/s to build their data culture. Some could just have some scattered data-related work that they want to centralize. Others might think that the first data scientist would be the magician who would transform their organization and help them check the "data-driven" box. 

The two types exist; companies who have a vision about forming a data science team and others who have no clue. And one can detect this from the early conversations with recruiters and hiring managers. But in both cases it is possible that the data science team gets pushed in a certain direction while growing in the first months/year. 

### Why do some teams get pushed towards reporting/dashboarding?

In his thread, [David Neuzerling](https://twitter.com/mdneuzerling) provided some reasonable points about why a team might face a pressure to work more on reporting/dashboarding.

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">This is because:<br>- reports are easily understood compared to machine learning<br>- the (perceived) value of reports comes very quickly<br>- the easiest way to deal with a request for a report is to just do it<br>- assertion skills are rare: most people prefer to &quot;prioritise&quot; than say no</p>&mdash; David Neuzerling (@mdneuzerling) <a href="https://twitter.com/mdneuzerling/status/1141202357390196736?ref_src=twsrc%5Etfw">June 19, 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

I personally believe the teams that are more susceptible to this pressure are the early stage teams, the newly formed ones. Whether the stakeholders want to offload some of the work they used to do or need inputs from the new team, it is more likely that they will ask for reports on the first few months. If the data science team members were generalists, and nobody else was responsible for the reporting task, they will start to work on it. Algorithms, APIs, data quality related stuff will be parallel projects and will take more time to get integrated in the system or productionized. Reports will have a higher perceived value for more stakeholders who will send more requests. If the data science team fails to prioritize or *get pressured to prioritize reporting work*, the team members will have no space to work on long term projects they came to work on in the first place. There could be worse consequences on the team or organization level, like what [Angela Bassa](https://twitter.com/AngeBassa) summarized about companies going from the excitement of *"We have a data science team"* to *"data science was not a good investment"!*:

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">Or news spread that “we have a DS team now” so everyone starts sending their sophisticated arithmetic to that team rather than just doing it like they used to before. DS team gets swamped, hypervaluable work gets backlogged, no ROI... “ugh, DS is not a good investment after all.”</p>&mdash; Angela Bassa (@AngeBassa) <a href="https://twitter.com/AngeBassa/status/1126805365721640961?ref_src=twsrc%5Etfw">May 10, 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


Usually data science teams do not go between these two states quickly. They'd gradually get overwhelmed by the reporting requests which would lead to discussions about their priorities. The team lead might ask for hiring a dedicated team/members for reporting and try to justify this to the decision makers who might be reluctant to make changes. In the middle of all this, some team members might leave because the job is not satisfactory to them. The rest will have a higher load of reporting work, which will affect their satisfaction and ability to work on long-term projects. Because it is not just about building dashboards!

### So what lies under dashboards?

Stakeholders and executives who benefit from dashboards would argue that it is simple, straightforward and of a high value, so data scientists should cooperate with them to make everything available in dashboards. **But rarley did I see a discussion about what lies under dashboards and the debt associated with them.** 

Actually, the first couple of dashboards usually fuels the enthusiasm of the stakeholders who will benefit from these insights or just start to wear the "data-driven" badge. With time, dashboards will accumulate and there will be other related tasks, that would vary according to the used tool, like:

- attending meetings to discuss requests and test the final dashboard.
- organizing dashboards.
- documenting *"where to find what"*, for better discoverability.
- getting feedback about the UI/UX.
- maintaining old dashboards *(including deleting, merging, recreating, etc.)*
- responding to inquiries about bugs, and debugging.
- managing user access.
- communicating with third parties for external issues *(e.g. if you use Tableau Online or similar hosting options)*.
- and more...

All this and more lies beneath the dashboard. This requires a lot of attention and significant amount of work from the data scientist. Sometimes it even requires additional skills that a dedicated designer can offer. That's why it is not fair to tell a data scientist, *it is just a dashboard let's do it*! 



### But aren't data science teams there to serve their organization?

Some people have valid arguments like **"The purpose of a data science team is to serve the organization according to its data-related needs"**.

In principle, it is true that any team should bring value to the organization **within its scope**. And it highly depends on what's communicated during the hiring process. When people get hired they come with certain expectations for the role. Many data scientists think about end-to-end analyses or projects where reporting is just a part of their work in the whole cycle. They'd gladly create a dashboard if it was the best way to communicate their work, certain metrics related to a new algorithm or results of an experiment. But once reporting starts to dominate their work for weeks or months with all the related tasks, some might get frustrated. It is as if you gave them DevOps work or Front-End tasks, you cannot expect them to do this **just to serve the organization**. 


### So what can we do about this?

Although it seems like something that differs from a case to another, I believe organizations and individuals could learn from previous experience. For instance:

- **Organizations** need to be clear about their expectations during the hiring process. They will definitely experiment with any new team, but they should assess their needs in advance and discuss the job description transparently, away from the general templates recruiters send in isolation of reality.

- **Job applicants** who have certain preferences and priorities should communicate that and ask enough questions to make an informed decision. They should expect that things could change when they join/ form a new team. After all their priorities will determine their tolerance to accept changes.

- **Team Leads**, who are hiring should encourage candidates to share their interests and priorities. *(I personally used to ask interviwees about their expectations of the distribution of time on different tasks, if they would hate specific tasks to dominate their work, what they would like to learn, etc.)*. And those who are leading teams should advocate for their team members, empower them, communicate their concerns with the leadership and show them the ROI of their work.

After all, I hope team leaders in different organizations could share more in this context for others to benefit from. because it is something beyond "just dashboards"!


