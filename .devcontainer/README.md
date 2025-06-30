# VS Code Extension Development Container

This dev container provides a complete development environment for working on VS Code extensions.

## What's included

- **Node.js 18**: Latest LTS version for extension development
- **TypeScript**: For extension development
- **VS Code Extension CLI tools**:
  - `vsce` - Visual Studio Code Extension Manager
  - `yo` - Yeoman generator
  - `generator-code` - VS Code extension generator
- **Git & GitHub CLI**: For version control and GitHub integration
- **Pre-configured VS Code settings**: Optimized for extension development

## Getting started

1. Open this project in VS Code
2. When prompted, click "Reopen in Container" or use Command Palette > "Dev Containers: Reopen in Container"
3. VS Code will build the container and install all dependencies
4. Start developing your extension!

## Testing the extension

1. Press `F5` or go to Run and Debug view
2. Select "Extension" configuration
3. A new VS Code window will open with your extension loaded for testing

## Building and packaging

- To package your extension: `vsce package`
- To publish your extension: `vsce publish`

## Useful commands

- `npm install` - Install dependencies
- `npm run compile` - Compile TypeScript (if applicable)
- `vsce package` - Create .vsix package
- `vsce publish` - Publish to VS Code Marketplace
