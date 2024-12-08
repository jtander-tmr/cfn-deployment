## IaC
The AWS platform must be bootstrapped with the resources in the [AWS IAM Resources](./aws_iam_resources/gh_iam_resources.yml) CloudFormation template (DISCLAIMER: there may be redundant/unnecessary IAM policies lingering in this bootstrap stack). The template, which produces the stack named `<project>-<environment>-github-resources`, must be deployed first in order to execute the workflows in this repo.

The AWS resources can be found in the [`stack`](./stack/) folder. The IaC is organised in [CloudFormation nested stacks](./stack/qluad_stack_architecture.md) and are deployed manually by running the `Deploy CloudFormation Stack` GitHub Actions workflow (located in the `.github` folder).