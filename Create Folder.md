---
created: Tuesday 16th May 2023 03:25:23
modified: Thursday 18th May 2023 01:20:13
---
#integration #usageInstructions 

Creates a new folder within the FileShare service.

Required properties:

-   folderID: A unique identifier for the folder.
-   folderName: The name of the folder.

Optional properties:

-   folderDescription: A brief description of the folder.
-   folderTags: Additional tags or labels associated with the folder.

The Create Folder API operation allows users to create a new folder in the FileShare service. The folderID must be unique to avoid conflicts with existing folders. Users need to provide the folderName, ensuring proper identification and organization of the folder structure. Optional properties such as folderDescription and folderTags can be included to provide additional information or categorization for the folder.

Endpoint: `POST /folders`

Request Body:
{
  "folderID": "abc123",
  "folderName": "Sample Folder",
  "folderDescription": "This is a sample folder for organizing files.",
  "folderTags": ["sample", "folder"]
}

LINKS:
[[FileShare API endpoints]]

