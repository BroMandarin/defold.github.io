---
layout: manual
language: en
title: How to get help
brief: This manual describes how to get help if you run into a problem while using Defold.
---

# Getting help

If you run into a problem while using Defold we'd like to hear from you so that we can fix the issue and/or help you work around the problem! There are several ways to discuss and also report issues. Chose the option that works best for you:

## Report a problem on the forum

A good way to discuss and get help with a problem is to post a question on our [forum](https://forum.defold.com). Post either in the [Questions](https://forum.defold.com/c/questions) or [Bugs](https://forum.defold.com/c/bugs) category depending on the type of problem you have. Remember to [search](https://forum.defold.com/search) for your question/issue before asking as there may already be a solution to your problem.

When you post a support question make sure to include as much information as possible. Provide [log files](#log-files), information about your operating system, steps to reproduce the problem, possible workarounds etc.

Also make sure to use a short and descriptive title. A good title would be "How do I move a game object in the direction it is rotated?" or "How do I fade out a sprite?". A bad title would be "I need some help using Defold!" or "My game is not working!".

If you have several questions, create multiple posts. Do not ask unrelated questions in the same post.

## Report a problem from the editor

The editor provides a convenient way to report issues. Select the <kbd>Help->Report Issue</kbd> menu option from within the editor to report an issue.

![](../images/getting_help/report_issue.png)

Selecting this menu option will bring you to an issue tracker on GitHub. Provide [log files](#log-files), information about your operating system, steps to reproduce the problem, possible workarounds etc.

<div class='sidenote' markdown='1'>
You need a GitHub account to submit a bug report this way.
</div>


## Discuss a problem on Slack

If you run into a problem while using Defold you can try to ask the question on [Slack](https://www.defold.com/slack/). We do however recommend that complex questions and in-depth discussions are posted on the forum. Also note that we do not accept bug reports submitted through Slack.


# Log files

The engine, editor and build server generates logging information that can be very valuable when asking for help and debugging an issue. Always provide log files when reporting a problem:

* [Engine logs](/manuals/debugging-game-and-system-logs)
* Editor logs
  * Windows: `C:\Users\ **Your Username** \AppData\Local\Defold`
  * macOS: `/Users/ **Your Username** /Library/Application Support/` or `~/Library/Application Support/Defold`
  * Linux: `~/.Defold`
* [Build server logs](/manuals/extensions#build-server-logs)
