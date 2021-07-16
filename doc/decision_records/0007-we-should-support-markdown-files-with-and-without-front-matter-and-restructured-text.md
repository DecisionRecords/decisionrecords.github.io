# 7. We should support markdown files with and without front matter and restructured text

Date: 2021-07-16

## Status

Status: Accepted on 2021-07-16  

## Context

Decision record tools should support whatever platform is being used for static site generation.
Two main markup formats have been widely selected, which are `md` "Markdown" and `rst`
"Restructured Text" files. Several static site generators use these formats, but in addition, they
often also use a data structure at the start of the file, called "front matter", which is used to
render the document in the static site generation tool.

Front matter looks a bit like this:

```md
---
title: Some document
date: "1970-01-01"
---
This is the actual content of that document.
```

This structure allows the static site generator to add metadata to the simple files, either to
inject navigation structures into the file, or to add tagging of resources, but either way, if
your tooling supports or even demands these file formats and layouts, this this tool should support
your requirement.

## Decision

By default, all templates will, initially, be written with markdown and restructured text formats
in mind. Unit tests should support all four delivery options:

1. Markdown, no front matter
2. Markdown with front matter
3. Restructured Text, no front matter
4. Restructured Text with front matter

## Consequences

More unit testing, more potential complexity, but ultimately, a better set of options for those
wishing to adopt decision records.
