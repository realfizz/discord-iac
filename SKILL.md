---
name: discord-iac
description: Use when a user wants to manage their discord server via infrastructure as code
---

# Discord as code

Work in the directory you were started in. The files you write are ordinary Terraform for one guild that already exists.

Read `references/provider.md`, `references/safety.md`, and `references/permissions.md` before the first plan. Those notes are the exceptions. Everything else you can infer.

## Session

1. `git init` when the directory is not a repository. Done when `git status` runs.
2. Pin the provider from `references/provider.md`. Ask for whatever is still missing: bot token, server id, user ids. The token goes in `.env` and nowhere else. Run `scripts/doctor` in the server directory. Done when it prints `bot: in server`. 
3. Change the `.tf` files to match what was asked. Done when the diff is only that request.
4. `tofu plan`. A destroy of a channel, role, category, webhook, or message needs the user to have named that object. Otherwise stop and show the plan. Done when the plan matches the request, or the user has the refusal.
5. Apply only after that plan. Commit each slice with a conventional message. `.env`, state, and `.terraform/` stay untracked. Done when the commit exists and `git status` is clean of secrets.

NEVER read the private env variables from ``terraform.tfvars`` or ANY other env files.
