---
layout: post
title:  "JavaScript and Lintly!"
date:   2017-01-23 07:00:00 -0600
categories: beta updates
author: Grant McConnaughey
comments: true
---

[Lintly](https://lintly.com) just received a sweet new feature... **JavaScript support!** JavaScript
support comes courtesy of the excellent JavaScript linter [ESLint](http://eslint.org/).

You can also **lint multiple languages in the same project** now. This is a brand new concept to Lintly,
who previously only knew how to handle one language at a time.

Read on to find out the details!

## ESLint

If you have an ESLint [configuration file](http://eslint.org/docs/user-guide/configuring) in your
project then Lintly will respect that. Otherwise, it will add a default config file with the
following contents:

```json
{
    "rules": {},
    "env": {
        "es6": true,
        "browser": true
    },
    "extends": "eslint:recommended"
}
```

Lintly's ESLint support also includes in-app help for any issue you may find. Just click the "More info"
label next to an issue and a modal will display with an explanation of the issue.

![Language filter]({{ site.url }}/assets/img/javascript/eslint_issues.png)

## Enabling ESLint

To enable ESLint on your repo, add the following to your `lintly.yml` config file:

```yaml
linters:
  eslint:
    enabled: true
```

You can also explicitly enable `flake8` (Python) support by adding this:

```yaml
linters:
  flake8:
    enabled: true
```

## Multiple linters at a time

By adding support for a second language, Lintly had to learn some new tricks. Originally, Lintly was
built under the assumption that all projects it checked were Python projects. Now, however, Lintly
can potentially check both Python and JavaScript at the same time. That way your backend code and
frontend code are all kept nice and tidy.

One of the new features is an additional filter for the Files with Issues table. If you lint your
project in both Python and JavaScript then buttons will appear allowing you to view issues for either
language or both at the same time.

Here's what it looks like:

![Language filter]({{ site.url }}/assets/img/javascript/language_filter.png)

## Default linters

With today's update there is also a new concept called **Default Linters**. Default linters are what
Lintly uses when a `lintly.yml` file is not present.

If you do not specify which linters you would like to use then Lintly will make an educated guess.
The default linters are determined based on the languages your code is written in. Lintly will lint
any language that makes up at least 25% of your codebase at the time you enable the project in Lintly.

For example, if your project is made up of 75% Python, 15% JavaScript, and 10% HTML then Lintly will
only lint Python. If your project is made up of 40% Python, 40% JavaScript, and 20% HTML then Lintly
will lint both Python and JavaScript.

You can always override Lintly's guess by specifying linters in your `lintly.yml` file.

## Conclusion

If you have any feature requests or notice any bugs then head on over to the
[Lintly issue tracker](https://github.com/LintlyCI/Lintly-Issues/issues), or send us a tweet
[@LintlyCI](https://twitter.com/LintlyCI). And as always, happy linting!
