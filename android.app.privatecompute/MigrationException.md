Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MigrationException

```
class MigrationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.app.privatecompute.MigrationException](https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException#) |
| --- | --- | --- | --- |

Exception thrown when a migration request fails.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException#ERROR_INVOCATION_FAILED:kotlin.Int` The migration request failed due to an invocation error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException#ERROR_TIMEOUT:kotlin.Int` The migration request failed due to a timeout. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException#MigrationException(kotlin.Int,%20kotlin.String)(errorCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException#getErrorCode()()` Returns the error code associated with this exception. |

## Constants

### ERROR_INVOCATION_FAILED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INVOCATION_FAILED: Int
```

The migration request failed due to an invocation error.

 Value: 1

### ERROR_TIMEOUT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_TIMEOUT: Int
```

The migration request failed due to a timeout.

 Value: 2

## Public constructors

### MigrationException

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MigrationException(
    errorCode: Int, 
    message: String?)
```

| Parameters ||
|---|---|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException#ERROR_INVOCATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException#ERROR_TIMEOUT:kotlin.Int` |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

## Public methods

### getErrorCode

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getErrorCode(): Int
```

Returns the error code associated with this exception.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException#ERROR_INVOCATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException#ERROR_TIMEOUT:kotlin.Int` |
