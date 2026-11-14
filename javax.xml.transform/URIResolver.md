# URIResolver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URIResolver

```
interface URIResolver
```

| [javax.xml.transform.URIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver#) |

An object that implements this interface that can be called by the processor to turn a URI used in document(), xsl:import, or xsl:include into a Source object.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source)! | [resolve](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver#resolve(kotlin.String,%20kotlin.String))`(`href:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `base:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by the processor when it encounters an xsl:include, xsl:import, or document() function. |

## Public methods

### resolve

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun resolve(
    href: String!, 
    base: String!
): Source!
```

Called by the processor when it encounters an xsl:include, xsl:import, or document() function.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `href` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:An href attribute, which may be relative or absolute. |
| `base` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The base URI against which the first argument will be made absolute if the absolute URI is required. |

| Return ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source)! | A Source object, or null if the href cannot be resolved, and the processor should try to resolve the URI itself. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------|
| `javax.xml.transform.TransformerException` | if an error occurs when trying to resolve the URI. |
