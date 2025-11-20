# OpenCode Server

This project provides a containerized environment for running the [OpenCode](https://www.npmjs.com/package/opencode-ai) server. It includes the necessary dependencies, such as the GitHub CLI, and simplifies the setup process for running the OpenCode agent.

## Features

- **Base Image**: Built on `oven/bun` (slim version).
- **Pre-installed Tools**: Includes `git`, `gh` (GitHub CLI), `jq`, `curl`, `wget`, and more.
- **Auto-Configuration**: Automatically configures GitHub authentication and Git user settings via environment variables.
- **Ready to Run**: Exposes port 4096 and runs the OpenCode server by default.

## Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `GITHUB_TOKEN` | GitHub Personal Access Token for authenticating `gh` CLI. | None |
| `GIT_USER_NAME` | Name to use for Git commits. | "OpenCode Agent" |
| `GIT_USER_EMAIL` | Email to use for Git commits. | "opencode@agent.local" |


API keys for model providers can be set via environment variables:

e.g. `OPENAI_API_KEY=...`, `ANTHROPIC_API_KEY=...`, etc.
## Ports

- **4096**: The default port where the OpenCode server listens.

