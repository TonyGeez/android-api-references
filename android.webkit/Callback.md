# GeolocationPermissions.Callback

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](https://developer.android.com/reference/android/webkit/GeolocationPermissions.Callback "View this page in Java") 

```
interface Callback
```

| [android.webkit.GeolocationPermissions.Callback](https://developer.android.com/reference/kotlin/android/webkit/GeolocationPermissions.Callback#) |

A callback interface used by the host application to set the Geolocation permission state for an origin.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invoke](https://developer.android.com/reference/kotlin/android/webkit/GeolocationPermissions.Callback#invoke(kotlin.String,%20kotlin.Boolean,%20kotlin.Boolean))`(`origin:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `retain:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the Geolocation permission state for the supplied origin. |

## Public methods

### invoke

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun invoke(
    origin: String!, 
    allow: Boolean, 
    retain: Boolean
): Unit
```

Sets the Geolocation permission state for the supplied origin.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `origin` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the origin for which permissions are set |
| `allow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not the origin should be allowed to use the Geolocation API |
| `retain` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the permission should be retained beyond the lifetime of a page currently being displayed by a WebView |
