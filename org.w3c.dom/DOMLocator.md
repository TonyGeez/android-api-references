# DOMLocator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMLocator

```
interface DOMLocator
```

| [org.w3c.dom.DOMLocator](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMLocator#) |

`DOMLocator`is an interface that describes a location (e.g. where an error occurred).

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getByteOffset](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMLocator#getByteOffset())`()` The byte offset into the input source this locator is pointing to or`-1`if there is no byte offset available. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMLocator#getColumnNumber())`()` The column number this locator is pointing to, or`-1`if there is no column number available. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMLocator#getLineNumber())`()` The line number this locator is pointing to, or`-1`if there is no column number available. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getRelatedNode](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMLocator#getRelatedNode())`()` The node this locator is pointing to, or`null`if no node is available. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUri](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMLocator#getUri())`()` The URI this locator is pointing to, or`null`if no URI is available. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUtf16Offset](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMLocator#getUtf16Offset())`()` The UTF-16, as defined in \[Unicode\] and Amendment 1 of \[ISO/IEC 10646\], offset into the input source this locator is pointing to or`-1`if there is no UTF-16 offset available. |

## Public methods

### getByteOffset

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getByteOffset(): Int
```

The byte offset into the input source this locator is pointing to or`-1`if there is no byte offset available. 

### getColumnNumber

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnNumber(): Int
```

The column number this locator is pointing to, or`-1`if there is no column number available. 

### getLineNumber

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineNumber(): Int
```

The line number this locator is pointing to, or`-1`if there is no column number available. 

### getRelatedNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRelatedNode(): Node!
```

The node this locator is pointing to, or`null`if no node is available. 

### getUri

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUri(): String!
```

The URI this locator is pointing to, or`null`if no URI is available. 

### getUtf16Offset

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUtf16Offset(): Int
```

The UTF-16, as defined in \[Unicode\] and Amendment 1 of \[ISO/IEC 10646\], offset into the input source this locator is pointing to or`-1`if there is no UTF-16 offset available.
