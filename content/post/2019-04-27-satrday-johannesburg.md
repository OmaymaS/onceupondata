---
title: Teaching Shiny Workshop at SatRday Johannesburg
subtitle: 'Eating the cake first and playing games!'
date: '2019-04-27'
slug: satrday-johannesburg
tags: [R, Shiny, SatRday]

---

This month three [SatRdays](https://satrdays.org/) took place on the same day around the world. I was invited to one of them, [SatRday Johannesburg](https://joburg2019.satrdays.org/), to give a training and a talk at. I was excited about it because it was my first #rstats event in Africa and I wanted to contribute to events in the region where few conferences are held relative to Europe or the US. The workshop I gave was about [Building Web Applications in Shiny](https://github.com/OmaymaS/intro_to_shiny_workshop). And this is what I will focus on in this post.


### My history with learning and teaching Shiny

I previously taught or helped others use Shiny, but this was the first full-day workshop I gave on Shiny. I hope some of the participants will also transfer what they learned to others. And that's what I had in mind two years ago when I was granted a spot at the **Intermediate Shiny workshop** at **[Rstudio::conf 2017](https://github.com/rstudio/rstudio-conf/tree/master/2017)** which was taught by [Joe Cheng](https://mobile.twitter.com/jcheng). At this time, I went to learn more about Shiny but I also had another objective; I wanted to learn how to teach this material in an effective way. So I was focusing on the workshop design, observing how Joe Cheng and his assistants facilitated it, and imagining what I'd do in the future.   

Two years later, the chance came to teach a full-day workshop, where I started to prepare my material. I already had an idea about how I'd setup the workshop but I luckily had additional resource about teaching Shiny made available by Rstudio on the **[Shiny Train-the-Trainer Workshop](http://teach-shiny.rbind.io/post/)** website, which is something everyone can benefit from. The sample curricula and the flow adopts [Mina CetinkayaRundel](https://mobile.twitter.com/minebocek) approach of [Let them eat the cake (first)](http://teach-shiny.rbind.io/materials/01-starting/01-starting.pdf). I like this top-down approach and I got positive feedback about it in several occasions so my workshop was also designed that way.

{{< gallery caption-effect="fade" >}}
  {{< figure thumb="-thumb" link="/post/2019-04-27-satrday-johannesburg/ws1.jpg" >}}
  {{< figure thumb="-thumb" link="/post/2019-04-27-satrday-johannesburg/ws2.jpg" >}}
  {{< figure thumb="-thumb" link="/post/2019-04-27-satrday-johannesburg/ws5.jpg">}}
{{< /gallery >}}

### The Interactivity Game

In addition, I had in mind a sort of a game about interactivity I wanted to experiment with during the workshop. The idea is to:

- write a simple Shiny App with inputs, reactive elements and outputs. 
- make each participant play the role of an input/reactive element/output and take its name. 
- have a participant to play the role of a user who would change the value of inputs *(here players)*.
- ask players to raise their hands whenever they are affected by a change in an input/reactive value.

The point is to  make participants understand dependencies and imagine the propagation of changes under the reactivity paradigm. I had a quick trial with this but the application was so simple we didn't have many scenarios. So I'd like to try a more complex application with lots of dependencies while playing the game in the future.


<img src="/post/2019-04-27-satrday-johannesburg/ws4.jpg" style="width:100%"/>


### Finally...

I am glad to have this opportunity to meet such motivated participants from different backgrounds where everyone of us learned something by the end of the workshop. I'd also like to thank the committee who organized the event and brought us all together


### Resources

- [Workshop Material](https://github.com/OmaymaS/intro_to_shiny_workshop)

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">✍️Material of the &quot;Building Web Applications with Shiny&quot; workshop at <a href="https://twitter.com/hashtag/satRdayJoburg?src=hash&amp;ref_src=twsrc%5Etfw">#satRdayJoburg</a><a href="https://t.co/NSPyZbOU1c">https://t.co/NSPyZbOU1c</a><a href="https://twitter.com/hashtag/rstats?src=hash&amp;ref_src=twsrc%5Etfw">#rstats</a> <a href="https://twitter.com/hashtag/rshiny?src=hash&amp;ref_src=twsrc%5Etfw">#rshiny</a></p>&mdash; Omayma🔎 (@OmaymaS_) <a href="https://twitter.com/OmaymaS_/status/1114176963197980685?ref_src=twsrc%5Etfw">April 5, 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

