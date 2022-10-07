# github-workflows

Shared GitHub workflows, to be referenced by other Padok projects.

The following [reusable workflows](https://docs.github.com/en/actions/using-workflows/reusing-workflows#creating-a-reusable-workflow) are available in [`.github/workflows`](./.github/workflows/):

| Name | Description | Must have |
| ---- | ----------- | --------- |
| [`release`](.github/workflows/release.yml) | Configure [Release Please](https://www.notion.so/How-to-configure-Release-Please-9f2c511fe22d4fd29c66cebe41b57a1f) to automate GitHub release creation | ⭐ |
| [`semantic-check`](.github/workflows/semantic-check.yml) | Check that pull requests follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) |
| [`terraform-docs`](.github/workflows/terraform-docs.yml) | Update Terraform module documentation using `terraform-docs` |
| [`terraform-quality`](.github/workflows/terraform-quality.yml) | Run several linter and static analysis tools on Terraform code | ⭐ |

## Workflows Design

### `terraform-quality` workflow

There are several tools to ensure that Terraform code is secure and follows best practices. We selected the following ones:

- [`tfswitch`](https://github.com/warrensbox/terraform-switcher) make sure that the correct version of Terraform is used
- [`terraform fmt`](https://www.terraform.io/docs/cli/commands/fmt.html) to check the basic formatting of Terraform code
- [`terraform validate`](https://www.terraform.io/docs/cli/commands/validate.html) to check the validity of Terraform code
- [`tflint`](https://github.com/terraform-linters/tflint) to check for code quality issues
- [`checkov`](https://www.checkov.io/) to check for security issues

The following tools were considered but ultimately not included:

- [`tfsec`](https://github.com/aquasecurity/tfsec) is redondant with `checkov`, and from Padok's experience, the later is more reliable
- [`terrascan`](https://github.com/tenable/terrascan) has not been tested yet by Padok
- [`terraform docs`](https://www.terraform.io/docs/commands/docs/index.html) is delegated to another workflow, since it could add a commit to the pull request

> Feel free to suggest other tools to add to this workflow!

## License

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
