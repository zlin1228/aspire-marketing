
## Get started

This project uses `yarn` as its package manager.

```shell
yarn
```

## Running Storybook

To run Storybook locally, simply run:

```shell
yarn storybook
```

## Committing

This repository uses commit message linting to enforce
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/). The basic commit structure is:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

If you are not familiar with the Conventional Commit types you can find them
[here](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#type).

## Releasing

This project uses [semantic-release](https://github.com/semantic-release/semantic-release) to manage the tagging and
release. `semantic-release` will automatically create a new release when a commit is merged into the `main` branch.

> The release will be based on the commit messages which is why it's imperative to follow the
> [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) format.

`semantic-release` will NOT work on a templated project without a GitHub
[personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).
You will need to create a new token and add it to the GitHub secrets for the project with the variable name `GH_TOKEN`.

If you do **NOT** want to use `semantic-release` in your project, you can remove all of the code between the semantic
release comments in the [CICD workflow file.](.github/workflows/cicd.yml) and remove all devDependencies starting with
`@semantic-release`.
