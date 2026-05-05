# Schema candidates

These two candidate schemas are anchors for the Session 1 discussion. The class is free to pick one, modify either, or design a third.

## Candidate A — minimal

Faster to fill in. Produces a thinner portfolio.

| Field | Type | Notes |
|---|---|---|
| `group_name` | string | e.g. *Hamra* |
| `challenge` | enum | one of *polarization, heal-internet, eurostack, job-automation* |
| `app_title` | string | |
| `one_liner` | string ≤ 140 chars | |
| `live_url` | URL | link to deployed prototype |
| `repo_url` | URL | link to the group's GitHub repo |
| `team_members` | list of strings | |

## Candidate B — positioning-heavy

More work to fill in. Forces each group to articulate its angle.

| Field | Type | Notes |
|---|---|---|
| `group_name` | string | |
| `challenge` | enum | |
| `app_title` | string | |
| `one_liner` | string ≤ 140 chars | |
| `problem_framing` | ~100 words | how this group defines the challenge |
| `target_user` | string | specific, not "everyone" |
| `approach` | ~50 words | method/technology summary |
| `differentiator` | ~30 words | "Unlike peers in this challenge, we…" |
| `non_goals` | list of strings | what this app is **not** doing |
| `peers` | list of group names | other groups in the same challenge |
| `live_url` | URL | |
| `repo_url` | URL | |
| `team_members` | list of strings | |
| `screenshot` | path | image in `docs/assets/` |

## Trade-off

Candidate A optimizes for short-term effort. Candidate B optimizes for the site's positioning purpose. The class chooses (or invents Candidate C). Either way, this is a *satisficing* decision — pick a good-enough schema in 25 minutes, knowing it could be improved with infinite time.