# 3. We will write unit tests for all code that will test any new functionality we create

Date: 2021-07-16

## Status

Status: Accepted on 2021-07-16  

## Context

Previously written ADR tools have rarely had unit or functional tests alongside the code which
is written ([npryce's adr-tools](https://github.com/npryce/adr-tools) is a notable exception, but
is using a non-standard method of performing these tests). This means it is hard to detect when
introduced changes break functionality. With tooling like Circle-CI, Github Actions or Gitlab CI/CD
being available to us, we should use unit testing, and ensure these tests all pass before accepting
any changes to the codebase. If a change is proposed without a unit test, someone in the project
should create that or those unit tests before merging the change into the code base.

## Decision

We will use unit testing with all code which is written.

## Consequences

Additional effort will be required to write more unit tests.
