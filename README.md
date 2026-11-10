# Default community health files

These files are the defaults for every repository under this account. A
repository that ships its own copy of a file overrides the default for that
file only.

```text
CONTRIBUTING.md                   contribution guide
CODE_OF_CONDUCT.md                code of conduct
SECURITY.md                       vulnerability disclosure policy
SUPPORT.md                        support guide
.github/
  ISSUE_TEMPLATE/                 default issue forms + config.yml
  PULL_REQUEST_TEMPLATE.md        default pull request template
  FUNDING.yml                     default funding links
```

## Overriding a default

Open a pull request against the affected repository and add the file you want
to override. The repository's own version always wins.

## Reporting

Security issues must not be opened publicly. See [SECURITY.md](SECURITY.md).

## License

MIT.
