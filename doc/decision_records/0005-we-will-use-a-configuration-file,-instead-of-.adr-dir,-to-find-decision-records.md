# 5. We will use a configuration file, instead of .adr-dir, to find decision records

Date: 2021-07-16

## Status

Status: Accepted on 2021-07-16  

## Context

The build of [npryce's adr-tools](https://github.com/npryce/adr-tools) used a simple text record
pointer to where the records were stored. While this is simple enough to replicate, the desired
condition of having [multiple language choices and relevant string substitution][i18n] means that
we must have some way of at least identifying which language template we want to select for string
substitutions.

[i18n]: 0002-we-will-make-the-tooling-capable-of-being-used-in-more-than-just-the-english-language.md

## Decision

A configuration file should be stored in the project root, reminiscent of the similarly functioning
.gitconfig, .vscode or .gitlab-ci.yml files.

This configuration file should store simple `key=value` pairs for such subjects as language
selection, path to the templates for the project, and so on.

This same file may also store project standard choices, like whether to append the date of changes
in status, or where to locate the template files.

## Consequences

This will break backwards compatibility with tools like adr-tools, however, gives us more
flexibility in the long run. It also encourages the cross-platform tool range, by using a
consistent set of options across a whole project...

For example, there may be a standard template library selected by an enterprise, with varying
language options, depending on the region the decision impacts. These templates could be stored
in their own git repository, and added as a submodule. The path to those templates would be
identified in the configuration file, and the language selection and format selected in that
configuration file also. Then, anyone who clones the repository containing the decision records,
while they may be obtaining a larger selection of possible templates, knows that they will all be
using the same eventual template.
