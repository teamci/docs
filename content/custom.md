---
title: "Custom"
date: 2018-06-20T17:24:20+07:00
anchor: "custom"
weight: 6
---

Teams can write their own checks using the custom check. The custom
check run as Docker containers, so teams can use whatever tools or
languages they like.

Create `custom/Dockerfile` in the shared configuration repo. TeamCI
builds the Docker image and runs a container with the code under test
mounted `/data`. Exit code `0` is success, `7` is skip, and anything
else is failure.

Here's an [example][example].

[example]: https://github.com/teamci/teamci/tree/master/custom
