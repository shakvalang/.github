# Contributing to shakvalang

shakvalang is the Shakva programming language: [shakva](https://github.com/shakvalang/shakva) holds
the compiler (`cyc`), the package manager (`flock`), the language book and the spec. How to build and
test it: its `CLAUDE.md`; what its docs are and when a change writes there: its `docs/README.md`.

## Commits and pull requests

[Conventional Commits](https://www.conventionalcommits.org), checked by [cocogitto](https://docs.cocogitto.io)
on every commit and on the PR's title, which becomes the commit: PRs are squash-merged.

A change to the language is the spec and the code in one PR; a real choice is an ADR; something
knowingly left open is an issue labeled `question`.

## Issues and labels

Every open issue of the organization is on [one board](https://github.com/orgs/shakvalang/projects/1)
(`.github/workflows/project.yml` adds those an issue form did not), and its priority is the board's
**Priority**, not a label, as where it stands is its **Status** (Backlog, Ready, In progress,
Blocked — on another issue, upstream, or whoever opened it —, In review, Done):

| | |
|---|---|
| **P0** | broken for a user now: a wrong program accepted, a right one refused, a crash. Taken before anything else |
| **P1** | on the way to the current goal |
| **P2** | some day |
| none | not triaged yet |

The current goal: **stage 1, scripts** — a program of expressions, bindings, functions, control flow,
`struct`/`enum`, `Option` and typed errors, strings and collections, parsed and run. The parser first.
A new goal is a change of this line.

An issue's kind is its type (Bug, Feature, Task), set for the whole organization. [`labels.yml`](labels.yml)
is every repository's labels, synced by `.github/workflows/labels.yml`:

| prefix | what | |
|---|---|---|
| — | kind | the issue's **type**: Bug, Feature, Task; `question` labels an open design question |
| `E-` | effort | `E-easy`, `E-hard`, `E-help-wanted` |
| `A-` | part of the language | `A-spec`, `A-syntax`, `A-diagnostics`, `A-analysis`, `A-vm`, `A-stdlib`, `A-flock`, `A-performance`, `A-infra` |

On Mondays: triage (every issue without a priority gets one, and its `A-`), then the dependency PRs.
