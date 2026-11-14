# Geocoder.GeocodeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GeocodeListener

Kotlin| [Java](../android/location/Geocoder.GeocodeListener.md) 
| --- | --- |

```
interface GeocodeListener
```

| [android.location.Geocoder.GeocodeListener](../android/location/Geocoder.GeocodeListener.md) |

A listener for asynchronous geocoding results. Only one of the methods will ever be invoked per geocoding attempt. There are no guarantees on how long it will take for a method to be invoked, nor any guarantees on the format or availability of error information.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](../android/location/Geocoder.GeocodeListener.md))`(`errorMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Invoked when geocoding fails, with an optional error message. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGeocode](../android/location/Geocoder.GeocodeListener.md))`(`addresses:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Address](../android/location/Address.md)!>`)` Invoked when geocoding completes successfully. |

## Public methods

### onError

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(errorMessage: String?): Unit
```

Invoked when geocoding fails, with an optional error message.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------|
| `errorMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

### onGeocode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGeocode(addresses: MutableList<Address!>): Unit
```

Invoked when geocoding completes successfully. May return an empty list.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `addresses` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Address](../android/location/Address.md)!\>:This value cannot be`null`. |
