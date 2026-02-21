# Agents-Collection

A centralized collection of [GitHub Copilot agent definitions](https://docs.github.com/en/copilot/using-github-copilot/using-github-copilot-coding-agent) shared across personal repositories via Git submodule. Agent definitions stored here are compatible with **GitHub CLI** and **Visual Studio Code**.

## How to use

### Add this repository as a submodule

Run the following commands inside the repository where you want to use these agent definitions:

```bash
# Add the submodule – agents will live at .github/agents
git submodule add https://github.com/Skuty/Agents-Collection.git .github/agents

# Commit the submodule reference
git add .gitmodules .github/agents
git commit -m "Add Agents-Collection as submodule"
git push
```

### Clone a repository that already uses this submodule

```bash
# Clone with submodules initialized in one step
git clone --recurse-submodules <your-repo-url>

# Or initialize the submodule after a regular clone
git submodule update --init --recursive
```

### Update agent definitions to the latest version

```bash
# Pull the latest changes from this repository
git submodule update --remote --merge .github/agents

# Commit the updated reference
git add .github/agents
git commit -m "Update Agents-Collection submodule"
git push
```

## Agents

| File | Description |
|------|-------------|
| [copilot-agent-builder.md](.github/agents/copilot-agent-builder.md) | Builds high-quality GitHub Copilot agents for CLI, VS Code, Visual Studio and GitHub.com |

