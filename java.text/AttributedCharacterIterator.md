# AttributedCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttributedCharacterIterator

```
interface AttributedCharacterIterator : CharacterIterator
```

| [java.text.AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md) |

An`AttributedCharacterIterator`allows iteration through both text and related attribute information.

An attribute is a key/value pair, identified by the key. No two attributes on a given character can have the same key.

The values for an attribute are immutable, or must not be mutated by clients or storage. They are always passed by reference, and not cloned.

A*run with respect to an attribute*is a maximum text range for which:

- the attribute is undefined or`null`for the entire range, or
- the attribute value is defined and has the same non-`null`value for the entire range.

A*run with respect to a set of attributes*is a maximum text range for which this condition is met for each member attribute.

When getting a run with no explicit attributes specified (i.e., calling [getRunStart()](../java/text/AttributedCharacterIterator.md))and [getRunLimit()](../java/text/AttributedCharacterIterator.md))), any contiguous text segments having the same attributes (the same set of attribute/value pairs) are treated as separate runs if the attributes have been given to those text segments separately.

The returned indexes are limited to the range of the iterator.

The returned attribute information is limited to runs that contain the current character.

Attribute keys are instances of [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md) and its subclasses, such as [java.awt.font.TextAttribute](../java/awt/font/TextAttribute.md).

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Attribute](../java/text/AttributedCharacterIterator.Attribute.md) Defines attribute keys that are used to identify text attributes. |

| Inherited constants ||
|---|---|
| From class [CharacterIterator](../java/text/CharacterIterator.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [DONE](../java/text/CharacterIterator.md) <br /> Constant that is returned when the iterator has reached either the end or the beginning of the text. The value is '\\\\uFFFF', the "not a character" value which should not occur in any valid Unicode string. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!\>! | [getAllAttributeKeys](../java/text/AttributedCharacterIterator.md))`()` Returns the keys of all attributes defined on the iterator's text range. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](../java/text/AttributedCharacterIterator.md))`(`attribute:` ` [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!`)` Returns the value of the named`attribute`for the current character. |
| abstract [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getAttributes](../java/text/AttributedCharacterIterator.md))`()` Returns a map with the attributes defined on the current character. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunLimit](../java/text/AttributedCharacterIterator.md))`()` Returns the index of the first character following the run with respect to all attributes containing the current character. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunLimit](../java/text/AttributedCharacterIterator.md))`(`attribute:` ` [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!`)` Returns the index of the first character following the run with respect to the given`attribute`containing the current character. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunLimit](../java/text/AttributedCharacterIterator.md))`(`attributes:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!>!`)` Returns the index of the first character following the run with respect to the given`attributes`containing the current character. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunStart](../java/text/AttributedCharacterIterator.md))`()` Returns the index of the first character of the run with respect to all attributes containing the current character. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunStart](../java/text/AttributedCharacterIterator.md))`(`attribute:` ` [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!`)` Returns the index of the first character of the run with respect to the given`attribute`containing the current character. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunStart](../java/text/AttributedCharacterIterator.md))`(`attributes:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!>!`)` Returns the index of the first character of the run with respect to the given`attributes`containing the current character. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [CharacterIterator](../java/text/CharacterIterator.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/text/CharacterIterator.md))`()` <br /> Create a copy of this iterator <br /> | | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [current](../java/text/CharacterIterator.md))`()` <br /> Gets the character at the current position (as returned by getIndex()). <br /> | | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [first](../java/text/CharacterIterator.md))`()` <br /> Sets the position to getBeginIndex() and returns the character at that position. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBeginIndex](../java/text/CharacterIterator.md))`()` <br /> Returns the start index of the text. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEndIndex](../java/text/CharacterIterator.md))`()` <br /> Returns the end index of the text. This index is the index of the first character following the end of the text. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](../java/text/CharacterIterator.md))`()` <br /> Returns the current index. <br /> | | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [last](../java/text/CharacterIterator.md))`()` <br /> Sets the position to getEndIndex()-1 (getEndIndex() if the text is empty) and returns the character at that position. <br /> | | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [next](../java/text/CharacterIterator.md))`()` <br /> Increments the iterator's index by one and returns the character at the new index. If the resulting index is greater or equal to getEndIndex(), the current index is reset to getEndIndex() and a value of DONE is returned. <br /> | | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [previous](../java/text/CharacterIterator.md))`()` <br /> Decrements the iterator's index by one and returns the character at the new index. If the current index is getBeginIndex(), the index remains at getBeginIndex() and a value of DONE is returned. <br /> | | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [setIndex](../java/text/CharacterIterator.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the position to the specified position in the text and returns that character. <br /> | ||

## Public methods

### getAllAttributeKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAllAttributeKeys(): MutableSet<AttributedCharacterIterator.Attribute!>!
```

Returns the keys of all attributes defined on the iterator's text range. The set is empty if no attributes are defined.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!>! | the keys of all attributes |

### getAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttribute(attribute: AttributedCharacterIterator.Attribute!): Any!
```

Returns the value of the named`attribute`for the current character. Returns`null`if the`attribute`is not defined.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attribute` | [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!:the desired attribute |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the value of the named`attribute`or`null` |

### getAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributes(): MutableMap<AttributedCharacterIterator.Attribute!, Any!>!
```

Returns a map with the attributes defined on the current character.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | a map with the attributes defined on the current character |

### getRunLimit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRunLimit(): Int
```

Returns the index of the first character following the run with respect to all attributes containing the current character.

Any contiguous text segments having the same attributes (the same set of attribute/value pairs) are treated as separate runs if the attributes have been given to those text segments separately.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first character following the run |

### getRunLimit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRunLimit(attribute: AttributedCharacterIterator.Attribute!): Int
```

Returns the index of the first character following the run with respect to the given`attribute`containing the current character.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attribute` | [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!:the desired attribute |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first character following the run |

### getRunLimit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRunLimit(attributes: MutableSet<out AttributedCharacterIterator.Attribute!>!): Int
```

Returns the index of the first character following the run with respect to the given`attributes`containing the current character.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!\>!:a set of the desired attributes |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first character following the run |

### getRunStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRunStart(): Int
```

Returns the index of the first character of the run with respect to all attributes containing the current character.

Any contiguous text segments having the same attributes (the same set of attribute/value pairs) are treated as separate runs if the attributes have been given to those text segments separately.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first character of the run |

### getRunStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRunStart(attribute: AttributedCharacterIterator.Attribute!): Int
```

Returns the index of the first character of the run with respect to the given`attribute`containing the current character.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attribute` | [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!:the desired attribute. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first character of the run |

### getRunStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRunStart(attributes: MutableSet<out AttributedCharacterIterator.Attribute!>!): Int
```

Returns the index of the first character of the run with respect to the given`attributes`containing the current character.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)!\>!:a set of the desired attributes. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first character of the run |
