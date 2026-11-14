Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaRouter2

```
class MediaRouter2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaRouter2](MediaRouter2.md) |

This API is not generally intended for third party application developers. Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Media Router Library](../androidx/mediarouter/media/_package.md) for consistent behavior across all devices.

MediaRouter2 allows applications to control the routing of media channels and streams from the current device to remote speakers and devices.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback` Callback for receiving `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` updates. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback` Callback for receiving events about device suggestions |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.OnGetControllerHintsListener` A listener interface to send optional app-specific hints when creating a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController`. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback` Callback for receiving events about media route discovery. |
| | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` Controls a media routing session. |
| | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanRequest` Represents a set of parameters for scanning requests. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken` Represents an active scan request registered in the system. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.TransferCallback` Callback for receiving events on media transfer. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancelScanRequest Releases the active scan request linked to the provided `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearDeviceSuggestions Clears the SuggestedDeviceInfo provided by this router. |
| [MediaRouter2.RoutingController](../android/media/MediaRouter2.RoutingController.md)? | getController Gets a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` whose ID is equal to the given ID. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaRouter2.RoutingController](../android/media/MediaRouter2.RoutingController.md)!\> | getControllers Gets the list of currently active `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` on which media can be played. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SuggestedDeviceInfo](SuggestedDeviceInfo.md)!\>!\> | getDeviceSuggestions Gets the current suggested devices. |
| static [MediaRouter2](MediaRouter2.md) | getInstance Gets an instance of the media router associated with the context. |
| --- | --- |
| static [MediaRouter2](MediaRouter2.md) | getInstance Returns a proxy MediaRouter2 instance that allows you to control the routing of an app specified by `clientPackageName`. |
| [RouteListingPreference](RouteListingPreference.md)? | getRouteListingPreference Returns the current RouteListingPreference of the target router. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaRoute2Info](MediaRoute2Info.md)!\> | getRoutes Gets the unmodifiable list of MediaRoute2Info currently known to the media router. |
| --- | --- |
| [MediaRouter2.RoutingController](../android/media/MediaRouter2.RoutingController.md) | getSystemController Gets a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` which can control the routes provided by system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerControllerCallback Registers a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerDeviceSuggestionsUpdatesCallback Registers the given callback to be invoked when the SuggestedDeviceInfo of the target router changes. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerRouteCallback Registers a callback to discover routes and to receive events when they change. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerRouteListingPreferenceUpdatedCallback Registers the given callback to be invoked when the RouteListingPreference of the target router changes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerTransferCallback Registers a callback to get the result of transferTo. |
| --- | --- |
| [MediaRouter2.ScanToken](../android/media/MediaRouter2.ScanToken.md) | requestScan Requests the system to actively scan for routes based on the router's RouteDiscoveryPreference. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDeviceSuggestions Sets a list of SuggestedDeviceInfo. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnGetControllerHintsListener Sets an `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.OnGetControllerHintsListener` to send hints when creating a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRouteListingPreference Sets the RouteListingPreference of the app associated to this media router. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRouteVolume Sets the volume for a specific route. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | showSystemOutputSwitcher Shows the system output switcher dialog. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | showSystemOutputSwitcher Shows the system output switcher dialog for a specific MediaSession. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stop Stops the current media routing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | transferTo Transfers the current media to the given route. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterControllerCallback Unregisters a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterDeviceSuggestionsUpdatesCallback Unregisters the given callback to not receive SuggestedDeviceInfo change events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterRouteCallback Unregisters the given callback. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterRouteListingPreferenceUpdatedCallback Unregisters the given callback to not receive RouteListingPreference change events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterTransferCallback Unregisters the given callback. |

## Public methods

### cancelScanRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancelScanRequest(token: MediaRouter2.ScanToken): Unit
```

Releases the active scan request linked to the provided `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken`.

| Parameters ||
|---|---|
| `token` | [MediaRouter2.ScanToken](../android/media/MediaRouter2.ScanToken.md): `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken` of the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanRequest` to release. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the token does not match any active scan request. |

**See Also**

- requestScan

### clearDeviceSuggestions

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearDeviceSuggestions(): Unit
```

Clears the SuggestedDeviceInfo provided by this router.

Use this method to tell the system that this router is not currently providing any suggestions.

If the router explicitly wants to recommend that no suggestion is appropriate, use setDeviceSuggestions with an empty list

### getController

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getController(id: String): MediaRouter2.RoutingController?
```

Gets a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` whose ID is equal to the given ID. Returns `null` if there is no matching controller.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### getControllers

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getControllers(): MutableList<MediaRouter2.RoutingController!>
```

Gets the list of currently active `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` on which media can be played.

Note: The list returned here will never be empty. The first element in the list is always the getSystemController.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController!>` | This value cannot be `null`. |

### getDeviceSuggestions

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeviceSuggestions(): MutableMap<String!, MutableList<SuggestedDeviceInfo!>!>
```

Gets the current suggested devices.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo!>!>` | the suggested devices, keyed by the package name providing each suggestion list. This value cannot be `null`. |

### getInstance

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(context: Context): MediaRouter2
```

Gets an instance of the media router associated with the context.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): This value cannot be `null`. |

| Return ||
|---|---|
| MediaRouter2 | This value cannot be `null`. |

### getInstance

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    context: Context, 
    clientPackageName: String, 
    executor: Executor, 
    onInstanceInvalidatedListener: Runnable
): MediaRouter2
```

Returns a proxy MediaRouter2 instance that allows you to control the routing of an app specified by `clientPackageName`.

Proxy MediaRouter2 instances operate differently than regular MediaRouter2 instances:

- registerRouteCallback ignores any RouteDiscoveryPreference passed by a proxy router. Use android.media.RouteDiscoveryPreference#EMPTY when setting a route callback.

- Methods returning non-system `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` always return new instances with the latest data. Do not attempt to compare or store them. Instead, use getController or getControllers to query the most up-to-date state.

- Calls to setOnGetControllerHintsListener are ignored.

Use this method when you only hold a revocable version of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` (e.g. acquired via the `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#`). Otherwise, use #getInstance(android.content.Context,java.lang.String).

`onInstanceInvalidatedListener` is called when the instance is invalidated because the calling app has lost `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` and does not hold `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String`. Do not use the invalidated instance after receiving this callback, as the system will ignore all operations. Call getInstance again after reacquiring the relevant permissions. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String`

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The `https://developer.android.com/reference/kotlin/android/content/Context.html#` of the caller. This value cannot be `null`. |
| `clientPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name of the app you want to control the routing of, or `"android"` to control the routing of the whole system. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke `onInstanceInvalidatedListener`. This value cannot be `null`. |
| --- | --- |
| `onInstanceInvalidatedListener` | [Runnable](../java.lang/Runnable.md): Callback for when the MediaRouter2 instance is invalidated due to lost permissions. This value cannot be `null`. |

| Return ||
|---|---|
| MediaRouter2 | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `clientPackageName` does not exist in the calling user. |

### getRouteListingPreference

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRouteListingPreference(): RouteListingPreference?
```

Returns the current RouteListingPreference of the target router.

If this instance was created using `getInstance(Context, String)`, then it returns the last RouteListingPreference set by the process this router was created for.

| Return ||
|---|---|
| RouteListingPreference | This value may be `null`. |

**See Also**

- setRouteListingPreference

### getRoutes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRoutes(): MutableList<MediaRoute2Info!>
```

Gets the unmodifiable list of MediaRoute2Info currently known to the media router.

Please note that the list can be changed before callbacks are invoked.

This method returns routes available to the routing framework that contain at least one of the getPreferredFeatures registered by the application through registerRouteCallback. As a result, you need to register at least one `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback` (associated with the features that you are interested in), in order for this method to return a non-empty list.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info!>` | the list of routes that contains at least one of the route features in discovery preferences registered by the application. This value cannot be `null`. |

### getSystemController

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSystemController(): MediaRouter2.RoutingController
```

Gets a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` which can control the routes provided by system. e.g. Phone speaker, wired headset, Bluetooth, etc.

Note: The system controller can't be released. Calling release will be ignored.

This method always returns the same instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` | This value cannot be `null`. |

### registerControllerCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerControllerCallback(
    executor: Executor, 
    callback: MediaRouter2.ControllerCallback
): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback`. If you register the same callback twice or more, it will be ignored.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [MediaRouter2.ControllerCallback](../android/media/MediaRouter2.ControllerCallback.md): This value cannot be `null`. |

**See Also**

- unregisterControllerCallback

### registerDeviceSuggestionsUpdatesCallback

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerDeviceSuggestionsUpdatesCallback(
    executor: Executor, 
    deviceSuggestionsUpdatesCallback: MediaRouter2.DeviceSuggestionsUpdatesCallback
): Unit
```

Registers the given callback to be invoked when the SuggestedDeviceInfo of the target router changes.

Calls using a previously registered callback will overwrite the previous executor.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `deviceSuggestionsUpdatesCallback` | [MediaRouter2.DeviceSuggestionsUpdatesCallback](../android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback.md): This value cannot be `null`. |

### registerRouteCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerRouteCallback(
    executor: Executor, 
    routeCallback: MediaRouter2.RouteCallback, 
    preference: RouteDiscoveryPreference
): Unit
```

Registers a callback to discover routes and to receive events when they change.

Clients can register multiple callbacks, as long as the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback` instances are different. Each callback can provide a unique RouteDiscoveryPreference and will only receive updates related to that set preference.

If the specified callback is already registered, its registration will be updated for the given `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` and RouteDiscoveryPreference.

getInstance must register a route callback to register in the system and start receiving updates. Otherwise, all operations will be no-ops.

Any discovery preference passed by a #getInstance(android.content.Context,java.lang.String) will be ignored and will receive route updates based on the preference set by its matching local router.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `routeCallback` | [MediaRouter2.RouteCallback](../android/media/MediaRouter2.RouteCallback.md): This value cannot be `null`. |
| `preference` | [RouteDiscoveryPreference](RouteDiscoveryPreference.md): This value cannot be `null`. |
| --- | --- |

### registerRouteListingPreferenceUpdatedCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerRouteListingPreferenceUpdatedCallback(
    executor: Executor, 
    routeListingPreferenceCallback: Consumer<RouteListingPreference!>
): Unit
```

Registers the given callback to be invoked when the RouteListingPreference of the target router changes.

Calls using a previously registered callback will overwrite the previous executor.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `routeListingPreferenceCallback` | [Consumer](../java.util.function/Consumer.md)\< [RouteListingPreference](RouteListingPreference.md)!\>: This value cannot be `null`. |

**See Also**

- setRouteListingPreference

### registerTransferCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerTransferCallback(
    executor: Executor, 
    callback: MediaRouter2.TransferCallback
): Unit
```

Registers a callback to get the result of transferTo. If you register the same callback twice or more, it will be ignored.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor to execute the callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [MediaRouter2.TransferCallback](../android/media/MediaRouter2.TransferCallback.md): the callback to register. This value cannot be `null`. |

**See Also**

- unregisterTransferCallback

### requestScan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestScan(scanRequest: MediaRouter2.ScanRequest): MediaRouter2.ScanToken
```

Requests the system to actively scan for routes based on the router's RouteDiscoveryPreference.

You must call cancelScanRequest promptly to preserve system resources like battery. Avoid scanning unless there is clear intention from the user to start routing their media.

`scanRequest` specifies relevant scanning options, like whether the system should scan with the screen off. Screen off scanning requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String`.

Proxy routers use the registered RouteDiscoveryPreference of their target routers.

| Parameters ||
|---|---|
| `scanRequest` | [MediaRouter2.ScanRequest](../android/media/MediaRouter2.ScanRequest.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken` | A unique `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken` that identifies the scan request. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanRequest` with setScreenOffScan true is passed, while not holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String`. |

### setDeviceSuggestions

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDeviceSuggestions(suggestedDeviceInfo: MutableList<SuggestedDeviceInfo!>): Unit
```

Sets a list of SuggestedDeviceInfo.

Use this method to tell the system about device suggestions for the current router. The system may use these suggestions to populate system UI such as Output Switcher and media controls.

Suggestions will be expired automatically by the system, at which point you should call this method again if the suggestion is still relevant and should still be surfaced.

| Parameters ||
|---|---|
| `suggestedDeviceInfo` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SuggestedDeviceInfo](SuggestedDeviceInfo.md)!\>: The SuggestedDeviceInfo the router suggests should be provided to the user. This value cannot be `null`. |

### setOnGetControllerHintsListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOnGetControllerHintsListener(listener: MediaRouter2.OnGetControllerHintsListener?): Unit
```

Sets an `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.OnGetControllerHintsListener` to send hints when creating a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController`. To send the hints, listener should be set *BEFORE* calling transferTo.

| Parameters ||
|---|---|
| `listener` | [MediaRouter2.OnGetControllerHintsListener](../android/media/MediaRouter2.OnGetControllerHintsListener.md)?: A listener to send optional app-specific hints when creating a controller. `null` for unset. |

### setRouteListingPreference

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRouteListingPreference(routeListingPreference: RouteListingPreference?): Unit
```

Sets the RouteListingPreference of the app associated to this media router.

Use this method to inform the system UI of the routes that you would like to list for media routing, via the Output Switcher.

You should call this method before registerRouteCallback and immediately after receiving any onRoutesUpdated in order to keep the system UI in a consistent state. You can also call this method at any other point to update the listing preference dynamically.

Calling this method on a proxy router instance will throw an `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

Notes:

1. You should not include the ids of two or more routes with a match in their getDeduplicationIds. If you do, the system will deduplicate them using its own criteria.
2. You can use this method to rank routes in the output switcher, placing the more important routes first. The system might override the proposed ranking.
3. You can use this method to avoid listing routes using dynamic criteria. For example, you can limit access to a specific type of device according to runtime criteria.

| Parameters ||
|---|---|
| `routeListingPreference` | [RouteListingPreference](RouteListingPreference.md)?: The RouteListingPreference for the system to use for route listing. When null, the system uses its default listing criteria. |

### setRouteVolume

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRouteVolume(
    route: MediaRoute2Info, 
    volume: Int
): Unit
```

Sets the volume for a specific route.

The call may have no effect if the route is currently not selected.

This method is only supported by #getInstance(android.content.Context,java.lang.String). Use setVolume instead for getInstance.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String`

| Parameters ||
|---|---|
| `route` | [MediaRoute2Info](MediaRoute2Info.md): This value cannot be `null`. |
| `volume` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new volume value between 0 and getVolumeMax. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If called on a getInstance. |

### showSystemOutputSwitcher

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun showSystemOutputSwitcher(): Boolean
```

Shows the system output switcher dialog.

Should only be called when the context of MediaRouter2 is in the foreground and visible on the screen.

The appearance and precise behaviour of the system output switcher dialog may vary across different devices, OS versions, and form factors, but the basic functionality stays the same.

See [Output Switcher documentation](https://developer.android.com/guide/topics/media/media-routing#output-switcher) for more details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the output switcher dialog is being shown, or `false` if the call is ignored because the app is in the background. |

### showSystemOutputSwitcher

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun showSystemOutputSwitcher(sessionToken: MediaSession.Token): Boolean
```

Shows the system output switcher dialog for a specific MediaSession.

The `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token` argument allows the system to identify which RoutingSessionInfo to display as active. This is done via setPlaybackToRemote and getVolumeControlId when playing remotely, and setPlaybackToLocal when playing on this device.

This method is preferred over showSystemOutputSwitcher to prevent the system from making wrong inferences about where playback is happening.

| Parameters ||
|---|---|
| `sessionToken` | [MediaSession.Token](../android/media/session/MediaSession.Token.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the output switcher dialog is being shown, or `false` if the call is ignored because the app is in the background. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the provided `sessionToken` is invalid. |

### stop

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stop(): Unit
```

Stops the current media routing. If the getSystemController controls the media routing, this method is a no-op.

### transferTo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transferTo(route: MediaRoute2Info): Unit
```

Transfers the current media to the given route. If it's necessary a new `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` is created or it is handled within the current routing controller.

| Parameters ||
|---|---|
| `route` | [MediaRoute2Info](MediaRoute2Info.md): the route you want to transfer the current media to. This value cannot be `null`. |

**See Also**

- onTransfer
- onTransferFailure

### unregisterControllerCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterControllerCallback(callback: MediaRouter2.ControllerCallback): Unit
```

Unregisters a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback`. The callback will no longer receive events. If the callback has not been added or been removed already, it is ignored.

| Parameters ||
|---|---|
| `callback` | [MediaRouter2.ControllerCallback](../android/media/MediaRouter2.ControllerCallback.md): This value cannot be `null`. |

**See Also**

- registerControllerCallback

### unregisterDeviceSuggestionsUpdatesCallback

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterDeviceSuggestionsUpdatesCallback(callback: MediaRouter2.DeviceSuggestionsUpdatesCallback): Unit
```

Unregisters the given callback to not receive SuggestedDeviceInfo change events.

| Parameters ||
|---|---|
| `callback` | [MediaRouter2.DeviceSuggestionsUpdatesCallback](../android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback.md): This value cannot be `null`. |

**See Also**

- registerDeviceSuggestionsUpdatesCallback

### unregisterRouteCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterRouteCallback(routeCallback: MediaRouter2.RouteCallback): Unit
```

Unregisters the given callback. The callback will no longer receive events. If the callback has not been added or been removed already, it is ignored.

| Parameters ||
|---|---|
| `routeCallback` | [MediaRouter2.RouteCallback](../android/media/MediaRouter2.RouteCallback.md): the callback to unregister. This value cannot be `null`. |

**See Also**

- registerRouteCallback

### unregisterRouteListingPreferenceUpdatedCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterRouteListingPreferenceUpdatedCallback(callback: Consumer<RouteListingPreference!>): Unit
```

Unregisters the given callback to not receive RouteListingPreference change events.

| Parameters ||
|---|---|
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [RouteListingPreference](RouteListingPreference.md)!\>: This value cannot be `null`. |

**See Also**

- registerRouteListingPreferenceUpdatedCallback

### unregisterTransferCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterTransferCallback(callback: MediaRouter2.TransferCallback): Unit
```

Unregisters the given callback. The callback will no longer receive events. If the callback has not been added or been removed already, it is ignored.

| Parameters ||
|---|---|
| `callback` | [MediaRouter2.TransferCallback](../android/media/MediaRouter2.TransferCallback.md): the callback to unregister. This value cannot be `null`. |

**See Also**

- registerTransferCallback
