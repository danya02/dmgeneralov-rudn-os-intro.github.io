---
title: Version control and Git
subtitle: Choice topic for week 18

# Summary for listings and search engines
summary: Choice topic for week 18

# Link this post with a project
projects: []

# Date published
date: '2022-05-07T18:30:00Z'

# Date updated
lastmod: '2022-05-07T18:30:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.

authors:
  - admin

tags:
  - Topical
  - Week 18

categories:
  - Topical
  - Week 18
---

Modification Control Systems (VCS) allow you to track changes in your code, look through history to look for specific changes, and coordinate work on the same code base between multiple developers.
Today we will look at how one of the most popular VCS, Git, works.

# Story
Git was developed in 2005 by Linus Torvalds to help develop the Linux kernel. Shortly before this, there was a scandal with Bitkeeper, a proprietary version control system that was used by many developers, but was no longer available for free after the copyright holder found out that it was reverse-engineered to create SourcePuller.

The goals of the project were: to make a distributed VCS that could support a procedure similar to Bitkeeper, but was also fast (no more than three seconds to apply a patch) and had strong protection against errors and unintentional modifications.

# Principles

Git's primitive data structures do not necessarily implement VCS. There are two places where information is stored -- a dynamic *index* that describes the state of the working tree, and an immutable *object database*. The latter stores the following five types of objects:

- BLOB -- the content of the file, denoted by its hash. Each BLOB is a separate version of a file.
- a tree is analogous to a directory, which has links to sub-trees and BLOBs to represent one version of the working tree.
- A commit is a history element pointing to the tree it describes and one or more previous commits.
- tag - an object that has a link to some other object and some additional information about this object. Most commonly used to add digital signatures to commits.
- packfile -- a file containing several other objects in a compressed format for compactness.

Because of this design, each repository contains the entire history and can be viewed locally. This is what makes Git *distributed* VCS.

The commit history is structured as a singly-linked tree, and because the identifiers are based on a cryptographic hash of the content, this can also be thought of as a blockchain instance. Each commit can have a parent, the commit that the changes are based on. With the help of them you can go back to the history of changes. Since each commit is identified by its hash, any change in history requires the hash of each object to be recalculated further, which provides cryptographic protection against changes.

In addition to this, Git maintains a linkbase. Head objects point to the latest commit on a branch, they call the branch, and are in fact branches. One special head, called HEAD, points to the current branch from which the comparison to the working tree is being made. There are also tags, which, like head, indicate commits, but unlike them do not move, and can instead be used to mark important points in the project's history.

# History keeping process

Git does not dictate how a project's history should be maintained. One option that is supposed to be used in the OS course involves short-lived branches within which work is done to implement a new feature, and then this branch is merged into the main tree when the feature is completed. Other options include long-lived branches ranked by code stability, or branches assigned to specific team members.

Different methods have their pros and cons, which are more or less obvious depending on the type of project and the development methodology that the team uses.

# Conclusions

Git is one of the most popular VCS, and for good reason. It was written to solve problems with existing SLEs, and it was able to solve them much more effectively than any other solution at the time.

One of the factors behind its popularity has been the rise of Git hosting services such as GitHub, GitLab, and BitBucket. These services allow you to publish a Git repository and make it available from the web, and their convenience has led many users to now associate Git with GitHub.

With such popularity, ease of casual use, and yet depth of functionality for advanced use, Git is now a must for any kind of code development. That is why in the OS course we learn the basics of using Git.