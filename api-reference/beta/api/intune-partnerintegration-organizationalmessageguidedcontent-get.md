---
title: "Get organizationalMessageGuidedContent"
description: "Read properties and relationships of the organizationalMessageGuidedContent object."
author: "dougeby"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Get organizationalMessageGuidedContent

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Read properties and relationships of the [organizationalMessageGuidedContent](../resources/intune-partnerintegration-organizationalmessageguidedcontent.md) object.

## Prerequisites
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|DeviceManagementConfiguration.Read.All, DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementApps.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|DeviceManagementConfiguration.Read.All, DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementApps.ReadWrite.All|

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/organizationalMessageGuidedContents/{organizationalMessageGuidedContentId}
```

## Optional query parameters
This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and [organizationalMessageGuidedContent](../resources/intune-partnerintegration-organizationalmessageguidedcontent.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/organizationalMessageGuidedContents/{organizationalMessageGuidedContentId}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1557

{
  "value": {
    "@odata.type": "#microsoft.graph.organizationalMessageGuidedContent",
    "id": "13e64843-4843-13e6-4348-e6134348e613",
    "scenario": "lifecycle",
    "theme": "training",
    "surface": "getStarted",
    "placementDetails": [
      {
        "@odata.type": "microsoft.graph.organizationalMessagePlacementDetail",
        "placement": "card0",
        "variants": [
          {
            "@odata.type": "microsoft.graph.organizationalMessageVariant",
            "variantId": "Variant Id value",
            "name": "Name value",
            "localizedTexts": [
              {
                "@odata.type": "microsoft.graph.organizationalMessageLocalizedText",
                "locale": "Locale value",
                "text": {
                  "@odata.type": "microsoft.graph.organizationalMessageText",
                  "title": "Title value",
                  "message": "Message value",
                  "clickUrl": "https://example.com/clickUrl/",
                  "buttonText": "Button Text value"
                }
              }
            ]
          }
        ]
      }
    ],
    "logo": {
      "@odata.type": "microsoft.graph.organizationalMessageLogoGuide",
      "logoCdnUrl": "https://example.com/logoCdnUrl/",
      "assetName": "Asset Name value",
      "dimensions": {
        "@odata.type": "microsoft.graph.organizationalMessageLogoDimensions",
        "minWidth": 8,
        "maxWidth": 8,
        "minHeight": 9,
        "maxHeight": 9
      }
    }
  }
}
```





