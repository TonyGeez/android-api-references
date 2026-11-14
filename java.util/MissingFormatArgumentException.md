Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MissingFormatArgumentException

```
open class MissingFormatArgumentException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) |||
| | | | | ↳ | [java.util.IllegalFormatException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatException) ||
| | | | | | ↳ | [java.util.MissingFormatArgumentException](https://developer.android.com/reference/kotlin/java/util/MissingFormatArgumentException#) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when there is a format specifier which does not have a corresponding argument or if an argument index refers to an argument that does not exist.

Unless otherwise specified, passing a `null` argument to any method or constructor in this class will cause a `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` to be thrown.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/MissingFormatArgumentException#MissingFormatArgumentException(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs an instance of this class with the unmatched format specifier. |

| Public methods ||
|---|---|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/util/MissingFormatArgumentException#getFormatSpecifier()()` Returns the unmatched format specifier. |

| Properties ||
|---|---|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/util/MissingFormatArgumentException#message:kotlin.String` Returns the detail message string of this throwable. |

## Public constructors

### MissingFormatArgumentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MissingFormatArgumentException(s: String!)
```

Constructs an instance of this class with the unmatched format specifier.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Format specifier which does not have a corresponding argument |

## Public methods

### getFormatSpecifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFormatSpecifier(): String!
```

Returns the unmatched format specifier.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The unmatched format specifier |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val message: String?
```

Returns the detail message string of this throwable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the detail message string of this `Throwable` instance (which may be `null`). |
