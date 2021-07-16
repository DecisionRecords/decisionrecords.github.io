# 6. We will provide several status options when generating a new decision record

Date: 2021-07-16

## Status

Status: Accepted on 2021-07-16  

## Context

In older ADR tools, the three "main" statuses are:

1. Accepted
2. Proposed
3. Superseded

This range does not provide all the available options that an organisation may need.

## Decision

This project will implement the following options.

1. Work in Progress
2. Proposed
3. Accepted
4. Amended
5. Superseded
6. Deprecated
7. Linked

The three main items, "Work in Progress", "Proposed" and "Accepted" will be primary options, and
are mutually exclusive.

The four subsequent items, "Amended", "Superseded", "Deprecated" and "Linked" will be allowed as
many times as are required, and will be added after the "main" status items, like this:

```text
Accepted
Superseded by [11. A later decision on the matter](0011-a-later-decision-on-the-matter.md)
Linked to [29. Why we superseded several records](0029-why-we-superseded-several-records.md)
Deprecated by [190. We selected a whole separate methodology](0190-we-selected-a-whole-separate-methodology.md)
```

## Consequences

Arguably, this change does not stray too far from tools such as adr-tools, however, as the decision
is made and will apply to [several platforms][several platforms], it should be consistently applied
to all the versions released.

[several platforms]: 0004-decision-record-tooling-must-not-be-limited-to-a-single-platform.md
