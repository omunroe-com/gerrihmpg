---
title: " gsql"
sidebar: gerritdoc_sidebar
permalink: pgm-gsql.html
---
## NAME

gsql - Administrative interface to idle database

## SYNOPSIS

> 
> 
>     java -jar gerrit.war gsql
>       -d <SITE_PATH>

## DESCRIPTION

Interactive query support against the configured SQL database. All SQL
statements are supported, including SELECT, UPDATE, INSERT, DELETE and
ALTER.

This command is primarily intended to access a local H2 database which
is not currently open by a Gerrit daemon. To access an open database use
[gerrit gsql](cmd-gsql.html) over SSH.

## OPTIONS

  - \-d; --site-path  
    Location of the gerrit.config file, and all other per-site
    configuration data, supporting libraries and log files.

## CONTEXT

This command can only be run on a server which has direct connectivity
to the metadata database, and local access to the managed Git
repositories.

## EXAMPLES

To manually correct a user’s SSH user name:

``` 
        $ java -jar gerrit.war gsql
        Welcome to Gerrit Code Review v2.0.25
        (PostgreSQL 8.3.8)

        Type '\h' for help.  Type '\r' to clear the buffer.

        gerrit> update accounts set ssh_user_name = 'alice' where account_id=1;
        UPDATE 1; 1 ms
        gerrit> \q
        Bye
```

## GERRIT

Part of [Gerrit Code Review](index.html)

## SEARCHBOX

