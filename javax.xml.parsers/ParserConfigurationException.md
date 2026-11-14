# ParserConfigurationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParserConfigurationException

```
open class ParserConfigurationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [javax.xml.parsers.ParserConfigurationException](../javax/xml/parsers/ParserConfigurationException.md) |
| --- | --- | --- | --- |

Indicates a serious configuration error.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParserConfigurationException](../javax/xml/parsers/ParserConfigurationException.md))`()` Create a new`ParserConfigurationException`with no detail message. |
| [ParserConfigurationException](../javax/xml/parsers/ParserConfigurationException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`ParserConfigurationException`with the`String`specified as an error message. |

## Public constructors

### ParserConfigurationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParserConfigurationException()
```

Create a new`ParserConfigurationException`with no detail message. 

### ParserConfigurationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParserConfigurationException(msg: String!)
```

Create a new`ParserConfigurationException`with the`String`specified as an error message.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The error message for the exception. |
