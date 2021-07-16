# 2. We will make the tooling capable of being used in more than just the English language

Date: 2021-07-16

## Status

Status: Accepted on 2021-07-16  

## Context

All of the ADR tooling I have found is written in, and for, English speakers. If this tool is to
have more application outside architectural purposes, it should appeal to people who do not use
computers in English. As such, the tool should support the use of non-English templates and string
substitutions.

## Decision

The initial builds will all support English, German, French, Spanish, Chinese and Japanese
languages, even if those initial builds use tools like Google Translate to perform this creation.

## Consequences

It means introducing more code to support these languages.
