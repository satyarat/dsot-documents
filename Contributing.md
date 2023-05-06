# Contributing to Satyarat (DSoT) Documentation
​
Thank you for considering the time and effort to contribute! 🎉

## How to Contribute

Satyarat documentation is released under the [FreeBSD Documentation License](licence), and we welcome contributions. Most of the document will use [Markdown](markdown), so please be sure to check how to write content in Markdown.

Submit fixes and additions in the form of [GitHub *Pull Requests* (PRs)][pull-requests]. The general process is the typical git fork-branch-PR-review-merge cycle:

1. Fork this repository into your GitHub account
2. Make changes in a topic branch or your fork's `main`
3. Send a Pull Request from that topic branch to this repository's main branch
4. Maintainers will review the PR and either merge it or make comments

Familiarity of the tribal customs described and linked to below will help get your contributions incorporated with the greatest of ease.

## Clear commit messages

Commit messages follow a format that makes clear **what** changed and **why** it changed. The first line of each commit message should clearly state what module or file changed, summarize the change very briefly, and should end, without a period, somewhere short of 70 characters. After a blank line, the body of the commit message should then explain why the change was needed, with lines wrapped at 72 characters wide and sentences normally punctuated. Cite related issues or previous revisions as appropriate. For example:

```
ignition: Update etcd example to use %m

Make the etcd configuration example use ignition's %m instead of the
ETCD_NAME environment variable. Fixes #123.
```

This format can be described somewhat more formally as:

```
<module or file name>: <what changed>
<BLANK LINE>
<why this change was made>
<BLANK LINE>
[<footer>]
```

Where the optional `[<footer>]` might include `signed-off-by` lines and other metadata.

## Style guide

The [style guide][style] prescribes the conventions of formatting and English style preferred in this project documentation.

[licence]: Licence.md "Satyarat documentation license"
[markdown]: https://www.markdownguide.org
[style]: STYLE.md "Documentation Style and Formatting"
[pull-requests]: https://help.github.com/articles/using-pull-requests/
