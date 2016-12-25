---
layout: post
title:  "Lintly Beta"
date:   2016-12-25 14:44:16 -0600
categories: beta
---

Welcome to Lintly! The Lintly beta is officially open to public repositories on GitHub. I'd like to
tell you a little about Lintly and why I think you'll like it.

## What is Lintly?

Lintly is a continuous code linting tool for Python (and soon to be other languages, as well). It
integrates with GitHub to check your code when changes are detected. The workflow currently looks
like this:

1. Import your GitHub repo into Lintly
2. Push some code to GitHub
3. Lintly will pull down your code, lint it, and keep track of any issues

During the beta, Lintly will be free and work only with public repositories. After the beta, Lintly
will still be free for public repositories and a paid service will be offerred for private repos.

## What is "linting"?

A really good [definition of linting](http://stackoverflow.com/a/8503586/2026351) is the following:

> Linting is the process of running a program that will analyze code for potential errors.

That's exactly what Lintly does. It runs programs against your code that analyze it for potential
errors. If it finds any errors, it will alert you via Slack, email, or a pull request comment.

## Why would I want to use Lintly?
