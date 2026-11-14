# NodeList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NodeList

```
interface NodeList
```

| [org.w3c.dom.NodeList](https://developer.android.com/reference/kotlin/org/w3c/dom/NodeList#) |

The`NodeList`interface provides the abstraction of an ordered collection of nodes, without defining or constraining how this collection is implemented.`NodeList`objects in the DOM are live.

The items in the`NodeList`are accessible via an integral index, starting from 0.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](https://developer.android.com/reference/kotlin/org/w3c/dom/NodeList#getLength())`()` The number of nodes in the list. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [item](https://developer.android.com/reference/kotlin/org/w3c/dom/NodeList#item(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the`index`th item in the collection. |

## Public methods

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLength(): Int
```

The number of nodes in the list. The range of valid child node indices is 0 to`length-1`inclusive. 

### item

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun item(index: Int): Node!
```

Returns the`index`th item in the collection. If`index`is greater than or equal to the number of nodes in the list, this returns`null`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index into the collection. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node at the`index`th position in the`NodeList`, or`null`if that is not a valid index. |
