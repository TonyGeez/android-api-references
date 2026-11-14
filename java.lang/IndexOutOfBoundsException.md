# IndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IndexOutOfBoundsException

```
open class IndexOutOfBoundsException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| | | | ↳ | [java.lang.IndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/IndexOutOfBoundsException#) |

| Known Direct Subclasses [ArrayIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException), [CursorIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/android/database/CursorIndexOutOfBoundsException.html#), [StringIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/StringIndexOutOfBoundsException) |------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------| | [ArrayIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException) | Thrown to indicate that an array has been accessed with an illegal index. | | [CursorIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/android/database/CursorIndexOutOfBoundsException.html#) | An exception indicating that a cursor is out of bounds. | | [StringIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/StringIndexOutOfBoundsException) | Thrown by`String`methods to indicate that an index is either negative or greater than the size of the string. | |

Thrown to indicate that an index of some sort (such as to an array, to a string, or to a vector) is out of range.

Applications can subclass this class to indicate similar exceptions.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/IndexOutOfBoundsException#IndexOutOfBoundsException())`()` Constructs an`IndexOutOfBoundsException`with no detail message. |
| [IndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/IndexOutOfBoundsException#IndexOutOfBoundsException(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`IndexOutOfBoundsException`class with an argument indicating the illegal index. |
| [IndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/IndexOutOfBoundsException#IndexOutOfBoundsException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IndexOutOfBoundsException`with the specified detail message. |
| [IndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/IndexOutOfBoundsException#IndexOutOfBoundsException(kotlin.Long))`(`index:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a new`IndexOutOfBoundsException`class with an argument indicating the illegal index. |

## Public constructors

### IndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IndexOutOfBoundsException()
```

Constructs an`IndexOutOfBoundsException`with no detail message. 

### IndexOutOfBoundsException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IndexOutOfBoundsException(index: Int)
```

Constructs a new`IndexOutOfBoundsException`class with an argument indicating the illegal index.

The index is included in this exception's detail message. The exact presentation format of the detail message is unspecified.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the illegal index. |

### IndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IndexOutOfBoundsException(s: String!)
```

Constructs an`IndexOutOfBoundsException`with the specified detail message.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |

### IndexOutOfBoundsException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IndexOutOfBoundsException(index: Long)
```

Constructs a new`IndexOutOfBoundsException`class with an argument indicating the illegal index.

The index is included in this exception's detail message. The exact presentation format of the detail message is unspecified.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `index` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the illegal index. |
