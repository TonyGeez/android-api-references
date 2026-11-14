# XPathFactoryConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathFactoryConfigurationException

```
open class XPathFactoryConfigurationException : XPathException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [javax.xml.xpath.XPathException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException) ||
| | | | ↳ | [javax.xml.xpath.XPathFactoryConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactoryConfigurationException#) |

`XPathFactoryConfigurationException`represents a configuration error in a`XPathFactory`environment.

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XPathFactoryConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactoryConfigurationException#XPathFactoryConfigurationException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`XPathFactoryConfigurationException`with the specified detail`message`. |
| [XPathFactoryConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactoryConfigurationException#XPathFactoryConfigurationException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`XPathFactoryConfigurationException`with the specified`cause`. |

| Inherited functions ||
|---|---|
| From class [XPathException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#printStackTrace())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#printStackTrace(java.io.PrintStream))`(`s:` ` [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#printStackTrace(java.io.PrintWriter))`(`s:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)`)` <br /> | ||

| Inherited properties ||
|---|---|
| From class [XPathException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException) |-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#cause:kotlin.Throwable) <br /> | ||

## Public constructors

### XPathFactoryConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XPathFactoryConfigurationException(message: String!)
```

Constructs a new`XPathFactoryConfigurationException`with the specified detail`message`.

The`cause`is not initialized.

If`message`is`null`, then a`NullPointerException`is thrown.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The detail message. |

### XPathFactoryConfigurationException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XPathFactoryConfigurationException(cause: Throwable!)
```

Constructs a new`XPathFactoryConfigurationException`with the specified`cause`.

If`cause`is`null`, then a`NullPointerException`is thrown.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The cause. |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`cause`is`null`. |
