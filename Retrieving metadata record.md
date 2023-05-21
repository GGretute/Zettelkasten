---
created: <% tp.file.creation_date("dddd Do MMMM YYYY HH:mm:ss") %>
modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
#integration #usageInstructions 

After [[Creating metadata record]] it can be retrieved by GET request. It should contain details about what to look for, from when records should be checked, and how many of them should be retrieved.

`GET /Metadata?filter={FILTER_BY_PROPS}

LINKS:
[[Metadata Service]]


