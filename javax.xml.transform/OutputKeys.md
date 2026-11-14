# OutputKeys

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutputKeys

```
open class OutputKeys
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.transform.OutputKeys](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#) |

Provides string constants that can be used to set output properties for a Transformer, or to retrieve output properties from a Transformer or Templates object.

All the fields in this class are read-only.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CDATA_SECTION_ELEMENTS](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#CDATA_SECTION_ELEMENTS:kotlin.String) cdata-section-elements = expanded names. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DOCTYPE_PUBLIC](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#DOCTYPE_PUBLIC:kotlin.String) doctype-public = string. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DOCTYPE_SYSTEM](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#DOCTYPE_SYSTEM:kotlin.String) doctype-system = string. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ENCODING](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#ENCODING:kotlin.String) encoding = string. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INDENT](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#INDENT:kotlin.String) indent = "yes" | "no". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_TYPE](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#MEDIA_TYPE:kotlin.String) media-type = string. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [METHOD](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#METHOD:kotlin.String) method = "xml" | "html" | "text" | expanded name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [OMIT_XML_DECLARATION](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#OMIT_XML_DECLARATION:kotlin.String) omit-xml-declaration = "yes" | "no". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STANDALONE](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#STANDALONE:kotlin.String) standalone = "yes" | "no". |
| --- | --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VERSION](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#VERSION:kotlin.String) version = nmtoken. |

## Constants

### CDATA_SECTION_ELEMENTS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDATA_SECTION_ELEMENTS: String
```

cdata-section-elements = expanded names.

`cdata-section-elements`specifies a whitespace delimited list of the names of elements whose text node children should be output using CDATA sections. Note that these names must use the format described in the section Qualfied Name Representation in [javax.xml.transform](https://developer.android.com/reference/kotlin/javax/xml/transform/package-summary). 

 Value: "cdata-section-elements"

**See Also**

### DOCTYPE_PUBLIC

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCTYPE_PUBLIC: String
```

doctype-public = string.

See the documentation for the [DOCTYPE_SYSTEM](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#DOCTYPE_SYSTEM:kotlin.String) property for a description of what the value of the key should be. 

 Value: "doctype-public"

**See Also**

### DOCTYPE_SYSTEM

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCTYPE_SYSTEM: String
```

doctype-system = string.

`doctype-system`specifies the system identifier to be used in the document type declaration.

If the doctype-system property is specified, the xml output method should output a document type declaration immediately before the first element. The name following \<!DOCTYPE should be the name of the first element. If doctype-public property is also specified, then the xml output method should output PUBLIC followed by the public identifier and then the system identifier; otherwise, it should output SYSTEM followed by the system identifier. The internal subset should be empty. The value of the doctype-public property should be ignored unless the doctype-system property is specified.

If the doctype-public or doctype-system properties are specified, then the html output method should output a document type declaration immediately before the first element. The name following \<!DOCTYPE should be HTML or html. If the doctype-public property is specified, then the output method should output PUBLIC followed by the specified public identifier; if the doctype-system property is also specified, it should also output the specified system identifier following the public identifier. If the doctype-system property is specified but the doctype-public property is not specified, then the output method should output SYSTEM followed by the specified system identifier.

`doctype-system`specifies the system identifier to be used in the document type declaration. 

 Value: "doctype-system"

**See Also**

### ENCODING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODING: String
```

encoding = string.

`encoding`specifies the preferred character encoding that the Transformer should use to encode sequences of characters as sequences of bytes. The value of the encoding property should be treated case-insensitively. The value must only contain characters in the range #x21 to #x7E (i.e., printable ASCII characters). The value should either be a`charset`registered with the Internet Assigned Numbers Authority[\[IANA\]](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#IANA),[\[RFC2278\]](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys#RFC2278) or start with`X-`. 

 Value: "encoding"

**See Also**

### INDENT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INDENT: String
```

indent = "yes" | "no".
| --- | --- |

`indent`specifies whether the Transformer may add additional whitespace when outputting the result tree; the value must be`yes`or`no`. 

 Value: "indent"

**See Also**

### MEDIA_TYPE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_TYPE: String
```

media-type = string.

`media-type`specifies the media type (MIME content type) of the data that results from outputting the result tree. The`charset`parameter should not be specified explicitly; instead, when the top-level media type is`text`, a`charset`parameter should be added according to the character encoding actually used by the output method. 

 Value: "media-type"

**See Also**

### METHOD

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METHOD: String
```

method = "xml" | "html" | "text" | expanded name.
| --- | --- | --- | --- |

The value of the method property identifies the overall method that should be used for outputting the result tree. Other non-namespaced values may be used, such as "xhtml", but, if accepted, the handling of such values is implementation defined. If any of the method values are not accepted and are not namespace qualified, then [javax.xml.transform.Transformer#setOutputProperty](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperty(kotlin.String,%20kotlin.String))or [javax.xml.transform.Transformer#setOutputProperties](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer#setOutputProperties(java.util.Properties))will throw a [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#). 

 Value: "method"

**See Also**

### OMIT_XML_DECLARATION

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OMIT_XML_DECLARATION: String
```

omit-xml-declaration = "yes" | "no".
| --- | --- |

`omit-xml-declaration`specifies whether the XSLT processor should output an XML declaration; the value must be`yes`or`no`. 

 Value: "omit-xml-declaration"

**See Also**

### STANDALONE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDALONE: String
```

standalone = "yes" | "no".
| --- | --- |

`standalone`specifies whether the Transformer should output a standalone document declaration; the value must be`yes`or`no`. 

 Value: "standalone"

**See Also**

### VERSION

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERSION: String
```

version = nmtoken.

`version`specifies the version of the output method.

When the output method is "xml", the version value specifies the version of XML to be used for outputting the result tree. The default value for the xml output method is 1.0. When the output method is "html", the version value indicates the version of the HTML. The default value for the xml output method is 4.0, which specifies that the result should be output as HTML conforming to the HTML 4.0 Recommendation \[HTML\]. If the output method is "text", the version property is ignored. 

 Value: "version"

**See Also**
