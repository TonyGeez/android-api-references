# StringCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringCharacterIterator

```
class StringCharacterIterator : CharacterIterator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.text.StringCharacterIterator](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#) |

`StringCharacterIterator`implements the`CharacterIterator`protocol for a`String`. The`StringCharacterIterator`class iterates over the entire`String`.

## Summary

| Inherited constants ||
|---|---|
| From class [CharacterIterator](https://developer.android.com/reference/kotlin/java/text/CharacterIterator) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [DONE](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#DONE:kotlin.Char) <br /> Constant that is returned when the iterator has reached either the end or the beginning of the text. The value is '\\\\uFFFF', the "not a character" value which should not occur in any valid Unicode string. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringCharacterIterator](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#StringCharacterIterator(kotlin.String))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an iterator with an initial index of 0. |
| [StringCharacterIterator](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#StringCharacterIterator(kotlin.String,%20kotlin.Int))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an iterator with the specified initial index. |
| [StringCharacterIterator](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#StringCharacterIterator(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `begin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an iterator over the given range of the given string, with the index set at the specified position. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#clone())`()` Creates a copy of this iterator. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [current](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#current())`()` Implements CharacterIterator. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the equality of two StringCharacterIterator objects. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [first](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#first())`()` Implements CharacterIterator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBeginIndex](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#getBeginIndex())`()` Implements CharacterIterator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEndIndex](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#getEndIndex())`()` Implements CharacterIterator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#getIndex())`()` Implements CharacterIterator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#hashCode())`()` Computes a hashcode for this iterator. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [last](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#last())`()` Implements CharacterIterator. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [next](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#next())`()` Implements CharacterIterator. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [previous](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#previous())`()` Implements CharacterIterator. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [setIndex](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#setIndex(kotlin.Int))`(`p:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implements CharacterIterator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator#setText(kotlin.String))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Reset this iterator to point to a new string. |

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

- [java.text.CharacterIterator#current](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#current()) 

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

- [java.text.CharacterIterator#first](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#first()) 

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

- [java.text.CharacterIterator#getBeginIndex](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#getBeginIndex()) 

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

- [java.text.CharacterIterator#getEndIndex](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#getEndIndex()) 

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

- [java.text.CharacterIterator#getIndex](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#getIndex()) 

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

- [java.text.CharacterIterator#last](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#last()) 

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

- [java.text.CharacterIterator#next](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#next()) 

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

- [java.text.CharacterIterator#previous](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#previous()) 

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

- [java.text.CharacterIterator#setIndex](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#setIndex(kotlin.Int)) 

### setText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setText(text: String!): Unit
```

Reset this iterator to point to a new string. This package-visible method is used by other java.text classes that want to avoid allocating new StringCharacterIterator objects every time their setText method is called.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The String to be iterated over |
