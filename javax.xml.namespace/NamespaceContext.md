# NamespaceContext

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NamespaceContext

```
interface NamespaceContext
```

| [javax.xml.namespace.NamespaceContext](https://developer.android.com/reference/kotlin/javax/xml/namespace/NamespaceContext#) |

Interface for read only XML Namespace context processing.

An XML Namespace has the properties:

- Namespace URI: Namespace name expressed as a URI to which the prefix is bound
- prefix: syntactically, this is the part of the attribute name following the`XMLConstants.XMLNS_ATTRIBUTE`("xmlns") in the Namespace declaration

example:`<element xmlns:prefix="http://Namespace-name-URI">`

All`get*(*)`methods operate in the current scope for Namespace URI and prefix resolution.

Note that a Namespace URI can be bound to**multiple** prefixes in the current scope. This can occur when multiple`XMLConstants.XMLNS_ATTRIBUTE`("xmlns") Namespace declarations occur in the same Start-Tag and refer to the same Namespace URI. e.g. 

```kotlin
<element xmlns:prefix1="http://Namespace-name-URI"
           xmlns:prefix2="http://Namespace-name-URI">
  
```
This can also occur when the same Namespace URI is used in multiple`XMLConstants.XMLNS_ATTRIBUTE`("xmlns") Namespace declarations in the logical parent element hierarchy. e.g. 

```kotlin
<parent xmlns:prefix1="http://Namespace-name-URI">
    <child xmlns:prefix2="http://Namespace-name-URI">
      ...
    </child>
  </parent>
  
```

<br />

A prefix can only be bound to a**single**Namespace URI in the current scope.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNamespaceURI](https://developer.android.com/reference/kotlin/javax/xml/namespace/NamespaceContext#getNamespaceURI(kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get Namespace URI bound to a prefix in the current scope. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPrefix](https://developer.android.com/reference/kotlin/javax/xml/namespace/NamespaceContext#getPrefix(kotlin.String))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get prefix bound to Namespace URI in the current scope. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>! | [getPrefixes](https://developer.android.com/reference/kotlin/javax/xml/namespace/NamespaceContext#getPrefixes(kotlin.String))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get all prefixes bound to a Namespace URI in the current scope. |
| --- | --- |

## Public methods

### getNamespaceURI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamespaceURI(prefix: String!): String!
```

Get Namespace URI bound to a prefix in the current scope.

When requesting a Namespace URI by prefix, the following table describes the returned Namespace URI value for all possible prefix values:

| `getNamespaceURI(prefix)`return value for specified prefixes ||
| --- | --- |
| prefix parameter | Namespace URI return value |
| `DEFAULT_NS_PREFIX`("") | default Namespace URI in the current scope or [XMLConstants.NULL_NS_URI("")](https://developer.android.com/reference/kotlin/javax/xml/XMLConstants.html#NULL_NS_URI:kotlin.String) when there is no default Namespace URI in the current scope |
| bound prefix | Namespace URI bound to prefix in current scope |
| --- | --- |
| unbound prefix | [XMLConstants.NULL_NS_URI("")](https://developer.android.com/reference/kotlin/javax/xml/XMLConstants.html#NULL_NS_URI:kotlin.String) |
| `XMLConstants.XML_NS_PREFIX`("xml") | `XMLConstants.XML_NS_URI`("http://www.w3.org/XML/1998/namespace") |
| `XMLConstants.XMLNS_ATTRIBUTE`("xmlns") | `XMLConstants.XMLNS_ATTRIBUTE_NS_URI`("http://www.w3.org/2000/xmlns/") |
| --- | --- |
| `null` | `IllegalArgumentException`is thrown |

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:prefix to look up |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Namespace URI bound to prefix in the current scope |

### getPrefix

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrefix(namespaceURI: String!): String!
```

Get prefix bound to Namespace URI in the current scope.

To get all prefixes bound to a Namespace URI in the current scope, use [getPrefixes(java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/namespace/NamespaceContext#getPrefixes(kotlin.String)).

When requesting a prefix by Namespace URI, the following table describes the returned prefix value for all Namespace URI values:

| `getPrefix(namespaceURI)`return value for specified Namespace URIs ||
| --- | --- |
| Namespace URI parameter | prefix value returned |
| \<default Namespace URI\> | `XMLConstants.DEFAULT_NS_PREFIX`("") |
| bound Namespace URI | prefix bound to Namespace URI in the current scope, if multiple prefixes are bound to the Namespace URI in the current scope, a single arbitrary prefix, whose choice is implementation dependent, is returned |
| --- | --- |
| unbound Namespace URI | `null` |
| `XMLConstants.XML_NS_URI`("http://www.w3.org/XML/1998/namespace") | `XMLConstants.XML_NS_PREFIX`("xml") |
| `XMLConstants.XMLNS_ATTRIBUTE_NS_URI`("http://www.w3.org/2000/xmlns/") | `XMLConstants.XMLNS_ATTRIBUTE`("xmlns") |
| --- | --- |
| `null` | `IllegalArgumentException`is thrown |

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:URI of Namespace to lookup |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | prefix bound to Namespace URI in current context |

### getPrefixes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrefixes(namespaceURI: String!): MutableIterator<Any?>!
```

Get all prefixes bound to a Namespace URI in the current scope.

An Iterator over String elements is returned in an arbitrary,**implementation dependent**, order.

**The`Iterator`is*not* modifiable. e.g. the`remove()`method will throw`UnsupportedOperationException`.**

When requesting prefixes by Namespace URI, the following table describes the returned prefixes value for all Namespace URI values:

| ` getPrefixes(namespaceURI)`return value for specified Namespace URIs ||
| --- | --- |
| Namespace URI parameter | prefixes value returned |
| bound Namespace URI, including the \<default Namespace URI\> | `Iterator`over prefixes bound to Namespace URI in the current scope in an arbitrary,**implementation dependent**, order |
| unbound Namespace URI | empty`Iterator` |
| --- | --- |
| `XMLConstants.XML_NS_URI`("http://www.w3.org/XML/1998/namespace") | `Iterator`with one element set to`XMLConstants.XML_NS_PREFIX`("xml") |
| `XMLConstants.XMLNS_ATTRIBUTE_NS_URI`("http://www.w3.org/2000/xmlns/") | `Iterator`with one element set to`XMLConstants.XMLNS_ATTRIBUTE`("xmlns") |
| `null` | `IllegalArgumentException`is thrown |
| --- | --- |

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:URI of Namespace to lookup |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>! | `Iterator`for all prefixes bound to the Namespace URI in the current scope |
