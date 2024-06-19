# Example use of the `terraform-mod-vpc` Terraform Module

An example of how to use the `terraform-mod-vpc` module in a Terraform script.

# Pre-requisites

Because this example contains specific AWS resources, the following must be configured with pre-existing items in order to work.

- An AWS `profile` named `default`
- Environment variable `TF_VAR_examples_owner` (or get prompted for `examples_owner` value)
- `key_name`

# Quick start guide

- Make sure this `example` directory is your current working directory
- Run `terraform init`
- Run `terraform plan -out=plan`
- Run `terraform apply plan ; rm plan`
- Edit `locals` values `main.tf` for testing
- Run `terraform plan -out=plan`
- Run `terraform apply plan ; rm plan`
- When finished, run `terraform destroy` and remove any remaining temporary files

# Use

This directory is not only an example of how to call the module, but is also used for
testing the module as changes are made.
When testing, the main items to reconfigure are `locals` and parameters of the `module`
inside the `main.tf` file.

## Recommendation

## Source

The source for the module here is specifically set to a path so testing can be performed
before checking any changes into the `git` repository.
For some reason using a source of just `..` doesn't work and
you must instead use `../../terraform-mod-c4-ubuntu-instance`.
