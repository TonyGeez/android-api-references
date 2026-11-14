# XPathConstants

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathConstants

```
open class XPathConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.xpath.XPathConstants](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#) |

XPath constants.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DOM_OBJECT_MODEL](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#DOM_OBJECT_MODEL:kotlin.String) The URI for the DOM object model, "http://java. |

| Properties ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [QName](https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#)! | [BOOLEAN](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#BOOLEAN:javax.xml.namespace.QName) The XPath 1. |
| static [QName](https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#)! | [NODE](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#NODE:javax.xml.namespace.QName) The XPath 1. |
| static [QName](https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#)! | [NODESET](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#NODESET:javax.xml.namespace.QName) The XPath 1. |
| --- | --- |
| static [QName](https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#)! | [NUMBER](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#NUMBER:javax.xml.namespace.QName) The XPath 1. |
| static [QName](https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#)! | [STRING](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathConstants#STRING:javax.xml.namespace.QName) The XPath 1. |

## Constants

### DOM_OBJECT_MODEL

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOM_OBJECT_MODEL: String
```

The URI for the DOM object model, "http://java.sun.com/jaxp/xpath/dom". 

 Value: "http://java.sun.com/jaxp/xpath/dom"

## Properties

### BOOLEAN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BOOLEAN: QName!
```

The XPath 1.0 boolean data type.

Maps to Java [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html#). 

### NODE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NODE: QName!
```

The XPath 1.0 NodeSet data type.

Maps to Java [org.w3c.dom.Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html). 

### NODESET

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NODESET: QName!
```

The XPath 1.0 NodeSet data type.

Maps to Java [org.w3c.dom.NodeList](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node-list/index.html). 

### NUMBER

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMBER: QName!
```

The XPath 1.0 number data type.

Maps to Java [Double](https://developer.android.com/reference/kotlin/java/lang/Double.html#). 

### STRING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRING: QName!
```

The XPath 1.0 string data type.

Maps to Java [String](https://developer.android.com/reference/kotlin/java/lang/String.html#).
