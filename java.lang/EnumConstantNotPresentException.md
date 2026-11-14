# EnumConstantNotPresentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EnumConstantNotPresentException

```
open class EnumConstantNotPresentException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.EnumConstantNotPresentException](https://developer.android.com/reference/kotlin/java/lang/EnumConstantNotPresentException#) |

Thrown when an application tries to access an enum constant by name and the enum type contains no constant with the specified name. This exception can be thrown by the .

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EnumConstantNotPresentException](https://developer.android.com/reference/kotlin/java/lang/EnumConstantNotPresentException#EnumConstantNotPresentException(java.lang.Class,%20kotlin.String))`(`enumType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class)<out` ` [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)< [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)<*>>!>!`, `constantName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`EnumConstantNotPresentException`for the specified constant. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [constantName](https://developer.android.com/reference/kotlin/java/lang/EnumConstantNotPresentException#constantName())`()` Returns the name of the missing enum constant. |
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\<out [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\<\*\>\>!\>! | [enumType](https://developer.android.com/reference/kotlin/java/lang/EnumConstantNotPresentException#enumType())`()` Returns the type of the missing enum constant. |

## Public constructors

### EnumConstantNotPresentException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EnumConstantNotPresentException(
    enumType: Class<out Enum<Enum<*>>!>!, 
    constantName: String!)
```

Constructs an`EnumConstantNotPresentException`for the specified constant.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enumType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\<out [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\<\*\>\>!\>!:the type of the missing enum constant |
| `constantName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the missing enum constant |

## Public methods

### constantName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun constantName(): String!
```

Returns the name of the missing enum constant.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the missing enum constant |

### enumType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enumType(): Class<out Enum<Enum<*>>!>!
```

Returns the type of the missing enum constant.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class)<out` ` [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)< [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)<*>>!>! | the type of the missing enum constant |
