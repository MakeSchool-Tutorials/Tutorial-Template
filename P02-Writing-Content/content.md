---
title: "Writing Content"
slug: writing-content
---

Each tutorial is going to be different in terms of how it's broken up, what the content looks like, etc. But with that, there should be some consistencies that exist within every chapter of a tutorial. The following sections outline specific sections and general concepts to include with every tutorial.

# Highlighting Big Ideas/Vocab

Make sure to **bold** new vocab/terminology as well as _underline_ key phrases in the definition of the term.

New ideas should always be explained assuming 0 previous knowledge of the idea, and the bare minimum in background knowledge required for the new idea.

# Breaking up Content

After the intro/overview chapter, the tutorial should continue with the core content. Longer chapters should be broken up into multiple chapters.

Each `h1` header (headers created with a single `#`) will create a new tutorial step (with it's own "Mark As Complete" button). Make sure each step makes sense as a step. All the content in a step should be related but short enough to be digestible.

# Using the Action Highlight Boxes

Make sure to utilize the action highlight boxes to help break up just staring at walls of text:

- **Action:** for when they need to do something (write/copy code, run terminal command, etc.)
- **Solution:** for when you want to hide/show a solution
- **Challenge:** extra for experts, tasks for students who want to go the extra mile
- **Info:** for adding non-essential information to a concept/idea/function/etc.
_ **Quote:** for adding quotes

# User Story Checklist

Make sure to remind students of their user stories, and which ones they're going to be working on by **bolding** them, and then ~~cross off~~ the ones that have been completed.

If possible, try to break down the user story as well into sub-tasks, which can just be sub-bullets in the list

This should be one of the first sections of a tutorial. An example is below for a student who has finished the first 4 user stories and is about to start the 5th in this chapter:

1. ~~Create a post~~
1. ~~Show all posts~~
1. ~~Show one post~~
1. ~~Comment on posts~~
1. **Create subreddits**
    1. Add a `subreddit` attribute to our post resource
    1. Navigate to view all the posts of the same subreddit
1. Sign up and Login
1. Associate posts and comments with their author
1. Make comments on comments
1. Vote a post up or down

# Git Commits

Students need to be prompted to commit their work and push to GitHub. This should happen at a _minimum_ of once per chapter, but feel free to include more if you feel it is needed.

The following can be used for each section of a chapter. Remember to update the commit message and REPO-NAME to something relevant, and to remove the `\`:

```
# Now Commit

>[action]
>
\```bash
$ git add .
$ git commit -m 'Commit Message'
$ git push
\```
```

# Learning Outcome Reminders

Be sure to alert students at the end of a chapter if they've achieved (or even worked on) a Learning Outcome. Can be a simple affirmation such as the following (with the marked parts replaced):

Great job! By doing `this action`, you've successfully `COMPLETED_LEARNING_OUTCOME_1`!

Make sure to **bold** the Learning Outcome when doing this.

# Test Chapters/Sub-Sections

Try to include code tests as either 1-2 chapters in the tutorial, or as sub-sections throughout chapters. These can be unit tests, integration tests, etc. We just want to ingrain testing as a best practice into students, and our tutorials should reflect that.

Check out the [Rotten Potatoes Testing Chapter](https://www.makeschool.com/academy/track/rotten-potatoes---movie-reviews-with-express-js/tutorial/adding-tests) for an example of this in action.
