# CI/CD Tools and Practices Final Project Tekton Workflows

This directory will contain all the Tekton workflows you create in the CI/CD Tools and Practices Final Project.

## Running the tests

The `nose` task in `tasks.yml` runs `nosetests` against the source workspace. Pass extra nose arguments with the `args` param (default `-v`), for example `--params args="-v --with-coverage"`.
