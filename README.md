# A collection of Cloudformation templates used for JWCC accounts

## Setup

1. Install [Mise](https://mise.jdx.dev/getting-started.html).
2. In this repo, run `mise install`. This will install python, the AWSCLI, and cfn-lint for this repo.

## Deploying

You will need to have your AWS config setup similar to [here](https://github.com/Onebrief/infrastructure/blob/master/terraform/org/aws.config). After that, you can do a simple `mise deploy-all` or the other more specific deploy tasks to deploy the Cloudformation templates. We do not currently have CICD for this repo so coordinate carefully when testing.
