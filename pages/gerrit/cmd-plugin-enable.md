---
title: " plugin enable"
sidebar: cmd_sidebar
permalink: cmd-plugin-enable.html
---
## NAME

plugin enable - Enable plugins.

## SYNOPSIS

> 
> 
>     ssh -p <port> <host> gerrit plugin enable
>       <NAME> …

## DESCRIPTION

Enable plugins currently disabled. The plugins will be enabled by
renaming the plugin jars in the site path’s `plugins` directory from
`<plugin-jar-name>.disabled` to `<plugin-jar-name>`.

## ACCESS

  - Caller must be a member of the privileged *Administrators*
    group.

  - [plugins.allowRemoteAdmin](config-gerrit.html#plugins.allowRemoteAdmin)
    must be enabled in `$site_path/etc/gerrit.config`.

## SCRIPTING

This command is intended to be used in scripts.

## OPTIONS

  - \<NAME\>  
    Name of the plugin that should be enabled. Multiple names of plugins
    that should be enabled may be specified.

## EXAMPLES

Enable a plugin:

``` 
        ssh -p 29418 localhost gerrit plugin enable my-plugin
```

## GERRIT

Part of [Gerrit Code Review](index.html)

## SEARCHBOX

