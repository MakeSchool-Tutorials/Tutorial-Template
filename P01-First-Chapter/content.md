---
title: "Writing the First Chapter"
slug: first-chapter
---

Make School tutorials should have a consistent flow, which starts by stating all expectations of a tutorial upfront in the first chapter. This is a short guide to structuring the first chapter of a tutorial so that students are fully aware of what they're building, why they're doing it, what they need to know before diving in, and a reminder of tools to use.

**This entire file can be cloned for the header sections, formatting as well as for specific copy, such as the git/github or Learning Outcomes section.**

# Overview

Use this section to give a brief overview of what the students will be building in the tutorial. This should summarize what the student will build and what tools they'll use.

A screenshot or video of the final product should be shown here as well, so that students can get a preview of the end product that they'll be building.

**When copying this for your tutorial, remember that since this is the first section, you don't need a header**

# Why Is This Important

Use this section to concisely covey to students why this topic is important for them to learn. This should be tied to industry examples, or fundamentals of the course. Try to keep this brief, and possibly include an action block asking them to think of examples they see of this in industry.

# Prerequisites

This section should outline any prerequisites for understanding the material and link to resources for getting up to speed.

Resources can include (but are not limited to):

- Class slides/materials
- Previous tutorials
- Outside references (articles/tutorials not from Make School)

# Learning Outcomes

List 5-8 learning outcomes for the tutorial. These should concepts or ideas that the student should now have a solid understanding of by the end of the tutorial (example: Understand how WebSockets work within a server/client relationship through socket.io).

Be sure to use the language from the _Student Learning Outcomes_ (PDF Page 30) chapter of the [WASC Program Assessment Binder](https://drive.google.com/open?id=15GeE0LsGH73TNk2BVHd8VgbKnDb80N2j). Specific action verbs are given on PDF pages 35-36.

The following format should be used for this section. Copy/paste this into your tutorial:

```
By the end of this tutorial, you should be able to...

1. Learning Outcome 1
1. Learning Outcome 2
1. Learning Outcome 3
1. Learning Outcome 4
1. Learning Outcome 5
1. Learning Outcome 6
1. Learning Outcome 7
1. Learning Outcome 8

>[action]
> Take a moment to write down these learning outcomes and reflect on them. Make sure that as you progress through the tutorial that you're furthering your understanding, and that by the end, you have completed all of the outcomes.
```

# User Stories/Technical Planning

**This may not be applicable to every tutorial, but it is if they're building an end product (Reddit clone, slack clone, Product Hunt reader, etc.)**

To get students in the habit of understanding user stories for building an app, provide them with a list upfront. _We want User Stories to be the requirements on building their product/app, whereas the Learning Outcomes represent the knowledge gained from building the product/app._

The following format can be used for this section. Copy/paste this into your tutorial and adapt as needed:

```
# User Stories

Here is what we need to accomplish in order to build PRODUCT_NAME.

Remember that we need to think of these from the user's perspective, so we will be writing the requirements as User Stories:

1. As a PERSONA, I want to ACTION so that REASON
1. As a PERSONA, I want to ACTION so that REASON
1. As a PERSONA, I want to ACTION so that REASON
1. As a PERSONA, I want to ACTION so that REASON
...
```

```
# Technical Planning

Here is what we need to accomplish in order to build PRODUCT_NAME:

1. Build this component
1. Hook up the backend
1. Write Tests
1. Style this view
...
```

# Using Git/GitHub

Good to remind students to set up a git repo for their code and to commit along the way (more on commit reminders in the next section).

**For all 1.1 and 1.2 classes, please use the following text for this section**

```
# Using Git/GitHub

As you go through this tutorial, you will also be making commits after completing milestones. This is a requirement, you must make a commit whenever the tutorial prompts you. This not only further enforces best practices for software engineering, but also will help you more easily figure out where a bug originated from if you break your progress up into discrete, trackable chunks.

When prompted to commit, you'll see a sample commit message. Feel free to use your own message, so long as it clearly and concisely covers the work done.

Lastly, the commit prompts in this tutorial should be the minimum amount of times you commit. If you want to do more commits, breaking your chunks into even smaller chunks, that is totally fine!
```

**For all 1.3 and higher classes, please use the following text for this section**

```
# Using Git/GitHub

Much like we've done in earlier tutorials, make sure you're committing your code as you complete milestones. At a minimum, you should make a commit whenever the tutorial prompts you.
```

# Git Setup

The following can be used for the first chapter to make sure students set up Git/GitHub for their tutorial. Remember to update the commit message and REPO-NAME to something relevant, and to remove the `\`:

## If there is NO starter code

```
# Set Up Git/GitHub

Set up your repo!

>[action]
> Make your first commit
>
\```bash
$ git init
$ git add .
$ git commit -m 'project init'
\```

Now Go to GitHub and create a public repository called REPO-NAME, and now associate it as a remote for your local git project and then push to it.

>[action]
> Push it!
>
\```bash
$ git remote add origin GITHUB-REPO-URL
$ git push origin main -u
\```

```

## If there IS starter code

Remember to update the commit message, update the ALL_CAPS_WORDS to something relevant, and to remove the `\`:

```
# Set up Git/GitHub

Set up your repo!

> [action]
> Go to the [starter repo](LINK_HERE_TO_REPO) and clone the repo locally
>
\```bash
$ git clone [URL to your starter repo]
\```

Now we need to change the remote so that you can commit/push/pull the changes you make to your own repo. **It is very important you do the below steps in order to get everything working properly.**

> [action]
> Go to GitHub and create an _empty_, public repository called REPO-NAME, and now associate it as a remote for your cloned starter code, and then push to it.
>
\```bash
$ cd NAME_OF_REPO
# can grab the url from the "Clone or download" link on your repo page
$ git remote set-url origin git@github.com:YOUR_USERNAME/REPO-NAME
$ git push -u origin main
\```

Go to your repo on GitHub and make sure your previously empty repo is now full with starter code! Now when you add/commit/push, it'll be to your repo!

```
