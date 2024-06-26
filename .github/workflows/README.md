# GitHub-Actions-Workflow

GitHub Actions Workflow: -Create a new file in the .github/workflows directory (you may need to create these directories). Name the file docker-image.yml.

Define a new workflow in this file. Use the on: push event to trigger the workflow on every push to the repository.
Define a job that does the following:
Checks out your repository.
Builds the Docker image.
Logs in to the GitHub Container Registry.
Pushes the Docker image to the registry.
GitHub Secrets:

For authentication with the GitHub Container Registry, you’ll need to use a token. In your repository, go to Settings > Secrets and create a new secret named CR_PAT that holds a Personal Access Token with the write:packages, read:packages, and delete:packages (if needed) scopes.
Notes:

The GitHub Container Registry requires Docker images to be tagged with a specific format. Ensure you follow the required naming conventions.
Ensure you use the GitHub Secrets appropriately in your workflow to avoid exposing sensitive information.
Hints:

Use GitHub’s marketplace to find pre-existing actions that help with Docker and container registry tasks, such as actions/checkout for checking out code and docker/login-action for logging into a container registry.
Always use secrets (never hard-code) for any tokens or sensitive information in GitHub Actions workflows.
