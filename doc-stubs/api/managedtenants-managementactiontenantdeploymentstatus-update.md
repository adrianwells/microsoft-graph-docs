---
title: "Update managementActionTenantDeploymentStatus"
description: "Update the properties of a managementActionTenantDeploymentStatus object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update managementActionTenantDeploymentStatus
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md) object.

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
PATCH /tenantRelationships/managedTenants/managementActionTenantDeploymentStatuses/{managementActionTenantDeploymentStatusId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md) object.

The following table shows the properties that are required when you update the [managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md)|
|tenantGroupId|String|**TODO: Add Description**|
|tenantId|String|**TODO: Add Description**|
|statuses|[microsoft.graph.managedTenants.managementActionDeploymentStatus](../resources/managedtenants-managementactiondeploymentstatus.md) collection|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_managementactiontenantdeploymentstatus"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managementActionTenantDeploymentStatuses/{managementActionTenantDeploymentStatusId}
Content-Type: application/json
Content-length: 275

{
  "@odata.type": "#microsoft.graph.managedTenants.managementActionTenantDeploymentStatus",
  "tenantGroupId": "String",
  "tenantId": "String",
  "statuses": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managementActionDeploymentStatus"
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
  "@odata.type": "#microsoft.graph.managedTenants.managementActionTenantDeploymentStatus",
  "id": "d1fd96a1-96a1-d1fd-a196-fdd1a196fdd1",
  "tenantGroupId": "String",
  "tenantId": "String",
  "statuses": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managementActionDeploymentStatus"
    }
  ]
}
```

