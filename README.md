# .github

Organization-wide GitHub configuration and community health files for **MCP-B**.

## What is MCP-B?

**MCP-B** is a bridge between web and backend systems that brings the Model Context Protocol to the browser. It serves two critical functions:

1. **API Implementation** — Acts as a polyfill that implements the `navigator.modelContext` interface for browsers lacking native support
2. **Protocol Translation** — Converts between WebMCP's web-native format and the MCP protocol, enabling cross-compatibility

MCP-B creates interoperability by enabling WebMCP-formatted tools to function with MCP clients, and MCP-formatted tools to operate within WebMCP-enabled browsers. This allows both standards to evolve independently without breaking existing implementations.

## What is WebMCP?

**WebMCP** (Web Model Context Protocol) is a W3C web standard currently being incubated by the Web Machine Learning Community Group. It enables websites to expose tools to AI agents through the browser's `navigator.modelContext` API. WebMCP is optimized for browser-based, user-present interactions with built-in web security features, while traditional MCP handles backend services and headless integrations.

The two protocols complement rather than compete — both can operate within the same application simultaneously.

## About This Repository

This repository contains default community health files that apply to all repositories in the **MCP-B** organization. These files provide guidelines, policies, and resources for contributors and users.

## Contents

- **[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)** — Community standards and behavior guidelines
- **[CONTRIBUTING.md](CONTRIBUTING.md)** — How to contribute to MCP-B projects
- **[SECURITY.md](SECURITY.md)** — Security policies and vulnerability reporting
- **[SUPPORT.md](SUPPORT.md)** — Getting help and community resources
- **[profile/README.md](profile/README.md)** — Organization profile displayed on GitHub

## Resources

- **Website:** [mcp-b.ai](https://mcp-b.ai)
- **Documentation:** [docs.mcp-b.ai](https://docs.mcp-b.ai)
- **Chrome Extension:** [MCP-B Extension](https://chromewebstore.google.com/detail/mcp-bextension/daohopfhkdelnpemnhlekblhnikhdhfa)
- **WebMCP Explainer:** [webmachinelearning/webmcp](https://github.com/webmachinelearning/webmcp)
- **Discord:** [discord.gg/ZnHG4csJRB](https://discord.gg/ZnHG4csJRB)
- **NPM:** [@mcp-b packages](https://www.npmjs.com/package/@mcp-b/transports)

## For Maintainers

These files serve as defaults for all **MCP-B** repositories. Individual repositories can override these by adding their own versions.

### Updating Community Files

1. Make changes to files in this repository
2. Test changes locally
3. Submit a pull request
4. Changes will apply to all repos once merged

### Adding New Templates

Consider adding:
- Issue templates (`.github/ISSUE_TEMPLATE/`)
- Pull request template (`.github/PULL_REQUEST_TEMPLATE.md`)
- GitHub Actions workflows (`.github/workflows/`)
- Funding configuration (`.github/FUNDING.yml`)

---

**MCP-B Organization** © 2025 | [MIT License](LICENSE)
