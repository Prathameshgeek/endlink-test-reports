# Endlink Test Reports Repository

[![Tests Status](https://img.shields.io/badge/tests-automated-brightgreen)](https://github.com/Prathameshgeek/endlink-test-reports)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-blue)](https://prathameshgeek.github.io/endlink-test-reports/)
[![Jenkins](https://img.shields.io/badge/CI%2FCD-Jenkins-orange)](https://jenkins.io/)

## 📋 Overview

This repository serves as a centralized hub for hosting automated test reports generated from the **Endlink Web Automation** project. The reports are automatically published via Jenkins CI/CD pipeline and made accessible through GitHub Pages.

## 🏗️ Repository Structure

```
endlink-test-reports/
├── reports/                    # Historical test reports (last 30 runs)
│   ├── {BUILD_NUMBER}_{TIMESTAMP}_{ENVIRONMENT}/
│   │   ├── index.html         # Main report entry point
│   │   ├── ExtentReport.html  # Detailed Extent Report
│   │   └── ...                # Supporting report files
│   └── ...
├── latest/                    # Latest test run report
│   ├── index.html            # Quick access to most recent results
│   ├── ExtentReport.html     # Latest detailed report
│   └── ...                   # Supporting files
└── README.md                 # This file
```


## 🔧 Automated Pipeline Features

### 🎯 Multi-Environment Testing
- **QA Environment**: Default testing environment for daily automated runs
- **Production Environment**: On-demand production testing with parameter selection

### ⏰ Scheduled Execution
- **Daily Automated Runs**: Every day at 9:00 AM (QA environment)
- **Manual Triggers**: On-demand execution with environment selection

### 🧹 Automatic Cleanup
- **Smart Retention**: Automatically maintains last 30 test runs
- **Storage Optimization**: Removes reports older than 30 days to prevent repository bloat

### 📧 Notifications
- **Email Reports**: Configurable email notifications with test results
- **Build Status**: Real-time status updates for each test execution

## 📝 Report Details

Each test report includes:
- **Test Execution Summary**: Pass/fail statistics and overall health
- **Environment Information**: Target environment (QA/Production) details
- **Timestamp**: Precise execution time and build number
- **Detailed Results**: Comprehensive test case results with screenshots
- **Error Analysis**: Detailed failure analysis when applicable

## 🔄 Integration Details

### Source Repository
- **Main Project**: [Endlink Web Automation](https://github.com/Prathameshgeek/Endlink_WebAutomation)
- **Technology Stack**: Selenium WebDriver + Java + Maven
- **Test Framework**: TestNG with Extent Reports

### CI/CD Pipeline
- **Build Tool**: Jenkins
- **Deployment**: GitHub Pages
- **Authentication**: Secure token-based GitHub integration
- **Build Retention**: Last 7 Jenkins builds maintained

## 📋 Build Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `ENVIRONMENT` | Choice | QA | Target environment (QA/Production) |
| `SEND_EMAIL` | Boolean | true | Enable/disable email notifications |

## 🛠️ Technical Configuration

### Prerequisites
- Jenkins with GitHub integration
- Maven 3.8.6+
- JDK 11
- Valid GitHub Personal Access Token

### Environment Variables
- `GITHUB_TOKEN`: GitHub authentication token
- `TEST_ENVIRONMENT`: Target environment for test execution
- `BUILD_TIMESTAMP`: Unique identifier for each build

## 📊 Report Metrics

The repository automatically tracks:
- **Test Execution Trends**: Success/failure rates over time
- **Environment Stability**: Comparative analysis between QA and Production
- **Performance Metrics**: Test execution duration and reliability
- **Coverage Analysis**: Feature coverage across different environments

## 🚨 Troubleshooting

### Common Issues
1. **Missing Reports**: Check Jenkins build logs for execution errors
2. **Broken Links**: Verify GitHub Pages deployment status
3. **Old Reports**: Automatic cleanup removes reports older than 30 days

### Support
For technical issues or questions regarding test reports:
- **Email**: prathamesh@geekyants.com
- **Team**: Geekyants QA Team

## 📜 License

This repository contains automated test reports and is maintained by the Geekyants QA Team.

---

**Last Updated**: Auto-generated via Jenkins Pipeline  
**Maintained By**: Geekyants QA Team  
**Report Generation**: Automated via Jenkins CI/CD
