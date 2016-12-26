---
layout: post
title:  "Announcing the Lintly Beta"
date:   2016-12-25 14:44:16 -0600
categories: beta
author: Grant McConnaughey
comments: true
---

Welcome to Lintly! The [Lintly beta](https://lintly.com) is officially open to public repositories
on GitHub. Lintly is a project I have worked on for a few months now, and I'm pretty proud with how
it has turned out.

If you have the time, I'd like to tell you a little about Lintly and why I think you'll find it useful.

## What is Lintly?

Lintly is a continuous code linting tool for Python (and soon to be for other languages, as well). It
integrates with GitHub to check your code when changes are detected. The workflow currently looks
like this:

1. Import your GitHub repo into Lintly
2. Push some code to GitHub
3. Lintly will pull down your code, lint it, and keep track of any issues

During the beta, Lintly will be totally free and work only with public repositories. After the beta,
Lintly will still be free for public repositories and a paid service will be offerred for private repos.

## What is "linting"?

A really good [definition of linting](http://stackoverflow.com/a/8503586/2026351) is the following:

> Linting is the process of running a program that will analyze code for potential errors.

That's exactly what Lintly does. It analyzes your code for potential errors and style violations.
If it finds any issues, it will alert you via Slack, email, or a pull request comment. Then you'll
have the chance to fix those issues immediately.

## Why would I want to use Lintly?

It's no secret that code is read more often than its written. For this reason, code should be as
well-formatted as possible. Reading over horribly formatted code can make for a system that is
difficult to maintain (because you can't tell what it's doing in the first place!).

Lintly makes it easier to keep your codebase clean. If you push code that violates our linters, then
Lintly will politely inform you that a violation has been detected. Lintly will also provide helpful
examples and links to help you improve your code.

## Next up for Lintly

This is just the beginning. There are loads of features that will make their way into Lintly. There
will be support for other languages (like JavaScript, CSS, SCSS, and Ruby) and other linters (like
[EsLint](eslint.org), [stylelint](stylelint.io), and [RuboCop](rubocop.readthedocs.io)). There will
also be support for private repositories. Finally, I plan to add GitLab and BitBucket support at
some point.

If you would like to help steer the direction of Lintly then please create a feature request as a
[GitHub issue here](https://github.com/LintlyCI/Lintly-Issues).

## Try out Lintly

If you would like to try out Lintly, head on over to [lintly.com](https://lintly.com) and click the
big blue Register with GitHub button.

I'd love to receive tons of feedback during the beta. If you have any suggestions or notice any bugs
then simply click the Provide Feedback button over on the left, or simply head over to the [Lintly
Issues repo in GitHub](https://github.com/LintlyCI/Lintly-Issues/issues) and create a new issue.

Thanks for reading, and happy linting!
