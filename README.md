# Dashfena - BPS Sidoarjo Phenomena Dashboard

## Overview

Dashfena is a production-grade web application designed for the Statistics Office (BPS) of Sidoarjo, Indonesia. The system provides comprehensive visualization and management capabilities for economic, social, and developmental phenomena data sourced directly from structured CSV files hosted on GitHub.

The application employs a modular Flask architecture with clear separation of concerns, featuring an integrated desktop control panel for server management and real-time log monitoring capabilities.

## Architecture

### Technology Stack

- **Backend Framework**: Flask (Python 3.8+)
- **Frontend**: Tailwind CSS 3, Font Awesome 6, Vanilla JavaScript
- **Control Panel**: Tkinter (Desktop Application)
- **Data Source**: GitHub Repository (CSV-based)
- **Session Management**: Flask-Session with server-side storage
- **Security**: CSRF Protection, Request Validation, Rate Limiting

## Features

### Core Functionality

**Real-Time GitHub Integration**
- Automatic synchronization with remote CSV data repository
- Branch-specific data fetching with configurable refresh intervals
- Intelligent caching mechanism to minimize API calls
- Last sync timestamp display on dashboard
- GitHub activity logging for audit trails

**Analytical Dashboard**
- Monthly trend visualization with interactive charts
- Category-based data segmentation
- Month-over-month growth calculations
- Sentiment analysis indicators
- Statistical summaries with percentage changes
- Real-time data updates from GitHub source

**Administrative Interface**
- Complete CRUD operations for phenomena entries
- CSV file upload with validation and parsing
- Bulk data operations support
- Direct GitHub repository updates
- Row and cell level editing capabilities
- File deletion and management
- Session-based authentication system
- System diagnostics and environment checking
- Cache management and status monitoring

**Desktop Control Panel**
- Tkinter-based server management application
- Real-time log monitoring across multiple categories
- Server start, stop, and restart controls
- Live server status indicators
- Log filtering and search capabilities
- Multiple log file viewing (ERROR, GET, POST, GITHUB, SECURITY, SERVER)
- Process monitoring and resource usage
- Color-coded log entries for better readability
- Splash screen with loading animations
- Theme customization support

### Technical Features

**Security Measures**
- CSRF token validation for all state-changing operations
- Session-based authentication with secure cookie handling
- Comprehensive request logging for suspicious activity detection
- Input sanitization and validation across all forms
- Rate limiting on sensitive endpoints
- IP address validation and geolocation utilities
- Security pattern detection for attack prevention
- Environment-based configuration for sensitive credentials

**Performance Optimization**
- Intelligent caching system for GitHub data
- Reduced API calls through strategic data persistence
- Optimized CSV parsing and data loading
- Lazy loading for large datasets
- Cache status monitoring and clearing capabilities
- Efficient log file handling with tail reading

**Logging System**
- Categorized logging (ERROR, GET, POST, GITHUB, SECURITY, SERVER)
- Real-time log tailing for monitoring
- Structured log format for easy parsing
- Log rotation support
- Separate security and admin logging
- HTTP request/response logging with detailed metadata

**Error Handling**
- Comprehensive error logging system
- Custom error pages for common HTTP errors (400, 403, 404, 405, 500, 503)
- Graceful degradation for API failures
- Detailed error traces in development mode
- User-friendly error messages in production

## Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Git
- GitHub personal access token with repository read permissions
- Windows OS for CPanel functionality (Linux/Mac compatible with modifications)

### Control Panel Features

The desktop control panel (CPanel) provides comprehensive server management:

**Server Management**
- Start, stop, and restart Flask server
- Real-time server status monitoring
- Process ID tracking
- Automatic server health checks

**Log Monitoring**
- Real-time log viewing with automatic updates
- Multi-file log support (ERROR, GET, POST, GITHUB, SECURITY, SERVER)
- Color-coded log entries for different severity levels
- Search and filter capabilities
- Log file path display with quick folder access

**User Interface**
- Modern themed interface with dark mode support
- Splash screen with loading animation
- Tabbed interface for different log categories
- Responsive layout with proper sizing
- System tray integration (optional)

### Accessing Admin Panel

**Admin Features:**
- Dashboard with system overview
- Data table with inline editing
- CSV file upload and processing
- Row and cell deletion
- Bulk data operations
- Cache management
- System diagnostics
- Environment variable checking
- Session debugging tools

## API Integration

### GitHub Data Source

The application connects to the following repository:

```
https://github.com/fbrianzy/database-fenomena
```

### Supported Categories

- Economy
- Social
- Infrastructure
- Health
- Education
- Environment
- Technology
- Government
- etc

### Migration from Legacy Code

The `legacy/` folder contains the original monolithic application for reference:
- `app.py`: Original 1000+ line Flask application
- `admin.py`: Original 800+ line admin module
- `admin_github.py`: Original GitHub integration
- Other supporting modules

These files are maintained for historical reference and should not be imported into the current application.

### Environment Recommendations

- Use environment variables for all sensitive data
- Enable HTTPS in production
- Configure proper firewall rules
- Set up automated backups for logs
- Implement log rotation policies
- Monitor server resources
- Regular security audits
- Keep dependencies updated

## Troubleshooting

### Common Issues

**Issue**: GitHub API rate limit exceeded

**Solution**: Implement longer cache durations or use authenticated requests with higher limits. Check cache configuration in `app/config/cache.py`.

---

**Issue**: CSRF token mismatch

**Solution**: Ensure consistent HOST configuration and clear browser cookies. Verify `FLASK_SECRET_KEY` in `.env` is properly set.

---

**Issue**: Import errors after refactoring

**Solution**: Verify `__init__.py` files exist in all packages and check import paths. Ensure virtual environment is activated.

---

**Issue**: CPanel won't start

**Solution**: Check Tkinter installation: `python -m tkinter`. Install if missing: `pip install tk`.

---

**Issue**: Logs not appearing

**Solution**: Verify write permissions for `logs/` directory. Check log configuration in `app/config/logger.py`.

---

**Issue**: Server won't stop from CPanel

**Solution**: Check process reader in `CPanel/services/procReader.py`. Manually terminate Python processes if needed.

---

**Issue**: Empty data on dashboard

**Solution**: Verify GitHub token and repository settings. Check `logs/GITHUB.log` for API errors. Ensure CSV files exist in repository.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on contributing to this project.

## Security

For security concerns, please review [SECURITY.md](SECURITY.md) and report vulnerabilities responsibly.

## Version History

See [CHANGELOG.md](CHANGELOG.md) for detailed version history and migration guides.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- BPS Sidoarjo for project requirements and domain expertise
- Flask community for comprehensive framework documentation
- Contributors to open-source libraries used in this project

## Contact

**Project Lead**: Bagus Febriansyah Pratama

**Email**: dashfena.dev@dashfena.bps.go.id

**GitHub**: https://github.com/fbrianzy/dashfena

**Data Repository**: https://github.com/fbrianzy/database-fenomena

---

**Version**: 3.0.0  
**Last Updated**: October 16, 2025  
**Status**: Production Ready
