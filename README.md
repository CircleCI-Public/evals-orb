# evals orb

[![CircleCI Build Status](https://circleci.com/gh/CircleCI-Public/evals-orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/CircleCI-Public/evals-orb) [![CircleCI Orb Version](https://badges.circleci.com/orbs/circleci/evals.svg)](https://circleci.com/orbs/registry/orb/circleci/evals) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/circleci-public/evals-orb/main/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)

This repository has the code for the CircleCI [Evals Orb](https://github.com/CircleCI-Public/evals-orb).

## Usage

### Setup

In order to post comments to PRs on GitHub, you will need to set the `GITHUB_TOKEN` environment variable with an access token that has repo scope access.

#### Orb Parameters

The [evals orb](https://github.com/circleci-public/evals-orb) accepts the following parameters:

_Some of the parameters are optional based on the eval platform being used._

##### Common parameters

- `circle_pipeline_id` - CircleCI Pipeline ID

- `cmd` - Command to run the evaluation

- `eval_platform` - Evaluation platform (e.g. `braintrust`, `langsmith` etc. - default: `braintrust`)

- `evals_result_location` - Location to save evaluation results (default: `./results`)

##### Braintrust-specific parameters

- `braintrust_experiment_name` (optional) - Braintrust experiment name. We will generate a unique name based on an MD5 hash of "`<CIRCLE_PIPELINE_ID>_<CIRCLE_WORKFLOW_ID>`" if no `braintrust_experiment_name` is provided.

##### LangSmith-specific parameters

- `langsmith_endpoint` - (optional) LangSmith API endpoint (default: `https://api.smith.langchain.com`)

- `langsmith_experiment_name` (optional) - LangSmith experiment name. We will generate a unique name based on an MD5 hash of "`<CIRCLE_PIPELINE_ID>_<CIRCLE_WORKFLOW_ID>`" if no `langsmith_experiment_name` is provided.

### Use In Config

For full usage guidelines, see the [Orb Registry listing](http://circleci.com/orbs/registry/orb/circleci/evals).

## Usage Examples

For [Evals Orb](https://github.com/CircleCI-Public/evals-orb) usage examples, check out the [llm-eval-examples](https://github.com/CircleCI-Public/llm-eval-examples) repo.

## FAQ

View the [FAQ in the wiki](https://github.com/CircleCI-Public/evals-orb/wiki/FAQ)

## Contributing

We welcome [issues](https://github.com/CircleCI-Public/evals-orb/issues) to and [pull requests](https://github.com/CircleCI-Public/evals-orb/pulls) against this repository!

For further questions/comments about this or other orbs, visit the [CircleCI Orbs discussion forum](https://discuss.circleci.com/c/orbs).
