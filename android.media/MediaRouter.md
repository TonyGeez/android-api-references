# MediaRouter

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaRouter

Kotlin| [Java](../android/media/MediaRouter.md) 
| --- | --- |

```
open class MediaRouter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaRouter](../android/media/MediaRouter.md) |

This API is not recommended for new applications. Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Media Router Library](../androidx/mediarouter/media/_package.md) for consistent behavior across all devices.

MediaRouter allows applications to control the routing of media channels and streams from the current device to external speakers and destination devices.

A MediaRouter is retrieved through [Context.getSystemService()](../android/content/Context.md))of a [Context.MEDIA_ROUTER_SERVICE](../android/content/Context.md).

This API is not thread-safe; all interactions with it must be done from the main thread of the process.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/media/MediaRouter.Callback.md) Interface for receiving events about media routing changes. |
| open | [RouteCategory](../android/media/MediaRouter.RouteCategory.md) Definition of a category of routes. |
| open | [RouteGroup](../android/media/MediaRouter.RouteGroup.md) Information about a route that consists of multiple other routes in a group. |
| --- | --- |
| open | [RouteInfo](../android/media/MediaRouter.RouteInfo.md) Information about a media route. |
| open | [SimpleCallback](../android/media/MediaRouter.SimpleCallback.md) Stub implementation of [MediaRouter.Callback](../android/media/MediaRouter.Callback.md). |
| open | [UserRouteInfo](../android/media/MediaRouter.UserRouteInfo.md) Information about a route that the application may define and modify. |
| --- | --- |
| abstract | [VolumeCallback](../android/media/MediaRouter.VolumeCallback.md) Interface for receiving events about volume changes. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALLBACK_FLAG_PERFORM_ACTIVE_SCAN](../android/media/MediaRouter.md) Flag for #addCallback: Actively scan for routes while this callback is registered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALLBACK_FLAG_UNFILTERED_EVENTS](../android/media/MediaRouter.md) Flag for #addCallback: Do not filter route events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUTE_TYPE_LIVE_AUDIO](../android/media/MediaRouter.md) Route type flag for live audio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUTE_TYPE_LIVE_VIDEO](../android/media/MediaRouter.md) Route type flag for live video. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUTE_TYPE_USER](../android/media/MediaRouter.md) Route type flag for application-specific usage. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCallback](../android/media/MediaRouter.md))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cb:` ` [MediaRouter.Callback](../android/media/MediaRouter.Callback.md)!`)` Add a callback to listen to events about specific kinds of media routes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCallback](../android/media/MediaRouter.md))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cb:` ` [MediaRouter.Callback](../android/media/MediaRouter.Callback.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Add a callback to listen to events about specific kinds of media routes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addUserRoute](../android/media/MediaRouter.md))`(`info:` ` [MediaRouter.UserRouteInfo](../android/media/MediaRouter.UserRouteInfo.md)!`)` Add an app-specified route for media to the MediaRouter. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearUserRoutes](../android/media/MediaRouter.md))`()` Remove all app-specified routes from the MediaRouter. |
| open [MediaRouter.RouteCategory](../android/media/MediaRouter.RouteCategory.md)! | [createRouteCategory](../android/media/MediaRouter.md))`(`nameResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isGroupable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a new route category. |
| open [MediaRouter.RouteCategory](../android/media/MediaRouter.RouteCategory.md)! | [createRouteCategory](../android/media/MediaRouter.md))`(`name:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `isGroupable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a new route category. |
| --- | --- |
| open [MediaRouter.UserRouteInfo](../android/media/MediaRouter.UserRouteInfo.md)! | [createUserRoute](../android/media/MediaRouter.md))`(`category:` ` [MediaRouter.RouteCategory](../android/media/MediaRouter.RouteCategory.md)!`)` Create a new user route that may be modified and registered for use by the application. |
| open [MediaRouter.RouteCategory](../android/media/MediaRouter.RouteCategory.md)! | [getCategoryAt](../android/media/MediaRouter.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the [category](../android/media/MediaRouter.RouteCategory.md) at the given index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCategoryCount](../android/media/MediaRouter.md))`()` Return the number of [categories](../android/media/MediaRouter.RouteCategory.md) currently represented by routes known to this MediaRouter. |
| --- | --- |
| open [MediaRouter.RouteInfo](../android/media/MediaRouter.RouteInfo.md)! | [getDefaultRoute](../android/media/MediaRouter.md))`()` Gets the default route for playing media content on the system. |
| open [MediaRouter.RouteInfo](../android/media/MediaRouter.RouteInfo.md)! | [getRouteAt](../android/media/MediaRouter.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the route at the specified index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRouteCount](../android/media/MediaRouter.md))`()` Return the number of [routes](../android/media/MediaRouter.RouteInfo.md) currently known to this MediaRouter. |
| --- | --- |
| open [MediaRouter.RouteInfo](../android/media/MediaRouter.RouteInfo.md)! | [getSelectedRoute](../android/media/MediaRouter.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the currently selected route for any of the given types |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallback](../android/media/MediaRouter.md))`(`cb:` ` [MediaRouter.Callback](../android/media/MediaRouter.Callback.md)!`)` Remove the specified callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeUserRoute](../android/media/MediaRouter.md))`(`info:` ` [MediaRouter.UserRouteInfo](../android/media/MediaRouter.UserRouteInfo.md)!`)` Remove an app-specified route for media from the MediaRouter. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [selectRoute](../android/media/MediaRouter.md))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `route:` ` [MediaRouter.RouteInfo](../android/media/MediaRouter.RouteInfo.md)`)` Select the specified route to use for output of the given media types. |

## Constants

### CALLBACK_FLAG_PERFORM_ACTIVE_SCAN

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALLBACK_FLAG_PERFORM_ACTIVE_SCAN: Int
```

Flag for #addCallback: Actively scan for routes while this callback is registered.

When this flag is specified, the media router will actively scan for new routes. Certain routes, such as wifi display routes, may not be discoverable except when actively scanning. This flag is typically used when the route picker dialog has been opened by the user to ensure that the route information is up to date.

Active scanning may consume a significant amount of power and may have intrusive effects on wireless connectivity. Therefore it is important that active scanning only be requested when it is actually needed to satisfy a user request to discover and select a new route. 

 Value: 1

### CALLBACK_FLAG_UNFILTERED_EVENTS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALLBACK_FLAG_UNFILTERED_EVENTS: Int
```

Flag for #addCallback: Do not filter route events.

When this flag is specified, the callback will be invoked for event that affect any route even if they do not match the callback's filter. 

 Value: 2

### ROUTE_TYPE_LIVE_AUDIO

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUTE_TYPE_LIVE_AUDIO: Int
```

Route type flag for live audio.

A device that supports live audio routing will allow the media audio stream to be routed to supported destinations. This can include internal speakers or audio jacks on the device itself, A2DP devices, and more.

Once initiated this routing is transparent to the application. All audio played on the media stream will be routed to the selected destination. 

 Value: 1

### ROUTE_TYPE_LIVE_VIDEO

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUTE_TYPE_LIVE_VIDEO: Int
```

Route type flag for live video.

A device that supports live video routing will allow a mirrored version of the device's primary display or a customized [Presentation](../android/app/Presentation.md) to be routed to supported destinations.

Once initiated, display mirroring is transparent to the application. While remote routing is active the application may use a [Presentation](../android/app/Presentation.md) to replace the mirrored view on the external display with different content. 

 Value: 2

**See Also**

- [android.media.MediaRouter.RouteInfo#getPresentationDisplay()](../android/media/MediaRouter.RouteInfo.md))
- [android.app.Presentation](../android/app/Presentation.md) 

### ROUTE_TYPE_USER

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROUTE_TYPE_USER: Int
```

Route type flag for application-specific usage.

Unlike other media route types, user routes are managed by the application. The MediaRouter will manage and dispatch events for user routes, but the application is expected to interpret the meaning of these events and perform the requested routing tasks. 

 Value: 8388608

## Public methods

### addCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCallback(
    types: Int, 
    cb: MediaRouter.Callback!
): Unit
```

Add a callback to listen to events about specific kinds of media routes. If the specified callback is already registered, its registration will be updated for any additional route types specified.

This is a convenience method that has the same effect as calling [addCallback(int,android.media.MediaRouter.Callback,int)](../android/media/MediaRouter.md))without flags.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Types of routes this callback is interested in |
| `cb` | [MediaRouter.Callback](../android/media/MediaRouter.Callback.md)!:Callback to add |

### addCallback

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCallback(
    types: Int, 
    cb: MediaRouter.Callback!, 
    flags: Int
): Unit
```

Add a callback to listen to events about specific kinds of media routes. If the specified callback is already registered, its registration will be updated for any additional route types specified.

By default, the callback will only be invoked for events that affect routes that match the specified selector. The filtering may be disabled by specifying the [CALLBACK_FLAG_UNFILTERED_EVENTS](../android/media/MediaRouter.md) flag.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Types of routes this callback is interested in |
| `cb` | [MediaRouter.Callback](../android/media/MediaRouter.Callback.md)!:Callback to add |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags to control the behavior of the callback. May be zero or a combination of [CALLBACK_FLAG_PERFORM_ACTIVE_SCAN](../android/media/MediaRouter.md) and [CALLBACK_FLAG_UNFILTERED_EVENTS](../android/media/MediaRouter.md). |
| --- | --- |

### addUserRoute

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addUserRoute(info: MediaRouter.UserRouteInfo!): Unit
```

Add an app-specified route for media to the MediaRouter. App-specified route definitions are created using [createUserRoute(android.media.MediaRouter.RouteCategory)](../android/media/MediaRouter.md))

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [MediaRouter.UserRouteInfo](../android/media/MediaRouter.UserRouteInfo.md)!:Definition of the route to add |

**See Also**

- [#createUserRoute(RouteCategory)](../android/media/MediaRouter.md))
- [#removeUserRoute(UserRouteInfo)](../android/media/MediaRouter.md)) 

### clearUserRoutes

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearUserRoutes(): Unit
```

Remove all app-specified routes from the MediaRouter. 
**See Also**

- [#removeUserRoute(UserRouteInfo)](../android/media/MediaRouter.md)) 

### createRouteCategory

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createRouteCategory(
    nameResId: Int, 
    isGroupable: Boolean
): MediaRouter.RouteCategory!
```

Create a new route category. Each route must belong to a category.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `nameResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource ID of the name of the new category |
| `isGroupable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if routes in this category may be grouped with one another |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------|
| [MediaRouter.RouteCategory](../android/media/MediaRouter.RouteCategory.md)! | the new RouteCategory |

### createRouteCategory

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createRouteCategory(
    name: CharSequence!, 
    isGroupable: Boolean
): MediaRouter.RouteCategory!
```

Create a new route category. Each route must belong to a category.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:Name of the new category |
| `isGroupable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if routes in this category may be grouped with one another |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------|
| [MediaRouter.RouteCategory](../android/media/MediaRouter.RouteCategory.md)! | the new RouteCategory |

### createUserRoute

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createUserRoute(category: MediaRouter.RouteCategory!): MediaRouter.UserRouteInfo!
```

Create a new user route that may be modified and registered for use by the application.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `category` | [MediaRouter.RouteCategory](../android/media/MediaRouter.RouteCategory.md)!:The category the new route will belong to |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MediaRouter.UserRouteInfo](../android/media/MediaRouter.UserRouteInfo.md)! | A new UserRouteInfo for use by the application |

**See Also**

- [#addUserRoute(UserRouteInfo)](../android/media/MediaRouter.md))
- [#removeUserRoute(UserRouteInfo)](../android/media/MediaRouter.md))
- [#createRouteCategory(CharSequence, boolean)](../android/media/MediaRouter.md)) 

### getCategoryAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCategoryAt(index: Int): MediaRouter.RouteCategory!
```

Return the [category](../android/media/MediaRouter.RouteCategory.md) at the given index. Valid indices are in the range \[0-getCategoryCount).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):which category to return |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------|
| [MediaRouter.RouteCategory](../android/media/MediaRouter.RouteCategory.md)! | the category at index |

### getCategoryCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCategoryCount(): Int
```

Return the number of [categories](../android/media/MediaRouter.RouteCategory.md) currently represented by routes known to this MediaRouter.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of unique categories represented by this MediaRouter's known routes |

### getDefaultRoute

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultRoute(): MediaRouter.RouteInfo!
```

Gets the default route for playing media content on the system.

The system always provides a default route.

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MediaRouter.RouteInfo](../android/media/MediaRouter.RouteInfo.md)! | The default route, which is guaranteed to never be null. |

### getRouteAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRouteAt(index: Int): MediaRouter.RouteInfo!
```

Return the route at the specified index.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the route to return |

| Return ||
|--------------------------------------------------------------------------------------------------------------|--------------------|
| [MediaRouter.RouteInfo](../android/media/MediaRouter.RouteInfo.md)! | the route at index |

### getRouteCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRouteCount(): Int
```

Return the number of [routes](../android/media/MediaRouter.RouteInfo.md) currently known to this MediaRouter.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of routes tracked by this router |

### getSelectedRoute

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectedRoute(type: Int): MediaRouter.RouteInfo!
```

Return the currently selected route for any of the given types

| Parameters ||
|--------|----------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):route types |

| Return ||
|--------------------------------------------------------------------------------------------------------------|--------------------|
| [MediaRouter.RouteInfo](../android/media/MediaRouter.RouteInfo.md)! | the selected route |

### removeCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeCallback(cb: MediaRouter.Callback!): Unit
```

Remove the specified callback. It will no longer receive events about media routing.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [MediaRouter.Callback](../android/media/MediaRouter.Callback.md)!:Callback to remove |

### removeUserRoute

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeUserRoute(info: MediaRouter.UserRouteInfo!): Unit
```

Remove an app-specified route for media from the MediaRouter.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [MediaRouter.UserRouteInfo](../android/media/MediaRouter.UserRouteInfo.md)!:Definition of the route to remove |

**See Also**

- [#addUserRoute(UserRouteInfo)](../android/media/MediaRouter.md)) 

### selectRoute

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun selectRoute(
    types: Int, 
    route: MediaRouter.RouteInfo
): Unit
```

Select the specified route to use for output of the given media types.

As API version 18, this function may be used to select any route. In prior versions, this function could only be used to select user routes and would ignore any attempt to select a system route.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):type flags indicating which types this route should be used for. The route must support at least a subset. |
| `route` | [MediaRouter.RouteInfo](../android/media/MediaRouter.RouteInfo.md):Route to select This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------|
| `java.lang.IllegalArgumentException` | if the given route is`null` |
