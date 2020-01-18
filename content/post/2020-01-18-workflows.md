---
title: A Journey into a Team's Workflows
author: ~
date: '2020-01-18'
slug: data-projects-workflows
categories: []
tags: [R, python, data]
subtitle: 'or how to navigate chaos and bring order to data projects!'
---

**"I thought my code was clear and organized, but I figured out it was not!"**, that's how a data analyst told me after a couple of sessions I held to examine the workflows of different team members and discuss their practices. I like to help people reach this realization to see the value of improving their workflows to them as well as to others with whom they collaborate. And when I say workflows I mean how to organize a project? how to make analysis reproducible? How to read, save and version related data? and so on.

From my experience of collaborating, hiring and leading teams, I could see how this topic was under-valued for many of the data analysts/scientists I spoke to or interviewed. **But why is this a common pattern? and what do I do help others move torwards better workflows?**

## Why is the topic of workflows under-valued?

I'd would attribute this to several factors, but I will mention two in specific:

### 1- The topic of workflows is under-taught 

I'd start with a point mentioned by [@JennyBryan](https://twitter.com/JennyBryan) highlighting that this topic is consistently "under-taught and under-examined". I think few people really generate good content that addresses beginners or intermediate users. You can find this out when you scroll into playlists of conferences talks or top blog posts. 

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">I’ve reached a similar conclusion re: talks for a broad audience.<br><br>I think it’s almost orthogonal to advanced vs beginner. Certain topics are consistently under-taught and under-examined, such as “workflow”. Maybe because they don’t really fit into tool-centric manuals and docs? <a href="https://t.co/EMczplRLVl">https://t.co/EMczplRLVl</a></p>&mdash; Jenny Bryan (@JennyBryan) <a href="https://twitter.com/JennyBryan/status/1200497358212980736?ref_src=twsrc%5Etfw">November 29, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

I believe this is either because the content creators and speakers take it for granted assuming that everyone is aware of these tips or because there are "cooler" topics for them to talk about.

### 2- The solo data analyst/scientist setup

Another reason I see is the evolution of the data analyst/scientist role at many organizations, whether small or big. It is common to find one data analyst/scientist being hired to start a team or to serve several function with no peer. When this team member works on their own with no standards or a collaborative environment, they follow their own workflow, whatever makes things easier for them as long as they get the job done. Bad practices might creep in but they don't seem to be so harmful, because nobody else is interacting with these projects, running them or giving any feedback. The team might grow later with new members adopting different workflows. And unless they start to collaborate heavily, each one would think that everything is clear and organized.


## What do I do help others move torwards better workflows?

I believe that generating more content and integrating this topic into courses would emphasize its importance and let people think more often about it even if they were the solo data analyst/scientist. 

Another thing I do, is when I face a situation where I have a team that haven't thought about the topic before. They might have messy unreproducible code but I take this as a chance to let them examine their practices closely and realize there's a better way of doing things.

I start to organize some session in which I invite the team members to participate in the following activities:

### Step 1: Exchange your code with others

First of all, I'd ask each one to bring a script/notebook that is relatively organized for them and give it to someone else to run. And here we would stop and ask the question:

**- How would you share your code?**

They would say github, mail, slack, etc. And I'd ask each one why, and whether there are pros and cons for their method.

### Step 2: Run each other's code

Then, I'd ask them to try and run each others code. It is highly likely that everyone fails to run the whole script/notebook. This is the first realization that collaboration wouldn't be smooth under the current circumstances. Here we would pause and discuss:

**- Why is there a diffuculty to run this script/notebook?**

**- At which step did it fail?** *(reading data, loading libraries, calling functions, retrieving data from a database, other reasons)*.

### Step 3: Describe your workflow

At this point, the team members start to see the differences in their thought processes and mental models. So I'd ask them to reflect on the outcome of the previous step and describe their workflow by answering some questions like:


**- How do you organize your projects?** *(Rstudio project, ProjectTemplate, package, cookiecutter, etc.)*

**- How do you distribute files in sub folders?** *(data, scripts, notebooks, output, models etc.)*

**- Do you keep any remote version on Github/Bitbucket? How often do you commit/push your changes?**

**- How and where do you load your libraries?**

**- How do you read data? Do you keep a local copy of the raw data? where?**

**- Do you use relative paths to files/scripts? Do you ever `setwd()`  or  `chdir()` in the middle of your script? What are the alternatives?**

**- When do you use `scripts` vs. `Rmd/Jupyter notebook`?**

**- Where do you keep your functions?**

**- Where do you keep the database credentials that you load in your scripts?**

**- do you follow a style guide or use a linter? What are your preferences?**

**....and more**

It is possible to find that some of the participants in this discussion never considered these points, couldn't give specific answers or were not familiar with these concepts. But this is not a problem, and everyone should be encouraged to share their thoughts without harsh judgement. After all, I take this discussion as an opportunity to learn about the different approaches of the team, discuss good practices and reflect on the difficulties faced while running each others code. 

### Step 4: Agree on some standards

After all these discussions, I'd invite the team to take some time, digest all the inputs and read/watch some relevant resources. Then we would all come back later to agree on some rules like the project structure, credentials storage, documentation, etc. If the team works with different tools, which was always the case for my teams *(used both R and python)*, we could discuss some preferences that make our collaboration easier.


**In conclusion, when it comes to data practitioners who already worked on some analaysis or projects, I find it better to let them realize the problems with their current workflows on their own through such discussions. Instead of giving them a set of instructions or recommendations to follow, I try to lead them in this journey to discover the issues they have in their workflows, struggle to collaborate with others and then get motivated to find a better way**.





