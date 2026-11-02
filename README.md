# napbat/.github

This repository holds the default community health files for the napbat organization.
GitHub shows each file on every napbat repository that does not have its own file of that type.

| File | Purpose |
| --- | --- |
| [`SECURITY.md`](SECURITY.md) | The security policy and the procedure to report a vulnerability. |

## Keep this repository public

GitHub uses default files only from a public `.github` repository.
If this repository becomes private, every napbat repository loses its security policy.

## Private vulnerability reporting

`SECURITY.md` tells reporters to use the **Report a vulnerability** form.
The form is available only when private vulnerability reporting is enabled.
GitHub supports private vulnerability reporting only for public repositories.

The organization enables private vulnerability reporting with these settings:

- Each public repository has private vulnerability reporting enabled.
- This repository has private vulnerability reporting enabled.
  It receives reports for hosted services and private repositories.
- The `Private vulnerability reporting` security configuration is the default for new public repositories.
  It changes no other security setting.

## Check

Run this command from any directory.
The command lists each public repository that does not have private vulnerability reporting enabled.
Correct output is empty.

```bash
gh repo list napbat --visibility public --limit 500 --json name --jq '.[].name' |
  while read -r repo; do
    enabled="$(gh api "repos/napbat/$repo/private-vulnerability-reporting" --jq .enabled)" || { echo "$repo: query failed"; continue; }
    [ "$enabled" = true ] || echo "$repo"
  done
```

A query that fails prints `query failed`.
Do not read a failed query as an enabled repository.
