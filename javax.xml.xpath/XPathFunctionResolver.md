# XPathFunctionResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathFunctionResolver

```
interface XPathFunctionResolver
```

| [javax.xml.xpath.XPathFunctionResolver](XPathFunctionResolver.md) |

`XPathFunctionResolver`provides access to the set of user defined`XPathFunction`s.

XPath functions are resolved by name and arity. The resolver is not needed for XPath built-in functions and the resolver***cannot***be used to override those functions.

In particular, the resolver is only called for functions in an another namespace (functions with an explicit prefix). This means that you cannot use the`XPathFunctionResolver`to implement specifications like [XML-Signature Syntax and Processing](http://www.w3.org/TR/xmldsig-core/) which extend the function library of XPath 1.0 in the same namespace. This is a consequence of the design of the resolver.

If you wish to implement additional built-in functions, you will have to extend the underlying implementation directly.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [XPathFunction](XPathFunction.md)! | [resolveFunction](XPathFunctionResolver.md))`(`functionName:` ` [QName](../javax.xml.namespace/QName.md)!`, `arity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Find a function in the set of available functions. |

## Public methods

### resolveFunction

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun resolveFunction(
    functionName: QName!, 
    arity: Int
): XPathFunction!
```

Find a function in the set of available functions.

If`functionName`or`arity`is`null`, then a`NullPointerException`is thrown.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `functionName` | [QName](../javax.xml.namespace/QName.md)!:The function name. |
| `arity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of arguments that the returned function must accept. |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [XPathFunction](XPathFunction.md)! | The function or`null`if no function named`functionName`with`arity`arguments exists. |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | If`functionName`or`arity`is`null`. |
