# IndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IndexOutOfBoundsException

```
open class IndexOutOfBoundsException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IndexOutOfBoundsException](IndexOutOfBoundsException.md) |

| Known Direct Subclasses [ArrayIndexOutOfBoundsException](ArrayIndexOutOfBoundsException.md), [CursorIndexOutOfBoundsException](../android.database/CursorIndexOutOfBoundsException.md), [StringIndexOutOfBoundsException](StringIndexOutOfBoundsException.md) |------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------| | [ArrayIndexOutOfBoundsException](ArrayIndexOutOfBoundsException.md) | Thrown to indicate that an array has been accessed with an illegal index. | | [CursorIndexOutOfBoundsException](../android.database/CursorIndexOutOfBoundsException.md) | An exception indicating that a cursor is out of bounds. | | [StringIndexOutOfBoundsException](StringIndexOutOfBoundsException.md) | Thrown by`String`methods to indicate that an index is either negative or greater than the size of the string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Thrown to indicate that an index of some sort (such as to an array, to a string, or to a vector) is out of range.

Applications can subclass this class to indicate similar exceptions.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IndexOutOfBoundsException](IndexOutOfBoundsException.md))`()` Constructs an`IndexOutOfBoundsException`with no detail message. |
| [IndexOutOfBoundsException](IndexOutOfBoundsException.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`IndexOutOfBoundsException`class with an argument indicating the illegal index. |
| [IndexOutOfBoundsException](IndexOutOfBoundsException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IndexOutOfBoundsException`with the specified detail message. |
| [IndexOutOfBoundsException](IndexOutOfBoundsException.md))`(`index:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a new`IndexOutOfBoundsException`class with an argument indicating the illegal index. |

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
