# Contributing

Please contribute! 

If this is your first time, follow the steps listed below. Or if you're familiar with the process, TLDR: Fork the repository, commit your changes then raise a PR! If you're closing an issue, mention the issue number in the branch name and PR.

## Contents
1. [Code Contributions Through Git](#code-contributions-through-git)
   1. [Fork and Clone the Repo](#fork-and-clone-the-repo)
   2. [Adding a Blog Post](#adding-a-blog-post)
   2. [Raising Your Pull Request](#raising-your-pull-request)
2. [Contributions Through the Web Browser](#contributions-through-the-web-browser)
3. [Jekyll Theme](#jekyll-theme)


## Code Contributions Through Git

## Fork and Clone the Repo

First, follow this [step by step guide](https://guides.github.com/activities/forking/) to fork the repository and then clone it so you have a copy on your local computer.

If you've never used GitHub before, you'll need to add ssh keys to communicate to GitHub from your computer. Full steps [here](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/).

Make sure you have your keys set up before continuing.

Next, open a terminal wherever you want the project directory to be and run:

```
$ git clone https://github.com/<your-username-goes-here>/hacktoberfest-website/
```

Replace the URL with your own repository URL path. If you're not sure what it is, go to GitHub where you forked the project and check your repository home page for the full URL.

Once that's cloned, cd into the new project:

```
$ cd hacktoberfest-website/
```

To make sure your fork knows which is the upstream repository, run:

```
$ git remote add upstream git@github.com:AnnaDodson/hacktoberfest-website.git
```

This means if there are any changes to the main branch you can get them by running the following:

``` 
$ git fetch upstream

$ git checkout master

$ git merge upstream/master

 ```

It's good practice to do this often and make sure your branch is up to date before raising your PR.

If you ever want to check your origin and upstream, you can run the following:

```
$ git remote -v 
```

There are some more in-depth instructions [here](https://help.github.com/articles/fork-a-repo/) that you can take a look at if you want some further reading.

To make your changes, you'll want to create a new branch to work on. Use a descriptive branch name with no spaces, capital letters or special characters. If you're working on an issue, mention the issue number.

```
$ git checkout -b post/my-blog-post
```

Woohoo, you're all ready! Follow the instructions in the README to get the site up and running locally.

## Adding a Blog Post
To add a post, create a file under the `_posts/` directory. Name the file with the date and title like so `YYYY-MM-DD-title`:

```
_posts/2018-10-01-my-epic-post-title.md
```

This is a markdown file so you can use markdown syntax. You can also add HTML tags too.

In the file, make sure to include all your posts details:

```
---
layout: post
title:  "My Epic Post Title"
date:   2018-10-01 14:01:10 +0100
categories: community contributions
---
```

Follow the documentation [here](https://jekyllrb.com/docs/posts/) for more details, including some handy markup syntax if you're not familiar with it.

### Raising Your Pull Request

Once you've created your blog post, fixed an issue or added a feature it's time to commit your changes and raise a pull request.

To make a commit, first check what files you've changed or added:

```
$ git status
```

You'll see all the files you've either edited or added.

Before committing, it's always good to check you're on the right branch.

```
$ git branch
```

If you want to switch branch:

```
$ git checkout <branch-name>
```

Add `-b` after `checkout` if you want to make a new branch. Then to commit the files you want, add them by running:

```
$ git add _posts/my-epic-post-title.md

// or to add them all, you can run this

$ git add .
```

Then commit them:
```
$ git commit -m "Adding my blog post"
```

You can enter any other details that you think are necessary too.

Once you've committed, you push!
```
$ git push origin <your-branch-name>
```

Also see [here](https://help.github.com/articles/adding-a-file-to-a-repository-using-the-command-line/) for more information.

If you go over to GitHub in your browser, you should see a flag appear in your fork about raising a PR - click that and follow the instructions. Don't forget to add a good message explaining what you have done in your merge. [More details here](https://help.github.com/articles/creating-a-pull-request/)

If at any point you're confused or lost, speak up and get in touch!! You can respond to an issue if you're working on one or email me, tweet me or find me on tech Nottingham slack. Don't give up or keep quiet, I want to help.

## Contributions Through the Web Browser

If coding isn't your day job but you want to contribute your story, follow the steps below.

First, follow this [step by step guide](https://guides.github.com/activities/forking/) to fork the repository and then clone it so you have your own copy on your GitHub profile.

Once you're on your fork of the repo, click Branch to make a new branch for you to add your work to.

![alt text][one-branch]

Make sure you're on the right branch. It likes to switch back a lot - so always check before adding or editing anything.

![alt text][two-branch]

To upload a blog post, click into the `_post/` directory and then click to create a new file:

![alt text][three-new-file]

Name the file with the date and title like so:

```
2018-10-01-my-epic-post-title.md
```

This is a markdown file so you can use markdown syntax. You can also add HTML tags too.

In the file, make sure to include all your posts details:

```
---
layout: post
title:  "My Epic Post Title"
date:   2018-10-01 14:01:10 +0100
categories: community contributions
---
```

![alt text][four-post]

To upload images, choose `Upload Files`:

![alt text][three-new-file]

And link to them from your page. Follow the documentation [here](https://jekyllrb.com/docs/posts/) for more details, including some handy markup syntax if you're not familiar with it.

When you're happy and ready to commit (check you're on the right branch first!), scroll to the bottom of the page and add a commit message:

![alt text][five-commit]

[one-branch]: repo-images/one-branch.png "Add a branch"
[two-branch]: repo-images/two-branch.png "Check which branch you're on"
[three-new-file]: repo-images/three-new-file.png "Create a new file"
[four-post]: repo-images/four-post.png "Add writting or images"
[five-commit]: repo-images/five-commit.png "Add commit message"

Once all your files have been committed, raise a PR against the [main repo](https://github.com/AnnaDodson/hacktoberfest-website)! You should see a flag appear in your fork about raising a PR - click that and follow the instructions. Don't forget to add a good message explaining what you have done in your merge. [More details here](https://help.github.com/articles/creating-a-pull-request/)


### Jekyll Theme
This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](https://jekyllrb.com/)

You can find the source code for Minima at GitHub:
[jekyll][jekyll-organization] /
[minima](https://github.com/jekyll/minima)

You can find the source code for Jekyll at GitHub:
[jekyll][jekyll-organization] /
[jekyll](https://github.com/jekyll/jekyll)


[jekyll-organization]: https://github.com/jekyll
