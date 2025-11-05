<div align="center">

  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/MCP-B/.github/main/profile/logo-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/MCP-B/.github/main/profile/logo-light.svg">
    <img src="https://raw.githubusercontent.com/MCP-B/.github/main/profile/logo.svg" alt="MCP-B Logo" width="200" height="200">
  </picture>

  # MCP-B

  ### W3C Standard for Making Websites AI-Accessible

  <br>

  [![Documentation](https://img.shields.io/badge/docs-docs.mcp--b.ai-5B8DEE?style=for-the-badge)](https://docs.mcp-b.ai)
  [![Discord](https://img.shields.io/badge/Discord-Join_Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/ZnHG4csJRB)
  [![NPM](https://img.shields.io/npm/v/@mcp-b/transports?label=npm&style=for-the-badge&color=CB3837)](https://www.npmjs.com/package/@mcp-b/transports)
  [![License](https://img.shields.io/badge/license-MIT-00C853?style=for-the-badge)](LICENSE)

  <br>

  **[Website](https://mcp-b.ai)** • **[Documentation](https://docs.mcp-b.ai)** • **[Discord](https://discord.gg/ZnHG4csJRB)** • **[Examples](https://github.com/MCP-B/examples)**

  <br>
</div>

---

## Overview

**MCP-B** (Model Context Protocol for Browsers) extends the [Model Context Protocol](https://modelcontextprotocol.io) to the browser, enabling websites to expose AI-callable tools through `navigator.modelContext`. Build intelligent, interactive web applications that AI agents can discover and control seamlessly.

## Key Features

- **Browser-Native MCP** — Implements W3C Web Model Context API for standardized AI tool registration
- **Secure by Default** — Leverages browser authentication and origin-based security model
- **Zero Backend Required** — Expose tools directly from your frontend application
- **Agent-Ready** — Works with Claude, ChatGPT, and any MCP-compatible AI client
- **Framework Agnostic** — React hooks, vanilla JS, and framework-specific integrations available

## Quick Start

```bash
# Install the core package
npm install @mcp-b/global

# Or use React hooks
npm install @mcp-b/react-webmcp
```

```javascript
// Register a tool that AI agents can discover and call
navigator.modelContext.registerTool({
  name: "get_user_profile",
  description: "Get the current user's profile information",
  inputSchema: {
    type: "object",
    properties: {},
  },
  handler: async () => {
    return { name: "John Doe", email: "john@example.com" };
  }
});
```

[View Full Documentation →](https://docs.mcp-b.ai/quickstart)

## Core Packages

| Package | Description | Links |
|---------|-------------|-------|
| [`@mcp-b/global`](https://docs.mcp-b.ai/packages/global) | W3C Web Model Context API polyfill | [npm](https://www.npmjs.com/package/@mcp-b/global) |
| [`@mcp-b/react-webmcp`](https://docs.mcp-b.ai/packages/react-webmcp) | React hooks for WebMCP | [npm](https://www.npmjs.com/package/@mcp-b/react-webmcp) |
| [`@mcp-b/transports`](https://docs.mcp-b.ai/packages/transports) | Browser transport implementations | [npm](https://www.npmjs.com/package/@mcp-b/transports) |
| [`@mcp-b/webmcp-ts-sdk`](https://docs.mcp-b.ai/packages/webmcp-ts-sdk) | TypeScript SDK for MCP-B | [npm](https://www.npmjs.com/package/@mcp-b/webmcp-ts-sdk) |
| [`@mcp-b/extension-tools`](https://docs.mcp-b.ai/packages/extension-tools) | Chrome Extension API wrappers | [npm](https://www.npmjs.com/package/@mcp-b/extension-tools) |

## Resources

- **[Documentation](https://docs.mcp-b.ai)** — Comprehensive guides, API references, and examples
- **[Live Demo](https://mcp-b.ai)** — Interactive tool examples and playground
- **[Browser Extension](https://docs.mcp-b.ai/extension/index)** — Chrome extension for tool discovery
- **[Best Practices](https://docs.mcp-b.ai/best-practices)** — Tool design patterns and security guidelines
- **[AI Framework Integration](https://docs.mcp-b.ai/ai-frameworks/index)** — Connect with Assistant-UI, AG-UI, and more

## Community

- **[Discord](https://discord.gg/ZnHG4csJRB)** — Get help, share ideas, and collaborate
- **[GitHub Discussions](https://github.com/orgs/MCP-B/discussions)** — Ask questions and discuss features
- **[Contributing](CONTRIBUTING.md)** — Learn how to contribute to MCP-B
- **[Code of Conduct](CODE_OF_CONDUCT.md)** — Our community standards

## Use Cases

- **Interactive Dashboards** — Let AI agents query metrics and visualize data
- **E-commerce Sites** — Enable natural language product search and checkout
- **Documentation Sites** — AI-powered search and content generation
- **SaaS Applications** — Expose app functionality as composable AI tools
- **Admin Panels** — Voice and chat-based admin controls

## License

MCP-B is open source software licensed under the [MIT License](LICENSE).

---

<div align="center">

  ### Built with care by the MCP-B community

  <br>

  **[Website](https://mcp-b.ai)** • **[Docs](https://docs.mcp-b.ai)** • **[Discord](https://discord.gg/ZnHG4csJRB)** • **[NPM](https://www.npmjs.com/package/@mcp-b/transports)**

  <br>

  <sub>Making the web AI-accessible, one tool at a time.</sub>

</div>
