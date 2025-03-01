# README

This README would normally document whatever steps are necessary to get your application up and running.

## What is this repository for?

* This is a repo to store my website+ blog. I will use pipelines to push to the github pages repo.
* [Theme](https://adityatelange.github.io/hugo-PaperMod/posts/papermod/papermod-installation/)

## How does this work:

* Updating the theme: `git submodule update --remote --merge`
* Writing blog posts in draft mode: with the draft: true
* Run with `hugo serve -D`
* Publishing changes: remove the draft flag.
* Deployment instructions: go to the public folder and `git add commit push`

To deploy simply . Using git
modules is much much simpler than using the nightmare that is git actions. I had
some `Error loading key "/home/runner/.ssh/github": error in libcrypto`. Which I
dk how to solve. But submodules is a great solution, which I can live with.

## Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines

## Who do I talk to? ###

* Repo owner or admin
* Other community or team contact
