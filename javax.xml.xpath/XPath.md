Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPath

```
interface XPath
```

| [javax.xml.xpath.XPath](XPath.md) |

`XPath` provides access to the XPath evaluation environment and expressions.

| Evaluation of XPath Expressions. ||
|---|---|
| context | If a request is made to evaluate the expression in the absence of a context item, an empty document node will be used for the context. For the purposes of evaluating XPath expressions, a DocumentFragment is treated like a Document node. |
| variables | If the expression contains a variable reference, its value will be found through the XPathVariableResolver set with setXPathVariableResolver. An XPathExpressionException is raised if the variable resolver is undefined or the resolver returns `null` for the variable. The value of a variable must be immutable through the course of any single evaluation. <br /> |
| functions | If the expression contains a function reference, the function will be found through the XPathFunctionResolver set with setXPathFunctionResolver. An XPathExpressionException is raised if the function resolver is undefined or the function resolver returns `null` for the function. <br /> |
| --- | --- |
| QNames | QNames in the expression are resolved against the XPath namespace context set with setNamespaceContext. |
| result | This result of evaluating an expression is converted to an instance of the desired return type. Valid return types are defined in XPathConstants. Conversion to the return type follows XPath conversion rules. <br /> |

## Summary

| Public methods ||
|---|---|
| abstract [XPathExpression](XPathExpression.md)! | compile Compile an XPath expression for later evaluation. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | evaluate Evaluate an XPath expression in the specified context and return the result as a `String`. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | evaluate Evaluate an `XPath` expression in the specified context and return the result as the specified type. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | evaluate Evaluate an XPath expression in the context of the specified `InputSource` and return the result as a `String`. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | evaluate Evaluate an XPath expression in the context of the specified `InputSource` and return the result as the specified type. |
| abstract [NamespaceContext](../javax.xml.namespace/NamespaceContext.md)! | getNamespaceContext Return the current namespace context. |
| --- | --- |
| abstract [XPathFunctionResolver](XPathFunctionResolver.md)! | getXPathFunctionResolver Return the current function resolver. |
| abstract [XPathVariableResolver](XPathVariableResolver.md)! | getXPathVariableResolver Return the current variable resolver. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | reset Reset this `XPath` to its original configuration. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNamespaceContext Establish a namespace context. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setXPathFunctionResolver Establish a function resolver. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setXPathVariableResolver Establish a variable resolver. |
| --- | --- |

## Public methods

### compile

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun compile(expression: String!): XPathExpression!
```

Compile an XPath expression for later evaluation.

If `expression` contains any XPathFunctions, they must be available via the XPathFunctionResolver. An XPathExpressionException will be thrown if the `XPathFunction` cannot be resolved with the `XPathFunctionResolver`.

If `expression` is `null`, a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `expression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The XPath expression. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpression!` | Compiled XPath expression. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `expression` is `null`. |
| `javax.xml.xpath.XPathExpressionException` | If `expression` cannot be compiled. |

### evaluate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun evaluate(
    expression: String!, 
    item: Any!
): String!
```

Evaluate an XPath expression in the specified context and return the result as a `String`.

This method calls evaluate with a `returnType` of `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#STRING:javax.xml.namespace.QName`.

See [Evaluation of XPath Expressions](XPath.md) for context item evaluation, variable, function and QName resolution and return type conversion.

If a `null` value is provided for `item`, an empty document will be used for the context. If `expression` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `expression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The XPath expression. |
| `item` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The starting context (node or node list, for example). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The `String` that is the result of evaluating the expression and converting the result to a `String`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `expression` is `null`. |
| `javax.xml.xpath.XPathExpressionException` | If `expression` cannot be evaluated. |

### evaluate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun evaluate(
    expression: String!, 
    item: Any!, 
    returnType: QName!
): Any!
```

Evaluate an `XPath` expression in the specified context and return the result as the specified type.

See [Evaluation of XPath Expressions](XPath.md) for context item evaluation, variable, function and `QName` resolution and return type conversion.

If `returnType` is not one of the types defined in XPathConstants ( `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#NUMBER:javax.xml.namespace.QName`, `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#STRING:javax.xml.namespace.QName`, `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#BOOLEAN:javax.xml.namespace.QName`, `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#NODE:javax.xml.namespace.QName` or `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#NODESET:javax.xml.namespace.QName`) then an `IllegalArgumentException` is thrown.

If a `null` value is provided for `item`, an empty document will be used for the context. If `expression` or `returnType` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `expression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The XPath expression. |
| `item` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The starting context (node or node list, for example). |
| `returnType` | [QName](../javax.xml.namespace/QName.md)!: The desired return type. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | Result of evaluating an XPath expression as an `Object` of `returnType`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `returnType` is not one of the types defined in XPathConstants. |
| `java.lang.NullPointerException` | If `expression` or `returnType` is `null`. |
| `javax.xml.xpath.XPathExpressionException` | If `expression` cannot be evaluated. |
| --- | --- |

### evaluate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun evaluate(
    expression: String!, 
    source: InputSource!
): String!
```

Evaluate an XPath expression in the context of the specified `InputSource` and return the result as a `String`.

This method calls evaluate with a `returnType` of `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#STRING:javax.xml.namespace.QName`.

See [Evaluation of XPath Expressions](XPath.md) for context item evaluation, variable, function and QName resolution and return type conversion.

If `expression` or `source` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `expression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The XPath expression. |
| `source` | [InputSource](../org.xml.sax/InputSource.md)!: The `InputSource` of the document to evaluate over. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The `String` that is the result of evaluating the expression and converting the result to a `String`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `expression` or `source` is `null`. |
| `javax.xml.xpath.XPathExpressionException` | If expression cannot be evaluated. |

### evaluate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun evaluate(
    expression: String!, 
    source: InputSource!, 
    returnType: QName!
): Any!
```

Evaluate an XPath expression in the context of the specified `InputSource` and return the result as the specified type.

This method builds a data model for the `https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#` and calls evaluate on the resulting document object.

See [Evaluation of XPath Expressions](XPath.md) for context item evaluation, variable, function and QName resolution and return type conversion.

If `returnType` is not one of the types defined in XPathConstants, then an `IllegalArgumentException` is thrown.

If `expression`, `source` or `returnType` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `expression` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The XPath expression. |
| `source` | [InputSource](../org.xml.sax/InputSource.md)!: The input source of the document to evaluate over. |
| `returnType` | [QName](../javax.xml.namespace/QName.md)!: The desired return type. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | The `Object` that encapsulates the result of evaluating the expression. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `returnType` is not one of the types defined in XPathConstants. |
| `java.lang.NullPointerException` | If `expression`, `source` or `returnType` is `null`. |
| `javax.xml.xpath.XPathExpressionException` | If expression cannot be evaluated. |
| --- | --- |

### getNamespaceContext

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNamespaceContext(): NamespaceContext!
```

Return the current namespace context.

`null` is returned in no namespace context is in effect.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/namespace/NamespaceContext.html#!` | Current Namespace context. |

### getXPathFunctionResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getXPathFunctionResolver(): XPathFunctionResolver!
```

Return the current function resolver.

`null` is returned in no function resolver is in effect.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFunctionResolver!` | Current function resolver. |

### getXPathVariableResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getXPathVariableResolver(): XPathVariableResolver!
```

Return the current variable resolver.

`null` is returned in no variable resolver is in effect.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathVariableResolver!` | Current variable resolver. |

### reset

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun reset(): Unit
```

Reset this `XPath` to its original configuration.

`XPath` is reset to the same state as when it was created with newXPath. `reset()` is designed to allow the reuse of existing `XPath`s thus saving resources associated with the creation of new `XPath`s.

The reset `XPath` is not guaranteed to have the same XPathFunctionResolver, XPathVariableResolver or `https://developer.android.com/reference/kotlin/javax/xml/namespace/NamespaceContext.html#` `Object`s, e.g. equals. It is guaranteed to have a functionally equal `XPathFunctionResolver`, `XPathVariableResolver` and `NamespaceContext`.

### setNamespaceContext

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setNamespaceContext(nsContext: NamespaceContext!): Unit
```

Establish a namespace context.

A `NullPointerException` is thrown if `nsContext` is `null`.

| Parameters ||
|---|---|
| `nsContext` | [NamespaceContext](../javax.xml.namespace/NamespaceContext.md)!: Namespace context to use. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `nsContext` is `null`. |

### setXPathFunctionResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setXPathFunctionResolver(resolver: XPathFunctionResolver!): Unit
```

Establish a function resolver.

A `NullPointerException` is thrown if `resolver` is `null`.

| Parameters ||
|---|---|
| `resolver` | [XPathFunctionResolver](XPathFunctionResolver.md)!: XPath function resolver. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `resolver` is `null`. |

### setXPathVariableResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setXPathVariableResolver(resolver: XPathVariableResolver!): Unit
```

Establish a variable resolver.

A `NullPointerException` is thrown if `resolver` is `null`.

| Parameters ||
|---|---|
| `resolver` | [XPathVariableResolver](XPathVariableResolver.md)!: Variable resolver. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `resolver` is `null`. |
