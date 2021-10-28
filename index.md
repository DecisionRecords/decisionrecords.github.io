---
layout: home
title: Decision Records
---
Once a fragmented mess, now we're trying to make Decision Records a bit easier,
one implementation at a time.

## Work in Progress

* [Rust](https://github.com/DecisionRecords/rust-decision-records)
* [Bash](https://github.com/DecisionRecords/bash-decision-records)
* [Javascript](https://github.com/DecisionRecords/javascript-decision-records)

## Principles

All Decision Records scripts will all be implemented to use the same standards.

1. The script stores its documents (referred to as `DOC_ROOT`), by default, in `doc/decision_records`
  1. If there is a `.decisionrecords-config` file, in which it defines the decision record path, this will be used by preference.
  2. If there is a `.adr-dir` file, the path written in that file will be used as the next preference.
  3. If there is no configuration file, it will also look for `doc/adr`, and will use that as the last preference.
  4. If the above configuration files and paths do not exist, it will fall-back to `doc/decision_records`.
2. The script stores the template, by default, in `DOC_ROOT/.templates`. This is configurable by setting a value in `.decisionrecords-config`.
3. The script stores the template as, by default, `template.LANGUAGE.FORMAT`, where language defaults to `en-GB` and format defaults to `md` (MarkDown). These are all also configurable by setting a value in `.decisionrecords-config`. If there is also a file `TEMPLATE_NAME.LANGUAGE.ref` in the same directory, this will be used to see what the translation strings are to search for, allowing for translation opportunities.
4. The script will allow for the following commands:
  * `init`: create the `DOC_ROOT` and `TEMPLATE_ROOT` path, insert the template and language reference files in there, and create the config file.
  * `new`: create a new decision record in the `DOC_ROOT` path, using the template.
  * `approve` and `proposed`: change the status of an existing decision record from `proposed` to `approved` and vice versa.
  * `supersede`, `deprecate`, `amend` and `link`: indicate that a decision record has a relationship to another decision record.

A mid-term aim of the script is to allow internationalization of these scripts, but so far, this has not been a design priority. PRs will be welcomed!
