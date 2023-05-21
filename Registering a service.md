---
created: <% tp.file.creation_date("dddd Do MMMM YYYY HH:mm:ss") %>
modified: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
#integration #usageInstructions 

All service needs to be registered. Data will be partitioned by service's registration id which will be given after the creation of service instance in the [[Metadata Service]].

`POST /ServiceRegistration`

```
{
  "name": "My Service",
  "ownerEmail": "name.surname@mail.com",
  "regId": "112233"
}
```

Required properties are _name_, _ownerEmail_ and regId.  

_serviceRegistrationId_ will be set in the response. This property should be used while [[Creating metadata record]] or [[Retrieving metadata record]]

LINKS:
[[Metadata Service]]


