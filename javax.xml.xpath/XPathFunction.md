# XPathFunction

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathFunction

```
interface XPathFunction
```

| [javax.xml.xpath.XPathFunction](XPathFunction.md) |

`XPathFunction`provides access to XPath functions.

Functions are identified by QName and arity in XPath.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [evaluate](XPathFunction.md))`(`args:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>!`)` Evaluate the function with the specified arguments. |

## Public methods

### evaluate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun evaluate(args: MutableList<Any?>!): Any!
```

Evaluate the function with the specified arguments.

To the greatest extent possible, side-effects should be avoided in the definition of extension functions. The implementation evaluating an XPath expression is under no obligation to call extension functions in any particular order or any particular number of times.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>!:The arguments,`null`is a valid value. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The result of evaluating the`XPath`function as an`Object`. |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------|
| `javax.xml.xpath.XPathFunctionException` | If`args`cannot be evaluated with this`XPath`function. |
