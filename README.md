This repository contains the Vale style linting tests for Chef Documentation.

[Vale](https://docs.errata.ai/)
[Microsoft Style Guide](https://docs.microsoft.com/en-us/style-guide/welcome/)
[Microsoft Vale](https://github.com/errata-ai/Microsoft)

We have copied the lint files from the Microsoft Vale into our repository. We have made changes to some Microsoft lints and added our own linting tests.

- Chef lints are in lower case and use an underscore, `_` to separate words.
- Microsoft lints are capitalized and use CamelCase.
- Changed Microsoft lints are in lower case

Exceptions to the Microsoft style:

|Style|Chef|Microsoft|
|-----|----|---------|
||eadings|title-case|sentence-case|
|HeadingAcronyms|yes|no|
|Contractions|no|yes|
|RangeFormat|no|yes|
|Quotes|no|yes|
|GeneralURL|no|yes|

Extended lints:

avoid.yml
foreign.yml
heading_punctuation.yml
metric.yml

Chef lints:

brands.yml
chef_automate.yml
chef_desktop.yml
chef_habitat.yml
chef_infra_client.yml
chef_infra_server.yml
habitat_artifact.yml
habitat_builder.yml
habitat_depot.yml
habitat_studio.yml
habitat_supervisor.yml
inclusive.yml
policyfile.yml

TODO: We should handle the Microsoft lints correctly, as documented on [docs.errata.ai](https://docs.errata.ai/vale/config)

## Releasing

The Vale GitHub Action requires a released `.zip` archive file. The `.github\workflows\main.yaml` workflow is a minimal approach to creating this release.

The release action uses:

- [Zip Release](https://github.com/marketplace/actions/zip-release)
- [Create Release](https://github.com/marketplace/actions/create-release)
- [GitHub Tag Bump](https://github.com/marketplace/actions/github-tag-bump)

**Manual Bumping**: Any commit message that includes #major, #minor, #patch, or #none will trigger the respective version bump. If two or more are present, the highest-ranking one will take precedence. If #none is contained in the commit message, it will skip bumping regardless DEFAULT_BUMP.

**Automatic Bumping**: If no #major, #minor or #patch tag is contained in the commit messages, it will bump whichever DEFAULT_BUMP is set to (which is minor by default). Disable this by setting DEFAULT_BUMP to none.

  This action uses:

  ```yml
  DEFAULT_BUMP: minor
  ```

Information about releasing:

1. [How to Release Code With GitHub](https://youtu.be/Ob9llA_QhQY) video.
1. GitHub [About releases](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases) documentation.

GitHub Actions:

1. CoderDave's detailed video tutorial on [GitHub Actions](https://youtu.be/TLB5MY9BBa4)
