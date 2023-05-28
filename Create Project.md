---
created: Tuesday 16th May 2023 03:24:47
modified: Thursday 18th May 2023 01:20:48
---
#integration #usageInstructions 

Creates a new project within the FileShare service.

Required properties:

-   projectID: A unique identifier for the project.
-   projectName: The name of the project.
-   projectDescription: A brief description of the project.
-   projectOwner: The user or entity that owns the project.

Optional properties:

-   projectStartDate: The start date of the project.
-   projectEndDate: The end date of the project.
-   projectTags: Additional tags or labels associated with the project.

The Create Project API operation allows users to create a new project by providing the necessary details. The projectID must be unique to avoid conflicts with existing projects. The projectOwner identifies the user or entity responsible for managing the project. Optional properties such as projectStartDate, projectEndDate, and projectTags can be included to provide additional information or categorization for the project.

Endpoint: `POST /projects`

Request Body:
{
  "projectID": "123456789",
  "projectName": "Sample Project",
  "projectDescription": "This is a sample project for demonstration purposes.",
  "projectOwner": "John Doe",
  "projectStartDate": "2023-05-21",
  "projectEndDate": "2023-08-31",
  "projectTags": ["sample", "demo"]
}

LINKS:
[[FileShare API endpoints]]


