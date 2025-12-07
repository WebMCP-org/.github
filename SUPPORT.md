# Getting Support

Welcome to the **MCP-B** community! We're here to help you build AI-accessible web applications. This guide will help you find the right resources and get answers to your questions.

## Quick Links

- **[Documentation](https://docs.mcp-b.ai)** - Comprehensive guides and API references
- **[Discord](https://discord.gg/ZnHG4csJRB)** - Real-time chat with the community
- **[GitHub Issues](https://github.com/WebMCP-org/npm-packages/issues)** - Report bugs and request features
- **[Examples](https://github.com/WebMCP-org/examples)** - Sample implementations
- **[Live Demo](https://mcp-b.ai)** - Interactive examples and playground

## Documentation

Start with our comprehensive documentation:

### Getting Started
- **[Introduction](https://docs.mcp-b.ai/introduction)** - What is MCP-B?
- **[Quick Start](https://docs.mcp-b.ai/quickstart)** - Get up and running in minutes
- **[Architecture Overview](https://docs.mcp-b.ai/concepts/architecture)** - Understand how it works
- **[Examples](https://docs.mcp-b.ai/examples)** - See MCP-B in action

### Core Concepts
- **[Tool Registration](https://docs.mcp-b.ai/concepts/tool-registration)** - Register tools with navigator.modelContext
- **[Tool Design Patterns](https://docs.mcp-b.ai/concepts/tool-design)** - Best practices for effective tools
- **[Security Model](https://docs.mcp-b.ai/concepts/security)** - Authentication and authorization
- **[Transport Layers](https://docs.mcp-b.ai/concepts/transports)** - How communication works

### Integration Guides
- **[AI Framework Integration](https://docs.mcp-b.ai/ai-frameworks/index)** - Connect with frontend AI frameworks
- **[Assistant-UI](https://docs.mcp-b.ai/ai-frameworks/assistant-ui)** - React framework integration
- **[AG-UI](https://docs.mcp-b.ai/ai-frameworks/ag-ui)** - Agentic framework integration
- **[Browser Extension](https://docs.mcp-b.ai/extension/index)** - Using the MCP-B extension
- **[Native Host Setup](https://docs.mcp-b.ai/native-host-setup)** - Connect to Claude Desktop/Code

### Package Documentation
- **[@mcp-b/global](https://docs.mcp-b.ai/packages/global)** - W3C API polyfill
- **[@mcp-b/react-webmcp](https://docs.mcp-b.ai/packages/react-webmcp)** - React hooks
- **[@mcp-b/transports](https://docs.mcp-b.ai/packages/transports)** - Transport implementations
- **[All Packages](https://docs.mcp-b.ai/packages/webmcp-ts-sdk)** - Complete package reference

## Community Support

### Discord (Recommended for Quick Help)

Join our [Discord server](https://discord.gg/ZnHG4csJRB) for:
- Real-time help from maintainers and community members
- Debugging assistance
- Announcements and updates
- Casual discussions

**Best for:** Quick questions, troubleshooting, community chat

### GitHub Issues

Use [GitHub Issues](https://github.com/WebMCP-org/npm-packages/issues) for:
- Bug reports and documentation issues
- Feature requests and ideas
- Architecture discussions
- Specific technical problems

**Best for:** Bug reports, feature requests, in-depth discussions

## Before Asking for Help

To get the fastest, most helpful response:

1. **Search First**
   - Check the [documentation](https://docs.mcp-b.ai)
   - Search [Discord history](https://discord.gg/ZnHG4csJRB)
   - Browse [GitHub Issues](https://github.com/WebMCP-org/npm-packages/issues)
   - Look through [existing issues](https://github.com/WebMCP-org/npm-packages/issues)

2. **Provide Context**
   - What are you trying to accomplish?
   - What have you tried so far?
   - What error messages are you seeing?
   - What's your environment (browser, versions, OS)?

3. **Share Code**
   - Provide a minimal reproduction
   - Use code blocks for formatting
   - Include relevant configuration files

4. **Be Specific**
   - "My tool doesn't work" → "My tool returns undefined when called from the extension"
   - "Integration failed" → "Getting CORS error when calling tools from React app"

## Common Issues

### Tool Not Discovered

**Problem:** AI agent can't find your registered tool

**Solutions:**
- Ensure `@mcp-b/global` is loaded before registering tools
- Check browser console for errors
- Verify the tool is registered: `navigator.modelContext.listTools()`
- Confirm the extension/client is connected
- See [Troubleshooting Guide](https://docs.mcp-b.ai/troubleshooting)

### CORS Errors

**Problem:** Cross-origin errors when calling tools

**Solutions:**
- Tools must be same-origin or use transports correctly
- Configure CORS headers for cross-origin requests
- Use the extension for cross-origin tool access
- Review [Security Documentation](https://docs.mcp-b.ai/concepts/security)

### TypeScript Errors

**Problem:** Type errors when using WebMCP packages

**Solutions:**
- Ensure you're using compatible TypeScript version
- Check package versions are in sync
- Review [Package Documentation](https://docs.mcp-b.ai/packages/global)
- Ask in Discord with specific error messages

### Extension Not Connecting

**Problem:** Browser extension not detecting tools

**Solutions:**
- Refresh the page after installing extension
- Check extension is enabled
- Verify tools are registered on page load
- See [Extension Documentation](https://docs.mcp-b.ai/extension/index)

For more solutions, see the [Troubleshooting Guide](https://docs.mcp-b.ai/troubleshooting).

## Professional Support

While MCP-B is open source and community-driven, the maintainers are available for:
- Consulting on MCP-B integration
- Enterprise support and training
- Custom development and implementation

Contact the maintainers through Discord or GitHub for inquiries.

## Contributing

Want to help improve MCP-B?
- Report bugs and issues
- Improve documentation
- Submit pull requests
- Help others in the community

See our [Contributing Guide](CONTRIBUTING.md) to get started.

## Stay Updated

- **[GitHub Releases](https://github.com/orgs/WebMCP-org/repositories)** - Release notes and changelogs
- **[Discord Announcements](https://discord.gg/ZnHG4csJRB)** - Important updates
- **[Changelog](https://docs.mcp-b.ai/changelog)** - Detailed version history
- **[Twitter/X](https://x.com/miguelsPizza)** - News and updates

## Code of Conduct

All community interactions are governed by our [Code of Conduct](CODE_OF_CONDUCT.md). We're committed to providing a welcoming and inclusive environment for everyone.

---

**Still need help?** Don't hesitate to ask! Join our [Discord](https://discord.gg/ZnHG4csJRB) or open a [GitHub Issue](https://github.com/WebMCP-org/npm-packages/issues).

We're here to help you succeed with MCP-B!
