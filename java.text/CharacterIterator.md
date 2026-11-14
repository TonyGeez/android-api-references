# CharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharacterIterator

```
interface CharacterIterator : Cloneable
```

| [java.text.CharacterIterator](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#) |

| Known Direct Subclasses [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator), [StringCharacterIterator](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator) |---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------| | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator) | An`AttributedCharacterIterator`allows iteration through both text and related attribute information. | | [StringCharacterIterator](https://developer.android.com/reference/kotlin/java/text/StringCharacterIterator) | `StringCharacterIterator`implements the`CharacterIterator`protocol for a`String`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This interface defines a protocol for bidirectional iteration over text. The iterator iterates over a bounded sequence of characters. Characters are indexed with values beginning with the value returned by getBeginIndex() and continuing through the value returned by getEndIndex()-1.

Iterators maintain a current character index, whose valid range is from getBeginIndex() to getEndIndex(); the value getEndIndex() is included to allow handling of zero-length text ranges and for historical reasons. The current index can be retrieved by calling getIndex() and set directly by calling setIndex(), first(), and last().

The methods previous() and next() are used for iteration. They return DONE if they would move outside the range from getBeginIndex() to getEndIndex() -1, signaling that the iterator has reached the end of the sequence. DONE is also returned by other methods to indicate that the current index is outside this range.

Examples:

Traverse the text from start to finish 

```kotlin
<code>public void traverseForward(CharacterIterator iter) {
      for(char c = iter.first(); c != CharacterIterator.DONE; c = iter.next()) {
          processChar(c);
      }
  }
  </code>
```
Traverse the text backwards, from end to start 

```kotlin
<code>public void traverseBackward(CharacterIterator iter) {
      for(char c = iter.last(); c != CharacterIterator.DONE; c = iter.previous()) {
          processChar(c);
      }
  }
  </code>
```
Traverse both forward and backward from a given position in the text. Calls to notBoundary() in this example represents some additional stopping criteria. 

```kotlin
<code>public void traverseOut(CharacterIterator iter, int pos) {
      for (char c = iter.setIndex(pos);
               c != CharacterIterator.DONE &amp;&amp; notBoundary(c);
               c = iter.next()) {
      }
      int end = iter.getIndex();
      for (char c = iter.setIndex(pos);
              c != CharacterIterator.DONE &amp;&amp; notBoundary(c);
              c = iter.previous()) {
      }
      int start = iter.getIndex();
      processSection(start, end);
  }
  </code>
```

## Summary

| Constants ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [DONE](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#DONE:kotlin.Char) Constant that is returned when the iterator has reached either the end or the beginning of the text. |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#clone())`()` Create a copy of this iterator |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [current](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#current())`()` Gets the character at the current position (as returned by getIndex()). |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [first](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#first())`()` Sets the position to getBeginIndex() and returns the character at that position. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBeginIndex](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#getBeginIndex())`()` Returns the start index of the text. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEndIndex](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#getEndIndex())`()` Returns the end index of the text. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#getIndex())`()` Returns the current index. |
| --- | --- |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [last](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#last())`()` Sets the position to getEndIndex()-1 (getEndIndex() if the text is empty) and returns the character at that position. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [next](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#next())`()` Increments the iterator's index by one and returns the character at the new index. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [previous](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#previous())`()` Decrements the iterator's index by one and returns the character at the new index. |
| --- | --- |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [setIndex](https://developer.android.com/reference/kotlin/java/text/CharacterIterator#setIndex(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the position to the specified position in the text and returns that character. |

## Constants

### DONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DONE: Char
```

Constant that is returned when the iterator has reached either the end or the beginning of the text. The value is '\\\\uFFFF', the "not a character" value which should not occur in any valid Unicode string. 

 Value: '\uffff'

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clone(): Any
```

Create a copy of this iterator

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | A copy of this |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### current

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun current(): Char
```

Gets the character at the current position (as returned by getIndex()).

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character at the current position or DONE if the current position is off the end of the text. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/CharacterIterator#getIndex()> 

### first

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun first(): Char
```

Sets the position to getBeginIndex() and returns the character at that position.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the first character in the text, or DONE if the text is empty |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/CharacterIterator#getBeginIndex()> 

### getBeginIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBeginIndex(): Int
```

Returns the start index of the text.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index at which the text begins. |

### getEndIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEndIndex(): Int
```

Returns the end index of the text. This index is the index of the first character following the end of the text.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index after the last character in the text |

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIndex(): Int
```

Returns the current index.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current index. |

### last

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun last(): Char
```

Sets the position to getEndIndex()-1 (getEndIndex() if the text is empty) and returns the character at that position.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the last character in the text, or DONE if the text is empty |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/CharacterIterator#getEndIndex()> 

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(): Char
```

Increments the iterator's index by one and returns the character at the new index. If the resulting index is greater or equal to getEndIndex(), the current index is reset to getEndIndex() and a value of DONE is returned.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character at the new position or DONE if the new position is off the end of the text range. |

### previous

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun previous(): Char
```

Decrements the iterator's index by one and returns the character at the new index. If the current index is getBeginIndex(), the index remains at getBeginIndex() and a value of DONE is returned.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character at the new position or DONE if the current position is equal to getBeginIndex(). |

### setIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIndex(position: Int): Char
```

Sets the position to the specified position in the text and returns that character.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position within the text. Valid values range from getBeginIndex() to getEndIndex(). An IllegalArgumentException is thrown if an invalid value is supplied. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character at the specified position or DONE if the specified position is equal to getEndIndex() |
