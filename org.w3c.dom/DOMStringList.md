# DOMStringList

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMStringList

```
interface DOMStringList
```

| [org.w3c.dom.DOMStringList](../org/w3c/dom/DOMStringList.md) |

The`DOMStringList`interface provides the abstraction of an ordered collection of`DOMString`values, without defining or constraining how this collection is implemented. The items in the`DOMStringList`are accessible via an integral index, starting from 0.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../org/w3c/dom/DOMStringList.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Test if a string is part of this`DOMStringList`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](../org/w3c/dom/DOMStringList.md))`()` The number of`DOMString`s in the list. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [item](../org/w3c/dom/DOMStringList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the`index`th item in the collection. |
| --- | --- |

## Public methods

### contains

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun contains(str: String!): Boolean
```

Test if a string is part of this`DOMStringList`.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The string to look for. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the string has been found,`false`otherwise. |

### getLength

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLength(): Int
```

The number of`DOMString`s in the list. The range of valid child node indices is 0 to`length-1`inclusive. 

### item

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun item(index: Int): String!
```

Returns the`index`th item in the collection. If`index`is greater than or equal to the number of`DOMString`s in the list, this returns`null`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index into the collection. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The`DOMString`at the`index`th position in the`DOMStringList`, or`null`if that is not a valid index. |
