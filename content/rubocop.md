---
title: "Rubocop"
date: 2018-06-20T17:24:56+07:00
anchor: "rubocop"
weight: 2
---

This checks runs [rubocop][rubocop] on Ruby files. There are two
configuration options available: the rubocop configuration file and
the `RUBOCOP_OPTS` environment variable.

TeamCI uses `rubocop/config.yml` if present the configuration repo.
Here's an [example][example].

TeamCI sets `RUBOCOP_OPTS` to the content of `rubocop/RUBOCOP_OPTS` if
present in the configuration repo.

[rubocop]: http://batsov.com/rubocop/
[example]: https://github.com/teamci/teamci/tree/master/rubocop
