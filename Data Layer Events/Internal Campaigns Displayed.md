# Internal Campaigns Displayed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Internal Campaigns Displayed",
    "internalCampaign": {
        "campaignList": [
            {
                "internalCampaignID": "<internalCampaignID>",
                "internalCampaignPosition": <internalCampaignPosition>
            }
        ]
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|internalCampaign.campaignList[n].internalCampaignID|string|Unique Identifier of an internal campaign|2345, 56789, 9876|||||||
|internalCampaign.campaignList[n].internalCampaignPosition|integer|The position of a internal campaign offering within a list of internal campaigns|1, 5, 78, 3||||1|||




