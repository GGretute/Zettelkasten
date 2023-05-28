---
created: Tuesday 16th May 2023 03:30:38
modified: Thursday 18th May 2023 01:31:43
---
#design

| Requirement or constraints                      | Solution approach                                                                                           |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| FS.RG1                                        | [[FileShare ]] exposes endpoints for storing files and folders.                                          |
| FS.RG2                                        | User [[permissions]] to access a file or folder are checked before returning file/folder information and download or upload URL.  |
| FS.RG4                                        | FileShare must log changes for the file and last modification data.                                          |
| FS.RG5                                        | There should be a possibility to make a versioned file and track its changes.                                |

FileShare endpoints for file and folder operations and information.

File/folder create: To create a file or create a folder - parent folder information must be provided. The client app then calls the file/folder endpoint that allows the creation of a file or folder. If a file is created successfully - the upload URL is provided.

LINKS:
[[FileShare Service]]
[[Permissions]]

