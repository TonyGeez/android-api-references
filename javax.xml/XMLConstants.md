# XMLConstants

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLConstants

```
class XMLConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.XMLConstants](XMLConstants.md) |

Utility class to contain basic XML values as constants.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFAULT_NS_PREFIX](XMLConstants.md) Prefix to use to represent the default XML Namespace. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_SECURE_PROCESSING](XMLConstants.md) Feature for secure processing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NULL_NS_URI](XMLConstants.md) Namespace URI to use to represent that there is no Namespace. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RELAXNG_NS_URI](XMLConstants.md) RELAX NG Namespace URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [W3C_XML_SCHEMA_INSTANCE_NS_URI](XMLConstants.md) W3C XML Schema Instance Namespace URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [W3C_XML_SCHEMA_NS_URI](XMLConstants.md) W3C XML Schema Namespace URI. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [W3C_XPATH_DATATYPE_NS_URI](XMLConstants.md) W3C XPath Datatype Namespace URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [XMLNS_ATTRIBUTE](XMLConstants.md) The official XML attribute used for specifying XML Namespace declarations. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [XMLNS_ATTRIBUTE_NS_URI](XMLConstants.md) The official XML attribute used for specifying XML Namespace declarations, [XMLConstants.XMLNS_ATTRIBUTE](XMLConstants.md), Namespace name URI. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [XML_DTD_NS_URI](XMLConstants.md) XML Document Type Declaration Namespace URI as an arbitrary value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [XML_NS_PREFIX](XMLConstants.md) The official XML Namespace prefix. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [XML_NS_URI](XMLConstants.md) The official XML Namespace name URI. |
| --- | --- |

## Constants

### DEFAULT_NS_PREFIX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_NS_PREFIX: String
```

Prefix to use to represent the default XML Namespace.

Defined by the XML specification to be "". 

 Value: ""

**See Also**

### FEATURE_SECURE_PROCESSING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_SECURE_PROCESSING: String
```

Feature for secure processing.

- `true`instructs the implementation to process XML securely. This may set limits on XML constructs to avoid conditions such as denial of service attacks.
- `false`instructs the implementation to process XML according to the letter of the XML specifications ignoring security issues such as limits on XML constructs to avoid conditions such as denial of service attacks.

 Value: "http://javax.xml.XMLConstants/feature/secure-processing"

### NULL_NS_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NULL_NS_URI: String
```

Namespace URI to use to represent that there is no Namespace.

Defined by the Namespace specification to be "". 

 Value: ""

**See Also**

### RELAXNG_NS_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RELAXNG_NS_URI: String
```

RELAX NG Namespace URI.

Defined to be "`http://relaxng.org/ns/structure/1.0`". 

 Value: "http://relaxng.org/ns/structure/1.0"

**See Also**

### W3C_XML_SCHEMA_INSTANCE_NS_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val W3C_XML_SCHEMA_INSTANCE_NS_URI: String
```

W3C XML Schema Instance Namespace URI.

Defined to be "`http://www.w3.org/2001/XMLSchema-instance`". 

 Value: "http://www.w3.org/2001/XMLSchema-instance"

**See Also**

### W3C_XML_SCHEMA_NS_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val W3C_XML_SCHEMA_NS_URI: String
```

W3C XML Schema Namespace URI.

Defined to be "`http://www.w3.org/2001/XMLSchema`". 

 Value: "http://www.w3.org/2001/XMLSchema"

**See Also**

### W3C_XPATH_DATATYPE_NS_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val W3C_XPATH_DATATYPE_NS_URI: String
```

W3C XPath Datatype Namespace URI.

Defined to be "`http://www.w3.org/2003/11/xpath-datatypes`". 

 Value: "http://www.w3.org/2003/11/xpath-datatypes"

**See Also**

### XMLNS_ATTRIBUTE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val XMLNS_ATTRIBUTE: String
```

The official XML attribute used for specifying XML Namespace declarations.

It is***NOT*** valid to use as a prefix. Defined by the XML specification to be "`xmlns`". 

 Value: "xmlns"

**See Also**

### XMLNS_ATTRIBUTE_NS_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val XMLNS_ATTRIBUTE_NS_URI: String
```

The official XML attribute used for specifying XML Namespace declarations, [XMLConstants.XMLNS_ATTRIBUTE](XMLConstants.md), Namespace name URI.

Defined by the XML specification to be "`http://www.w3.org/2000/xmlns/`". 

 Value: "http://www.w3.org/2000/xmlns/"

**See Also**

### XML_DTD_NS_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val XML_DTD_NS_URI: String
```

XML Document Type Declaration Namespace URI as an arbitrary value.

Since not formally defined by any existing standard, arbitrarily define to be "`http://www.w3.org/TR/REC-xml`". 

 Value: "http://www.w3.org/TR/REC-xml"

### XML_NS_PREFIX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val XML_NS_PREFIX: String
```

The official XML Namespace prefix.

Defined by the XML specification to be "`xml`". 

 Value: "xml"

**See Also**

### XML_NS_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val XML_NS_URI: String
```

The official XML Namespace name URI.

Defined by the XML specification to be "`http://www.w3.org/XML/1998/namespace`". 

 Value: "http://www.w3.org/XML/1998/namespace"

**See Also**
