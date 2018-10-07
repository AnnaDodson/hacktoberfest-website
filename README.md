# Hacktoberfest Website

This website is a community website for everyone to be able to contribute to. Tech should be accessible to everyone and everyone should be included in the making of it. This site aims to help break down barriers and allow people to contribute to a project with whatever skills they have.

# How to contribute

You can contribute through the browser or from your favourite terminal. Go the [contributing guide](/contributing.md) to learn how.

# Getting The Site Running

The site is built using [Jekyll](https://jekyllrb.com), a Ruby application, or **Gem**.

As such, you'll need a way to run Jekyll, to build and serve the site while you work on it.

The options for this are as follows:

- Run Jekyll in Docker
- Run Jekyll on your local machine

The sections below cover these options.

## Run Jekyll in Docker

You'll need to install Docker on your operating system.

- For **Mac** and **Windows**, install [Docker Desktop](https://www.docker.com/products/docker-desktop)
- For **Linux**:
    - Install [Docker Engine Community Edition](https://store.docker.com/search?type=edition&offering=community)
    - Also ensure you have [`docker-compose` installed](https://docs.docker.com/compose/install/)

:information_source: Ensure when you install that you are using **Linux containers**, not Windows ones (even if you're installing on Windows).

Once docker is installed, simply go to the root of the project folder in a terminal window, and run:

`docker-compose up`

The local site can be reached here: [http://localhost:4000/](http://localhost:4000/)

It will respond automatically to changes you make to the source; just refresh the page in the browser to see changes.

Well done, you're up and running! :tada:

## Run Jekyll Locally

you'll need Ruby installed (version `2.3.3` or newer).

This guide does include steps for installing Ruby, and other Jekyll dependencies, but you can always refer to Jekyll's own guide [here](https://jekyllrb.com/docs/installation/).

### Installing Ruby and other dependencies

#### Windows (native)

To install Ruby on Windows, you can

- Use **Chocolatey** (a Windows Package Manager)
    1. [Get Chocolatey](https://chocolatey.org)
    1. Open Command Prompt or Powershell
    1. `> choco install ruby -y`
- Download it from [RubyInstaller](https://rubyinstaller.org)
    1. Download **Ruby + Devkit**
    1. Run the installer

#### Mac OS X

OS X comes with many open source packages pre-installed, including Ruby. To check your version of ruby, open a terminal and run `$ ruby -v`

You should get some output like this, denoting version `2.3.7`:
```
ruby 2.3.7p456 (2018-03-28 revision 63024) [universal.x86_64-darwin17]
```

If your version is `2.3.3` or greater, you do not need to install ruby; you can move on to [Instaling Jekyll](#installing-jekyll).

Otherwise, you will need to upgrade ruby. The easiest way is to use `rvm`. In the terminal, run the following commands:
- `$ curl -sSL https://get.rvm.io | bash -s stable --ruby`
- `$ rvm install 2.3`
- `$ rvm use 2.3 --default`

Restart your terminal and check the ruby version using `> ruby -v`

#### Linux / Windows Subsystem for Linux

For Ubuntu / Debian-based distributions:

`$ sudo apt install ruby ruby-dev build-essential -y`

### Installing Jekyll

Now that Ruby is installed, installing Jekyll (and other gems) should be platform agnostic.

- :information_source: you may need to run commands prefixed by `sudo` on non-Windows environments.
- :information_source: You may need to logout / restart your terminal window to refresh paths.

Install **Jekyll** as follows, from a terminal window:

`gem install jekyll bundler`

### Install site dependencies

To ensure the site has any other gems it depends on installed, make sure you're in the project folder root and run:

`bundle update`

### Running the site

Now that everything is set up, you can run the site locally.

1. Make sure you're in the project folder root and run:
    - `jekyll serve`.
1. Leave that terminal window open
1. Head to your favourite web browser

The local site can be reached here: [http://localhost:4000/](http://localhost:4000/)

Well done, you're up and running! :tada:

### Instructions not clear?

Raise a pull request with your changes!