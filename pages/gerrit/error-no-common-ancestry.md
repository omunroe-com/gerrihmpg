---
title: " no common ancestry"
sidebar: errors_sidebar
permalink: error-no-common-ancestry.html
---
With this error message Gerrit rejects to push a commit for code review
if the pushed commit and the commit at the tip of the target branch do
not have a common ancestry.

This means that your local development history and the development
history of the branch to which the push is done are completely
independent (they have completely independent commit graphs).

This error usually occurs if you do a change in one project and then you
accidentally push the commit to another project for code review. To fix
the problem you should check your push specification and verify that you
are pushing the commit to the correct project.

## GERRIT

Part of [Gerrit Error Messages](error-messages.html)

## SEARCHBOX

