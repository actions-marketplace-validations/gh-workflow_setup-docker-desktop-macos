# Task 01: Create public GitHub action from existing workflows

This is a fresh repo, created from an action-template repo.

The goal of this repo is to serve as public GH action for: "Set up Docker on macOS using Docker Desktop".

## Source projects and other resources

### My own projects

The template/source projects to draw from are locally in:

- `../../aicage/aicage`: The `aicage` project with test workflows on macOS runners using Docker Desktop
  - workflows:
    - `.github/workflows/integration-test-macos-hosted.yml`
    - `.github/workflows/integration-test-macos-full.yml`
- `../multiarch-image-publish/`: My other public GH action with e2e setup to really test the action before releases

You may suggest to carry back lessons learned to either project if it arises.

### Other projects and online resources

- [douglascamata/setup-docker-macos-action](https://github.com/douglascamata/setup-docker-macos-action)  
  Similar action using Colima not Docker Desktop. I like the documentation and that it differs on runners.
- [GitHub-hosted runners reference](https://docs.github.com/en/actions/reference/runners/github-hosted-runners)  
  Starting point for information on the macOS runners

## Template project

This repo was created from the brand new template repo in `../action-template/`.  
Also feel free to suggest updates to it.

## Task Detail

The workflows in `aicage/aicage` already set up Docker Desktop and it works. Plus they have some testing or info bits.

This action here shall for users get Docker Desktop up and running. Plus have an optional boolean flag so the action
prints information.

The tests in the source workflows (run-hello-world, build image) can be nicely used here in workflows testing this
action. Overall I expect a maximum e2e test similar to the ones in `../multiarch-image-publish/`.

## Task workflow

- Don’t forget to read `AGENTS.md` and respect those rules.

You shall follow this order:

1. Read documentation and code to understand the task.
2. Ask me questions if something is not clear to you.
3. Present me with an implementation solution; this needs my approval.
4. Implement the change autonomously including a loop of running-tests, fixing bugs, running tests.
5. Run linters, use `scripts/lint.sh` with active venv.
6. Present me the change for review.
7. Interactively react to my review feedback.
8. Do not commit any changes unless explicitly instructed by the user.
