---
created: Saturday 13th May 2023 22:46:33
modified: Thursday 18th May 2023 01:23:50
---
#usageInstructions #integration 

The "Get Metadata" operation in the FileShare service allows users to retrieve the metadata information associated with a specified file or folder. This operation provides valuable details about the file or folder, such as its name, type, size, creation date, and modification date. By accessing the metadata, users can obtain essential information about the file or folder without retrieving the actual content. This operation is useful for various purposes, including file organization, auditing, and tracking file attributes.

**Properties for Get Metadata Operation:**

-   `fileId` (required): The unique identifier of the file or folder for which metadata is requested.

**Example Request:**

GET /metadata/{fileId}

**Example Response:**

{
  "fileId": "123456789",
  "name": "example_file.txt",
  "type": "text/plain",
  "size": "256 KB",
  "createdDate": "2023-05-21",
  "modifiedDate": "2023-05-22",
  "owner": "john@example.com",
  "permissions": {
    "read": true,
    "write": true,
    "delete": false
  },
  "tags": ["important", "documents"],
  "sharedWith": ["jane@example.com", "mark@example.com"]
}

LINKS:
[[FileShare Service]]
[[Metadata integration]]


