# ParserConfigurationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParserConfigurationException

```
open class ParserConfigurationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [javax.xml.parsers.ParserConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/parsers/ParserConfigurationException#) |
| --- | --- | --- | --- |

Indicates a serious configuration error.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParserConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/parsers/ParserConfigurationException#ParserConfigurationException())`()` Create a new`ParserConfigurationException`with no detail message. |
| [ParserConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/parsers/ParserConfigurationException#ParserConfigurationException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new`ParserConfigurationException`with the`String`specified as an error message. |

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
