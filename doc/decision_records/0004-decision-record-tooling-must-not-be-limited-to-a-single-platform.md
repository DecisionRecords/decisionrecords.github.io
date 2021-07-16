# 4. Decision Record tooling must not be limited to a single platform

Date: 2021-07-16

## Status

Status: Accepted on 2021-07-16  

## Context

There are currently three (that I'm aware of) "maintained" ADR/Decision Record tools that are
in general use. These are written by three disparate author groups, use three different methods
of execution, and can't (or don't) use the same template formats. This means that if you've got
decision makers who run Windows, Mac and Linux, they are unable to use the same-or-similar tools
across all three platforms.

## Decision

The same functional ideas should be written in all the desired platforms. Initially focused on:

1. Bash
2. Powershell
3. Javascript (for use in VSCode or NPM)

Other platforms may be selected at a later date.

## Consequences

A consistent set of design decisions will be written that will be applied to all platforms. A
platform will only be adopted as "Approved" once it functions similarly as on the other platforms.
