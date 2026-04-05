# How Embabel Works: AI-Powered Commit Messages Made Easy

Writing good commit messages is a struggle for many developers. Clear, consistent commits help teams understand code history—but describing changes well takes effort. Embabel solves this by generating commit messages automatically using AI.

## What is Embabel?

Embabel is an AI-powered tool that writes commit messages for you. It analyzes your code changes (the diff) and produces a clear, descriptive message following standard commit conventions. Think of it as a smart assistant that speaks "git."

## How It Works

The process is straightforward:

1. **You make code changes** in your editor
2. **You run Embabel** on your staged files
3. **Embabel analyzes** the diff using an LLM
4. **It generates** a conventional commit message

That's it—no more staring at the screen searching for the right words.

## A Quick Example

Here's a simple code change:

```python
# Before
def greet(name):
    return "Hello " + name

# After
def greet(name):
    return f"Hello {name}"
```

Embabel would generate:

```
Use f-string for string formatting

This improves readability and follows modern Python practices.
```

Clean and descriptive.

## Why Use It?

- **Saves time** - Eliminates writer's block
- **Enforces consistency** - Produces messages that follow conventional commit format
- **Learning tool** - Helps developers understand what good commits look like

## Getting Started

Embabel is available as:

- A command-line tool
- An IDE plugin (VS Code, JetBrains)
- A GitHub integration

Installation via npm:

```bash
npm install -g embabel
```

Run it on your staged changes:

```bash
embabel .
```

## Conclusion

Writing clear commit messages is a skill that takes practice to develop. Embabel accelerates that learning by showing you what well-crafted descriptions look like. Try it on your next PR—you might be surprised at how much smoother your git history becomes.

Happy coding!