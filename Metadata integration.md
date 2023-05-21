---
created: <% tp.file.creation_date("dddd Do MMMM YYYY HH:mm:ss") %>
modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
#integration #knownIssues

When an [[FileShare Operation]] is completed, a related Metadata record is created by [[FileShare Service]].  
This Design Document explains how the Audit Records are handled by the service.

# Step-by-Step
1.  [[FileShare Operation]] completed
2.  Metadata record is created
3.  Metadata record saved in FileShare Database
5.  The CleanMetadata WebJob is run daily. It
    1.  Sends created Metadata record from FileShare Database to [[Metadata Service]]
    2.  If operation is successful, the Metadata record is marked as 'sent' = 'true' (default is 'false')
    3.  Removes earliest sent records
    4.  Leaves not-sent records
6.  **[Currently disabled]** ResendRecords WebJob  
    _Disabling this WebJob might cause a build-up of non-acknowledged Audit Records._

LINKS:
[[FileShare Service]]



