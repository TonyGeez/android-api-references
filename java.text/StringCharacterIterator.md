# StringCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringCharacterIterator

```
class StringCharacterIterator : CharacterIterator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.text.StringCharacterIterator](../java/text/StringCharacterIterator.md) |

`StringCharacterIterator`implements the`CharacterIterator`protocol for a`String`. The`StringCharacterIterator`class iterates over the entire`String`.

## Summary

| Inherited constants ||
|---|---|
| From class [CharacterIterator](../java/text/CharacterIterator.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [DONE](../java/text/CharacterIterator.md) <br /> Constant that is returned when the iterator has reached either the end or the beginning of the text. The value is '\\\\uFFFF', the "not a character" value which should not occur in any valid Unicode string. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringCharacterIterator](../java/text/StringCharacterIterator.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an iterator with an initial index of 0. |
| [StringCharacterIterator](../java/text/StringCharacterIterator.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an iterator with the specified initial index. |
| [StringCharacterIterator](../java/text/StringCharacterIterator.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `begin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an iterator over the given range of the given string, with the index set at the specified position. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/text/StringCharacterIterator.md))`()` Creates a copy of this iterator. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [current](../java/text/StringCharacterIterator.md))`()` Implements CharacterIterator. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/text/StringCharacterIterator.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the equality of two StringCharacterIterator objects. |
| --- | --- |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [first](../java/text/StringCharacterIterator.md))`()` Implements CharacterIterator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBeginIndex](../java/text/StringCharacterIterator.md))`()` Implements CharacterIterator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEndIndex](../java/text/StringCharacterIterator.md))`()` Implements CharacterIterator. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](../java/text/StringCharacterIterator.md))`()` Implements CharacterIterator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/text/StringCharacterIterator.md))`()` Computes a hashcode for this iterator. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [last](../java/text/StringCharacterIterator.md))`()` Implements CharacterIterator. |
| --- | --- |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [next](../java/text/StringCharacterIterator.md))`()` Implements CharacterIterator. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [previous](../java/text/StringCharacterIterator.md))`()` Implements CharacterIterator. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [setIndex](../java/text/StringCharacterIterator.md))`(`p:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implements CharacterIterator. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](../java/text/StringCharacterIterator.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Reset this iterator to point to a new string. |

## Public constructors

### StringCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringCharacterIterator(text: String!)
```

Constructs an iterator with an initial index of 0.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the`String`to be iterated over |

### StringCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringCharacterIterator(
    text: String!, 
    pos: Int)
```

Constructs an iterator with the specified initial index.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The String to be iterated over |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Initial iterator position |

### StringCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringCharacterIterator(
    text: String!, 
    begin: Int, 
    end: Int, 
    pos: Int)
```

Constructs an iterator over the given range of the given string, with the index set at the specified position.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The String to be iterated over |
| `begin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the first character |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the character following the last character |
| --- | --- |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Initial iterator position |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clone(): Any
```

Creates a copy of this iterator.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | A copy of this |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### current

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun current(): Char
```

Implements CharacterIterator.current() for String.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character at the current position or DONE if the current position is off the end of the text. |

**See Also**

- [java.text.CharacterIterator#current](../java/text/CharacterIterator.md)) 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares the equality of two StringCharacterIterator objects.

| Parameters ||
|-------|---------------------------------------------------------|
| `obj` | the StringCharacterIterator object to be compared with. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given obj is the same as this StringCharacterIterator object; false otherwise. |

### first

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun first(): Char
```

Implements CharacterIterator.first() for String.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the first character in the text, or DONE if the text is empty |

**See Also**

- [java.text.CharacterIterator#first](../java/text/CharacterIterator.md)) 

### getBeginIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBeginIndex(): Int
```

Implements CharacterIterator.getBeginIndex() for String.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index at which the text begins. |

**See Also**

- [java.text.CharacterIterator#getBeginIndex](../java/text/CharacterIterator.md)) 

### getEndIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndIndex(): Int
```

Implements CharacterIterator.getEndIndex() for String.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index after the last character in the text |

**See Also**

- [java.text.CharacterIterator#getEndIndex](../java/text/CharacterIterator.md)) 

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIndex(): Int
```

Implements CharacterIterator.getIndex() for String.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current index. |

**See Also**

- [java.text.CharacterIterator#getIndex](../java/text/CharacterIterator.md)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Computes a hashcode for this iterator.

| Return ||
|----------------------------------------------------------------------------|-------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A hash code |

### last

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun last(): Char
```

Implements CharacterIterator.last() for String.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the last character in the text, or DONE if the text is empty |

**See Also**

- [java.text.CharacterIterator#last](../java/text/CharacterIterator.md)) 

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun next(): Char
```

Implements CharacterIterator.next() for String.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character at the new position or DONE if the new position is off the end of the text range. |

**See Also**

- [java.text.CharacterIterator#next](../java/text/CharacterIterator.md)) 

### previous

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun previous(): Char
```

Implements CharacterIterator.previous() for String.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character at the new position or DONE if the current position is equal to getBeginIndex(). |

**See Also**

- [java.text.CharacterIterator#previous](../java/text/CharacterIterator.md)) 

### setIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setIndex(p: Int): Char
```

Implements CharacterIterator.setIndex() for String.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | the position within the text. Valid values range from getBeginIndex() to getEndIndex(). An IllegalArgumentException is thrown if an invalid value is supplied. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character at the specified position or DONE if the specified position is equal to getEndIndex() |

**See Also**

- [java.text.CharacterIterator#setIndex](../java/text/CharacterIterator.md)) 

### setText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setText(text: String!): Unit
```

Reset this iterator to point to a new string. This package-visible method is used by other java.text classes that want to avoid allocating new StringCharacterIterator objects every time their setText method is called.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The String to be iterated over |
