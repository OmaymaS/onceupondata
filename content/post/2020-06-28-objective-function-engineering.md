---
title: Objective Function Engineering as an Interface Design Problem
subtitle: 'Will individuals ever be able to control algorithms?'
date: '2020-06-28'
slug: objective-function-engineering-interface-design
categories: []
tags: [Data Science, Machine Learning, Design]

---

**How many times have you been on a platform with an objective in mind that is *a bit* different than what the product optimizes for?**. I am saying *a bit* different because I mean the case when you want to use the original features of the platform but with some tweaks that improves *your* experience. This idea frequently comes up in a form of wishes by users saying *"I wish Youtube allowed me to.."*, *"what if Twitter made it possible to.."*, etc. 

 <blockquote class="twitter-tweet"><p lang="en" dir="ltr">I wish Twitter allowed me to follow individual personas instead of people. For example, I want to read this person’s AI and personal tweets, but I have no interest in his or her political tweets.</p>&mdash; Denny Britz (@dennybritz) <a href="https://twitter.com/dennybritz/status/1276426612926529536?ref_src=twsrc%5Etfw">June 26, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
 

I passed by one of these wishes yesterday by [Denny Britz](https://twitter.com/dennybritz) on Twitter . The tweet triggered an interesting discussion on this topic including different perspectives and strategies by users to control their own experience. 

This reminded me of an interesting idea I heard last year in an [interview](https://youtu.be/Bo8MY4JpiXE?t=4613) with [François Chollet](https://twitter.com/fchollet) on the [Artificial Intelligence Podcast
](https://www.youtube.com/channel/UCSHZKyawb77ixDdsGog4iWA) hosted by [Lex Fridman](https://twitter.com/lexfridman). The idea was about objective/loss function engineering as an interface design problem; particularly about the potential and challenges around giving control to users over algorithms. 

**In this post I will gather some thoughts about the discussion triggered by the original tweet and relevent interesting points from the interview with Chollet, like what does it mean to give users control, how could objective functions be defined or abstracted, etc.**
 
### Platform versus individual users objectives

Talking about objective functions from a high level, we can say that products usually try to find a point where users are "collectively" served while optimizing for what brings revenue. And if you think about marketplaces, there is an extra tension introduced because there are two sides of users. With the current state of most of the "social media" platforms and what is monetizable for them, engagement is in the heart of what they optimize for. This might be an oversimplification because definitely other metrics and signals are considered according to the business model, the complexity of the platform, etc. But engagement and how it is linked to Ads revenue remains a key objective that influences critical product decisions in most of the huge platforms. 

Users, on the other hand, are on the receiver side of these product decisions. They are not seen as individuals with different needs, they are just "users" or in the best case belonging to user groups or personas. Even with the claims of personlization, individuals are highly impacted by the net behavior of the groups they fall with according to how the product categorizes them. In addition, this personlaization aspects are strongly linked to what the product optimizes for like engagement.

### Users tweaks and hacks

Realistically products cannot, *till now*, optimize for individual needs with millions/billions of users. Consequently, users who need something beyond or different from what's offered to them try to find a work around. In the replies/retweets to the original tweet by [@dennybritz](https://twitter.com/dennybritz), we can see people approaching this issue in different ways.

**Technical solutions**

Some tend to think about an extra layer or an algorithm that would help them classify topics or catch signals about their interests.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Quadratic voting of tweets based on topic! So people who are experts in a kind of topic only get their tweets of that topic surface to our attention. Requires NLP of course to implement.</p>&mdash; Carlos E. Perez (@IntuitMachine) <a href="https://twitter.com/IntuitMachine/status/1276833536495026176?ref_src=twsrc%5Etfw">June 27, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Which is an extra effort that has its own caveats even if someone decided to take this path as clarified by [Denny Britz](https://twitter.com/dennybritz) who mentioned the limitations of Twitter API. 

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Actually, there is. The Twitter API sucks, probably because they need to serve their ads somehow. That’s why a lot of the third party clients have shut down or removed features over the past few years.</p>&mdash; Denny Britz (@dennybritz) <a href="https://twitter.com/dennybritz/status/1276644381202751491?ref_src=twsrc%5Etfw">June 26, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


**Control what is under control**

Others prefer to think about what's under their control like the **Unfollow**, **Mute** or **Lists**. Some of the mentioned strategies were:

- **unfollowing** people whose content is heavily loaded with topics of no interest to them, hoping that others will amplify the interesting signals in retweets.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">There were people I unfollowed but was worried about missing out key stuff. In the end though other accounts tended to retweet their best stuff so it mostly worked out</p>&mdash; HenryE (@Henry_E__) <a href="">June 26, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

- **muting** keywords to exclude certain topics while keeping following people.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">It’s interesting to see how different people’s preferences are on Twitter. I usually follow people who seem like they have a lot of good opinions on a variety of interests and use the mute keyword option liberally for stuff I’m not interested in. <a href="https://t.co/2UdVhYQyJh">https://t.co/2UdVhYQyJh</a></p>&mdash; Vicki Boykis (@vboykis) <a href="https://twitter.com/vboykis/status/1276842139943612417?ref_src=twsrc%5Etfw">June 27, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


**Go somewhere else**

Another perspective is just finding another platform to satisfy one's needs instead of trying to tweak the default experience. This discards the point that the user just wants a little bit of change on top of the original product. They don't hate it, they just wish for a an extra feature.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">So you basically just want to read trade publications...? Instead of turning Twitter into that, just subscribe to the current version of trade publications of which there are so many with the proliferation of newsletters.</p>&mdash; Stefan Negritoiu (@stefann42) <a href="https://twitter.com/stefann42/status/1276604491589021696?ref_src=twsrc%5Etfw">June 26, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

It is also worth mentioning that some people see such a tweak as a negative thing as it reduces them to targeted content rather than a whole person whose opinions are informed by the rest of their views.

*I just took this original tweet as an example of users wishes which could differ according to the platform and users. So let's go beyond this specific wish to the idea of control over algorithms and the objective function optimization in general.*

### Objective/Loss function optimization

When **Objective function optimization** is mentioned, most of the people who are oriented towards the technical aspects of building models will think about the algorithms, mathematics or code. Few will relate to the whole system and consider the interface design aspect associated with it. That's why I get excited once I find experts in the field talking about this side. 

I mentioned the original tweet and the discussions reminded me of a [segment](https://youtu.be/Bo8MY4JpiXE?t=4613) from an interview with François Chollet. I will pick the most relevant highlights in the following points:


- **User control over algorithms**

Chollet talked about the idea of giving users configuration settings to define what they care about and how they want to be impacted by a certain algorithm. 

> "What I would like to see. It is probably never gonna happen because it is not super realistic. But that's actually somthing I care about. I would like all these algorithms to present **configuration settings** to their users, so that their users can actually make the decision about how they want to be impacted by these information, recommendation, content recommendation algorithms. For instance as a user of something like Youtube or Twitter, maybe I would like to maximize learning about a specific topic, right? So I want the algorithm to feed my curiousity, right? Which is in itself very interesting problem."

So what he would like to see is people interfacing with the systems on their own terms which is a bit like the starting point of this post; *someone wants to customize their own experience on Twitter*.

> "I don't want actually any entity making decisions about in which direction they are gonna try to manipulte me, right? I want technology, so these algorithms are increasingly going to be our interface to a world that is increasingly made of of information, right? and I want everyone to in control of this interface to **interface with the world on their own terms** so if someone wants these algorithms to serve you know their own personal growth goals they should be able to configure the algorithms in such a way yeah. "

But talking about configuration settings might seem like users will be overwhelmed by many parameters which is unrealistic. So Chollet also tapped into this point during the discussion.

>"It is not realistic to give users control of a bunch of knobs that define algorithm instead we should purely put them in charge of defining the objective function like let the user tell us what they want to achive how they want this algorithm to impact their lives."

- **Abstract objective functions**

But defining an objective function is also challenging. The interviewer [Lex Fridman](https://twitter.com/lexfridman) referred to this point and argued that it would be too complex to define what *"personal growth"* or *"learning"* means to one person in order to be able to transfer this to an algorithm. I also believe it is a tough problem because we all know that the current systems are still dumb to understand such abstraction.

- **The interface design aspect**

Chollet agreed it is non-trivial problem, and tried to focus on the interface design aspect that is highly undervalued. He also said that he believed there would be a role or job title related to "Loss Function Engineering" in the future.

> "It is mosthly an interface design problem. The way I see it you want to create technology that's like a mentor or a coach or an assistant so that it is not your boss. You are in control of it you are telling it what to do for you and if you feel it is manipulating you, it is not actually doing what you want you should be able to switch to a different algorithm"


### So how would all this connect together?

I personally believe that:

- although this is a non-trivial problem, it is worth being on the table and it should be looked at as an interface design and UX problem. People who work on such products should think about it as an interdisciplinary challenge. It is not primarily about algorithms, state of the art methods or math. It is about system engineering and design which requires a lot of understanding of tradeoffs, consequences, feedback loops, and more. 

- we should aspire for a shift in the mindset of building products that exploits users or over-promise, towards products that assist and empower them while making profit.

- there should be more awareness about the design aspects in the field, especially for those who focus on the technical side, the benchmark applications, the isolated algorithms, etc.

It might take years or decades, but maybe one day, even if it is hard, there will be incremental steps towards giving individual users more control while keeping revenue flowing to the products.
