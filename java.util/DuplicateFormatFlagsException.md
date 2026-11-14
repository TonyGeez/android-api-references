# DuplicateFormatFlagsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DuplicateFormatFlagsException

```
open class DuplicateFormatFlagsException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) |||
| | | | | ↳ | [java.util.IllegalFormatException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatException) ||
| | | | | | ↳ | [java.util.DuplicateFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/DuplicateFormatFlagsException#) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when duplicate flags are provided in the format specifier.

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DuplicateFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/DuplicateFormatFlagsException#DuplicateFormatFlagsException(kotlin.String))`(`f:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class with the specified flags. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFlags](https://developer.android.com/reference/kotlin/java/util/DuplicateFormatFlagsException#getFlags())`()` Returns the set of flags which contains a duplicate flag. |

| Properties ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/util/DuplicateFormatFlagsException#message:kotlin.String) <br /> |

## Public constructors

### DuplicateFormatFlagsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DuplicateFormatFlagsException(f: String!)
```

Constructs an instance of this class with the specified flags.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------|
| `f` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The set of format flags which contain a duplicate flag. |

## Public methods

### getFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFlags(): String!
```

Returns the set of flags which contains a duplicate flag.

| Return ||
|-----------------------------------------------------------------------------------|-----------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The flags |

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
