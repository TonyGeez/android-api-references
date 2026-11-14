# StringIndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringIndexOutOfBoundsException

```
open class StringIndexOutOfBoundsException : IndexOutOfBoundsException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IndexOutOfBoundsException](../java/lang/IndexOutOfBoundsException.md) ||
| | | | | ↳ | [java.lang.StringIndexOutOfBoundsException](../java/lang/StringIndexOutOfBoundsException.md) |

Thrown by`String`methods to indicate that an index is either negative or greater than the size of the string. For some methods such as the [charAt](../java/lang/String.md))method, this exception also is thrown when the index is equal to the size of the string.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringIndexOutOfBoundsException](../java/lang/StringIndexOutOfBoundsException.md))`()` Constructs a`StringIndexOutOfBoundsException`with no detail message. |
| [StringIndexOutOfBoundsException](../java/lang/StringIndexOutOfBoundsException.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`StringIndexOutOfBoundsException`class with an argument indicating the illegal index. |
| [StringIndexOutOfBoundsException](../java/lang/StringIndexOutOfBoundsException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`StringIndexOutOfBoundsException`with the specified detail message. |

## Public constructors

### StringIndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringIndexOutOfBoundsException()
```

Constructs a`StringIndexOutOfBoundsException`with no detail message. 

### StringIndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringIndexOutOfBoundsException(index: Int)
```

Constructs a new`StringIndexOutOfBoundsException`class with an argument indicating the illegal index.

The index is included in this exception's detail message. The exact presentation format of the detail message is unspecified.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the illegal index. |

### StringIndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringIndexOutOfBoundsException(s: String!)
```

Constructs a`StringIndexOutOfBoundsException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
