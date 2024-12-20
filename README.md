# github-workflows

Shared GitHub workflows, to be referenced by other Padok projects.

The following [reusable workflows](https://docs.github.com/en/actions/using-workflows/reusing-workflows) are available in [`.github/workflows`](.github/workflows/):

<!-- prettier-ignore -->
| Name | Description | Must have |
| ---- | ----------- | --------- |
| [`release`](.github/workflows/release.yml) | Configure [Release Please](https://www.notion.so/How-to-configure-Release-Please-9f2c511fe22d4fd29c66cebe41b57a1f) to automate GitHub release creation | ⭐ |
| [`semantic-check`](.github/workflows/semantic-check.yml) | Check that pull requests follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) |
| [`terraform-docs`](.github/workflows/terraform-docs.yml) | Update Terraform module documentation using `terraform-docs` |
| [`terraform-quality`](.github/workflows/terraform-quality.yml) | Run several linter and static analysis tools on Terraform code | ⭐ |
| [`terragrunt-quality`](.github/workflows/terragrunt-quality.yml) | Run several linter and static analysis tools on Terragrunt code | ⭐ |

## Usage

To use these workflows in your project, copy files from the folders listed below, and paste them in the `.github/workflows/` folder in your own repo.

- [`global`](global/): for all your projects
- [`terraform`](terraform/): useful for Terraform modules
- [`terragrunt`](terragrunt/) : Use for Terragrunt project and terraform modules

Your repo should have the following structure:

```
.
├── .github
│   ├── CODEOWNERS
│   └── workflows
│       ├── release.yml
│       ├── semantic-check.yml
│       ├── terraform-docs.yml
│       └── terraform-quality.yml
├── .gitignore
├── LICENSE
├── main.tf
├── README.md
├── renovate.json
└── ... (other files)
```

## Workflow Designs

### `terragrunt-quality` workflow

- [`tenv`](https://github.com/tofuutils/tenv)make sure that the correct version of Terraform and terragrunt is used
- [`terraform fmt`](https://www.terraform.io/docs/cli/commands/fmt.html) to check the basic formatting of Terraform code
- [`terragrunt hclfmt`](https://terragrunt.gruntwork.io/docs/reference/cli-options/#hclfmt) to check the formatting of terragrunt hcl files
- [`guacamole`](https://github.com/padok-team/guacamole) check the code quality
- [`checkov`](https://www.checkov.io/) to check for security issues

### `terraform-quality` workflow

There are several tools to ensure that Terraform code is secure and follows best practices. We selected the following ones:

- [`tfswitch`](https://github.com/warrensbox/terraform-switcher) make sure that the correct version of Terraform is used
- [`terraform fmt`](https://www.terraform.io/docs/cli/commands/fmt.html) to check the basic formatting of Terraform code
- [`terraform validate`](https://www.terraform.io/docs/cli/commands/validate.html) to check the validity of Terraform code
- [`tflint`](https://github.com/terraform-linters/tflint) to check for code quality issues
- [`checkov`](https://www.checkov.io/) to check for security issues

The following tools were considered but ultimately not included:

- [`tfsec`](https://github.com/aquasecurity/tfsec) is redundant with `checkov`, and from Padok's experience, the latter is more reliable
- [`terrascan`](https://github.com/tenable/terrascan) has not been tested by Padok yet
- [`terraform docs`](https://www.terraform.io/docs/commands/docs/index.html) is delegated to another workflow, since it could add a commit to the pull request

> Feel free to suggest other tools to add to this workflow!

## License

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
