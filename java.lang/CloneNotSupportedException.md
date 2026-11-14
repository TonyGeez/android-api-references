# CloneNotSupportedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CloneNotSupportedException

```
open class CloneNotSupportedException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [java.lang.CloneNotSupportedException](../java/lang/CloneNotSupportedException.md) |
| --- | --- | --- | --- |

Thrown to indicate that the`clone`method in class`Object`has been called to clone an object, but that the object's class does not implement the`Cloneable`interface.

Applications that override the`clone`method can also throw this exception to indicate that an object could not or should not be cloned.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CloneNotSupportedException](../java/lang/CloneNotSupportedException.md))`()` Constructs a`CloneNotSupportedException`with no detail message. |
| [CloneNotSupportedException](../java/lang/CloneNotSupportedException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`CloneNotSupportedException`with the specified detail message. |

## Public constructors

### CloneNotSupportedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CloneNotSupportedException()
```

Constructs a`CloneNotSupportedException`with no detail message. 

### CloneNotSupportedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CloneNotSupportedException(s: String!)
```

Constructs a`CloneNotSupportedException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
