---
title: How do harmful algorithms evolve? 
subtitle: 'The seeds of bad data products'
author: ''
date: '2021-09-12'
slug: [how-do-harmful-algorithms-evolve]
categories: []
tags: [machine learning, algorithms, data products]
type: ''
---


**How do harmful data products and algorithms get enforced on us and impact our lives?**
a question that is widely discussed nowadays, although I am not sure if “widely” is a right description of the level of attention it takes. But there is another question that I find crucial which is, **How do these products emerge in the first place and gain credibility?** **How do crappy senseless products reach the market, proliferate our lives and put us in a reactive mode to analyze and prove their obvious worthlessness or harm?**

I always think about these questions, especially that I work in the tech industry and observe the new products and  services in  the market. I can imagine different scenarios for the emergence of bad data products and the dynamics behind these decisions. 

One of the scenarios I would like to discuss here is strongly related to **adopting ideas coming from pseudoscience or even solid research, without much reflection or verification**. I recently could imagine an example while reading [“Why We Sleep" by Matthew Walker](https://www.goodreads.com/book/show/34466963-why-we-sleep); one of the best selling books in the past couple of years. I have to clarify that this article is not a book review or a thorough investigation into the research and conclusions mentioned in the book. I am just picking some ideas that bugged me and explaining why I think they could be seeds for bad data products.

## What caught my attention in the book?

So few months ago, I was reading “Why We Sleep" by Matthew Walker. I have seen how many people were fascinated by the book, taking it as **THE REFERENCE** about sleeping. I am not an expert in the field of sleep science and the author seems to have the credentials to get the readers convinced by the cited research and conclusions. But while reading, I felt skeptical about the definitive tone, shallow correlations, & the relevance of some cited research. But this is another story out of the scope of this article. Here, I will just focus on a couple of things that triggered me, which I could associate to the evolution of data products.


Apart from the research and results shared by the author, the author tries to provide his own  vision for a better world with better sleep for more people as he believes it improves lots of aspects including health, education, and even GDP *(which is one of the unconvincing correlations in the book)* !


let me share a couple of quotes from the book about specific points that bugged me:

### 1- Linking ethical deviance and work ethics to sleep deprivation

The author talks about the ethical behavior and performance of employees given different levels of sleep as follows:


>Ethical deviance linked to a lack of sleep also weasels its way onto the work stage in a different guise, called social loafing [^VI]</sup>. The term refers to someone who, when group performance is being assessed, decides to exert less effort when working in that group than when working alone. Individuals see an opportunity to slack off and hide behind the collective hard work of others. They complete fewer aspects of the task themselves, and that work tends to be either wrong or of lower quality, relative to when they alone are being assessed. Sleepy employees therefore choose the more selfish path of least resistance when working in teams, coasting by on the disingenuous ticket of social loafing. Not only does this lead to lower group productivity, understandably it often creates feelings of resentment and interpersonal aggression among team members. 

> Of note to those in business, many of these studies report deleterious effects on business outcomes on the basis of only very modest reductions in sleep amount within an individual, perhaps twenty- to sixty-minute differences between an employee who is honest, creative, innovate, collaborative, and productive and one who is not.


This was one of the most troubling parts to me, coming from someone with a scientific background. It seemed like statements that were written only for the sake of supporting the narrative of the book which linked EVERYTHING to sleep. I even looked up the mentioned reference *[Social loafing under fatigue]*, and didn’t find it convincing to reach a broad statement like *“Ethical deviance linked to a lack of sleep also weasels its way onto the work stage in a different guise, called social loafing”* based on results from a study where *“2 experiments, 64 male students worked almost continuously for 20 hr without sleep under varying social conditions”*. 

But I can imagine that lots of readers will take the point about ethical deviance as an important insight from a trustworthy source. They will propagate it, mention in their presentations, and potentially use in decisions or algorithms related to employees hiring, firing, promotion, etc. 


### 2- Proposing the idea of sleep credit score to insurance companies

Another point which might be acceptable to many people is the **“sleep credit score”** idea. For me lots of algorithmic scores related to healthcare, employment, education, etc. have negative history and connotation. But let’s see what the author proposes in the book.

> At the very highest levels, transforming entire societies will be neither trivial nor easy. Yet we can borrow proven methods from other areas of health to shift society’s sleep for the better. I offer just one example.

> In the United States, many health insurance companies provide a financial credit to their members for joining a gym. Considering the health benefits of increased sleep amount, why don’t we institute a similar incentive for racking up more consistent and plentiful slumber? Health insurance companies could approve valid commercial sleep-tracking devices that individuals commonly own. You, the individual, could then upload your sleep credit score to your health-care provider profile. Based on a tiered, pro-rata system, with reasonable threshold expectations for different age groups, you would be awarded a lower insurance rate with increasing sleep credit on a month-to-month basis. Like exercise, this in turn will help improve societal health en masse and lower the cost of health-care utilization, allowing people to have longer and healthier lives.

So some would say that it is just positive reinforcement and nobody will be harmed or penalized. Which takes us to the next point about how such ideas might turn into bad data products given their source?

## How such ideas and theories become seeds of bad data products?

I believe there are good and bad ideas everywhere and everyone can share on any platform. But bad ideas are more dangerous when they come from scientists or figures with credibility because they are easier to adopt. So Looking into this as an example, I can see this path:

- a scientist who spent years studying a certain subject, wrote a book to communicate his research to people, emphasizing everything that supports his narrative even if it was a tiny sample study or an [edited chart](https://yngve.hoiseth.net/articles/why-we-sleep-institutional-failure/).

- The book gained a lot of attention and the scientist became a guest on many podcasts, conferences, google talks, etc. He even collaborated with google and this gave him more credibility.

- Many audience took everything they heard from the scientist as scientific facts or wisdom and started to propagate them around without filtering or rethinking some of the  statements.

- With all the established credibility, whatever the scientist says has a lot of weight for many, even if it was about something far from his area of expertise *(e.g. product design, computer vision, algorithmic fairness, etc.)*.

- The ideas and theories present a potential profitable business opportunity, and in a time where the hype about data, AI, wearables is in its peak, someone will pick these ideas and take them forward, mostly with no inherent bad intentions.


## And why such products grow and get worse?

So following  this path, it ends up with  an enthusiastic product team in an established company or most probably a startup, who got fascinated by the ideas of the author which were backed by “science” as they saw it. They will start to transform it into products, pitch it to investors, get busy working on the codebase and the powering algorithm, etc. Now they  are the accountable, not the originator of the idea, but I wonder how many would ask questions like:

- Are we in a world where everyone has the luxury to adjust their sleep patterns to raise their credit score?

- Why do people fail to adjust their sleeping patterns or get enough sleep? Is all what they need an incentive to do it?

- Which groups would fail to improve their “sleep credit score”? New parents, low-income groups who need to work more than one job, people with physical and mental illnesses, etc.?

- Should we aspire for a universal accessible healthcare to people? Are we trying to help sick people or penalize them for their inability to gain proper sleep due to their illness?

- Which groups would benefit from this system? The insurance companies, employers, and the healthy privileged persona that has control over many aspects of their life?

- What if the tracking apps or insurance data got shared with employers *(which happened before with period tracking data)*? Would they discriminate against the candidates/employees with low “sleep credit score” if they strongly believed in this link between ethical behavior and performance?

- What if employers took this ethical-performance correlation as a scientific fact and started to penalize new parents, sick, etc.? Is it sth we would like to see happening?!


These and many other questions are rarely asked, because founders think that they need to move fast, work on their data pipelines, mange their finances, hire, etc. On the  other hand investors want to push for growth and mostly care about the revenue. That's why these questions get lost and we face them as users or data practitioners after being impacted by the product that we don't sign up for in the first place, if it gets used by entities that has power over us *(e.g government, employer, etc.)*.


## So what can we do about it?

In this article, I tried to imagine a path from ideas by credible sources to product implementation. There could be sth already in the market similar to the examples I mentioned. Most probably, nobody would have bad intentions along this way, but some would be so privileged to even think about anything beyond their bubble, and many would just accept what's presented to them without questioning what it means to create a certain product. And that's the biggest problem! 

That's why even if we cannot prevent every harmful algorithm before it gets developed, we can at least as individual contributors, researchers or even founders, be more critical about the ideas we adopt, resist working on potential harmful products and question the ideas and hypotheses presented to us even if they come from credible sources.

[^VI]:   Hoeksema-van Orden CY, Gaillard AW, Buunk BP. Social loafing under fatigue. J Pers Soc Psychol. 1998 Nov;75(5):1179-90. doi: 10.1037//0022-3514.75.5.1179. PMID: 9866183.
