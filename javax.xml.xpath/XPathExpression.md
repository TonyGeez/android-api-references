Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathExpression

```
interface XPathExpression
```

| [javax.xml.xpath.XPathExpression](XPathExpression.md) |

`XPathExpression` provides access to compiled XPath expressions.

| Evaluation of XPath Expressions. ||
|---|---|
| context | If a request is made to evaluate the expression in the absence of a context item, an empty document node will be used for the context. For the purposes of evaluating XPath expressions, a DocumentFragment is treated like a Document node. |
| variables | If the expression contains a variable reference, its value will be found through the `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathVariableResolver`. An `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpressionException` is raised if the variable resolver is undefined or the resolver returns `null` for the variable. The value of a variable must be immutable through the course of any single evaluation. <br /> |
| functions | If the expression contains a function reference, the function will be found through the `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFunctionResolver`. An `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpressionException` is raised if the function resolver is undefined or the function resolver returns `null` for the function. <br /> |
| --- | --- |
| QNames | QNames in the expression are resolved against the XPath namespace context. |
| result | This result of evaluating an expression is converted to an instance of the desired return type. Valid return types are defined in `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants`. Conversion to the return type follows XPath conversion rules. <br /> |

## Summary

| Public methods ||
|---|---|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpression#evaluate(kotlin.Any)(item: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Evaluate the compiled XPath expression in the specified context and return the result as a `String`. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpression#evaluate(kotlin.Any,%20javax.xml.namespace.QName)(item: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, returnType: https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#!)` Evaluate the compiled XPath expression in the specified context and return the result as the specified type. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpression#evaluate(org.xml.sax.InputSource)(source: https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!)` Evaluate the compiled XPath expression in the context of the specified `InputSource` and return the result as a `String`. |
| --- | --- |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpression#evaluate(org.xml.sax.InputSource,%20javax.xml.namespace.QName)(source: https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!, returnType: https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#!)` Evaluate the compiled XPath expression in the context of the specified `InputSource` and return the result as the specified type. |

## Public methods

### evaluate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun evaluate(item: Any!): String!
```

Evaluate the compiled XPath expression in the specified context and return the result as a `String`.

This method calls `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpression#evaluate(kotlin.Any,%20javax.xml.namespace.QName)` with a `returnType` of `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#STRING:javax.xml.namespace.QName`.

See [Evaluation of XPath Expressions](XPathExpression.md) for context item evaluation, variable, function and QName resolution and return type conversion.

If a `null` value is provided for `item`, an empty document will be used for the context.

| Parameters ||
|---|---|
| `item` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The starting context (node or node list, for example). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The `String` that is the result of evaluating the expression and converting the result to a `String`. |

| Exceptions ||
|---|---|
| `javax.xml.xpath.XPathExpressionException` | If the expression cannot be evaluated. |

### evaluate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun evaluate(
    item: Any!, 
    returnType: QName!
): Any!
```

Evaluate the compiled XPath expression in the specified context and return the result as the specified type.

See [Evaluation of XPath Expressions](XPathExpression.md) for context item evaluation, variable, function and QName resolution and return type conversion.

If `returnType` is not one of the types defined in `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants`, then an `IllegalArgumentException` is thrown.

If a `null` value is provided for `item`, an empty document will be used for the context. If `returnType` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `item` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The starting context (node or node list, for example). |
| `returnType` | [QName](../javax.xml.namespace/QName.md)!: The desired return type. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | The `Object` that is the result of evaluating the expression and converting the result to `returnType`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `returnType` is not one of the types defined in `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants`. |
| `java.lang.NullPointerException` | If `returnType` is `null`. |
| `javax.xml.xpath.XPathExpressionException` | If the expression cannot be evaluated. |
| --- | --- |

### evaluate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun evaluate(source: InputSource!): String!
```

Evaluate the compiled XPath expression in the context of the specified `InputSource` and return the result as a `String`.

This method calls `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpression#evaluate(org.xml.sax.InputSource,%20javax.xml.namespace.QName)` with a `returnType` of `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#STRING:javax.xml.namespace.QName`.

See [Evaluation of XPath Expressions](XPathExpression.md) for context item evaluation, variable, function and QName resolution and return type conversion.

If `source` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `source` | [InputSource](../org.xml.sax/InputSource.md)!: The `InputSource` of the document to evaluate over. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The `String` that is the result of evaluating the expression and converting the result to a `String`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `source` is `null`. |
| `javax.xml.xpath.XPathExpressionException` | If the expression cannot be evaluated. |

### evaluate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun evaluate(
    source: InputSource!, 
    returnType: QName!
): Any!
```

Evaluate the compiled XPath expression in the context of the specified `InputSource` and return the result as the specified type.

This method builds a data model for the `https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#` and calls `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpression#evaluate(kotlin.Any,%20javax.xml.namespace.QName)` on the resulting document object.

See [Evaluation of XPath Expressions](XPathExpression.md) for context item evaluation, variable, function and QName resolution and return type conversion.

If `returnType` is not one of the types defined in `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants`, then an `IllegalArgumentException` is thrown.

If `source` or `returnType` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `source` | [InputSource](../org.xml.sax/InputSource.md)!: The `InputSource` of the document to evaluate over. |
| `returnType` | [QName](../javax.xml.namespace/QName.md)!: The desired return type. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | The `Object` that is the result of evaluating the expression and converting the result to `returnType`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `returnType` is not one of the types defined in `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants`. |
| `java.lang.NullPointerException` | If `source` or `returnType` is `null`. |
| `javax.xml.xpath.XPathExpressionException` | If the expression cannot be evaluated. |
| --- | --- |
