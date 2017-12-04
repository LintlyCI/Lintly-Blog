---
title:  Going Python-only and Open Sourcing Flake8 Rules
date:   2017-12-04 07:00:00 -0600
categories: beta updates
---

Hello! It's been awhile, friend. There are loads of big new changes that have come to Lintly in the last few weeks. In this post I'd like to talk about those changes as well as my future plans for Lintly.

## Going Python-only

I started Lintly with the plan to make it only work with Python. Then I decided to add support for JavaScript and CSS. I think this was a mistake. I simply don't keep up with JavaScript or CSS tools enough to keep Lintly up to date.

Therefore, I've decided to make Lintly work with Python only. This way I can stay focused on the language I work with most. I can also add some really great Python-only features without needing to worry about implementing them for the other languages as well.

## Python 3 and Zappa

This shouldn't affect anyone from a usage standpoint, but you might like to know that Lintly has received some backend library updates. Lintly is now written in Python 3 and runs on Django 1.11 (just in time for Django 2.0 to be released...). Also, Lintly is now hosted on [AWS Lambda](https://aws.amazon.com/lambda/) using [Zappa](https://github.com/Miserlou/Zappa). Huzzah!

## Open-sourcing Flake8 Rules

Lintly has always supported [inline documentation](https://lintly-assets.s3.amazonaws.com/static/img/issue_viewer.png) when viewing the issues in a file. When you click on an issue a modal will pop up to explain the issue and show some examples. I couldn't find examples of each of the Flake8 violations anywhere so I had to write my own. This used to be in the main (closed-source) Lintly codebase, but today I'm [open sourcing those rules](https://github.com/lintlyCI/Flake8Rules) into a standalone website. It's called [Flake8 Rules](https://lintlyci.github.io/Flake8Rules/).

Flake8 Rules provides a description of each violation, as well as examples of incorrect and correct code. The hope is for this to be the place to go when you get a
"[Visually indented line with same indent as next logical line](https://lintlyci.github.io/Flake8Rules/rules/E129.html)" error and don't know what the heck that means.

## Plans going forward

Lintly doesn't get as much attention as I'd like to give it. Therefore I have decided to open-source as much of it as I can.

This isn't something I can do overnight. The codebase has settings that are very specific to my AWS setup. However, I am actively working towards the goal of making Lintly completely open-source. The changes I've made in the last few weeks were the first steps in that process. I'll continue to pull pieces out of Lintly and put them in new open source repos on GitHub.

## Conclusion

That's it for today. Happy (Python-only) linting!
