# Terraform Module template

This repository is meant to be a template repo we can just spin up new module repos from with our general format.

## Creating a new Terraform Module

1. Clone this repo, renaming appropriately.
1. Write your terraform code in the root dir.
1. Create an example of the module in use in the `examples` dir.
1. Ensure you've completed the [Developer Setup](#developer-setup).
1. In the root dir, run `go mod init MODULE_NAME` to get a new `go.mod` file. Then run `go mod tidy`. This creates a new `go.sum` file and imports the dependencies and checksums specific to your repository.
1. Run your tests to ensure they work as expected using instructions below.

## Actual readme below  - Delete above here

Please put a description of what this module does here

## Terraform Versions

[ ] - todo:  "how to manage versions"

## Usage

### Put an example usage of the module here

```hcl
module "example" {
  source = "terraform/registry/path"

  <variables>
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 1.0 |

## Providers

No provider.

## Inputs

No input.

## Outputs

No output.

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Developer Setup

Install dependencies (macOS)

```shell
brew install pre-commit go terraform terraform-docs
pre-commit install --install-hooks
```

### Testing

[Terratest](https://github.com/gruntwork-io/terratest) is being used for
automated testing with this module. Tests in the `test` folder can be run
locally by running the following command:

```text
make test
```

## Contribution

[Contribution](CONTRIBUTING.md)