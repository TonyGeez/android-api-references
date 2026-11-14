# DOMImplementationList

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMImplementationList

```
interface DOMImplementationList
```

| [org.w3c.dom.DOMImplementationList](../org/w3c/dom/DOMImplementationList.md) |

The`DOMImplementationList`interface provides the abstraction of an ordered collection of DOM implementations, without defining or constraining how this collection is implemented. The items in the`DOMImplementationList`are accessible via an integral index, starting from 0.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](../org/w3c/dom/DOMImplementationList.md))`()` The number of`DOMImplementation`s in the list. |
| abstract [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html)! | [item](../org/w3c/dom/DOMImplementationList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the`index`th item in the collection. |

## Public methods

### getLength

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLength(): Int
```

The number of`DOMImplementation`s in the list. The range of valid child node indices is 0 to`length-1`inclusive. 

### item

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun item(index: Int): DOMImplementation!
```

Returns the`index`th item in the collection. If`index`is greater than or equal to the number of`DOMImplementation`s in the list, this returns`null`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index into the collection. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html)! | The`DOMImplementation`at the`index`th position in the`DOMImplementationList`, or`null`if that is not a valid index. |
