# QName

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# QName

```
open class QName : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.namespace.QName](QName.md) |

`QName`represents a**qualified name** as defined in the XML specifications: [XML Schema Part2: Datatypes specification](http://www.w3.org/TR/xmlschema-2/#QName), [Namespaces in XML](http://www.w3.org/TR/REC-xml-names/#ns-qualnames), [Namespaces in XML Errata](http://www.w3.org/XML/xml-names-19990114-errata).

The value of a`QName`contains a**Namespace URI** ,**local part** and**prefix**.

The prefix is included in`QName`to retain lexical information***when present*** in an . The prefix is***NOT*** used in [QName.equals(Object)](QName.md))or to compute the [QName.hashCode()](QName.md)). Equality and the hash code are defined using***only***the Namespace URI and local part.

If not specified, the Namespace URI is set to [XMLConstants.NULL_NS_URI](../javax.xml/XMLConstants.md). If not specified, the prefix is set to [XMLConstants.DEFAULT_NS_PREFIX](../javax.xml/XMLConstants.md).

`QName`is immutable.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [QName](QName.md))`(`localPart:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` `QName`constructor specifying the local part. |
| [QName](QName.md))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localPart:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` `QName`constructor specifying the Namespace URI and local part. |
| [QName](QName.md))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localPart:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` `QName`constructor specifying the Namespace URI, local part and prefix. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](QName.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Test this`QName`for equality with another`Object`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalPart](QName.md))`()` Get the local part of this`QName`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNamespaceURI](QName.md))`()` Get the Namespace URI of this`QName`. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPrefix](QName.md))`()` Get the prefix of this`QName`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](QName.md))`()` Generate the hash code for this`QName`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](QName.md))`()` `String`representation of this`QName`. |
| --- | --- |
| openstatic [QName](QName.md)! | [valueOf](QName.md))`(`qNameAsString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` `QName`derived from parsing the formatted`String`. |

## Public constructors

### QName

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
QName(localPart: String!)
```

`QName`constructor specifying the local part.

If the local part is`null`an`IllegalArgumentException`is thrown. A local part of "" is allowed to preserve compatible behavior with QName 1.0.

When using this constructor, the Namespace URI is set to [XMLConstants.NULL_NS_URI](../javax.xml/XMLConstants.md) and the prefix is set to [XMLConstants.DEFAULT_NS_PREFIX](../javax.xml/XMLConstants.md).

*In an XML context, all Element and Attribute names exist in the context of a Namespace. Making this explicit during the construction of a`QName`helps prevent hard to diagnosis XML validity errors. The constructors [QName(String](QName.md))and [QName(java.lang.String,java.lang.String,java.lang.String)](QName.md))are preferred.*

The local part is not validated as a [NCName](http://www.w3.org/TR/REC-xml-names/#NT-NCName) as specified in [Namespaces in XML](http://www.w3.org/TR/REC-xml-names/).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------|
| `localPart` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:local part of the`QName` |

**See Also**

- [#QName(String namespaceURI, String localPart)](QName.md))
- [#QName(String namespaceURI, String localPart, String
* prefix)](QName.md)) 

### QName

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
QName(
    namespaceURI: String!, 
    localPart: String!)
```

`QName`constructor specifying the Namespace URI and local part.

If the Namespace URI is`null`, it is set to [XMLConstants.NULL_NS_URI](../javax.xml/XMLConstants.md). This value represents no explicitly defined Namespace as defined by the [Namespaces in XML](http://www.w3.org/TR/REC-xml-names/#ns-qualnames) specification. This action preserves compatible behavior with QName 1.0. Explicitly providing the [XMLConstants.NULL_NS_URI](../javax.xml/XMLConstants.md) value is the preferred coding style.

If the local part is`null`an`IllegalArgumentException`is thrown. A local part of "" is allowed to preserve compatible behavior with QName 1.0.

When using this constructor, the prefix is set to [XMLConstants.DEFAULT_NS_PREFIX](../javax.xml/XMLConstants.md).

The Namespace URI is not validated as a [URI reference](http://www.ietf.org/rfc/rfc2396.txt). The local part is not validated as a [NCName](http://www.w3.org/TR/REC-xml-names/#NT-NCName) as specified in [Namespaces in XML](http://www.w3.org/TR/REC-xml-names/).

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Namespace URI of the`QName` |
| `localPart` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:local part of the`QName` |

**See Also**

- [#QName(String namespaceURI, String localPart, String
* prefix)](QName.md)) 

### QName

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
QName(
    namespaceURI: String!, 
    localPart: String!, 
    prefix: String!)
```

`QName`constructor specifying the Namespace URI, local part and prefix.

If the Namespace URI is`null`, it is set to [XMLConstants.NULL_NS_URI](../javax.xml/XMLConstants.md). This value represents no explicitly defined Namespace as defined by the [Namespaces in XML](http://www.w3.org/TR/REC-xml-names/#ns-qualnames) specification. This action preserves compatible behavior with QName 1.0. Explicitly providing the [XMLConstants.NULL_NS_URI](../javax.xml/XMLConstants.md) value is the preferred coding style.

If the local part is`null`an`IllegalArgumentException`is thrown. A local part of "" is allowed to preserve compatible behavior with QName 1.0.

If the prefix is`null`, an`IllegalArgumentException`is thrown. Use [XMLConstants.DEFAULT_NS_PREFIX](../javax.xml/XMLConstants.md) to explicitly indicate that no prefix is present or the prefix is not relevant.

The Namespace URI is not validated as a [URI reference](http://www.ietf.org/rfc/rfc2396.txt). The local part and prefix are not validated as a [NCName](http://www.w3.org/TR/REC-xml-names/#NT-NCName) as specified in [Namespaces in XML](http://www.w3.org/TR/REC-xml-names/).

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Namespace URI of the`QName` |
| `localPart` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:local part of the`QName` |
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:prefix of the`QName` |
| --- | --- |

## Public methods

### equals

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Test this`QName`for equality with another`Object`.

If the`Object`to be tested is not a`QName`or is`null`, then this method returns`false`.

Two`QName`s are considered equal if and only if both the Namespace URI and local part are equal. This method uses`String.equals()`to check equality of the Namespace URI and local part. The prefix is***NOT***used to determine equality.

This method satisfies the general contract of [Object.equals(Object)](../java.lang/Object.md))

| Parameters ||
|----------------|--------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `objectToTest` | the`Object`to test for equality with this`QName` |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the given`Object`is equal to this`QName`else`false` |

### getLocalPart

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalPart(): String!
```

Get the local part of this`QName`.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | local part of this`QName` |

### getNamespaceURI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNamespaceURI(): String!
```

Get the Namespace URI of this`QName`.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Namespace URI of this`QName` |

### getPrefix

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrefix(): String!
```

Get the prefix of this`QName`.

The prefix assigned to a`QName`might***NOT*** be valid in a different context. For example, a`QName`may be assigned a prefix in the context of parsing a document but that prefix may be invalid in the context of a different document.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | prefix of this`QName` |

### hashCode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Generate the hash code for this`QName`.

The hash code is calculated using both the Namespace URI and the local part of the`QName`. The prefix is***NOT***used to calculate the hash code.

This method satisfies the general contract of [Object.hashCode()](../java.lang/Object.md)).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hash code for this`QName``Object` |

### toString

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

`String`representation of this`QName`.

The commonly accepted way of representing a`QName`as a`String`was [defined](http://jclark.com/xml/xmlns.htm) by James Clark. Although this is not a*standard* specification, it is in common use, e.g. [javax.xml.transform.Transformer#setParameter(String name, Object value)](../javax.xml.transform/Transformer.md)). This implementation represents a`QName`as: "{" + Namespace URI + "}" + local part. If the Namespace URI`.equals(XMLConstants.NULL_NS_URI)`, only the local part is returned. An appropriate use of this method is for debugging or logging for human consumption.

Note the prefix value is***NOT*** returned as part of the`String`representation.

This method satisfies the general contract of [Object.toString()](../java.lang/Object.md)).

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `String`representation of this`QName` |

### valueOf

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(qNameAsString: String!): QName!
```

`QName`derived from parsing the formatted`String`.

If the`String`is`null`or does not conform to [QName.toString()](QName.md))formatting, an`IllegalArgumentException`is thrown.

*The`String`**MUST** be in the form returned by [QName.toString()](QName.md)).*

The commonly accepted way of representing a`QName`as a`String`was [defined](http://jclark.com/xml/xmlns.htm) by James Clark. Although this is not a*standard* specification, it is in common use, e.g. [javax.xml.transform.Transformer#setParameter(String name, Object value)](../javax.xml.transform/Transformer.md)). This implementation parses a`String`formatted as: "{" + Namespace URI + "}" + local part. If the Namespace URI`.equals(XMLConstants.NULL_NS_URI)`, only the local part should be provided.

The prefix value***CANNOT*** be represented in the`String`and will be set to [XMLConstants.DEFAULT_NS_PREFIX](../javax.xml/XMLConstants.md).

This method does not do full validation of the resulting`QName`.

The Namespace URI is not validated as a [URI reference](http://www.ietf.org/rfc/rfc2396.txt). The local part is not validated as a [NCName](http://www.w3.org/TR/REC-xml-names/#NT-NCName) as specified in [Namespaces in XML](http://www.w3.org/TR/REC-xml-names/).

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------|
| `qNameAsString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:`String`representation of the`QName` |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------|
| [QName](QName.md)! | `QName`corresponding to the given`String` |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/xml/namespace/QName#toString()>
