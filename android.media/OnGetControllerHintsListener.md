Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGetControllerHintsListener

Kotlin | [Java](../android/media/MediaRouter2.OnGetControllerHintsListener.md)
| --- | --- |

```
interface OnGetControllerHintsListener
```

| [android.media.MediaRouter2.OnGetControllerHintsListener](../android/media/MediaRouter2.OnGetControllerHintsListener.md) |

A listener interface to send optional app-specific hints when creating a `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController`.

## Summary

| Public methods ||
|---|---|
| abstract [Bundle](../android.os/Bundle.md)? | `https://developer.android.com/reference/kotlin/android/media/MediaRouter2.OnGetControllerHintsListener#onGetControllerHints(android.media.MediaRoute2Info)(route: https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info)` Called when the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2` or the system is about to request a media route provider service to create a controller with the given route. |

## Public methods

### onGetControllerHints

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onGetControllerHints(route: MediaRoute2Info): Bundle?
```

Called when the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2` or the system is about to request a media route provider service to create a controller with the given route. The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` returned here will be sent to media route provider service as a hint.

Since controller creation can be requested by the `https://developer.android.com/reference/kotlin/android/media/MediaRouter2` and the system, set the listener as soon as possible after acquiring `https://developer.android.com/reference/kotlin/android/media/MediaRouter2` instance. The method will be called on the same thread that calls `https://developer.android.com/reference/kotlin/android/media/MediaRouter2#transferTo(android.media.MediaRoute2Info)` or the main thread if it is requested by the system.

| Parameters ||
|---|---|
| `route` | [MediaRoute2Info](MediaRoute2Info.md): the route to create a controller with. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | An optional bundle of app-specific arguments to send to the provider, or `null` if none. The contents of this bundle may affect the result of controller creation. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRoute2ProviderService#onCreateSession(kotlin.Long,%20kotlin.String,%20kotlin.String,%20android.os.Bundle)`
