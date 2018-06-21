---
title: "Shellcheck"
date: 2018-06-20T17:25:11+07:00
anchor: "shellcheck"
weight: 4
---

This check runs [shellcheck][link] on shell programs. Shellcheck
requires an explicit list of files, so TeamCI tries to be smart enough
about matching files for shellcheck. TeamCI will shellcheck executable
files found with `git ls-files` with the following shebangs:

* `#!/usr/bin/env bash`
* `#!/usr/bin/env sh`
* `#!/usr/bin/env dash`
* `#!/usr/bin/env ksh`
* `#!/bin/bash`
* `#!/bin/sh`
* `#!/bin/dash`
* `#!/bin/ksh`

You can customize the file list by writing a custom ls files script.
TeamCI will use the output from `shellcheck/ls-files` in the
configuration repo if present. Here's an [example][example].

Shellcheck reads configuration from the `SHELLCHECK_OPTS` environment
variable. TeamCI sets to the content of `shellcheck/SHELLCHECK_OPTS`
in the configuration repo if present.

[link]: https://github.com/koalaman/shellcheck
[example]: https://github.com/teamci/teamci/blob/master/shellcheck/ls-files
