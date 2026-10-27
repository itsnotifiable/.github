# GitHub rulesets

Import these JSON files into each public SDK repo (`flutter`, `react-native`, …) so only the owner can push to `main` or create tags. Everyone else opens an issue or a pull request.

## Import

1. Open the repo on GitHub → **Settings** → **Rules** → **Rulesets**
2. **New ruleset** → **Import a ruleset**
3. Import [`protect-main.json`](protect-main.json)
4. Import [`protect-tags.json`](protect-tags.json)
5. Confirm **Create** for each

`bypass_actors.actor_id` `59323287` is the owner (`iietmoon`). Only that user can push directly to `main` or create/delete tags. Collaborators must use a fork + PR (or an issue).

Publishing to npm / pub.dev is separate: keep those credentials on the owner account only. These rules block others from pushing release tags on GitHub.
