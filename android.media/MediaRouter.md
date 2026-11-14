# MediaRouter

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaRouter

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaRouter "View this page in Java") 

```
open class MediaRouter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaRouter](https://developer.android.com/reference/kotlin/android/media/MediaRouter#) |

This API is not recommended for new applications. Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Media Router Library](https://developer.android.com/reference/androidx/mediarouter/media/package-summary.html) for consistent behavior across all devices.

MediaRouter allows applications to control the routing of media channels and streams from the current device to external speakers and destination devices.

A MediaRouter is retrieved through [Context.getSystemService()](https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String))of a [Context.MEDIA_ROUTER_SERVICE](https://developer.android.com/reference/kotlin/android/content/Context.html#MEDIA_ROUTER_SERVICE:kotlin.String).

This API is not thread-safe; all interactions with it must be done from the main thread of the process.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.Callback) Interface for receiving events about media routing changes. |
| open | [RouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory) Definition of a category of routes. |
| open | [RouteGroup](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteGroup) Information about a route that consists of multiple other routes in a group. |
| open | [RouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo) Information about a media route. |
| open | [SimpleCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.SimpleCallback) Stub implementation of [MediaRouter.Callback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.Callback). |
| open | [UserRouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.UserRouteInfo) Information about a route that the application may define and modify. |
| abstract | [VolumeCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.VolumeCallback) Interface for receiving events about volume changes. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALLBACK_FLAG_PERFORM_ACTIVE_SCAN](https://developer.android.com/reference/kotlin/android/media/MediaRouter#CALLBACK_FLAG_PERFORM_ACTIVE_SCAN:kotlin.Int) Flag for #addCallback: Actively scan for routes while this callback is registered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALLBACK_FLAG_UNFILTERED_EVENTS](https://developer.android.com/reference/kotlin/android/media/MediaRouter#CALLBACK_FLAG_UNFILTERED_EVENTS:kotlin.Int) Flag for #addCallback: Do not filter route events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUTE_TYPE_LIVE_AUDIO](https://developer.android.com/reference/kotlin/android/media/MediaRouter#ROUTE_TYPE_LIVE_AUDIO:kotlin.Int) Route type flag for live audio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUTE_TYPE_LIVE_VIDEO](https://developer.android.com/reference/kotlin/android/media/MediaRouter#ROUTE_TYPE_LIVE_VIDEO:kotlin.Int) Route type flag for live video. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROUTE_TYPE_USER](https://developer.android.com/reference/kotlin/android/media/MediaRouter#ROUTE_TYPE_USER:kotlin.Int) Route type flag for application-specific usage. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter#addCallback(kotlin.Int,%20android.media.MediaRouter.Callback))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cb:` ` [MediaRouter.Callback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.Callback)!`)` Add a callback to listen to events about specific kinds of media routes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter#addCallback(kotlin.Int,%20android.media.MediaRouter.Callback,%20kotlin.Int))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cb:` ` [MediaRouter.Callback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.Callback)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Add a callback to listen to events about specific kinds of media routes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addUserRoute](https://developer.android.com/reference/kotlin/android/media/MediaRouter#addUserRoute(android.media.MediaRouter.UserRouteInfo))`(`info:` ` [MediaRouter.UserRouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.UserRouteInfo)!`)` Add an app-specified route for media to the MediaRouter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearUserRoutes](https://developer.android.com/reference/kotlin/android/media/MediaRouter#clearUserRoutes())`()` Remove all app-specified routes from the MediaRouter. |
| open [MediaRouter.RouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory)! | [createRouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter#createRouteCategory(kotlin.Int,%20kotlin.Boolean))`(`nameResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isGroupable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a new route category. |
| open [MediaRouter.RouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory)! | [createRouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter#createRouteCategory(kotlin.CharSequence,%20kotlin.Boolean))`(`name:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `isGroupable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a new route category. |
| open [MediaRouter.UserRouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.UserRouteInfo)! | [createUserRoute](https://developer.android.com/reference/kotlin/android/media/MediaRouter#createUserRoute(android.media.MediaRouter.RouteCategory))`(`category:` ` [MediaRouter.RouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory)!`)` Create a new user route that may be modified and registered for use by the application. |
| open [MediaRouter.RouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory)! | [getCategoryAt](https://developer.android.com/reference/kotlin/android/media/MediaRouter#getCategoryAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the [category](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory) at the given index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCategoryCount](https://developer.android.com/reference/kotlin/android/media/MediaRouter#getCategoryCount())`()` Return the number of [categories](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory) currently represented by routes known to this MediaRouter. |
| open [MediaRouter.RouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo)! | [getDefaultRoute](https://developer.android.com/reference/kotlin/android/media/MediaRouter#getDefaultRoute())`()` Gets the default route for playing media content on the system. |
| open [MediaRouter.RouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo)! | [getRouteAt](https://developer.android.com/reference/kotlin/android/media/MediaRouter#getRouteAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the route at the specified index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRouteCount](https://developer.android.com/reference/kotlin/android/media/MediaRouter#getRouteCount())`()` Return the number of [routes](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo) currently known to this MediaRouter. |
| open [MediaRouter.RouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo)! | [getSelectedRoute](https://developer.android.com/reference/kotlin/android/media/MediaRouter#getSelectedRoute(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the currently selected route for any of the given types |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter#removeCallback(android.media.MediaRouter.Callback))`(`cb:` ` [MediaRouter.Callback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.Callback)!`)` Remove the specified callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeUserRoute](https://developer.android.com/reference/kotlin/android/media/MediaRouter#removeUserRoute(android.media.MediaRouter.UserRouteInfo))`(`info:` ` [MediaRouter.UserRouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.UserRouteInfo)!`)` Remove an app-specified route for media from the MediaRouter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [selectRoute](https://developer.android.com/reference/kotlin/android/media/MediaRouter#selectRoute(kotlin.Int,%20android.media.MediaRouter.RouteInfo))`(`types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `route:` ` [MediaRouter.RouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo)`)` Select the specified route to use for output of the given media types. |

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

A device that supports live video routing will allow a mirrored version of the device's primary display or a customized [Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation.html#) to be routed to supported destinations.

Once initiated, display mirroring is transparent to the application. While remote routing is active the application may use a [Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation.html#) to replace the mirrored view on the external display with different content. 

 Value: 2

**See Also**

- [android.media.MediaRouter.RouteInfo#getPresentationDisplay()](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo#getPresentationDisplay())
- [android.app.Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation.html#) 

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

This is a convenience method that has the same effect as calling [addCallback(int,android.media.MediaRouter.Callback,int)](https://developer.android.com/reference/kotlin/android/media/MediaRouter#addCallback(kotlin.Int,%20android.media.MediaRouter.Callback,%20kotlin.Int))without flags.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Types of routes this callback is interested in |
| `cb` | [MediaRouter.Callback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.Callback)!:Callback to add |

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

By default, the callback will only be invoked for events that affect routes that match the specified selector. The filtering may be disabled by specifying the [CALLBACK_FLAG_UNFILTERED_EVENTS](https://developer.android.com/reference/kotlin/android/media/MediaRouter#CALLBACK_FLAG_UNFILTERED_EVENTS:kotlin.Int) flag.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Types of routes this callback is interested in |
| `cb` | [MediaRouter.Callback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.Callback)!:Callback to add |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags to control the behavior of the callback. May be zero or a combination of [CALLBACK_FLAG_PERFORM_ACTIVE_SCAN](https://developer.android.com/reference/kotlin/android/media/MediaRouter#CALLBACK_FLAG_PERFORM_ACTIVE_SCAN:kotlin.Int) and [CALLBACK_FLAG_UNFILTERED_EVENTS](https://developer.android.com/reference/kotlin/android/media/MediaRouter#CALLBACK_FLAG_UNFILTERED_EVENTS:kotlin.Int). |

### addUserRoute

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addUserRoute(info: MediaRouter.UserRouteInfo!): Unit
```

Add an app-specified route for media to the MediaRouter. App-specified route definitions are created using [createUserRoute(android.media.MediaRouter.RouteCategory)](https://developer.android.com/reference/kotlin/android/media/MediaRouter#createUserRoute(android.media.MediaRouter.RouteCategory))

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [MediaRouter.UserRouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.UserRouteInfo)!:Definition of the route to add |

**See Also**

- [#createUserRoute(RouteCategory)](https://developer.android.com/reference/kotlin/android/media/MediaRouter#createUserRoute(android.media.MediaRouter.RouteCategory))
- [#removeUserRoute(UserRouteInfo)](https://developer.android.com/reference/kotlin/android/media/MediaRouter#removeUserRoute(android.media.MediaRouter.UserRouteInfo)) 

### clearUserRoutes

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearUserRoutes(): Unit
```

Remove all app-specified routes from the MediaRouter. 
**See Also**

- [#removeUserRoute(UserRouteInfo)](https://developer.android.com/reference/kotlin/android/media/MediaRouter#removeUserRoute(android.media.MediaRouter.UserRouteInfo)) 

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
| [MediaRouter.RouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory)! | the new RouteCategory |

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
| [MediaRouter.RouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory)! | the new RouteCategory |

### createUserRoute

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createUserRoute(category: MediaRouter.RouteCategory!): MediaRouter.UserRouteInfo!
```

Create a new user route that may be modified and registered for use by the application.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `category` | [MediaRouter.RouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory)!:The category the new route will belong to |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MediaRouter.UserRouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.UserRouteInfo)! | A new UserRouteInfo for use by the application |

**See Also**

- [#addUserRoute(UserRouteInfo)](https://developer.android.com/reference/kotlin/android/media/MediaRouter#addUserRoute(android.media.MediaRouter.UserRouteInfo))
- [#removeUserRoute(UserRouteInfo)](https://developer.android.com/reference/kotlin/android/media/MediaRouter#removeUserRoute(android.media.MediaRouter.UserRouteInfo))
- [#createRouteCategory(CharSequence, boolean)](https://developer.android.com/reference/kotlin/android/media/MediaRouter#createRouteCategory(kotlin.CharSequence,%20kotlin.Boolean)) 

### getCategoryAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCategoryAt(index: Int): MediaRouter.RouteCategory!
```

Return the [category](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory) at the given index. Valid indices are in the range \[0-getCategoryCount).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):which category to return |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------|
| [MediaRouter.RouteCategory](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory)! | the category at index |

### getCategoryCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCategoryCount(): Int
```

Return the number of [categories](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteCategory) currently represented by routes known to this MediaRouter.

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
| [MediaRouter.RouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo)! | The default route, which is guaranteed to never be null. |

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
| [MediaRouter.RouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo)! | the route at index |

### getRouteCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRouteCount(): Int
```

Return the number of [routes](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo) currently known to this MediaRouter.

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
| [MediaRouter.RouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo)! | the selected route |

### removeCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeCallback(cb: MediaRouter.Callback!): Unit
```

Remove the specified callback. It will no longer receive events about media routing.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [MediaRouter.Callback](https://developer.android.com/reference/kotlin/android/media/MediaRouter.Callback)!:Callback to remove |

### removeUserRoute

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeUserRoute(info: MediaRouter.UserRouteInfo!): Unit
```

Remove an app-specified route for media from the MediaRouter.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [MediaRouter.UserRouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.UserRouteInfo)!:Definition of the route to remove |

**See Also**

- [#addUserRoute(UserRouteInfo)](https://developer.android.com/reference/kotlin/android/media/MediaRouter#addUserRoute(android.media.MediaRouter.UserRouteInfo)) 

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
| `route` | [MediaRouter.RouteInfo](https://developer.android.com/reference/kotlin/android/media/MediaRouter.RouteInfo):Route to select This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------|
| `java.lang.IllegalArgumentException` | if the given route is`null` |
