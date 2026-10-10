# darrenbuse

This repo is my GitHub profile README. `README.md` is the only file that matters;
it renders at github.com/darrenbuse.

## Side Projects section

The list is curated. Not every repo belongs on it, so a repo missing from the
list is a candidate to mention, never an error.

- A public repo gets a link to `https://github.com/darrenbuse/<name>`.
- A private repo appears as plain text with no link.
- Every entry has an emoji, a bold name and a one-line description that agrees
  with the repo's GitHub description.

## Keeping it current

When asked to check the README, or before editing the Side Projects section, run:

    gh repo list darrenbuse --limit 200 --json name,visibility,isArchived,description \
      --jq 'sort_by(.name)[] | [.name, .visibility, (if .isArchived then "archived" else "" end), (.description // "<none>")] | @tsv'

Compare the output with the Side Projects section and report, in this order:

1. Listed entries whose repo is missing, archived or renamed on GitHub.
2. Linked entries whose repo is now private, and plain-text entries whose repo is now public.
3. Unlisted, unarchived repos, offered as candidates.
4. Repos with no GitHub description, or one that no longer agrees with the README line.

Report first and wait for a yes before editing the README or running `gh repo edit`.
Never commit or push without a yes.

## Repo naming skill

`.claude/skills/repo-naming/SKILL.md` holds how I name repos, families of repos
and the bits that follow a name: the GitHub description, the Side Projects line
and the `gh repo create` command. It loads only when the working directory is
this repo. Its "Existing names" list is a copy kept by hand, so a repo missing
from it is a candidate to add, never an error.
