# Contributing to Isaree

Thank you for your interest in contributing to Isaree! As an open-source medical AI platform, we welcome contributions from developers, healthcare professionals, researchers, and anyone interested in advancing AI in healthcare.

This document provides guidelines and instructions for contributing to the project. By participating, you are expected to uphold our [Code of Conduct](CODE_OF_CONDUCT.md).

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)
- [Testing Guidelines](#testing-guidelines)
- [Documentation](#documentation)
- [Medical Compliance Considerations](#medical-compliance-considerations)
- [Community](#community)

## Code of Conduct

Our community strives to be open, inclusive, and respectful. Please read our [Code of Conduct](CODE_OF_CONDUCT.md) before contributing.

## Getting Started

### Prerequisites

- Node.js 18+
- Python 3.9+
- Docker (for containerized development)
- Git

### Setting Up Your Development Environment

1. Fork the repository on GitHub
2. Clone your fork locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/isaree.git
   cd isaree
   ```
3. Add the original repository as an upstream remote:
   ```bash
   git remote add upstream https://github.com/isaree/isaree.git
   ```
4. Install dependencies:
   ```bash
   npm install
   ```
5. Set up pre-commit hooks:
   ```bash
   npm run setup-hooks
   ```

## Development Workflow

1. Create a new branch for your feature or bugfix:
   ```bash
   git checkout -b feature/your-feature-name
   ```
   or
   ```bash
   git checkout -b fix/issue-you-are-fixing
   ```

2. Make your changes, following our [coding standards](#coding-standards)

3. Write or update tests as necessary

4. Run tests locally:
   ```bash
   npm test
   ```

5. Update documentation as needed

6. Commit your changes with a clear commit message:
   ```bash
   git commit -m "feat: add new feature X that does Y"
   ```
   We follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages.

7. Push your branch to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```

8. Open a pull request against the `main` branch of the original repository

## Pull Request Process

1. Ensure your PR includes a clear description of the changes and the value they add
2. Link any relevant issues using keywords (e.g., "Fixes #123")
3. Make sure all tests pass in the CI pipeline
4. Update documentation as necessary
5. Add your changes to the CHANGELOG.md file under the "Unreleased" section
6. Request a review from at least one maintainer
7. Address any feedback from reviewers
8. Once approved, a maintainer will merge your PR

## Coding Standards

### General Guidelines

- Write clean, readable, and maintainable code
- Follow the principle of "Do One Thing Well"
- Keep functions small and focused
- Use meaningful variable and function names
- Comment complex logic, but prefer self-documenting code

### JavaScript/TypeScript

- We follow the [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
- Use TypeScript for type safety
- Use async/await for asynchronous code
- Use ES6+ features when appropriate

### Python

- Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/) style guide
- Use type hints (PEP 484)
- Use docstrings for all public functions, classes, and modules

## Testing Guidelines

- Write unit tests for all new functionality
- Aim for at least 80% code coverage
- Include integration tests for complex features
- For medical components, include validation against standard datasets where applicable

### Running Tests

```bash
# Run all tests
npm test

# Run specific test suite
npm test -- --suite=client-layer

# Run tests with coverage report
npm test -- --coverage
```

## Documentation

Good documentation is crucial for a medical AI platform. Please follow these guidelines:

- Update README.md if you change functionality
- Document all public APIs, functions, and classes
- Include examples for complex features
- For medical components, clearly document limitations and intended use cases
- Update architecture diagrams if you change system design

## Medical Compliance Considerations

As a medical AI platform, Isaree has special compliance requirements:

- All code must adhere to our security standards
- Patient data, even synthetic, must be handled according to our [Data Governance Policy](docs/compliance/data-governance.md)
- New features must include a compliance assessment
- AI models must include documentation on training data, limitations, and potential biases
- Any external dependencies must be evaluated for security and compliance

## Community

- Join our [GitHub Discussions](https://github.com/isaree/isaree/discussions) for questions and community support
- Report bugs and request features through [GitHub Issues](https://github.com/isaree/isaree/issues)
- For security issues, please follow our [Security Policy](SECURITY.md)

Thank you for contributing to Isaree and helping advance AI in healthcare!
