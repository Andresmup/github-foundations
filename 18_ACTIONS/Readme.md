# ACTIONS

Github actions is CI/CD pipeline directly integrated with your Github Repository.

Within a Github repo you'll have a tab for Actions.

Github actions allows you to automate:
- Running test suites
- Building images
- Compiling static sites
- Deploy code to servers
- and more...

Github Actions has templates you can use to get started.

Github Actions files are defined as YAML files located in the `.github/workflow` folder of your repo. You can have multiple workflows in a repo triggered by different events.


When you run Github Actions you'll get a history of workflows runs where it will indicate if it was success, failure, in progress and how long it took to run it.

## FINDING GITHUB ACTIONS

In Actions repository starter-workflow are examples of workflows, that you can use to get started. https://github.com/actions/starter-workflows

## EVENT TYPES

Event Triggers causes a Github Action to run.

> [!TIP]
> The **on** attribute specifies the <ins>event trigger</ins> to be used. Example: `on: [push]`

Github Actions has 35+ events triggers, here are the most common:
- **push**: Trigger action on any push to the repository.
- **pull_request**: Run actions when pull request are opened, synchronize, reopened, updated or merged.
- **issues**: Execute actions base on issue activities, like creation or labeling.
- **release**: Automate workflows when a new release is published.
- **schedule**: Schedule actions to run at specific times (events).
- ***manual trigger***: Allow manual triggering of action the Github UI.
