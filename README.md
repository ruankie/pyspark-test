# Description
This is a template for setting up containerised development environments. This environment works really well with the `Remote - Containers` extensoin in VS Code.

# How to use
1. Copy `.devcontainer/` and `requiremets.txt` to the root directory of your repo
2. Edit the `.devcontainer/Dockerfile` to specify your containerised development environment
3. Edit `.devcontainer/devcontainer.json` to specify how VS Code will interact with the container
4. Edit `requiremets.txt` to specify all labraries and specific versions used in your development environment
5. Use the `Remote - Containers` extensoin in VS Code and run the `Open Folder in Container...` command to start developing inside the container
