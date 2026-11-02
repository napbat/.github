# Security policy

This policy applies to every repository in the napbat organization.
It also applies to the services that napbat operates under the `napbat.ca` domain.
A repository can replace this policy with its own `SECURITY.md` file.

## Security maintainer

The napbat security maintainer receives and handles vulnerability reports.

| Name | GitHub |
| --- | --- |
| Jon-Luke Biddle | [@coconutbird](https://github.com/coconutbird) |

## Report a vulnerability

Report each vulnerability privately through GitHub.
Do not report a vulnerability in a public issue, pull request, or discussion.
A public report can expose users before a fix is available.

Only you and the napbat people who manage security can see a private report.
GitHub adds you to the report as a collaborator.

### A vulnerability in a public repository

To report a vulnerability in a public repository, do these steps:

1. Open the repository on GitHub.
2. Select the **Security and quality** tab.
3. Select **Report a vulnerability**.
4. Complete the form.
5. Submit the form.

You can also open the form directly at this address:

```text
https://github.com/napbat/<repository>/security/advisories/new
```

### A vulnerability in a hosted service or a private repository

Use the form in the `napbat/.github` repository for these vulnerabilities:

- A vulnerability in a service under `napbat.ca`.
- A vulnerability in a private napbat repository.
- A vulnerability that affects more than one repository.
- A vulnerability that you cannot connect to a repository.

Open the form at this address:

```text
https://github.com/napbat/.github/security/advisories/new
```

Write the affected host name or repository name in the form.

### What to include

Give the information that follows, if you have it:

- The affected repository, package, image, or host name.
- The affected version, release tag, or commit.
- The steps that reproduce the vulnerability.
- A proof of concept.
- The effect that an attacker can get.
- Your plan for public disclosure.

A report with steps that reproduce the vulnerability is faster to assess.

## What happens after you report

1. We acknowledge your report within 5 business days.
2. We assess the report and tell you if we accept it as a vulnerability.
3. We develop the fix privately.
4. We can ask you to test the fix.
5. We release the fix.
6. For a vulnerability in released code, we publish a GitHub security advisory.
7. For a vulnerability in released code, we request a CVE identifier.

For a vulnerability in a hosted service, we tell you when the fix is in production.

We give you credit when we publish information about the vulnerability.
If you do not want credit, tell us in the report.

We send you a status update at least every 14 days until we release the fix.

## Disclosure

Keep the vulnerability private until we release the fix.
If we do not release a fix within 90 days of your report, you can disclose the vulnerability.
If we need more time, we ask you before the 90 days end.
Then we agree on a new date with you.

## Supported versions

We fix vulnerabilities in the latest release of each project.
We also fix vulnerabilities in the default branch of each repository.
We fix an older release only when the advisory identifies that release as fixed.

For a hosted service, we fix the version that runs in production.

## Scope

These items are in scope:

- Source code in napbat repositories.
- Packages and container images that napbat publishes.
- Services that napbat operates under the `napbat.ca` domain.

These items are not in scope:

- A vulnerability in a third-party dependency.
  Report it to the project that owns the dependency.
  If a napbat project uses the dependency in a way that makes the vulnerability exploitable, report that use to us.
- A vulnerability in the original code of a fork, for example `napbat/dnSpy`.
  Report it to the original project.
  Report a vulnerability to us only if a napbat change caused it.
- A report that does not show a security effect.
  For example, scanner output without a proof of concept is not in scope.

## Rules for tests on hosted services

When you test a service under `napbat.ca`, obey these rules:

- Use only accounts that you own.
- Do not get access to, change, or delete data that belongs to another person.
- If you get access to data that is not yours, stop the test and report it.
- Do not do denial-of-service tests or load tests.
- Do not send spam.
- Do not use social engineering or physical attacks against napbat people or locations.

## Safe harbor

This section applies to research that you do in good faith and that obeys this policy.

- We consider the research to be authorized.
- We do not start legal action against you because of the research.
- We do not report the research to law enforcement.
- We do not use the terms of service of a napbat service against you because of the research.
- If a third party starts legal action against you because of the research, we tell them that the research obeyed this policy.

You must still obey all laws that apply to you.
If you are not sure that an action obeys this policy, ask us in a report before you do it.

## Rewards

napbat does not have a bug bounty program.
We do not pay for reports.
