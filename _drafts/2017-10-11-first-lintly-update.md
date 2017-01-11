---
layout: post
title:  "Lintly's First Update"
date:   2017-01-11 10:00:00 -0600
categories: beta
author: Grant McConnaughey
comments: true
---

Today Lintly is getting its first update! Thank you so much to everyone who has signed up for the beta so far. Please continue to provide feedback by tweeting to [@LintlyCI](https://twitter.com/LintlyCI) or creating an [issue in GitHub](https://github.com/LintlyCI/Lintly-Issues/issues). And if you haven't signed up yet then head on over to [lintly.com](https://lintly.com).

Now let's go over the new features in Lintly.

## Project badges

Lintly now has some handy project badges that you can display in your repo's README or documentation. To get your badge, go to your project and click on the badge in the top right corner.

![Lintly project badges](/assets/img/first-lintly-update/project_badges.png)

## Improvements to running builds

Now you can see your currently running builds on the dashboard and project pages.

![See running builds](/assets/img/first-lintly-update/running_builds.png)

## Navigate to project after import

A link to your project will now display when you import the project into Lintly.

<img src="/assets/img/first-lintly-update/import_links.png" alt="Navigate to project" class="img-50">

## Bug fixes

A few bugs were squashed in this release as well:

* Changed the GitHub API scope from `user` (read/write) to `user:email` (read-only)
* Fixed a bug where projects with underscores would result in a 404
* Fixed a bug where all project owners were being set to Organization

## Next up

I'm already hard at work on the next update to Lintly. The next update will contain (drum roll please)...

**Python 3 support!**

Thanks again to everyone that has signed up for the beta. Happy linting!
