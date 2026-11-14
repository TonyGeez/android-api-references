# DOMImplementationSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMImplementationSource

```
interface DOMImplementationSource
```

| [org.w3c.dom.DOMImplementationSource](../org/w3c/dom/DOMImplementationSource.md) |

This interface permits a DOM implementer to supply one or more implementations, based upon requested features and versions, as specified in . Each implemented`DOMImplementationSource`object is listed in the binding-specific list of available sources so that its`DOMImplementation`objects are made available.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html)! | [getDOMImplementation](../org/w3c/dom/DOMImplementationSource.md))`(`features:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` A method to request the first DOM implementation that supports the specified features. |
| abstract [DOMImplementationList](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation-list/index.html)! | [getDOMImplementationList](../org/w3c/dom/DOMImplementationSource.md))`(`features:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` A method to request a list of DOM implementations that support the specified features and versions, as specified in . |

## Public methods

### getDOMImplementation

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDOMImplementation(features: String!): DOMImplementation!
```

A method to request the first DOM implementation that supports the specified features.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `features` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string that specifies which features and versions are required. This is a space separated list in which each feature is specified by its name optionally followed by a space and a version number. This method returns the first item of the list returned by`getDOMImplementationList`. As an example, the string`"XML 3.0 Traversal +Events 2.0"`will request a DOM implementation that supports the module "XML" for its 3.0 version, a module that support of the "Traversal" module for any version, and the module "Events" for its 2.0 version. The module "Events" must be accessible using the method`Node.getFeature()`and`DOMImplementation.getFeature()`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html)! | The first DOM implementation that support the desired features, or`null`if this source has none. |

### getDOMImplementationList

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDOMImplementationList(features: String!): DOMImplementationList!
```

A method to request a list of DOM implementations that support the specified features and versions, as specified in .

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `features` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string that specifies which features and versions are required. This is a space separated list in which each feature is specified by its name optionally followed by a space and a version number. This is something like: "XML 3.0 Traversal +Events 2.0" |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [DOMImplementationList](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation-list/index.html)! | A list of DOM implementations that support the desired features. |
