# Security Policy

## Our Commitment

**MCP-B** takes security seriously. As a protocol that bridges AI agents with web applications, we're committed to ensuring the safety and security of our users, their data, and their applications.

## Security Architecture

MCP-B is designed with security as a core principle:

- **Origin-based Security** - Tools are scoped to their origin, preventing cross-origin tool access
- **Browser Security Model** - Leverages the browser's built-in authentication and security features
- **No Backend Required** - Reduces attack surface by operating entirely in the browser
- **Explicit User Consent** - Tool invocation requires user awareness and authorization
- **Input Validation** - JSON Schema validation for all tool inputs

Learn more in our [Security Documentation](https://docs.mcp-b.ai/concepts/security).

## Supported Versions

We release security updates for the following versions:

| Package | Supported Versions |
| ------- | ------------------ |
| @mcp-b/global | Latest major version |
| @mcp-b/react-webmcp | Latest major version |
| @mcp-b/transports | Latest major version |
| @mcp-b/webmcp-ts-sdk | Latest major version |
| Browser Extension | Latest version |

We strongly recommend always using the latest stable version.

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

If you discover a security vulnerability, please report it by:

1. **Email** - Contact the maintainers at: `security@mcp-b.ai` (or the appropriate security contact email)
2. **Discord** - Send a direct message to a core maintainer
3. **GitHub Security Advisory** - Use the "Security" tab in the relevant repository

### What to Include

Please include the following information:

- **Description** - Detailed description of the vulnerability
- **Impact** - What an attacker could potentially do
- **Reproduction Steps** - Step-by-step instructions to reproduce
- **Affected Versions** - Which versions are vulnerable
- **Proof of Concept** - Code or screenshots demonstrating the issue (if applicable)
- **Suggested Fix** - If you have ideas for how to fix it (optional)

### What to Expect

- **Acknowledgment** - We'll acknowledge receipt within 48 hours
- **Assessment** - We'll assess the vulnerability and determine severity
- **Communication** - We'll keep you updated on our progress
- **Resolution** - We'll work on a fix and coordinate disclosure timing
- **Credit** - We'll credit you in the security advisory (unless you prefer to remain anonymous)

## Security Best Practices

When building with MCP-B, follow these best practices:

### For Tool Developers

1. **Validate All Inputs** - Use JSON Schema validation for tool inputs
2. **Sanitize Outputs** - Never return sensitive data without authorization
3. **Implement CSRF Protection** - For state-changing operations
4. **Use HTTPS** - Always serve WebMCP tools over HTTPS
5. **Rate Limiting** - Implement rate limits on sensitive operations
6. **Audit Logs** - Log tool invocations for security monitoring
7. **Principle of Least Privilege** - Only expose necessary functionality

```javascript
// Example: Secure tool implementation
navigator.modelContext.registerTool({
  name: "update_user_email",
  description: "Update the user's email address",
  inputSchema: {
    type: "object",
    properties: {
      email: {
        type: "string",
        format: "email",
        maxLength: 255
      }
    },
    required: ["email"]
  },
  handler: async ({ email }) => {
    // Verify user is authenticated
    if (!isAuthenticated()) {
      throw new Error("Unauthorized");
    }

    // Sanitize input
    const sanitizedEmail = sanitizeEmail(email);

    // Validate CSRF token
    await validateCSRFToken();

    // Perform update with audit logging
    await updateEmailWithAudit(sanitizedEmail);

    return { success: true };
  }
});
```

### For Integration Developers

1. **Origin Validation** - Verify tool origins before invocation
2. **User Consent** - Always show users what tools will be called
3. **Timeout Limits** - Set reasonable timeouts for tool calls
4. **Error Handling** - Handle errors gracefully without exposing internals
5. **Secure Storage** - Store credentials securely (use browser APIs)

See our [Security Best Practices Guide](https://docs.mcp-b.ai/security) for more details.

## Known Security Considerations

### Cross-Site Scripting (XSS)
If a website has XSS vulnerabilities, attackers could potentially register malicious tools or intercept tool calls. Always implement proper XSS protection on your website.

### Tool Impersonation
Without proper origin validation, a malicious website could attempt to impersonate tools from another origin. The browser extension and transport layers include origin validation to prevent this.

### Data Exfiltration
Tools that return user data should implement proper authorization checks. Never expose sensitive data without verifying the user has permission to access it.

## Security Updates

Security updates are released as soon as possible after a vulnerability is confirmed. We follow these practices:

1. **Patch Development** - Develop and test a fix privately
2. **Coordinated Disclosure** - Notify affected users before public disclosure
3. **Release** - Publish patched versions to NPM and extension stores
4. **Advisory** - Publish a security advisory with details and mitigation steps
5. **Notification** - Announce via Discord, GitHub, and other channels

## Bug Bounty Program

We don't currently have a formal bug bounty program, but we recognize and appreciate security researchers who responsibly disclose vulnerabilities. We'll:

- Publicly credit researchers (with permission)
- Provide recognition in our documentation
- Consider contributions for future bounty programs

## Contact

For security concerns:
- Email: `security@mcp-b.ai` (recommended for sensitive issues)
- Discord: Direct message to core maintainers
- GitHub: Use Security Advisories in the relevant repository

For general security questions:
- [Documentation](https://docs.mcp-b.ai/security)
- [Discord](https://discord.gg/ZnHG4csJRB)
- [GitHub Discussions](https://github.com/orgs/MCP-B/discussions)

---

Thank you for helping keep **MCP-B** and our community safe!
