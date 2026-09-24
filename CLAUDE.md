# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This is a learning/practice repository for GitHub Actions. There is no application code, build system, or test suite — the only content is workflow definitions under `.github/workflows/`.

## Structure

- `.github/workflows/github-actions-demo.yml` — the GitHub quickstart demo workflow. Triggers on every `push`, runs a single job (`Explore-GitHub-Actions`) on `ubuntu-latest` that echoes context values (`github.event_name`, `runner.os`, `github.ref`, `github.repository`, `job.status`), checks out the repo with `actions/checkout@v6`, and lists the workspace.

## Running and validating workflows

- Workflows run only on GitHub after a push; the repo currently has no git remote configured, so one must be added (`git remote add origin <url>`) and pushed before anything executes.
- No local workflow tooling (`act`, `actionlint`, `gh`) is installed. If local validation is needed, install one of these first rather than assuming it exists.
- Because the demo workflow triggers on every push, any pushed commit (including edits to `CLAUDE.md`) will start a run.
