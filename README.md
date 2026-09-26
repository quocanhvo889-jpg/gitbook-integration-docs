# GitBook Integration Guide

This repository is set up as a GitBook-ready documentation starter for connecting a GitHub repository to GitBook.

## Recommended repository structure

```text
.
├── README.md
├── GITBOOK_CLI_SETUP.md
├── CLI_SETUP_INSTRUCTIONS.md
├── gitbook-manifest.yaml
├── docs/
│   ├── overview.md
│   ├── getting-started.md
│   ├── architecture.md
│   ├── api.md
│   ├── deployment.md
│   ├── security.md
│   ├── troubleshooting.md
│   └── gitbook-mcp.md
├── .gitignore
└── .github/
    └── workflows/
```

## GitBook connection steps

1. Log in to GitBook.
2. Open the target space.
3. Go to Integrations or GitHub.
4. Connect your GitHub account.
5. Select the repository to sync.
6. Choose the branch, usually `main`.
7. Choose the docs folder, usually `docs/`.
8. Save the integration.
9. Ensure files are Markdown (`.md`) files.

## GitBook MCP endpoint

GitBook also supports MCP-style access through the remote MCP endpoint:

```text
https://mcp.gitbook.com/mcp
```

Use this endpoint in compatible MCP clients or AI tooling when you want to connect GitBook to an MCP-enabled environment.

## GitBook sync prompt

Use this prompt in GitBook or when requesting support:

> Connect my GitHub repository to GitBook. I want GitBook to sync documentation from the `docs/` folder in my repository. The repository is under my GitHub account and should use the `main` branch. Please authorize access to the repository, select the correct branch, and sync markdown files from the `docs/` directory for publishing in my GitBook space. If the repo is not visible, verify my GitHub account has access and that the repository contains markdown files in a supported docs folder.

## Notes

- GitBook reads markdown files, not raw app code.
- The repo must be visible to the GitHub account connected to GitBook.
- If the repo is private, GitBook must be authorized to access it.
- If the repo is empty or has no docs folder, GitBook will not show content.
- The MCP endpoint can be used with compatible MCP clients to access GitBook resources programmatically.
