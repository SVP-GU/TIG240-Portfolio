# Contributing to TIG240 Portfolio

This guide is written for students who haven't worked with Git or GitHub before. The goal is to get your group's page added to the site without drama.

## Before the workshop

1. Make sure you have a GitHub account and have accepted the SVP-GU collaborator invite.
2. Install Git:
   - **macOS:** `git --version` will prompt to install command-line tools.
   - **Windows:** download from <https://git-scm.com>.
   - **Linux:** `sudo apt install git` (or your distro's equivalent).
3. Read this whole document once. It's short.

## How to add your group's page

### 1. Clone the repository

```bash
git clone https://github.com/SVP-GU/TIG240-Portfolio.git
cd TIG240-Portfolio
```

### 2. Create a branch

A branch lets you work on changes without touching the canonical version on `main`.

```bash
git checkout -b add-<your-park>-page
```

Replace `<your-park>` with your group's park name in lowercase, e.g. `add-hamra-page`.

### 3. Create your page

Copy `_template.md` to `docs/challenges/<your-challenge>/<your-park>.md`:

```bash
cp _template.md docs/challenges/polarization/hamra.md
```

Fill in every field according to the schema in `docs/decisions/schema.md`.

### 4. Add your group to the challenge index

Open `docs/challenges/<your-challenge>/index.md` and add a line for your group under the "Groups in this challenge" section.

This file is **deliberately shared** — every group in the challenge edits it. Conflicts will likely arise here. That is by design (see `docs/decisions/coupling.md`).

### 5. Commit and push

```bash
git add .
git commit -m "Add <park> page"
git push -u origin add-<your-park>-page
```

### 6. Open a pull request

Go to GitHub. You'll see a banner offering to open a PR for your branch. Click it.

In the PR description:

- Confirm your page follows the schema.
- Tag your **track lead** for review.

### 7. Respond to review

Your track lead may ask for changes. Make them on the same branch and push again — the PR updates automatically.

## What to do when you hit a merge conflict

If two PRs touch the same lines of the same file, the second one to merge will hit a **conflict**. GitHub will tell you. Don't panic.

1. Pull the latest `main` into your branch:

    ```bash
    git fetch origin
    git rebase origin/main
    ```

2. Git will pause and show you the conflicting file with markers like:

    ```
    <<<<<<< HEAD
    - Hamra
    =======
    - Sarek
    >>>>>>> your-branch
    ```

3. Edit the file to keep both lines (or whichever is correct), and remove the markers.

4. Continue the rebase:

    ```bash
    git add <conflicted-file>
    git rebase --continue
    git push --force-with-lease
    ```

If you're stuck: ask your track lead. If they're stuck: ask the instructor.

## Track lead workflow

If you've been nominated as a track lead for your challenge:

1. Watch the PR queue for your challenge.
2. Review each PR for schema compliance and clarity.
3. Approve and merge once it's good.
4. Help your peers resolve merge conflicts on the challenge index.
5. Maintain `docs/challenges/<your-challenge>/index.md` — keep the framing and group list up to date.
6. Review and approve PRs against class-level decisions (purpose, schema, coupling). Any track lead can merge these once approved.

## Who reviews and merges what

Branch protection requires one approval before any PR is merged into `main`. The reviewer expected for each file is encoded in [`.github/CODEOWNERS`](.github/CODEOWNERS) and summarised here:

| File pattern | Reviewer | Merges |
|---|---|---|
| `docs/challenges/<challenge>/<park>.md` | Track lead of that challenge | Track lead |
| `docs/challenges/<challenge>/index.md` | Track lead of that challenge | Track lead |
| `docs/decisions/axes-of-variation/<challenge>.md` | Track lead of that challenge | Track lead |
| `docs/decisions/{purpose,schema,coupling,schema-candidates}.md` | Any track lead (all four are tagged) | Any track lead |
| `docs/adr/NNNN-*.md` | Instructor | Instructor |
| Repo infrastructure (`mkdocs.yml`, this file, README, workflows, CODEOWNERS) | Instructor | Instructor |

Class-level decision files (`purpose.md`, `schema.md`, `coupling.md`) only change via PR with a clear reference to the class agreement they reflect. Once a class-level decision is in place, the way to revise it is to open an **ADR** under `docs/adr/`, which the instructor reviews. ADRs are the escalation valve.