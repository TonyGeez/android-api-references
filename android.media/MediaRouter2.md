Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaRouter2

```
class MediaRouter2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaRouter2](https://developer.android.com/reference/kotlin/android/media/MediaRouter2#) |

This API is not generally intended for third party application developers. Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Media Router Library](https://developer.android.com/reference/androidx/mediarouter/media/package-summary.html) for consistent behavior across all devices.

MediaRouter2 allows applications to control the routing of media channels and streams from the current device to remote speakers and devices.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback` Callback for receiving `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` updates. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback` Callback for receiving events about device suggestions |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.OnGetControllerHintsListener` A listener interface to send optional app-specific hints when creating a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController`. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback` Callback for receiving events about media route discovery. |
| | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` Controls a media routing session. |
| | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanRequest` Represents a set of parameters for scanning requests. |
| | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken` Represents an active scan request registered in the system. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.TransferCallback` Callback for receiving events on media transfer. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#cancelScanRequest(android.media.MediaRouter2.ScanToken)(token: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken)` Releases the active scan request linked to the provided `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#clearDeviceSuggestions()()` Clears the `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo` provided by this router. |
| [MediaRouter2.RoutingController](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController)? | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getController(kotlin.String)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` whose ID is equal to the given ID. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaRouter2.RoutingController](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController)!\> | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getControllers()()` Gets the list of currently active `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` on which media can be played. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SuggestedDeviceInfo](https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo)!\>!\> | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getDeviceSuggestions()()` Gets the current suggested devices. |
| static [MediaRouter2](https://developer.android.com/reference/kotlin/android/media/MediaRouter2#) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getInstance(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Gets an instance of the media router associated with the context. |
| static [MediaRouter2](https://developer.android.com/reference/kotlin/android/media/MediaRouter2#) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getInstance(android.content.Context,%20kotlin.String,%20java.util.concurrent.Executor,%20java.lang.Runnable)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, clientPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, onInstanceInvalidatedListener: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` Returns a proxy MediaRouter2 instance that allows you to control the routing of an app specified by `clientPackageName`. |
| [RouteListingPreference](https://developer.android.com/reference/kotlin/android/media/RouteListingPreference)? | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getRouteListingPreference()()` Returns the current `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` of the target router. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaRoute2Info](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info)!\> | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getRoutes()()` Gets the unmodifiable list of `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info` currently known to the media router. |
| [MediaRouter2.RoutingController](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getSystemController()()` Gets a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` which can control the routes provided by system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerControllerCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.ControllerCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback)` Registers a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerDeviceSuggestionsUpdatesCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.DeviceSuggestionsUpdatesCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, deviceSuggestionsUpdatesCallback: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback)` Registers the given callback to be invoked when the `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo` of the target router changes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerRouteCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.RouteCallback,%20android.media.RouteDiscoveryPreference)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, routeCallback: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback, preference: https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference)` Registers a callback to discover routes and to receive events when they change. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerRouteListingPreferenceUpdatedCallback(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, routeListingPreferenceCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/media/RouteListingPreference!>)` Registers the given callback to be invoked when the `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` of the target router changes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerTransferCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.TransferCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.TransferCallback)` Registers a callback to get the result of `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#transferTo(android.media.MediaRoute2Info)`. |
| [MediaRouter2.ScanToken](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#requestScan(android.media.MediaRouter2.ScanRequest)(scanRequest: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanRequest)` Requests the system to actively scan for routes based on the router's `https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#setDeviceSuggestions(kotlin.collections.MutableList)(suggestedDeviceInfo: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo!>)` Sets a list of `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#setOnGetControllerHintsListener(android.media.MediaRouter2.OnGetControllerHintsListener)(listener: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.OnGetControllerHintsListener?)` Sets an `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.OnGetControllerHintsListener` to send hints when creating a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#setRouteListingPreference(android.media.RouteListingPreference)(routeListingPreference: https://developer.android.com/reference/kotlin/android/media/RouteListingPreference?)` Sets the `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` of the app associated to this media router. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#setRouteVolume(android.media.MediaRoute2Info,%20kotlin.Int)(route: https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info, volume: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the volume for a specific route. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#showSystemOutputSwitcher()()` Shows the system output switcher dialog. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#showSystemOutputSwitcher(android.media.session.MediaSession.Token)(sessionToken: https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token)` Shows the system output switcher dialog for a specific `https://developer.android.com/reference/kotlin/android/media/session/MediaSession`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#stop()()` Stops the current media routing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#transferTo(android.media.MediaRoute2Info)(route: https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info)` Transfers the current media to the given route. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#unregisterControllerCallback(android.media.MediaRouter2.ControllerCallback)(callback: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback)` Unregisters a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#unregisterDeviceSuggestionsUpdatesCallback(android.media.MediaRouter2.DeviceSuggestionsUpdatesCallback)(callback: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback)` Unregisters the given callback to not receive `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo` change events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#unregisterRouteCallback(android.media.MediaRouter2.RouteCallback)(routeCallback: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback)` Unregisters the given callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#unregisterRouteListingPreferenceUpdatedCallback(java.util.function.Consumer)(callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/media/RouteListingPreference!>)` Unregisters the given callback to not receive `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` change events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#unregisterTransferCallback(android.media.MediaRouter2.TransferCallback)(callback: https://developer.android.com/reference/kotlin/android/media/MediaRouter2.TransferCallback)` Unregisters the given callback. |

## Public methods

### cancelScanRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancelScanRequest(token: MediaRouter2.ScanToken): Unit
```

Releases the active scan request linked to the provided `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken`.

| Parameters ||
|---|---|
| `token` | [MediaRouter2.ScanToken](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken): `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken` of the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanRequest` to release. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the token does not match any active scan request. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#requestScan(android.media.MediaRouter2.ScanRequest)`

### clearDeviceSuggestions

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearDeviceSuggestions(): Unit
```

Clears the `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo` provided by this router.

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

Note: The list returned here will never be empty. The first element in the list is always the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getSystemController()`.

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#` | This value cannot be `null`. |

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

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerRouteCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.RouteCallback,%20android.media.RouteDiscoveryPreference)` ignores any `https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference` passed by a proxy router. Use android.media.RouteDiscoveryPreference#EMPTY when setting a route callback.

- Methods returning non-system `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` always return new instances with the latest data. Do not attempt to compare or store them. Instead, use `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getController(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getControllers()` to query the most up-to-date state.

- Calls to `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#setOnGetControllerHintsListener(android.media.MediaRouter2.OnGetControllerHintsListener)` are ignored.

Use this method when you only hold a revocable version of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` (e.g. acquired via the `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#`). Otherwise, use #getInstance(android.content.Context,java.lang.String).

`onInstanceInvalidatedListener` is called when the instance is invalidated because the calling app has lost `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` and does not hold `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String`. Do not use the invalidated instance after receiving this callback, as the system will ignore all operations. Call `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getInstance(android.content.Context,%20kotlin.String,%20java.util.concurrent.Executor,%20java.lang.Runnable)` again after reacquiring the relevant permissions. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): The `https://developer.android.com/reference/kotlin/android/content/Context.html#` of the caller. This value cannot be `null`. |
| `clientPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name of the app you want to control the routing of, or `"android"` to control the routing of the whole system. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke `onInstanceInvalidatedListener`. This value cannot be `null`. |
| `onInstanceInvalidatedListener` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#): Callback for when the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#` instance is invalidated due to lost permissions. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `clientPackageName` does not exist in the calling user. |

### getRouteListingPreference

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRouteListingPreference(): RouteListingPreference?
```

Returns the current `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` of the target router.

If this instance was created using `getInstance(Context, String)`, then it returns the last `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` set by the process this router was created for.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#setRouteListingPreference(android.media.RouteListingPreference)`

### getRoutes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRoutes(): MutableList<MediaRoute2Info!>
```

Gets the unmodifiable list of `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info` currently known to the media router.

Please note that the list can be changed before callbacks are invoked.

This method returns routes available to the routing framework that contain at least one of the `https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference#getPreferredFeatures()` registered by the application through `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerRouteCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.RouteCallback,%20android.media.RouteDiscoveryPreference)`. As a result, you need to register at least one `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback` (associated with the features that you are interested in), in order for this method to return a non-empty list.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info!>` | the list of routes that contains at least one of the route features in discovery preferences registered by the application. This value cannot be `null`. |

### getSystemController

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSystemController(): MediaRouter2.RoutingController
```

Gets a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` which can control the routes provided by system. e.g. Phone speaker, wired headset, Bluetooth, etc.

Note: The system controller can't be released. Calling `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController#release()` will be ignored.

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
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [MediaRouter2.ControllerCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#unregisterControllerCallback(android.media.MediaRouter2.ControllerCallback)`

### registerDeviceSuggestionsUpdatesCallback

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerDeviceSuggestionsUpdatesCallback(
    executor: Executor, 
    deviceSuggestionsUpdatesCallback: MediaRouter2.DeviceSuggestionsUpdatesCallback
): Unit
```

Registers the given callback to be invoked when the `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo` of the target router changes.

Calls using a previously registered callback will overwrite the previous executor.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `deviceSuggestionsUpdatesCallback` | [MediaRouter2.DeviceSuggestionsUpdatesCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback): This value cannot be `null`. |

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

Clients can register multiple callbacks, as long as the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback` instances are different. Each callback can provide a unique `https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference` and will only receive updates related to that set preference.

If the specified callback is already registered, its registration will be updated for the given `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` and `https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference`.

`https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getInstance(android.content.Context)` must register a route callback to register in the system and start receiving updates. Otherwise, all operations will be no-ops.

Any discovery preference passed by a #getInstance(android.content.Context,java.lang.String) will be ignored and will receive route updates based on the preference set by its matching local router.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `routeCallback` | [MediaRouter2.RouteCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback): This value cannot be `null`. |
| `preference` | [RouteDiscoveryPreference](https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference): This value cannot be `null`. |

### registerRouteListingPreferenceUpdatedCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerRouteListingPreferenceUpdatedCallback(
    executor: Executor, 
    routeListingPreferenceCallback: Consumer<RouteListingPreference!>
): Unit
```

Registers the given callback to be invoked when the `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` of the target router changes.

Calls using a previously registered callback will overwrite the previous executor.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `routeListingPreferenceCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [RouteListingPreference](https://developer.android.com/reference/kotlin/android/media/RouteListingPreference)!\>: This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#setRouteListingPreference(android.media.RouteListingPreference)`

### registerTransferCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerTransferCallback(
    executor: Executor, 
    callback: MediaRouter2.TransferCallback
): Unit
```

Registers a callback to get the result of `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#transferTo(android.media.MediaRoute2Info)`. If you register the same callback twice or more, it will be ignored.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor to execute the callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [MediaRouter2.TransferCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.TransferCallback): the callback to register. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#unregisterTransferCallback(android.media.MediaRouter2.TransferCallback)`

### requestScan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestScan(scanRequest: MediaRouter2.ScanRequest): MediaRouter2.ScanToken
```

Requests the system to actively scan for routes based on the router's `https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference`.

You must call `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#cancelScanRequest(android.media.MediaRouter2.ScanToken)` promptly to preserve system resources like battery. Avoid scanning unless there is clear intention from the user to start routing their media.

`scanRequest` specifies relevant scanning options, like whether the system should scan with the screen off. Screen off scanning requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String`.

Proxy routers use the registered `https://developer.android.com/reference/kotlin/android/media/RouteDiscoveryPreference` of their target routers.

| Parameters ||
|---|---|
| `scanRequest` | [MediaRouter2.ScanRequest](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanRequest): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken` | A unique `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanToken` that identifies the scan request. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanRequest` with `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ScanRequest.Builder#setScreenOffScan(kotlin.Boolean)` true is passed, while not holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String`. |

### setDeviceSuggestions

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDeviceSuggestions(suggestedDeviceInfo: MutableList<SuggestedDeviceInfo!>): Unit
```

Sets a list of `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo`.

Use this method to tell the system about device suggestions for the current router. The system may use these suggestions to populate system UI such as Output Switcher and media controls.

Suggestions will be expired automatically by the system, at which point you should call this method again if the suggestion is still relevant and should still be surfaced.

| Parameters ||
|---|---|
| `suggestedDeviceInfo` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SuggestedDeviceInfo](https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo)!\>: The `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo` the router suggests should be provided to the user. This value cannot be `null`. |

### setOnGetControllerHintsListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOnGetControllerHintsListener(listener: MediaRouter2.OnGetControllerHintsListener?): Unit
```

Sets an `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.OnGetControllerHintsListener` to send hints when creating a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController`. To send the hints, listener should be set *BEFORE* calling `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#transferTo(android.media.MediaRoute2Info)`.

| Parameters ||
|---|---|
| `listener` | [MediaRouter2.OnGetControllerHintsListener](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.OnGetControllerHintsListener)?: A listener to send optional app-specific hints when creating a controller. `null` for unset. |

### setRouteListingPreference

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRouteListingPreference(routeListingPreference: RouteListingPreference?): Unit
```

Sets the `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` of the app associated to this media router.

Use this method to inform the system UI of the routes that you would like to list for media routing, via the Output Switcher.

You should call this method before `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerRouteCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.RouteCallback,%20android.media.RouteDiscoveryPreference)` and immediately after receiving any `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback#onRoutesUpdated(kotlin.collections.MutableList)` in order to keep the system UI in a consistent state. You can also call this method at any other point to update the listing preference dynamically.

Calling this method on a proxy router instance will throw an `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

Notes:

1. You should not include the ids of two or more routes with a match in their `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getDeduplicationIds()`. If you do, the system will deduplicate them using its own criteria.
2. You can use this method to rank routes in the output switcher, placing the more important routes first. The system might override the proposed ranking.
3. You can use this method to avoid listing routes using dynamic criteria. For example, you can limit access to a specific type of device according to runtime criteria.

| Parameters ||
|---|---|
| `routeListingPreference` | [RouteListingPreference](https://developer.android.com/reference/kotlin/android/media/RouteListingPreference)?: The `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` for the system to use for route listing. When null, the system uses its default listing criteria. |

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

This method is only supported by #getInstance(android.content.Context,java.lang.String). Use `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController#setVolume(kotlin.Int)` instead for `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getInstance(android.content.Context)`.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_ROUTING_CONTROL:kotlin.String`

| Parameters ||
|---|---|
| `route` | [MediaRoute2Info](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info): This value cannot be `null`. |
| `volume` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new volume value between 0 and `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getVolumeMax()`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If called on a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getInstance(android.content.Context)`. |

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

Shows the system output switcher dialog for a specific `https://developer.android.com/reference/kotlin/android/media/session/MediaSession`.

The `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token` argument allows the system to identify which `https://developer.android.com/reference/kotlin/android/media/RoutingSessionInfo` to display as active. This is done via `https://developer.android.com/reference/kotlin/android/media/session/MediaSession#setPlaybackToRemote(android.media.VolumeProvider)` and `https://developer.android.com/reference/kotlin/android/media/VolumeProvider#getVolumeControlId()` when playing remotely, and `https://developer.android.com/reference/kotlin/android/media/session/MediaSession#setPlaybackToLocal(android.media.AudioAttributes)` when playing on this device.

This method is preferred over `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#showSystemOutputSwitcher()` to prevent the system from making wrong inferences about where playback is happening.

| Parameters ||
|---|---|
| `sessionToken` | [MediaSession.Token](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token): This value cannot be `null`. |

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

Stops the current media routing. If the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#getSystemController()` controls the media routing, this method is a no-op.

### transferTo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transferTo(route: MediaRoute2Info): Unit
```

Transfers the current media to the given route. If it's necessary a new `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController` is created or it is handled within the current routing controller.

| Parameters ||
|---|---|
| `route` | [MediaRoute2Info](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info): the route you want to transfer the current media to. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.TransferCallback#onTransfer(android.media.MediaRouter2.RoutingController,%20android.media.MediaRouter2.RoutingController)`
- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.TransferCallback#onTransferFailure(android.media.MediaRoute2Info)`

### unregisterControllerCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterControllerCallback(callback: MediaRouter2.ControllerCallback): Unit
```

Unregisters a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback`. The callback will no longer receive events. If the callback has not been added or been removed already, it is ignored.

| Parameters ||
|---|---|
| `callback` | [MediaRouter2.ControllerCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.ControllerCallback): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerControllerCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.ControllerCallback)`

### unregisterDeviceSuggestionsUpdatesCallback

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterDeviceSuggestionsUpdatesCallback(callback: MediaRouter2.DeviceSuggestionsUpdatesCallback): Unit
```

Unregisters the given callback to not receive `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo` change events.

| Parameters ||
|---|---|
| `callback` | [MediaRouter2.DeviceSuggestionsUpdatesCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerDeviceSuggestionsUpdatesCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.DeviceSuggestionsUpdatesCallback)`

### unregisterRouteCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterRouteCallback(routeCallback: MediaRouter2.RouteCallback): Unit
```

Unregisters the given callback. The callback will no longer receive events. If the callback has not been added or been removed already, it is ignored.

| Parameters ||
|---|---|
| `routeCallback` | [MediaRouter2.RouteCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RouteCallback): the callback to unregister. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerRouteCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.RouteCallback,%20android.media.RouteDiscoveryPreference)`

### unregisterRouteListingPreferenceUpdatedCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterRouteListingPreferenceUpdatedCallback(callback: Consumer<RouteListingPreference!>): Unit
```

Unregisters the given callback to not receive `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference` change events.

| Parameters ||
|---|---|
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [RouteListingPreference](https://developer.android.com/reference/kotlin/android/media/RouteListingPreference)!\>: This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerRouteListingPreferenceUpdatedCallback(java.util.concurrent.Executor,%20java.util.function.Consumer)`

### unregisterTransferCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterTransferCallback(callback: MediaRouter2.TransferCallback): Unit
```

Unregisters the given callback. The callback will no longer receive events. If the callback has not been added or been removed already, it is ignored.

| Parameters ||
|---|---|
| `callback` | [MediaRouter2.TransferCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.TransferCallback): the callback to unregister. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#registerTransferCallback(java.util.concurrent.Executor,%20android.media.MediaRouter2.TransferCallback)`
