# A collection of Cloudformation templates used for JWCC accounts

## Setup

1. Install [Mise](https://mise.jdx.dev/getting-started.html).
2. In this repo, run `mise install`. This will install python, the AWSCLI, and cfn-lint for this repo.

## Deploying

You will need to have your AWS config setup similar to [here](https://github.com/Onebrief/infrastructure/blob/master/terraform/org/aws.config). After that, you can do a simple `mise deploy-all` or the other more specific deploy tasks to deploy the Cloudformation templates. We do not currently have CICD for this repo so coordinate carefully when testing.

## Importing an AMI

If you want to import an AMI, first upload your AMI export to the artifacts S3 bucket in the `amis` folder. You can then run the command: `mise run import-ami-dev -- --parameter-overrides BucketName=jwcc-vm-artifacts-artifactss3bucket-kycsbnnkbvqd AmiId=ami-0257f58967e2e2d18`. The AMI id will be in the stack outputs.
