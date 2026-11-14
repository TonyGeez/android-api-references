# ClassCastException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClassCastException

```
open class ClassCastException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.ClassCastException](../java/lang/ClassCastException.md) |

Thrown to indicate that the code has attempted to cast an object to a subclass of which it is not an instance. For example, the following code generates a`ClassCastException`: 

```kotlin
Object x = new Integer(0);
      System.out.println((String)x);
  
```

<br />

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClassCastException](../java/lang/ClassCastException.md))`()` Constructs a`ClassCastException`with no detail message. |
| [ClassCastException](../java/lang/ClassCastException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`ClassCastException`with the specified detail message. |

## Public constructors

### ClassCastException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClassCastException()
```

Constructs a`ClassCastException`with no detail message. 

### ClassCastException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClassCastException(s: String!)
```

Constructs a`ClassCastException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
