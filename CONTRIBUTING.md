# Contributing to MCP-B

Thank you for your interest in contributing to **MCP-B**! We're building the standard for AI-accessible web applications, and we welcome contributions from the community.

## Getting Started

1. **Join our community**
   - [Discord](https://discord.gg/ZnHG4csJRB) - Chat with maintainers and other contributors
   - [GitHub Issues](https://github.com/WebMCP-org/npm-packages/issues) - Report bugs and request features

2. **Find something to work on**
   - Browse [open issues](https://github.com/WebMCP-org/npm-packages/issues)
   - Look for issues labeled `good first issue` or `help wanted`
   - Check our [project boards](https://github.com/orgs/WebMCP-org/projects) for planned work

3. **Read the documentation**
   - [Architecture Overview](https://docs.mcp-b.ai/concepts/architecture)
   - [Tool Design Patterns](https://docs.mcp-b.ai/concepts/tool-design)
   - [Best Practices](https://docs.mcp-b.ai/best-practices)

## How to Contribute

### Reporting Bugs

Before creating a bug report:
- Check if the bug has already been reported
- Verify the bug exists in the latest version
- Gather relevant information (browser version, console errors, reproduction steps)

Create a bug report with:
- Clear, descriptive title
- Step-by-step reproduction instructions
- Expected vs actual behavior
- Screenshots or error messages
- Environment details

### Suggesting Features

We love new ideas! When suggesting a feature:
- Search existing discussions and issues first
- Explain the problem your feature would solve
- Describe your proposed solution
- Consider backwards compatibility and security implications
- Share use cases and examples

### Contributing Code

1. **Fork and clone** the relevant repository
2. **Create a branch** with a descriptive name:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/bug-description
   ```

3. **Make your changes**
   - Follow the existing code style
   - Write clear, concise commit messages
   - Add tests for new functionality
   - Update documentation as needed

4. **Test your changes**
   ```bash
   npm install
   npm test
   npm run build
   ```

5. **Submit a pull request**
   - Reference any related issues
   - Describe what changes you made and why
   - Include screenshots for UI changes
   - Ensure all checks pass

### Code Style Guidelines

- **TypeScript**: Use strict mode, proper types, avoid `any`
- **Formatting**: We use Prettier (run `npm run format`)
- **Linting**: Fix all ESLint warnings (run `npm run lint`)
- **Comments**: Document complex logic, but prefer self-documenting code
- **Tests**: Write unit tests for new features and bug fixes

### Pull Request Process

1. Update documentation for any API changes
2. Add changelog entry if applicable
3. Ensure all tests pass and linting succeeds
4. Maintainers will review your PR and may request changes
5. Once approved, your PR will be merged!

## Development Setup

```bash
# Clone your fork
git clone https://github.com/your-username/repo-name.git
cd repo-name

# Install dependencies
npm install

# Run development server
npm run dev

# Run tests
npm test

# Build for production
npm run build
```

## Repository Structure

- **`/packages`** - Core NPM packages
  - `@mcp-b/global` - W3C API polyfill
  - `@mcp-b/react-webmcp` - React hooks
  - `@mcp-b/transports` - Transport implementations
  - And more...

- **`/extension`** - Browser extension source code
- **`/docs`** - Documentation source files
- **`/examples`** - Example implementations

## Documentation

Documentation improvements are always welcome! To contribute:

1. Edit documentation files (usually Markdown)
2. Test locally if possible
3. Submit a PR with your changes
4. Explain what you improved and why

See [docs.mcp-b.ai](https://docs.mcp-b.ai) for the current documentation.

## Security

Found a security vulnerability? Please **do not** open a public issue. Instead:
- Email security concerns to the maintainers
- See our [Security Policy](SECURITY.md) for details
- We'll work with you to address the issue promptly

## Code of Conduct

This project adheres to a [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you agree to uphold this code. Please report unacceptable behavior to the maintainers.

## Recognition

Contributors who make significant contributions will be:
- Listed in project documentation
- Credited in release notes
- Invited to join the maintainers team (for sustained contributions)

## Questions?

- Ask in [Discord](https://discord.gg/ZnHG4csJRB)
- Open a [GitHub Issue](https://github.com/WebMCP-org/npm-packages/issues)
- Check the [documentation](https://docs.mcp-b.ai)

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for contributing to **MCP-B**! Together, we're building the future of AI-accessible web applications.
