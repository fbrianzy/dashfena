# Contributing Guide

Welcome to the Dashfena project. This document provides comprehensive guidelines for contributing to the development and documentation of the Dashfena dashboard system.

Dashfena is an interactive Flask-based dashboard built for BPS Sidoarjo to visualize, analyze, and manage news phenomena data through GitHub-integrated CSV files.

## Project Overview

### Purpose

Dashfena serves as a data visualization and management platform for economic, social, and developmental phenomena in Sidoarjo, Indonesia. The system enables:

- Real-time data synchronization from GitHub repositories
- Interactive trend analysis and visualization
- Comprehensive administrative data management
- Professional server monitoring through desktop control panel

### Architecture

The project follows a modular Flask architecture with clear separation of concerns:

- **Configuration Layer**: Centralized settings and configurations
- **Routes Layer**: HTTP request handling and routing
- **Services Layer**: Business logic and data processing
- **Utilities Layer**: Helper functions and common operations
- **Middlewares Layer**: Request/response processing and validation
- **Security Layer**: Authentication, authorization, and protection mechanisms
- **Logging Layer**: Comprehensive event and error logging

## Getting Started

### Prerequisites

Before contributing, ensure you have:

- Python 3.8 or higher installed
- Git for version control
- Code editor (VS Code, PyCharm, or similar)
- Basic understanding of Flask framework
- Familiarity with REST APIs and HTTP protocols
- Understanding of CSV data structures
- GitHub account with repository access

## Contribution Guidelines

### Code Standards

**Python Style Guide**

Follow PEP 8 guidelines with these specifications:

- Use 4 spaces for indentation
- Maximum line length: 100 characters
- Use descriptive variable and function names
- Add docstrings to all functions and classes
- Use type hints where applicable

**Import Organization**

Order imports as follows:

```python
# Standard library imports
import os
import sys
from datetime import datetime

# Third-party imports
from flask import Flask, request, jsonify
import requests

# Local application imports
from app.config import settings
from app.services import csvLoader
from app.utils import validators
```

**Naming Conventions**

- Modules: `lowercase_with_underscores.py`
- Classes: `PascalCase`
- Functions: `lowercase_with_underscores()`
- Constants: `UPPERCASE_WITH_UNDERSCORES`
- Private methods: `_leading_underscore()`

### Git Workflow

**Branch Naming**

Use descriptive branch names with prefixes:

- `feature/description` - New features
- `bugfix/description` - Bug fixes
- `hotfix/description` - Critical fixes
- `refactor/description` - Code refactoring
- `docs/description` - Documentation updates

**Commit Messages**

Follow conventional commit format:

```
type(scope): subject

body (optional)

footer (optional)
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting)
- `refactor`: Code refactoring
- `test`: Test additions or modifications
- `chore`: Maintenance tasks

## Development Areas

### Adding New Routes

When adding new routes, follow this structure:

1. Create route file in appropriate directory
2. Define blueprint and routes
3. Implement route handlers
4. Add necessary middleware
5. Update documentation

### Adding New Services

Services handle business logic:

1. Create service file in `app/services/`
2. Implement service functions
3. Add error handling
4. Document functions
5. Add unit tests

### Improving CPanel

The desktop control panel accepts contributions for:

- Enhanced log visualization
- Additional monitoring features
- Performance optimizations
- UI/UX improvements

When modifying CPanel:

1. Maintain backward compatibility
2. Test on Windows environment
3. Update version number appropriately
4. Document new features

## Documentation

### Code Documentation

- Add docstrings to all functions and classes
- Use clear, concise language
- Include parameter types and return values
- Provide usage examples where helpful

### Project Documentation

When updating documentation:

- Keep README.md comprehensive but concise
- Update CHANGELOG.md for all versions
- Maintain SECURITY.md for security policies
- Document breaking changes clearly

## Data Access

The main data repository is publicly accessible:

**Repository**: https://github.com/fbrianzy/database-fenomena/tree/main/data

This data is freely available for:
- Development and testing
- Local experimentation
- Feature development
- Documentation examples

## Community Guidelines

### Code of Conduct

All contributors must adhere to professional standards:

- Be respectful in all interactions
- Provide constructive feedback
- Value clarity and accuracy
- Maintain professional tone
- Focus on technical merit
- Avoid personal information
- Respect intellectual property
- No political or religious discussions

### Communication Channels

- **Issues**: Bug reports and feature requests
- **Pull Requests**: Code contributions and reviews
- **Email**: dashfena.dev@dashfena.bps.go.id for sensitive matters

### Review Process

All contributions undergo review:

1. Automated tests must pass
2. Code style checks must pass
3. Documentation must be updated
4. At least one maintainer approval required
5. No merge conflicts
6. Breaking changes must be justified

### Response Times

- **Issues**: Response within 72 hours
- **Pull Requests**: Initial review within 5 business days
- **Security Issues**: Response within 24 hours

## Recognition

Contributors will be recognized in:

- Release notes and changelog
- Project documentation
- GitHub contributors page

Significant contributions may result in:

- Maintainer status
- Direct commit access
- Involvement in architectural decisions

## License Agreement

By contributing to Dashfena, you agree that:

- Your contributions are licensed under the MIT License
- Your contributions may be incorporated into official releases
- You have the right to submit the contributed work
- Your contributions do not violate any third-party rights

## Questions and Support

For questions or assistance:

- Open an issue for technical questions
- Email dashfena.dev@gmail.com for general inquiries
- Review existing documentation and issues first

## Project Lead

**Lead Developer**: Bagus Febriansyah Pratama

**GitHub**: https://github.com/fbrianzy

**Email**: dashfena.dev@dashfena.bps.go.id

---

Thank you for contributing to Dashfena. Your efforts help improve data visualization and management for BPS Sidoarjo and the wider community.
