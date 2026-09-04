# Testing_Lab

## Purpose

Testing_Lab is a lightweight repository for organizing repeatable SQL Server testing work. Use it to keep setup scripts, test scripts, and reference documentation in one place so database testing is easier to run, review, and share.

## Repository layout

- `sql/setup/` - database setup, schema, and seed scripts
- `sql/tests/` - repeatable SQL Server test scripts
- `docs/wiki/` - starter content to copy into the GitHub wiki

## How to use this repository

1. Create or connect to a SQL Server instance for testing.
2. Add environment-specific setup scripts to `sql/setup/`.
3. Add repeatable validation scripts to `sql/tests/`.
4. Run scripts with your preferred SQL Server tool, such as:
   - `sqlcmd -S <server> -d <database> -i sql/setup/<script>.sql`
   - `sqlcmd -S <server> -d <database> -i sql/tests/<script>.sql`
   - SQL Server Management Studio or Azure Data Studio
5. Record longer test procedures, expected outcomes, and troubleshooting notes in the wiki.

## Wiki pages

This repository is intended to use GitHub wiki pages for documentation that changes often or is easier to browse outside the code tree.

Starter wiki content is included in `docs/wiki/`:

- `docs/wiki/Home.md`
- `docs/wiki/Running-SQL-Tests.md`

Recommended wiki usage:

- Keep executable `.sql` files in the repository.
- Keep test plans, runbooks, and troubleshooting notes in the wiki.
- Update the wiki whenever a new testing workflow is introduced.
- In GitHub, enable the repository wiki under **Settings > General > Features**, then create pages from the starter content in `docs/wiki/`.

## Branch protection

Protect the default branch for this repository (`main` today; apply the same rule to `master` if the branch name is changed) with:

- pull requests required before merging
- at least 1 approval
- resolved conversations before merge
- force pushes disabled
- branch deletion disabled

Set these protections in GitHub under **Settings > Rules > Rulesets** (or the branch protection settings for the repository).
