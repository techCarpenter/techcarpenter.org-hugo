---
title: "Getting Started With Hugo"
date: 2020-01-06T13:43:51-05:00
draft: false
comments: false
images:
---

The web started out as plain html files. As the web has evolved, servers and backend code provided the ability to process requests and access database values. The rise of JavaScript as the front-end language allowed for more dynamic UI. Now, with the ability to outsource server requests through APIs, static site generators have been growing in popularity.

Static site generators provide a way to get the performance benefits of truly static sites (.html files) while creating a better developer experience through templates and building the site before it is deployed. In this post, I'm going to show you how to get started with the [Hugo Static Site Generator](https://gohugo.io) so you can build your very own website and experience the benefits of working with Hugo.

## Installation

The first thing you'll have to do is install the latest version of Hugo. For this example, you'll be installing the binary file of Hugo.

1. Navigate to the [latest released version of Hugo](https://github.com/gohugoio/hugo/releases/latest).
2. Download the files that are compatible with your system.
3. Extract the files to your preferred folder. I extracted mine to `C:\Hugo`.
4. Enter the command `set PATH=%PATH%;C:\Hugo\` with your relevant path in place of `C:\Hugo`.
5. Close Command Prompt to update the environment variable.

Once you've completed these steps, Hugo will be installed and your PATH variable will be updated. Next, you'll build your first hugo site!

## Create Your Site

Creating a new site with Hugo is very simple.

1. Open your preferred command line interface (mine is [Git Bash](https://gitforwindows.org/) for Windows).
2. Navigate to the folder where you'd like to create your new site:
   - `cd C:\SiteFolder`
3. Now run the following command:
   - `hugo new site exampleSite`
4. You should see a congratulations text appear. My folder structure looks like this:
   - `C:\SiteFolder\exampleSite`

If you did receive a congratulations output from the command, then congratulations, you've created your first hugo site! Once you have your site folder created, you can add a theme to get the hang of working with hugo.

## Add a Theme

Themes provide a quick way to add styling and layouts to a new wesite in hugo.

First, browse the [hugo themes](https://themes.gohugo.io/) to find one that you like. Once you've selected a theme, follow the instructions below. This example uses the [Hermit theme](https://themes.gohugo.io/hermit/).

### For Git Users

Simply enter the following commands:

```batch
cd C:\SiteFolder\exampleSite
git init
git submodule add https://github.com/Track3/hermit.git themes/hermit
```

### For Non-Git Users

If you don't have git installed, you'll have to download the theme zip file from the repo.

1. Select 'Clone or download' and click 'Download ZIP'.
2. Extract the .zip file to get a "hermit-master" folder.
3. Rename that folder to "hermit" and move it to `C:\SiteFolder\exampleSite\themes`.

---

You should have your theme added to your site now. Just add the following line to your config.toml file:

```batch
echo "theme = \"hermit\"" >> config.toml
```

## Testing the Site
