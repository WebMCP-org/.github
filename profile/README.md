<div align="center">

  # MCP-B

  ### Model Context Protocol for the Browser

  #### Building a Better Web for Browser Agents

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

### What is WebMCP?

**WebMCP** (Web Model Context Protocol) is a proposed W3C web standard being incubated by the [Web Machine Learning Community Group](https://github.com/webmachinelearning/webmcp). It enables websites to expose AI-callable tools through the browser's `navigator.modelContext` API, allowing AI agents to discover and interact with web applications directly in the browser.

WebMCP is optimized for browser-based, user-present interactions with built-in web security features, leveraging the browser's origin-based security model and user authentication. Learn more in the [W3C WebMCP Explainer](https://github.com/webmachinelearning/webmcp).

### What is MCP-B?

**MCP-B** bridges the gap between WebMCP and the [Model Context Protocol (MCP)](https://modelcontextprotocol.io), serving two critical functions:

1. **API Implementation** — Provides a polyfill that implements the `navigator.modelContext` interface for browsers lacking native support
2. **Protocol Translation** — Converts between WebMCP's web-native format and the MCP protocol, enabling cross-compatibility

MCP-B creates interoperability by enabling WebMCP-formatted tools to function with MCP clients (like Claude Desktop), and MCP-formatted tools to operate within WebMCP-enabled browsers. This allows both standards to evolve independently without breaking existing implementations.

### Open Source & Licensing

All MCP-B libraries and SDKs are **open source** (MIT Licensed), enabling developers to build WebMCP-enabled applications freely. However, the browser extension for connecting to MCP clients is **not open source**.

For developers interested in contributing to browser extension development, check out the [POC MCP-B Extension](https://github.com/MiguelsPizza/WebMCP) (AGPL-3.0) by the community.

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
