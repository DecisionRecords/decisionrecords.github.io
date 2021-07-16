# 1. We will use the name Decision Records instead of Architecture Decision Records

Date: 2021-07-16

## Status

Status: Accepted on 2021-07-16  

## Context

The term "Architecture Decision Record" implies this decision is made about the architecture of a
solution, whereas I want this to be about any decision which is made. While "Any Decision Record"
still matches the acronym ADR, this allows us to be more specific that it's "just" a decision, not
anything to do with architecture.

## Decision

To use the term "Decision Record" rather than "Architecture Decision Record" or "Architectural
Decision Record". This will use the acronym "DR" instead of "ADR", however, this will be minimally
used, and largely targetted at internal function and variable names.

## Consequences

There is a risk of being harder to find, due to the term "DR" being heavily used in IT, meaning
disaster recovery. As people are more likely to spell "decision record" than "architecture decision
record", we will use the long form in all scripts and documentation.
