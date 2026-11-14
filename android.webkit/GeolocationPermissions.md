Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GeolocationPermissions

```
open class GeolocationPermissions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.GeolocationPermissions](GeolocationPermissions.md) |

This class is used to manage permissions for the WebView's Geolocation JavaScript API. Geolocation permissions are applied to an origin, which consists of the host, scheme and port of a URI. In order for web content to use the Geolocation API, permission must be granted for that content's origin. This class stores Geolocation permissions. An origin's permission state can be either allowed or denied. This class uses Strings to represent an origin. When an origin attempts to use the Geolocation API, but no permission state is currently set for that origin, onGeolocationPermissionsShowPrompt is called. This allows the permission state to be set for that origin. The methods of this class can be used to modify and interrogate the stored Geolocation permissions at any time.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/webkit/GeolocationPermissions.Callback` A callback interface used by the host application to set the Geolocation permission state for an origin. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | allow Allows the specified origin to use the Geolocation API. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clear Clears the Geolocation permission state for the specified origin. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearAll Clears the Geolocation permission state for all origins. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getAllowed Gets the Geolocation permission state for the specified origin. |
| open static [GeolocationPermissions](GeolocationPermissions.md)! | getInstance Gets the singleton instance of this class. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getOrigins Gets the set of origins for which Geolocation permissions are stored. |
| --- | --- |

## Public methods

### allow

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun allow(origin: String!): Unit
```

Allows the specified origin to use the Geolocation API.

| Parameters ||
|---|---|
| `origin` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the origin for which Geolocation API use is allowed |

### clear

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(origin: String!): Unit
```

Clears the Geolocation permission state for the specified origin.

| Parameters ||
|---|---|
| `origin` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the origin for which Geolocation permissions are cleared |

### clearAll

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearAll(): Unit
```

Clears the Geolocation permission state for all origins.

### getAllowed

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowed(
    origin: String!, 
    callback: ValueCallback<Boolean!>!
): Unit
```

Gets the Geolocation permission state for the specified origin.

| Parameters ||
|---|---|
| `origin` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the origin for which Geolocation permission is requested |
| `callback` | [ValueCallback](ValueCallback.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>!: a ValueCallback to receive the result of this request. This object's onReceiveValue method will be invoked asynchronously with a boolean indicating whether or not the origin can use the Geolocation API. |

### getInstance

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): GeolocationPermissions!
```

Gets the singleton instance of this class. This method cannot be called before the application instantiates a WebView instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/webkit/GeolocationPermissions#!` | the singleton GeolocationPermissions instance |

### getOrigins

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOrigins(callback: ValueCallback<MutableSet<String!>!>!): Unit
```

Gets the set of origins for which Geolocation permissions are stored.

| Parameters ||
|---|---|
| `callback` | [ValueCallback](ValueCallback.md)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!: a ValueCallback to receive the result of this request. This object's onReceiveValue method will be invoked asynchronously with a set of Strings containing the origins for which Geolocation permissions are stored. |
