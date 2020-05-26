---
id: github
title: Github
sidebar_label: GitHub for beginners
---

# For who is this guide?

This guide is only for people that don't know how to work with git or GitHub yet. The git steps that are needed for publishing a mod on ParkitectNexus are commonly used. If you can work with git, you don't need this tutorial.

# Intro

Most programmers know how to work with git and GitHub but most other workfields have no idea what it does or how to use it. Git is a so-called version control system (vcs), vcs means that you can revert your project to any point in history and have different versions of the same project on different computers (even on the same computer). A coworker can work on one version while you're working on your own version of the project, in the end you can simply merge 2 versions in 1.

GitHub is a website that hosts git repositories, see a repository as 1 project, as long as that repository is open (open source) for everyone, hosting on GitHub is free. This makes it suitable to host the source of mods. 

**This method is only usable for small mod. If you want to create something medium-large, you should really try to [learn real git](https://try.github.io/levels/1/challenges/1)**

# Requirements

- A GitHub account, create one [here](https://github.com/join)

# How-to

## Create repository

We need to create a repository first, this repository has **one** mod that can be installed through ParkitectNexus.

![create repo](http://i.imgur.com/e11zW5h.png)

Fill in the name of your repository (mod) and add an optional description. Make sure you select that the repo is public and "Initialize this repository with a README", click on "Create repository"

![create repo](http://i.imgur.com/4KqW4ns.png)

## Uploading files

After creating the repository, click "Upload files".

![upload files](http://i.imgur.com/JRjVw7O.png)

Select all files in your mod.

![select files](http://i.imgur.com/oXzsxwh.png)

Drag them to GitHub and add a commit message. A commit message represents a short description of what you've changed since last version. Click "Commit changes"

![create commit](http://i.imgur.com/NLTbfOV.png)

## Creating Release

Now your mod is on GitHub, you do need to create a so called "release" to be able to publish your mod on ParkitectNexus, the ParkitectNexus client will **always** download your last created release.

Click the releases link.

![releases link](http://i.imgur.com/go53Psh.png)

Fill in the version of your mod (2 times) and add a short description of what changed since your last release. After that, click "Publish release".

![publish release](http://i.imgur.com/04GxGOF.png)

You're mod is now released and ready to be published on ParkitectNexus. You'll see the following screen.

![release created](http://i.imgur.com/rAFtVTk.png)

## Publish on ParkitectNexus

Copy the url of your repository, make sure you're not on the release page or something, just the url to the root of your repository.

![repo url](http://i.imgur.com/OYax8tj.png)

Now copy that in the textfield on ParkitectNexus and follow the steps! If you want to publish an update of your mod, repeat the steps of uploading and creating a release. Remember, the client will always download the latest created release.

![pn mod](http://i.imgur.com/elb1jMv.png)