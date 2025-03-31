---
layout: post
title: 'Data Refusal in Conversation with List Projects 31: Kite'
img: '/images/blog/kite.jpg'
---

_On March 5, 2025, I gave a [talk at the MIT List Visual Arts Center](https://listart.mit.edu/calendar/graduate-student-talk-jonathan-zong) as part of a public engagement talk series that pairs researchers with ongoing exhibitions at the List. Below is a video and transcript of that talk._

<style>
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
img {
	margin-top: 2em;
}
</style>

<div class="video-container">
	<iframe class="video" src="https://www.youtube-nocookie.com/embed/GZJGUE9JJK0?si=T7Uy8UbAxWg4dVzp" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

## Introduction by Cassidy Westjohn

Hi, everyone. Thanks so much for coming out tonight. My name is Cassidy Westjohn. I'm the public programs coordinator here. Welcome to the List Visual Arts Center. And this is a Graduate Student Talk with Jonathan Zong.

This is a series where we invite graduate students and postdoc researchers to expand on our exhibitions using their expertise in a similar subject-matter as a way to see how art and research are overlapping on MIT's campus.

Tonight, we'll be hearing from Jonathan Zong, a Postdoctoral Associate at MIT CSAIL, and fellow at Harvard's Berkman Klein Center for Internet and Society, and who will be an assistant professor in Information Science at University of Colorado Boulder in 2025.

In his research, Jonathan partners with blind collaborators and study participants to co-design interfaces for non-visual data exploration. He also developed software and conceptual frameworks for managing the ethics of consent and large scale social media data collection.

Jonathan's work has been recognized by the MIT Morningside Academy for Design Fellowship, the Paul & Daisy Soros Fellowship for New Americans, and Forbes 30 under 30 scientists.

In this talk, Jonathan will explore this central question. How do people say no when they're not given permission to say no? Feminists and Indigenous scholars and activists have developed the concept of refusal as something that people with the least power in society can take up to challenge authority and open up new possibilities.

Jonathan will discuss his research on data refusal as design, how people work to reshape systems of large scale data collection. Zong will draw connections between this work and Kite's artistic and scholarly engagement with Lakȟóta ontologies and Indigenous AI.

At the end, we'll have a Q&A, where you'll have a chance to ask any questions you may have. And that is it. So thank you so much for being here and showing interest in our programming. And I'll hand it off now to Jonathan.

## Jonathan Zong's Talk

Thank you so much, Cassidy, for that introduction. And thank you to you and the List for having me here tonight.

So the goal of my talk today is to introduce some of my work on the idea of data refusal and put it in conversation with the work that you see here by the artist [Kite](https://www.kitekitekitekite.com/), who is a Lakȟóta artist and scholar, multi-talented visual artist, performer, composer, also a professor at Bard College. And it's my hope that hearing about some of my work will help you see some of these works in a new way and have interesting conversations around them.

So my work engages with the idea of data refusal, and I'll break this talk apart into maybe like three parts.

First, I'll introduce the idea of refusal and talk about where that idea comes from. Then I'll go deeper into my work on the idea of refusal as an act of design and how it contributes to design and computer science and the creation of technology. And then lastly, third, I will draw connections between my work and the work by Kite that you see around you. And then we'll open the conversation for Q&A from there.

### What is Refusal?

So first, what is refusal? As Cassidy suggested, I think about refusal as this idea of saying no without being given permission to say no. And it's an intentionally broad concept. It's a way of describing a category of thing that people do.

And the reason we have a concept that's intentionally this broad is because it describes actions that people take in a lot of different situations, in a lot of different areas of society.

And we think about refusal in the context of data. When we talk about data, we're talking about something that's very ubiquitous. It's information about people that's automatically collected and then used in a lot of different areas that are inputs into decisions that have a lot of important social consequences.

So whether that's data about you that goes into your credit score or some pretrial risk assessment algorithm or any other number of systems. Because data touches so many areas of life, the situations that people find themselves in when they are practicing refusal against data are very varied.

So we're thinking about things like, there was a family who tried to hide their pregnancy from e-commerce ad targeting algorithms. And they had to do things like use cash and be careful about what they typed into Google and things like that.

There's examples of advocacy organizations, like organizing people into class action lawsuits against governments and companies for using racially-biased facial recognition algorithms in services or policing.

And there's even direct forms of refusal, like protesters in Hong Kong taking saws and chopping down lampposts because they might have surveillance cameras in them.

So even though these various actions all look different from each other, some are things that individuals do, some are organized legal actions, some are maybe illegal actions. The idea of refusal helps us see these different concepts as part of the same phenomenon or same movement in society.

### Origins of Refusal as a Concept

So refusal is an idea that comes from scholarship and thinking from feminist and Indigenous scholars. And I'll talk a bit about what it means to name those as the conversations that we're starting from.

So if we think about consent, maybe as an example of a conversation that feminist scholars have found very important in recent years, the idea that for consent to be freely given, being able to say no without coercion or any outside influence is really important.

And I think that feminist perspective of thinking about power when it comes to decisions and consent informs ideas of refusal, where sometimes companies who are asking for our data, give us an opt-out button, or either agree to the terms and conditions or just like, don't use this thing. And those aren't equally weighted options.

So a feminist analysis of power helps us see maybe all the choices on the table are bad. And refusal turns into a way of not just saying yes or no to an option that's presented to you, but even questioning why aren't other alternatives on the table and questioning the legitimacy and authority of people who are offering us these constrained choices.

And a lot of conversations around refusal have happened in the context of ideas around biological citizenship, which is really important to Indigenous scholars who are thinking about what makes someone a citizen of a sovereign nation and what happens when external governments and forces try to impose a way of identifying you based on things like your genetic ancestry, that might not align with the way that you see yourself or the social reality of the communities that you live in.

### An Example of Refusal in Practice

So I'll give an example of one maybe inspiring instance of refusal that I think exemplifies a way that refusal can be a thing that not just says no to a thing in the present, but also suggests alternate future possibilities.

So there's a movement called Indigenous Data Sovereignty. And one of the organizations that's been leading this movement is called the First Nations Information Governance Center. And the story of that center is that there were First Nations groups in Canada that had been systematically left out of health surveys that were conducted by the Canadian government.

And these were sovereign nations. And the Canadian government wasn't necessarily thinking of them in the way that they were thinking of themselves. But they also felt the effects of being left out. No data about them meant that they maybe weren't getting as good access to resources that were being allocated on the basis of this data.

So they ended up doing bottom-up community-led development process of an alternate regional health survey that was made by and for First Nations people. And then taking that to the Canadian government and saying like, this is the data that we want to be understood by.

And so refusal in this sense, was saying no to one kind of existing way of working, but also proposing an alternative.

### Data Refusal as Design

And this ties into-- the reason I think this serves as an inspiration for my work is that much of what I've been thinking about is the idea of data refusal as an act of design.

So I work in a computer science department, where I'm thinking about designing technology. Making decisions about how technology should work, what kinds of inputs should go into technology, and where it should be deployed in the world.

And I think conventionally, computer scientists think of technology non-use as like a form of deprivation or a lack of access. So the assumption maybe is that if people are not using the thing that we built, we just need to make our thing better, and then people will then use it. Once it's more usable or user friendly.

And that starts from an assumption that the thing that we decided to build is like a thing that people want in the first place.

And so I think something that's interesting about refusal from the context of this conversation about technology design is that refusal is a way for people who have historically not been part of these conversations—about what technology should be designed, how it should be designed, how it should be used in the first place—to have a say.

And we can look at acts of refusal, like people avoiding the use of certain technologies or trying to get them banned through the law as responses to one version of a set of relationships between technology and society that's being advanced.

And maybe behind that refusal, there's the seed of an alternative. Refusal is always implicitly about we would rather not have this, we would rather have something else.

And even if we don't know what that something else is, I think considering refusal as a kind of legitimate way of engaging with technology helps us see those instances where our current technologies are maybe insufficient or helps us see the unequal power relations that go into the development of technology.

### Connections with Kite's Work

And because Kite's work weaves together her scholarly and artistic background so well, I think there's a lot of ways that I see my work and hers as potentially being in conversation.

I first learned about Kite's work on the scholarly side of her work, where she has done a lot of writing around how Lakȟóta ways of thinking and ontologies and perspectives around how people relate to materials and other non-human entities, how all of that can inform practices of design.

So she has this essay called How to Design Anything Ethically or something like that. And it's taking the perspective of what can we learn from-- she as a Lakȟóta citizen, is really engaging with her community's cultural practices.

And she walks through this example of the process and the thought that goes into designing a Lakȟóta sweat lodge. And breaks down that process into a framework that might apply to the design of other things.

So she uses that as a template for thinking about what would be a starting point for trying to design AI more ethically.

And I guess, a lot of her work deals with this idea of process and protocol. And she describes protocol as decisions and actions that define relationships between humans and non-humans.

She talks about the stars and the stones, the local and the global. And she's thinking about the way that we decide how to do things affects the outcomes that are created.

And I think even though she might not explicitly use the word design all the time, I think this is very resonant with the way that I'm thinking about refusal as design, refusal as part of a process of society collectively coming to terms with decisions about what technology should be.

### Protocol and Materiality in Kite's Exhibition

And in the gallery here, I can talk a bit about the centerpiece of this show, which is a piece called Dreamlike Star.

And it's a multi-part-- there's this film aspect, there's a flat sculpture on the ground made of stone. And there's this graphical component that's on the wall.

And the piece is about-- Kite worked with a Lakȟóta designer or visual artist to create what they call a shape kit. So a set of icons, shapes that serve as a visual vocabulary.

And she used that to translate three months of her dreams into a visual score that then informs a performance that takes place between a performer and a set of instructions that are on the wall.

So you can see how the idea of protocol is taking shape in this piece where a performer is kind of following a score, which is a set of instructions, maybe behaving in a machine-like way.

And she, in her performance, has sensors and she has this braid of hair that she created that's also a musical instrument with machine learning models that she trained herself, that map her movements and the movements of the braid into musical output.

And I think the engagement with materials like her own hair or the stones that we see here, I see as important to her engagement with her Lakȟóta background. She describes computers as melted stones that are mined from the Earth.

And I think this attention to material echoes some other conversations that are happening too in conversations about the sustainability of AI. There's a big lithium mine in Nevada that powers a lot of AI systems that's built on the ancestral land of Indigenous peoples. And the way that we think about AI as something that's abstract and maybe disembodied, but it's really something that is being created from resources that are from the Earth and is situated in a place and is altering the relationship that we have with these materials.

### Conclusion

When I think about her work, I see this kind of concern with the context and the place in which things are happening. And I think about the idea that refusals are always situated in a context and responding to things that are maybe happening in specific communities and specific cultures and as a result, no two responses that people will have even to the same type of data system will look the same.

But I think attending to that specificity is actually an important way that we push back against the way that we are often encouraged to think about AI as removed from our surrounding environments and ecologies and communities.

So I think I'll wrap it up there, and open it up for questions. But thank you for coming to this talk, and I hope you enjoyed.
