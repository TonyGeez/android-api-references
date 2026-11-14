# XPathVariableResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathVariableResolver

```
interface XPathVariableResolver
```

| [javax.xml.xpath.XPathVariableResolver](../javax/xml/xpath/XPathVariableResolver.md) |

`XPathVariableResolver`provides access to the set of user defined XPath variables.

The`XPathVariableResolver`and the XPath evaluator must adhere to a contract that cannot be directly enforced by the API. Although variables may be mutable, that is, an application may wish to evaluate the same XPath expression more than once with different variable values, in the course of evaluating any single XPath expression, a variable's value***must***be immutable.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [resolveVariable](../javax/xml/xpath/XPathVariableResolver.md))`(`variableName:` ` [QName](../javax/xml/namespace/QName.md)!`)` Find a variable in the set of available variables. |

## Public methods

### resolveVariable

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun resolveVariable(variableName: QName!): Any!
```

Find a variable in the set of available variables.

If`variableName`is`null`, then a`NullPointerException`is thrown.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------|
| `variableName` | [QName](../javax/xml/namespace/QName.md)!:The`QName`of the variable name. |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The variables value, or`null`if no variable named`variableName`exists. The value returned must be of a type appropriate for the underlying object model. |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | If`variableName`is`null`. |
