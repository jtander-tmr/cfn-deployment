# GitHub Actions
GitHub Actions are used to deploy the QLUAD project onto the TAU AWS platform.
## GH Access to AWS
GitHub [OpenID Connect (OIDC)](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services) is used to access resources on the target AWS platform. The AWS account must be configured by following the OIDC steps in the link above and the link below to allow OIDC to request a short-lived access token each time a workflow is kicked off.
### AWS Configuration
The following AWS resources were created to support the use of GitHub Actions for deploying this stack (see [AWS documentation](https://aws.amazon.com/blogs/security/use-iam-roles-to-connect-github-actions-to-actions-in-aws/) for detailed instructions on how this was accomplished)