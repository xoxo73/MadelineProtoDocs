---
title: "danog\\MadelineProto\\EventHandler: Event handler."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\EventHandler`
[Back to index](../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Event handler.  




## Method list:
* [`startAndLoop(string $session, \danog\MadelineProto\SettingsAbstract $settings): void`](#startandloop-string-session-danog-madelineproto-settingsabstract-settings-void)
* [`startAndLoopBot(string $session, string $token, \danog\MadelineProto\SettingsAbstract $settings): void`](#startandloopbot-string-session-string-token-danog-madelineproto-settingsabstract-settings-void)
* [`getReportPeers(): string|int|(string|int)[]`](#getreportpeers-string-int-string-int-)
* [`MTProtoToBotAPI(array $data): array`](#mtprototobotapi-array-data-array)
* [`MTProtoToTd(mixed $params): mixed`](#mtprotototd-mixed-params-mixed)
* [`MTProtoToTdcli(mixed $params): mixed`](#mtprotototdcli-mixed-params-mixed)
* [`acceptCall(array $call): bool`](#acceptcall-array-call-bool)
* [`acceptSecretChat(array $params): void`](#acceptsecretchat-array-params-void)
* [`arr(mixed $params): array`](#arr-mixed-params-array)
* [`base64urlDecode(string $data): string`](#base64urldecode-string-data-string)
* [`base64urlEncode(string $data): string`](#base64urlencode-string-data-string)
* [`botAPIToMTProto(array $arguments): array`](#botapitomtproto-array-arguments-array)
* [`botLogin(string $token): ?array`](#botlogin-string-token-array)
* [`broadcastCustom(\Action $action, ?\danog\MadelineProto\Broadcast\Filter $filter): int`](#broadcastcustom-action-action-danog-madelineproto-broadcast-filter-filter-int)
* [`broadcastForwardMessages(mixed $from_peer, list<int> $message_ids, bool $drop_author, ?\danog\MadelineProto\Broadcast\Filter $filter): int`](#broadcastforwardmessages-mixed-from_peer-list-int-message_ids-bool-drop_author-danog-madelineproto-broadcast-filter-filter-int)
* [`broadcastMessages(array $messages, ?\danog\MadelineProto\Broadcast\Filter $filter): int`](#broadcastmessages-array-messages-danog-madelineproto-broadcast-filter-filter-int)
* [`callStatus(int $id): int`](#callstatus-int-id-int)
* [`cancelBroadcast(int $id): void`](#cancelbroadcast-int-id-void)
* [`closeConnection(string $message): void`](#closeconnection-string-message-void)
* [`complete2faLogin(string $password): array`](#complete2falogin-string-password-array)
* [`completeCall(array $params): mixed`](#completecall-array-params-mixed)
* [`completePhoneLogin(string $code): mixed`](#completephonelogin-string-code-mixed)
* [`completeSignup(string $first_name, string $last_name): array`](#completesignup-string-first_name-string-last_name-array)
* [`confirmCall(array $params): mixed`](#confirmcall-array-params-mixed)
* [`discardCall(array $call, array $rating, bool $need_debug, array $reason): ?\danog\MadelineProto\VoIP`](#discardcall-array-call-array-rating-bool-need_debug-array-reason-danog-madelineproto-voip)
* [`discardSecretChat(int $chat): void`](#discardsecretchat-int-chat-void)
* [`downloadToBrowser(array|string|\danog\MadelineProto\FileCallbackInterface $messageMedia, null|callable $cb, null|int $size, null|string $mime, null|string $name): void`](#downloadtobrowser-array-string-danog-madelineproto-filecallbackinterface-messagemedia-null-callable-cb-null-int-size-null-string-mime-null-string-name-void)
* [`downloadToCallable(mixed $messageMedia, callable|\danog\MadelineProto\FileCallbackInterface $callable, callable $cb, bool $seekable, int $offset, int $end, int $part_size): mixed`](#downloadtocallable-mixed-messagemedia-callable-danog-madelineproto-filecallbackinterface-callable-callable-cb-bool-seekable-int-offset-int-end-int-part_size-mixed)
* [`downloadToDir(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $dir, callable $cb): mixed`](#downloadtodir-mixed-messagemedia-string-danog-madelineproto-filecallbackinterface-dir-callable-cb-mixed)
* [`downloadToFile(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $file, callable $cb): string|false`](#downloadtofile-mixed-messagemedia-string-danog-madelineproto-filecallbackinterface-file-callable-cb-string-false)
* [`downloadToResponse(array|string|\danog\MadelineProto\FileCallbackInterface $messageMedia, \Amp\Http\Server\Request $request, callable $cb, null|int $size, null|string $name, null|string $mime): \Amp\Http\Server\Response`](#downloadtoresponse-array-string-danog-madelineproto-filecallbackinterface-messagemedia-amp-http-server-request-request-callable-cb-null-int-size-null-string-name-null-string-mime-amp-http-server-response)
* [`downloadToStream(mixed $messageMedia, mixed|\danog\MadelineProto\FileCallbackInterface|\resource|\Amp\ByteStream\WritableStream $stream, callable $cb, int $offset, int $end): mixed`](#downloadtostream-mixed-messagemedia-mixed-danog-madelineproto-filecallbackinterface-resource-amp-bytestream-writablestream-stream-callable-cb-int-offset-int-end-mixed)
* [`echo(string $string): void`](#echo-string-string-void)
* [`end(array $what): mixed`](#end-array-what-mixed)
* [`exportAuthorization(): array{0: int|string, 1: string}`](#exportauthorization-array-0-int-string-1-string-)
* [`extractBotAPIFile(array $info): ?array`](#extractbotapifile-array-info-array)
* [`extractMessage(array $updates): array`](#extractmessage-array-updates-array)
* [`extractMessageId(array $updates): int`](#extractmessageid-array-updates-int)
* [`extractMessageUpdate(array $updates): array`](#extractmessageupdate-array-updates-array)
* [`extractUpdates(array $updates): array[]`](#extractupdates-array-updates-array-)
* [`fileGetContents(string $url): string`](#filegetcontents-string-url-string)
* [`flock(string $file, int $operation, float $polling, ?\Amp\Cancellation $token, ?\Closure $failureCb): mixed`](#flock-string-file-int-operation-float-polling-amp-cancellation-token-closure-failurecb-mixed)
* [`fromSupergroup(int $id): int`](#fromsupergroup-int-id-int)
* [`fullChatLastUpdated(mixed $id): int`](#fullchatlastupdated-mixed-id-int)
* [`fullGetSelf(): array|false`](#fullgetself-array-false)
* [`genVectorHash(array $ints): string`](#genvectorhash-array-ints-string)
* [`getAllMethods(): array`](#getallmethods-array)
* [`getAuthorization(): \danog\MadelineProto\API::NOT_LOGGED_IN|\danog\MadelineProto\API::WAITING_CODE|\danog\MadelineProto\API::WAITING_SIGNUP|\danog\MadelineProto\API::WAITING_PASSWORD|\danog\MadelineProto\API::LOGGED_IN`](#getauthorization-danog-madelineproto-api-not_logged_in-danog-madelineproto-api-waiting_code-danog-madelineproto-api-waiting_signup-danog-madelineproto-api-waiting_password-danog-madelineproto-api-logged_in)
* [`getBroadcastProgress(int $id): ?\danog\MadelineProto\Broadcast\Progress`](#getbroadcastprogress-int-id-danog-madelineproto-broadcast-progress)
* [`getCachedConfig(): array`](#getcachedconfig-array)
* [`getCall(int $call): array`](#getcall-int-call-array)
* [`getCdnConfig(): void`](#getcdnconfig-void)
* [`getConfig(array $config): array`](#getconfig-array-config-array)
* [`getDNSClient(): \Amp\Dns\DnsResolver`](#getdnsclient-amp-dns-dnsresolver)
* [`getDhConfig(): array`](#getdhconfig-array)
* [`getDialogIds(): list<int>`](#getdialogids-list-int-)
* [`getDialogs(): list<array>`](#getdialogs-list-array-)
* [`getDownloadInfo(mixed $messageMedia): array`](#getdownloadinfo-mixed-messagemedia-array)
* [`getEventHandler(): \danog\MadelineProto\EventHandler|\__PHP_Incomplete_Class|null`](#geteventhandler-danog-madelineproto-eventhandler-__php_incomplete_class-null)
* [`getExtensionFromLocation(mixed $location, string $default): string`](#getextensionfromlocation-mixed-location-string-default-string)
* [`getExtensionFromMime(string $mime): string`](#getextensionfrommime-string-mime-string)
* [`getFileInfo(mixed $constructor): array`](#getfileinfo-mixed-constructor-array)
* [`getFolderId(mixed $id): ?int`](#getfolderid-mixed-id-int)
* [`getFullDialogs(): array<int, array>`](#getfulldialogs-array-int-array-)
* [`getFullInfo(mixed $id): array`](#getfullinfo-mixed-id-array)
* [`getHTTPClient(): \Amp\Http\Client\HttpClient`](#gethttpclient-amp-http-client-httpclient)
* [`getHint(): string`](#gethint-string)
* [`getId(mixed $id): int`](#getid-mixed-id-int)
* [`getInfo(mixed $id, \MTProto::INFO_TYPE_* $type): mixed`](#getinfo-mixed-id-mtproto-info_type_-type-mixed)
* [`getLogger(): \danog\MadelineProto\Logger`](#getlogger-danog-madelineproto-logger)
* [`getMaps(): ?int`](#getmaps-int)
* [`getMaxMaps(): ?int`](#getmaxmaps-int)
* [`getMethodNamespaces(): array`](#getmethodnamespaces-array)
* [`getMethodsNamespaced(): array`](#getmethodsnamespaced-array)
* [`getMimeFromBuffer(string $buffer): string`](#getmimefrombuffer-string-buffer-string)
* [`getMimeFromExtension(string $extension, string $default): string`](#getmimefromextension-string-extension-string-default-string)
* [`getMimeFromFile(string $file): string`](#getmimefromfile-string-file-string)
* [`getPropicInfo(mixed $data): array`](#getpropicinfo-mixed-data-array)
* [`getPsrLogger(): \Psr\Log\LoggerInterface`](#getpsrlogger-psr-log-loggerinterface)
* [`getPwrChat(mixed $id, bool $fullfetch): array`](#getpwrchat-mixed-id-bool-fullfetch-array)
* [`getSecretChat(array|int $chat): array`](#getsecretchat-array-int-chat-array)
* [`getSelf(): array|false`](#getself-array-false)
* [`getSessionName(): string`](#getsessionname-string)
* [`getSettings(): \danog\MadelineProto\Settings`](#getsettings-danog-madelineproto-settings)
* [`getSponsoredMessages(int|string|array $peer): ?array`](#getsponsoredmessages-int-string-array-peer-array)
* [`getTL(): \danog\MadelineProto\TL\TL`](#gettl-danog-madelineproto-tl-tl)
* [`getType(mixed $id): \"user"|\"bot"|\"chat"|\"supergroup"|\"channel"`](#gettype-mixed-id-user-bot-chat-supergroup-channel-)
* [`getUpdates(array{offset?: int, limit?: int, timeout?: float} $params): list<array{update_id: mixed, update: mixed}>`](#getupdates-array-offset-int-limit-int-timeout-float-params-list-array-update_id-mixed-update-mixed-)
* [`getWebMessage(string $message): string`](#getwebmessage-string-message-string)
* [`hasEventHandler(): bool`](#haseventhandler-bool)
* [`hasReportPeers(): bool`](#hasreportpeers-bool)
* [`hasSecretChat(array|int $chat): bool`](#hassecretchat-array-int-chat-bool)
* [`importAuthorization(array<int, string> $authorization, int $mainDcID): array`](#importauthorization-array-int-string-authorization-int-maindcid-array)
* [`inflateStripped(string $stripped): string`](#inflatestripped-string-stripped-string)
* [`initSelfRestart(): void`](#initselfrestart-void)
* [`isAltervista(): bool`](#isaltervista-bool)
* [`isArrayOrAlike(mixed $var): bool`](#isarrayoralike-mixed-var-bool)
* [`isIpc(): bool`](#isipc-bool)
* [`isIpcWorker(): bool`](#isipcworker-bool)
* [`isPremium(): bool`](#ispremium-bool)
* [`isSupergroup(int $id): bool`](#issupergroup-int-id-bool)
* [`logger(mixed $param, int $level, string $file): void`](#logger-mixed-param-int-level-string-file-void)
* [`mbStrSplit(string $text, int $length): string[]`](#mbstrsplit-string-text-int-length-string-)
* [`mbStrlen(string $text): int`](#mbstrlen-string-text-int)
* [`mbSubstr(string $text, int $offset, null|int $length): string`](#mbsubstr-string-text-int-offset-null-int-length-string)
* [`packDouble(float $value): string`](#packdouble-float-value-string)
* [`packSignedInt(int $value): string`](#packsignedint-int-value-string)
* [`packSignedLong(int $value): string`](#packsignedlong-int-value-string)
* [`packUnsignedInt(int $value): string`](#packunsignedint-int-value-string)
* [`peerIsset(mixed $id): bool`](#peerisset-mixed-id-bool)
* [`phoneLogin(string $number, int $sms_type): mixed`](#phonelogin-string-number-int-sms_type-mixed)
* [`posmod(int $a, int $b): int`](#posmod-int-a-int-b-int)
* [`qrLogin(): ?\danog\MadelineProto\TL\Types\LoginQrCode`](#qrlogin-danog-madelineproto-tl-types-loginqrcode)
* [`random(int $length): string`](#random-int-length-string)
* [`randomInt(int $modulus): int`](#randomint-int-modulus-int)
* [`readLine(string $prompt, ?\Amp\Cancellation $cancel): string`](#readline-string-prompt-amp-cancellation-cancel-string)
* [`refreshFullPeerCache(mixed $id): void`](#refreshfullpeercache-mixed-id-void)
* [`refreshPeerCache(mixed $ids): void`](#refreshpeercache-mixed-ids-void)
* [`rekey(int $chat): ?string`](#rekey-int-chat-string)
* [`report(string $message, string $parseMode): void`](#report-string-message-string-parsemode-void)
* [`requestCall(mixed $user): mixed`](#requestcall-mixed-user-mixed)
* [`requestSecretChat(mixed $user): mixed`](#requestsecretchat-mixed-user-mixed)
* [`resetUpdateState(): void`](#resetupdatestate-void)
* [`restart(): void`](#restart-void)
* [`rethrow(\Throwable $e): void`](#rethrow-throwable-e-void)
* [`rleDecode(string $string): string`](#rledecode-string-string-string)
* [`rleEncode(string $string): string`](#rleencode-string-string-string)
* [`secretChatStatus(int $chat): \int One of MTProto::SECRET_EMPTY, MTProto::SECRET_REQUESTED, MTProto::SECRET_READY`](#secretchatstatus-int-chat-int-one-of-mtproto-secret_empty-mtproto-secret_requested-mtproto-secret_ready)
* [`sendCustomEvent(mixed $payload): void`](#sendcustomevent-mixed-payload-void)
* [`setNoop(): void`](#setnoop-void)
* [`setReportPeers(int|string|(int|string)[] $userOrId): void`](#setreportpeers-int-string-int-string-userorid-void)
* [`setWebhook(string $webhookUrl): void`](#setwebhook-string-webhookurl-void)
* [`setupLogger(): void`](#setuplogger-void)
* [`sleep(float $time): void`](#sleep-float-time-void)
* [`start(): mixed`](#start-mixed)
* [`stop(): void`](#stop-void)
* [`subscribeToUpdates(mixed $channel): \bool False if we were already subscribed`](#subscribetoupdates-mixed-channel-bool-false-if-we-were-already-subscribed)
* [`tdToMTProto(array $params): array`](#tdtomtproto-array-params-array)
* [`tdToTdcli(mixed $params): mixed`](#tdtotdcli-mixed-params-mixed)
* [`tdcliToTd(mixed $params, array $key): array`](#tdclitotd-mixed-params-array-key-array)
* [`testFibers(int $fiberCount): array{maxFibers: int, realMemoryMb: int, maps: ?int, maxMaps: ?int}`](#testfibers-int-fibercount-array-maxfibers-int-realmemorymb-int-maps-int-maxmaps-int-)
* [`toCamelCase(string $input): string`](#tocamelcase-string-input-string)
* [`toSnakeCase(string $input): string`](#tosnakecase-string-input-string)
* [`toSupergroup(int $id): int`](#tosupergroup-int-id-int)
* [`unpackDouble(string $value): float`](#unpackdouble-string-value-float)
* [`unpackFileId(string $fileId): \array Unpacked file ID`](#unpackfileid-string-fileid-array-unpacked-file-id)
* [`unpackSignedInt(string $value): int`](#unpacksignedint-string-value-int)
* [`unpackSignedLong(string $value): int`](#unpacksignedlong-string-value-int)
* [`unpackSignedLongString(string|int|array $value): string`](#unpacksignedlongstring-string-int-array-value-string)
* [`unsetEventHandler(): void`](#unseteventhandler-void)
* [`update2fa(array{password?: string, new_password?: string, email?: string, hint?: string} $params): void`](#update2fa-array-password-string-new_password-string-email-string-hint-string-params-void)
* [`updateSettings(\danog\MadelineProto\SettingsAbstract $settings): void`](#updatesettings-danog-madelineproto-settingsabstract-settings-void)
* [`upload(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb, bool $encrypted): mixed`](#upload-danog-madelineproto-filecallbackinterface-string-array-file-string-filename-callable-cb-bool-encrypted-mixed)
* [`uploadEncrypted(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb): mixed`](#uploadencrypted-danog-madelineproto-filecallbackinterface-string-array-file-string-filename-callable-cb-mixed)
* [`uploadFromCallable(mixed $callable, int $size, string $mime, string $fileName, callable $cb, bool $seekable, bool $encrypted): mixed`](#uploadfromcallable-mixed-callable-int-size-string-mime-string-filename-callable-cb-bool-seekable-bool-encrypted-mixed)
* [`uploadFromStream(mixed $stream, int $size, string $mime, string $fileName, callable $cb, bool $encrypted): mixed`](#uploadfromstream-mixed-stream-int-size-string-mime-string-filename-callable-cb-bool-encrypted-mixed)
* [`uploadFromTgfile(mixed $media, callable $cb, bool $encrypted): mixed`](#uploadfromtgfile-mixed-media-callable-cb-bool-encrypted-mixed)
* [`uploadFromUrl(string|\danog\MadelineProto\FileCallbackInterface $url, int $size, string $fileName, callable $cb, bool $encrypted): mixed`](#uploadfromurl-string-danog-madelineproto-filecallbackinterface-url-int-size-string-filename-callable-cb-bool-encrypted-mixed)
* [`viewSponsoredMessage(int|array $peer, string|array{random_id: string} $message): bool`](#viewsponsoredmessage-int-array-peer-string-array-random_id-string-message-bool)

## Methods:
### `startAndLoop(string $session, \danog\MadelineProto\SettingsAbstract $settings): void`

Start MadelineProto and the event handler.
Also initializes error reporting, catching and reporting all errors surfacing from the event loop.

Parameters:

* `$session`: `string` Session name  
* `$settings`: `\danog\MadelineProto\SettingsAbstract` Settings  


#### See also: 
* `\danog\MadelineProto\SettingsAbstract`




### `startAndLoopBot(string $session, string $token, \danog\MadelineProto\SettingsAbstract $settings): void`

Start MadelineProto as a bot and the event handler.
Also initializes error reporting, catching and reporting all errors surfacing from the event loop.

Parameters:

* `$session`: `string` Session name  
* `$token`: `string` Bot token  
* `$settings`: `\danog\MadelineProto\SettingsAbstract` Settings  


#### See also: 
* `\danog\MadelineProto\SettingsAbstract`




### `getReportPeers(): string|int|(string|int)[]`

Get peers where to send error reports.



### `MTProtoToBotAPI(array $data): array`

Convert MTProto parameters to bot API parameters.


Parameters:

* `$data`: `array` Data  



### `MTProtoToTd(mixed $params): mixed`

MTProto to TD params.


Parameters:

* `$params`: `mixed` Params  



### `MTProtoToTdcli(mixed $params): mixed`

MTProto to TDCLI params.


Parameters:

* `$params`: `mixed` Params  



### `acceptCall(array $call): bool`

Accept call.


Parameters:

* `$call`: `array` Call  



### `acceptSecretChat(array $params): void`

Accept secret chat.


Parameters:

* `$params`: `array` Secret chat ID  



### `arr(mixed $params): array`

Create array.


Parameters:

* `$params`: `mixed` Params  



### `base64urlDecode(string $data): string`

base64URL decode.


Parameters:

* `$data`: `string` Data to decode  



### `base64urlEncode(string $data): string`

Base64URL encode.


Parameters:

* `$data`: `string` Data to encode  



### `botAPIToMTProto(array $arguments): array`

Convert bot API parameters to MTProto parameters.


Parameters:

* `$arguments`: `array` Arguments  



### `botLogin(string $token): ?array`

Login as bot.


Parameters:

* `$token`: `string` Bot token  



### `broadcastCustom(\Action $action, ?\danog\MadelineProto\Broadcast\Filter $filter): int`

Executes a custom broadcast action with all peers (users, chats, channels) of the bot.
Will return an integer ID that can be used to:  
  
- Get the current broadcast progress with getBroadcastProgress  
- Cancel the broadcast using cancelBroadcast  
  
Note that to avoid manually polling the progress,  
MadelineProto will also periodically emit updateBroadcastProgress updates,  
containing a Progress object for all broadcasts currently in-progress.

Parameters:

* `$action`: `\Action` A custom, serializable Action class that will be called once for every peer.  
* `$filter`: `?\danog\MadelineProto\Broadcast\Filter`   


#### See also: 
* `\Action`
* [`\danog\MadelineProto\Broadcast\Filter`: Broadcast filter.](../../danog/MadelineProto/Broadcast/Filter.html)




### `broadcastForwardMessages(mixed $from_peer, list<int> $message_ids, bool $drop_author, ?\danog\MadelineProto\Broadcast\Filter $filter): int`

Forwards a list of messages to all peers (users, chats, channels) of the bot.
Will return an integer ID that can be used to:  
  
- Get the current broadcast progress with getBroadcastProgress  
- Cancel the broadcast using cancelBroadcast  
  
Note that to avoid manually polling the progress,  
MadelineProto will also periodically emit updateBroadcastProgress updates,  
containing a Progress object for all broadcasts currently in-progress.

Parameters:

* `$from_peer`: `mixed` Bot API ID or Update, from where to forward the messages.  
* `$message_ids`: `list<int>` IDs of the messages to forward.  
* `$drop_author`: `bool` If true, will forward messages without quoting the original author.  
* `$filter`: `?\danog\MadelineProto\Broadcast\Filter`   


#### See also: 
* [`\danog\MadelineProto\Broadcast\Filter`: Broadcast filter.](../../danog/MadelineProto/Broadcast/Filter.html)




### `broadcastMessages(array $messages, ?\danog\MadelineProto\Broadcast\Filter $filter): int`

Sends a list of messages to all peers (users, chats, channels) of the bot.
A simplified version of this method is also available: broadcastForwardMessages can work with pre-prepared messages.  
  
Will return an integer ID that can be used to:  
  
- Get the current broadcast progress with getBroadcastProgress  
- Cancel the broadcast using cancelBroadcast  
  
Note that to avoid manually polling the progress,  
MadelineProto will also periodically emit updateBroadcastProgress updates,  
containing a Progress object for all broadcasts currently in-progress.

Parameters:

* `$messages`: `array` The messages to send: an array of arrays, containing parameters to pass to messages.sendMessage.  
* `$filter`: `?\danog\MadelineProto\Broadcast\Filter`   


#### See also: 
* [`\danog\MadelineProto\Broadcast\Filter`: Broadcast filter.](../../danog/MadelineProto/Broadcast/Filter.html)




### `callStatus(int $id): int`

Get call status.


Parameters:

* `$id`: `int` Call ID  



### `cancelBroadcast(int $id): void`

Cancel a running broadcast.


Parameters:

* `$id`: `int` Broadcast ID  



### `closeConnection(string $message): void`

Close connection with client, connected via web.


Parameters:

* `$message`: `string` Message  



### `complete2faLogin(string $password): array`

Complete 2FA login.


Parameters:

* `$password`: `string` Password  



### `completeCall(array $params): mixed`

Complete call handshake.


Parameters:

* `$params`: `array` Params  



### `completePhoneLogin(string $code): mixed`

Complet user login using login code.


Parameters:

* `$code`: `string` Login code  



### `completeSignup(string $first_name, string $last_name): array`

Complete signup to Telegram.


Parameters:

* `$first_name`: `string` First name  
* `$last_name`: `string` Last name  



### `confirmCall(array $params): mixed`

Confirm call.


Parameters:

* `$params`: `array` Params  



### `discardCall(array $call, array $rating, bool $need_debug, array $reason): ?\danog\MadelineProto\VoIP`

Discard call.


Parameters:

* `$call`: `array` Call  
* `$rating`: `array` Rating  
* `$need_debug`: `bool` Need debug?  
* `$reason`: `array`   


#### See also: 
* `\danog\MadelineProto\VoIP`




### `discardSecretChat(int $chat): void`

Discard secret chat.


Parameters:

* `$chat`: `int` Secret chat ID  



### `downloadToBrowser(array|string|\danog\MadelineProto\FileCallbackInterface $messageMedia, null|callable $cb, null|int $size, null|string $mime, null|string $name): void`

Download file to browser.
Supports HEAD requests and content-ranges for parallel and resumed downloads.

Parameters:

* `$messageMedia`: `array|string|\danog\MadelineProto\FileCallbackInterface` File to download  
* `$cb`: `null|callable` Status callback (can also use FileCallback)  
* `$size`: `null|int` Size of file to download, required for bot API file IDs.  
* `$mime`: `null|string` MIME type of file to download, required for bot API file IDs.  
* `$name`: `null|string` Name of file to download, required for bot API file IDs.  


#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../danog/MadelineProto/FileCallbackInterface.html)




### `downloadToCallable(mixed $messageMedia, callable|\danog\MadelineProto\FileCallbackInterface $callable, callable $cb, bool $seekable, int $offset, int $end, int $part_size): mixed`

Download file to callable.
The callable must accept two parameters: string $payload, int $offset  
The callable will be called (possibly out of order, depending on the value of $seekable).

Parameters:

* `$messageMedia`: `mixed` File to download  
* `$callable`: `callable|\danog\MadelineProto\FileCallbackInterface` Chunk callback  
* `$cb`: `callable` Status callback (DEPRECATED, use FileCallbackInterface)  
* `$seekable`: `bool` Whether the callable can be called out of order  
* `$offset`: `int` Offset where to start downloading  
* `$end`: `int` Offset where to stop downloading (inclusive)  
* `$part_size`: `int` Size of each chunk  


#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../danog/MadelineProto/FileCallbackInterface.html)




### `downloadToDir(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $dir, callable $cb): mixed`

Download file to directory.


Parameters:

* `$messageMedia`: `mixed` File to download  
* `$dir`: `string|\danog\MadelineProto\FileCallbackInterface` Directory where to download the file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../danog/MadelineProto/FileCallbackInterface.html)




### `downloadToFile(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $file, callable $cb): string|false`

Download file.


Parameters:

* `$messageMedia`: `mixed` File to download  
* `$file`: `string|\danog\MadelineProto\FileCallbackInterface` Downloaded file path  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../danog/MadelineProto/FileCallbackInterface.html)




### `downloadToResponse(array|string|\danog\MadelineProto\FileCallbackInterface $messageMedia, \Amp\Http\Server\Request $request, callable $cb, null|int $size, null|string $name, null|string $mime): \Amp\Http\Server\Response`

Download file to amphp/http-server response.
Supports HEAD requests and content-ranges for parallel and resumed downloads.

Parameters:

* `$messageMedia`: `array|string|\danog\MadelineProto\FileCallbackInterface` File to download  
* `$request`: `\Amp\Http\Server\Request` Request  
* `$cb`: `callable` Status callback (can also use FileCallback)  
* `$size`: `null|int` Size of file to download, required for bot API file IDs.  
* `$name`: `null|string` Name of file to download, required for bot API file IDs.  
* `$mime`: `null|string` MIME type of file to download, required for bot API file IDs.  


#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../danog/MadelineProto/FileCallbackInterface.html)
* `\Amp\Http\Server\Request`
* `\Amp\Http\Server\Response`




### `downloadToStream(mixed $messageMedia, mixed|\danog\MadelineProto\FileCallbackInterface|\resource|\Amp\ByteStream\WritableStream $stream, callable $cb, int $offset, int $end): mixed`

Download file to stream.


Parameters:

* `$messageMedia`: `mixed` File to download  
* `$stream`: `mixed|\danog\MadelineProto\FileCallbackInterface|\resource|\Amp\ByteStream\WritableStream` Stream where to download file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$offset`: `int` Offset where to start downloading  
* `$end`: `int` Offset where to end download  


#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../danog/MadelineProto/FileCallbackInterface.html)
* `\resource`
* `\Amp\ByteStream\WritableStream`




### `echo(string $string): void`

Asynchronously write to stdout/browser.


Parameters:

* `$string`: `string` Message to echo  



### `end(array $what): mixed`

Get final element of array.


Parameters:

* `$what`: `array` Array  



### `exportAuthorization(): array{0: int|string, 1: string}`

Export authorization.



### `extractBotAPIFile(array $info): ?array`

Extract file info from bot API message.


Parameters:

* `$info`: `array` Bot API message object  



### `extractMessage(array $updates): array`

Extract a message constructor from an Updates constructor.


Parameters:

* `$updates`: `array`   



### `extractMessageId(array $updates): int`

Extract a message ID from an Updates constructor.


Parameters:

* `$updates`: `array`   



### `extractMessageUpdate(array $updates): array`

Extract an update message constructor from an Updates constructor.


Parameters:

* `$updates`: `array`   



### `extractUpdates(array $updates): array[]`

Extract Update constructors from an Updates constructor.


Parameters:

* `$updates`: `array`   



### `fileGetContents(string $url): string`

Get contents of remote file asynchronously.


Parameters:

* `$url`: `string` URL  



### `flock(string $file, int $operation, float $polling, ?\Amp\Cancellation $token, ?\Closure $failureCb): mixed`

Asynchronously lock a file
Resolves with a callbable that MUST eventually be called in order to release the lock.


Parameters:

* `$file`: `string` File to lock  
* `$operation`: `int` Locking mode  
* `$polling`: `float` Polling interval  
* `$token`: `?\Amp\Cancellation` Cancellation token  
* `$failureCb`: `?\Closure` Failure callback, called only once if the first locking attempt fails.  


#### See also: 
* `\Amp\Cancellation`
* `\Closure`




### `fromSupergroup(int $id): int`

Convert bot API channel ID to MTProto channel ID.


Parameters:

* `$id`: `int` Bot API channel ID  



### `fullChatLastUpdated(mixed $id): int`

When were full info for this chat last cached.


Parameters:

* `$id`: `mixed` Chat ID  



### `fullGetSelf(): array|false`

Get info about the logged-in user, not cached.



### `genVectorHash(array $ints): string`

Generate MTProto vector hash.
Returns a vector hash.

Parameters:

* `$ints`: `array` IDs  



### `getAllMethods(): array`

Get full list of MTProto and API methods.



### `getAuthorization(): \danog\MadelineProto\API::NOT_LOGGED_IN|\danog\MadelineProto\API::WAITING_CODE|\danog\MadelineProto\API::WAITING_SIGNUP|\danog\MadelineProto\API::WAITING_PASSWORD|\danog\MadelineProto\API::LOGGED_IN`

Get authorization info.


#### See also: 
* `\danog\MadelineProto\API::NOT_LOGGED_IN`
* `\danog\MadelineProto\API::WAITING_CODE`
* `\danog\MadelineProto\API::WAITING_SIGNUP`
* `\danog\MadelineProto\API::WAITING_PASSWORD`
* `\danog\MadelineProto\API::LOGGED_IN`




### `getBroadcastProgress(int $id): ?\danog\MadelineProto\Broadcast\Progress`

Get the progress of a currently running broadcast.
Will return null if the broadcast doesn't exist, has already completed or was cancelled.  
  
Use updateBroadcastProgress updates to get real-time progress status without polling.

Parameters:

* `$id`: `int` Broadcast ID  


#### See also: 
* [`\danog\MadelineProto\Broadcast\Progress`: Broadcast progress.](../../danog/MadelineProto/Broadcast/Progress.html)




### `getCachedConfig(): array`

Get cached server-side config.



### `getCall(int $call): array`

Get call info.


Parameters:

* `$call`: `int` Call ID  



### `getCdnConfig(): void`

Store RSA keys for CDN datacenters.



### `getConfig(array $config): array`

Get cached (or eventually re-fetch) server-side config.


Parameters:

* `$config`: `array` Current config  



### `getDNSClient(): \Amp\Dns\DnsResolver`

Get async DNS client.


#### See also: 
* `\Amp\Dns\DnsResolver`




### `getDhConfig(): array`

Get diffie-hellman configuration.



### `getDialogIds(): list<int>`

Get dialog IDs.



### `getDialogs(): list<array>`

Get dialog peers.



### `getDownloadInfo(mixed $messageMedia): array`

Get download info of file
Returns an array with the following structure:.
`$info['ext']` - The file extension  
`$info['name']` - The file name, without the extension  
`$info['mime']` - The file mime type  
`$info['size']` - The file size

Parameters:

* `$messageMedia`: `mixed` File ID  



### `getEventHandler(): \danog\MadelineProto\EventHandler|\__PHP_Incomplete_Class|null`

Get event handler.


#### See also: 
* [`\danog\MadelineProto\EventHandler`: Event handler.](../../danog/MadelineProto/EventHandler.html)
* `\__PHP_Incomplete_Class`




### `getExtensionFromLocation(mixed $location, string $default): string`

Get extension from file location.


Parameters:

* `$location`: `mixed` File location  
* `$default`: `string` Default extension  



### `getExtensionFromMime(string $mime): string`

Get extension from mime type.


Parameters:

* `$mime`: `string` MIME type  



### `getFileInfo(mixed $constructor): array`

Get info about file.


Parameters:

* `$constructor`: `mixed` File ID  



### `getFolderId(mixed $id): ?int`

Get folder ID from object.


Parameters:

* `$id`: `mixed` Object  



### `getFullDialogs(): array<int, array>`

Get full info of all dialogs.
Bots should use getDialogs or getDialogIds, instead.


### `getFullInfo(mixed $id): array`

Get full info about peer, returns an FullInfo object.


Parameters:

* `$id`: `mixed` Peer  


#### See also: 
* [https://docs.madelineproto.xyz/FullInfo.html](https://docs.madelineproto.xyz/FullInfo.html)




### `getHTTPClient(): \Amp\Http\Client\HttpClient`

Get async HTTP client.


#### See also: 
* `\Amp\Http\Client\HttpClient`




### `getHint(): string`

Get current password hint.



### `getId(mixed $id): int`

Get the bot API ID of a peer.


Parameters:

* `$id`: `mixed` Peer  



### `getInfo(mixed $id, \MTProto::INFO_TYPE_* $type): mixed`

Get info about peer, returns an Info object.


Parameters:

* `$id`: `mixed` Peer  
* `$type`: `\MTProto::INFO_TYPE_*` Whether to generate an Input*, an InputPeer or the full set of constructors  


#### See also: 
* [https://docs.madelineproto.xyz/Info.html](https://docs.madelineproto.xyz/Info.html)




### `getLogger(): \danog\MadelineProto\Logger`

Get logger.


#### See also: 
* [`\danog\MadelineProto\Logger`: Logger class.](../../danog/MadelineProto/Logger.html)




### `getMaps(): ?int`

Get current number of memory-mapped regions, UNIX only.



### `getMaxMaps(): ?int`

Get maximum number of memory-mapped regions, UNIX only.
Use testFibers to get the maximum number of fibers on any platform.


### `getMethodNamespaces(): array`

Get TL namespaces.



### `getMethodsNamespaced(): array`

Get namespaced methods (method => namespace).



### `getMimeFromBuffer(string $buffer): string`

Get mime type from buffer.


Parameters:

* `$buffer`: `string` Buffer  



### `getMimeFromExtension(string $extension, string $default): string`

Get mime type from file extension.


Parameters:

* `$extension`: `string` File extension  
* `$default`: `string` Default mime type  



### `getMimeFromFile(string $file): string`

Get mime type of file.


Parameters:

* `$file`: `string` File  



### `getPropicInfo(mixed $data): array`

Get download info of the propic of a user
Returns an array with the following structure:.
`$info['ext']` - The file extension  
`$info['name']` - The file name, without the extension  
`$info['mime']` - The file mime type  
`$info['size']` - The file size

Parameters:

* `$data`: `mixed`   



### `getPsrLogger(): \Psr\Log\LoggerInterface`

Get PSR logger.


#### See also: 
* `\Psr\Log\LoggerInterface`




### `getPwrChat(mixed $id, bool $fullfetch): array`

Get full info about peer (including full list of channel members), returns a Chat object.


Parameters:

* `$id`: `mixed` Peer  
* `$fullfetch`: `bool`   


#### See also: 
* [https://docs.madelineproto.xyz/Chat.html](https://docs.madelineproto.xyz/Chat.html)




### `getSecretChat(array|int $chat): array`

Get secret chat.


Parameters:

* `$chat`: `array|int` Secret chat ID  



### `getSelf(): array|false`

Get info about the logged-in user, cached.
Use fullGetSelf to bypass the cache.


### `getSessionName(): string`

Returns the session name.



### `getSettings(): \danog\MadelineProto\Settings`

Return current settings.


#### See also: 
* [`\danog\MadelineProto\Settings`: Settings class used for configuring MadelineProto.](../../danog/MadelineProto/Settings.html)




### `getSponsoredMessages(int|string|array $peer): ?array`

Get sponsored messages for channel.
This method will return an array of [sponsored message objects](https://docs.madelineproto.xyz/API_docs/constructors/sponsoredMessage.html).  
  
See [the API documentation](https://core.telegram.org/api/sponsored-messages) for more info on how to handle sponsored messages.

Parameters:

* `$peer`: `int|string|array` Channel ID, or Update, or Message, or Peer.  



### `getTL(): \danog\MadelineProto\TL\TL`

Get TL serializer.


#### See also: 
* `\danog\MadelineProto\TL\TL`




### `getType(mixed $id): \"user"|\"bot"|\"chat"|\"supergroup"|\"channel"`

Get type of peer.


Parameters:

* `$id`: `mixed` Peer  



### `getUpdates(array{offset?: int, limit?: int, timeout?: float} $params): list<array{update_id: mixed, update: mixed}>`

Get updates.


Parameters:

* `$params`: `array{offset?: int, limit?: int, timeout?: float}` Params  



### `getWebMessage(string $message): string`

Get a message to show to the user when starting the bot.


Parameters:

* `$message`: `string`   



### `hasEventHandler(): bool`

Check if an event handler instance is present.



### `hasReportPeers(): bool`

Check if has report peers.



### `hasSecretChat(array|int $chat): bool`

Check whether secret chat exists.


Parameters:

* `$chat`: `array|int` Secret chat ID  



### `importAuthorization(array<int, string> $authorization, int $mainDcID): array`

Import authorization.


Parameters:

* `$authorization`: `array<int, string>` Authorization info  
* `$mainDcID`: `int` Main DC ID  



### `inflateStripped(string $stripped): string`

Inflate stripped photosize to full JPG payload.


Parameters:

* `$stripped`: `string` Stripped photosize  



### `initSelfRestart(): void`

Initialize self-restart hack.



### `isAltervista(): bool`

Whether this is altervista.



### `isArrayOrAlike(mixed $var): bool`

Check if is array or similar (traversable && countable && arrayAccess).


Parameters:

* `$var`: `mixed` Value to check  



### `isIpc(): bool`

Whether we're an IPC client instance.



### `isIpcWorker(): bool`

Whether we're an IPC server process (as opposed to an event handler).



### `isPremium(): bool`

Returns whether the current user is a premium user, cached.



### `isSupergroup(int $id): bool`

Check whether provided bot API ID is a channel.


Parameters:

* `$id`: `int` Bot API ID  



### `logger(mixed $param, int $level, string $file): void`

Logger.


Parameters:

* `$param`: `mixed` Parameter  
* `$level`: `int` Logging level  
* `$file`: `string` File where the message originated  



### `mbStrSplit(string $text, int $length): string[]`

Telegram UTF-8 multibyte split.


Parameters:

* `$text`: `string` Text  
* `$length`: `int` Length  



### `mbStrlen(string $text): int`

Get Telegram UTF-8 length of string.


Parameters:

* `$text`: `string` Text  



### `mbSubstr(string $text, int $offset, null|int $length): string`

Telegram UTF-8 multibyte substring.


Parameters:

* `$text`: `string` Text to substring  
* `$offset`: `int` Offset  
* `$length`: `null|int` Length  



### `packDouble(float $value): string`

Convert double to binary version.


Parameters:

* `$value`: `float` Value to convert  



### `packSignedInt(int $value): string`

Convert integer to base256 signed int.


Parameters:

* `$value`: `int` Value to convert  



### `packSignedLong(int $value): string`

Convert integer to base256 long.


Parameters:

* `$value`: `int` Value to convert  



### `packUnsignedInt(int $value): string`

Convert value to unsigned base256 int.


Parameters:

* `$value`: `int` Value  



### `peerIsset(mixed $id): bool`

Check if peer is present in internal peer database.


Parameters:

* `$id`: `mixed` Peer  



### `phoneLogin(string $number, int $sms_type): mixed`

Login as user.


Parameters:

* `$number`: `string` Phone number  
* `$sms_type`: `int` SMS type  



### `posmod(int $a, int $b): int`

Positive modulo
Works just like the % (modulus) operator, only returns always a postive number.


Parameters:

* `$a`: `int` A  
* `$b`: `int` B  



### `qrLogin(): ?\danog\MadelineProto\TL\Types\LoginQrCode`

Initiates QR code login.
Returns a QR code login helper object, that can be used to render the QR code, display the link directly, wait for login, QR code expiration and much more.  
  
Returns null if we're already logged in, or if we're waiting for a password (use getAuthorization to distinguish between the two cases).

#### See also: 
* [`\danog\MadelineProto\TL\Types\LoginQrCode`: Represents a login QR code.](../../danog/MadelineProto/TL/Types/LoginQrCode.html)




### `random(int $length): string`

Get secure random string of specified length.


Parameters:

* `$length`: `int` Length  



### `randomInt(int $modulus): int`

Get random integer.


Parameters:

* `$modulus`: `int` Modulus  



### `readLine(string $prompt, ?\Amp\Cancellation $cancel): string`

Asynchronously read line.


Parameters:

* `$prompt`: `string` Prompt  
* `$cancel`: `?\Amp\Cancellation`   


#### See also: 
* `\Amp\Cancellation`




### `refreshFullPeerCache(mixed $id): void`

Refresh full peer cache for a certain peer.


Parameters:

* `$id`: `mixed` The peer to refresh  



### `refreshPeerCache(mixed $ids): void`

Refresh peer cache for a certain peer.


Parameters:

* `$ids`: `mixed`   



### `rekey(int $chat): ?string`

Rekey secret chat.


Parameters:

* `$chat`: `int` Secret chat to rekey  



### `report(string $message, string $parseMode): void`

Report an error to the previously set peer.


Parameters:

* `$message`: `string` Error to report  
* `$parseMode`: `string` Parse mode  



### `requestCall(mixed $user): mixed`

Request VoIP call.


Parameters:

* `$user`: `mixed` User  



### `requestSecretChat(mixed $user): mixed`

Request secret chat.


Parameters:

* `$user`: `mixed` User to start secret chat with  



### `resetUpdateState(): void`

Reset the update state and fetch all updates from the beginning.



### `restart(): void`

Restart update loop.



### `rethrow(\Throwable $e): void`

Rethrow exception into event loop.


Parameters:

* `$e`: `\Throwable`   


#### See also: 
* `\Throwable`




### `rleDecode(string $string): string`

null-byte RLE decode.


Parameters:

* `$string`: `string` Data to decode  



### `rleEncode(string $string): string`

null-byte RLE encode.


Parameters:

* `$string`: `string` Data to encode  



### `secretChatStatus(int $chat): \int One of MTProto::SECRET_EMPTY, MTProto::SECRET_REQUESTED, MTProto::SECRET_READY`

Get secret chat status.


Parameters:

* `$chat`: `int` Chat ID  


Return value: One of MTProto::SECRET_EMPTY, MTProto::SECRET_REQUESTED, MTProto::SECRET_READY


### `sendCustomEvent(mixed $payload): void`

Sends an updateCustomEvent update to the event handler.


Parameters:

* `$payload`: `mixed`   



### `setNoop(): void`

Set NOOP update handler, ignoring all updates.



### `setReportPeers(int|string|(int|string)[] $userOrId): void`

Set peer(s) where to send errors occurred in the event loop.


Parameters:

* `$userOrId`: `int|string|(int|string)[]` Username(s) or peer ID(s)  



### `setWebhook(string $webhookUrl): void`

Set webhook update handler.


Parameters:

* `$webhookUrl`: `string` Webhook URL  



### `setupLogger(): void`

Setup logger.



### `sleep(float $time): void`

Asynchronously sleep.


Parameters:

* `$time`: `float` Number of seconds to sleep for  



### `start(): mixed`

Log in to telegram (via CLI or web).



### `stop(): void`

Stop update loop.



### `subscribeToUpdates(mixed $channel): \bool False if we were already subscribed`

Subscribe to event handler updates for a channel/supergroup we're not a member of.


Parameters:

* `$channel`: `mixed` Channel/supergroup to subscribe to  


Return value: False if we were already subscribed


### `tdToMTProto(array $params): array`

Convert TD to MTProto parameters.


Parameters:

* `$params`: `array` Parameters  



### `tdToTdcli(mixed $params): mixed`

Convert TD parameters to tdcli.


Parameters:

* `$params`: `mixed` Parameters  



### `tdcliToTd(mixed $params, array $key): array`

Convert tdcli parameters to tdcli.


Parameters:

* `$params`: `mixed` Params  
* `$key`: `array` Key  



### `testFibers(int $fiberCount): array{maxFibers: int, realMemoryMb: int, maps: ?int, maxMaps: ?int}`

Test fibers.


Parameters:

* `$fiberCount`: `int`   



### `toCamelCase(string $input): string`

Convert to camelCase.


Parameters:

* `$input`: `string` String  



### `toSnakeCase(string $input): string`

Convert to snake_case.


Parameters:

* `$input`: `string` String  



### `toSupergroup(int $id): int`

Convert MTProto channel ID to bot API channel ID.


Parameters:

* `$id`: `int` MTProto channel ID  



### `unpackDouble(string $value): float`

Unpack binary double.


Parameters:

* `$value`: `string` Value to unpack  



### `unpackFileId(string $fileId): \array Unpacked file ID`

Unpack bot API file ID.


Parameters:

* `$fileId`: `string` Bot API file ID  


Return value: Unpacked file ID


### `unpackSignedInt(string $value): int`

Unpack base256 signed int.


Parameters:

* `$value`: `string` base256 int  



### `unpackSignedLong(string $value): int`

Unpack base256 signed long.


Parameters:

* `$value`: `string` base256 long  



### `unpackSignedLongString(string|int|array $value): string`

Unpack base256 signed long to string.


Parameters:

* `$value`: `string|int|array` base256 long  



### `unsetEventHandler(): void`

Unset event handler.



### `update2fa(array{password?: string, new_password?: string, email?: string, hint?: string} $params): void`

Update the 2FA password.
The params array can contain password, new_password, email and hint params.

Parameters:

* `$params`: `array{password?: string, new_password?: string, email?: string, hint?: string}` The params  



### `updateSettings(\danog\MadelineProto\SettingsAbstract $settings): void`

Parse, update and store settings.


Parameters:

* `$settings`: `\danog\MadelineProto\SettingsAbstract` Settings  


#### See also: 
* `\danog\MadelineProto\SettingsAbstract`




### `upload(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb, bool $encrypted): mixed`

Upload file.


Parameters:

* `$file`: `\danog\MadelineProto\FileCallbackInterface|string|array` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../danog/MadelineProto/FileCallbackInterface.html)




### `uploadEncrypted(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb): mixed`

Upload file to secret chat.


Parameters:

* `$file`: `\danog\MadelineProto\FileCallbackInterface|string|array` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../danog/MadelineProto/FileCallbackInterface.html)




### `uploadFromCallable(mixed $callable, int $size, string $mime, string $fileName, callable $cb, bool $seekable, bool $encrypted): mixed`

Upload file from callable.
The callable must accept two parameters: int $offset, int $size  
The callable must return a string with the contest of the file at the specified offset and size.

Parameters:

* `$callable`: `mixed` Callable  
* `$size`: `int` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$seekable`: `bool` Whether chunks can be fetched out of order  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  



### `uploadFromStream(mixed $stream, int $size, string $mime, string $fileName, callable $cb, bool $encrypted): mixed`

Upload file from stream.


Parameters:

* `$stream`: `mixed` PHP resource or AMPHP async stream  
* `$size`: `int` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  



### `uploadFromTgfile(mixed $media, callable $cb, bool $encrypted): mixed`

Reupload telegram file.


Parameters:

* `$media`: `mixed` Telegram file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  



### `uploadFromUrl(string|\danog\MadelineProto\FileCallbackInterface $url, int $size, string $fileName, callable $cb, bool $encrypted): mixed`

Upload file from URL.


Parameters:

* `$url`: `string|\danog\MadelineProto\FileCallbackInterface` URL of file  
* `$size`: `int` Size of file  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../danog/MadelineProto/FileCallbackInterface.html)




### `viewSponsoredMessage(int|array $peer, string|array{random_id: string} $message): bool`

Mark sponsored message as read.


Parameters:

* `$peer`: `int|array` Channel ID, or Update, or Message, or Peer.  
* `$message`: `string|array{random_id: string}` Random ID or sponsored message to mark as read.  



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
