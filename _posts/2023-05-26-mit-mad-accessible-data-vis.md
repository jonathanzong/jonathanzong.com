---
layout: post
title: "MIT Morningside Academy for Design: Accessible Data Visualization for Blind and Low Vision Users"
slug: mit-mad-accessible-data-vis
---

<style>
ol {
   list-style-type: decimal;
   list-style-position: inside;
   margin-bottom: 1em;
}

ol li {
  margin-bottom: 0.6em;
}

.video-container {
  position: relative;
  width: 100%;
  max-width: 100% !important;
  padding-bottom: 56.25%;
  margin: 0 auto 1em auto !important;
}
.video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 0;
}
</style>

<div class="video-container">
	<iframe class="video" src="https://www.youtube-nocookie.com/embed/lNvPY8-FrvY?start=46" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

_The following is a lightly edited transcript of the above recorded talk organized by the MIT Morningside Academy for Design._

The next fellow is Jonathan Zong. He's a computer scientist and now in his fifth year of his PhD over at MIT CSAIL where he's working with the Visualization Group. Not only have you been recognized as a MAD Fellow, but also by the Paul and Daisy Soros Fellowship and Forbes 30 under 30. He's joined today by his advisor, Professor Arvind Satyanarayan. He is an Associate Professor and leads the Visualization group at MIT CSAIL. Please welcome Jonathan to the stage.

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-1.png">

My name is Jonathan, and I'm excited to share my work today on designing accessible data visualizations for blind and low-vision users.

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-2.png">

According to a survey by the National Federation of the Blind, 7 million people in the United States have a visual disability.

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-3.png">

And for many of these people and for more globally, 96.8% of the top 1 million pages on the internet are simply not accessible to the screen reader assistive technology that they use almost every day.

If you're not familiar with how screen readers work, I'm going to kick it over to my past self to explain what they are.

<div class="video-container">
	<iframe class="video" src="https://www.youtube-nocookie.com/embed/3zF5bVbqJQw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

So that's the experience of the internet that you can expect if you're using a screen reader. But often when you're dealing with image content, if the authors of the web page haven't provided an alternative text description of the image, your experience will look more like this.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">I wonder who’s gonna claim the state of Image. <br><br>Video alt: VoiceOver on the mobile version of The Guardian reading every US state on the map as “Image”. <a href="https://t.co/KRs9pustXz">pic.twitter.com/KRs9pustXz</a></p>&mdash; Sarah L. Fossheim (they/them) (@SarahFossheim) <a href="https://twitter.com/SarahFossheim/status/1324427612723253250?ref_src=twsrc%5Etfw">November 5, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-6.png">

In the work that I've been doing with the Visualization Group and as a MAD Fellow this year, I've been thinking about this question of: how do we make charts, which are particular kind of image content, more accessible to screen reader users?

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-7.png">

And there's a couple of reasons why this is a challenging and interesting design question because this is essentially a question of cross-sensory translation. Visualizations and text descriptions just work differently. Charts have these various visual features that, as a reader, you can shift your attention around the chart
look at high-level patterns, look at individual data points, and you can do this on the fly. But if you're using a screen reader, the text description imposes a linear predefined reading order. So you're beholden to the decisions that the person who wrote the text made about what information was important to include.

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-8.png">

And so if we walk through an example of what current best practices for making charts accessible look like using this example election map from that video earlier, there's two main approaches. The first is alt text.

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-9.png" alt="A map of 2020 US Presidential Election results. Joe Biden has 227 electoral votes. Donald Trump has 213 electoral votes. 98 votes remain.">

If someone were to provide an alternate textual description of that map, it might look like something like this:

A map of 2020 U.S. presidential election results. Joe Biden has 227 electoral votes. Donald Trump has 213 electoral votes. 98 votes remain.

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-10.png">

So alt text has some strengths and some limitations. One great thing about alt text is that it gives you a high-level overview of the data pretty efficiently. After listening to that couple of sentences, I know what the general takeaway of the map is. But on the flip side, there's no way to do self-guided data exploration. So if I know the amount of votes that Joe Biden has but I want to know how many of those votes came from each state, if that information is not included in the sentence, then there's no way to find out.

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-11.png">

The other way that people make charts accessible on the internet is by including a data table of the underlying data
that the chart is representing. And data tables address this limitation of alt text.

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-12.png">

They enable detailed exploration that you can do in a self-guided manner. You can use your screen reader to move around the different parts of the table as you please. But with data tables, it's very tedious and time-consuming to build a mental picture of what's going on with the data. If you're reading individual data rows one by one, there's a lot that you have to remember in order to understand higher-level patterns.

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-13.png">
Link: <a href="https://mitvis.github.io/olli/">mitvis.github.io/olli</a>

So to address the limitations of these existing practices, our group at MIT Vis has been developing Olli, which is an open source JavaScript library for converting data visualizations on the internet into keyboard-navigable textual descriptions that both allow you to get high-level overviews in the form of text and also navigate around varying levels of detail and do self-guided exploration. And this is something that's open source and people can use it today.

So here's a demo video of how Olli works. And pay attention to how we are moving between text descriptions at varying levels of detail.

<div class="video-container">
	<iframe class="video" src="https://www.youtube-nocookie.com/embed/pkNoU2yfDa4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

So how is Olli different from prior best practices?

<img src="/images/blog/mit-mad-accessible-data-vis/jzong-mad-05.3.2023-15.png">

We prioritize these design goals of enabling open-ended, self-guided exploration where screen reader users can control their position within this hierarchy at their own pace, and also provide descriptions at varied levels of detail. So if a high level description isn't enough information for you, you can dive in deeper and get more pecific about the data.

Now to preview what's next in this work, and this is work that I've been doing for this past spring that I haven't shown publicly yet, we've been thinking about this question of multisensory data representations.

So currently, accessibility approaches are very vision centric.

Here, we started with a chart and converted it into a text description.

And we're still thinking about these two things as very independent entities.
But what if we think about using all these different modalities together in one system?

So here's a demo of a version of Olli that's kind of more integrated with the visualization so that blind data analysts and their sighted collaborators can have a common point of reference.

And as I navigate the structure here, you'll see that the visualization updates to show where the screen reader is focused.

And then we can integrate other forms of sensory modalities with their own pros and cons, like data sonification, which is very good for giving a gist of large amounts of data
very quickly but can't really tell you about individual data values.

[DIGITAL TONES]

And we can't escape talking about ChatGPT when we're talking about textual content.

We've also been kind of exploring methods where we query GPT to offer us kind of additional analysis of the data that's kind of situated in the hierarchy. So I'll give an example of that here.

And so what I find really interesting about that is that this information can incorporate not just information that's in the data, but information that accounts for things like current events and social context. And that can just provide another avenue for helping people through analysis.

So I've highlighted here a couple of interesting outputs that are situated in that Amazon section of the Olli hierarchy. So the model is providing information about things like product launches and entering into new markets to contextualize the data that you're looking at. And it knows about events like the global financial crisis in 2008 and offers that as a hypothesis for why your data is the way that it is.

And doing this situated in the Olli structure means that rather than kind of relying on it to summarize your entire data set, you can use it to understand targeted subsets of your data and also verify its claims against the data that you already have on hand.

So I just want to thank my enormous list of collaborators.
A special shout out to Daniel Hajas, who's a blind researcher based at the Global Disability Innovation Hub in London who's been an important co-design and research partner. And also my two current masters and undergrad advisees, Shuli Jones and Isabella Pedraza Pineros.

Thank you so much. And I look forward to the conversations today.

**Q&A with Arvind Satyanarayan**

**Arvind**<br/>
Great. That was really awesome. Even though I've seen the work day to day, week to week, it's just nice to see it come together and hear you tell the story of it versus the story that I tell. And I was just thinking about particularly the way you were introduced as a computer scientist. I'm curious if I can prompt you to sort of reflect on-- I think the computer science bit of your identity is only part of what makes you such an effective designer. And I'm curious about the path that led you to working on accessibility and how maybe it's prompting you to draw on other parts of your sort of skill set.

**Jonathan**<br/>
Yeah. Thank you, Arvind. I guess coming out of undergrad, I did undergrad at Princeton, where I studied computer science and visual arts with a focus in graphic design. And I think I kind of stumbled into data visualization just because it seemed like a natural intersection of those two things.

Within computer science, my undergrad thesis was around the ethics of data collection and designing systems to support people in saying no to researchers who want to collect their data. I think there's a few through lines
from that work that I've tried to bring into the accessibility work.

One is the idea of designing systems that support people's autonomy and agency and making software flexible enough to allow people to express their preferences and their values. And I think another is just the idea of design as something that can help us answer or at least make progress on really tough social and ethical questions.

In the ethics work, that looks like drawing from ideas in feminist philosophy to understand how we should interpret the way that users interact with a system that's designed around them saying no to powerful actors. I think in the accessibility work, it's thinking about broader conversations in disability studies about how there's no such thing as one-size-fits-all solutions and really taking that to heart when we design software.

**Arvind**<br/>
Oh, I love it because you set me up for my next question. Riffing on that idea of no one-size-fits-all, I was curious-- there's this notion in accessibility, which I know you're familiar with, called the curb cut effect where something that was designed for accessibility purposes ends up having a larger impact and benefit for everyone. And I'm curious whether you're seeing some of that emerge in some of your work, whether it's in the specific things you showed us today or in some of your thinking around the ethical implications of user agency and autonomy and things like that.

**Jonathan**<br/>
Absolutely. Yeah. One thing that we've discussed a lot amongst our collaborators is the idea that for accessible representations, like textual representations of data, why even refer to the visualization? Why do blind users need to know that there's an x- and a y-axis?

And I think part of that is just that we're all kind of situated in our social and relational contexts. Blind folks have sighted friends, and they want to talk to them about the data that they're looking at. And so it's important to create those common reference points even as we're kind of translating the modality that people access this information through.

And so with the work that I was showing at the end, we're really thinking about facilitating collaboration between blind and sighted users in a way that benefits everybody. Because having access to those multiple modalities just gives you more options for understanding and analyzing your data.

And something that we've talked about a lot too is there's kind of increasing momentum around accessibility in data visualization right now and increasing recognition that this is an important issue. And I think part of what we're trying to show with our work is that it's both important because it's socially important, but it's also just a very interesting and intellectually rich area for design. And there's all these questions about-- what are the different relative strengths of these different sensory modalities that will then feed back into creating better data visualizations?

**Arvind**<br/>
Yeah, I really love that point that it's not only the morally right thing to do, but it's just intellectually deep and interesting. And these two things don't have to be mutually exclusive. And so I was curious about what that means in the context of that really provocative demo that we ended on of GPT doing the data analysis. I don't even know if that's the right way to describe it. Doing the data analysis for us or doing the interpretation for us. And so I'm curious for-- I know that it's a very early prototype, but I'm curious already what are some of your hunches, and what the balance we might want to achieve there might be?

**Jonathan**<br/>
Absolutely. I went back and forth a lot on the title for that slide and how to describe what was happening. I think something that's come up a lot in our conversations with blind and low vision users is just the idea of agency and who is in charge of doing the interpreting.

When one of my colleagues, Alan, tested a lot of different kinds of textual descriptions with folks, we realized that for sighted people, people really like descriptions that do a lot of interpretation analysis and give you the high level takeaway. Because we can look at the chart and do the kind of low level numbers-accessing stuff,
relatively quickly.

But for blind and low vision users, they actually didn't like those kind of too interpret-y descriptions because they
felt like it was kind of taking away their ability to draw their own conclusions first by engaging directly
with the data themselves. So with something like using GPT to offer these additional descriptions, I really
think that we should be thinking of these more as kind of hypothesis generation exercises rather than asking for the answer. And part of that is, GPT gets it wrong more frequently than we would like it to. And there's other work in our lab kind of thinking about the ways in which it gets it wrong.

But yeah, I was trying to articulate in the demo, situating that additional information within the data structure where you can hear that description but then go back and do the analysis yourself and decide whether or not you agree that the global financial crisis actually caused this dip in the data is powerful to leave in the user's hands.
