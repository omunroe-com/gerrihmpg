---
title: " gerrit ls-user-refs"
sidebar: cmd_sidebar
permalink: cmd-ls-user-refs.html
---
## NAME

gerrit ls-user-refs - List refs visible to a specific user

## SYNOPSIS

> 
> 
>     ssh -p <port> <host> gerrit ls-user-refs
>       [--project PROJECT> | -p <PROJECT>]
>       [--user <USER> | -u <USER>]
>       [--only-refs-heads]

## DESCRIPTION

Displays all refs that the specified user can see.

Allows an administrator to query which refs are visible for a user. The
command is helpful for admins when debugging why a user cannot access
certain refs and also to help admins verify that certain secret refs are
not exposed to the wrong groups.

## ACCESS

Administrators

## OPTIONS

  - \--project; -p  
    Required; Name of the project for which the refs should be listed.

  - \--user; -u  
    Required; User for which the visible refs should be listed. Gerrit
    will query the database to find matching users, so the full
    identity/name does not need to be specified.

  - \--only-refs-heads  
    Only list the refs found under refs/heads/\*

## EXAMPLES

List visible refs for the user "mr.developer" in project
"gerrit"

``` 
        $ ssh -p 29418 review.example.com gerrit ls-user-refs -p gerrit -u mr.developer
```

## GERRIT

Part of [Gerrit Code Review](index.html)

## SEARCHBOX

