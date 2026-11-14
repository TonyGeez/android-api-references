# StringIndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringIndexOutOfBoundsException

```
open class StringIndexOutOfBoundsException : IndexOutOfBoundsException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/IndexOutOfBoundsException) ||
| | | | | ↳ | [java.lang.StringIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/StringIndexOutOfBoundsException#) |

Thrown by`String`methods to indicate that an index is either negative or greater than the size of the string. For some methods such as the [charAt](https://developer.android.com/reference/kotlin/java/lang/String#get(kotlin.Int))method, this exception also is thrown when the index is equal to the size of the string.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/StringIndexOutOfBoundsException#StringIndexOutOfBoundsException())`()` Constructs a`StringIndexOutOfBoundsException`with no detail message. |
| [StringIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/StringIndexOutOfBoundsException#StringIndexOutOfBoundsException(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`StringIndexOutOfBoundsException`class with an argument indicating the illegal index. |
| [StringIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/StringIndexOutOfBoundsException#StringIndexOutOfBoundsException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`StringIndexOutOfBoundsException`with the specified detail message. |

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
