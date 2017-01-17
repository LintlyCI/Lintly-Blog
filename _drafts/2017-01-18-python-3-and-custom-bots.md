---
layout: post
title:  "Python 3 and Custom Bots"
date:   2017-01-18 07:00:00 -0600
categories: beta updates
author: Grant McConnaughey
comments: true
---

Lintly received another update was released yesterday evening. The update contains several cool new
features, mostly notably (drumroll please)... **Python 3 support!**

Here's an overview of what is new:

* Python 3 support
* Support for custom bots
* The new `lintly.yml` config file

## Python 3

Previously, Lintly would only lint projects using Python 2.7. That meant that Python 3-only features
like `async def` would result in a `SyntaxError`.

Lintly now lints projects against Python 2.7 by default, but you can use the new `lintly.yml` config
file to specify the Python version you would like to use. For Python 2, Lintly will use Python version
2.7.12. For Python 3, Lintly will use Python version 3.6.0.

To start linting your projects with Python 3, add a file called `lintly.yml` in the root of your
project. The file should have this structure:

```yaml
languages:
  python:
    version: 2
```

The valid values for `version` are 2 or 3, with 2 being the default if you don't have this file. The
`lintly.yml` file will be home to future lintly configuration options. Which brings us to...

## Custom bots

The new `lintly.yml` file opens up a lot of possibilities to customize Lintly. One of the new additions
today is the concept of a custom bot account.

Before today, Lintly would always interact with the GitHub API using the account that first imported the
repository. The downside of this approach was that your precious API tokens would get used quite a
bit and could start to get rate-limited (especially if you use the GitHub API with several other services).

Now, however, you can use your own bot accounts to retrieve PR diffs, comment on PRs, create PR
reviews, and create [commit statuses](https://developer.github.com/v3/repos/statuses/).

To add a custom bot to Lintly, first login into Lintly with the bot account. You need to do this so
that Lintly will have access to the bot's API token. Next, add the following YAML to your `lintly.yml`
file (substituting `{bot_username}` with the GitHub username of your bot):

```yaml
lintly:
  bot: {bot_username}
```

With custom bot accounts you will **now have commit statuses and pull request reviews in your pull
requests**. Commit statuses only work with custom bots, as the default lintly-bot account likely won't
have permission to create them.

There is one restriction I want to point out: **the bot account must have collaborator access to your
repository in GitHub**. This is a security feature to ensure the bot account you're using really does
have the appropriate access to the repo.

## Conclusion

If you have any feature requests or notice any bugs then head on over to the [Lintly issue tracker](https://github.com/LintlyCI/Lintly-Issues/issues), or send us a tweet [@LintlyCI](https://twitter.com/LintlyCI). And as always,
happy linting!
