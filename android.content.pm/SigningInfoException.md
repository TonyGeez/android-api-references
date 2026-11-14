# SigningInfoException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SigningInfoException

Kotlin| [Java](SigningInfoException.md) 
| --- | --- |

```
open class SigningInfoException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.content.pm.SigningInfoException](SigningInfoException.md) |
| --- | --- | --- | --- |

Indicates an error when verifying the [app signing](https://source.android.com/docs/security/features/apksigning) information.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCode](SigningInfoException.md))`()` Returns a code representing the cause, in one of the installation parse return codes in [PackageManager](PackageManager.md). |

## Public methods

### getCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCode(): Int
```

Returns a code representing the cause, in one of the installation parse return codes in [PackageManager](PackageManager.md).
