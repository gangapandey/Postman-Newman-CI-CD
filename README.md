
# Postman API Testing with Jenkins

## Overview
This project demonstrates automated API testing using Postman for the **Reqres.in** API. It integrates Jenkins for continuous integration, enabling automated test execution and reporting. This setup showcases my skills in API testing, CI/CD practices, and utilizing modern testing tools.

## Features
- **Postman Collection**: Comprehensive tests for various API endpoints provided by Reqres.in.
- **Automated Test Execution**: Tests are automatically run in Jenkins whenever changes are pushed to the repository.
- **HTML Reports**: Generates detailed HTML reports using Newman and the Newman HTML Extra reporter for easy viewing of test results.
- **Notifications**: Jenkins sends notifications in case of build failures, ensuring prompt attention to issues.

## Getting Started

### Prerequisites
To run this project locally, you need:
- [Node.js](https://nodejs.org/) installed on your machine.
- [Postman](https://www.postman.com/downloads/) for creating and testing API requests.
- [Newman](https://github.com/postmanlabs/newman) installed globally:
  
  ```bash
  
  npm install -g newman

  ```

## Running the test locally

### 1. Clone the repository
```bash
  git clone https://github.com/gangapandey/Postman-Newman-CI-CD.git
  ```
### 2. Run the postman collection using Newman
```bash
   newman run "Collection/reqres.in_tests.postman_collection.json" -r cli,html,htmlextra --reporter-html-export "Report/newman-report.html" --reporter-htmlextra-export "Report/newman-report-extra.html"
```

## Jenkins Integration
### Jenkins Configuration 
```bash
newman run "Collection/reqres.in_tests.postman_collection.json" -r cli,html,htmlextra --reporter-html-export "Report/newman-report.html" --reporter-htmlextra-export "Report/newman-report-extra.html"
```

## Common Issues and Troubleshooting

- **Issue: Newman Not Found**: If you encounter a "Newman not found" error, ensure Newman is installed globally and your PATH environment variable includes the npm global bin directory.
  
- **Issue: Postman Collection Not Found**: Ensure the path to your Postman collection is correct in the run command.
  
- **Issue: Report Generation Fails**: Ensure the `Report` directory exists or create it before running the Newman command.

## Newman HTML Extra Report Screenshots




## Acknowledgments
- **Reqres.in** for providing a great API for testing.
- **Postman** for the powerful API testing tool.
- **Jenkins** for continuous integration support.




  

