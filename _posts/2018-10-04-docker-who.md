---
layout: post
title:  "Docker Who"
date:   2018-10-04 21:17:00 +0100
author: jon_couldridge
categories: community docker
---

Documenting *Getting Started* on a project is hard. You want to give the absolute simplest directions for getting a quick result, while simultaneously not missing anything important out, and catering to all possible scenarios that someone wishing to *Get Started* might find themselves in. 

There are three intended takeaways from the ramble that follows, and they relate to *Getting Started*, and also actually **getting started**:
1. Understand, and believe in, the **Docker** sell
2. Dispel the **Docker** fear
3. Love **open source** :heart:

## The Sell
- What if you didn't need to write a *Getting Started* guide that first has to cover installing Ruby in multiple environments, before it even gets to setting up the build system to run the site you want to *Get Started* with?
- What if you didn't need to *read* that same complicated guide?
- What if you knew that the setup *you* run the site under is exactly the same as *everyone else*?

That's the sell of **Docker**, plain and simple.

The "Run Locally" section of *Getting Started* has sections for different OSes, that eventually converge into some further platform agnostic instructions.

The **Docker** section has basically two instructions:
1. Install **Docker**
2. Run a single command

*That* section was a lot easier to write; is it easier to read?

The hidden bonus, is that the exact same setup steps happen for you wherever you run it - inside **Docker**, everyone is the same, all running (in this case) on a minimal Linux installation with exactly the same components (and versions of components) that run the site. No more "it works on my machine".

## The Fear
**Docker** and **Containerisation** are big buzzwords, and the technology can be quite something to get your head around, letting alone getting started using it.

Don't be afraid, just ease yourself in by using projects that use it. You don't need to go all in and setup a complex n-tier stack with multiple environments right away. Start by getting a simple project that can run inside **Docker** on the go. Then familiarise yourself with using it in that role. Walk before you can run. There's nothing to be afraid of; just take it easy.

## The Love
When I started trying to get the site to work in **Docker** for local development, I was initially going to do quite a bit of work. I knew how to get it running locally on an actual machine, and I know how to write a `Dockerfile`, so I was going to start with a base Linux image, and follow the steps to get the site building, finally adding the ability to mount the local project directory for live changes without rebuilding.

As I worked towards this goal, there were a few steps along the way where I stopped to think "Someone's probably already done this."

First of all, there is an official **Jekyll** container image. So I didn't have to start from scratch, I could just mount the directory and run `jekyll serve` after installing the site dependencies, and configuring ports.

Then I found that someone had already done *that* work, and published a derived container image. And provided a configuration file.

So what started out as a lot of work really became taking an existing configuration file, modifying it slightly, and including it in the site's repository.

And now *Getting Started* is easier for everyone.

Love open source. Don't reinvent the wheel: depend upon the community, and give back to the community. We're better together.

That sounds like Hacktoberfest spirit to me.