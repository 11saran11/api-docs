# FloorPlanDesk

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of floorplandesks based on one or more filter querystring parameters.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="Id" type="int" %}
?Id=...
{% endapi-method-parameter %}

{% api-method-parameter name="UniqueId" type="Guid" %}
?UniqueId=...
{% endapi-method-parameter %}

{% api-method-parameter name="SystemId" type="string" %}
?FloorPlanDesk\_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="FloorPlan" type="FloorPlan" %}
?FloorPlanDesk\_FloorPlan=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker" type="Coworker" %}
?FloorPlanDesk\_Coworker=...
{% endapi-method-parameter %}

{% api-method-parameter name="Name" type="string" %}
?FloorPlanDesk\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="ItemType" type="enum" %}
?FloorPlanDesk\_ItemType=...
{% endapi-method-parameter %}

{% api-method-parameter name="Size" type="decimal" %}
?FloorPlanDesk\_Size=...
{% endapi-method-parameter %}

{% api-method-parameter name="Capacity" type="decimal" %}
?FloorPlanDesk\_Capacity=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" %}
?FloorPlanDesk\_Price=...
{% endapi-method-parameter %}

{% api-method-parameter name="Area" type="string" %}
?FloorPlanDesk\_Area=...
{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" %}
?FloorPlanDesk\_Notes=...
{% endapi-method-parameter %}

{% api-method-parameter name="Available" type="bool" %}
?FloorPlanDesk\_Available=...
{% endapi-method-parameter %}

{% api-method-parameter name="PositionX" type="int" %}
?FloorPlanDesk\_PositionX=...
{% endapi-method-parameter %}

{% api-method-parameter name="PositionY" type="int" %}
?FloorPlanDesk\_PositionY=...
{% endapi-method-parameter %}

{% api-method-parameter name="PositionZ" type="int" %}
?FloorPlanDesk\_PositionZ=...
{% endapi-method-parameter %}

{% api-method-parameter name="TunnelPrivateGroupId" type="string" %}
?FloorPlanDesk\_TunnelPrivateGroupId=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerContractIds" type="string" %}
?FloorPlanDesk\_CoworkerContractIds=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerContractFullNames" type="string" %}
?FloorPlanDesk\_CoworkerContractFullNames=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerContractStartDates" type="string" %}
?FloorPlanDesk\_CoworkerContractStartDates=...
{% endapi-method-parameter %}

{% api-method-parameter name="FloorPlan\_Name" type="string" %}
?FloorPlanDesk\_FloorPlan\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="FloorPlan\_Business\_Currency\_Code" type="string" %}
?FloorPlanDesk\_FloorPlan\_Business\_Currency\_Code=...
{% endapi-method-parameter %}

{% api-method-parameter name="FloorPlan\_Business\_Name" type="string" %}
?FloorPlanDesk\_FloorPlan\_Business\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_FullName" type="string" %}
?FloorPlanDesk\_Coworker\_FullName=...
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "FloorPlan": null,
        "Coworker": null,
        "Name": "00001",
        "ItemType": Nexudus.Coworking.Core.Enums.eFloorPlanItemType.Office,
        "Size": 00001,
        "Capacity": 00001,
        "Price": 00001,
        "Area": "00001",
        "Notes": "00001",
        "Available": true,
        "PositionX": 1,
        "PositionY": 1,
        "PositionZ": 1,
        "TunnelPrivateGroupId": "",
        "CoworkerContractIds": "",
        "CoworkerContractFullNames": "",
        "CoworkerContractStartDates": "",
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `floorplandesk-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of floorplandesks.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="dir" type="string" required=false %}
one of 'Ascending' or 'Ascending'
{% endapi-method-parameter %}

{% api-method-parameter name="orderby" type="string" required=false %}
?orderby=Id
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=false %}
?page=1
{% endapi-method-parameter %}

{% api-method-parameter name="size" type="integer" required=false %}
size=25 \(maximum=1000\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "FloorPlan": null,
        "Coworker": null,
        "Name": "00001",
        "ItemType": Nexudus.Coworking.Core.Enums.eFloorPlanItemType.Office,
        "Size": 00001,
        "Capacity": 00001,
        "Price": 00001,
        "Area": "00001",
        "Notes": "00001",
        "Available": true,
        "PositionX": 1,
        "PositionY": 1,
        "PositionZ": 1,
        "TunnelPrivateGroupId": "",
        "CoworkerContractIds": "",
        "CoworkerContractFullNames": "",
        "CoworkerContractStartDates": "",
    }],
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `floorplandesk-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of floorplandesks based on a range of dates, integer or decimal properties.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="CreatedOn" type="object" required=false %}
?to\_FloorPlanDesk\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_FloorPlanDesk\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_FloorPlanDesk\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_FloorPlanDesk\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Size" type="decimal" required=false %}
?from\_FloorPlanDesk\_Size=...
{% endapi-method-parameter %}

{% api-method-parameter name="Size" type="decimal" required=false %}
?to\_FloorPlanDesk\_Size=...
{% endapi-method-parameter %}

{% api-method-parameter name="Capacity" type="decimal" required=false %}
?from\_FloorPlanDesk\_Capacity=...
{% endapi-method-parameter %}

{% api-method-parameter name="Capacity" type="decimal" required=false %}
?to\_FloorPlanDesk\_Capacity=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=false %}
?from\_FloorPlanDesk\_Price=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=false %}
?to\_FloorPlanDesk\_Price=...
{% endapi-method-parameter %}

{% api-method-parameter name="PositionX" type="int" required=false %}
?from\_FloorPlanDesk\_PositionX=...
{% endapi-method-parameter %}

{% api-method-parameter name="PositionX" type="int" required=false %}
?to\_FloorPlanDesk\_PositionX=...
{% endapi-method-parameter %}

{% api-method-parameter name="PositionY" type="int" required=false %}
?from\_FloorPlanDesk\_PositionY=...
{% endapi-method-parameter %}

{% api-method-parameter name="PositionY" type="int" required=false %}
?to\_FloorPlanDesk\_PositionY=...
{% endapi-method-parameter %}

{% api-method-parameter name="PositionZ" type="int" required=false %}
?from\_FloorPlanDesk\_PositionZ=...
{% endapi-method-parameter %}

{% api-method-parameter name="PositionZ" type="int" required=false %}
?to\_FloorPlanDesk\_PositionZ=...
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "FloorPlan": null,
        "Coworker": null,
        "Name": "00001",
        "ItemType": Nexudus.Coworking.Core.Enums.eFloorPlanItemType.Office,
        "Size": 00001,
        "Capacity": 00001,
        "Price": 00001,
        "Area": "00001",
        "Notes": "00001",
        "Available": true,
        "PositionX": 1,
        "PositionY": 1,
        "PositionZ": 1,
        "TunnelPrivateGroupId": "",
        "CoworkerContractIds": "",
        "CoworkerContractFullNames": "",
        "CoworkerContractStartDates": "",
    }],
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `floorplandesk-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks?FloorPlanDesk\_Id=\[:id1,:id2,...\]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more floorplandesk records based on their Id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every floorplandesk to fetch. I.e. \[123456,789102,...\]
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "FloorPlan": null,
        "Coworker": null,
        "Name": "00001",
        "ItemType": Nexudus.Coworking.Core.Enums.eFloorPlanItemType.Office,
        "Size": 00001,
        "Capacity": 00001,
        "Price": 00001,
        "Area": "00001",
        "Notes": "00001",
        "Available": true,
        "PositionX": 1,
        "PositionY": 1,
        "PositionZ": 1,
        "TunnelPrivateGroupId": "",
        "CoworkerContractIds": "",
        "CoworkerContractFullNames": "",
        "CoworkerContractStartDates": "",
    }],
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
"Not found"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `floorplandesk-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one floorplandesk record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the floorplandesk to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "FloorPlan": null,
        "Coworker": null,
        "Name": "00001",
        "ItemType": Nexudus.Coworking.Core.Enums.eFloorPlanItemType.Office,
        "Size": 00001,
        "Capacity": 00001,
        "Price": 00001,
        "Area": "00001",
        "Notes": "00001",
        "Available": true,
        "PositionX": 1,
        "PositionY": 1,
        "PositionZ": 1,
        "TunnelPrivateGroupId": "",
        "CoworkerContractIds": "",
        "CoworkerContractFullNames": "",
        "CoworkerContractStartDates": "",
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
"Not found"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `floorplandesk-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new floorplandesk.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="FloorPlanId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Name" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="ItemType" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Size" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Capacity" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Area" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Available" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PositionX" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="PositionY" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="PositionZ" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="TunnelPrivateGroupId" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerContractIds" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerContractFullNames" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerContractStartDates" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 200,
    "WasSuccessful": true,
    "Message": "Record 'Name of the record' has been succesfully created.",
    "Value": {
        "Id": 12354678,
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
_This response is an example, errors and messages will follow this structure but keys and descriptions may be different for each record._
{% endapi-method-response-example-description %}

```javascript
{
    "Status": 500,
    "Message": "Email: may not be null or empty",
    "Value": null,
    "WasSuccessful": false,
    "Errors": [
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "FullName"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "Email"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "Country"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "SimpleTimeZone"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Message": "An error has occurred."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `floorplandesk-create`

```javascript
{
    "FloorPlan": 12345678,
    "Coworker": 12345678,
    "Name": "00001",
    "ItemType": 1 (check Enumerated values section below),
    "Size": 00001,
    "Capacity": 00001,
    "Price": 00001,
    "Area": "00001",
    "Notes": "00001",
    "Available": true,
    "PositionX": 1,
    "PositionY": 1,
    "PositionZ": 1,
    "TunnelPrivateGroupId": "",
    "CoworkerContractIds": "",
    "CoworkerContractFullNames": "",
    "CoworkerContractStartDates": "",
}
```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing floorplandesk.Required User Role: `floorplandesk-edit`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="FloorPlanId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Name" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="ItemType" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Size" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Capacity" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Area" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Available" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PositionX" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="PositionY" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="PositionZ" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="TunnelPrivateGroupId" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerContractIds" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerContractFullNames" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerContractStartDates" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 200,
    "WasSuccessful": true,
    "Message": "The record 'name of the record' was updated successfully,
    "Value": {
        "Id": 123456
    },
    "OpenInDialog": false,
    "Errors": null
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
_This response is an example, errors and messages will follow this structure but keys and descriptions may be different for each record._
{% endapi-method-response-example-description %}

```javascript
{
    "Status": 500,
    "Message": "Email: may not be null or empty",
    "Value": null,
    "WasSuccessful": false,
    "Errors": [
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "FullName"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "Email"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "Country"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "SimpleTimeZone"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Message": "An error has occurred."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `floorplandesk-edit`

```javascript
{
    "FloorPlan": 12345678,
    "Coworker": 12345678,
    "Name": "00001",
    "ItemType": 1 (check Enumerated values section below),
    "Size": 00001,
    "Capacity": 00001,
    "Price": 00001,
    "Area": "00001",
    "Notes": "00001",
    "Available": true,
    "PositionX": 1,
    "PositionY": 1,
    "PositionZ": 1,
    "TunnelPrivateGroupId": "",
    "CoworkerContractIds": "",
    "CoworkerContractFullNames": "",
    "CoworkerContractStartDates": "",
}
```

{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a floorplandesk.Required User Roles: `floorplandesk-delete`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Id" type="integer" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 200,
    "WasSuccessful": true,
    "Message": "The record was deleted successfully.",
    "Value": null,
    "OpenInDialog": false,
    "RedirectURL": null,
    "JavaScript": null,
    "Errors": null
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
"Not found"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Message": "An error has occurred."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `floorplandesk-delete`

## Commands

Commands allow to perform actions against one or more floorplandesk records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for floorplandesk records.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
_This response is an example._
{% endapi-method-response-example-description %}

```javascript
[
    {
        "Key": "COMMAND_KEY_1",
        "Name": "Command English Description",
        "AppliesOnlyToMultipleEntities": false,
        "AppliesOnlyToOneEntity": false,
        "AppliesOnlyToTwoEntities": false,
        "NeedsEntitiesToRun": true,
        "Order": 1,
        "RequiresParameters": []
    },
    {
        "Key": "COMMAND_KEY_2",
        "Name": "Command 2 English Description",
        "AppliesOnlyToMultipleEntities": true
        "AppliesOnlyToOneEntity": false,
        "AppliesOnlyToTwoEntities": false,
        "NeedsEntitiesToRun": true,
        "Order": 2,
        "RequiresParameters": []
    },
    ...
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/floorplandesks/runcommand" %}
{% api-method-summary %}
Run Command
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="Key" type="string" required=true %}
The command Key defining the command to run. `"COMMAND_KEY_1"`
{% endapi-method-parameter %}

{% api-method-parameter name="Parameters" type="array" required=false %}
A list of object with the structure below. The parameters required for each command are returned in the "RequiresParameters" array return by the "commands" endpoint.`[    
{    
"Name": "Name",    
"Type":"Type",    
"Value":recordId    
}    
]`
{% endapi-method-parameter %}

{% api-method-parameter name="Ids" type="array" required=true %}
A list of integer IDs for each of the records to run this command for.`[987654321, 123565978]`
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
_Commands also return a status 200 when they fail to process one or more of the records. Use the 'WasSuccessful' property to know if the command run succeeded._
{% endapi-method-response-example-description %}

```javascript
{  
   "Status":500 or 200,
   "Message":"Command error description",
   "Value":null,
   "Errors":null,
   "WasSuccessful":false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `floorplandesk-edit`

## Enumerated values

### ItemType:

> GET /api/utils/enums?name=eFloorPlanItemType

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

## Related Entities

* [FloorPlan](floorplan.md)
* [Coworker](../spaces/coworker.md)

