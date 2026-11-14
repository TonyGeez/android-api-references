# XPathFunctionException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathFunctionException

```
open class XPathFunctionException : XPathExpressionException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [javax.xml.xpath.XPathException](../javax/xml/xpath/XPathException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [javax.xml.xpath.XPathExpressionException](../javax/xml/xpath/XPathExpressionException.md) ||
| | | | | ↳ | [javax.xml.xpath.XPathFunctionException](../javax/xml/xpath/XPathFunctionException.md) |

`XPathFunctionException`represents an error with an XPath function.

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XPathFunctionException](../javax/xml/xpath/XPathFunctionException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`XPathFunctionException`with the specified detail`message`. |
| [XPathFunctionException](../javax/xml/xpath/XPathFunctionException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`XPathFunctionException`with the specified`cause`. |

## Public constructors

### XPathFunctionException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XPathFunctionException(message: String!)
```

Constructs a new`XPathFunctionException`with the specified detail`message`.

The`cause`is not initialized.

If`message`is`null`, then a`NullPointerException`is thrown.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The detail message. |

### XPathFunctionException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XPathFunctionException(cause: Throwable!)
```

Constructs a new`XPathFunctionException`with the specified`cause`.

If`cause`is`null`, then a`NullPointerException`is thrown.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The cause. |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`cause`is`null`. |
