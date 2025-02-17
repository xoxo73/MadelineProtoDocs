---
title: "bots.getBotInfo"
description: "Get localized name, about text and description of a bot (or of the current account, if called by a bot)."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/bots_getBotInfo.html
---
# Method: bots.getBotInfo
[Back to methods index](index.html)



Get localized name, about text and description of a bot (or of the current account, if called by a bot).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|bot|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | If called by a user, **must** contain the peer of a bot we own. | Optional|
|lang\_code|[string](/API_docs/types/string.html) | Language code, if left empty this method will return the fallback about text and description. | Yes|


### Return type: [bots.BotInfo](/API_docs/types/bots.BotInfo.html)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$bots_BotInfo = $MadelineProto->bots->getBotInfo(bot: InputUser, lang_code: 'string', );
```

