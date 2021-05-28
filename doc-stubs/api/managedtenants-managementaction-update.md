---
title: "Update managementAction"
description: "Update the properties of a managementAction object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update managementAction
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [managementAction](../resources/managedtenants-managementaction.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /tenantRelationships/managedTenants/managementActions/{managementActionId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [managementAction](../resources/managedtenants-managementaction.md) object.

The following table shows the properties that are required when you update the [managementAction](../resources/managedtenants-managementaction.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md)|
|referenceTemplateId|String|**TODO: Add Description**|
|referenceTemplateVersion|Int32|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|description|String|**TODO: Add Description**|
|category|managementCategory|**TODO: Add Description**. Possible values are: `devices`, `identity`, `custom`, `unknownFutureValue`.|
|workloadActions|[microsoft.graph.managedTenants.workloadAction](../resources/managedtenants-workloadaction.md) collection|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [managementAction](../resources/managedtenants-managementaction.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_managementaction"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managementActions/{managementActionId}
Content-Type: application/json
Content-length: 346

{
  "@odata.type": "#microsoft.graph.managedTenants.managementAction",
  "referenceTemplateId": "String",
  "referenceTemplateVersion": "Integer",
  "displayName": "String",
  "description": "String",
  "category": "String",
  "workloadActions": [
    {
      "@odata.type": "microsoft.graph.managedTenants.workloadAction"
    }
  ]
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.managedTenants.managementAction",
  "id": "e96139fd-39fd-e961-fd39-61e9fd3961e9",
  "referenceTemplateId": "String",
  "referenceTemplateVersion": "Integer",
  "displayName": "String",
  "description": "String",
  "category": "String",
  "workloadActions": [
    {
      "@odata.type": "microsoft.graph.managedTenants.workloadAction"
    }
  ]
}
```

