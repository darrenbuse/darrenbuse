# darrenbuse

This file provides guidance to Claude Code when working with code in this repository.

This repo is my GitHub profile README. `README.md` is the only file that matters;
it renders at github.com/darrenbuse.

## Setup

    npm install                                            # husky, which runs the commit hook
    npm install -g commitizen cz-conventional-changelog    # commitizen, which the hook calls

## Side Projects section

The list is curated. Not every repo belongs on it, so a repo missing from the
list is a candidate to mention, never an error.

- A public repo gets a link to `https://github.com/darrenbuse/<name>`.
- A private repo appears as plain text with no link.
- Every entry has an emoji, a bold name and a one-line description that agrees
  with the repo's GitHub description.

## Keeping it current

When asked to check the README, or before editing the Side Projects section, run:

    gh repo list darrenbuse --limit 200 --json name,visibility,isArchived,isFork,description \
      --jq '[.[] | select(.isFork | not)] | sort_by(.name)[] | [.name, .visibility, (if .isArchived then "archived" else "" end), (.description // "<none>")] | @tsv'

Compare the output with the Side Projects section and report, in this order:

1. Listed entries whose repo is missing, archived or renamed on GitHub.
2. Linked entries whose repo is now private, and plain-text entries whose repo is now public.
3. Unlisted, unarchived repos, offered as candidates. Forks are skipped unless asked for.
4. Repos with no GitHub description, or one that no longer agrees with the README line.

Report first and wait for a yes before editing the README or running `gh repo edit`.
Never commit or push without a yes.

## Commits

Commit messages follow conventional commits, `type(scope): subject` with a body,
the shape the commitizen hook produces. The hook needs a terminal, so a commit
made from Claude Code skips the prompt and the message has to be written in that
shape by hand.

## Repo naming skill

`.claude/skills/repo-naming/SKILL.md` holds how I name repos, families of repos
and the bits that follow a name: the GitHub description, the Side Projects line
and the `gh repo create` command. It loads only when the working directory is
this repo. Its "Existing names" list is a copy kept by hand, so a repo missing
from it is a candidate to add, never an error.
