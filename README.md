# QALabPlaywrightMCP

This repository contains the initial configuration for a Playwright MCP project.

The project is designed to test different client applications, with each application kept in a separate folder and workspace. This separation helps avoid MCP chat confusion and keeps test contexts isolated per client.

## Prerequisites

### Node.js Installation
1. Download and install Node.js (version 18 or higher recommended) from the official website: [https://nodejs.org/](https://nodejs.org/).
2. Verify the installation by running the following commands in your terminal:
   ```bash
   node --version
   npm --version
   ```

### VS Code Environment Configuration
1. Install Visual Studio Code from [https://code.visualstudio.com/](https://code.visualstudio.com/).
2. Install the following recommended extensions:
   - **Playwright Test for VS Code**: Provides test runner and debugging support for Playwright tests.
   - **Model Context Protocol (MCP)**: If available, install any MCP-related extensions for enhanced AI assistance (check the VS Code marketplace for "MCP" or "Model Context Protocol").
3. Configure VS Code settings for optimal development:
   - Enable "Format on Save" in settings.
   - Set the default formatter for TypeScript/JavaScript files.

### MCP Installation Commands
To enable MCP (Model Context Protocol) support for Playwright automation:
1. Install the MCP SDK globally (if required for your setup):
   ```bash
   npm install -g @modelcontextprotocol/sdk
   ```
2. For each application workspace, install local MCP dependencies (assuming each `app-*/` folder has its own `package.json`):
   ```bash
   cd app-one
   npm install
   # If MCP server is included, run setup commands as per documentation
   cd ..
   ```
   Repeat for `app-two` and `app-three`.
3. Configure MCP servers in VS Code settings (if applicable):
   - Open VS Code settings (Ctrl+,).
   - Search for "MCP" and configure server endpoints or paths as needed for Playwright integration.

## Project structure

- `app-one/` - workspace for the first client application
- `app-two/` - workspace for the second client application
- `app-three/` - workspace for the third client application

## Initial configuration

- Use Playwright with MCP enabled for interactive test assistance.
- Keep separate Playwright configs per application workspace.
- Store common utilities and shared test helpers in a top-level `common/` folder if needed.
- Ensure each workspace has its own `playwright.config.ts` and `package.json` to maintain isolation.

## Notes

This repository serves as an overview and starting point for multi-application MCP testing. Each application is isolated in its own workspace to reduce chat context overlap and improve test reliability.
