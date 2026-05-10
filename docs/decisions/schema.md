# Schema

> **Status:** Decided by the class in Session 1.
> **TODO:** Replace this placeholder with the agreed schema. Until that is done, the schema is *unspecified* and `_template.md` cannot be filled in.

The schema is the **architectural contract** between groups. It defines what fields every group's page must contain, in what format. Once it is set, every group can work in parallel on their own page without coordinating with anyone.

The class chooses the schema in Session 1 — see [Schema candidates](schema-candidates.md) for the two anchor proposals brought into that discussion.

## Decision

Vo kommer överens om att använda Schema A från de exempel som fanns tillgängliga. 

## Required fields

Field,	Type,	Notes

group_name,	string,	e.g. Hamra

challenge,	enum, one of polarization, heal-internet, eurostack, job-automation

app_title,	string

one_liner,	string ≤ 140 chars	

live_url, URL link to deployed prototype

repo_url, URL link to the group's GitHub repo

team_members, list of strings	

## Optional fields

Inga fält i schemat är frivilliga. 

## Notes on enforcement

- Pull requests ska granskas innan merge.
- Reviewers kontrollerar att alla obligatoriska fält i schemat är ifyllda.
- Felaktiga eller ofullständiga schemafält ska rättas innan godkännande.