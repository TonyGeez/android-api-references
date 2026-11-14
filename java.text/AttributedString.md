# AttributedString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttributedString

```
open class AttributedString
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.text.AttributedString](https://developer.android.com/reference/kotlin/java/text/AttributedString#) |

An AttributedString holds text and related attribute information. It may be used as the actual data storage in some cases where a text reader wants to access attributed text through the AttributedCharacterIterator interface.

An attribute is a key/value pair, identified by the key. No two attributes on a given character can have the same key.

The values for an attribute are immutable, or must not be mutated by clients or storage. They are always passed by reference, and not cloned.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AttributedString](https://developer.android.com/reference/kotlin/java/text/AttributedString#AttributedString(kotlin.String))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an AttributedString instance with the given text. |
| [AttributedString](https://developer.android.com/reference/kotlin/java/text/AttributedString#AttributedString(kotlin.String,%20kotlin.collections.MutableMap))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<out` ` [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!,` `*>!`)` Constructs an AttributedString instance with the given text and attributes. |
| [AttributedString](https://developer.android.com/reference/kotlin/java/text/AttributedString#AttributedString(java.text.AttributedCharacterIterator))`(`text:` ` [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)!`)` Constructs an AttributedString instance with the given attributed text represented by AttributedCharacterIterator. |
| [AttributedString](https://developer.android.com/reference/kotlin/java/text/AttributedString#AttributedString(java.text.AttributedCharacterIterator,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)!`, `beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an AttributedString instance with the subrange of the given attributed text represented by AttributedCharacterIterator. |
| [AttributedString](https://developer.android.com/reference/kotlin/java/text/AttributedString#AttributedString(java.text.AttributedCharacterIterator,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array))`(`text:` ` [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)!`, `beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!>!`)` Constructs an AttributedString instance with the subrange of the given attributed text represented by AttributedCharacterIterator. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAttribute](https://developer.android.com/reference/kotlin/java/text/AttributedString#addAttribute(java.text.AttributedCharacterIterator.Attribute,%20kotlin.Any))`(`attribute:` ` [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Adds an attribute to the entire string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAttribute](https://developer.android.com/reference/kotlin/java/text/AttributedString#addAttribute(java.text.AttributedCharacterIterator.Attribute,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int))`(`attribute:` ` [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds an attribute to a subrange of the string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAttributes](https://developer.android.com/reference/kotlin/java/text/AttributedString#addAttributes(kotlin.collections.MutableMap,%20kotlin.Int,%20kotlin.Int))`(`attributes:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<out` ` [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!,` `*>!`, `beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a set of attributes to a subrange of the string. |
| open [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | [getIterator](https://developer.android.com/reference/kotlin/java/text/AttributedString#getIterator())`()` Creates an AttributedCharacterIterator instance that provides access to the entire contents of this string. |
| open [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | [getIterator](https://developer.android.com/reference/kotlin/java/text/AttributedString#getIterator(kotlin.Array))`(`attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!>!`)` Creates an AttributedCharacterIterator instance that provides access to selected contents of this string. |
| open [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | [getIterator](https://developer.android.com/reference/kotlin/java/text/AttributedString#getIterator(kotlin.Array,%20kotlin.Int,%20kotlin.Int))`(`attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!>!`, `beginIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an AttributedCharacterIterator instance that provides access to selected contents of this string. |

## Public constructors

### AttributedString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributedString(text: String!)
```

Constructs an AttributedString instance with the given text.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The text for this attributed string. |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`text`is null. |

### AttributedString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributedString(
    text: String!, 
    attributes: MutableMap<out AttributedCharacterIterator.Attribute!, *>!)
```

Constructs an AttributedString instance with the given text and attributes.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The text for this attributed string. |
| `attributes` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<out [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!,\*\>!:The attributes that apply to the entire string. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`text`or`attributes`is null. |
| `java.lang.IllegalArgumentException` | if the text has length 0 and the attributes parameter is not an empty Map (attributes cannot be applied to a 0-length range). |

### AttributedString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributedString(text: AttributedCharacterIterator!)
```

Constructs an AttributedString instance with the given attributed text represented by AttributedCharacterIterator.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)!:The text for this attributed string. |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`text`is null. |

### AttributedString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributedString(
    text: AttributedCharacterIterator!, 
    beginIndex: Int, 
    endIndex: Int)
```

Constructs an AttributedString instance with the subrange of the given attributed text represented by AttributedCharacterIterator. If the given range produces an empty text, all attributes will be discarded. Note that any attributes wrapped by an Annotation object are discarded for a subrange of the original attribute range.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)!:The text for this attributed string. |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the first character of the range. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the character following the last character of the range. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`text`is null. |
| `java.lang.IllegalArgumentException` | if the subrange given by beginIndex and endIndex is out of the text range. |

**See Also**

- [java.text.Annotation](https://developer.android.com/reference/kotlin/java/text/Annotation) 

### AttributedString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AttributedString(
    text: AttributedCharacterIterator!, 
    beginIndex: Int, 
    endIndex: Int, 
    attributes: Array<AttributedCharacterIterator.Attribute!>!)
```

Constructs an AttributedString instance with the subrange of the given attributed text represented by AttributedCharacterIterator. Only attributes that match the given attributes will be incorporated into the instance. If the given range produces an empty text, all attributes will be discarded. Note that any attributes wrapped by an Annotation object are discarded for a subrange of the original attribute range.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)!:The text for this attributed string. |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the first character of the range. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the character following the last character of the range. |
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!\>!:Specifies attributes to be extracted from the text. If null is specified, all available attributes will be used. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`text`is null. |
| `java.lang.IllegalArgumentException` | if the subrange given by beginIndex and endIndex is out of the text range. |

**See Also**

- [java.text.Annotation](https://developer.android.com/reference/kotlin/java/text/Annotation)

## Public methods

### addAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAttribute(
    attribute: AttributedCharacterIterator.Attribute!, 
    value: Any!
): Unit
```

Adds an attribute to the entire string.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attribute` | [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!:the attribute key |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the value of the attribute; may be null |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`attribute`is null. |
| `java.lang.IllegalArgumentException` | if the AttributedString has length 0 (attributes cannot be applied to a 0-length range). |

### addAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAttribute(
    attribute: AttributedCharacterIterator.Attribute!, 
    value: Any!, 
    beginIndex: Int, 
    endIndex: Int
): Unit
```

Adds an attribute to a subrange of the string.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attribute` | [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!:the attribute key |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The value of the attribute. May be null. |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the first character of the range. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the character following the last character of the range. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`attribute`is null. |
| `java.lang.IllegalArgumentException` | if beginIndex is less than 0, endIndex is greater than the length of the string, or beginIndex and endIndex together don't define a non-empty subrange of the string. |

### addAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAttributes(
    attributes: MutableMap<out AttributedCharacterIterator.Attribute!, *>!, 
    beginIndex: Int, 
    endIndex: Int
): Unit
```

Adds a set of attributes to a subrange of the string.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<out [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!,\*\>!:The attributes to be added to the string. |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the first character of the range. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the character following the last character of the range. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`attributes`is null. |
| `java.lang.IllegalArgumentException` | if beginIndex is less than 0, endIndex is greater than the length of the string, or beginIndex and endIndex together don't define a non-empty subrange of the string and the attributes parameter is not an empty Map. |

### getIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIterator(): AttributedCharacterIterator!
```

Creates an AttributedCharacterIterator instance that provides access to the entire contents of this string.

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | An iterator providing access to the text and its attributes. |

### getIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIterator(attributes: Array<AttributedCharacterIterator.Attribute!>!): AttributedCharacterIterator!
```

Creates an AttributedCharacterIterator instance that provides access to selected contents of this string. Information about attributes not listed in attributes that the implementor may have need not be made accessible through the iterator. If the list is null, all available attribute information should be made accessible.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!\>!:a list of attributes that the client is interested in |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | an iterator providing access to the entire text and its selected attributes |

### getIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIterator(
    attributes: Array<AttributedCharacterIterator.Attribute!>!, 
    beginIndex: Int, 
    endIndex: Int
): AttributedCharacterIterator!
```

Creates an AttributedCharacterIterator instance that provides access to selected contents of this string. Information about attributes not listed in attributes that the implementor may have need not be made accessible through the iterator. If the list is null, all available attribute information should be made accessible.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute)!\>!:a list of attributes that the client is interested in |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the first character |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the character following the last character |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | an iterator providing access to the text and its attributes |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if beginIndex is less than 0, endIndex is greater than the length of the string, or beginIndex is greater than endIndex. |
