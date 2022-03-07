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

Note: We should handle the Microsoft lints correctly, as documented on [docs.errata.ai](https://docs.errata.ai/vale/config)

## Releasing

The Vale GitHub Action requires a released `.zip` archive file. The `.github\workflows\main.yaml` workflow is a minimal approach to creating this release.

1. Create a zip file with the Chef lints

    ```bash
    cd Chef
    zip -r chef-style.zip ../releases
    ```

2. Commit the changes and merge
3. Create and tag the release from the [release tab](https://github.com/chef/vale-chef/releases)
