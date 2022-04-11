# Chat Shown

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Chat Shown",
    "chat": {
        "isProactive": <isProactive>,
        "isReactive": <isReactive>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|chat.isProactive|boolean|Indicates whether a chat was offered proactively \(i.e. based on a behavioral rule or algorithm\)|true, false|||||||
|chat.isReactive|boolean|Indicates whether a chat was offered in response to a user request \(i.e. user clicked the chat button\)|true, false|||||||




