---
title: '1000: Documentation Platform'
description: How notes are kept
linkTitle: '1000: Doc Platform'
date: 2025-01-01
---

## Context

As we build out the SCALE A/V platform, we need a place to keep track of notes.

### Considerations

- **Docs-as-Code** use the same workflow that developers are familiar with and lives next to the source code. This makes it more likely that the documentation is kept up-to-date.
- **Markdown** is a minimal markup language; most developers are familiar with it.

## Decision

To use [Hugo] with the [Docsy] theme.

[Hugo] may be the most popular static generator. [Docsy] is well designed and developed by Google.

## Alternatives

### [Material for MkDocs]

[Material for MkDocs] is a popular and powerful theme for [MkDocs]. [MkDocs] has a smaller community than [Hugo] and has fewer options out of the box.

### [Docusaurus]

[Docusaurus] is a [React](https://reactjs.org/) application. Users need knowledge of the [React] framework in order to make configuration changess and customizations.

### [Gatsby]

[Gatsby] is a popular static generator. Unfortunately, a well supported theme for documentation was not found.

### [GitHub Wiki]

[GitHub Wiki] is backed by the Ruby based static site generator, [Gollum]. It comes with a frontend, reducing friction for novices getting started.
It is not clear how to easily use CI gates with GitHub wikis. Customization are limited. Also, the presentation is basic and not the most intative to navigate.

<!-- LINKS -->

[docsy]: https://www.docsy.dev/
[Docusaurus]: https://docusaurus.io/
[Gatsby]: https://www.gatsbyjs.com/
[GitHub Wiki]: https://docs.github.com/en/communities/documenting-your-project-with-wikis/
[Gollum]: https://github.com/gollum/gollum/
[hugo]: https://gohugo.io/
[mkdocs]: https://www.mkdocs.org/
[Material for MkDocs]: https://squidfunk.github.io/mkdocs-material/
