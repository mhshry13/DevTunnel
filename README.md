# DevTunnel
Dev Tunnel test Project

Creating a development tunnel in GitHub Codespaces involves a few steps to set up and expose your development environment. Here's a step-by-step guide:

Open Your Repository: Go to the repository where you want to create the dev tunnel.

Create a Codespace:

Click on the Code button.
Select the Codespaces tab.
Click on New codespace to create a new codespace.
Configure the Dev Container:

If you don't have a .devcontainer directory, create one in your repository.
Inside the .devcontainer directory, create a devcontainer.json file. This file will define the configuration for your development environment.
Add Configuration to devcontainer.json:

Here is an example of a basic devcontainer.json file:
{
  "name": "My Dev Container",
  "image": "mcr.microsoft.com/vscode/devcontainers/base:0-focal",
  "features": {
    "ghcr.io/devcontainers/features/docker-in-docker:1": {}
  },
  "postCreateCommand": "echo 'Setup complete!'"
}
Start the Codespace:

Once the configuration is set, start the codespace. GitHub Codespaces will use the devcontainer.json file to set up the environment.
Expose a Port:

In the Codespaces interface, you can expose a port by clicking on the Ports tab.
Click on Add Port and enter the port number you want to expose.
You can also set the visibility of the port (public, private, or internal).
Access the Dev Tunnel:

Once the port is exposed, you can access your development environment through the provided URL.
For more detailed instructions, you can refer to the GitHub Docs on dev containers.
