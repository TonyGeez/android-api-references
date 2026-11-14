# MediaBrowser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaBrowser

Kotlin| [Java](MediaBrowser.md) 
| --- | --- |

```
class MediaBrowser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.browse.MediaBrowser](MediaBrowser.md) |

Browses media content offered by a link MediaBrowserService.

This object is not thread-safe. All calls should happen on the thread on which the browser was constructed.

### Standard Extra Data

These are the current standard fields that can be used as extra data via [subscribe(java.lang.String,android.os.Bundle,android.media.browse.MediaBrowser.SubscriptionCallback)](MediaBrowser.md)), [unsubscribe(java.lang.String,android.media.browse.MediaBrowser.SubscriptionCallback)](MediaBrowser.md)), and [SubscriptionCallback.onChildrenLoaded(String, List, Bundle)](../android/media/browse/MediaBrowser.SubscriptionCallback.md)).

- [EXTRA_PAGE](MediaBrowser.md)
- [EXTRA_PAGE_SIZE](MediaBrowser.md)

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ConnectionCallback](../android/media/browse/MediaBrowser.ConnectionCallback.md) Callbacks for connection related events. |
| abstract | [ItemCallback](../android/media/browse/MediaBrowser.ItemCallback.md) Callback for receiving the result of [getItem](MediaBrowser.md)). |
| | [MediaItem](../android/media/browse/MediaBrowser.MediaItem.md) A class with information on a single media item for use in browsing/searching media. |
| --- | --- |
| abstract | [SubscriptionCallback](../android/media/browse/MediaBrowser.SubscriptionCallback.md) Callbacks for subscription related events. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PAGE](MediaBrowser.md) Used as an int extra field to denote the page number to subscribe. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PAGE_SIZE](MediaBrowser.md) Used as an int extra field to denote the number of media items in a page. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaBrowser](MediaBrowser.md))`(`context:` ` [Context](../android.content/Context.md)!`, `serviceComponent:` ` [ComponentName](../android.content/ComponentName.md)!`, `callback:` ` [MediaBrowser.ConnectionCallback](../android/media/browse/MediaBrowser.ConnectionCallback.md)!`, `rootHints:` ` [Bundle](../android.os/Bundle.md)!`)` Creates a media browser for the specified media browser service. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](MediaBrowser.md))`()` Connects to the media browser service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](MediaBrowser.md))`()` Disconnects from the media browser service. |
| [Bundle](../android.os/Bundle.md)? | [getExtras](MediaBrowser.md))`()` Gets any extras for the media service. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getItem](MediaBrowser.md))`(`mediaId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cb:` ` [MediaBrowser.ItemCallback](../android/media/browse/MediaBrowser.ItemCallback.md)`)` Retrieves a specific [MediaItem](../android/media/browse/MediaBrowser.MediaItem.md) from the connected service. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getRoot](MediaBrowser.md))`()` Gets the root id. |
| [ComponentName](../android.content/ComponentName.md) | [getServiceComponent](MediaBrowser.md))`()` Gets the service component that the media browser is connected to. |
| --- | --- |
| [MediaSession.Token](../android/media/session/MediaSession.Token.md) | [getSessionToken](MediaBrowser.md))`()` Gets the media session token associated with the media browser. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](MediaBrowser.md))`()` Returns whether the browser is connected to the service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [subscribe](MediaBrowser.md))`(`parentId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `callback:` ` [MediaBrowser.SubscriptionCallback](../android/media/browse/MediaBrowser.SubscriptionCallback.md)`)` Queries for information about the media items that are contained within the specified id and subscribes to receive updates when they change. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [subscribe](MediaBrowser.md))`(`parentId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `options:` ` [Bundle](../android.os/Bundle.md)`, `callback:` ` [MediaBrowser.SubscriptionCallback](../android/media/browse/MediaBrowser.SubscriptionCallback.md)`)` Queries with service-specific arguments for information about the media items that are contained within the specified id and subscribes to receive updates when they change. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unsubscribe](MediaBrowser.md))`(`parentId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Unsubscribes for changes to the children of the specified media id. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unsubscribe](MediaBrowser.md))`(`parentId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `callback:` ` [MediaBrowser.SubscriptionCallback](../android/media/browse/MediaBrowser.SubscriptionCallback.md)`)` Unsubscribes for changes to the children of the specified media id through a callback. |
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

- [#EXTRA_PAGE_SIZE](MediaBrowser.md) 

### EXTRA_PAGE_SIZE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PAGE_SIZE: String
```

Used as an int extra field to denote the number of media items in a page. The value of`EXTRA_PAGE_SIZE`should be greater than or equal to 1. 

 Value: "android.media.browse.extra.PAGE_SIZE"

**See Also**

- [#EXTRA_PAGE](MediaBrowser.md)

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
| `context` | [Context](../android.content/Context.md)!:The context. |
| `serviceComponent` | [ComponentName](../android.content/ComponentName.md)!:The component name of the media browser service. |
| `callback` | [MediaBrowser.ConnectionCallback](../android/media/browse/MediaBrowser.ConnectionCallback.md)!:The connection callback. |
| --- | --- |
| `rootHints` | [Bundle](../android.os/Bundle.md)!:An optional bundle of service-specific arguments to send to the media browser service when connecting and retrieving the root id for browsing, or null if none. The contents of this bundle may affect the information returned when browsing. |

**See Also**

- [android.service.media.MediaBrowserService.BrowserRoot#EXTRA_RECENT](../android/service/media/MediaBrowserService.BrowserRoot.md)
- [android.service.media.MediaBrowserService.BrowserRoot#EXTRA_OFFLINE](../android/service/media/MediaBrowserService.BrowserRoot.md)
- [android.service.media.MediaBrowserService.BrowserRoot#EXTRA_SUGGESTED](../android/service/media/MediaBrowserService.BrowserRoot.md)

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
| [Bundle](../android.os/Bundle.md)? | This value may be`null`. |

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

Retrieves a specific [MediaItem](../android/media/browse/MediaBrowser.MediaItem.md) from the connected service. Not all services may support this, so falling back to subscribing to the parent's id should be used when unavailable.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The id of the item to retrieve. This value cannot be`null`. |
| `cb` | [MediaBrowser.ItemCallback](../android/media/browse/MediaBrowser.ItemCallback.md):The callback to receive the result on. This value cannot be`null`. |

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
| [ComponentName](../android.content/ComponentName.md) | This value cannot be`null`. |

### getSessionToken

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionToken(): MediaSession.Token
```

Gets the media session token associated with the media browser.

Note that the session token may become invalid or change when the browser is disconnected.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MediaSession.Token](../android/media/session/MediaSession.Token.md) | The session token for the browser, never null. |

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
| `callback` | [MediaBrowser.SubscriptionCallback](../android/media/browse/MediaBrowser.SubscriptionCallback.md):The callback to receive the list of children. This value cannot be`null`. |

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
| `options` | [Bundle](../android.os/Bundle.md):The bundle of service-specific arguments to send to the media browser service. The contents of this bundle may affect the information returned when browsing. This value cannot be`null`. |
| `callback` | [MediaBrowser.SubscriptionCallback](../android/media/browse/MediaBrowser.SubscriptionCallback.md):The callback to receive the list of children. This value cannot be`null`. |
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
| `callback` | [MediaBrowser.SubscriptionCallback](../android/media/browse/MediaBrowser.SubscriptionCallback.md):A callback sent to the media browser service to subscribe. This value cannot be`null`. |
