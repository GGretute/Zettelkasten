---
created: <% tp.file.creation_date("dddd Do MMMM YYYY HH:mm:ss") %>
modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
#security

Metadata Service uses only OIDC for Authentication.  
Scopes:
-   metadata-api:read - allows [[Retrieving metadata record]]
-   metadata-api:write - enables [[Creating metadata record]]
-   metadata-api:reporting -  endpoints related to [[Registering a service]]

LINKS:
[[Metadata Service]]
