# AGENTS.md

Guidelines for people and coding agents working in this repository. See [README.md](README.md) for an overview and [docs/design.md](docs/design.md) for the design.

## Rules

- **Do not edit Redmine:** use only Redmine's extension points (plugins, hooks, `prepend`). List replaced code in the documentation.
- **Works in any environment:** do not depend on one way of running Redmine (such as Lambda). Notes for use with redmine-serverless go in their own section.
- **No secrets in the repository:** the GitHub App's private key and webhook secrets are kept neither in this repository nor in plain text in Redmine's database (where they are kept is decided in [docs/design.md](docs/design.md)).
- **No specific companies or customers:** examples use `example.com` and similar. For the default (hosted) gateway, only the service URL goes in the default settings; prices and the operator are not written here.

## Documentation

- **Two languages.** English is the source (`README.md`, `docs/`); the Japanese translation is `README.ja.md` and `docs/ja/`, with the same file names. Change both together.
- **Layout.** The details go in `docs/`, published at https://redmine-kit.github.io/redmine_github/ with [redmine-kit/docs-skeleton](https://github.com/redmine-kit/docs-skeleton).
- **Anchors in Japanese.** Put `<a id="..."></a>` with the English heading's anchor before each Japanese heading.
- **Facts and guesses apart:** separate official documentation, what was read from source code, and guesses. Mark what has not been checked yet.
- **Decisions and proposals apart:** write undecided points as proposals, and move them to the decisions with the date they were decided.
- **Diagrams** are Mermaid, without colors or themes.
- **Japanese wording.** Plain, precise Japanese. Keep established technical terms. Do not use "版" for a version; write "通知" rather than "知らせ", and "確認" rather than "確かめる".

## Commits

- English, imperative mood, 72 characters or fewer in the first line, no trailing period.
- One purpose per commit.
- Do not rewrite pushed history.
