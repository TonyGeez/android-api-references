# UnknownFormatFlagsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnknownFormatFlagsException

```
open class UnknownFormatFlagsException : IllegalFormatException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java/lang/IllegalArgumentException.md) |||
| | | | | ↳ | [java.util.IllegalFormatException](../java/util/IllegalFormatException.md) ||
| | | | | | ↳ | [java.util.UnknownFormatFlagsException](../java/util/UnknownFormatFlagsException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Unchecked exception thrown when an unknown flag is given.

Unless otherwise specified, passing a`null`argument to any method or constructor in this class will cause a [NullPointerException](../java/lang/NullPointerException.md) to be thrown.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnknownFormatFlagsException](../java/util/UnknownFormatFlagsException.md))`(`f:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class with the specified flags. |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFlags](../java/util/UnknownFormatFlagsException.md))`()` Returns the set of flags which contains an unknown flag. |

| Properties ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](../java/util/UnknownFormatFlagsException.md) <br /> |

## Public constructors

### UnknownFormatFlagsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnknownFormatFlagsException(f: String!)
```

Constructs an instance of this class with the specified flags.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| `f` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The set of format flags which contain an unknown flag |

## Public methods

### getFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFlags(): String!
```

Returns the set of flags which contains an unknown flag.

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
