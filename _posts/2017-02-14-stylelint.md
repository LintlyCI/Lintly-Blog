---
title:  "CSS/SCSS support"
date:   2017-02-14 07:00:00 -0600
categories: beta updates
---

Happy Valentines Day! [Lintly](https://lintly.com) just received a new update that I think you'll love:
**CSS and SCSS support!** Support for CSS and SCSS comes courtesy of [stylelint](http://stylelint.io).

This is the first update in a few weeks. Here's a 140 character explanation why:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">I haven&#39;t had a chance to work on <a href="https://twitter.com/LintlyCI">@LintlyCI</a> much lately. I think I have a decent excuse, though. <a href="https://t.co/kNeFq792gd">pic.twitter.com/kNeFq792gd</a></p>&mdash; Grant McConnaughey (@gmcconnaughey) <a href="https://twitter.com/gmcconnaughey/status/830465212759281665">February 11, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Anyway, we'll start with a **TL;DR** for today's update:

* CSS/SCSS support via stylelint
* All project settings moved to `lintly.yml`
* Update to [flake8 3.3.0](http://flake8.readthedocs.io/en/latest/release-notes/3.3.0.html)
* Automatic repo syncing from GitHub every few hours
* The end of adding new languages/linters to Lintly ([read below](#time-to-focus-on-python) to find out more)

## stylelint

If you have a stylelint [configuration file](http://stylelint.io/user-guide/configuration/) in your
project then Lintly will respect that. Otherwise, it will add a default config file.

Lintly's stylelint support also includes in-app help for any issue you may find. Just click the "More info"
label next to an issue and a modal will display with an explanation of the issue.

## Enabling stylelint

To enable stylelint on your repo, add the following to your `lintly.yml` config file:

```yaml
linters:
  stylelint:
    enabled: true
```

## Project settings moved to lintly.yml

All project settings have been moved to `lintly.yml`. This includes Slack and email notifications, and settings to enable or disable commit statuses and PR comments. [Check out the `lintly.yml` documentation](http://docs.lintly.com/#build-configuration) to see how you can enable these features.

## Time to focus on Python

This update will mark the end of new languages added to Lintly. Why? Because there are tons of great web apps that lint all sorts of languages. Therefore, Lintly is going to start focusing _just_ on Python in order to provide the best Python support possible.

## Conclusion

If you have any feature requests or notice any bugs then head on over to the
[Lintly issue tracker](https://github.com/LintlyCI/Lintly-Issues/issues), or send us a tweet
[@LintlyCI](https://twitter.com/LintlyCI). And as always, happy linting!
