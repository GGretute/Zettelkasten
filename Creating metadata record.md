---
created: <% tp.file.creation_date("dddd Do MMMM YYYY HH:mm:ss") %>
modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
#integration 

Metadata Records can be created after [[Registering a service]].

Required properties:
-   id - identifies metadata record. It needs to be unique.
-   eventType - identifies the type of event
-   eventTime - the time when even occurred
-   source - the initiator of event
-   serviceRegistrationId - registered service in Audit Trail Id
-   data - object containing all event related information

Optional properties:
-   userId - the id of user who initiated an event

Here is a bit modified example from Project Share:  
`POST /Metadata`

```
{
  "id": "8787998-97879789",
  "eventType": "com.projectshareservice.folder.create",
  "eventTime": "2020-06-03T16:19:15.566693Z",
  "source": "testService.com",
  "serviceRegistrationId": "cb7532f8-f5b9-4dcb-b85c-0310758ea534",
  "userId": "465465-132446",
  "data": {
    "messageDetails": {
      "instanceType": "Folder",
      "instanceID": "52baa8cd-95e1-4ee7-964f-5e78c8402668",
      "actionPerformedBy": "465465-132446",
      "actionPerformedByName": "John Doe"
    },
    "propertiesAfterEvent": {
      "name": "TestName",
      "type": "Folder",
      "createdBy": "465465-132446",
      "createdTimeStamp": "2020-06-03T16:19:15.566693Z"
    }
  }
}

```

Optional properties can be left unset but it is highly recommended to set them when possible. Those properties will help to map metadata records easier and consistently between same service which uses [[Metadata Service]] and between multiple services.

Data in the data property will be used for generating dashboards. It is up to developers to put useful information there. If only ids will be in the metadata record then only they will represented in the dashboards or other analysis results.

LINKS:
[[Metadata Service]]
