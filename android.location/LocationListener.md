Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocationListener

Kotlin | [Java](../android/location/LocationListener.md)
| --- | --- |

```
interface LocationListener
```

| [android.location.LocationListener](../android/location/LocationListener.md) |

Used for receiving notifications when the device location has changed. These methods are called when the listener has been registered with the LocationManager.
|
| ### Developer Guides
|
| For more information about identifying user location, read the [Obtaining User Location](https://developer.android.com/guide/topics/location/obtaining-user-location.html) developer guide.

<br />

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationListener#onFlushComplete(kotlin.Int)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Invoked when a flush operation is complete and after flushed locations have been delivered. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationListener#onLocationChanged(android.location.Location)(location: https://developer.android.com/reference/kotlin/android/location/Location)` Called when the location has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationListener#onLocationChanged(kotlin.collections.MutableList)(locations: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/location/Location!>)` Called when the location has changed and locations are being delivered in batches. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationListener#onProviderDisabled(kotlin.String)(provider: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Called when the provider this listener is registered with becomes disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationListener#onProviderEnabled(kotlin.String)(provider: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Called when a provider this listener is registered with becomes enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/location/LocationListener#onStatusChanged(kotlin.String,%20kotlin.Int,%20android.os.Bundle)(provider: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` This callback will never be invoked on Android Q and above, and providers can be considered as always in the `https://developer.android.com/reference/kotlin/android/location/LocationProvider#AVAILABLE:kotlin.Int` state. |
| --- | --- |

## Public methods

### onFlushComplete

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFlushComplete(requestCode: Int): Unit
```

Invoked when a flush operation is complete and after flushed locations have been delivered.

| Parameters ||
|---|---|
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the request code passed into `https://developer.android.com/reference/kotlin/android/location/LocationManager#requestFlush(kotlin.String,%20android.location.LocationListener,%20kotlin.Int)` |

### onLocationChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onLocationChanged(location: Location): Unit
```

Called when the location has changed. A wakelock may be held on behalf on the listener for some brief amount of time as this callback executes. If this callback performs long running operations, it is the client's responsibility to obtain their own wakelock if necessary.

| Parameters ||
|---|---|
| `location` | [Location](../android/location/Location.md): the updated location. This value cannot be `null`. |

### onLocationChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onLocationChanged(locations: MutableList<Location!>): Unit
```

Called when the location has changed and locations are being delivered in batches. The default implementation calls through to `https://developer.android.com/reference/kotlin/android/location/LocationListener#onLocationChanged(android.location.Location)` with all locations in the batch. The list of locations is always guaranteed to be non-empty, and is always guaranteed to be ordered from earliest location to latest location (so that the earliest location in the batch is at index 0 in the list, and the latest location in the batch is at index size-1 in the list).

| Parameters ||
|---|---|
| `locations` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Location](../android/location/Location.md)!\>: the location list. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/location/LocationRequest#getMaxUpdateDelayMillis()`

### onProviderDisabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProviderDisabled(provider: String): Unit
```

Called when the provider this listener is registered with becomes disabled. If a provider is disabled when this listener is registered, this callback will be invoked immediately.

Note that this method only has a default implementation on Android R and above, and this method must still be overridden in order to run successfully on Android versions below R. LocationListenerCompat from the compat libraries may be used to avoid the need to override for older platforms.

| Parameters ||
|---|---|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the location provider. This value cannot be `null`. |

### onProviderEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProviderEnabled(provider: String): Unit
```

Called when a provider this listener is registered with becomes enabled.

Note that this method only has a default implementation on Android R and above, and this method must still be overridden in order to run successfully on Android versions below R. LocationListenerCompat from the compat libraries may be used to avoid the need to override for older platforms.

| Parameters ||
|---|---|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the location provider. This value cannot be `null`. |

### onStatusChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStatusChanged(
    provider: String!, 
    status: Int, 
    extras: Bundle!
): Unit
```

**Deprecated:** *This callback will never be invoked on Android Q and above.*

This callback will never be invoked on Android Q and above, and providers can be considered as always in the `https://developer.android.com/reference/kotlin/android/location/LocationProvider#AVAILABLE:kotlin.Int` state.

Note that this method only has a default implementation on Android R and above, and this method must still be overridden in order to run successfully on Android versions below R. LocationListenerCompat from the compat libraries may be used to avoid the need to override for older platforms.
