Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaScannerConnection

Kotlin | [Java](MediaScannerConnection.md)
| --- | --- |

```
open class MediaScannerConnection : ServiceConnection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaScannerConnection](MediaScannerConnection.md) |

MediaScannerConnection provides a way for applications to pass a newly created or downloaded media file to the media scanner service. The media scanner service will read metadata from the file and add the file to the media content provider. The MediaScannerConnectionClient provides an interface for the media scanner service to return the Uri for a newly scanned file to the client of the MediaScannerConnection class.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.MediaScannerConnectionClient` An interface for notifying clients of MediaScannerConnection when a connection to the MediaScanner service has been established and when the scanning of a file has completed. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.OnScanCompletedListener` Interface for notifying clients of the result of scanning a requested media file. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#MediaScannerConnection(android.content.Context,%20android.media.MediaScannerConnection.MediaScannerConnectionClient)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, client: https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.MediaScannerConnectionClient!)` Constructs a new MediaScannerConnection object. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#connect()()` Initiates a connection to the media scanner service. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#disconnect()()` Releases the connection to the media scanner service. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#isConnected()()` Returns whether we are connected to the media scanner service |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#onServiceConnected(android.content.ComponentName,%20android.os.IBinder)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, service: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!)` Part of the ServiceConnection interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#onServiceDisconnected(android.content.ComponentName)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Part of the ServiceConnection interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#scanFile(kotlin.String,%20kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Requests the media scanner to scan a file. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#scanFile(android.content.Context,%20kotlin.Array,%20kotlin.Array,%20android.media.MediaScannerConnection.OnScanCompletedListener)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, paths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, mimeTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, callback: https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.OnScanCompletedListener!)` Convenience for constructing a `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#`, calling `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#connect()` on it, and calling `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#scanFile(kotlin.String,%20kotlin.String)` with the given path and mimeType when the connection is established. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#onBindingDied(android.content.ComponentName)(name: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Called when the binding to this connection is dead. This means the interface will never receive another connection. The application will need to unbind and rebind the connection to activate it again. This may happen, for example, if the application hosting the service it is bound to has been updated. **Note:** The app that requested the binding must call `https://developer.android.com/reference/kotlin/android/content/Context.html#unbindService(android.content.ServiceConnection)` to release the tracking resources associated with this ServiceConnection even if this callback was invoked following android.content.Context#bindService. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#onNullBinding(android.content.ComponentName)(name: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Called when the service being bound has returned `null` from its `https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent)` method. This indicates that the attempted service binding represented by this ServiceConnection will never become usable. **Note:** The app that requested the binding must still call `https://developer.android.com/reference/kotlin/android/content/Context.html#unbindService(android.content.ServiceConnection)` to release the tracking resources associated with this ServiceConnection even if this callback was invoked following android.content.Context#bindService. <br /> | ||

## Public constructors

### MediaScannerConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaScannerConnection(
    context: Context!, 
    client: MediaScannerConnection.MediaScannerConnectionClient!)
```

Constructs a new MediaScannerConnection object.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: the Context object, required for establishing a connection to the media scanner service. |
| `client` | [MediaScannerConnection.MediaScannerConnectionClient](../android/media/MediaScannerConnection.MediaScannerConnectionClient.md)!: an optional object implementing the MediaScannerConnectionClient interface, for receiving notifications from the media scanner. |

## Public methods

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun connect(): Unit
```

Initiates a connection to the media scanner service. `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.MediaScannerConnectionClient#onMediaScannerConnected()` will be called when the connection is established.

### disconnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun disconnect(): Unit
```

Releases the connection to the media scanner service.

### isConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isConnected(): Boolean
```

Returns whether we are connected to the media scanner service

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if we are connected, false otherwise |

### onServiceConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onServiceConnected(
    className: ComponentName!, 
    service: IBinder!
): Unit
```

Part of the ServiceConnection interface. Do not call.

| Parameters ||
|---|---|
| `name` | The concrete component name of the service that has been connected. |
| `service` | [IBinder](../android.os/IBinder.md)!: The IBinder of the Service's communication channel, which you can now make calls on. |

### onServiceDisconnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onServiceDisconnected(className: ComponentName!): Unit
```

Part of the ServiceConnection interface. Do not call.

| Parameters ||
|---|---|
| `name` | The concrete component name of the service whose connection has been lost. |

### scanFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun scanFile(
    path: String!, 
    mimeType: String!
): Unit
```

Requests the media scanner to scan a file. Success or failure of the scanning operation cannot be determined until `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.OnScanCompletedListener#onScanCompleted(kotlin.String,%20android.net.Uri)` is called.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the path to the file to be scanned. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: an optional mimeType for the file. If mimeType is null, then the mimeType will be inferred from the file extension. |

### scanFile

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun scanFile(
    context: Context!, 
    paths: Array<String!>!, 
    mimeTypes: Array<String!>!, 
    callback: MediaScannerConnection.OnScanCompletedListener!
): Unit
```

Convenience for constructing a `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#`, calling `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#connect()` on it, and calling `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#scanFile(kotlin.String,%20kotlin.String)` with the given path and mimeType when the connection is established.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: The caller's Context, required for establishing a connection to the media scanner service. Success or failure of the scanning operation cannot be determined until `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.OnScanCompletedListener#onScanCompleted(kotlin.String,%20android.net.Uri)` is called. |
| `paths` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: Array of paths to be scanned. |
| `mimeTypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: Optional array of MIME types for each path. If mimeType is null, then the mimeType will be inferred from the file extension. |
| --- | --- |
| `callback` | [MediaScannerConnection.OnScanCompletedListener](../android/media/MediaScannerConnection.OnScanCompletedListener.md)!: Optional callback through which you can receive the scanned URI and MIME type; If null, the file will be scanned but you will not get a result back. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection#scanFile(kotlin.String,%20kotlin.String)`
