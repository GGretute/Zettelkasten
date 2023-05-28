---
created: Tuesday 16th May 2023 03:26:05
modified: Thursday 18th May 2023 01:19:52
---
#integration #usageInstructions 

Creates a new file within the FileShare service.

Required properties:

-   fileID: A unique identifier for the file.
-   fileName: The name of the file.
-   fileType: The type or format of the file.
-   fileContent: The content or data contained within the file.

Optional properties:

-   fileDescription: A brief description of the file.
-   fileTags: Additional tags or labels associated with the file.

The Create File API operation enables users to upload and create a new file in the FileShare service. The fileID must be unique to avoid conflicts with existing files. Users need to provide the fileName and specify the fileType, ensuring proper identification and handling of the file. The fileContent represents the actual data or content contained within the file. Optional properties such as fileDescription and fileTags can be included to provide additional information or categorization for the file.

Endpoint: `POST /files`

Request Body:
{
  "fileID": "987654321",
  "fileName": "Sample File.docx",
  "fileType": "document",
  "fileContent": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec euismod eros a nisi interdum.",
  "fileDescription": "This is a sample document file.",
  "fileTags": ["sample", "document"]
}


LINKS:
[[FileShare API endpoints]]