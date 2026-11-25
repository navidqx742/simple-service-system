# CI/CD Pipeline - Bank System

## Pipeline Stages

1. Developer pushes code to GitHub.
2. CI Pipeline starts.
3. Project files are checked.
4. Test cases are executed.
5. Test results are checked.
6. If tests pass, Docker Image is built.
7. If tests fail, pipeline stops.
8. If all stages succeed, application is deployed.

## Test Failure Handling

If a test fails:

- Pipeline stops.
- Failed test is reported.
- Error details are displayed.
- Developer fixes the problem.
- Pipeline runs again after a new push.

## Example Error

Test Case: TC-05

Expected Result: 400 Bad Request

Actual Result: 500 Internal Server Error

Pipeline Result: FAILED

Action: Stop the pipeline and report the error.

## Docker Integration

- Docker builds the application image.
- Docker Build runs after successful tests.
- If tests fail, Docker Image is not built.
- The Docker Image is used to create a container.
- The container runs the application.

## Pipeline Success

Status: SUCCESS

All tests passed and the Docker Image was created successfully.
flowchart TD
    A["Developer Push"] --> B["GitHub Repository"]
    B --> C["Build Project"]
    C --> D["Run Test Cases"]
    D --> E{"Tests Passed?"}

    E -->|No| F["Stop Pipeline"]
    F --> G["Show Error Report"]

    E -->|Yes| H["Docker Build"]
    H --> I["Create Docker Image"]
    I --> J["Run Container"]
    J --> K["Application Ready"]
