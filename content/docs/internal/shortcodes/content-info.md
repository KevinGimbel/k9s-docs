---
title: "content-info"
---

A note-like container providing additional context or important information.

## Parameters 

|Param|Description|
|-----|-----------|
|`title`|The title to put infront of the text. Can be empty.|
|`color`|A color variation. Currently supports `error`, `warning` or `info`.|
## Examples


{{< content-info title="Info" color="info" >}}
This is a content-info block wiht "info" colors.
{{< /content-info >}}

{{< content-info title="Warning" color="warning" >}}
This is a content-info block wiht "warning" colors.
{{< /content-info >}}

{{< content-info title="Error" color="error" >}}
This is a content-info block wiht "error" colors.
{{< /content-info >}}