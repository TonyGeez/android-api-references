# NullPointerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NullPointerException

```
open class NullPointerException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.NullPointerException](NullPointerException.md) |

Thrown when an application attempts to use`null`in a case where an object is required. These include:

- Calling the instance method of a`null`object.
- Accessing or modifying the field of a`null`object.
- Taking the length of`null`as if it were an array.
- Accessing or modifying the slots of`null`as if it were an array.
- Throwing`null`as if it were a`Throwable`value.

<br />

Applications should throw instances of this class to indicate other illegal uses of the`null`object.`NullPointerException`objects may be constructed by the virtual machine as if [stack trace was not writable](Throwable.md)).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NullPointerException](NullPointerException.md))`()` Constructs a`NullPointerException`with no detail message. |
| [NullPointerException](NullPointerException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`NullPointerException`with the specified detail message. |

## Public constructors

### NullPointerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NullPointerException()
```

Constructs a`NullPointerException`with no detail message. 

### NullPointerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NullPointerException(s: String!)
```

Constructs a`NullPointerException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
