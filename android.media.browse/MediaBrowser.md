# MediaBrowser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaBrowser

Kotlin| [Java](https://developer.android.com/reference/android/media/browse/MediaBrowser "View this page in Java") 
| --- | --- |

```
class MediaBrowser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.browse.MediaBrowser](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#) |

Browses media content offered by a link MediaBrowserService.

This object is not thread-safe. All calls should happen on the thread on which the browser was constructed.

### Standard Extra Data

These are the current standard fields that can be used as extra data via [subscribe(java.lang.String,android.os.Bundle,android.media.browse.MediaBrowser.SubscriptionCallback)](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#subscribe(kotlin.String,%20android.os.Bundle,%20android.media.browse.MediaBrowser.SubscriptionCallback)), [unsubscribe(java.lang.String,android.media.browse.MediaBrowser.SubscriptionCallback)](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#unsubscribe(kotlin.String,%20android.media.browse.MediaBrowser.SubscriptionCallback)), and [SubscriptionCallback.onChildrenLoaded(String, List, Bundle)](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.SubscriptionCallback#onChildrenLoaded(kotlin.String,%20kotlin.collections.MutableList,%20android.os.Bundle)).

- [EXTRA_PAGE](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#EXTRA_PAGE:kotlin.String)
- [EXTRA_PAGE_SIZE](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#EXTRA_PAGE_SIZE:kotlin.String)

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ConnectionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.ConnectionCallback) Callbacks for connection related events. |
| abstract | [ItemCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.ItemCallback) Callback for receiving the result of [getItem](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#getItem(kotlin.String,%20android.media.browse.MediaBrowser.ItemCallback)). |
| | [MediaItem](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.MediaItem) A class with information on a single media item for use in browsing/searching media. |
| --- | --- |
| abstract | [SubscriptionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.SubscriptionCallback) Callbacks for subscription related events. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PAGE](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#EXTRA_PAGE:kotlin.String) Used as an int extra field to denote the page number to subscribe. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PAGE_SIZE](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#EXTRA_PAGE_SIZE:kotlin.String) Used as an int extra field to denote the number of media items in a page. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaBrowser](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#MediaBrowser(android.content.Context,%20android.content.ComponentName,%20android.media.browse.MediaBrowser.ConnectionCallback,%20android.os.Bundle))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `serviceComponent:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!`, `callback:` ` [MediaBrowser.ConnectionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.ConnectionCallback)!`, `rootHints:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Creates a media browser for the specified media browser service. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#connect())`()` Connects to the media browser service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#disconnect())`()` Disconnects from the media browser service. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [getExtras](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#getExtras())`()` Gets any extras for the media service. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getItem](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#getItem(kotlin.String,%20android.media.browse.MediaBrowser.ItemCallback))`(`mediaId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cb:` ` [MediaBrowser.ItemCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.ItemCallback)`)` Retrieves a specific [MediaItem](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.MediaItem) from the connected service. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getRoot](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#getRoot())`()` Gets the root id. |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) | [getServiceComponent](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#getServiceComponent())`()` Gets the service component that the media browser is connected to. |
| --- | --- |
| [MediaSession.Token](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token.html#) | [getSessionToken](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#getSessionToken())`()` Gets the media session token associated with the media browser. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#isConnected())`()` Returns whether the browser is connected to the service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [subscribe](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#subscribe(kotlin.String,%20android.media.browse.MediaBrowser.SubscriptionCallback))`(`parentId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `callback:` ` [MediaBrowser.SubscriptionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.SubscriptionCallback)`)` Queries for information about the media items that are contained within the specified id and subscribes to receive updates when they change. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [subscribe](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#subscribe(kotlin.String,%20android.os.Bundle,%20android.media.browse.MediaBrowser.SubscriptionCallback))`(`parentId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`, `callback:` ` [MediaBrowser.SubscriptionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.SubscriptionCallback)`)` Queries with service-specific arguments for information about the media items that are contained within the specified id and subscribes to receive updates when they change. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unsubscribe](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#unsubscribe(kotlin.String))`(`parentId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Unsubscribes for changes to the children of the specified media id. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unsubscribe](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#unsubscribe(kotlin.String,%20android.media.browse.MediaBrowser.SubscriptionCallback))`(`parentId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `callback:` ` [MediaBrowser.SubscriptionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.SubscriptionCallback)`)` Unsubscribes for changes to the children of the specified media id through a callback. |
| --- | --- |

## Constants

### EXTRA_PAGE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PAGE: String
```

Used as an int extra field to denote the page number to subscribe. The value of`EXTRA_PAGE`should be greater than or equal to 0. 

 Value: "android.media.browse.extra.PAGE"

**See Also**

- [#EXTRA_PAGE_SIZE](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#EXTRA_PAGE_SIZE:kotlin.String) 

### EXTRA_PAGE_SIZE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PAGE_SIZE: String
```

Used as an int extra field to denote the number of media items in a page. The value of`EXTRA_PAGE_SIZE`should be greater than or equal to 1. 

 Value: "android.media.browse.extra.PAGE_SIZE"

**See Also**

- [#EXTRA_PAGE](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser#EXTRA_PAGE:kotlin.String)

## Public constructors

### MediaBrowser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaBrowser(
    context: Context!, 
    serviceComponent: ComponentName!, 
    callback: MediaBrowser.ConnectionCallback!, 
    rootHints: Bundle!)
```

Creates a media browser for the specified media browser service.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context. |
| `serviceComponent` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!:The component name of the media browser service. |
| `callback` | [MediaBrowser.ConnectionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.ConnectionCallback)!:The connection callback. |
| --- | --- |
| `rootHints` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:An optional bundle of service-specific arguments to send to the media browser service when connecting and retrieving the root id for browsing, or null if none. The contents of this bundle may affect the information returned when browsing. |

**See Also**

- [android.service.media.MediaBrowserService.BrowserRoot#EXTRA_RECENT](https://developer.android.com/reference/kotlin/android/service/media/MediaBrowserService.BrowserRoot.html#EXTRA_RECENT:kotlin.String)
- [android.service.media.MediaBrowserService.BrowserRoot#EXTRA_OFFLINE](https://developer.android.com/reference/kotlin/android/service/media/MediaBrowserService.BrowserRoot.html#EXTRA_OFFLINE:kotlin.String)
- [android.service.media.MediaBrowserService.BrowserRoot#EXTRA_SUGGESTED](https://developer.android.com/reference/kotlin/android/service/media/MediaBrowserService.BrowserRoot.html#EXTRA_SUGGESTED:kotlin.String)

## Public methods

### connect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connect(): Unit
```

Connects to the media browser service.

The connection callback specified in the constructor will be invoked when the connection completes or fails. 

### disconnect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disconnect(): Unit
```

Disconnects from the media browser service. After this, no more callbacks will be received. 

### getExtras

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle?
```

Gets any extras for the media service.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

| Exceptions ||
|-----------------------------------|-------------------|
| `java.lang.IllegalStateException` | if not connected. |

### getItem

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getItem(
    mediaId: String, 
    cb: MediaBrowser.ItemCallback
): Unit
```

Retrieves a specific [MediaItem](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.MediaItem) from the connected service. Not all services may support this, so falling back to subscribing to the parent's id should be used when unavailable.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The id of the item to retrieve. This value cannot be`null`. |
| `cb` | [MediaBrowser.ItemCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.ItemCallback):The callback to receive the result on. This value cannot be`null`. |

### getRoot

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoot(): String
```

Gets the root id.

Note that the root id may become invalid or change when the browser is disconnected.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------|
| `java.lang.IllegalStateException` | if not connected. |

### getServiceComponent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceComponent(): ComponentName
```

Gets the service component that the media browser is connected to.

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------|
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) | This value cannot be`null`. |

### getSessionToken

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionToken(): MediaSession.Token
```

Gets the media session token associated with the media browser.

Note that the session token may become invalid or change when the browser is disconnected.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MediaSession.Token](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token.html#) | The session token for the browser, never null. |

| Exceptions ||
|-----------------------------------|-------------------|
| `java.lang.IllegalStateException` | if not connected. |

### isConnected

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

Returns whether the browser is connected to the service. 

### subscribe

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun subscribe(
    parentId: String, 
    callback: MediaBrowser.SubscriptionCallback
): Unit
```

Queries for information about the media items that are contained within the specified id and subscribes to receive updates when they change.

The list of subscriptions is maintained even when not connected and is restored after the reconnection. It is ok to subscribe while not connected but the results will not be returned until the connection completes.

If the id is already subscribed with a different callback then the new callback will replace the previous one and the child data will be reloaded.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The id of the parent media item whose list of children will be subscribed. This value cannot be`null`. |
| `callback` | [MediaBrowser.SubscriptionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.SubscriptionCallback):The callback to receive the list of children. This value cannot be`null`. |

### subscribe

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun subscribe(
    parentId: String, 
    options: Bundle, 
    callback: MediaBrowser.SubscriptionCallback
): Unit
```

Queries with service-specific arguments for information about the media items that are contained within the specified id and subscribes to receive updates when they change.

The list of subscriptions is maintained even when not connected and is restored after the reconnection. It is ok to subscribe while not connected but the results will not be returned until the connection completes.

If the id is already subscribed with a different callback then the new callback will replace the previous one and the child data will be reloaded.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The id of the parent media item whose list of children will be subscribed. This value cannot be`null`. |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):The bundle of service-specific arguments to send to the media browser service. The contents of this bundle may affect the information returned when browsing. This value cannot be`null`. |
| `callback` | [MediaBrowser.SubscriptionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.SubscriptionCallback):The callback to receive the list of children. This value cannot be`null`. |
| --- | --- |

### unsubscribe

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unsubscribe(parentId: String): Unit
```

Unsubscribes for changes to the children of the specified media id.

The query callback will no longer be invoked for results associated with this id once this method returns.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The id of the parent media item whose list of children will be unsubscribed. This value cannot be`null`. |

### unsubscribe

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unsubscribe(
    parentId: String, 
    callback: MediaBrowser.SubscriptionCallback
): Unit
```

Unsubscribes for changes to the children of the specified media id through a callback.

The query callback will no longer be invoked for results associated with this id once this method returns.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parentId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The id of the parent media item whose list of children will be unsubscribed. This value cannot be`null`. |
| `callback` | [MediaBrowser.SubscriptionCallback](https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.SubscriptionCallback):A callback sent to the media browser service to subscribe. This value cannot be`null`. |
