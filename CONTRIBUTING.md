# Contributing to 100xBot Community Hub

Thank you for your interest in contributing to 100xBot! This guide will help you file effective issues and participate in the community.

## Table of Contents

- [Before You Start](#before-you-start)
- [How to File a Good Bug Report](#how-to-file-a-good-bug-report)
- [How to Request Features](#how-to-request-features)
- [How to Ask Questions](#how-to-ask-questions)
- [Code Contributions](#code-contributions)
- [Community Guidelines](#community-guidelines)

## Before You Start

### Search First

Before creating a new issue:

1. **Search existing issues** - Your issue might already be reported
2. **Check closed issues** - The issue might have been resolved
3. **Review documentation** - The answer might be in the docs
4. **Browse discussions** - Similar topics might have been discussed

### Choose the Right Template

We provide several issue templates:

- **Bug Report** - Something is broken or not working as expected
- **Feature Request** - Suggest a new feature or enhancement
- **Model Support** - Request support for a new LLM model
- **Integration Request** - Request integration with third-party services
- **Documentation** - Report documentation issues
- **Question/Support** - Ask for help or clarification

## How to File a Good Bug Report

A good bug report should be:

### Clear and Descriptive

- Use a clear, specific title: ❌ "Doesn't work" ✅ "Agent fails when extracting data from dynamic tables"
- Describe what you expected to happen
- Describe what actually happened
- Include the impact of the bug

### Reproducible

Provide step-by-step instructions:

```
1. Open extension on website: https://example.com
2. Click side panel
3. Run agent with prompt: "Extract all product prices"
4. Observe error: "Failed to locate elements"
```

### Complete

Include all relevant information:

- **Browser**: Chrome, Firefox, Brave, Edge
- **Browser Version**: e.g., 120.0.6099.109
- **Extension Version**: Found in `chrome://extensions`
- **Operating System**: Windows, macOS, Linux (with version)
- **LLM Provider**: OpenAI, Anthropic, Google, etc.

### Evidence-Based

Attach supporting materials:

- **Screenshots**: Show the error or unexpected behavior
- **Console Logs**: Open DevTools (F12) and copy relevant errors
- **Extension Logs**: Check the extension's logging output
- **Network Logs**: For API-related issues

### Example of a Good Bug Report

```markdown
Title: Agent fails to click buttons with dynamic IDs on e-commerce sites

Description:
When attempting to click "Add to Cart" buttons on product pages with
dynamically generated IDs, the agent fails with "Element not found" error.

Steps to Reproduce:
1. Navigate to: https://example-shop.com/product/123
2. Open 100xBot side panel
3. Run prompt: "Add this product to cart"
4. Agent attempts to locate button but fails

Expected: Button should be clicked successfully
Actual: Error "Element not found: button.add-to-cart"

Environment:
- Browser: Chrome 120.0.6099.109
- Extension: v1.4.130
- OS: macOS 14.2
- LLM: Claude 3.5 Sonnet via Anthropic API

Logs:
[ERROR] ElementLocator: Failed to locate element with selector: button.add-to-cart
[DEBUG] DOM snapshot: <attached>

Screenshots: [attached]
```

## How to Request Features

Good feature requests should:

### Solve a Real Problem

- Describe the problem you're facing
- Explain why current solutions don't work
- Show how the feature would improve your workflow

### Be Specific

❌ "Make the agent smarter"
✅ "Add ability to handle pagination automatically when extracting table data"

### Include Use Cases

Provide concrete examples:

```markdown
Use Case 1: When scraping multi-page product listings
Currently: I have to manually instruct the agent to click "Next" repeatedly
Proposed: Agent automatically detects pagination and extracts all pages

Use Case 2: When monitoring price changes
Currently: I have to run the agent manually each day
Proposed: Schedule automatic runs and get notifications on changes
```

### Consider Alternatives

- What workarounds have you tried?
- How do other tools solve this problem?
- What are the trade-offs?

## How to Ask Questions

For support questions:

### Be Specific

❌ "How do I use the agent?"
✅ "How do I configure the agent to extract data from password-protected pages?"

### Show What You've Tried

```markdown
I'm trying to: Extract product data from Amazon

What I've tried:
1. Used prompt: "Get all product names" - got timeout error
2. Tried with GPT-4 instead of Claude - same result
3. Checked logs - seeing "Rate limit exceeded"

My configuration:
- LLM: OpenAI GPT-4
- Timeout: 30s
- Headless: No
```

### Provide Context

- What are you trying to accomplish?
- What's your experience level?
- What documentation have you checked?

## Code Contributions

For code contributions, please:

1. **Visit the main repository**: [100x-bot/agent4](https://github.com/100x-bot/agent4)
2. **Read the main repo's contributing guide**
3. **Discuss major changes first** - File an issue before starting work on large features
4. **Follow the coding standards**
5. **Write tests** - Especially for bug fixes
6. **Update documentation** - Keep docs in sync with code changes

### Types of Contributions

- **Bug Fixes**: Submit PRs to the main repository
- **Features**: Discuss in an issue first, then implement
- **Documentation**: Fix typos, add examples, clarify instructions
- **Testing**: Help test new features and report issues
- **Community Support**: Answer questions, help others debug issues

## Community Guidelines

### Be Respectful

- Treat others with kindness and respect
- Welcome newcomers and help them get started
- Assume good intentions
- Avoid inflammatory language

### Be Constructive

- Provide actionable feedback
- Focus on solutions, not blame
- Celebrate good contributions
- Learn from mistakes

### Be Patient

- Maintainers are often volunteers
- Complex issues take time to debug
- Features require careful design
- Good things take time

### Be Collaborative

- Share knowledge and learnings
- Help others troubleshoot issues
- Review and test proposed changes
- Build on each other's ideas

## Label Guide

Issues are labeled to help organize and prioritize:

- `bug` - Something isn't working correctly
- `enhancement` - New feature or improvement
- `documentation` - Documentation improvements
- `question` - Support questions
- `triage` - Needs review by maintainers
- `good-first-issue` - Good for newcomers
- `help-wanted` - Community help requested
- `model-support` - LLM model integration
- `integration` - Third-party integration
- `priority:high` - High priority issue
- `priority:low` - Low priority issue

## Recognition

Contributors are recognized in:

- Issue comments and PR reviews
- Main repository contributors list
- Community showcases
- Release notes (for significant contributions)

## Getting Help

Need help contributing?

- Ask in [GitHub Discussions](https://github.com/100x-bot/100xbot/discussions)
- File a question issue
- Check existing issues for examples
- Read the [Code of Conduct](CODE_OF_CONDUCT.md)

Thank you for contributing to 100xBot! Your participation makes this project better for everyone.
