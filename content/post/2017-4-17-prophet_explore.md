---
layout: post
title: 'Prophet Explore: A Simple Shiny App to Get Introduced to Prophet'
---

Last February, I read about [**prophet**](https://github.com/facebookincubator/prophet) package, which was released by Facebook's [**Core Data Science team**](https://research.fb.com/category/data-science/). I skimmed the published paper [**Forecasting at Scale**](https://facebookincubator.github.io/prophet/static/prophet_paper_20170113.pdf) quickly and I got the main concept. I also liked how the creators; Sean Taylor and Ben Letham were trying to empower analysts to produce high quality forecasts by offering them a flexible and configurable model that requires general understanding, but not necessarily deep knowledge about time series models.

Later in April, I listened to Sean's discussion with Roger Peng and Hilary Parker in **Not So Standard Deviations** 35th episode  [**Special Guest Sean Taylor**](https://soundcloud.com/nssd-podcast/episode-35-special-guest-sean-taylor). It was an interesting espisode, where they discussed different aspects of the prophet project and the underlying challenges. They also discussed the different points of views on generic tools that give analysts some parameters to tune, with limited understanding of the underlying concepts. 

At this phase, I was discovering the package, so I thought about creating a Shiny App [**(Prophet Explore)**](ttps://omaymas.shinyapps.io/prophet_explore/) to play with the parameters and discover any issues quickly. But then I enhanced it a little bit, deployed it on Shinyapp.io to give access to more people and tweeted about it. Interestingly, in two days, it was active for 30 hours and  ate up 1/3 of my hours on Shinyapp.io. I kept working on it, adding some validations and I am still enhancing it.

To use the interactive App, one should upload the data in the right format. And to tune the parameters, one should understand the significance of those parameters. [**Prophet documentation**](https://facebookincubator.github.io/prophet/docs/quick_start.html) provides a detailed explanation with examples to follow for deeper understanding and guidance

### Try Prophet Explore

**Prophet Explore** is available on Github [**Here**](https://github.com/OmaymaS/Prophet_Explore). 

In case I still have active hours on Shinyapp.io, you'll see the App below.

<iframe  src= "https://omaymas.shinyapps.io/prophet_explore/"  style="border: none; width: 920px; height: 640px" ></iframe>

