Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SdkExtensions

Kotlin | [Java](SdkExtensions.md)
| --- | --- |

```
open class SdkExtensions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.ext.SdkExtensions](SdkExtensions.md) |

Methods for interacting with the extension SDK.

This class provides information about the extension SDK versions present on this device. Use the getExtensionVersion method to lookup the version of a given extension.

The extension version advances as the platform evolves and new APIs are added, so is suitable to use for determining API availability at runtime.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ext/SdkExtensions#AD_SERVICES:kotlin.Int` <br /> |

| Public methods ||
|---|---|
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | getAllExtensionVersions Return all extension versions that exist on this device. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getExtensionVersion Return the version of the specified extensions. |

## Constants

### AD_SERVICES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 4](https://developer.android.com/sdkExtensions)

```
static val AD_SERVICES: Int
```

 Value: 1000000

## Public methods

### getAllExtensionVersions

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAllExtensionVersions(): MutableMap<Int!, Int!>
```

Return all extension versions that exist on this device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | a map from extension to extension version. This value cannot be `null`. |

### getExtensionVersion

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getExtensionVersion(extension: Int): Int
```

Return the version of the specified extensions.

This method is suitable to use in conditional statements to determine whether an API is available and is safe to use. For example:

```kotlin
if (getExtensionVersion(VERSION_CODES.R) >= 3) {
    // Safely use API available since R extensions version 3
  }
  
```

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extension to get the version of. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ext/SdkExtensions#AD_SERVICES:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if extension is not a valid extension |
