# XPathConstants

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathConstants

```
open class XPathConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.xpath.XPathConstants](XPathConstants.md) |

XPath constants.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DOM_OBJECT_MODEL](XPathConstants.md) The URI for the DOM object model, "http://java. |

| Properties ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [QName](../javax.xml.namespace/QName.md)! | [BOOLEAN](XPathConstants.md) The XPath 1. |
| static [QName](../javax.xml.namespace/QName.md)! | [NODE](XPathConstants.md) The XPath 1. |
| static [QName](../javax.xml.namespace/QName.md)! | [NODESET](XPathConstants.md) The XPath 1. |
| --- | --- |
| static [QName](../javax.xml.namespace/QName.md)! | [NUMBER](XPathConstants.md) The XPath 1. |
| static [QName](../javax.xml.namespace/QName.md)! | [STRING](XPathConstants.md) The XPath 1. |

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

Maps to Java [Boolean](../java.lang/Boolean.md). 

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

Maps to Java [Double](../java.lang/Double.md). 

### STRING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRING: QName!
```

The XPath 1.0 string data type.

Maps to Java [String](../java.lang/String.md).
