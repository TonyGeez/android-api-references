# ArrayIndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrayIndexOutOfBoundsException

```
open class ArrayIndexOutOfBoundsException : IndexOutOfBoundsException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IndexOutOfBoundsException](IndexOutOfBoundsException.md) ||
| | | | | ↳ | [java.lang.ArrayIndexOutOfBoundsException](ArrayIndexOutOfBoundsException.md) |

Thrown to indicate that an array has been accessed with an illegal index. The index is either negative or greater than or equal to the size of the array.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArrayIndexOutOfBoundsException](ArrayIndexOutOfBoundsException.md))`()` Constructs an`ArrayIndexOutOfBoundsException`with no detail message. |
| [ArrayIndexOutOfBoundsException](ArrayIndexOutOfBoundsException.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`ArrayIndexOutOfBoundsException`class with an argument indicating the illegal index. |
| [ArrayIndexOutOfBoundsException](ArrayIndexOutOfBoundsException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`ArrayIndexOutOfBoundsException`class with the specified detail message. |

## Public constructors

### ArrayIndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayIndexOutOfBoundsException()
```

Constructs an`ArrayIndexOutOfBoundsException`with no detail message. 

### ArrayIndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayIndexOutOfBoundsException(index: Int)
```

Constructs a new`ArrayIndexOutOfBoundsException`class with an argument indicating the illegal index.

The index is included in this exception's detail message. The exact presentation format of the detail message is unspecified.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the illegal index. |

### ArrayIndexOutOfBoundsException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayIndexOutOfBoundsException(s: String!)
```

Constructs an`ArrayIndexOutOfBoundsException`class with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
