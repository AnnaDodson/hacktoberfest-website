---
layout: post
title: "Branding yourself: Building and deploying a website and a blog using Netlify, Hashnode and Google domains"
date: 2019-10-08 20:31:00 +0100
author: chinaza_egbo
categories: community contributions
---

So you just completed a course on programming, done some projects or perhaps working with one of the unicorns of a startup and are the "baddest" and greatest developer and software engineer to walk the surface of this planet.

Unfortunately, this knowledge and fame might only be known to you and your colleagues. It's time to rev up and put yourself out there contributing to the river of knowledge as much as you are drinking from it while also gaining new exposure and opportunities. I'm not trying to sell a product here so let's get to it.

![giphy.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1560126260962/6xnH4k_wn.gif)

We would be increasing your reach by building a website that showcases your portfolio and a blog to share your experiences at minimal cost.

Head over to [Google Domains](https://domains.google) and get a cool domain name (Yipee! I got my name: https://chinaza.dev)

![Screen Shot 2019-06-10 at 1.14.33 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1560125882762/tyawQpWu4.png)
Pay the \$12 fee and giddy up, the journey has just commenced.

So it's either you're like me who has no time building a new website from scratch or you're like them who have the patience and time. If you're like me, you can head over to [ThemeForest](https://themeforest.net) and pick a template to get started. Push some bits, make some updates and write some codes to showcase those talents and skills you have. For HTML, CSS and JS tutorials, you can head over to [codecademy](https://www.codecademy.com/) and take some lessons so you can assemble a nice looking portfolio website.

Now you have your cool looking website, we need to talk about deployment. This is where Netlify comes in. Netlify offers hosting and serverless backend services for static websites.
Deploying your site on Netlify is easy. Let's take a ride:

1. ## Add your website from git

Push your codes to git and head over to https://netlify.com to create an account. Select add a new site and specify your git provider

![Screen Shot 2019-06-10 at 1.33.50 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1560127313171/NKkMuenAf.png)

Your Git provider would prompt you to carry out some authorizations and you are good for the next step

2. ## Select your repo

![b9ea7f7c-5bfe-11e5-94a0-f957a7d1986e.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1560127517221/pifw3P6e-.png)

Select your repo and proceed to specify build parameters

3. ## Configure your deployment

![config-your-repo.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1560128542750/1d3jL6Aqa.png)
Here you get to specify the branch you wish to deploy which by default is master.
Specify the directory which holds you built files.
Specify your build command if you used a build tool or a framework like angular, react, vue...
and go ahead to click the **Build** button

Sit back and relax and let Netlify do the heavy lifting.

4. ## Attach your domain

Head over to domains.google, login and select Manage domain.
On the sidebar, select DNS and add the following custom resource records:

name: @

type: A

ttl: 1h

data: 104.198.14.52

name: www

type: cname

ttl: 1h

data: chinaza.netlify.com [This can be gotten from your Netlify dashboard. See screenshot below]

![domain.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1560260504843/HfXVcaUZU.jpeg)

Head over to domain settings on Netlify, and add domain.

5. ## Setup your blog
   Head over to hashnode.com and create an account. Follow through with the on-boarding process and select My Blog
   ![Screen Shot 2019-06-11 at 2.50.11 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1560261104676/jH59LKPpU.png)

On your blog, click on the settings icon and proceed with the following configuration for domain linking:

- Select Domain and enter your blog subdomain i.e. blog.chinaza.dev and save
- Head back to Google domains and add the following record

name: blog

type: CNAME

ttl: 1h

data: hashnode.network

If you could keep up to this point, you're a branded developer. Go forth and create content!

![giphy-downsized.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1560262801067/k9XNe19Nb.gif)
