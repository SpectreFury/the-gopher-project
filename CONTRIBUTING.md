# Contributing to The Gopher Project 🤝

Thank you for considering contributing to The Gopher Project! This document provides guidelines and information for contributors.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Writing Guidelines](#writing-guidelines)
- [Code Style Guidelines](#code-style-guidelines)
- [Commit Message Guidelines](#commit-message-guidelines)
- [Pull Request Process](#pull-request-process)
- [Issue Reporting](#issue-reporting)

## 📜 Code of Conduct

This project adheres to a Code of Conduct that all contributors are expected to follow:

- **Be respectful**: Treat everyone with respect and kindness
- **Be inclusive**: Welcome newcomers and help them learn
- **Be constructive**: Provide helpful feedback and suggestions
- **Be patient**: Remember that everyone was a beginner once
- **Be collaborative**: Work together to improve the project

## 🤝 How Can I Contribute?

### Content Contributions
- **Write new lessons**: Add tutorials, explanations, or examples
- **Improve existing content**: Fix errors, add clarity, or update outdated information
- **Create exercises**: Develop practical assignments and projects
- **Add code examples**: Provide clear, working code snippets

### Technical Contributions
- **Fix bugs**: Help resolve issues in the codebase
- **Improve design**: Enhance UI/UX and accessibility
- **Add features**: Implement new functionality
- **Optimize performance**: Improve site speed and efficiency

### Community Contributions
- **Answer questions**: Help other learners in discussions
- **Review pull requests**: Provide feedback on contributions
- **Report issues**: Identify bugs or suggest improvements
- **Spread the word**: Share the project with others

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v16 or higher)
- **npm** or **yarn**
- **Git**
- **Code editor** 

### Local Development Setup

1. **Fork the repository**
   ```bash
   # Click the "Fork" button on GitHub
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/the-gopher-project.git
   cd the-gopher-project
   ```

3. **Install dependencies**
   ```bash
   npm install
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:4321`

### Project Structure

```
src/
├── components/          # Reusable Astro components
├── layouts/            # Page layouts
│   ├── Layout.astro         # Base layout
│   └── MarkdownLayout.astro # Markdown content layout
├── pages/              # Page routes
│   ├── index.astro          # Homepage
│   ├── roadmap.astro        # Learning roadmap
│   └── go/                  # Go lesson content
│       ├── the-beginning/
│       └── the-basics/
└── styles/             # Global styles
    └── global.css
```

## 🔄 Development Workflow

1. **Create a new branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/issue-description
   ```

2. **Make your changes**
   - Write code or content
   - Test your changes locally
   - Ensure everything works as expected

3. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add new lesson on Go interfaces"
   ```

4. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Create a pull request**
   - Go to the original repository
   - Click "New Pull Request"
   - Fill out the PR template

## ✍️ Writing Guidelines

### Content Structure

**For new lessons:**
1. **Frontmatter**: Include layout, title, subtitle, and backlink
2. **Introduction**: Brief overview of what will be covered
3. **Main content**: Step-by-step explanations with examples
4. **Code examples**: Working, tested code snippets
5. **Assignment**: Practical exercises for learners

### Writing Style

- **Clear and concise**: Use simple, direct language
- **Beginner-friendly**: Assume no prior knowledge
- **Practical**: Include real-world examples
- **Engaging**: Use analogies and relatable examples
- **Consistent**: Follow the established tone and style

### Markdown Guidelines

```markdown
---
layout: "../../../layouts/MarkdownLayout.astro"
title: "Your Lesson Title"
subtitle: "Section Name"
backlink: "/roadmap#section-anchor"
---

# Your Lesson Title

Brief introduction paragraph explaining what this lesson covers.

## Main Section

Content with explanations...

### Subsection

More detailed content...

```go
// Always include comments in code examples
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

## Assignment

1. First task with clear instructions
2. Second task building on the first
```

## 🎨 Code Style Guidelines

### Astro Components
- Use meaningful component names
- Keep components focused and reusable
- Include proper TypeScript types
- Add comments for complex logic

### CSS/Styling
- Use Tailwind CSS classes when possible
- Follow the existing color scheme
- Ensure responsive design
- Maintain accessibility standards

### Go Code Examples
- Follow standard Go formatting (`gofmt`)
- Include meaningful variable names
- Add comments explaining complex concepts
- Ensure all examples compile and run

## 📝 Commit Message Guidelines

Use the conventional commits format:

```
type(scope): description

[optional body]

[optional footer]
```

### Types
- `feat`: New feature or lesson
- `fix`: Bug fix or correction
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code changes that neither fix a bug nor add a feature
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

### Examples
```
feat(lessons): add variables and constants lesson
fix(layout): correct responsive navigation on mobile
docs(readme): update installation instructions
style(css): improve list styling in markdown layout
```

## 🔍 Pull Request Process

### Before Submitting

1. **Test your changes**
   - Run the development server
   - Check all affected pages
   - Verify responsive design

2. **Update documentation**
   - Update README if needed
   - Add comments to complex code

3. **Follow the checklist**
   - [ ] Changes are tested locally
   - [ ] Code follows style guidelines
   - [ ] Commit messages are descriptive
   - [ ] Documentation is updated

### PR Template

When creating a PR, include:

```markdown
## Description
Brief description of what this PR does

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Code refactoring

## Testing
- [ ] Tested locally
- [ ] All examples work correctly
- [ ] Responsive design verified

## Screenshots (if applicable)
Add screenshots for UI changes
```

## 🐛 Issue Reporting

### Before Creating an Issue

1. **Search existing issues** to avoid duplicates
2. **Check the FAQ** for common questions
3. **Try the latest version** to see if it's already fixed

### Creating a Good Issue

Include:
- **Clear title** describing the problem
- **Steps to reproduce** the issue
- **Expected behavior** vs **actual behavior**
- **Screenshots** if applicable
- **Environment details** (OS, browser, etc.)

### Issue Templates

**Bug Report:**
```markdown
## Bug Description
Clear description of the bug

## Steps to Reproduce
1. Go to '...'
2. Click on '...'
3. See error

## Expected Behavior
What should happen

## Actual Behavior
What actually happens

## Environment
- OS: [e.g., macOS, Windows, Linux]
- Browser: [e.g., Chrome, Firefox, Safari]
- Version: [e.g., 1.0.0]
```

## 🎯 Specific Contribution Areas

### Content Writing
- Check the [learning roadmap](src/pages/roadmap.astro) for needed lessons
- Look for `// TODO` comments in existing lessons
- Review and improve existing content

### Code Improvements
- Enhance responsive design
- Improve accessibility
- Optimize performance
- Add new features

### Design Enhancements
- Improve visual hierarchy
- Enhance user experience
- Add animations or transitions
- Create new components

## 📞 Getting Help

Need help contributing?

- **GitHub Discussions**: Ask questions about contributing
- **Discord**: Join our community for real-time help
- **Issues**: Create an issue with the "help wanted" label

## 🙏 Recognition

All contributors are recognized in:
- GitHub contributors page
- Annual contributor highlights
- Community Discord channels

Thank you for making The Gopher Project better for everyone! 🚀
