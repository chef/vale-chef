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
|headings|title-case|sentence-case|
|Contractions|no|yes|
|RangeFormat|no|yes|
|Quotes|no|yes|

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

We should consolidate the Chef brand lints at some point.
