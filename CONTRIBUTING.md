# 🤝 Contributing to ProtectClone

Thank you for your interest in contributing to **ProtectClone**! We welcome contributions from the community and are excited to see what you can bring to this project. 🎉

## 📋 Table of Contents

- [Code of Conduct](#-code-of-conduct)
- [How Can I Contribute?](#-how-can-i-contribute)
- [Getting Started](#-getting-started)
- [Development Setup](#-development-setup)
- [Coding Standards](#-coding-standards)
- [Submitting Changes](#-submitting-changes)
- [Issue Guidelines](#-issue-guidelines)
- [Pull Request Process](#-pull-request-process)
- [Community](#-community)

---

## 📜 Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

---

## 🚀 How Can I Contribute?

### 🐛 Reporting Bugs

Found a bug? Help us fix it by:

1. **Check existing issues** to avoid duplicates
2. **Use the issue template** when creating new bug reports
3. **Provide detailed information**:
   - Your operating system and Python version
   - Steps to reproduce the issue
   - Expected vs actual behavior
   - Error messages or logs
   - Screenshots if applicable

### 💡 Suggesting Enhancements

Have an idea for improvement? We'd love to hear it:

1. **Check existing feature requests** first
2. **Create a detailed proposal** including:
   - Use case description
   - Benefits to users
   - Implementation considerations
   - Examples or mockups if applicable

### 🔧 Code Contributions

We welcome code contributions! Areas where help is especially appreciated:

- 🐛 **Bug fixes**
- ✨ **New features**
- 📚 **Documentation improvements**
- 🧪 **Tests and test coverage**
- 🎨 **UI/UX enhancements**
- ⚡ **Performance optimizations**

---

## 🛠️ Getting Started

### Prerequisites

- Python 3.7 or higher
- Git
- A Telegram account and API credentials
- Basic knowledge of Python and async programming

### First-Time Setup

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/<your-username>/protect-clone.git
   cd protect-clone
   ```
3. **Add the upstream remote**:
   ```bash
   git remote add upstream https://github.com/<your-username>/protect-clone.git
   ```

---

## 💻 Development Setup

### Environment Setup

1. **Create a virtual environment**:
   ```powershell
   python -m venv .env
   .env\Scripts\activate  # Windows
   source .env/bin/activate  # Linux/macOS
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   pip install -r requirements-dev.txt  # Development dependencies
   ```

3. **Set up pre-commit hooks** (if available):
   ```bash
   pre-commit install
   ```

### Testing Your Changes

Before submitting any changes:

1. **Run the script** with different modes to ensure functionality
2. **Test edge cases** (network errors, invalid inputs, etc.)
3. **Verify compatibility** with different Python versions
4. **Check for memory leaks** in long-running operations

---

## 📝 Coding Standards

### Python Style Guide

- Follow **PEP 8** style guidelines
- Use **4 spaces** for indentation (no tabs)
- Maximum line length: **88 characters**
- Use **meaningful variable and function names**
- Add **docstrings** for functions and classes

### Code Quality

```python
# Good example
async def clone_channel_messages(app, source_id, dest_id, mention_mode):
    """
    Clone messages from source channel to destination channel.
    
    Args:
        app: Pyrogram client instance
        source_id: Source channel ID or username
        dest_id: Destination channel ID or username
        mention_mode: 1 for mention, 2 for hide author
    
    Returns:
        bool: True if successful, False otherwise
    """
    try:
        # Implementation here
        pass
    except Exception as e:
        logger.error(f"Failed to clone messages: {e}")
        return False
```

### Code Organization

- **Keep functions focused** and single-purpose
- **Use async/await** properly for I/O operations
- **Handle exceptions gracefully**
- **Add logging** for debugging and monitoring
- **Avoid hardcoded values** - use configuration

---

## 📤 Submitting Changes

### Workflow

1. **Create a new branch** for your feature/fix:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/issue-number
   ```

2. **Make your changes** following the coding standards

3. **Commit your changes** with descriptive messages:
   ```bash
   git add .
   git commit -m "feat: add batch download functionality

   - Implement parallel downloading for multiple files
   - Add progress tracking for batch operations
   - Include error handling for failed downloads
   
   Closes #42"
   ```

4. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Create a Pull Request** on GitHub

### Commit Message Format

Use [Conventional Commits](https://www.conventionalcommits.org/) format:

```
type(scope): short description

[optional body]

[optional footer]
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

---

## 🐛 Issue Guidelines

### Before Creating an Issue

- [ ] Search existing issues to avoid duplicates
- [ ] Use the latest version of the code
- [ ] Provide minimal reproduction steps

### Issue Templates

#### Bug Report
```markdown
**Describe the bug**
A clear description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. Run command '...'
2. Enter channel ID '...'
3. Select option '...'
4. See error

**Expected behavior**
What you expected to happen.

**Environment:**
- OS: [e.g., Windows 10]
- Python version: [e.g., 3.9.0]
- Pyrogram version: [e.g., 2.0.0]

**Additional context**
Add any other context about the problem here.
```

#### Feature Request
```markdown
**Is your feature request related to a problem?**
A clear description of what the problem is.

**Describe the solution you'd like**
A clear description of what you want to happen.

**Describe alternatives you've considered**
Any alternative solutions or features you've considered.

**Additional context**
Add any other context or screenshots about the feature request here.
```

---

## 🔄 Pull Request Process

### PR Checklist

Before submitting your PR, ensure:

- [ ] Code follows the project's coding standards
- [ ] All existing tests pass
- [ ] New features include appropriate tests
- [ ] Documentation is updated if needed
- [ ] Commit messages follow the conventional format
- [ ] PR description clearly explains the changes

### PR Template

```markdown
## Description
Brief description of the changes made.

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update

## Testing
Describe the tests you ran to verify your changes.

## Checklist
- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
```

### Review Process

1. **Automated checks** will run on your PR
2. **Maintainers will review** your code
3. **Address feedback** promptly and professionally
4. **Squash commits** if requested before merge

---

## 🌟 Community

### Getting Help

- 💬 **GitHub Discussions**: For questions and general discussion
- 🐛 **GitHub Issues**: For bug reports and feature requests
- 📧 **Email**: For private inquiries

### Recognition

Contributors are recognized in:
- The project's `README.md`
- Release notes for significant contributions
- GitHub's contributors graph

---

## 🎉 Thank You!

Your contributions make this project better for everyone. Whether you're fixing a typo, reporting a bug, or implementing a major feature, every contribution is valued and appreciated!

**Happy coding!** 🚀

---

<div align="center">

[![Contributors](https://contrib.rocks/image?repo=juansilvadesign/protect-clone)](https://github.com/juansilvadesign/protect-clone/graphs/contributors)

*Made with ❤️ by the ProtectClone community*

</div>