# XPathExpressionException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathExpressionException

```
open class XPathExpressionException : XPathException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [javax.xml.xpath.XPathException](XPathException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.xml.xpath.XPathExpressionException](XPathExpressionException.md) |

| Known Direct Subclasses [XPathFunctionException](XPathFunctionException.md) |-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [XPathFunctionException](XPathFunctionException.md) | `XPathFunctionException` represents an error with an XPath function. | |
| --- | --- | --- | --- | --- | --- | --- |

`XPathExpressionException` represents an error in an XPath expression.

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XPathExpressionException](XPathExpressionException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new `XPathExpressionException` with the specified detail `message`. |
| [XPathExpressionException](XPathExpressionException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new `XPathExpressionException` with the specified `cause`. |

| Inherited functions ||
|---|---|
| From class [XPathException](XPathException.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](XPathException.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](XPathException.md))`(`s:` ` [PrintStream](../java.io/PrintStream.md)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](XPathException.md))`(`s:` ` [PrintWriter](../java.io/PrintWriter.md)`)` <br /> | ||

| Inherited properties ||
|---|---|
| From class [XPathException](XPathException.md) |-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------| | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](XPathException.md) <br /> | ||

## Public constructors

### XPathExpressionException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XPathExpressionException(message: String!)
```

Constructs a new `XPathExpressionException` with the specified detail `message`.

The `cause` is not initialized.

If `message` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The detail message. |

### XPathExpressionException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
XPathExpressionException(cause: Throwable!)
```

Constructs a new `XPathExpressionException` with the specified `cause`.

If `cause` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: The cause. |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if `cause` is `null`. |
