---
layout: post
title:  Knowing When to Bodge and when to do things the "Right Way"
date:   2017-06-14 00:00:00 -0400
categories: programming
---

There's a delightfully British term that I've come across in my time as a developer called "Bodging." I first heard of this term in a video by Tom Scott (included below), where he talks about how he managed to hack together a series of keyboards that let him type the entire Emoji alphabet: 

<div style="position:relative;height:0;padding-bottom:56.25%"><iframe src="https://www.youtube.com/embed/lIFE7h3m40U?ecver=2" width="640" height="360" frameborder="0" style="position:absolute;width:100%;height:100%;left:0" allowfullscreen></iframe></div>

I love the word "Bodge", because I knew exactly what it meant before I even watched the video. Some people may call it "Hacking," or 'MacGuyvering,' or maybe you just think about it as improvising. Either way, you've probably done it as a developer, be it a few (or a few hundred) times. Some examples of bodges I've seen (or done) include:

* Manually editing database tables instead of writing a migration script. 
* FTPing into a site and change some files manually instead of dealing with version control and deploying. 
* Creating large, several-dozen-lined methods instead of implementing more "proper" design patterns like Service Classes, Factories, etc..
* Repurposing an existing tool (often via copy/paste) with small tweaks 

I've known some developers to be instinctively opposed to the bodging - they'll recoil at the idea of not making their code elegant, well-tested, and as efficient as they can make it. If they bodge at all, it's out of sheer necessity, and they'll often feel dirty when doing it.

On the other hand, some developers will reach for a bodge first-thing, and only establish a more methodical approach to the problem when a task is so complex that a quick hack won't do the trick. Maybe they justify the bodge as being the fastest solution to the problem, or they're adverse to what they see as unnecessary complexity.

If I'm being completely honest, I see myself as much more of the latter developer than the former. I'm very pro-Bodge in my personal projects or when doing something that I know won't be reviewed or used by anyone but me. 

As an example, I have a small [Laravel](https://laravel.com/) project on my computer that I use solely for creating and running console commands. Why? Because I'd rather just use something like [Guzzle](http://docs.guzzlephp.org/) to make HTTP requests from my console instead of having to remember the right syntax for Curl requests.

## In Defense of the Bodge

For the example above, you could easily argue that the method above is _more_ complicated than just using Curl. I wouldn't argue with you - it most definitely has a lot more dependencies! But the important part for me is that it's _cognitively_ cheaper. It takes me less brainpower to bodge together a console command in Artisan than it does for me to remember or lookup the syntax for adding an authorization header to a curl request, and formulate a properly-organized request in my terminal.

As relatively junior developer, I find that cognitive fatigue tends to set in for me much faster than physical fatigue (or running out of time in the workday). The limiting factor in how much I can get done in a day depends far more on my ability to focus than it does on my ability to type quickly. A bodge like the one above transfers tasks in a tool that I'm not as comfortable with (writing terminal/bash scripts), and transfers it to a tool that I'm very comfortable with (Laravel/Artisan).

Now, this bodge probably wouldn't transfer well for everyone. If you're a Python developer, a PHP bodge is _way_ more inconvenient than writing out a bash script. Many of these bodges aren't very transferrable between people, so that's something to keep in mind if anyone other than yourself have to touch these bodges.

### But Am I Shooting Myself in the Foot?

I know what you're thinking - if someone like me just spent 20 minutes to learn how to create those commands the "Right Way," and maybe committed to using them for a few weeks, they could be both more effective _and_ reduce their cognitive load. And you're right. 

But here's the thing - I'm _not_ only learning how to properly use Curl from the console. I'm also trying to deliver a new feature on time for my boss, figuring out how to optimize my webpack build process, and attempting to be more mindful about writing useful tests for my application. There are a lot of competitions for my attention that are going to be a lot more useful to me (and my employer), than a couple small quirks in my workflow.

That being said, I also know I don't want to be committed to this workflow for the rest of my career. Eventually, I'll get around to learning how to do that particular task "correctly", and then maybe I'll finally abandon my bodge once and for all.

### The Ideal Bodge

The best situations for bodging are cases where you maybe only need a tool to work for one specific situation or set of parameters, you need it quickly, and you're unlikely to need the same tool again anytime soon. Those of us who  over-bodge (myself included), probably reach outside those rules more than we should. We justify that we only need something once, then we realize we could use it again in another context, or that we missed out on an opportunity to solve a broader problem.

As beginners, our parameters for a bodge are probably too wide. We overestimate how much time it will save us, we don't see the value of our work in other contexts, and we end up needing it dozens of times instead of just once. I think this is why so many developers are so stringent about following their best practices at all times - in their experience, not doing so nearly always leads to getting burned.

But if we insist on doing everything the "Right Way", it also cuts out a lot of room for experimentation. Just like bodging can lead to oversimplifying a complex tax, the "Right way" can lead us to complexify a simple task. While we may get a workable result eventually, we could potentially only solve one problem in the time a Bodger could have solved five.

Like many aspects of programming, to Bodge or not to Bodge ultimately comes down to your own personal judgement. Some of my best learning experiences in coding have come from discussing an issue that I thought could be Bodged with a colleague that saw the problem more complexly. Often times, we both realize we had flaws in the way we were thinking about the problem, and it helped us better define what needed to be in a project, and what could be simplified or removed.










