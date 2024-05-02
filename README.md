# evals orb

[![CircleCI Build Status](https://circleci.com/gh/CircleCI-Public/evals-orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/CircleCI-Public/evals-orb) [![CircleCI Orb Version](https://badges.circleci.com/orbs/circleci/evals.svg)](https://circleci.com/orbs/registry/orb/circleci/evals) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/circleci-public/evals-orb/main/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)

This repository has the code for the [CircleCI Evals Orb](https://circleci.com/developer/orbs/orb/circleci/evals).

For [evals orb](https://circleci.com/developer/orbs/orb/circleci/evals) usage examples, check out the [llm-eval-examples](https://github.com/CircleCI-Public/llm-eval-examples) repo.

## Usage

### Setup

In order to post comments to GitHub pull requests, you will need to set a [`GITHUB_TOKEN`](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) environment variable with a [GitHub Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) that has repo scope access.

You can add this [`GITHUB_TOKEN`](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) environment variable in CircleCI project settings. Alternatively, you could include this secret in the context you created as part of an LLMOps integration, if applicable.

### Orb Parameters

The [evals orb](https://github.com/circleci-public/evals-orb) accepts the following parameters:

_Some of the parameters are optional based on the eval platform being used._

#### Common parameters

- **`circle_pipeline_id`**: CircleCI Pipeline ID

- **`cmd`**: Command to run the evaluation

- **`eval_platform`**: Evaluation platform (e.g. `braintrust`, `langsmith` etc.; default: `braintrust`)

- **`evals_result_location`**: Location to save evaluation results (default: `./results`)

#### Braintrust-specific parameters

- **`braintrust_experiment_name`** _(optional)_: Braintrust experiment name
  - If no value is provided, an experiment name will be auto-generated based on an MD5 hash of `<CIRCLE_PIPELINE_ID>_<CIRCLE_WORKFLOW_ID>`.

#### LangSmith-specific parameters

- **`langsmith_endpoint`** _(optional)_: LangSmith API endpoint (default: `https://api.smith.langchain.com`)

- **`langsmith_experiment_name`** _(optional)_: LangSmith experiment name
  - If no value is provided, an experiment name will be auto-generated based on an MD5 hash of `<CIRCLE_PIPELINE_ID>_<CIRCLE_WORKFLOW_ID>`.

### Use in Config

For full usage guidelines, see the [Orb Registry listing](http://circleci.com/orbs/registry/orb/circleci/evals).

## Usage Examples

For [evals orb](https://circleci.com/developer/orbs/orb/circleci/evals) usage examples, check out the [llm-eval-examples](https://github.com/CircleCI-Public/llm-eval-examples) repo.

## FAQ

View the [FAQ in the wiki](https://github.com/CircleCI-Public/evals-orb/wiki/FAQ)

## Contributing

We welcome [issues](https://github.com/CircleCI-Public/evals-orb/issues) to and [pull requests](https://github.com/CircleCI-Public/evals-orb/pulls) against this repository!

For further questions/comments about this or other orbs, visit the [CircleCI Orbs discussion forum](https://discuss.circleci.com/c/orbs).
