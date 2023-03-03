# Circle/Ci Pipeline

This is a readme file to explain the different steps in the pipeline.

## File content

- Version.
- Orbs.
- Jobs.
- Workflows.

### Version

The version number refers to the times of changes that happened in the `config.yml` file.

### Orbs

CircleCI orbs are shareable packages of configuration elements, including jobs, commands, and executors. Orbs make writing and customizing CircleCI config simple. The reusable configuration elements used in orbs are explained fully in the Reusable Configuration Reference.

### Jobs

A CircleCI job is a collection of steps. All of the steps in the job are executed in a single unit.
In jobs we have:

- the `build` step will have the following:
  - docker image.
  - installing node.
  - installing dependencies for frontend app.
  - installing dependencies for backend api app.
  - handle frontend app linting.
  - build frontend app.
  - build backend api app.
- the `deploy` step will have the following:
  - docker image.
  - installing node.
  - handle eb setup.
  - handle aws-cli setup.
  - handle deploying the app.

### Workflows

A workflow is a set of rules for defining a collection of jobs and their run order.
In the workflow we have:

- build phase.
- hold phase which require manual approval.
- deploy phase.
